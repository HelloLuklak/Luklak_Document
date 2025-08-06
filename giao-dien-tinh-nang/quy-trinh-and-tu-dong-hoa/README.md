---
icon: arrow-progress
---

# Quy trình & tự động hóa

{% embed url="https://youtu.be/YNW1G16Wc9o" %}

## Universal workflow & automation

* luklak unified & universal là ứng dụng thế hệ 3 có tính hợp nhất và phổ quát.
* Xét riêng về tính năng workflow & automation thì luklak cũng đầy đủ như thế hệ 2, với khả năng định nghĩa status, transition, condition, automation rất mạnh
* Thứ làm cho luklak workflow vượt trội đó là tính universal của workflow, nghĩa là bất kì chức năng công việc nào trên hệ thống thì đều có workflow & automation engine mặc định có sẵn trong đó. có thể cài đặt workflow & automation ở bất kì chức năng công việc nào như it helpdesk, task management, crm, hrm, request & approval…

Quy trình là trái tim của hệ thống vận hành doanh nghiệp, và nó phải thực sâu rộng ăn sâu vào mọi ngõ ngách, mọi nơi công việc của doanh nghiệp. nghĩa là cần universal workflow có tính phổ quát.

## luklak universal workflow

### Universal workflow

<figure><img src="../../.gitbook/assets/image (235).png" alt=""><figcaption></figcaption></figure>

* Workflow của luklak mang tính universal là một phần cơ hữu vận hành trên toàn hệ thống, với mọi công việc của doanh nghiệp. không kiểu như các phần mềm feature software thế hệ 2 là app workflow rời riêng, chỉ vào đó mới làm được workflow, còn đa số các công việc khác làm ở app khác thì không
* Workflow & automation của luklak có khả năng ứng dụng trực tiếp về quy trình và chuẩn hóa vận hành như BPM, SOP, CMMS
* Cốt lõi nhất, universal workflow
* Nó cũng là một trong số các **miếng lego nocode lõi** để từ đó doanh nghiệp có thể tự tay kéo đó tạo ra được ra dạng các chức năng công việc khác nhau.

### Universal object

<figure><img src="../../.gitbook/assets/image (236).png" alt=""><figcaption></figcaption></figure>

Universal object của luklak chính là đối tượng phổ quát để làm tính năng với nocode & lowcode.

Bên trong mỗi universal object có 2 nửa do người dùng có thể tự định nghĩa:

* Workflow
* Data field

Bên ngoài là các đối tượng có thể làm việc trực tiếp với universal object bao gồm:

* Universal query language: truy vấn và tổng hợp dữ liệu đối với mọi chức năng được tạo ra từ universal object
* Universal automation: tự động hóa các hành động, xử lý logic và kết nối mọi dữ liệu được tạo ra từ universal object
* Object connection: tương tự như khái niệm “connecting the dots” để tạo ra thứ mới, thì luklak cho phép người dùng tự định nghĩa các kết nối giữa universal object để tạo ra bức tranh lớn hơn, chức năng lớn hơn.
* Live chat: mọi công việc, dữ liệu, chức năng tạo ra bởi universal object đều có khả năng live chat trao đổi trực tiếp trên đó, chứ không phải lôi sang chỗ khác để chat.

Universal workflow là 1 trong những miếng lego nocode lõi của giúp người dùng tự tay kéo thả tạo ra các chức năng đa dạng đặc thù theo nhu cầu

<figure><img src="../../.gitbook/assets/image (237).png" alt=""><figcaption></figcaption></figure>

## luklak & universal automation

### Universal automation

#### Automation thế hệ 3

**luklak unified & universal** là ứng dụng thế hệ 3, nên workflow của luklak là **universal workflow** với các tính chất:

* Phổ quát và có sẵn trên toàn hệ thống, ở bất kì chức năng, ứng dụng nào được tạo ra
* Có khả năng tương tác và kết nối thông suốt với tất cả các ứng dụng, dữ liệu, đầu việc ở bất kì đâu
* Các chức năng khác nhau của luklak đều được tạo nên từ universal object duy nhất, nên cấu trúc dữ liệu cách làm là phổ quát giống nhau, có thể kết nối tương tác luôn được với nhau, chỉ cần tìm hiểu một lần là dùng dễ dàng cho mọi nơi.

<figure><img src="../../.gitbook/assets/image (225).png" alt=""><figcaption></figcaption></figure>

## Nguyên lý hoạt động của Automation

Automation cho phép

* Tự động hóa sâu rộng và linh hoạt các công việc, luồng, dữ liệu, logic cần xử lý
* Kết nối tương tác với các hệ thống bên ngoài
* Tăng hiệu suất và chất lượng công việc làm sự phụ thuộc vào cảm xúc và sai sót cá nhân

Một automation rule (quy tắc tự động hóa) sẽ gồm 3 thành phần cài đặt chính:

* **Trigger (event & condition)**: định nghĩa điểm khởi để kích hoạt khởi chạy một quy tắc tự động hóa nào đó. ví dụ có thể dựa trên hành động một đầu việc dữ liệu mới được tạo ra, một công việc được chuyển trạng thái hoặc chuyển người làm… có thêm bộ lọc dựa trên NQL để tinh lọc chỉ bắt các sự kiện đáp ứng được các điều kiện, tiêu chí nhất định.
* **Advanced logic**: cung cấp các logic xử lý đa dạng và linh hoạt theo các nhu cầu khác nhau, ví dụ như if/ else, multi paths, branching
* **Automated action**: là các hành động được tự động hóa, bao gồm cả các hành động trong nội bộ hệ thống luklak (như cập nhật trường, chuyển trạng thái, gửi tin nhắn chat…) cho đến các hành động kết nối với bên ngoài (gửi webhook, gửi email, zalo…)

ACTION

Các hành động tự động thực hiện trong luklak:

* Create issue/ sub issue/ checklist
* Change status
* Update field
* Link issue
* Send chat message to space chat, issue chat, private chat

Các hành động kết nối với bên ngoài:

* Gửi email

Các hành động kết nối với bên ngoài đang được làm:

* Gửi tin nhắn zalo oa (đang làm)
* Gửi sms tới số điện thoại
* Tích hợp với n8n để thực hiện hành động ở các app khác
* Gửi webhook/ api

IF/ ELSE & MULTI-PATHS

* lulak automation cung cấp logic rẽ nhánh sâu rộng, linh hoạt
* If/esle: rẽ 2 nhánh hành động dựa trên kết quả đúng sai của 1 điều kiện lọc. cài đặt nhanh chóng.
* Multi-paths: rẽ theo nhiều nhánh khác nhau, dựa trên nhiều điều kiện khác nhau.

BRANCHING

Là tính năng khá đặc thù và sâu của luklak, ít ứng dụng nào có automation cho việc này.

Automation rule thường sẽ chạy các hành động trên mục kích hoạt (trigger issue) đáp ứng trigger & condition. và branching cho phép rẽ nhánh thực hiện các hành động tự động có liên quan đến mục kích hoạt (trigger issue), bao gồm:

* Các mục được lọc tùy ý theo nql
* Parent/ child issue
* Tất các issue được tạo ra trong quá trình chạy một automation rule
* Issue mới nhất được tạo ra trong quá trình chạy
* Các issue được kết nối

FUNCTIONAL ACCOUNT

Đây là tính năng rất mạnh và đặc biệt của luklak, rất hiếm ứng dụng làm automation cho đầu tư sâu đến mức này. functional account là tài khoản chức năng (khác với tài khoản người dùng - user) chuyên dùng để chạy các automation rule, để đảm bảo đúng phân quyền:

* Đủ quyền để truy cập đủ các dữ liệu và thực hiện các hành động cần thiết
* Không cho vượt quyền xử lý dữ liệu ngoài phạm vi cho phép, dẫn tới các lỗ hổng về bảo mật dữ liệu.

Các app khác mà automation không có automation account thì sẽ phải dùng 2 loại tài khoản cực hữu để chạy các automation rule:

* Dùng tài khoản cá nhân của nhân sự (user): thì khó truy cập hết dữ liệu, và rule của người này tạo ra sẽ khó ứng dụng được cho người khác
* Dùng tài khoản hệ thống (system account) thì tài khoản này thường có quyền truy cập dữ liệu toàn hệ thống. nếu cá nhân (user) bất kì được dùng tài khoản này thì có thể làm lộ hoặc xóa các dữ liệu mà bình thường họ không có quyền truy cập.

Functional account của luklak sẽ hoạt động như sau:

* Admin sẽ tạo các functional account dành riêng cho các bộ phận, mảng việc. và sẽ cấp quyền cho phép những user nhất định được chọn và dùng tài account này cho automation.
* Admin cấp quyền truy cập dữ liệu cho các functional account này thông qua permission scheme như bình thường, để đảm bảo các tài khoản sử dụng sẽ không bao giờ vượt quá quyền truy cập được phép.

<figure><img src="../../.gitbook/assets/image (226).png" alt=""><figcaption></figcaption></figure>



