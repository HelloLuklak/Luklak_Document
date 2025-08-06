# Universal Object

<figure><img src="../.gitbook/assets/image (490).png" alt=""><figcaption></figcaption></figure>

## feature software

<figure><img src="../.gitbook/assets/image (406).png" alt=""><figcaption></figcaption></figure>

các phần mềm phổ biến hiện cho đến hiện nay là thế hệ 2 - feature software - mỗi chức năng thường tách thành các app rời rạc khác nhau:

* báo cáo statista cho thấy một doanh nghiệp phải dùng tới 130 saas app khác nhau dạng này. và thậm chí 1 công ty làm phần mềm như zoho, base, misa cũng làm tầm 40 con app khác nhau.
* các app hoặc module cũng được tách rời khỏi nhau, với giao diện, logic và cách hoạt động khác nhau hoàn toàn. người dùng trong một phiên làm việc phải liên tục chuyển qua lại giữa các màn hình khác nhau làm đứt gãy luồng công việc, giảm hiệu suất làm việc.

<figure><img src="../.gitbook/assets/image (407).png" alt=""><figcaption></figcaption></figure>

* mỗi app đó được phát triển riêng, với các database được thiết kế riêng với các table/ column khác nhau ở bên dưới, dẫn tới các chức năng và dữ liều không thông suốt tổng hợp được với nhau, không làm việc được với nhau một cách tự nhiên. muốn kết nối dữ liệu thì phải đầu tư thêm quá trình làm ETL (Extract - Transform - Load) rất tốn kém và phức tạp về mặt kĩ thuật, như hình bên dưới.

## luklak unified & universal

<figure><img src="../.gitbook/assets/image (408).png" alt=""><figcaption></figcaption></figure>

* luklak là thế hệ ứng dụng doanh nghiệp thế hệ tiếp theo - thế hệ 3 - với cách tiếp cận hoàn toàn mới với tính chất _**unified & universal (hợp nhất & phổ quát)**_ với khả năng nocode & lowcode cho phép kéo thả tự tạo ra được nhiều chức năng công việc khác nhau mà không cần code.
* cốt lõi của luklak được xây dựng trên một đơn vị lõi phổ quát gọi là _**universal object**_. mọi tính năng, dữ liệu, đầu việc khác nhau đều được tạo ra bởi _**universal object**_ này, nên có khả năng thông suốt dữ liệu và làm việc tương tác ngay với nhau một cách tự nhiên, thông suốt.

## universal object

<figure><img src="../.gitbook/assets/image (409).png" alt=""><figcaption></figcaption></figure>

cốt lõi mọi tính năng ở luklak đều được tạo nên từ đơn vị lõi _**universal object**_ bên dưới, còn bên trên với người dùng nó sẽ hiện hình thành các _**issue type (loại mục)**_ khác nhau do người dùng tự tạo ra tương ứng với các mỗi năng - luồng công việc nhất định.

mỗi khi người dùng tạo một tính năng nào đó, nghĩa là tạo và đặt tên cho một issue type mới từ universal object, ví dụ:

* **customer** trong CRM
* **employee** trong HRM
* **task** trong task management
* **request/ ticket** trong IT Helpdesk, Customer Service
* **machine/ equipment** trong Asset Tracking
* … và bất kì chức năng gì doanh nghiệp tự nghĩ ra, tự kéo thả tự làm để đáp ứng nhu cầu đa dạng và đặc thù của riêng mình

<figure><img src="../.gitbook/assets/image (477).png" alt=""><figcaption></figcaption></figure>

trong mỗi issue type sẽ có 2 nửa hợp thành:

* workflow
* data field

<figure><img src="../.gitbook/assets/image (448).png" alt=""><figcaption></figcaption></figure>

bên ngoài sẽ có các đối tượng phổ quát khả dụng với mọi issue type được tạo ra từ universal object:

* universal automation
* universal query language
* object connection
* live chat



## universal workflow

* mỗi đối tượng - chức năng (issue type) tạo ra sẽ luôn cần định nghĩa một luồng công việc cho nó, đó là workflow.
* phần mềm thế hệ 2 (feature software) sẽ tách chức năng workflow thành một app riêng biệt, chỉ vào app đó mới có thể làm workflow, còn rất nhiều công việc ở vài chục app khác thì không có.
* universal workflow của luklak có tính phổ quát toàn hệ thống, bất kì ở đâu, ở chức năng công việc nào cũng có thể định nghĩa được workflow.

<figure><img src="../.gitbook/assets/image (410).png" alt=""><figcaption></figcaption></figure>

## data field

* mỗi issue type tạo ra từ universal object sẽ cho phép định nghĩa bộ data field riêng, cung cấp các trường thông tin dữ liệu cho tính năng công việc được tạo ra.
* mọi trường dữ liệu được tạo ra đều có thể được lọc và tổng hợp bởi universal query language (nói cụ thể hơn ở bên dưới) để lọc tìm thông tin, tổng hợp dữ liệu dashboard…

<figure><img src="../.gitbook/assets/image (411).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (413).png" alt=""><figcaption></figcaption></figure>

## universal query language

sự khác biệt lớn:

* phần mềm thế hệ 2 (feature software) mỗi chức năng công việc lại được tách thành app/ module riêng với sql databse với các table/ column được định nghĩa riêng. dẫn tới để tổng hợp dữ liệu từ các chức năng khác nhau sẽ cần kiến thức kĩ thuật chuyên sâu về sql, cũng như quyền truy cập database bên dưới. đây đều là thứ mà khách hàng - người dùng không có, dẫn tới hàng ngày họ không tự chủ trong việc tổng hợp dữ liệu từ các phần mềm khác nhau được.
* mọi chức năng, dữ liệu của luklak được tạo từ một đơn vị universal object đã được trừu tượng hóa xử lý mọi vấn đề phức tạp về kĩ thuật database sql bên dưới hệ thống, để bên trên người dùng có thể dễ dàng kéo thả sử dụng mà không cần động đến sql mà vẫn truy vấn, tổng hợp được mọi dữ liệu công việc của mình.
* không còn cần đến hệ thống xử lý dữ liệu phức tạp với Data Warehouse/ ETL phức tạp và tốn kém nữa.

<figure><img src="../.gitbook/assets/image (412).png" alt=""><figcaption></figcaption></figure>

_**UQL (universal query language)**_ cho phép truy vấn và tổng hợp mọi dữ liệu công việc nằm ở các chức năng đa dạng khác nhau,

tính phổ quát của universal object và universal query language (UQL) mang lại tiện ích tiện lợi hàng ngày cho người dùng

* **thanh lọc nhanh (quick search)**: ở trên cùng, quen thuộc cùng một giao diện và lọc được mọi dữ liệu chức năng khác nhau
* **bộ lọc lưu sẵn (save fitler)**: tạo sẵn các tiêu chí lọc dữ liệu cho một nhu cầu công việc nào đó, lưu lại để dùng về sau và chia sẻ với người liên quan.
* **dashboard tổng hợp**: dễ dàng kéo thả tự tạo các báo cáo tổng hợp được dữ liệu từ nhiều nơi, nhiều chức năng khác nhau về một nơi để phân tích.

## universal automation

* automation cho phép người dùng tự tạo ra các hành động tự động hóa, để thay thế cho các thao tác người dùng làm thủ công, cũng như xử lý các dữ liệu, tính năng mà mình mong muốn.
* phần mềm thế hệ 2 (feature software) sẽ tách chức năng automation thành một app riêng biệt, chỉ vào app đó mới có thể làm automation, còn rất nhiều công việc ở vài chục app khác thì không có.
* universal automation của luklak có tính phổ quát toàn hệ thống, bất kì ở đâu, ở chức năng công việc nào cũng có thể định nghĩa được workflow, cho phép kết nối tương tác xử lý tự động mọi dữ liệu ở mọi chức năng công việc khác nhau.

<figure><img src="../.gitbook/assets/image (414).png" alt=""><figcaption></figcaption></figure>

## unified ui/ ux

tất cả các chức năng, quy trình được tạo ra từ nocode & lowcode này của luklak đều hiện với người dùng trên một màn hình, một hệ thống làm việc thông suốt, không đứt gãy, không phải chuyển qua lại giữa các app, các giao diện màn hình khác nhau.

có sẵn cả web app, desktop app, mobile hoạt động được luôn với mọi chức năng mà người dùng tự tạo ra.

<figure><img src="../.gitbook/assets/image (415).png" alt=""><figcaption></figcaption></figure>

## nocode & lowcode

các yếu tố trên là các miếng _**lego nocode**_ của luklak, từ đó cho phép người dùng, doanh nghiệp tự tay kéo thả lắp ghép tạo ra các chức năng đa dạng & đặc thù theo nhu cầu của mình mà không cần biết code, không phải phụ thuộc vào các công ty làm phần mềm nữa.

<figure><img src="../.gitbook/assets/image (416).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (417).png" alt=""><figcaption></figcaption></figure>
