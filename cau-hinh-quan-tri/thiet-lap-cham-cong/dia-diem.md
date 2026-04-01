# Địa điểm

{% embed url="https://guidejar.com/guides/515c8df5-b5b9-4147-9548-4c095164a5f4" %}

## 1. Tổng quan

**Địa điểm** (Location) là các quy định về yêu cầu, điều kiện chấm công: GPS, Wi-Fi (MAC address), IP address hoặc Livephoto. Nhân sự phải đáp ứng các điều kiện này mới có thể chấm công, giúp kiểm soát chấm công chính xác hơn, tránh tình trạng chấm công hộ hoặc chấm công từ xa không hợp lệ.

<figure><img src="../../.gitbook/assets/image (26).png" alt=""><figcaption></figcaption></figure>

## 2. Thiết lập & Quản lý

{% hint style="info" %}
Người dùng có quyền mới có thể thiết lập Địa điểm, [**xem chi tiết tại đây 📚**](phan-quyen.md)
{% endhint %}

### 2.1. Tạo mới Địa điểm

Tại màn hình Danh sách các Địa điểm, click icon <img src="../../.gitbook/assets/image (4) (1).png" alt="" data-size="line"> để mở giao diện tạo mới địa điểm

{% hint style="success" %}
**Gợi ý 💡:**

* Có thể kết hợp nhiều điều kiện (GPS, IP Address, MAC Address) để đảm bảo tính chính xác khi chấm công.
* Nếu muốn nhân sự chấm công mà không cần điều kiện ràng buộ**c**, chỉ cần tạo **Địa điểm** mà không thiết lập bất kỳ điều kiện nào.
{% endhint %}

Tùy vào quy định của từng Doanh nghiệp mà thiết lập các điều kiện khác nhau

* **GPS**: Nhân sự chỉ có thể chấm công khi đang ở trong phạm vi cho phép

<details>

<summary>Thiết lập GPS</summary>

Người dùng có thể thêm nhiều địa chỉ/tọa độ khác nhau cho điều kiện về GPS, nhân sự chỉ cần đáp ứng một trong các địa chỉ đó là có thể chấm công

{% hint style="info" %}
**Lưu ý:**

* Trong trường hợp có phạm vi làm việc lớn như công trường hoặc có nhiều địa điểm làm việc nên thêm nhiều địa chỉ/tọa độ khác nhau
* Nếu không thêm bất kỳ địa chỉ/tọa độ nào, nhân sự có thể chấm công ở bất kì vị trí nào
{% endhint %}

<figure><img src="../../.gitbook/assets/image (27).png" alt=""><figcaption></figcaption></figure>

Click <img src="../../.gitbook/assets/image (28).png" alt="" data-size="line"> , chọn tọa độ và phạm vi bán kính cho từng địa chỉ

<figure><img src="../../.gitbook/assets/image (29).png" alt="" width="563"><figcaption></figcaption></figure>

</details>

* **Wi-Fi (MAC address):** Nhân sự chỉ có thể chấm công khi điện thoại kết nối với mạng Wi-Fi đươc quy định

<details>

<summary>Thiết lập Wi-Fi (MAC address)</summary>

{% hint style="info" %}
Người dùng hãy liên hệ tới bộ phận IT của Doanh nghiệp hoặc bên thiết lập hệ thống mạng để nhập chính xác tên Wi-Fi và MAC address tương ứng
{% endhint %}

Người dùng có thể thêm danh sách tên Wi-Fi và MAC Address tương ứng để làm điều kiện xác thực chấm công, điện thoại của nhân sự chỉ cần kết nối với một trong các mạng trên là có thể chấm công

{% hint style="info" %}
**Lưu ý:**

* Cần nhập chính xác cả tên Wi-Fi (SSID) và địa chỉ MAC của thiết bị phát Wi-Fi. Nếu nhập sai hoặc thiếu thông tin, nhân sự sẽ không thể chấm công khi kết nối mạng đó
* Nếu không thêm bất kỳ tên Wi-Fi hay MAC nào, nhân sự có thể chấm công từ mạng bất kỳ.
{% endhint %}

<figure><img src="../../.gitbook/assets/image (30).png" alt=""><figcaption></figcaption></figure>

#### 💡 Cách lấy tên Wi-Fi và MAC address

* _**Yêu cầu:**_&#x20;
  * Máy tính chạy hệ điều hành Windows (Windows 7, 8, 10, hoặc 11).
  * Máy tính có kết nối Wi-Fi (Wi-Fi phải được bật).
*   _**Các bước thực hiện**_:

    * Nhấn tổ hợp **Windows + R**, gõ `cmd` và nhấn **Enter**

    <figure><img src="../../.gitbook/assets/image (31).png" alt="" width="304"><figcaption></figcaption></figure>



    * Tại giao diện `cmd`, nhập câu lệnh **`netsh wlan show networks mode=Bssid`**&#x20;

    <figure><img src="../../.gitbook/assets/image (32).png" alt="" width="563"><figcaption></figcaption></figure>

    * Hệ thống sẽ hiển thị danh sách các Wi-Fi xung quanh. Mỗi Wi-Fi sẽ có:
      * **SSID (Tên Wi-Fi)**
      * **BSSID** (chính là địa chỉ **MAC** của thiết bị phát Wi-Fi)

    <figure><img src="../../.gitbook/assets/image (33).png" alt="" width="563"><figcaption></figcaption></figure>

    * Xác định đúng tên Wi-Fi đang sử dụng và nhập đủ các địa chỉ MAC tương ứng vào cấu hình Địa điểm.

</details>

* **IP address**: Nhân sự chỉ có thể chấm công khi điện thoại kết nối với đúng địa chỉ IP nội bộ của công ty

<details>

<summary>Thiết lập IP address</summary>

{% hint style="info" %}
Sử dụng nếu công ty sử dụng mạng nội bộ. Người dùng hãy liên hệ tới bộ phận IT của Doanh nghiệp hoặc bên thiết lập hệ thống mạng để nhập chính xác địa chỉ IP
{% endhint %}

Người dùng có thể thêm danh sách các địa chỉ IP để để làm điều kiện xác thực chấm công, điện thoại của nhân sự chỉ cần kết nối với một trong các địa chỉ IP trên là có thể chấm công

{% hint style="info" %}
**Lưu ý:**

* Cần nhập chính xác địa chỉ IP mạng của văn phòng. Nếu nhập sai hoặc thiếu thông tin, nhân sự sẽ không thể chấm công khi kết nối mạng đó
* Nếu không thêm bất kỳ địa chỉ IP nào, nhân sự có thể chấm công từ mạng bất kỳ
{% endhint %}

<figure><img src="../../.gitbook/assets/image (34).png" alt=""><figcaption></figcaption></figure>

</details>

Ngoài ra, người dùng có thể thêm các tùy chỉnh khác

* Yêu cầu livephoto khi chấm công: cần chụp ảnh livephoto để xác nhận chấm công
* Cho phép chấm công ngoài địa điểm: nhân sự có thể chấm công dù không đáp ứng các điều kiện về GPS, Wi-Fi (MAC address) hay IP address

### 2.2. Nhân bản Địa điểm

Chọn <img src="../../.gitbook/assets/image (13).png" alt="" data-size="line"> -> <img src="../../.gitbook/assets/image (14).png" alt="" data-size="line"> ở địa điểm bất kỳ để nhân bản

{% hint style="success" %}
**Gợi ý 💡:**&#x20;

Nếu cần tạo một địa điểm mới có điều kiện về GPS, Wifi,... tương tự địa điểm đã có, hãy nhân bản thay vì thiết lập lại từ đầu
{% endhint %}

### 2.3. Sửa Địa điểm

Người dùng có thể chỉnh sửa lại thông tin, thiết lập của Địa điểm để phù hợp với chính sách, thay đổi của Doanh nghiệp

{% hint style="info" %}
**Lưu ý:** Khi thay đổi về điều kiện, quy định của địa điểm: Nếu trong ngày hôm đó đã có dữ liệu chấm công của nhân sự, kết quả chấm công có thể bị sai lệch
{% endhint %}

### 2.4. Xóa Địa điểm

Chọn <img src="../../.gitbook/assets/image (13).png" alt="" data-size="line"> -> <img src="../../.gitbook/assets/image (16) (1).png" alt="" data-size="line">  để thực hiện việc xóa địa điểm

{% hint style="info" %}
**Lưu ý**:

* Không thể xóa Địa điểm đang được sử dụng trong Quy tắc chấm công
* Việc xóa Địa điểm có thể ảnh hưởng đến dữ liệu chấm công của nhân sự, vì vậy cần kiểm tra kỹ trước khi thực hiện.
{% endhint %}

## 💡 FAQs

<details>

<summary>Làm sao để tạo Địa điểm không có yêu cầu về điều kiện nào khi chấm công?</summary>

👉 Người dùng chỉ cần không chọn hay thêm bất kỳ thiết lập nào cho GPS, Wi-Fi (MAC address) và IP address

</details>

