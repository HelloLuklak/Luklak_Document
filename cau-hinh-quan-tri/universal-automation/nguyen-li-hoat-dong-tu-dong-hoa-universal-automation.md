# Nguyên lí hoạt động - Tự động hóa (Universal Automation)

{% @guidejar/embed guideId="2219847e-4891-4073-b3e5-25b128586a03" type="1" controls="on" url="https://www.guidejar.com/embed/2219847e-4891-4073-b3e5-25b128586a03?type=1&controls=on" %}

## Automation - Bộ não của hệ thống

{% hint style="info" %}
<img src="../../.gitbook/assets/image (512).png" alt="" data-size="line">**Universal Automation** là một miếng lego của Luklak Nocode & Lowcode, cho phép tự động _kết nối dữ liệu từ mọi Object, xử lý logic và tự động hóa_ đa dạng tác vụ cho doanh nghiệp. Giải phóng nhân sự khỏi các thao tác thủ công, tăng hiệu suất & độ chính xác.
{% endhint %}

<figure><img src="../../.gitbook/assets/image (513).png" alt="" width="176"><figcaption></figcaption></figure>

### Ví dụ thực tế

* **Marketing**: Khi Khách đăng kí trên website, tự động tạo <img src="../../.gitbook/assets/image (514).png" alt="" data-size="line"> **Lead** trong Mảng việc <img src="../../.gitbook/assets/image (515).png" alt="" data-size="line">, và điền giá trị trường <img src="../../.gitbook/assets/image (516).png" alt="" data-size="line"> `nguồn khách` = <img src="../../.gitbook/assets/image (517).png" alt="" data-size="line"> **Ad** tương ứng
* **Sales**: Khi Kinh doanh chốt khách <img src="../../.gitbook/assets/image (518).png" alt="" data-size="line">, tự động bắn chat chúc mừng vào <img src="../../.gitbook/assets/image (519).png" alt="" data-size="line">kênh chat của kinh doanh
* **Thiết kế:** Khi khách ký <img src="../../.gitbook/assets/image (520).png" alt="" data-size="line"> [**Hợp đồng**](#user-content-fn-1)[^1], tự động chuyển link yêu cầu của khách từ <img src="../../.gitbook/assets/image (521).png" alt="" data-size="line"> **Customer** sang <img src="../../.gitbook/assets/image (522).png" alt="" data-size="line">**Yêu cầu thiết kế**, ở trường <img src="../../.gitbook/assets/image (523).png" alt="" data-size="line">`Yêu cầu`

## 3 yếu tố cấu thành quy tắc Automation



Mỗi Quy tắc Automation được tạo nên từ 3 nguyên liệu chính:

### <img src="../../.gitbook/assets/image (524).png" alt="" data-size="line"> Kích hoạt (Trigger)

{% hint style="info" %}
**Trigger** cho phép người dùng định nghĩa điểm khởi đầu kích hoạt một quy tắc, khi có sự kiện gì đó xảy ra. Automation có thể lắng nghe kích hoạt từ **cả trong & ngoài** hệ thống Luklak
{% endhint %}

<figure><img src="../../.gitbook/assets/image (525).png" alt=""><figcaption><p>Các loại Trigger</p></figcaption></figure>

#### 2 cách kích hoạt

**Kích hoạt thủ công**: Người dùng tự tạo nút ấn trên Object, khi chủ động ấn sẽ kích hoạt quy tắc

<div align="center"><figure><img src="../../.gitbook/assets/image (526).png" alt="" width="375"><figcaption><p>VD: Kế toán tự ấn nút Tạo Phiêu Thu để kích hoạt Quy tắc <br>Tự động tạo mục phiếu thu</p></figcaption></figure></div>

**Kích hoạt chạy ngầm:** Hệ thống tự động bắt sự kiện, người dùng không cần ấn nút.

* <img src="../../.gitbook/assets/image (527).png" alt="" data-size="line">Tạo Nghiệp vụ ( Create Object ) : Khi một Mục/Nghiệp vụ (Object) hoặc Nghiệp vụ con (Sub-Object) được tạo
* <img src="../../.gitbook/assets/image (528).png" alt="" data-size="line"> Chuyển Trạng thái ( Change Status ): Khi trạng thái của một Nghiệp vụ/Nghiệp vụ con được chuyển
* <img src="../../.gitbook/assets/image (529).png" alt="" data-size="line"> Cập nhật trường ( Update Fields ): Khi một Trường dữ liệu của Nghiệp vụ được cập nhật.
* <img src="../../.gitbook/assets/image (530).png" alt="" data-size="line">Lịch trình ( Schedule ): Khi đến một thời điểm nhất định
* <img src="../../.gitbook/assets/image (531).png" alt="" data-size="line">Webhook: Khi nhận được webhook từ hệ thống ngoài.

### <img src="../../.gitbook/assets/image (532).png" alt="" data-size="line"> Điều kiện (Flow logic)

{% hint style="info" %}
**Flow logic/Condition** xác định rõ **điều kiện, tình huống** để thực hiện hành động tự động.
{% endhint %}

<figure><img src="../../.gitbook/assets/image (533).png" alt="" width="350"><figcaption><p>Các loại Flow logic</p></figcaption></figure>

* <img src="../../.gitbook/assets/image (534).png" alt="" data-size="line"> If/Else: Đặt điều kiện Đúng/Sai để đi tiếp, dựa vào bộ lọc UQL.&#x20;
* <img src="../../.gitbook/assets/image (535).png" alt="" data-size="line">Multi-path: Đặt nhiều điều kiện khác nhau, nếu thỏa mãn thì đi tiếp.
* <img src="../../.gitbook/assets/image (536).png" alt="" data-size="line">Branching: Tìm đến các Nghiệp vụ (Object) khác Nghiệp vụ (Object) hoạt để thực hiện hành động.

### <img src="../../.gitbook/assets/image (537).png" alt="" data-size="line"> Action (Hành động)

{% hint style="info" %}
**Action** là định nghĩa các tác vụ tự động hóa, tác động lên các đối tượng nghiệp vụ được sinh ra từ <img src="../../.gitbook/assets/image (538).png" alt="" data-size="line"> **Universal Object** trong hệ thống Luklak & tương tác kết nối với hệ thống ngoài.
{% endhint %}

<figure><img src="../../.gitbook/assets/image (52).png" alt=""><figcaption><p>Các loại Action</p></figcaption></figure>

#### Ví dụ: Phân tích các Quy tắc tự động hóa & các thành phần cấu thành tương ứng

## Nâng cao: Cả hệ thống tự động



:bulb:Đây là một cách tiếp cận đột phá của Luklak, giúp tối ưu hóa năng suất theo cấp số nhân:

### **Một ngôn ngữ chung**

* Bản chất là vì mọi chức năng của Luklak đều được tạo ra từ Universal Object, nói chung một ngôn ngữ nên sinh ra đã là một, kết nối tự động tự nhiên như hơi thở.

### **"Đồng bào" tự động hóa**

{% hint style="warning" %}
**Cách tích hợp truyền thống:** Mỗi chức năng đặc thù có một app riêng. Doanh nghiệp dùng 30-40 apps vận hành rời rạc với database, giao diện, logic khác nhau. _Vì chúng không thể "nói chuyện, hiểu nhau"_ nên phải tích hợp qua app trung gian, dễ lỗi và chỉ truyền tài được 20-30% dữ liệu.&#x20;
{% endhint %}

{% hint style="success" %}
**Luklak sinh ra đã hợp nhất:** Các chức năng, đối tượng nghiệp vụ trong Luklak đã có khả năng _"nói chuyện, hiểu nhau"_ ngay từ khi sinh ra. Như "**Đồng bào**" cùng sinh ra từ một mẹ, chung một tiếng nói, không mất công phiên dịch - KHÔNG CẦN app trung gian kết nối tích hợp.
{% endhint %}

### **Kết nối ra ngoài**

* Tích hợp với các hệ thống bên ngoài thông qua Webhooks, đảm bảo tự động hóa xuyên biên giới công cụ.

### Toàn hệ thống thông suốt

* Bất kì đối tượng nghiệp vụ nào cũng có thể nói chuyện, thiết lập quy tắc tự động hóa, không kể ranh rới phòng ban.
* Ví dụ: CRM chỉ có Kinh doanh mới biết, còn team Sản phẩm thì chẳng bao giờ biết Kinh doanh nói với khách những gì. Với Luklak, mọi thứ được tự động, thông suốt.

{% @guidejar/embed guideId="VhwVgOzOOul3m2JF2uip" type="1" controls="on" url="https://www.guidejar.com/embed/VhwVgOzOOul3m2JF2uip?type=1&controls=on" %}

## <img src="../../.gitbook/assets/image (540).png" alt="" data-size="line"> Lắp ghép miếng lego - Automation

### Với  Universal Object

* **Thông qua Trigger:** Mọi thay đổi trên của  <img src="../../.gitbook/assets/image (538).png" alt="" data-size="line"> **Universal Object** đều được coi là một hành động, có thể làm đầu vào Trigger cho  <img src="../../.gitbook/assets/image (512).png" alt="" data-size="line">**Universal Automation**
* **Thông qua Action:**   <img src="../../.gitbook/assets/image (512).png" alt="" data-size="line">**Universal Automation** có thể thiết lập các Action tương tác vào bất cứ nghiệp vụ nào trên hệ thống, vì chúng đều được tạo ra từ  <img src="../../.gitbook/assets/image (538).png" alt="" data-size="line"> **Universal Object**\
  \
  **Ví dụ**: Automation tương tác kết nối các Object trong 1 doanh nghiệp Thiết kế túi giấy theo yêu cầu

<table><thead><tr><th>Loại Trigger</th><th>Đối tượng nguồn</th><th>Đối tượng đích</th><th data-hidden><select></select></th></tr></thead><tbody><tr><td><img src="../../.gitbook/assets/image (541).png" alt="" data-size="line"> Chuyển trạng thái<br></td><td> <img src="../../.gitbook/assets/image (521).png" alt="" data-size="line"> <strong>Customer</strong><br><br>Nhân viên Kinh doanh chuyển trạng thái sang LÊN THIẾT KẾ</td><td><img src="../../.gitbook/assets/image (542).png" alt="" data-size="line"> <strong>Yêu cầu thiết kế</strong><br><br>Tự động tạo nghiệp vụ này, giao cho Nhân viên thiết kế</td><td></td></tr><tr><td><img src="../../.gitbook/assets/image (541).png" alt="" data-size="line"> Chuyển trạng thái<br><img src="../../.gitbook/assets/image (544).png" alt="" data-size="line"> Cập nhật trường</td><td> <img src="../../.gitbook/assets/image (520).png" alt="" data-size="line"> <strong>Hợp đồng</strong><br><br>Kế toán chuyển sang ĐÃ THANH TOÁN &#x26; điền <code>Contract Value</code></td><td> <img src="../../.gitbook/assets/image (521).png" alt="" data-size="line"> <strong>Customer</strong><br><br>Tự động tính <code>Total Value</code>  = tổng số tiền khách đã mua</td><td></td></tr><tr><td><img src="../../.gitbook/assets/image (543).png" alt="" data-size="line"> Webhook</td><td>Khách đăng kí qua form được kết nối với Luklak</td><td> <img src="../../.gitbook/assets/image (514).png" alt="" data-size="line"> <strong>Lead</strong><br><br>Tự động tạo nghiệp vụ này trong CRM, với đầy đủ thông tin của khách</td><td></td></tr></tbody></table>

### Với Object Link

<figure><img src="../../.gitbook/assets/image (545).png" alt=""><figcaption><p>Kết nối mọi ngõ ngách công việc</p></figcaption></figure>

Thông qua <img src="../../.gitbook/assets/image (546).png" alt="" data-size="line">**Object Link** đã được người dùng định nghĩa, <img src="../../.gitbook/assets/image (512).png" alt="" data-size="line">**Universal Automation** có thể sử dụng Branching để tìm đến các nghiệp vụ liên quan trên toàn hệ thống, thực hiện thao tác tự động trên đó

**Ví dụ**:&#x20;

| Quy tắc Tự động                                                                                                                                                                                          | Cấu hình                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | Object link cần có                                                                                                                                                                                                                                        |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Tính tổng số  <img src="../../.gitbook/assets/image (521).png" alt="" data-size="line"> **Customer** mà   <img src="../../.gitbook/assets/image (517).png" alt="" data-size="line"> **Ad** này chốt được | Khi   <img src="../../.gitbook/assets/image (521).png" alt="" data-size="line"> **Customer** được chuyển sang trạng thái  <img src="../../.gitbook/assets/image (518).png" alt="" data-size="line">, cộng 1 vào trường `Số khách chốt được` ở   <img src="../../.gitbook/assets/image (517).png" alt="" data-size="line"> **Ad** tương ứng                                                                                                                                                                                                                                                      |  <img src="../../.gitbook/assets/image (521).png" alt="" data-size="line"> **Customer** <img src="../../.gitbook/assets/image (546).png" alt="" data-size="line"> <img src="../../.gitbook/assets/image (517).png" alt="" data-size="line"> **Ad**        |
| Tính tổng công nợ còn lại trên  <img src="../../.gitbook/assets/image (520).png" alt="" data-size="line"> **Hợp đồng**                                                                                   | Khi  <img src="../../.gitbook/assets/image (547).png" alt="" data-size="line"> **Phiếu thu** của  <img src="../../.gitbook/assets/image (520).png" alt="" data-size="line"> **Hợp đồng** chuyển sang trạng thái ĐÃ THANH TOÁN, thực hiện cập nhật giá trị trường `Công nợ`\|  <img src="../../.gitbook/assets/image (520).png" alt="" data-size="line"> **Hợp đồng** = `Giá trị Hợp đồng`\| <img src="../../.gitbook/assets/image (520).png" alt="" data-size="line"> **Hợp đồng** - `Số tiền đã thu`\| <img src="../../.gitbook/assets/image (547).png" alt="" data-size="line"> **Phiếu thu** |  <img src="../../.gitbook/assets/image (547).png" alt="" data-size="line"> **Phiếu thu** <img src="../../.gitbook/assets/image (546).png" alt="" data-size="line"> <img src="../../.gitbook/assets/image (520).png" alt="" data-size="line"> **Hợp đồng** |



:bulb:Creativity is connecting the dots. System is elements & connection.

### Với Universal Workflow

Khi người dùng chuyển trạng thái trên <img src="../../.gitbook/assets/image (548).png" alt="" data-size="line"> **Universal** **Workflow**, có thể cấu hình các quy tắc tự động, đảm bảo luồng công việc phối hợp thông suốt

**Ví dụ:**

| Quy tắc tự động                                                                                                                                                                                   | Cấu hình ở Workflow                                                                                                                                                                                                                                                                                                                 |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Tự động chat & tag tên nhân viên kinh doanh vào chat của nghiệp vụ <img src="../../.gitbook/assets/image (542).png" alt="" data-size="line"> **Yêu cầu thiết kế** khi nhân viên thiết kế làm xong | Ở trạng thái <img src="../../.gitbook/assets/image (549).png" alt="" data-size="line">, cấu hình từ động <img src="../../.gitbook/assets/image (550).png" alt="" data-size="line"> Chat lên mục kích hoạt ( <img src="../../.gitbook/assets/image (542).png" alt="" data-size="line"> **Yêu cầu thiết kế**) với nội dung mong muốn. |



[^1]: Được tạo ra từ  <img src="../../.gitbook/assets/image (538).png" alt="" data-size="line"> **Universal Object**&#x20;
