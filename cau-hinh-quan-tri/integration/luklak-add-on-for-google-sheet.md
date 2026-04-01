# Luklak Add-on for Google Sheet

**LuklakSheet** là một Google Apps Script Add-on giúp bạn đẩy dữ liệu từ Google Sheets lên nền tảng Luklak thông qua Webhook. Add-on hỗ trợ cấu hình mapping cột, tự động chuyển đổi định dạng dữ liệu, và theo dõi kết quả push.

{% hint style="info" %}
Add-on hiện chưa được publish lên Google Workspace Marketplace. Bạn cần cài đặt thủ công bằng cách copy code trực tiếp vào Google Apps Script Editor.
{% endhint %}

## I. Hướng dẫn cấu hình

{% stepper %}
{% step %}
### Cài đặt Add-on

#### 1.1. Mở Google Apps Script Editor

* Mở file Google Sheets mà bạn muốn sử dụng
* Vào menu **Extensions > Apps Script** (hoặc **Phần mở rộng > Apps Script**)
* Trình soạn Google Apps Script sẽ mở ra trong tab mới

#### 1.2. Tạo file Code.gs

* Trong Apps Script Editor, bạn sẽ thấy file `Code.gs` mặc định
* **Xóa toàn bộ nội dung** trong file `Code.gs`
* Mở file `Code.gs` từ [folder Google Drive](https://drive.google.com/drive/u/0/folders/10e2BgZ6H7LQg93HpOgPk4sPeIdV03-nP)
* Copy toàn bộ nội dung và dán vào file `Code.gs` trong Apps Script Editor

#### 1.3. Tạo file Sidebar.html

* Trong Apps Script Editor, nhấn vào dấu **+** bên cạnh mục **Files** (hoặc vào **File > New > HTML**)
* Đặt tên file là `Sidebar` (không cần phần đuôi `.html`, hệ thống sẽ tự thêm)
* **Xóa toàn bộ nội dung** trong file `Sidebar.html` vừa tạo
* Mở file `Sidebar.html` từ [folder Google Drive](https://drive.google.com/drive/u/0/folders/10e2BgZ6H7LQg93HpOgPk4sPeIdV03-nP)
* Copy toàn bộ nội dung và dán vào file `Sidebar.html` trong App Scripts Editor

#### 1.4. Lưu và cấp quyền

* Nhấn **Ctrl + S** (hoặc biểu tượng Save) để lưu cả 2 file
* Quay lại Google Sheets, **tải lại trang** (F5)
* Sau khi tải lại, chọn **Extension** bạn sẽ thấy menu **Luklak for Sheet** xuất hiện trên thanh menu
* Nhấn **Luklak for Sheet > Mở LuklakSheet**
* Lần đầu tiên, Google sẽ yêu cầu bạn **cấp quyền truy cập** (Authorization). Nhấn **Allow / Cho phép** để tiếp tục

{% hint style="info" %}
Vì đây là script chưa được Google xác minh, bạn sẽ thấy cảnh báo "This app isn't verified". Nhấn **Advanced > Go to LuklakSheet (unsafe)** để tiếp tục. Điều này là bình thường khi sử dụng script tự cài đặt.
{% endhint %}
{% endstep %}

{% step %}
### Cấu hình kết nối Webhook

Sau khi mở sidebar, bạn sẽ thấy giao diện cấu hình với 2 tab: **Cấu hình** và **Log**.

#### 2.1. Nhập Webhook URL

* Trong tab **Cấu hình**, nhập **Webhook URL Luklak** mà bạn đã tạo trên nền tảng Luklak
  * Định dạng: `https://idealer.luklak.com/api/org/...`

#### 2.2. Test kết nối

* Nhấn nút **Test kết nối** để kiểm tra URL có hoạt động không
* Nếu thành công, bạn sẽ thấy thông báo màu xanh "Kết nối thành công! (HTTP 200)"
* Nếu thất bại, kiểm tra lại URL và token

#### 2.3. Lưu cấu hình

* Nhấn nút **Lưu** để lưu thông tin webhook. Cấu hình sẽ được lưu theo tài khoản Google của bạn.
{% endstep %}

{% step %}
### Chọn dữ liệu cần push

#### 3.1. Chọn Sheet nguồn

* Chọn sheet chứa dữ liệu từ dropdown **Sheet nguồn**
* Các sheet có tên bắt đầu bằng `_Luklak` sẽ bị ẩn (dùng cho hệ thống)

#### 3.2. Cấu hình phạm vi dữ liệu

| Trường   | Mô tả                           | Mặc định          |
| -------- | ------------------------------- | ----------------- |
| Từ cột   | Cột bắt đầu (vd: `A`)           | A                 |
| Đến cột  | Cột kết thúc (vd: `F`)          | Cột cuối có data  |
| Từ dòng  | Dòng bắt đầu (dòng 1 là header) | 2                 |
| Đến dòng | Dòng kết thúc                   | Dòng cuối có data |

{% hint style="warning" %}
Tối đa **200 dòng** mỗi lần push. Nếu dữ liệu nhiều hơn, bạn cần chia thành nhiều lần push bằng cách thay đổi phạm vi dòng.

Webhook của Luklak hiện đang **limit 6000 lần** nhận request trong **1 giờ**. Nếu dữ liệu nhiều hơn cần chia thời gian đẩy
{% endhint %}

#### 3.3. Tải cột và tạo Mapping

* Nhấn **Tải cột & tạo Mapping** để load danh sách cột từ sheet đã chọn
{% endstep %}

{% step %}
### Cấu hình Mapping

Đây là bước quan trọng nhất. Bạn cần chỉ định:

* **Variable**: Tên biến tương ứng trong cấu hình automation ở Luklak. Đây là tên sau `$input.` trong Smart Value của Luklak. Các biến này nên đặt viết liền, không dấu.
* **Loại trường**: Kiểu dữ liệu của trường trên Luklak, dùng để add-on tự động chuyển đổi giá trị cho phù hợp.

{% hint style="info" %}
Nếu cột nào không cần push, để trống **Variable** — cột đó sẽ bị bỏ qua.
{% endhint %}
{% endstep %}

{% step %}
### Xem trước và Push dữ liệu

#### 5.1. Xem trước (Preview)

* Nhấn **Xem trước** để xem 3 dòng đầu tiên sau khi chuyển đổi
* Giá trị gốc sẽ bị gạch ngang, giá trị sau chuyển đổi hiển thị màu xanh
*   Kiểm tra kỹ trước khi push thật<br>

    <div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (652).png" alt=""><figcaption></figcaption></figure></div>

#### 5.2. Push dữ liệu

* Nhấn **Push lên Luklak**
* Thanh tiến trình sẽ hiển thị trạng thái
* Sau khi hoàn tất, hệ thống tự động chuyển sang tab **Log** để hiển thị kết quả:
  * **Cần đẩy**: Tổng số dòng
  * **Thành công**: Số dòng gửi thành công
  * **Lỗi**: Số dòng bị lỗi (kèm chi tiết)

{% hint style="info" %}
Mỗi dòng được gửi riêng lẻ (1 request/dòng) với độ trễ 200ms giữa các request để tránh quá tải.
{% endhint %}
{% endstep %}
{% endstepper %}

## II. Chi tiết chuyển đổi theo loại trường

Add-on tự động chuyển đổi giá trị dựa trên **Loại trường** bạn chọn trong Mapping. Dưới đây là bảng chi tiết:

### Các trường KHÔNG cần chuyển đổi (giữ nguyên giá trị)

| Loại trường              | Field Type (code) | Yêu cầu dữ liệu trong Sheet                                   |
| ------------------------ | ----------------- | ------------------------------------------------------------- |
| Dòng chữ / Đoạn văn bản  | `text`            | Văn bản thường, gửi nguyên                                    |
| Số nguyên / Số thập phân | `number`          | Giá trị số. Chuỗi sẽ được chuyển thành số, không hợp lệ → `0` |
| Một email                | `email`           | Email, sẽ được trim và chuyển thành chữ thường                |
| Nhiều email              | `multi_email`     | Nhiều email cách nhau bởi dấu phẩy, trim giá trị              |
| Số điện thoại            | `phone`           | Là số điện thoại hợp lệ, có thể có mã                         |

### Các trường CẦN chuyển đổi tự động

| Loại trường         | Field Type (code) | Logic chuyển đổi                                                                                                                                                           | Ví dụ                                             |
| ------------------- | ----------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------- |
| Sổ xuống chọn một   | `single_select`   | <p>Cần khớp chính xác với key của option trong cấu hình field<br></p><p>Normalize: bỏ dấu tiếng Việt, chuyển chữ thường, khoảng trắng, kí tự đặc biệt → <code>_</code></p> | `"Hà Nội"` → `"ha_noi"`                           |
| Sổ xuống chọn nhiều | `multi_select`    | <p>Cần khớp chính xác với key của option trong cấu hình field<br><br>Mỗi giá trị (cách bởi dấu phẩy) được normalize riêng</p>                                              | `"Hà Nội, Hồ Chí Minh"` → `"ha_noi, ho_chi_minh"` |
| Hộp kiểm đơn        | `checkbox`        | Chuyển thành `true` hoặc `false`                                                                                                                                           | `TRUE` → `true`, `FALSE` → `false`                |
| Nhiều hộp kiểm      | `multi_checkbox`  | <p>Cần khớp chính xác với key của option trong cấu hình field<br><br>Mỗi giá trị (cách bởi dấu phẩy) được normalize riêng</p>                                              | `"Có, Không"` → `"co, khong"`                     |
| Chọn ngày           | `date`            | Chuyển thành định dạng `yyyy-mm-dd`                                                                                                                                        | `15/01/2024` → `"2024-01-15"`                     |
| Chọn ngày giờ       | `datetime`        | Chuyển thành ISO 8601 với timezone +07:00                                                                                                                                  | → `"2024-01-15T09:00:00.000+07:00"`               |

### Các trường cần TỰ CHUẨN BỊ GIÁ TRỊ trước khi push

{% hint style="warning" %}
Các trường dưới đây yêu cầu bạn phải tự lấy ID/mã tương ứng từ Luklak và điền vào Google Sheets trước khi push. Add-on **KHÔNG** tự động tra cứu ID — chỉ gửi nguyên giá trị bạn điền.
{% endhint %}

| Loại trường             | Field Type (code) | Cách chuẩn bị dữ liệu trong Sheet                                                     |
| ----------------------- | ----------------- | ------------------------------------------------------------------------------------- |
| **Chọn một người**      | `single_user`     | Điền **1 ID người dùng** Luklak. Lấy ID từ trang quản trị người dùng trên Luklak.     |
| **Chọn nhiều người**    | `multi_user`      | Điền **nhiều ID người dùng**, phân cách bởi dấu phẩy. VD: `id_user1, id_user2`        |
| **Chọn một nhóm**       | `single_group`    | Điền **1 ID nhóm** Luklak. Lấy ID từ trang quản lý nhóm trên Luklak.                  |
| **Chọn nhiều nhóm**     | `multi_group`     | Điền **nhiều ID nhóm**, phân cách bởi dấu phẩy. VD: `id_group1, id_group2`            |
| **Chọn một đầu việc**   | `single_task`     | Điền **1 mã đầu việc** Luklak (object key). Lấy mã từ giao diện đầu việc trên Luklak. |
| **Chọn nhiều đầu việc** | `multi_task`      | Điền **nhiều mã đầu việc**, phân cách bởi dấu phẩy. VD: `TASK-001, TASK-002`          |

#### Cách lấy ID người dùng / nhóm / mã đầu việc từ Luklak

1. **ID người dùng**:
   1. Vào tính năng **Chấm công** trên Luklak
   2. Chọn **Báo cáo tổng hợp**, thêm cột hiển thị là ID
   3.  Export báo cáo ra là sẽ có dữ liệu người dùng kèm ID trong Luklak<br>

       <div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (648).png" alt=""><figcaption></figcaption></figure></div>
2.  **ID nhóm**: Vào **Cài đặt nhóm**, tìm nhóm cần chọn, click vào nhóm đó và copy id ở trên URL của web

    <div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (646).png" alt=""><figcaption></figcaption></figure></div>


3.  **Mã đầu việc**: Mở đầu việc trên Luklak, mã đầu việc thường hiển thị dạng `TASK-XXX` hoặc tương tự

    <div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (647).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
Bạn có thể tạo một sheet riêng làm "bảng tra cứu" chứa danh sách ID người dùng, nhóm, đầu việc để tiện tham chiếu khi điền dữ liệu.
{% endhint %}

## III. Ví dụ thực tế

### Ví dụ 1: Push danh sách khách hàng

**Dữ liệu trong Sheet:**

<div align="left" data-with-frame="true"><figure><img src="../../.gitbook/assets/image (650).png" alt=""><figcaption></figcaption></figure></div>

**Cấu hình Mapping:**

<div align="center" data-with-frame="true"><figure><img src="../../.gitbook/assets/image (651).png" alt=""><figcaption></figcaption></figure></div>

| Cột Sheet | Field Key | Loại trường       |
| --------- | --------- | ----------------- |
| Name      | name      | Dòng chữ          |
| Email     | email     | Một email         |
| Phone     | phone     | Số điện thoại     |
| City      | city      | Sổ xuống chọn một |
| VIP       | vip       | Hộp kiểm đơn      |

**Kết quả gửi lên Luklak (JSON payload cho dòng 1):**

```json
{
  "name": "Nguyễn Văn A",
  "email": "a@gmail.com",
  "phone": "0356459055",
  "city": "ha_noi",
  "vip": true
}
```

**Cấu hình automation bên Luklak**

<figure><img src="../../.gitbook/assets/image (653).png" alt=""><figcaption></figcaption></figure>

### Ví dụ 2: Push đầu việc có người phụ trách

**Dữ liệu trong Sheet:**

<table><thead><tr><th width="122">Tên công việc</th><th>Người phụ trách</th><th>Người phụ trách (ID)</th><th>Nhóm phụ trách</th><th>Nhóm (ID)</th><th>Tình trạng</th></tr></thead><tbody><tr><td>Thiết kế logo</td><td>Nguyễn Văn D</td><td>118732a2-7995-11f0-b29b-991ed3bb2377</td><td>Design</td><td>13e15c9e-29b2-11f1-b977-373666a1dc2c</td><td>Đang làm</td></tr><tr><td>Viết bài marketing</td><td>Nguyễn Thị E</td><td>3cd7771e-8485-11f0-b2c4-991ed3bb2377</td><td>Marketing</td><td>f50614b8-29b1-11f1-b977-373666a1dc2c</td><td>Chưa bắt đầu</td></tr></tbody></table>

{% hint style="info" %}
Bạn nên dùng công thức trong Google Sheet để mapping giá trị cột kiểu dữ liệu Người, Nhóm, Chọn Đầu việc với các id/key đã lưu trữ sẵn
{% endhint %}

**Cấu hình Mapping:**

| Cột Sheet            | Field Key      | Loại trường       |
| -------------------- | -------------- | ----------------- |
| Tên công việc        | task           | Dòng chữ          |
| Người phụ trách      | assignee\_name | Dòng chữ          |
| Người phụ trách (ID) | assignee\_id   | Chọn một người    |
| Trạng thái           | status         | Sổ xuống chọn một |

**Kết quả gửi lên Luklak (JSON payload cho dòng 1):**

```json
{
  "task": "Thiết kế logo",
  "assignee_name": "Nguyễn Văn D",
  "assignee_id": "118732a2-7995-11f0-b29b-991ed3bb2377",
  "status": "dang_lam"
}
```

**Cấu hình automation ở Luklak**

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (649).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
`assignee_id` gửi **nguyên giá trị ID** — bạn phải đảm bảo ID này tồn tại trên Luklak. Riêng `status` được **normalize** từ "Đang làm" thành "dang\_lam".
{% endhint %}

## IV. Logic normalize (chuyển đổi tên tiếng Việt thành key)

Add-on sử dụng hàm normalize cho các trường dạng **select** và **checkbox**. Logic như sau:

1. Chuyển thành **chữ thường**: `"Hà Nội"` → `"hà nội"`
2. **Bỏ dấu tiếng Việt**: `"hà nội"` → `"ha noi"` (ví dụ khác: `"Đà Nẵng"` → `"da nang"`)
3. Thay **khoảng trắng và ký tự đặc biệt** bằng `_`: `"ha noi"` → `"ha_noi"`
4. **Loại bỏ `_` thừa** ở đầu/cuối và trùng lặp

**Thêm ví dụ:**

| Giá trị gốc           | Sau normalize         |
| --------------------- | --------------------- |
| `Hà Nội`              | `ha_noi`              |
| `Hồ Chí Minh`         | `ho_chi_minh`         |
| `Đang thực hiện`      | `dang_thuc_hien`      |
| `Ưu tiên CAO`         | `uu_tien_cao`         |
| `Option 1`            | `option_1`            |
| `Có, Không, Tạm dừng` | `co, khong, tam_dung` |

{% hint style="warning" %}
Giá trị sau normalize phải **khớp chính xác** với key của option/checkbox đã cấu hình trong Luklak. Hãy kiểm tra bằng chức năng **Xem trước** trước khi push.
{% endhint %}

## V. Xử lý lỗi thường gặp

| Lỗi                             | Nguyên nhân                                          | Cách xử lý                                               |
| ------------------------------- | ---------------------------------------------------- | -------------------------------------------------------- |
| "Kết nối thất bại"              | Sai Webhook URL hoặc Luklak chưa bật webhook         | Kiểm tra lại URL, đảm bảo webhook đang hoạt động         |
| HTTP 401 / 403                  | Secret Token sai hoặc thiếu                          | Kiểm tra lại Secret Token                                |
| HTTP 400                        | Dữ liệu gửi không đúng định dạng Luklak yêu cầu      | Dùng **Xem trước** để kiểm tra giá trị chuyển đổi        |
| "Vượt quá 200 dòng"             | Phạm vi dòng quá lớn                                 | Thu hẹp phạm vi dòng (vd: push 100 dòng mỗi lần)         |
| Dòng bị lỗi riêng lẻ            | Dữ liệu dòng đó có vấn đề (thiếu trường bắt buộc...) | Xem chi tiết lỗi trong tab Log, sửa dữ liệu và push lại  |
| Menu LuklakSheet không hiển thị | Chưa lưu code hoặc chưa tải lại trang                | Lưu code trong Apps Script Editor, tải lại Google Sheets |

## VI. Lưu ý quan trọng

{% hint style="info" %}
* **Dòng 1 luôn là header** — dữ liệu bắt đầu từ dòng 2 trở đi
* Mỗi lần push sẽ gửi **từng dòng một** (không phải gửi toàn bộ 1 lúc), với **độ trễ 200ms** giữa mỗi dòng
* Cấu hình được **lưu theo tài khoản Google** của bạn (không chia sẻ với người khác)
* Chỉ các dòng **có lỗi** mới được ghi vào sheet ẩn `_LuklakLog`
* Nút **Xem trước** rất hữu ích — luôn kiểm tra trước khi push thật
{% endhint %}
