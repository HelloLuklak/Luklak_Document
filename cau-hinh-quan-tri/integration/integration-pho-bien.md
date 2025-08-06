# Integration phổ biến

## Google Sheet -> Luklak

### Tạo Đầu việc trong Luklak khi có dòng mới trên Google Sheet \[Add Row]

{% hint style="info" %}
Hướng dẫn đẩy dữ liệu từ Google Sheet về Luklak thông qua App Script. Ứng dụng phổ biến: đẩy thông tin khách hàng đăng kí.
{% endhint %}

#### Thiết lập trên App scripts

{% @guidejar/embed guideId="3665f37e-42fb-4b57-af94-cdfcf92eff42" type="1" controls="on" url="https://www.guidejar.com/embed/3665f37e-42fb-4b57-af94-cdfcf92eff42?type=1&controls=on" %}

<details>

<summary>Luồng thiết lập</summary>

```javascript
function processAndPushSingleRow() {
  const sheet = SpreadsheetApp.getActiveSpreadsheet().getActiveSheet();
  const data = sheet.getDataRange().getValues();
  const headers = data[0]; // Tiêu đề cột

  const url = "https://idealer.luklak.com/api/org/newspaceconcept/hooks/P7t5dL-x-UoZQ5m0gkyprlR0y7Sv3Kzr_07fnr3ThFY"; // Thay link webhook được lấy trên Luklak vào đây


  // Map tiêu đề cột sang key của API
  const columnMapping = {
    "Số điện thoại cá nhân": "sdt",
    "Mã khách hàng": "makh",
    "Số CCCD": "cccd",
    "Khối": "khoi",
    "Họ và tên": "hoten",
    "Cấp bậc chức danh": "capbac",
    "Dân tộc": "dantoc",
    "Địa chỉ liên hệ (Địa chỉ ở Hà Nội)": "diachi",
    "Loại hợp đồng": "loaihd",
    "Nơi sinh": "noisinh",
    "Hình thức đào tạo": "trinhdo",
    "Chức danh": "chucdanh",
    "Giới tính": "gioitinh",
    "Ngày sinh": "ngaysinh",
    "Phòng/Ban/Chi nhánh": "phongban",
    "Ngày vào làm việc": "ngayvaolam",
    "Email cá nhân": "emailcanhan",
    "Email công ty": "emailcongty",
    "Tình trạng hôn nhân": "tinhtranghonnhan",
    "Nguyên quán": "noisinh",
    "Tỉnh/TP": "thuongtru",
  };


// Xử lý mã hóa dữ liệu 
  for (let i = 1; i < data.length; i++) { // Bắt đầu từ dòng thứ 2
    const row = data[i];
    const processedRow = {};

    headers.forEach((header, index) => {
      const key = columnMapping[header];
      const cellValue = row[index];

      if (key) {
        // Xử lý chuẩn hóa dữ liệu
        if (["capbac", "trinhdo", "tinhtranghonnhan"].includes(key)) { // Sử dụng với các cột dữ liệu trường sổ xuống chọn 1
          processedRow[key] = normalizeText(cellValue);
        } else if (key === "ngaysinh" || key === "ngayvaolam") { // Sử dụng với các trường mã hóa thời gian cho đúng định dạng
          processedRow[key] = formatDate(cellValue);
        } else if (key === "gioitinh") {
          processedRow[key] = normalizeText(cellValue);
        } else {
          processedRow[key] = cellValue || ""; // Điền giá trị hoặc để trống
        }
      }
    });

    // Gửi dữ liệu đã xử lý đến API
    const options = {
      method: "POST",
      contentType: "application/json",
      payload: JSON.stringify(processedRow),
    };

    try {
      const response = UrlFetchApp.fetch(url, options);
      Logger.log(`Dòng ${i + 1}: ${response.getContentText()}`); // Log dòng hiện tại
    } catch (error) {
      Logger.log(`Lỗi dòng ${i + 1}: ${error}`);
    }

    // Tạm dừng 1 giây trước khi xử lý dòng tiếp theo
    Utilities.sleep(1000);
  }
}

// Hàm chuẩn hóa văn bản: Loại bỏ dấu, thay khoảng trắng bằng dấu gạch ngang
function normalizeText(text) {
  if (!text) return "";
  const accentsMap = [
    { base: "a", regex: /[àáạảãâầấậẩẫăằắặẳẵ]/g },
    { base: "e", regex: /[èéẹẻẽêềếệểễ]/g },
    { base: "i", regex: /[ìíịỉĩ]/g },
    { base: "o", regex: /[òóọỏõôồốộổỗơờớợởỡ]/g },
    { base: "u", regex: /[ùúụủũưừứựửữ]/g },
    { base: "y", regex: /[ỳýỵỷỹ]/g },
    { base: "d", regex: /[đ]/g },
  ];

  text = text.toLowerCase().trim();
  accentsMap.forEach(({ base, regex }) => {
    text = text.replace(regex, base);
  });

  return text.replace(/\s+/g, "_");
}

// Hàm chuyển định dạng ngày từ dd/mm/yyyy sang yyyy-mm-dd
function formatDate(date) {
  if (!date) return "";
  if (typeof date === "string" && date.includes("/")) {
    const parts = date.split("/");
    return `${parts[2]}-${parts[1].padStart(2, "0")}-${parts[0].padStart(2, "0")}`;
  }
  if (Object.prototype.toString.call(date) === "[object Date]") {
    return Utilities.formatDate(date, "GMT+7", "yyyy-MM-dd");
  }
  return "";
}

```

</details>

#### Lấy Webhook URL từ Luklak

{% @guidejar/embed guideId="e6ef5720-dbe0-495d-961d-c6662c249f4c" type="1" controls="on" url="https://www.guidejar.com/embed/e6ef5720-dbe0-495d-961d-c6662c249f4c?type=1&controls=on" %}

### Cập nhật Đầu việc (Object) khi có thay đổi trên Google Sheet \[Update row]

{% hint style="info" %}
### Tình huống ứng dụng

Tính năng này đặc biệt hữu ích trong các trường hợp:

* Cập nhật giá sản phẩm từ bảng tính sang hệ thống
* Cập nhật trạng thái dự án từ báo cáo Excel
* Nhập nhanh thông tin khách hàng từ sheet thu thập dữ liệu
* Điều chỉnh thông tin nhân sự hoặc phân công từ xa
{% endhint %}

{% @guidejar/embed guideId="92b15122-2912-4a8c-b577-3b7e9de0823a" type="1" controls="on" url="https://www.guidejar.com/embed/92b15122-2912-4a8c-b577-3b7e9de0823a?type=1&controls=on" %}

<details>

<summary>Luồng thiết lập</summary>

1. Người dùng cập nhật thông tin trong Google Sheet
2. Trigger từ Apps Script phát hiện sự thay đổi

{% code overflow="wrap" %}
```javascript
// Đoạn code Appscript để lắng nghe thay đổi -> Gửi về Luklak

function handleEdit(e) {
  try {
    const sheet = e.range.getSheet();
    const row = e.range.getRow();


    if (row === 1) return;


    const headers = sheet.getRange(1, 1, 1, sheet.getLastColumn()).getValues()[0];
    const rowData = sheet.getRange(row, 1, 1, headers.length).getValues()[0];


    const data = {};
    headers.forEach((header, index) => {
      data[header.trim()] = rowData[index];
    });


    const issueKey = data["Mã"]; // Mã là tên cột được đặt ở sheet
    if (!issueKey) return;


    const apiUrl = `https://idealer.luklak.work/api/org/demoempty/hooks/HZ5wIxDhhTN6HzFAvOr9Zx-uvEdtBzRjw_c5x1nLoI8?issueKey=${issueKey}`; // Đường link Webhook lấy trên Luklak 


    const options = {
      method: "post",
      contentType: "application/json",
      payload: JSON.stringify(data),
      muteHttpExceptions: true,
    };


    const response = UrlFetchApp.fetch(apiUrl, options);
    Logger.log(response.getContentText());
  } catch (err) {
    Logger.log("Lỗi khi xử lý onEdit: " + err);
  }
}


```
{% endcode %}

3. Dữ liệu được gửi trực tiếp sang Luklak kèm mã mục (Object key)

4) Dữ liệu được nhận lại thông qua Webhook và tìm ra đúng mục theo mã mục đã gửi

5. Thông tin được cập nhật trong LUKLAK tương ứng với mục đã được xác định

</details>

## Luklak -> n8n -> Google Doc

{% hint style="info" %}
Ứng dụng: In văn bản theo giá trị smart value trong Luklak, như phiếu thu cho khách hàng, tờ trình...
{% endhint %}

{% @guidejar/embed guideId="8113f48e-ea52-4504-91e7-66038cb8558c" type="1" controls="on" url="https://www.guidejar.com/embed/8113f48e-ea52-4504-91e7-66038cb8558c?type=1&controls=on" %}

<details>

<summary>Luồng thiết lập</summary>

```javascript
let time = $('Webhook').item.json.body.fields.sinh_ngay.value.value.split('-')
let ngay = time[2]
let thang = time[1]
let nam = time[0]
let newTime = `${ngay}/${thang}/${nam}`

let time1 = $('Webhook').item.json.body.fields.ngay_bat.value.value.split('-')
let ngay1 = time1[2]
let thang1 = time1[1]
let nam1 = time1[0]
let newTime1 = `${ngay1}/${thang1}/${nam1}`

let time2 = $('Webhook').item.json.body.fields.vao_nha_tam_giu.value.value.split('T')
let time3 = time2[0].split('-')
let ngay2 = time3[2]
let thang2 = time3[1]
let nam2 = time3[0]
let newTime2 = `${ngay2}/${thang2}/${nam2}`

let gio = time2[1].split('+')
let gio1 = gio[0]



return {ngaysinh: newTime, nagy_bat: newTime1,vaonhatamgiam: newTime2, gio: gio1};
```

</details>

## Luklak -> n8n -> Google Calendar

{% hint style="info" %}
Trong nhiều tình huống kinh doanh, việc kết nối thông tin từ hệ thống quản lý công việc với lịch làm việc là nhu cầu thiết yếu. LUKLAK Universal Automation kết hợp với n8n cho phép bạn tự động đồng bộ các thông tin ngày tháng từ LUKLAK sang Google Calendar để tạo lịch hẹn\


### Tình huống ứng dụng

Tính năng này đặc biệt hữu ích trong các trường hợp:

* Đặt lịch demo sản phẩm với khách hàng tiềm năng
* Lập lịch phỏng vấn ứng viên tuyển dụng
* Tạo cuộc họp với đối tác hoặc nhà cung cấp
* Lên lịch kiểm tra/nghiệm thu dự án
{% endhint %}

{% @guidejar/embed guideId="5850fe48-f9fa-4729-a9da-bd203905c4bb" type="1" controls="on" url="https://www.guidejar.com/embed/5850fe48-f9fa-4729-a9da-bd203905c4bb?type=1&controls=on" %}

<details>

<summary>Giải thích logic thiết lập</summary>

### Thiết lập trong LUKLAK

| QUY TẮC                | TRIGGER                                                                                                                      | CONDITION  | ACTION                                                                                                                    |
| ---------------------- | ---------------------------------------------------------------------------------------------------------------------------- | ---------- | ------------------------------------------------------------------------------------------------------------------------- |
| Tạo mục con `Lịch hẹn` | <p>Ấn "Tạo lịch hẹn" tại Action Menu trên mục <code>Khách hàng</code><br><br>Hiện popup để điền ngày, giờ hẹn (bắt buộc)</p> | (không có) | Tạo mục con `Lịch hẹn`, tự động cập nhật trường thời gian hẹn & các thông tin khách hàng để đặt lịch (email, lời nhắn...) |
| Đẩy dữ liệu sang n8n   | Mục `Lịch hẹn` được tạo                                                                                                      | (không có) | Bắn webhook sang n8n với đầy đủ thông tin về lịch hẹn                                                                     |

### Thiết lập trong n8n

| QUY TẮC                     | NODE CẦN DÙNG     | NGHIỆP VỤ                                                                                                 |
| --------------------------- | ----------------- | --------------------------------------------------------------------------------------------------------- |
| Tạo sự kiện Google Calendar | 1/Webhook         | Nhận dữ liệu từ Luklak                                                                                    |
|                             | 2/Code            | <p>Chuẩn hóa dữ liệu date format để khớp với Google Calendar</p><p><code>HH:mm ngày DD/MM/YYYY</code></p> |
|                             | 3/Google Calendar | Tạo sự kiện trên Google Calendar với các thông tin ngày tháng, email khách,... từ webhook                 |

</details>

<details>

<summary>Luồng thiết lập</summary>

```javascript
var originalDateString = $json.body.fields.ngay_hen_demo.value.value;
var nguoilam = $json.body.fields.assignee.value.value.displayName;
var emailnguoilam = $json.body.fields.assignee.value.value.email;
var tieude = $json.body.fields.title.value.value;
// Chỉnh dạng
var formattedDateString = originalDateString.replace('T', ' ').slice(0, 19);

// Tạo start - end từ chuỗi đã được định dạng
var dateStart = new Date(formattedDateString);
var dateEnd = new Date(dateStart.getTime());

// Tạo ngày kết thúc hẹn
dateStart.setHours(dateEnd.getHours() + 0);

dateEnd.setHours(dateEnd.getHours() + 0);

// Định dạng ngày thành chuỗi
var formattedStart = dateStart.toISOString().slice(0, 19).replace('T', ' ');
var formattedEnd = dateEnd.toISOString().slice(0, 19).replace('T', ' ');

return { 
  formattedDateString: formattedDateString,
  tieu_de: tieude,
  time_start: formattedStart, 
  time_end: formattedEnd, 
  nguoilam: nguoilam,
  emailnguoilam: emailnguoilam
};
```

</details>
