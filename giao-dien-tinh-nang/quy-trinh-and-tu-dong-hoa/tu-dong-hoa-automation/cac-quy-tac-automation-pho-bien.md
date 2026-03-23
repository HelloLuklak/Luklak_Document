# Các quy tắc Automation phổ biển

## Cảnh báo trùng lặp/check trùng

{% hint style="info" %}
**Tình huống**: Khi nhập dữ liệu khách hàng từ nguồn bên ngoài (ví dụ: file Google Sheet, API...) vào Luklak, có thể xảy ra tình huống khách hàng bị trùng lặp đã tồn tại trong hệ thống.
{% endhint %}

#### **Hướng xử lý:**

* Sử dụng **Số điện thoại** của khách hàng làm điều kiện kiểm tra.

Nếu **số điện thoại trùng** với một khách hàng đã có trong Luklak:

* Không tạo bản ghi mới. Thay vào đó, **cập nhật trường “Lịch sử hoạt động”** (hoặc một trường đã được định nghĩa kiểu dữ liệu đoạn văn bản).

Nếu **số điện thoại không trùng**:

* Tạo mới một bản ghi khách hàng mới.

{% embed url="https://guidejar.com/guides/96bcd426-d212-4ed9-808d-cbdbf0428764" %}

## Cộng dồn/Trừ dồn

{% hint style="info" %}
Việc quản lý tài chính, theo dõi công nợ, tính toán các khoản phiếu thu/chi hay cộng/trừ dồn thường đòi hỏi nhiều thao tác thủ công và dễ gây sai sót. LUKLAK Universal Automation giúp bạn tự động hóa hoàn toàn các quy trình này, đảm bảo tính chính xác và hiệu quả.
{% endhint %}

#### Ứng dụng thực tế

* **Quản lý hợp đồng**: Tự động tính tổng giá trị, điều chỉnh trạng thái thanh toán
* **Theo dõi công nợ**: Cập nhật số dư khi phát sinh phiếu thu/chi
* **Quản lý quỹ**: Tự động cộng/trừ số dư khi có giao dịch
* **Tính giờ làm việc**: Cộng dồn thời gian làm việc theo nhân viên hoặc dự án

### Thông qua liên kết (Object Connection)

{% @guidejar/embed guideId="4ae6cb6b-21da-4736-bb89-1f1ece62cf2e" type="1" controls="on" url="https://www.guidejar.com/embed/4ae6cb6b-21da-4736-bb89-1f1ece62cf2e?type=1&controls=on" %}

### Thông qua trường chọn mục (Object Picker field)

{% @guidejar/embed guideId="e1057863-7495-4fad-9306-666293301d8b" type="1" controls="on" url="https://www.guidejar.com/embed/e1057863-7495-4fad-9306-666293301d8b?type=1&controls=on" %}

### Thay đổi giá trị cần cộng/trừ dồn (thông qua Action Menu với  biến số)

{% hint style="info" %}
Tình huống ứng dụng: Sửa đổi giá trị phiếu thu -> cần thay thế số tiền cũ bằng số tiền mới -> cập nhật chính xác tổng số tiền trên Hợp đồng
{% endhint %}

{% @guidejar/embed guideId="b6b66f1f-8c2b-48e8-8617-3e62e913bba5" type="1" controls="on" url="https://www.guidejar.com/embed/b6b66f1f-8c2b-48e8-8617-3e62e913bba5?type=1&controls=on" %}

### Thay đổi giá trị cần cộng/trừ dồn (thông qua Object Picker)

{% @guidejar/embed guideId="540529d1-85e9-4849-b22d-3d9542e0a10f" type="1" controls="on" url="https://www.guidejar.com/embed/540529d1-85e9-4849-b22d-3d9542e0a10f?type=1&controls=on" %}



### Sumup với Velocity

{% @guidejar/embed guideId="080374ca-7668-41ce-9024-649cc2aa4851" type="1" controls="on" url="https://www.guidejar.com/embed/080374ca-7668-41ce-9024-649cc2aa4851?type=1&controls=on" %}

{% hint style="info" %}
**Bài toán: Quản lý Phiếu thu trong Công nợ**

* Tại mục **Công nợ**, người dùng sẽ có thể **chọn các Phiếu thu tương ứng** từ danh sách hiện có.
* Khi người dùng **chọn các Phiếu thu** trong mục Công nợ:
* Hệ thống sẽ **tự động cộng dồn số tiền** từ các Phiếu thu được chọn để hiển thị vào trường **"Tổng số tiền"**.
* Đồng thời, tại từng **Phiếu thu**, hệ thống sẽ hiển thị thông tin **đã được liên kết với mục Công nợ nào**, giúp dễ dàng truy vết và kiểm soát mối liên hệ hai chiều.
{% endhint %}

## Lấy dữ liệu từ một mục (Object) khác

{% hint style="info" %}
Tình huống ứng dụng: Lấy dữ liệu cần sử dụng từ mục được chọn, gán/biến đổi/sử dụng trong mục khác. \
Ví dụ:

* **Quy trình đề xuất ngân sách**
  * Khi chọn dự án trong đề xuất chi → tự động lấy thông tin ngân sách, người phụ trách, mã dự án
* **Quản lý nhân sự và dự án**
  * Khi chọn nhân viên vào dự án → tự động lấy thông tin vị trí, phòng ban, mức lương giờ
* **Quản lý khách hàng và hợp đồng**
  * Khi chọn khách hàng trong hợp đồng → tự động lấy địa chỉ, người đại diện, mã số thuế
{% endhint %}

{% @guidejar/embed guideId="c3cbec28-ba2c-410e-b3cf-c99bfc8cc475" type="1" controls="on" url="https://www.guidejar.com/embed/c3cbec28-ba2c-410e-b3cf-c99bfc8cc475?type=1&controls=on" %}

## Kết nối mục bằng bộ lọc (thông qua smart value)

{% hint style="info" %}
Tình huống ứng dụng: Thực hiện hành động kết nối đến mục liên quan, thông qua việc có chung 1 giá trị trường dữ liệu. VD:<br>

* **Quản lý khách hàng và giao dịch**
  * Tự động liên kết giao dịch mới với khách hàng hiện có dựa trên số điện thoại/email
  * Đảm bảo lịch sử giao dịch luôn gắn với đúng khách hàng
* **Quản lý tài sản và vị trí**
  * Tự động liên kết tài sản với địa điểm dựa trên mã vị trí
  * Dễ dàng theo dõi tài sản theo từng địa điểm
{% endhint %}

{% @guidejar/embed guideId="ddab6e89-0f6f-4b67-88e3-fe246e9acdc4" type="1" controls="on" url="https://www.guidejar.com/embed/ddab6e89-0f6f-4b67-88e3-fe246e9acdc4?type=1&controls=on" %}

## Đổi người làm (assignee) hàng loạt

{% hint style="info" %}
Tình huống sử dụng: Mỗi khi đến 1 lịch trình nhất định (hàng ngày, tuần...), kiểm tra các công việc cần theo dõi & đổi người làm nếu muốn.\
\
Ví dụ:

**Cảnh báo và phân công lại khi task trễ hạn**

* Tự động phát hiện task quá hạn chưa hoàn thành
* Thông báo cho người quản lý
* Tự động phân công lại cho người có thẩm quyền xử lý

**Phân công task theo lịch trình**

* Tự động đổi người phụ trách theo lịch làm việc
* Đảm bảo công việc luôn có người theo dõi trong ca trực
* Thông báo cho người nhận nhiệm vụ mới
{% endhint %}

{% @guidejar/embed guideId="ddab6e89-0f6f-4b67-88e3-fe246e9acdc4" type="1" controls="on" url="https://www.guidejar.com/embed/ddab6e89-0f6f-4b67-88e3-fe246e9acdc4?type=1&controls=on" %}

Chị Ánh nhắc chuẩn quá! Hệ thống hiện tại đúng là cần một lực đẩy (Push) từ bên ngoài qua Webhook thay vì tự đi kéo (Pull) dữ liệu từ Sheet về. Việc dùng Google Apps Script hoặc N8n/Make để bắn Webhook từng dòng từ Sheet về Luklak là giải pháp thực tế và chính xác nhất cho trường hợp này.

Em đã điều chỉnh lại Cách 3 cho chuẩn xác về mặt kỹ thuật, đồng thời tinh chỉnh toàn bộ bài viết tuân thủ tuyệt đối định dạng không dùng thẻ `##` (chỉ dùng chữ in đậm cho các tiêu đề chính), riêng phần Guidejar vẫn giữ nguyên format code block như quy định.

Dưới đây là bản hoàn thiện `.mdx` nhé chị:

***

## Đưa đối tượng liên kết vào trường chọn đối tượng (hàng loạt)



### Bối cảnh & Bài toán thực tế

Trong giai đoạn đầu thiết lập hệ thống, đội ngũ của bạn thường dùng tính năng `🔗 Kết nối Đối tượng` (Liên kết tự do) để nối nhanh một Phiếu thu với một Khách hàng. Thao tác này rất linh hoạt và dễ dùng cho cá nhân.

{% hint style="info" %}
Tuy nhiên, khi doanh nghiệp mở rộng quy mô, nhu cầu vận hành tinh gọn đòi hỏi hệ thống phải tự động tính tổng doanh thu trên từng khách hàng, lọc danh sách công nợ, hoặc đồng bộ dữ liệu tài chính sang ERP. Lúc này, những liên kết tự do không còn đáp ứng được. Bạn bắt buộc phải quy chuẩn chúng thành Trường Chọn Đầu việc (Object Picker Field) để tạo ra một cấu trúc dữ liệu chặt chẽ và thông suốt.
{% endhint %}

### Tại sao cần đưa Liên kết đổ vào Trường Chọn Đầu việc?

* **Mở khóa sức mạnh truy vấn**: Dữ liệu nằm trong trường chuẩn giúp bạn tận dụng tối đa `🔍 UQL` để lọc (Ví dụ: Tìm mọi Khách hàng có _Trường Phiếu thu_ trống).
* **Nền tảng cho Báo cáo**: Dữ liệu có cấu trúc cho phép hệ thống tính toán (Sum/Count) và hiển thị trực quan trên Dashboard.
* **Tự động hoá & Tích hợp**: Các hệ thống bên ngoài hoặc các luồng tự động hoá tiếp theo dễ dàng đọc/ghi dữ liệu khi nó là một trường cố định.

### Bức tranh Tổng thể: 3 Phương pháp thực thi

Thay vì cập nhật thủ công hàng ngàn hồ sơ cũ, Luklak cung cấp cho bạn công cụ `⚙️ Tự động hoá Phổ quát` để xử lý hàng loạt. Tuỳ thuộc vào tình trạng dữ liệu hiện tại, bạn có thể chọn 1 trong 3 cách sau:

#### Cách 1: Quét ngược và Cập nhật trực tiếp (Nhanh & Tinh gọn nhất)

_Dành cho trường hợp: 2 Đầu việc đã có sẵn liên kết trực tiếp trên hệ thống._

Thay vì đứng từ Khách hàng để tìm Phiếu thu, ta sẽ đặt Tự động hoá Lịch trình đứng từ Phiếu thu, quét sang Khách hàng được liên kết, sau đó lấy chính ID của Phiếu thu đó (sử dụng biến `$trigger.key`) ghi thẳng vào Trường Chọn Đầu việc trên hồ sơ Khách hàng.

#### Cách 2: Luân chuyển nội bộ qua Webhook (Nâng cao)

_Dành cho trường hợp: Cần bóc tách, xử lý thêm logic phức tạp giữa các Mảng việc hoặc người thiết lập quen với tư duy API._

Phương pháp này dùng 2 luồng tự động hoá:

1. Luồng Gửi: Chạy lịch trình tại Khách hàng, dùng hành động Rẽ nhánh (Branching) tới các Phiếu thu liên kết, sau đó bắn Webhook mang theo "Mã Khách hàng" và "Mã Phiếu thu" (`$trigger.key và $current.key`)
2. Luồng Nhận: Hứng Webhook, dùng UQL để tìm lại hồ sơ Khách hàng dựa trên mã nhận được, cuối cùng cập nhật "Bổ sung" Mã Phiếu thu vào Trường Chọn Đầu việc.

#### Cách 3: Xử lý qua Spreadsheet & Webhook

_Dành cho trường hợp: Dữ liệu có điểm chung (như Số điện thoại)._

1. Xuất danh sách 2 `🧊 Đầu việc` (Khách hàng và Phiếu thu) ra Google Sheet.
2. Dùng hàm VLOOKUP ghép Mã Phiếu thu vào cạnh Số điện thoại của Khách hàng.
3. Dùng Google Apps Script (hoặc công cụ trung gian như Make/N8n) để thiết lập luồng quét từng dòng trên Sheet và bắn Webhook về nền tảng Luklak (gửi kèm Số điện thoại và Mã Phiếu thu).
4. Trên Luklak, tạo một Tự động hoá với Trigger "Nhận Webhook". Sử dụng UQL để dò tìm đúng Khách hàng mang Số điện thoại đó và cập nhật Mã Phiếu thu vào trường tương ứng.

### Hướng dẫn thiết lập chi tiết (Cách 1 - Khuyên dùng)



```
# Thiết lập luồng Cập nhật Trường dữ liệu trực tiếp
Hướng dẫn cách dùng biến $trigger.key để ánh xạ dữ liệu lịch sử tinh gọn nhất.

## Section 1: Chuẩn bị Trường dữ liệu
! Important: Tại cấu hình Chức năng Khách hàng, hãy đảm bảo bạn đã tạo một "Trường Chọn Đầu việc" (chỉ định tới Mảng việc Phiếu thu) và BẬT tính năng "Chọn nhiều" (Multiple).

1. Truy cập Mảng việc Phiếu thu


2. Tạo Tự động hoá theo Lịch trình
![Tạo lịch trình quét Phiếu thu]


## Section 2: Cấu hình Rẽ nhánh và Cập nhật


1. Thêm hành động Rẽ nhánh (Branching)
![Cấu hình Branching]
* Chọn mục tiêu Rẽ nhánh tới: Đầu việc được liên kết.
* Điều kiện lọc: Chỉ định loại Đầu việc là "Khách hàng".

2. Thêm hành động Cập nhật Trường (bên trong nhánh)
* Hành động này sẽ tác động trực tiếp lên hồ sơ Khách hàng đang được rẽ nhánh tới.

3. Điền giá trị ID Phiếu thu
![Cập nhật trường Phiếu thu]
* Tại Trường Chọn Đầu việc (chứa Phiếu thu), sử dụng biến hệ thống `$trigger.key` (đại diện cho ID của Phiếu thu đang kích hoạt luồng) để điền vào. Lưu lại và kích hoạt luồng.
```

