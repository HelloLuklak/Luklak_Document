# Branching

## Tổng quan

Trong [Luklak](https://luklak.com/vi/), các Mục (issue) rất hiếm khi tồn tại độc lập, chúng thường được liên kết với các Mục khác qua Kết nối mục (issue link) hay trường Chọn mục (issue picker filed), chứa các Mục con (sub-tasks) hay thuộc về một Mục nào đó.&#x20;

Do đó khi xây dựng các quy trình Tự động hóa (automation), bạn không chỉ áp dụng Hành động (action) cho Mục kích hoạt hành động (trigger issue) mà còn có thể mở rộng các Hành động tới các Mục liên quan khác. &#x20;

{% embed url="https://guidejar.com/guides/5ea4cc2e-4fea-4601-9c0f-a58e7d65dd0d" %}



### User-flow

<figure><img src="../../../../.gitbook/assets/image (552).png" alt=""><figcaption></figcaption></figure>

### Ví dụ sử dụng thực tế

Khi thực hiện dự án, bạn sẽ có nhiều hạng mục công việc cần thực hiện. Để quản lý tiến độ dự án bạn có thể tạo các hạng mục công việc là <img src="../../../../.gitbook/assets/image (53).png" alt="" data-size="line"> _Mục con (sub-tasks)_ cho dự án, thiết lập <img src="../../../../.gitbook/assets/image (55).png" alt="" data-size="line"> _Quy tắc tự động_ để mỗi khi hạng mục công việc cập nhật tiến độ thì tiến độ của dự án cũng được cập nhật theo

<figure><img src="../../../../.gitbook/assets/image (553).png" alt=""><figcaption></figcaption></figure>

## Cấu hình

Lựa chọn các điều kiện để chuyển có thể chuyển tới các Mục mong muốn và thực hiện hành động với các Mục đó

<figure><img src="../../../../.gitbook/assets/image (554).png" alt=""><figcaption></figcaption></figure>

### Lọc mục qua UQL

Rẽ nhánh sang các Mục thỏa mãn các điều kiện cụ thể thông qua UQL.

<figure><img src="../../../../.gitbook/assets/image (555).png" alt=""><figcaption></figcaption></figure>

{% stepper %}
{% step %}
Thêm các **tiêu chí lọc UQL**

* Bạn cần cấu hình ít nhất 1 tiêu chí lọc
* Thêm các tiêu chí tương tự như Tiêu chí lọc (filter medium)
{% endstep %}

{% step %}
Cấu hình **Cách cắt chọn**

* **Tất cả các mục thỏa mãn:** lọc ra 100 mục đầu tiên thỏa mãn theo tiêu chí lọc ở trên
* **Cài đặt nâng cao:** Thêm trường dữ liệu làm tiêu chí để sắp xếp các Mục thỏa mãn ở trên
{% endstep %}
{% endstepper %}

### Mục cha

Rẽ nhánh qua Mục cha của Mục kích hoạt hành động (trigger issue)

### Mục con

Rẽ nhánh qua tất cả các Mục con của Mục kích hoạt hành động

{% hint style="info" %}
Bạn có thể sử dụng bộ lọc UQL và Cách cắt chọn để giới hạn các Mục con muốn rẽ nhánh
{% endhint %}

### Mục từ trường chọn mục

Rẽ nhánh qua các Mục là giá trị của trường Chọn mục (issue picker field) ở Mục kích hoạt hành động

<figure><img src="../../../../.gitbook/assets/image (556).png" alt=""><figcaption></figcaption></figure>

{% stepper %}
{% step %}
**Cấu hình:** Lấy ra các Mục là giá trị của các trường Chọn mục được chọn
{% endstep %}

{% step %}
**Điều kiện lọc:** Lọc các Mục được lấy ra ở cấu hình trên theo các tiêu chí lọc UQL
{% endstep %}

{% step %}
Thêm **Cách cắt chọn** để chọn ra được các Mục mong muốn

* **Tất cả các mục thỏa mãn:** lọc ra 100 mục đầu tiên thỏa mãn theo tiêu chí lọc ở trên
* **Cài đặt nâng cao:** Thêm trường dữ liệu làm tiêu chí để sắp xếp các Mục thỏa mãn ở trên
{% endstep %}
{% endstepper %}

### Mục được tạo

Rẽ nhánh qua tất cả các Mục được tạo từ các Hành động trước trong quy tắc

{% hint style="info" %}
Bạn có thể sử dụng bộ lọc UQL và Cách cắt chọn để giới hạn các Mục được tạo muốn rẽ nhánh
{% endhint %}

### Mục được tạo gần nhất

Rẽ nhánh qua Mục được tạo ra gần nhất từ các Hành động trước trong quy tắc

### Mục có kết nối

Rẽ nhánh qua tất cả các Mục có kết nối (issue link) với Mục kích hoạt hành động

<figure><img src="../../../../.gitbook/assets/image (557).png" alt=""><figcaption></figcaption></figure>

{% stepper %}
{% step %}
**Cấu hình:** Lấy ra các Mục có kết nối tới Mục kích hoạt hành động thuộc các loại kết nối được chọn
{% endstep %}

{% step %}
**Điều kiện lọc:** Lọc các Mục được lấy ra ở cấu hình trên theo các tiêu chí lọc UQL
{% endstep %}

{% step %}
Thêm **Cách cắt chọn** để chọn ra được các Mục mong muốn

* **Tất cả các mục thỏa mãn:** lọc ra 100 mục đầu tiên thỏa mãn theo tiêu chí lọc ở trên
* **Cài đặt nâng cao:** Thêm trường dữ liệu làm tiêu chí để sắp xếp các Mục thỏa mãn ở trên
{% endstep %}
{% endstepper %}

### Mục được kết nối đến

Hiện tại tính năng này Luklak chưa hỗ trợ
