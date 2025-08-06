# Trigger (Automation)

<figure><img src="../../../.gitbook/assets/image (194).png" alt="" width="375"><figcaption></figcaption></figure>

## Trigger event

Đây là điểm khởi đầu để kích hoạt chạy một quy tắc tự động hóa nào đó (automation rule). luklak hiện cung cấp các loại trigger event như dưới đây, và có thể được phát triển bổ sung trong tương lai.

Dưới đây chỉ mô tả các loại trigger event khác nhau, và tất cả các event này sau đó đều có thể đưa vào lọc (condition) sử dụng NQL dùng chung. nên phần lọc với NQL này sẽ được tách rời thành phần riêng ở bên dưới.

## Create issue / trigger

* Bắt sự kiện khi có một mục nào đó được tạo ra
* **mục (issue)** ở đây chính là một chức năng, một quy trình, một công việc hoặc một đầu mục dữ liệu nào đó được tạo ra từ [\*\*universal object](https://www.notion.so/UNIVERSAL-OBJECT-FOR-NOCODE-LOWCODE-8c85ef31ea484b688b6e58147dfe8a8e?pvs=21).\*\* như đã nói thì một task trong task management, một customer trong crm, một employee trong hrm… đều là một mục.
* _Có thể sử dụng NQL để tinh lọc những ra những mục đáp ứng những tiêu chí cụ thể, nhất định. phần này giống nhau dùng chung cho mọi event, nên sẽ được mô tả ở phần **condition** bên dưới._

<figure><img src="../../../.gitbook/assets/image (195).png" alt=""><figcaption></figcaption></figure>

## Change status / trigger

Bắt sự kiện khi một mục nào đó chuyển trạng thái trong workflow của một mục (issue)

* Có thể định nghĩa cụ thể cả tráng thái nguồn và trạng thái đích chuyển đến
* Có thể chọn cả các **trạng thái cụ thể (status)** đa dạng do người dùng tự tạo ra và đặt tên bất kì, hoặc chọn 1 trong 6 **loại trạng thái (status category)** cố định của hệ thống (Mở, Kế Hoạch, Hoạt Động, Hoàn Thành, Tạm Dừng, Đóng Hủy). Loại trạng thái là dữ liệu tiêu chuẩn cố định, và mỗi trạng thái cụ thể đa dạng do người dùng tạo ra đều sẽ phải chọn là thuộc về 1 trong 6 Loại Trạng Thái có sẵn kia.

<figure><img src="../../../.gitbook/assets/image (196).png" alt=""><figcaption></figcaption></figure>

## Update field / trigger

Nếu có sự kiện nếu có cập nhật trường thông tin dữ liệu ở mục nào đó thì sẽ kích hoạt các hành động tự động.

* Có thể lựa chọn là nếu có bất kì trường nào được cập nhật, hoặc sâu sát hơn thì chỉ theo dõi cụ thể một số trường nhất định được cập nhật
* Thậm chí có thể cài đặt sâu hơn tới mức là hành động cập nhật giá trị của trường là là kiểu gì: từ không có giá trị thành có giá trị, hay từ có thành không, hay từ đang có giá trị này chuyển sang thành giá trị khác.

### Cập nhật trường chọn mục

**Ví dụ: Khi cập nhật trường là trường Chọn mục -> Tự động thực hiện hành động**&#x20;

{% @guidejar/embed guideId="c3cbec28-ba2c-410e-b3cf-c99bfc8cc475" type="1" controls="on" url="https://www.guidejar.com/embed/c3cbec28-ba2c-410e-b3cf-c99bfc8cc475?type=1&controls=on" %}



## Schedule / trigger

* Đặt lịch trình chạy cố định theo thời gian, và có rất nhiều phương án cài đặt đa dạng theo giờ phút, theo ngày, theo tuần, theo tháng…
* Bắt buộc sẽ phải nhập các điều kiện lọc ra các mục cụ thể đáp ứng tiêu chí nhất định chứ không thể chỉ có lịch trình không, xong automation tác động vào toàn bộ dữ liệu trên hệ thống
* Khi lọc ra quá nhiều mục dữ liệu không cần chạy automation, thì có thể cắt chọn chỉ chạy trên một số mục nhất định, bằng cách sắp xếp kết quả theo tiêu chí (trường thông tin nào đó), và chỉ chạy trên 1 hoặc 1 số mục dữ liệu đầu tiên.

<figure><img src="../../../.gitbook/assets/image (197).png" alt=""><figcaption></figcaption></figure>

## n8n / trigger

<figure><img src="../../../.gitbook/assets/image (471).png" alt=""><figcaption></figcaption></figure>

## **Kết nối luklak với ứng dụng bên ngoài:**

* Phía bên trên là các trigger event từ nội bộ của hệ thống luklak, từ đây trở xuống là các trigger từ các phần mềm bên ngoài, cho phép **kết nối làm việc giữa luklak và các phần mềm bên ngoài** đó.
* Thế giới phần mềm bên ngoài ra vô cùng đa dạng và phong phú, với cực kì nhiều phần mềm khác nhau. do đó, nếu bất kì một doanh nghiệp nào tiếp cận theo hướng tự tìm hiểu và tự làm tích hợp với tất cả các phần mềm đó, thì đó là con đường dài đằng đẵng trải đầy mìn, tốn rất nhiều thời gian, công sức, và nhiều lỗi phát sinh.
* Nên thế giới đã sinh ra các app chuyên dùng để kết nối sẵn với rất nhiều các app phổ biến ngoài kia, người dùng chỉ việc cài đặt kết nối đơn giả chút là chạy được. phổ biến nhất trước giờ là zapier, với chi phí khá cao. gần đây nổi lên một lựa chọn rất tốt đó là , nếu mua bản cloud thì chi phí cũng khá thấp ($20/ tháng) mua tại [\*\*n8n.io](http://n8n.io)\*\* gốc của nước ngoài, và thậm chí nó còn có bản open source miễn phí, tải về cài trên server/ vps của mình dùng thoải mái; hoặc có giải pháp trung gian là thuê dịch vụ của bên [**n8n.vn**](http://n8n.vn) của việt nam dùng bản n8n của nước ngoài và cung cấp các dịch vụ giá rẻ:
  * Bán tài khoản n8n với giá rẻ (trên server họ tự cài)
  * Dịch vụ cài đặt bản open source n8n lên server/ vps riêng cho doanh nghiệp
  * Đào tạo hướng dẫn sử dụng n8n
  * Cài đặt chìa khóa trao tay các automation rule trên n8n cho doanh nghiệp chỉ việc dùng, không phải làm gì, chỉ việc trả tiền. rất tiện lợi.

<figure><img src="../../../.gitbook/assets/image (199).png" alt=""><figcaption></figcaption></figure>

**Ứng dụng phổ biến**

* Gần như tất cả các ứng dụng phổ biến bên ngoài đều đã được n8n đóng gói sẵn đấu nối tích hợp, và luklak cũng kết nối làm việc tốt với n8n. đồng nghĩa với việc luklak có thể kết nối với rất nhiều ứng dụng phổ biến bên ngoài, thông qua n8n.
* Thông qua n8n thì có thể bắn trigger từ các ứng dụng phổ biến như google, microsoft, sql server, github…. dưới dạng webhook/ http request về luklak để khởi chạy một automation rule trên luklak.
* **Lưu ý về workflow**: nhiều khi cùng một từ nhưng được dùng với các tính chất khác nhau, kiểu từ đồng âm khác nghĩa ấy. zapier, n8n, lark anycross.. cũng được dùng với từ **tự động hóa quy trình (worflow automation)** nhưng hàm ý ở đây là nó kết nối dữ liệu của các phần mềm khác nhau để thực hiện các tác vụ khác nhau. chứ nó không phải là workflow theo dạng **business process automation** là kiểu định nghĩa các quy trình làm việc của doanh nghiệp, trực quan hóa nó thành workflow với các status và transition, đi kèm với nó là các thao tác tự động hóa.

\*\*xem thêm về các integration với các app của n8n tại [https://n8n.io/integrations/\*\*](https://n8n.io/integrations/**)

## Webhook & api / trigger

* Webhook là cách thức đơn giản và nhanh tiện nhất trong việc kết nối với các phần mềm bên ngoài mà không cần các cài đặt tài khoản phức tạp.
* Một phần mềm bên ngoài có thể bắn một webhook về luklak nhận, để khởi chạy một automation rule.
* Bản thân automation của luklak cũng có hành động cho phép bắn webhook từ luklak sang phần mềm khác bên ngoài.
* Phần api luklak sẽ mở sau đó

<figure><img src="../../../.gitbook/assets/image (200).png" alt=""><figcaption></figcaption></figure>

#### **CONDITION FOR AUTOMATION**

Giới thiệu chung condition data field condition with nql checklist & subtask condition linked issue condition\


#### 3 loại hình kích hoạt tự động hóa <a href="#id-3-automation-trigger-type" id="id-3-automation-trigger-type"></a>

{% hint style="info" %}
**Đa dạng loại quy tắc tự động hóa**: Quy tắc chạy ngầm, hành động trên mục & tự động hóa trên tiến trình.
{% endhint %}



{% @guidejar/embed guideId="1596e906-d27c-4d14-946b-abf2c9346dd1" type="1" controls="on" url="https://www.guidejar.com/embed/1596e906-d27c-4d14-946b-abf2c9346dd1?type=1&controls=on" %}



##
