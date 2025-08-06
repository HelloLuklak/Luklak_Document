# n8n

#### n8n / trigger

**kết nối luklak với ứng dụng bên ngoài:**

* luklak automation không chỉ cho phép nhận trigger trực tiếp từ các sự kiện xảy ra trong luklak, mà còn cả ngoài luklak để **kết nối làm việc giữa luklak và các phần mềm bên ngoài** đó.
* thế giới phần mềm bên ngoài ra vô cùng đa dạng và phong phú, với cực kì nhiều phần mềm khác nhau. do đó, nếu bất kì một doanh nghiệp nào tiếp cận theo hướng tự tìm hiểu và tự làm tích hợp với tất cả các phần mềm đó, thì đó là con đường dài đằng đẵng trải đầy mìn, tốn rất nhiều thời gian, công sức, và nhiều lỗi phát sinh.
*   nên thế giới đã sinh ra các app chuyên dùng để kết nối sẵn với rất nhiều các app phổ biến ngoài kia, người dùng chỉ việc cài đặt kết nối đơn giả chút là chạy được. phổ biến nhất trước giờ là zapier, với chi phí khá cao. gần đây nổi lên một lựa chọn rất tốt đó là , nếu mua bản cloud thì chi phí cũng khá thấp ($20/ tháng) mua tại [\*\*n8n.io](http://n8n.io)\*\* gốc của nước ngoài, và thậm chí nó còn có bản open source miễn phí, tải về cài trên server/ vps của mình dùng thoải mái; hoặc có giải pháp trung gian là thuê dịch vụ của bên [**n8n.vn**](http://n8n.vn) của việt nam dùng bản n8n của nước ngoài và cung cấp các dịch vụ giá rẻ:

    * bán tài khoản n8n với giá rẻ (trên server họ tự cài)
    * dịch vụ cài đặt bản open source n8n lên server/ vps riêng cho doanh nghiệp
    * đào tạo hướng dẫn sử dụng n8n
    * cài đặt chìa khóa trao tay các automation rule trên n8n cho doanh nghiệp chỉ việc dùng, không phải làm gì, chỉ việc trả tiền. rất tiện lợi.



<figure><img src="../../.gitbook/assets/image (201).png" alt=""><figcaption></figcaption></figure>

**ứng dụng phổ biến**

* gần như tất cả các ứng dụng phổ biến bên ngoài đều đã được n8n đóng gói sẵn đấu nối tích hợp, và luklak cũng kết nối làm việc tốt với n8n. đồng nghĩa với việc luklak có thể kết nối với rất nhiều ứng dụng phổ biến bên ngoài, thông qua n8n.
* thông qua n8n thì có thể bắn trigger từ các ứng dụng phổ biến như google, microsoft, sql server, github…. dưới dạng webhook/ http request về luklak để khởi chạy một automation rule trên luklak.
* **lưu ý về workflow**: nhiều khi cùng một từ nhưng được dùng với các tính chất khác nhau, kiểu từ đồng âm khác nghĩa ấy. zapier, n8n, lark anycross.. cũng được dùng với từ **tự động hóa quy trình (worflow automation)** nhưng hàm ý ở đây là nó kết nối dữ liệu của các phần mềm khác nhau để thực hiện các tác vụ khác nhau. chứ nó không phải là workflow theo dạng **business process automation** là kiểu định nghĩa các quy trình làm việc của doanh nghiệp, trực quan hóa nó thành workflow với các status và transition, đi kèm với nó là các thao tác tự động hóa.

\*\*xem thêm về các integration với các app của n8n tại [https://n8n.io/integrations/\*\*](https://n8n.io/integrations/**)

{% embed url="https://tungoi.notion.site/ACTION-FOR-AUTOMATION-144a45982af9475ca0712f0920906ffb" %}
&#x20;(có ảnh)
{% endembed %}

