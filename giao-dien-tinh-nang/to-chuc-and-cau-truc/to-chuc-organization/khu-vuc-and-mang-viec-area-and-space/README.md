# Khu vực & mảng việc (Area & Space)

<figure><img src="../../../../.gitbook/assets/image (269).png" alt=""><figcaption><p>Cấu trúc Khu vực (Area) &#x26; Mảng việc (Space) trong Tổ chức (Organiazation)</p></figcaption></figure>

### Tổng quan

**Tổ chức** là nơi lưu trữ toàn bộ dữ liệu công việc của doanh nghiệp, được chính doanh nghiệp đó sắp xếp và quản lý theo một cấu trúc vừa chặt chẽ vừa linh hoạt. Tổ chức cho phép xây dựng và thể hiện bức tranh tổng thể về hoạt động của toàn công ty.

Trong Tổ chức, có các Khu vực để quản lý các phạm vi công việc lớn, và bên trong mỗi Khu vực là các Mảng Việc nhỏ hơn.

#### Khu vực là gì?

Area là đơn vị tổ chức trong hệ thống luklak, thường tương ứng với cấp bộ phận, phòng ban hoặc các phạm vi công việc lớn. Ví dụ: Khu vực Phòng Kinh doanh, Khu vực Phối hợp Sản phẩm, Khu vực Nhân sự.

Mỗi Area chứa nhiều Mảng việc (Space) bên trong, phân chia công việc thành các phạm vi nhỏ hơn, dễ quản lý.

#### Mảng việc là gì?

Mảng Việc là không gian làm việc trực tiếp của nhân sự trong doanh nghiệp. Nó chứa toàn bộ dữ liệu công việc (Issue) và là nơi các hoạt động hàng ngày được thực hiện và quản lý.

### Mối quan hệ Chức năng - Mảng việc - Khu vực - Mục việc

* Mỗi Mảng Việc được tạo ra từ một Chức Năng
* Mỗi Mảng Việc thuộc về một Khu Vực cụ thể." Khu Vực (Area)
* Mỗi Mảng Việc có chứa các Mục việc (Issue Types) & Mục việc con (Sub-Issue Types) bên trong

<figure><img src="../../../../.gitbook/assets/image (441).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../../.gitbook/assets/image (450).png" alt=""><figcaption><p>Ví dụ các Mục việc tiêu chuẩn &#x26; Mục việc con trực thuộc mảng việc Sales &#x26; CRM</p></figcaption></figure>

### Hướng dẫn tạo mảng việc

1. **Xác định khu vực để tạo mảng việc**

Di chuyển đến khu vực mà bạn muốn tạo mảng việc trong đó. Tìm đến "Tạo mảng việc" để bắt đầu tạo.

<figure><img src="../../../../.gitbook/assets/image (270).png" alt=""><figcaption><p>Ví dụ thao tác tạo thêm mảng việc trong Khu vực Kinh doanh</p></figcaption></figure>

2. **Nhập thông tin mảng việc**

Điền các thông tin chung cho mảng việc để dễ quản lý

* Tên mảng việc
* Mô tả
* Mã mảng việc
* Biểu tượng

<figure><img src="../../../../.gitbook/assets/image (271).png" alt=""><figcaption></figcaption></figure>

3. **Chọn chức năng**

{% hint style="info" %}
**Mỗi mảng việc đều cần gắn liền với 01 chức năng**: Chức năng quyết định Mảng việc sẽ có những nghiệp vụ, thông tin dữ liệu, quy trình làm việc, tự động hóa, và báo cáo gì, phân quyền & thông báo như thế nào.
{% endhint %}

Hai cách xác định chức năng cho mảng việc:

#### Sử dụng template có sẵn

<figure><img src="../../../../.gitbook/assets/image (272).png" alt=""><figcaption><p>Chọn 1 trong các chức năng có sẵn để dùng cho mảng việc</p></figcaption></figure>



#### Tạo mới từ đầu

<figure><img src="../../../../.gitbook/assets/image (273).png" alt=""><figcaption></figcaption></figure>

#### 4. Cấu hình chức năng

Sau khi ấn "Khởi tạo", mảng việc của bạn đã được gắn với 01 chức năng thành công. Mảng việc này sẽ có sẵn cấu hình của template chức năng tương ứng (nếu chọn chức năng có sẵn) hoặc có sẵn cấu hình mặc định của hệ thống (task & substask và các workflow cơ bản).

<figure><img src="../../../../.gitbook/assets/image (274).png" alt=""><figcaption></figcaption></figure>

Để thiết kế chức năng theo mong muốn cho mảng việc, vui lòng vào "Chức năng của mảng việc", sau đó thực hiện các bước cấu hình theo hướng dẫn.

<figure><img src="../../../../.gitbook/assets/image (277).png" alt=""><figcaption></figcaption></figure>

### Làm việc trong mảng việc

{% hint style="info" %}
**Quản lý mọi nghiệp vụ trong cấu trúc mảng việc:** Sau khi thiết kế xong chức năng với các nghiệp vụ cần thiết, các nghiệp vụ này sẽ hiện liền mạch ngay dưới Mảng việc.
{% endhint %}

* Ấn vào từng tab để hiện ra danh sách mục tương ứng
* Ấn lần 2 để bỏ chọn

<figure><img src="../../../../.gitbook/assets/image (438).png" alt=""><figcaption><p>Ví dụ: Mảng việc Product Delivery, được sinh ra từ chức năng TCS Product Delivery. Mảng việc này bao gồm 3 nghiệp vụ (Design, Production, Delivery) như được được cấu hình trong Chức năng (Function)</p></figcaption></figure>

{% content-ref url="../../../../cau-hinh-quan-tri/function/cau-hinh-function.md" %}
[cau-hinh-function.md](../../../../cau-hinh-quan-tri/function/cau-hinh-function.md)
{% endcontent-ref %}
