# Tổng quan

<figure><img src="../../.gitbook/assets/image (66).png" alt=""><figcaption></figcaption></figure>

### Tính chất chung

* **Mỗi loại mục (issue type)** là một nghiệp cụ cụ thể bên trong chức năng (fucntion) và được cấu hình với 2 yếu tố: trường dữ liệu (data field/ screen) và luồng việc (workflow) của công việc - nghiệp vụ đó.
* Ở luklak là **universal workflow**, khác với isolated workflow app ở phần mềm thế hệ 2 (feature software)

### Workflow

* Tạo nên từ status + transition.
* Thiết kế 2 tầng: status tự tạo, đa dạng, số lượng lớn, ko biết trước. status category có 6 loại cố định biết trước. sau đó có thể đưa vào UQL/ filter cả 2 tầng.
* Bổ sung thêm các cấu hình cài đặt sâu rộng, như condition, task....
* Gọi được các hành động từ automation ra để tự động xử lý

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXeRzO3DEkvLNL16PxkF5A9WvTDz51vYdZRl1e97_kWO8lWhO62mkR5vOuAGxudm7YWE2VRJ992a_ip4dFh0iKJggafu67bmsplcs8la0dXqNrm3DKvu8162UxZv79YI1QODd04eLIqNpssNmTIMUD1kCao?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

### I, MỘT SỐ KHÁI NIỆM VÀ PHÂN LOẠI WORKFLOW TRÊN LUKLAK

#### 1, Workflow là gì?

Workflow có thể được mô tả như là một chuỗi các bước, công việc hoặc quy trình được thực hiện để hoàn thành một nhiệm vụ hoặc một dự án cụ thể. Đối với các doanh nghiệp, workflow thường liên quan đến cách các quy trình làm việc được tổ chức và thực hiện để đạt được các mục tiêu kinh doanh.\


Cụ thể, workflow thường bao gồm:&#x20;

* **Bước và Công Việc:** Các công việc cụ thể được thực hiện trong quá trình làm việc.
* **Thứ Tự Các Bước:** Sự liên kết và thứ tự của các bước và công việc trong quy trình.
* **Người Thực Hiện:** Người hoặc các đơn vị chịu trách nhiệm thực hiện công việc.
* **Quyết Định và Phê Duyệt:** Các điểm kiểm soát hoặc quyết định trong quy trình.
* **Tương Tác Hệ Thống:** Cách hệ thống và công nghệ liên quan tương tác trong quy trình.
* **Tối Ưu Hóa:** Cố gắng để tối ưu hóa hiệu suất và hiệu quả của quy trình.\


Workflow thường được quản lý thông qua các công cụ và hệ thống về quy trình làm việc như các ứng dụng quản lý dự án, hệ thống ERP (Enterprise Resource Planning), hay các giải pháp quản lý công việc. Workflow giúp doanh nghiệp hiểu rõ và tối ưu hóa cách công việc được thực hiện để đạt được hiệu suất cao và đáp ứng mục tiêu kinh doanh.

Workflow (Tiến trình) trên Luklak được tạo nên từ 2 yếu tố chính:

* **Status (Trạng thái):** thể hiện trạng thái công việc đó đang ở giai đoạn nào.
* **Transition (Bước chuyển):** là các hành động để kết nối, chuyển công việc đó từ trạng thái này sang trạng thái khác.

### 2, Tính ứng dụng

Tính ứng dụng của workflow rất đa dạng và mạnh mẽ, có thể được áp dụng trong nhiều lĩnh vực khác nhau. Dưới đây là một số ứng dụng chính của workflow:

* **Quản lý Dự án:** Workflow giúp tổ chức và theo dõi các công việc, nhiệm vụ, và bước tiến trong các dự án. Các công cụ quản lý dự án thường tích hợp tính năng workflow để đơn giản hóa quy trình làm việc.
* **Quy trình sản xuất:** Trong môi trường sản xuất, workflow giúp định hướng rõ các bước sản xuất, từ đặt hàng nguyên liệu đến sản xuất và kiểm tra chất lượng.
* **Quy trình Kinh doanh:** Workflow có thể được sử dụng để tối ưu hóa các quy trình kinh doanh, bao gồm quy trình bán hàng, quản lý đơn hàng, và chăm sóc khách hàng.
* **Quản lý Tiếp thị:** Trong lĩnh vực tiếp thị, workflow có thể được sử dụng để theo dõi chiến lược tiếp thị, tạo nội dung, và duyệt xét chiến dịch quảng cáo.
* **Quản lý Dịch vụ Khách hàng:** Workflow giúp tổ chức các quy trình chăm sóc và hỗ trợ khách hàng để cải thiện trải nghiệm của họ.
* **Quy trình Nhân Sự:** Trong lĩnh vực nhân sự, workflow có thể được sử dụng để quản lý quy trình tuyển dụng, đào tạo nhân viên, đánh giá hiệu suất, và các quy trình nhân sự khác.
* **Quy trình Tài chính và Kế toán:** Workflow có thể giúp tổ chức các quy trình tài chính như xử lý hóa đơn, quản lý chi phí, và báo cáo tài chính.
* **Quy trình Y tế:** Trong lĩnh vực y tế, workflow có thể được sử dụng để theo dõi lịch trình bệnh nhân, xác định các bước điều trị, và quản lý dữ liệu y tế.

Bằng cách sử dụng workflow, tổ chức có thể cải thiện hiệu suất, minh bạch, và quản lý tổ chức một cách hiệu quả hơn trong nhiều lĩnh vực khác nhau.

### 3, Các loại workflow của phần mềm Luklak

Quy trình chuẩn hoá chính là yếu tố cốt lõi để xây dựng và vận hành hệ thống. Với nhiều phần mềm thì workflow là một tính năng đặc thù, mỗi một quy trình làm việc sẽ có một app riêng lẻ ví dụ như phần mềm HRM, CRM,... và chỉ ở app đó mới có tính năng workflow đó. Điều này dẫn đến việc doanh nghiệp phải dùng nhiều phần mềm khác nhau để vận hành, quản lý công việc và tốn nhiều chi phí để sử dụng. Còn ở luklak thì workflow là thuộc tính phổ quát, mặc định của issue (universal smart object) nên tất cả các công việc, chức năng tạo nên từ issue, dù lớn hay nhỏ, đều có workflow.

Workflow Luklak cho phép người dùng kéo thả, tùy chỉnh các status, transition một cách dễ dàng, linh hoạt theo từng quy trình công việc đặc thù khác nhau, tạo nên workflow trực quan. Nhân sự đang làm bất kì việc gì cũng có workflow đi kèm để hình dung ngay được chu trình là như nào và làm theo chuẩn.

Các tính năng đi cùng mỗi transition như validation, postfunction (action before, during, after a transition) giúp kiểm soát quy trình một cách chặt chẽ. Automation sẽ giúp kết nối nhiều bước trong một quy trình, nhiều quy trình khác nhau thành một hệ thống thông suốt business process management/ automation.

* **Workflow loại 1:** basic bộ workflow cũ vẫn dùng: bộ workflow này chỉ bao gồm định nghĩa các trạng thái và các bước chuyển. Cho phép người dùng có thể tự thiết lập các tiến trình trên màn hình theo đường thẳng hoặc rẽ nhánh linh hoạt. Là phiên bản workflow cũ mà hiện tại khách hàng vẫn đang sử dụng.&#x20;
* **Workflow loại 2:** standard - tiêu chuẩn: Bao gồm các trạng thái và bước chuyển chỉ đi theo đường thẳng nhưng người dùng có thể cấu hình được các điều kiện, nhập các trường dữ liệu cũng như có thêm tính năng tự động khi chuyển từ trạng thái này sang trạng thái kia, hoặc cấu hình ở ngay bước chuyển.&#x20;
* **Workflow loại 3:** advance - nâng cao: Là phiên bản hoàn thiện nhất của workflow trên Luklak, ở đó người dùng có thể linh hoạt tạo các tiến trình đi theo đường thẳng hoặc tiến trình đi theo luồng rẽ nhánh, kèm theo đó là cấu hình các điều kiện, trường dữ liệu, tự động khi chuyển trạng thái trên tất cả các nhánh của quy trình.

\


\
&#x20;
