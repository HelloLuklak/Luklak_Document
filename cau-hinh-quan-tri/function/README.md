# Function

## phân tách nghiệp vụ & issue type

việc cơ bản đầu tiên, đó là một cần phân tách chức năng định làm ra thành các **nghiệp vụ** bên trong, nhỏ hơn. ví dụ dưới đây, hoạch định chức năng QUẢN LÝ NHÂN SỰ, sẽ tách thành các **nghiệp vụ**:

* **employee**: hồ sơ nhân sự
* **onboarding**: hội nhập nhân sự mới
* **offboarding**: thủ tục nhân sự nghỉ
* **situation**: tình huống nhân sự

mỗi nghiệp vụ cụ thể của doanh nghiệp sẽ tương ứng với một **loại mục (issue type)** ở luklak.

<figure><img src="../../.gitbook/assets/image (418).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (419).png" alt=""><figcaption></figcaption></figure>

**issue type** là do người dùng tự tạo & đặt tên. mọi issue type đều được tạo ra từ **universal object** - là đơn vị cốt lõi & phổ quát quan trọng nhất của luklak. xem chi tiết tại [UNIVERSAL OBJECT FOR NOCODE & LOWCODE](https://www.notion.so/UNIVERSAL-OBJECT-FOR-NOCODE-LOWCODE-8c85ef31ea484b688b6e58147dfe8a8e?pvs=21)

mọi nghiệp vụ được người dùng tạo ra trên luklak đều là **issue type**:

* **customer** trong CRM
* **employee** trong HRM
* **task** trong task management
* **request/ ticket** trong IT Helpdesk, Customer Service
* **machine/ equipment** trong CMMS (Computerized Maintenance Management System)
* …

<figure><img src="../../.gitbook/assets/image (420).png" alt=""><figcaption></figcaption></figure>

## trường thông tin dữ liệu

mỗi công việc sẽ cần các trường thông tin dữ liệu. luklak cho phép người kéo thả tự tạo nhiều loại trường thông tin khác nhau…

ví dụ dưới đây là các trường thông tin một hồ sơ ứng viên trong chức năng QUẢN LÝ TUYỂN DỤNG

<figure><img src="../../.gitbook/assets/image (421).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (422).png" alt=""><figcaption></figcaption></figure>

## thiết kế workflow

mỗi công việc - nghiệp vụ sẽ cần định nghĩa được quy trình các bước và các quy chuẩn, điều kiện thực hiện.

* các trạng thái (status) và luồng đi (transition) giữa các trạng thái
* điều kiện và phân quyền hành động chuyển trạng thái
* tự động hóa các tác vụ tiêu chuẩn

**luklak workflow** có thể sử dụng cho rất nhiều tính chất khác nhau:

* BPM (Business Process Management): chuẩn hóa và tự động hóa các quy trình hoạt động trong doanh nghiệp, trong văn phòng
* SOP (Standard Operating Procedure): với các doanh nghiệp vận hành theo kiểu chuỗi nhiều cơ sở ở nhiều nơi như các cửa hàng, phòng khám, trung tâm tiếng anh thì SOP là rất quan trọng để đảm bảo chất lượng đồng đều ở các cơ sở
* CMMS (Computerized Maintenace Management System): quản lý bảo trì trang thiết bị, máy móc, cơ sở vật chất.

<figure><img src="../../.gitbook/assets/image (423).png" alt=""><figcaption></figcaption></figure>

sự khác nhau giữa universal workflow của luklak (thế hệ 3) và các app quy trình riêng lẻ của base, misa, 1office (thế hệ 2)

* **base, misa, 1office**: các bên đó là phần mềm thế hệ 2 (feature software), mỗi chức năng tách thành 1 app riêng, mỗi bên thường có tầm 40 con app riêng biệt cho các chức năng khác nhau. và quy trình là 1 trong số 40 con app đó. chỉ khi vào app quy trình thì mới thiết lập được quy trình và một số tác vụ tự động hóa, còn ở 39 app chức năng khác như quan lý công việc, nhân sự, phê quyệt… thì không có khả năng thiết lập quy trình & tự động hóa…
* **luklak universal workflow & automation:** có tính phổ quát áp dụng được trên toàn hệ thống, ở bất kì đâu, bất kì chức năng công việc nào cũng có thể thiết lập quy trình, và có thể tự động hóa các tác vụ, kết nối dữ liệu tương tác với nhau được. task management của luklak cũng có workflow xịn này, các chức năng tự tạo ra như hrm, crm, request… đều có hết

## cài đặt automation

* luklak automation cho phép tự động hóa các tác vụ một cách chính xác, không mất thời gian, không phụ thuộc vào con người.
* đây là universal automation (tượng tự universal workflow), nên nó không phải là một app automation riêng biệt tách riêng nằm một nơi, mà nó là một thứ phổ quát có hiệu lực ở bất kì đâu, bất kì chức năng nào tạo ra đều có thể dùng universal automation này, và universal automation này có khả năng tác động và kết nối dữ liệu và nghiệp vụ ở tất cả các chức năng lại với nhau.
* khi cài đặt **workflow** ở trên thì bên trong workflow cũng cho phép gọi các automation ra để gia tăng sức mạnh vượt trội cho workflow. ngoài ra thì có thể cài đặt automation ở mọi nơi khác nhau như **function (chức năng), area (khu vực), space (mảng việc)**

<figure><img src="../../.gitbook/assets/image (424).png" alt=""><figcaption></figcaption></figure>

một số ví dụ tự động hóa:

* khi ứng viên phỏng vấn đạt và nhận offer (chuyển trạng thái sang NHÂN OFFER) thì tự động tạo một mục việc hội nhập nhân sự, và lấy thông tin ứng viên điền vào thông tin nhân sự mới
* khi đề xuất chi từ bộ phận đưa lên, nếu chuyển sang trạng thái DUYỆT & ĐỢI CHI thì sẽ chuyển người làm (assignee) từ người đề xuất ban đầu sang cho kế toán chi.
* một khách hàng mới được tạo trên hệ thống CRM thì sẽ tự động gửi đi một email chào mừng và có nội dung tài liệu giới thiệu về sản phẩm.

## bộ lọc (filter)

* bộ lọc (filter) và báo cáo (dashboard) tạo ra để phục vụ tính chất quản lý công việc, khi có nhiều đầu mục việc, nhiều thông tin dữ liệu thì filter & dashboard sẽ tổng hợp lại các thông tin đó theo tiêu chí đề ra từ trước.
* vì mọi đầu việc, dữ liệu người dùng tự tạo ra trên luklak đều là từ đối tượng universal object, nên luklak cho phép tổng hợp kết hợp dữ liệu từ mọi chức năng lại với nhau trong cùng 1 filter, dashboard… rất tiện (các phần mềm thế hệ 2 như base, misa, 1office… mỗi chức năng tách một app rời, không thể tổng hợp dữ liệu cùng nhau
* tạo bộ lọc dữ liệu theo một nhu cầu, tiêu chí nào đó và lưu lại để sau đó dùng hàng ngày hoặc chia sẻ cho người dùng cùng. bất kì trường thông tin dữ liệu nào tạo ra trên hệ thống đều có thể đưa vào làm điều kiện lọc
* cài đặt thông báo tự động về tình trạng công việc dựa trên filter, định kì gửi tới những người liên quan

một vài ví dụ ứng dụng về bộ lọc lưu sẵn và gửi thông báo:

* _các nhân sự nghỉ ngày hôm nay, gửi thông báo lúc 8h00 tới bộ phận nhân sự & trưởng các bộ phận khác_
* _các dữ liệu khách hàng mới về mà trong vòng 24h giờ nhân viên kinh doanh chưa xử lý, gửi thông báo lúc 9h00 tới quản lý kinh doanh_
* _các đầu việc chưa xong và trong vòng 7 ngày gần đây không có cập nhật gì, gửi thông báo 9h sáng thứ 2 hàng tuần tới cho nhân viên làm trực tiếp và người quản lý._

<figure><img src="../../.gitbook/assets/image (425).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (426).png" alt=""><figcaption></figcaption></figure>

## báo cáo (dashboard)

* đầu tiên là bắt đầu với cơ chế của filter (như ở trên) tổng hợp các dữ liệu đầu vào
* sau đó dùng các gadget của dashboard để thể hiện trực quan hóa (visualize) dữ liệu theo cách dễ nắm bắt nhất
* luklak nocode & lowcode cho phép người dùng tự tay kéo thả tạo các báo cáo đa dạng và đặc thù theo nhu cầu của riêng mình.

<figure><img src="../../.gitbook/assets/image (427).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (428).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (429).png" alt=""><figcaption></figcaption></figure>
