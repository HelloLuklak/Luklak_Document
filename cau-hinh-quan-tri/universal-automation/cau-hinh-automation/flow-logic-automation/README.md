# Flow logic (Automation)

## giới thiệu chung condition

* sau khi bắt event trigger (create issue, change status, update field, schedule, n8n, webhook, api) (xem thêm tại [TRIGGER FOR AUTOMATION](https://www.notion.so/TRIGGER-FOR-AUTOMATION-393378a7500a4657b1b8333385111ad9?pvs=21)) thì thường hệ thống sẽ trả về nhiều mục dữ liệu (issue) khác nhau.
* sẽ phải áp dụng các điều kiện lọc sử dụng NQL filter và các điều kiện khác để lọc ra các mục dữ liệu (issue) theo các tiêu chí nhất định, đúng nhu cầu từ đó đưa vào action chạy các hành động tự động.

<figure><img src="../../../../.gitbook/assets/image (505).png" alt=""><figcaption></figcaption></figure>

dùng các điều kiện sau để lọc dữ liệu trước khi chạy tự động:

* **data field** (dùng luklak nql - natural query language): dùng để đặt các điều kiện lọc cho các trường thông tin dữ liệu (system field & custom field) trên các mục dữ liệu (issue)
* **checklist/ subtask**: kiểm tra xem bao nhiêu đầu việc con/ mục kiểm bên trong đã được hoàn thành
* **linked issued**: kiểm tra điều kiện của các mục dữ liệu có liên quan được kết nối tới mục hiện tại

## data field condition with nql

* đây là cách lọc dữ liệu phổ biến và sâu rộng nhất, lọc các trường thông tin dữ liệu (system field & custom field) trên các mục dữ liệu (issue).
* luklak với **universal object** (xem thêm tại [UNIVERSAL OBJECT FOR NOCODE & LOWCODE](https://www.notion.so/UNIVERSAL-OBJECT-FOR-NOCODE-LOWCODE-8c85ef31ea484b688b6e58147dfe8a8e?pvs=21)) trở nên mạnh mẽ vượt trội so với các phần mềm thế hệ 2 mỗi chức năng lại tách rời rạc thành các app khác nhau. khi mọi chức năng, mọi dữ liệu được tạo ra trên luklak đều là từ một thực thể phổ quát là **universal object** thì các dữ liệu đó dễ dàng được tổng hợp, kết nối, tương tác với nhau mà không phải trải qua quá trình **ETL (Extract - Transform - Load)** phức tạp tốn kém.
* **NQL (Natural Query Language**: luklak phát triển một ngôn ngữ truy vấn và tổng hợp dữ liệu là NQL (Natural Query Language) tương tự như truy vấn kĩ thuật vào SQL Database. nhưng NQL được thiết kế giao diện thân thiện, tự nhiên với người dùng mà không cần biết kĩ thuật.
* **NQL** này được dùng để lọc dữ liệu cho tính năng automation ở đây, cũng như được dùng để tạo ra các filter, dashboard tùy biến mạnh mẽ & dễ dàng cho người dùng, tự tạo.
* bất kì trường thông tin dữ liệu nào có được cài đặt, dù là các system field do hệ thống tạo sẵn hay các custom field do người dùng tạo ra đều có thể truy vấn và đặt các điều kiện lọc với NQL
* **NQL** rất mạnh mẽ sâu rộng gần tương đương với SQL nhưng lại được thiết kế tự nhiên, dễ dùng với giao diện trực quan, chứ không phức tạp cần nhiều kĩ thuật như truy vấn SQL vào database.

<figure><img src="../../../../.gitbook/assets/image (506).png" alt=""><figcaption></figcaption></figure>

_hiện tại không một hệ thống nào ở việt nam có khả năng mạnh mẽ sâu rộng như vậy, có nocode & lowcode cho phép tự tạo các chức năng - dữ liệu đa dạng khác nhau theo nhu cầu của doanh nghiệp, và có ngôn ngữ truy vấn phổ quát và tự nhiên như NQL của luklak để ngay lập tức tổng hợp được dữ liệu cho mọi chức năng khác nhau trên hệ thống như vầy._

## checklist & subtask condition

data field condition with nql ở trên thì kiểm tra các trường thông tin dữ liệu của mục cụ thể hiện tại, còn:

* **checklist** thì kiểm tra số mục kiểm bên trong mục dữ liệu hiện tại, đặt điều kiện xem bao nhiêu mục kiểm đã hoàn thành thì mới cho chạy hành động hoặc chuyển trạng thái

<figure><img src="../../../../.gitbook/assets/image (507).png" alt=""><figcaption></figcaption></figure>

* **subtask** là khái niệm lớn hơn, là các mục việc con (sub-issue) bên dưới mục hiện tại, có thể sử dụng câu lệnh lọc NQL sâu rộng bên trên, lọc theo các trường dữ liệu đa dạng của mục con (sub-issue) rồi sau đó mới thiết lập điều kiện là bao nhiêu mục con trong đó thỏa mãn điều kiện/ số lượng đề ra thì mới cho chạy hành động.

<figure><img src="../../../../.gitbook/assets/image (508).png" alt=""><figcaption></figcaption></figure>

## linked issue condition

issue linked (kết nối mục) là tính năng rất mạnh của luklak:

* cho phép tạo ra các liên kết (link) giữa các mục việc khác nhau & có liên quan đến nhau để tạo ra bức tranh tổng thể rộng lớn hơn.
* các mục cụ thể như là các điểm (**dots**), và link sẽ như là **connection**. sự sáng tạo chính là **connection the dots**. khi có cả dots và connection như vậy sẽ tạo nên khả năng linh hoạt sáng tạo sâu rộng để tạo ra các chức năng đa dạng mạnh mẽ cho người dùng, doanh nghiệp
* các kết nối mục (link) này cũng là cơ sở/ đường dẫn để kiểm tra các điều kiện dữ liệu mở rộng ra ngoài mà có liên quan tới **mục (issue)** hiện tại.

cụ thể cài đặt điều kiện với linked issues cho automation như sau:

* **loại kết nối (link type)**: cho phép chọn lọc các loại kết nối phù hợp với nhu cầu lọc

<figure><img src="../../../../.gitbook/assets/image (509).png" alt=""><figcaption></figcaption></figure>

* **field condition with NQL**: sau khi chọn link type ở trên thì hệ thống sẽ trả về danh sách nhiều mục (issue) ăn theo link type đó, và có thể tiếp tục áp dụng NQL để tinh lọc chọn ra các mục (issue) đáp ứng yêu cầu cụ thể, tương tự cách lọc của sub-task

<figure><img src="../../../../.gitbook/assets/image (510).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../../.gitbook/assets/image (511).png" alt=""><figcaption></figcaption></figure>
