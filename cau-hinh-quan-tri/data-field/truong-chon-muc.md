# Trường chọn mục

## Tổng quan

Mỗi Mục (issue) là một đối tượng lưu trữ dữ liệu (đầu việc, tài liệu,...). Ngoài cách thể hiện mối quan hệ giữa các Mục với nhau qua Kết nối mục (issue link) thì <mark style="color:blue;">luklak</mark> bổ sung thêm loại **Trường Chọn mục** (issue picker field).

Với loại trường này giúp tăng sự liên kết giữa các phần dữ liệu khác nhau trong hệ thống, cho phép tìm kiếm thông tin liên quan qua UQL, khả năng truy xuất dữ liệu dễ dàng qua Tự động (automation), đa dạng khả năng tùy biến cho nhiều nghiệp vụ,...

{% embed url="https://guidejar.com/guides/a150ff23-10ac-4eb0-b9f4-a2977516c77c" %}
Hướng dẫn tổng quan Issue picker field
{% endembed %}

### User-flow

<figure><img src="../../.gitbook/assets/image (558).png" alt=""><figcaption></figcaption></figure>

### Ví dụ sử dụng thực tế

Quản lý thông tin về Giáo viên, Học viên của Lớp học bằng cách tại Loại mục (issue type) sử dụng loại trường **Chọn một mục** để chọn các Mục Giáo viên cho lớp, loại trường **Chọn nhiều mục** để chọn các Mục Học viên của lớp

<figure><img src="../../.gitbook/assets/image (559).png" alt=""><figcaption></figcaption></figure>

## Cài đặt

{% hint style="info" %}
**Lưu ý:**

Để tạo mới và cấu hình các Trường dữ liệu (data field), bạn cần hạng thành viên Quản lý ứng dụng (app manager) trở lên trong Tổ chức (organization membership) hoặc  trong Chức năng (function membership), xem chi tiết [tại đây](../user-group-role-and-membership/)
{% endhint %}

### Tạo mới trường

Trường Chọn mục gồm 2 [Loại trường dữ liệu (field type)](./) :

* Chọn một mục (single issue picker)
* Chọn nhiều mục (multi issue picker)

Tạo mới các trường này tương tự như các Trường dữ liệu tự tạo khác. Xem lại [guidejar hướng dẫn](truong-chon-muc.md#tong-quan) hoặc đọc thêm [tại đây](./).&#x20;

### Cấu hình trường

Khi đã tạo Trường dữ liệu với kiểu trường **Chọn một mục**, **Chọn nhiều mục**, bạn có thể cấu hình trường để phù hợp nhu cầu:

<figure><img src="../../.gitbook/assets/image (560).png" alt=""><figcaption></figcaption></figure>

{% stepper %}
{% step %}
Chọn <img src="../../.gitbook/assets/image (561).png" alt="" data-size="line"> để cấu hình các **Tiêu chí lọc (UQL)**

* Nếu không thêm các tiêu chí để lọc Mục, chọn được tất cả các Mục có trong Doanh nghiệp (business) làm giá trị cho Trường chọn mục
* Thêm các tiêu chí để lọc Mục tương tự như Tiêu chí lọc (filter medium)
*   &#x20;Bạn có thể thêm tiêu chí sắp xếp để xác định danh sách thứ tự các Mục, xem chi tiết về cơ chế sắp xếp tại đây\


    <figure><img src="../../.gitbook/assets/image (562).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
Tùy chọn **Điền tự động**

* Khi tạo Mục, điền tự động các Mục thỏa mãn Tiêu chí lọc vào trường theo thứ tự sắp xếp đã cấu hình ở trên
*   Số lượng Mục được điền tự động **từ** **1 đến 100** tùy vào cấu hình. Với loại trường **Chọn một mục** chỉ điền tự động một Mục đầu tiên theo thứ tự\


    <figure><img src="../../.gitbook/assets/image (563).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
**Lưu ý:**

Các Mục mà bạn không có quyền Xem (View) hoặc đã bị Xóa thì sẽ không được điền tự động dù có thỏa mãn các tiêu chí
{% endhint %}
{% endstep %}
{% endstepper %}

## Sử dụng

### Thao tác trên Chi tiết Mục (issue detail)

<figure><img src="../../.gitbook/assets/image (564).png" alt=""><figcaption></figcaption></figure>

* Để thêm các Mục làm giá trị của trường (tối đa 100 Mục), bạn cần có quyền Xem các Mục làm giá trị đó
* Với các Mục được chọn làm giá trị cho trường, bạn có thể Chỉnh sửa trực tiếp các thông tin nếu như bạn có quyền Chỉnh sửa các Mục đó&#x20;

{% hint style="info" %}
**Lưu ý:**

Với các Mục được chọn làm giá trị của trường nếu đã bị xóa hoặc người dùng không có quyền Xem chỉ hiển thị **Mã mục** kèm dòng chữ _'(Mục đã bị xóa hoặc bạn không có quyền)_'&#x20;
{% endhint %}

### Thao tác trên Danh sách mục (issue list)

<figure><img src="../../.gitbook/assets/image (565).png" alt=""><figcaption></figcaption></figure>

* Hiển thị Tiêu đề (title) của Mục được chọn đầu tiên và số lượng Mục được chọn còn lại (nếu nhiều hơn 1)
* Hover vào hiển thị danh sách các Mục được chọn . Click vào mở ra Mục đó

{% hint style="info" %}
**Lưu ý:**&#x20;

Với các Mục được chọn làm giá trị của trường nếu đã bị xóa hoặc người dùng không có quyền Xem chỉ hiển thị **Mã mục** (Issue Key) kèm dòng chữ _'(Mục đã bị xóa hoặc bạn không có quyền)_'&#x20;
{% endhint %}

### Lọc dữ liệu với trường

guidejar

Các toán tử để lọc dữ liệu với tiêu chí lọc là các trường Chọn mục:

{% tabs %}
{% tab title="Trường Chọn một mục" %}
Các toán tử khi lọc dữ liệu với trường Chọn một mục tương tự như các trường Sổ xuống chọn một, Chọn một nhóm,...&#x20;

<figure><img src="../../.gitbook/assets/image (566).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Trường Chọn nhiều mục" %}
Các toán tử khi lọc dữ liệu với trường Chọn nhiều mục tương tự như các trường Sổ xuống chọn nhiều, Chọn nhiều nhóm,...&#x20;

<figure><img src="../../.gitbook/assets/image (567).png" alt=""><figcaption></figcaption></figure>
{% endtab %}
{% endtabs %}

Click icon <img src="../../.gitbook/assets/image (568).png" alt="" data-size="line"> để mở ra bảng chọn giá trị: Mục cụ thể hoặc thông qua Tiêu chí lọc

{% tabs %}
{% tab title="Mục cụ thể" %}
Chọn các Mục thỏa mãn theo cấu hình của trường, các mục mà người dùng không có quyền Xem sẽ không hiển thị để lựa chọn

<figure><img src="../../.gitbook/assets/image (569).png" alt="" width="563"><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Tiêu chí lọc" %}
Thêm các tiêu chí để lọc ra Mục theo mong muốn

<figure><img src="../../.gitbook/assets/image (570).png" alt="" width="563"><figcaption></figcaption></figure>

Click icon <img src="../../.gitbook/assets/image (571).png" alt="" data-size="line"> để mở ra panel tùy chỉnh các tiêu chí lọc, cấu hình tiêu chí sắp xếp để lọc ra các Mục theo mong muốn

<figure><img src="../../.gitbook/assets/image (572).png" alt="" width="563"><figcaption></figcaption></figure>
{% endtab %}
{% endtabs %}

### Tự động (Automation) với trường

#### Rẽ nhánh (Branching)

Bạn có thể chuyển tới các Mục là giá trị của trường **Chọn một mục**, **Chọn nhiều mục** (xem chi tiết [tại đây](../universal-automation/cau-hinh-automation/flow-logic-automation/branching.md))

#### Cập nhật trường (Update field)

Tự động cập nhật giá trị trường **Chọn một mục**, **Chọn nhiều mục** (xem chi tiết [tại đây](../universal-automation/cau-hinh-automation/action-automation/cap-nhat-truong-chon-muc.md))

#### Smart values

Sử dụng giá trị của trường **Chọn một mục**, **Chọn nhiều mục** qua các câu **Smart values** (xem chi tiết tại đây)
