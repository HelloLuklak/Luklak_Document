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
Tình huống ứng dụng: Thực hiện hành động kết nối đến mục liên quan, thông qua việc có chung 1 giá trị trường dữ liệu. VD:\


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
