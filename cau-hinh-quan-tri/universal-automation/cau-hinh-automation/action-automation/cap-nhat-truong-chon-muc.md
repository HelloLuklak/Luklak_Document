# Cập nhật trường chọn mục

## Tổng quan

Action cập nhật trường cho phép tự động thay đổi hoặc xóa các giá trị (mục) trong các trường [Chọn một mục](broken-reference) (Single issue picker), [Chọn nhiều mục](cap-nhat-truong-chon-muc.md#chon-nhieu-muc) (Multi issue picker). Tính năng này đặc biệt hữu ích trong việc tối ưu hóa luồng công việc bằng cách tự động hóa các mối liên kết giữa các mục, giảm thiểu sai sót thủ công và đảm bảo dữ liệu luôn được cập nhật chính xác.



### User-flow

{% tabs %}
{% tab title="Chọn một mục" %}
<figure><img src="../../../../.gitbook/assets/image (626).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Chọn nhiều mục" %}
<figure><img src="../../../../.gitbook/assets/image (627).png" alt=""><figcaption></figcaption></figure>
{% endtab %}
{% endtabs %}

### Ví dụ sử dụng thực tế

{% tabs %}
{% tab title="Chọn một mục" %}
Trong quản lý công việc, mỗi loại công việc thường liên quan đến một đối tác cụ thể. Bạn có thể thiết lập **Quy tắc tự động** để khi trường **Loại công việc** được thay đổi, hệ thống sẽ tự động cập nhật trường **Đối tác** (một trường dạng **Chọn một mục**) với mục đại diện cho công ty đối tác phù hợp.

<figure><img src="../../../../.gitbook/assets/image (628).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Chọn nhiều mục" %}
Trong quy trình tuyển dụng, thay vì phải thủ công thêm các ứng viên xuất sắc vào trường **Danh sách ứng viên nổi bật** (trường Chọn nhiều mục) của mục **Tuyển dụng**, bạn có thể dùng hành động tự động cập nhật trường **Danh sách ứng viên nổi bật** khi đạt tiêu chí như điểm đánh giá cao

<figure><img src="../../../../.gitbook/assets/image (629).png" alt=""><figcaption></figcaption></figure>
{% endtab %}
{% endtabs %}

## Cấu hình

Người dùng cần xác định Cách cập nhật, Dữ liệu đầu vào để cập nhật dữ liệu cho các trường Chọn mục

{% tabs %}
{% tab title="Chọn một mục" %}
<figure><img src="../../../../.gitbook/assets/image (630).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Chọn nhiều mục" %}
<figure><img src="../../../../.gitbook/assets/image (631).png" alt=""><figcaption></figcaption></figure>
{% endtab %}
{% endtabs %}

### Cách cập nhật

Có thể đáp ứng mọi nhu cầu của người dùng với nhiều lựa chọn

<figure><img src="../../../../.gitbook/assets/image (632).png" alt=""><figcaption></figcaption></figure>

> **✨ Ví dụ:**
>
> * _Ghi đè_: giá trị của trường cần cập nhật là A, B; giá trị trong Dữ liệu đầu vào là C, D, E -> Khi cập nhật: giá trị của trường thành C, D, E
> * _Bổ sung_: giá trị của trường cần cập nhật là A, B; giá trị trong Dữ liệu đầu vào là C, D, E -> Khi cập nhật: giá trị của trường thành A, B, C, D, E
> * _Loại bỏ:_ giá trị của trường cần cập nhật là A, B, C; giá trị trong Dữ liệu đầu vào là C, D -> Khi cập nhật: giá trị của trường thành A, B
> * _Xóa trống:_ giá trị của trường cần cập nhật là A, B, C -> Khi cập nhật: giá trị của trường thành trống

### Dữ liệu đầu vào

Xác định các giá trị để cập nhật cho trường, giá trị nào đưa vào thỏa mãn cấu hình của trường thì sẽ được cập nhật

<figure><img src="../../../../.gitbook/assets/image (633).png" alt=""><figcaption></figcaption></figure>

{% stepper %}
{% step %}
Xác định **Nguồn dữ liệu**

Click vào icon <img src="../../../../.gitbook/assets/image (634).png" alt="" data-size="line"> để mở ra bảng lựa chọn các giá trị

{% tabs %}
{% tab title="Mục cụ thể" %}
Chọn các Mục trong hệ thống thỏa mãn theo cấu hình của trường cần cập nhật.

**Lưu ý:** Các Mục mà người dùng không có quyền Xem sẽ không hiển thị ở đây

<figure><img src="../../../../.gitbook/assets/image (635).png" alt="" width="563"><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Tiêu chí lọc" %}
Sử dụng bộ lọc UQL để chọn ra được các Mục theo mong muốn

<figure><img src="../../../../.gitbook/assets/image (636).png" alt="" width="563"><figcaption></figcaption></figure>

Click vào icon <img src="../../../../.gitbook/assets/image (637).png" alt="" data-size="line"> để mở ra panel cấu hình các Tiêu chí lọc. Cách cấu hình tương tự như Lọc nhanh (Quick filter)

<figure><img src="../../../../.gitbook/assets/image (638).png" alt="" width="563"><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Mục kích hoạt / Mục cha / Mục hiện tại" %}
Lấy giá trị là các Mục đặc biệt (mục con, mục cha) hoặc giá trị của các trường Chọn mục của các Mục liên quan (Mục kích hoạt ,Mục cha, Mục hiện tại)

<figure><img src="../../../../.gitbook/assets/image (639).png" alt="" width="563"><figcaption></figcaption></figure>

* Nguồn dữ liệu Mục hiện tại chỉ khả dụng khi sử dụng action Cập nhật trường trong Rẽ nhánh (branching), để lấy giá trị của Mục rẽ nhánh sang
* Khi lấy mục con của Mục liên quan, người dùng có thể click vào <img src="../../../../.gitbook/assets/image (640).png" alt="" data-size="line"> để lọc các mục con muốn lấy, nếu không sẽ là tất cả các mục con
{% endtab %}
{% endtabs %}
{% endstep %}

{% step %}
**Cách cắt chọn**

{% hint style="info" %}
**Lưu ý:**&#x20;

Mặc định lựa chọn Cắt chọn là theo trường Cập nhật và áp dụng cho 3 Mục đầu tiên, người dùng cần thay đổi theo nhu cầu để tránh sai sót

Với loại trường Chọn một mục, sẽ luôn là áp dụng cho Mục đầu tiên
{% endhint %}

<figure><img src="../../../../.gitbook/assets/image (641).png" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}
