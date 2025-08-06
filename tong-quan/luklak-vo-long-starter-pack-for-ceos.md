---
description: >-
  Trọn bộ hướng dẫn để chủ doanh nghiệp bắt đầu thiết kế hệ thống & vận hành
  trên Luklak
hidden: true
icon: memo-pad
---

# Luklak vỡ lòng (Starter pack for CEOs)

## Hệ thống Luklak

<figure><img src="../.gitbook/assets/image (467).png" alt=""><figcaption></figcaption></figure>

{% hint style="success" %}
**Giao diện & logic hợp nhất**: Người dùng chỉ cần tìm hiểu giao diện & logic hệ thống một lần, sẽ có thể tự xây dựng mọi chức năng vận hành.&#x20;
{% endhint %}

### Giao diện



{% tabs %}
{% tab title="TỔNG THỂ" %}
<figure><img src="../.gitbook/assets/Cấu trúc UI chung.gif" alt=""><figcaption><p>1 giao diện hợp nhất để vận hành nhiều chức năng.</p></figcaption></figure>

<figure><img src="../.gitbook/assets/highlighted-GIF-2-v2.gif" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="VẬN HÀNH HẰNG NGÀY" %}


<figure><img src="../.gitbook/assets/Các thành phần trong Issue.gif" alt=""><figcaption><p>Phần lớn công việc hằng ngày diễn ra trong mảng việc, nơi mọi thành viên trong tổ chức làm việc, trao đổi, giám sát.</p></figcaption></figure>

What can happen inside a Space?

Take a peek (thực tế làm việc)
{% endtab %}
{% endtabs %}

<details>

<summary>Các thành phần chính cấu thành giao diện</summary>

<mark style="color:blue;">Main menu</mark>

* Phòng làm việc:&#x20;
* Cá nhân:&#x20;
* Thông báo:
* Chat riêng:
* Mở rộng:

<mark style="color:blue;">Structure column</mark>

<mark style="color:blue;">Content Area</mark>

<mark style="color:blue;">Issue Detail</mark>

<mark style="color:blue;">Issue Types</mark>

<mark style="color:blue;">Filter</mark>

<mark style="color:blue;">Quick Action</mark>

</details>

Hoạt động diễn ra hằng ngày trong mảng việc

### Logic hệ thống

{% hint style="info" %}
**Tự tin thiết kế chức năng**: Các miếng lego của hệ thống Luklak Nocode vừa độc lập, vừa có liên quan chặt chẽ. Hiểu mối liên kết giữa chúng, người dùng có thể tự tin thiết kế mọi chức năng.
{% endhint %}

#### Tổ chức - Khu vực - Mảng việc - Chức năng

<figure><img src="../.gitbook/assets/image (435).png" alt=""><figcaption></figcaption></figure>

#### Mảng việc - Các đối tượng bên trong

<figure><img src="../.gitbook/assets/image (443).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (451).png" alt=""><figcaption><p>Ví dụ các Mục việc tiêu chuẩn &#x26; Mục việc con trực thuộc mảng việc Sales &#x26; CRM</p></figcaption></figure>

{% hint style="info" %}
**Dữ liệu công việc - Cập nhật - Chat trao đổi hợp nhất**: Mảng việc là nơi nhân sự trực tiếp làm việc, trao đổi, tương tác & nắm bắt cập nhật. Lần đầu tiên, dữ liệu về đầu việc & chat trao đổi về công việc đó được hợp nhất một nơi, trong cấu trúc mảng việc.
{% endhint %}

#### Chức năng - Mảng việc - Người dùng

{% hint style="info" %}
**Mảng việc được sinh ra từ chức năng**: Chức năng quyết định Mảng việc sẽ có những _nghiệp vụ, thông tin dữ liệu, quy trình làm việc, tự động hóa, và báo cáo gì, phân quyền & thông báo_ như thế nào.
{% endhint %}

#### Chức năng - Các miếng lego

<figure><img src="../.gitbook/assets/image (452).png" alt=""><figcaption><p>Sơ đồ mối liên hệ logic giữa các miếng lego.</p></figcaption></figure>

<details>

<summary>Giải thích</summary>

* **Các Thành Phần của một Chức Năng:**
  * Sơ đồ cho thấy cách một **chức năng** được xây dựng từ nhiều yếu tố cốt lõi:
    * **Mục việc**: Nhiệm vụ hoặc đối tượng trung tâm cần quản lý.
    * **Trường Tùy Chỉnh**: Thông tin bổ sung hoặc điểm dữ liệu có thể điều chỉnh để phù hợp với yêu cầu cụ thể.
    * **Quy Trình**: Quá trình hoặc chuỗi các bước mà một mục việc phải trải qua.
    * **Trò Chuyện về Mục Việc**: Cho phép giao tiếp theo thời gian thực trong bối cảnh của mỗi nhiệm vụ hoặc mục việc.
    * **Bộ lọc/NQL**: Khả năng lọc sử dụng Ngôn Ngữ Truy Vấn Tự Nhiên của Luklak để truy xuất dữ liệu cụ thể.
    * **Sơ Đồ Phân Quyền**: Xác định ai có quyền truy cập và những hành động nào họ được phép thực hiện đối với mục việc.
    * **Sơ Đồ Thông Báo**: Xác định ai nhận được thông báo khi có thay đổi xảy ra.
    * **Hộp Thư Thống Nhất**: Tập hợp tất cả thông báo, tin nhắn và cập nhật vào một nơi.
    * **Tự Động Hóa**: Cho phép kích hoạt tự động, logic và hành động dựa trên các thay đổi hoặc điều kiện.
    * **Tích Hợp**: Cho phép chức năng tương tác với các hệ thống bên ngoài thông qua webhook và API.

- **Luồng Hoạt Động:**
  * **Mục việc** là trung tâm của chức năng, và nó **bao gồm** các trường tùy chỉnh, quy trình và trò chuyện.
  * Những thay đổi trong các yếu tố này (cập nhật trường tùy chỉnh, các bước quy trình, v.v.) hoạt động như **bộ kích hoạt** cho các thông báo hoặc quy tắc tự động hóa.
  * **Sơ Đồ Phân Quyền** kiểm soát ai có thể truy cập hoặc sửa đổi mục việc, và **Sơ Đồ Thông Báo** quyết định ai được thông báo về các thay đổi.
  * Các quy tắc tự động hóa dựa trên các bộ kích hoạt, và những quy tắc này thực hiện các hành động đã được xác định trước sử dụng logic (như thay đổi một trường hoặc thông báo cho một người).
  * Dữ liệu thu thập từ các mục việc có thể được sử dụng để tạo báo cáo thông qua **Bộ lọc/NQL**, được hiển thị trên **Bảng Điều Khiển**.
  * **Hộp Thư Thống Nhất** tổng hợp tất cả các cập nhật và thông báo liên quan, giúp các thành viên trong nhóm dễ dàng cập nhật thông tin.

* **Tự Động Hóa & Tích Hợp:**
  * **Quy Tắc Tự Động Hóa**: Phần này giải thích cách bạn có thể thiết lập các quy trình tự động được kích hoạt bởi các thay đổi trong mục việc.
  * **Kích Hoạt, Logic Luồng, Hành Động**: Các quy tắc tự động hóa dựa trên những yếu tố này:
    * **Kích Hoạt**: Một điều kiện hoặc sự kiện bắt đầu quá trình tự động hóa.
    * **Logic Luồng**: Quá trình ra quyết định xác định cách thức tiến hành tự động hóa.
    * **Hành Động**: Nhiệm vụ được thực hiện tự động, như gửi thông báo hoặc cập nhật các trường.
  * **Tích Hợp, Webhook, API**: Những điều này cho phép các hệ thống bên ngoài tương tác với Luklak, nâng cao hơn nữa chức năng.&#x20;

</details>

#### Tổng thể: Chức năng - Mục việc - Mảng việc - Khu Vực - Tổ chức - Người dùng

<figure><img src="../.gitbook/assets/image (432).png" alt=""><figcaption></figcaption></figure>

#### Ví dụ Phòng làm việc

<figure><img src="../.gitbook/assets/image (449).png" alt=""><figcaption><p>Ví dụ Phòng làm việc "Đào tạo nhân sự Marketing", được tạo ra nhằm tăng tốc việc đào tạo. Phòng làm việc này có chứa các mảng việc, báo cáo, bộ lọc thực sự cần thiết cho việc đào tạo này, được kéo về từ Tổ chức. </p></figcaption></figure>



## <mark style="color:blue;">Xác định bài toán vận hành</mark>



{% hint style="success" %}
**Doanh nghiệp mẫu:** \
\
Tên: **GIFTIFY**\
Lĩnh vực: Bán hộp quà, túi giấy, bao bì thiết kế theo yêu cầu\
Các phòng ban chính: \
Quy trình:\
Tự động hóa:

Báo cáo:\
Bộ lọc:\

{% endhint %}

### Cấu trúc tổ chức & công việc

<figure><img src="../.gitbook/assets/image (113).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (456).png" alt=""><figcaption><p>Tự tay thiết kế cấu trúc tổ chức &#x26; công việc linh hoạt, mở rộng đa chiều &#x26; liên kết chặt chẽ với nhau.</p></figcaption></figure>

<figure><img src="../.gitbook/assets/image (459).png" alt=""><figcaption><p>Ví dụ cách thiết kế cấu trúc tổ chức của Công ty GIFTIFY theo 3 cách khác nhau, linh hoạt phù hợp với quy mô, cơ cấu, cách thức vận hành của doanh nghiệp.</p></figcaption></figure>

<figure><img src="../.gitbook/assets/image (455).png" alt=""><figcaption></figcaption></figure>

### Quy trình (e.g. Thiết kế trên Draw.io)

{% tabs %}
{% tab title="QUY TRÌNH 1" %}

{% endtab %}

{% tab title="QUY TRÌNH 2" %}
{% embed url="https://guidejar.com/guides/0e07638f-81ef-446c-b183-6bb35cdfd76d" %}


{% endtab %}

{% tab title="QUY TRÌNH 3" %}

{% endtab %}
{% endtabs %}

### Tự động hóa

{% tabs %}
{% tab title="QUY MÔ MẢNG VIỆC" %}

{% endtab %}

{% tab title="QUY MÔ LIÊN PHÒNG BAN" %}

{% endtab %}
{% endtabs %}

## <mark style="color:blue;">Thiết kế giải pháp</mark>

<figure><img src="../.gitbook/assets/image (466).png" alt=""><figcaption></figcaption></figure>

### Cấu trúc tổ chức

<figure><img src="../.gitbook/assets/image (113).png" alt=""><figcaption></figcaption></figure>

### Chức năng vận hành

{% tabs %}
{% tab title="LUỒNG LIÊN CHỨC NĂNG" %}
<figure><img src="../.gitbook/assets/luồng tổng TCS.drawio.png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="CHỨC NĂNG 1" %}

{% endtab %}

{% tab title="CHỨC NĂNG 2" %}

{% endtab %}

{% tab title="CHỨC NĂNG 3" %}

{% endtab %}
{% endtabs %}

## <mark style="color:blue;">Vận hành thực tế</mark>

<figure><img src="../.gitbook/assets/image (465).png" alt=""><figcaption></figcaption></figure>

{% tabs %}
{% tab title="LÀM VIỆC" %}
<figure><img src="../.gitbook/assets/Các thành phần trong Issue (2).gif" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="GIAO TIẾP" %}
<figure><img src="../.gitbook/assets/Chat-da-tang-3 (1) (2).gif" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="QUẢN LÝ" %}
<figure><img src="../.gitbook/assets/Search-and-filter-GIF-v2 (1).gif" alt=""><figcaption><p>Kết hợp Bộ lọc + Newsfeed</p></figcaption></figure>
{% endtab %}
{% endtabs %}

{% embed url="https://youtu.be/38tvVjhEFaY" %}



## <mark style="color:blue;">Nâng tầm quản lý</mark>

<figure><img src="../.gitbook/assets/image (464).png" alt=""><figcaption></figcaption></figure>

{% tabs %}
{% tab title="TỰ ĐỘNG HÓA" %}
Tăng cường tự động hóa (universal automation)
{% endtab %}

{% tab title="BÁO CÁO THÔNG SUỐT" %}
Quản lý thông tin hợp nhất (unified data & system)

<figure><img src="../.gitbook/assets/image (390).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (391).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/dashboard GIF (1).gif" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="NẮM BẮT & PHỐI HỢP" %}
Nắm bắt cập nhật hiệu quả (unified inbox)

<figure><img src="../.gitbook/assets/Search-and-filter-GIF-v2.gif" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="PHÂN QUYỀN CHẶT CHẼ" %}
<figure><img src="../.gitbook/assets/image (85).png" alt=""><figcaption></figcaption></figure>
{% endtab %}
{% endtabs %}



## <mark style="color:blue;">FAQs</mark>

<details>

<summary>Triển khai có tốn nhiều nguồn lực không?</summary>



</details>

<details>

<summary>Lợi ích đầu tư cho doanh nghiệp</summary>



</details>
