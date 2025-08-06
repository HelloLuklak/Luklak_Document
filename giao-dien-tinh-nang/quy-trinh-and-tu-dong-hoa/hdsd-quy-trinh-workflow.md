# HDSD Quy trình (Workflow)

## Chuẩn hóa quy trình cho mọi nghiệp vụ

{% @guidejar/embed guideId="67485ecc-2c3d-46b6-bb0c-1098217dcda0" type="1" controls="on" url="https://www.guidejar.com/embed/67485ecc-2c3d-46b6-bb0c-1098217dcda0?type=1&controls=on" %}

## Chuẩn hóa chặt chẽ từng bước

Thiết lập điều kiện chuyển trạng thái, yêu cầu nhập liệu, các đầu việc liên quan & các quy tắc tự động hóa ở từng bước trên quy trình

### Điều kiện chuyển bước

<figure><img src="https://assets.guidejar.com/uploads/Ab6HdSyHa9nnByMIAaRL/ASlu6Wlc9hZwj7hXwAYmfwPOYJh2/1729728620481.png" alt=""><figcaption></figcaption></figure>

Luklak cho phép thiết kế linh hoạt nhiều điều kiện cho mọi quy trình. Cùng xem ví dụ bên dưới với các điều kiện được thiết kế cho nghiệp vụ Đề xuất mua sắm.

| Cấu hình                                                                                                                                                                              | Ví dụ                                                                                                                                        |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------- |
| <ul><li><p><strong>Người được chuyển:</strong> Chỉ ra chính xác người hoặc nhóm người có quyền chuyển đến trạng thái đích. Đảm bảo không vượt quá quyền hạn.</p><p><br></p></li></ul> | ![](https://assets.guidejar.com/uploads/Ab6HdSyHa9nnByMIAaRL/ASlu6Wlc9hZwj7hXwAYmfwPOYJh2/1729729265158.png)                                 |
| <ul><li><strong>Trường dữ liệu</strong>: Đảm bảo từng trường thông tin của nghiệp vụ phải đạt đúng yêu cấu trước khi chuyển trạng thái</li></ul>                                      | ![](https://assets.guidejar.com/uploads/Ab6HdSyHa9nnByMIAaRL/ASlu6Wlc9hZwj7hXwAYmfwPOYJh2/1729729282038.png)                                 |
| <ul><li><strong>Mục kiểm</strong>: Đặt ra điều kiện hoàn thành một phần hoặc toàn phần cho các checklist công việc cần làm</li></ul>                                                  | <p><br></p><p><img src="https://assets.guidejar.com/uploads/Ab6HdSyHa9nnByMIAaRL/ASlu6Wlc9hZwj7hXwAYmfwPOYJh2/1729729465573.png" alt=""></p> |
| <ul><li><strong>Mục việc con:</strong> Đảm bảo các mục việc con của nghiệp vụ đã đạt được các trạng thái, tiêu chí nhất định.</li></ul>                                               | <p><img src="https://assets.guidejar.com/uploads/Ab6HdSyHa9nnByMIAaRL/ASlu6Wlc9hZwj7hXwAYmfwPOYJh2/1729729417826.png" alt=""></p><p><br></p> |
| <ul><li><strong>Mục kết nối</strong>: Đảm bảo các đầu việc liên quan cần đạt các yêu cầu nhất định.</li></ul>                                                                         | <p><br></p><p><img src="https://assets.guidejar.com/uploads/Ab6HdSyHa9nnByMIAaRL/ASlu6Wlc9hZwj7hXwAYmfwPOYJh2/1729729452548.png" alt=""></p> |

👑**Linh hoạt ở mức độ cao nhất**: Hệ thống nocode linh hoạt cho phép cấu hình mọi điều kiện trong tích tắc. Chỉ cần chọn trạng thái đích đến, sau đó lựa chọn các cấu hình mong muốn là xong trong vài click. Không cần code, không phụ thuộc vào thuê ngoài.

<figure><img src="https://assets.guidejar.com/uploads/Ab6HdSyHa9nnByMIAaRL/ASlu6Wlc9hZwj7hXwAYmfwPOYJh2/1730698381247.png" alt=""><figcaption></figcaption></figure>

### Yêu cầu nhập liệu

{% @guidejar/embed guideId="52070ea6-95e3-449c-afab-232dbab8e878" type="1" controls="on" url="https://www.guidejar.com/embed/52070ea6-95e3-449c-afab-232dbab8e878?type=1&controls=on" %}

👑**Thu thập đầy đủ thông tin ở từng bước:** Trước mỗi bước trong quy trình, Luklak cho phép cấu hình pop-up nhập liệu, yêu cầu người chuyển trạng thái phải nhập liệu đủ các thông tin cần thiết mới cho chuyển sang bước tiếp theo. Đảm bảo chất lượng tuân thủ chặt chẽ, không mất công hỏi qua lại để làm rõ thông tin.

_Ví dụ pop-up yêu cầu nhập liệu trong luồng Đề xuất mua_:

![](https://assets.guidejar.com/uploads/Ab6HdSyHa9nnByMIAaRL/ASlu6Wlc9hZwj7hXwAYmfwPOYJh2/1729730167469.png)![](https://assets.guidejar.com/uploads/Ab6HdSyHa9nnByMIAaRL/ASlu6Wlc9hZwj7hXwAYmfwPOYJh2/1729730309021.png)

### Tự động hóa trên quy trình

👑**Tự động hóa sâu rộng ở từng bước:** Sau khi chuyển trạng thái, tự động kích hoạt các tác vụ tự động theo cấu hình bạn cần. Ví dụ:

* **Cập nhật trường**: Chọn ra trường dữ liệu đích và cập nhật giá trị theo nguồn đầu vào mong muốn. Ví dụ: Sau khi **Đề xuất mua** được chuyển sang _Lấy báo giá_, tự động lấy {_Tên sản phẩm_}ở phiếu đề xuất gắn vào trường {_Tiêu đề_} ở **Yêu cầu báo giá**
* **Cập nhật kết nối**: Yêu cầu hệ thống tìm và kết nối đến các mục liên quan. Ví dụ: Sau khi **Báo giá** đã được duyệt, tự động liên kết **Báo giá** với **Đề xuất mua.**
* **Tạo mục:** Tự động sinh ra các mục việc, nghiệp vụ liên quan trong quy trình. Ví dụ: Sau khi **Báo giá** được duyệt thì tự động sinh ra **Phiếu chi** để kế toán tiến hành nghiệp vụ xuất tiền.
* **Gửi email:** Tự động gửi email ra cho các đối tượng liên quan trong quy trình. Ví dụ: Ấn nút **Lấy báo giá** trên mục **Yêu cầu báo giá** để gửi email cho địa chỉ email của nhà cung cấp được liên kết đến.
* **Gửi chat:** Tự động gửi chat trong nội bộ hệ thống issue chat, space chat, private chat trong Luklak. Ví dụ: Khi **Đề xuất mua** chuyển sang Hoàn thành -> Gửi chat thông báo vào **Kênh Đề xuất mua sắm** với thông tin Sản phẩm, Số tiền & tag người liên quan vào.

ℹ️Tự động hóa thông suốt: Bên cạnh tự động hóa với kích hoạt là việc chuyển trạng thái trên quy trình, Luklak còn cung cấp Universal Automation, cho phép kéo thả linh hoạt tạo ra mọi quy tắc tự động. Với mô hình đơn giản: Trigger, Flow Logic, Action, bạn có thể nhanh chóng tự động kết nối dữ liệu, xử lý logic & tự động hóa tác vụ thông suốt mọi chức năng, nghiệp vụ trong hệ thống.



<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXcWdhB9aODdrSLFubwYQbzhYAFs2PtM_xdINx5MLlnFHGcNWT8rJc3kbi3OxhzyR-or6fCWyNo89Mt8AXzInnzmRRWWR-mbnFO2kjIoxX_T1Qw34Z2kb-sDFgWE38X9XG3tnx2jL1dw56ADTEqJJo7aoUk?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

## I, MỘT SỐ KHÁI NIỆM VÀ PHÂN LOẠI WORKFLOW TRÊN LUKLAK

#### 1, Workflow là gì?

Workflow có thể được mô tả như là một chuỗi các bước, công việc hoặc quy trình được thực hiện để hoàn thành một nhiệm vụ hoặc một dự án cụ thể. Đối với các doanh nghiệp, workflow thường liên quan đến cách các quy trình làm việc được tổ chức và thực hiện để đạt được các mục tiêu kinh doanh.

Cụ thể, workflow thường bao gồm:&#x20;

* Bước và Công Việc: Các công việc cụ thể được thực hiện trong quá trình làm việc.
* Thứ Tự Các Bước: Sự liên kết và thứ tự của các bước và công việc trong quy trình.
* Người Thực Hiện: Người hoặc các đơn vị chịu trách nhiệm thực hiện công việc.
* Quyết Định và Phê Duyệt: Các điểm kiểm soát hoặc quyết định trong quy trình.
* Tương Tác Hệ Thống: Cách hệ thống và công nghệ liên quan tương tác trong quy trình.
* Tối Ưu Hóa: Cố gắng để tối ưu hóa hiệu suất và hiệu quả của quy trình.

Workflow thường được quản lý thông qua các công cụ và hệ thống về quy trình làm việc như các ứng dụng quản lý dự án, hệ thống ERP (Enterprise Resource Planning), hay các giải pháp quản lý công việc. Workflow giúp doanh nghiệp hiểu rõ và tối ưu hóa cách công việc được thực hiện để đạt được hiệu suất cao và đáp ứng mục tiêu kinh doanh.

Workflow (Tiến trình) trên Luklak được tạo nên từ 2 yếu tố chính:

* Status (Trạng thái): thể hiện trạng thái công việc đó đang ở giai đoạn nào.
* Transition (Bước chuyển): là các hành động để kết nối, chuyển công việc đó từ trạng thái này sang trạng thái khác.

#### 2, Tính ứng dụng

Tính ứng dụng của workflow rất đa dạng và mạnh mẽ, có thể được áp dụng trong nhiều lĩnh vực khác nhau. Dưới đây là một số ứng dụng chính của workflow:

* Quản lý Dự án: Workflow giúp tổ chức và theo dõi các công việc, nhiệm vụ, và bước tiến trong các dự án. Các công cụ quản lý dự án thường tích hợp tính năng workflow để đơn giản hóa quy trình làm việc.
* Quy trình sản xuất: Trong môi trường sản xuất, workflow giúp định hướng rõ các bước sản xuất, từ đặt hàng nguyên liệu đến sản xuất và kiểm tra chất lượng.
* Quy trình Kinh doanh: Workflow có thể được sử dụng để tối ưu hóa các quy trình kinh doanh, bao gồm quy trình bán hàng, quản lý đơn hàng, và chăm sóc khách hàng.
* Quản lý Tiếp thị: Trong lĩnh vực tiếp thị, workflow có thể được sử dụng để theo dõi chiến lược tiếp thị, tạo nội dung, và duyệt xét chiến dịch quảng cáo.
* Quản lý Dịch vụ Khách hàng: Workflow giúp tổ chức các quy trình chăm sóc và hỗ trợ khách hàng để cải thiện trải nghiệm của họ.
* Quy trình Nhân Sự: Trong lĩnh vực nhân sự, workflow có thể được sử dụng để quản lý quy trình tuyển dụng, đào tạo nhân viên, đánh giá hiệu suất, và các quy trình nhân sự khác.\
  Quy trình Tài chính và Kế toán: Workflow có thể giúp tổ chức các quy trình tài chính như xử lý hóa đơn, quản lý chi phí, và báo cáo tài chính.
* Quy trình Y tế: Trong lĩnh vực y tế, workflow có thể được sử dụng để theo dõi lịch trình bệnh nhân, xác định các bước điều trị, và quản lý dữ liệu y tế.

Bằng cách sử dụng workflow, tổ chức có thể cải thiện hiệu suất, minh bạch, và quản lý tổ chức một cách hiệu quả hơn trong nhiều lĩnh vực khác nhau.&#x20;

#### 3, Các loại workflow của phần mềm Luklak

Quy trình chuẩn hoá chính là yếu tố cốt lõi để xây dựng và vận hành hệ thống. Với nhiều phần mềm thì workflow là một tính năng đặc thù, mỗi một quy trình làm việc sẽ có một app riêng lẻ ví dụ như phần mềm HRM, CRM,... và chỉ ở app đó mới có tính năng workflow đó. Điều này dẫn đến việc doanh nghiệp phải dùng nhiều phần mềm khác nhau để vận hành, quản lý công việc và tốn nhiều chi phí để sử dụng. Còn ở luklak thì workflow là thuộc tính phổ quát, mặc định của issue (universal smart object) nên tất cả các công việc, chức năng tạo nên từ issue, dù lớn hay nhỏ, đều có workflow.

Workflow Luklak cho phép người dùng kéo thả, tùy chỉnh các status, transition một cách dễ dàng, linh hoạt theo từng quy trình công việc đặc thù khác nhau, tạo nên workflow trực quan. Nhân sự đang làm bất kì việc gì cũng có workflow đi kèm để hình dung ngay được chu trình là như nào và làm theo chuẩn.

Các tính năng đi cùng mỗi transition như validation, postfunction (action before, during, after a transition) giúp kiểm soát quy trình một cách chặt chẽ. Automation sẽ giúp kết nối nhiều bước trong một quy trình, nhiều quy trình khác nhau thành một hệ thống thông suốt business process management/ automation.

* Workflow loại 1: basic bộ workflow cũ vẫn dùng: bộ workflow này chỉ bao gồm định nghĩa các trạng thái và các bước chuyển. Cho phép người dùng có thể tự thiết lập các tiến trình trên màn hình theo đường thẳng hoặc rẽ nhánh linh hoạt. Là phiên bản workflow cũ mà hiện tại khách hàng vẫn đang sử dụng.&#x20;
* Workflow loại 2: standard - tiêu chuẩn: Bao gồm các trạng thái và bước chuyển chỉ đi theo đường thẳng nhưng người dùng có thể cấu hình được các điều kiện, nhập các trường dữ liệu cũng như có thêm tính năng tự động khi chuyển từ trạng thái này sang trạng thái kia, hoặc cấu hình ở ngay bước chuyển.&#x20;
* Workflow loại 3: advance - nâng cao: Là phiên bản hoàn thiện nhất của workflow trên Luklak, ở đó người dùng có thể linh hoạt tạo các tiến trình đi theo đường thẳng hoặc tiến trình đi theo luồng rẽ nhánh, kèm theo đó là cấu hình các điều kiện, trường dữ liệu, tự động khi chuyển trạng thái trên tất cả các nhánh của quy trình.

## II, HƯỚNG DẪN SỬ DỤNG CHI TIẾT CÁC LOẠI WORKFLOW TRÊN LUKLAK

#### Workflow loại 1: Cơ bản-basic (bộ cũ vẫn dùng)

**1, Ví dụ thực tế**

VD1: Quy trình “Xử lý Khách hàng mới” và “Chốt Giao dịch”

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXcbn42pApYa9IpVb1Rp_2JO83pxkADgT1G9Pw3vMxljPgCS9CtP7ivuFz7oAcIhK6vex_SNovNzg1kLgoQikXu2NMudTtMgvEcB8nnS_3t1hlJqIxVjbteH3fSxFuj5yPzPeMpN1WStisPt4b5cYy5v_GlD?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

Dưới đây là một ví dụ cụ thể về tiến trình tư vấn bán hàng thường gọi là tiến trình deal trong một đơn vị kinh doanh. (Đây là tiến trình gồm các bước cơ bản - Tiến trình này có thể thay đổi tùy vào đặc thù kinh doanh của từng đơn vị)

Trạng thái ban đầu: **Khách hàng mới**

* Khách hàng mới: là nơi nhập các thông tin khách hàng đăng ký với doanh nghiệp hoặc tạo lên từ các nguồn như website hoặc qua các kênh khác.

Theo luồng thông thường, khi tiếp nhận thông tin, bộ phận kinh doanh sẽ tiến hành xử lý sơ bộ để xác định sự phù hợp của khách hàng với sản phẩm.

* Nếu Xử lý sơ bộ Đạt => chuyển thông tin khách mới đến bộ phận “Tư vấn”
* Nếu Xử lý sơ bộ không Đạt => chuyển thông tin khách vào trạng thái “Không phù hợp”, lưu trữ để sau này có thể tìm lại thông tin khách và chăm sóc lại nếu cần.

Bước tiếp theo là **Tư vấn**&#x20;

Ở bước này Tư vấn viên sẽ làm rõ yêu cầu khách hàng cần là gì? Và thuyết phục khách hàng mua sản phẩm của mình

* Nếu sản phẩm phù hợp, chuyển sang trạng thái “Báo giá” cho khách hàng
* Nếu sản phẩm không phù hợp, tiếp tục “Chăm sóc tiếp”

Bước thứ 3 là **Báo giá** &#x20;

* Nếu phù hợp, nhóm tư vấn sẽ tạo báo giá về sản phẩm/dịch vụ theo yêu cầu của khách hàng. Khách hàng đồng ý sẽ chuyển “Chốt sơ bộ”, sau đó lên Hợp đồng/Đặt cọc
* Trường hợp khách còn phân vân thì nhân viên kinh doanh lại tiếp tục “Chăm sóc tiếp”. &#x20;

Bước thứ 4 là **Chăm sóc tiếp** để lên hợp đồng/Đặt cọc

* Nếu khách hàng còn băn khoăn, thì nhân viên kinh doanh/tư vấn sẽ tiếp tục chăm sóc và hỗ trợ để thuyết phục khách hàng.

Bước thứ 5: **Chốt sơ bộ**

* Sau khi các điều khoản cơ bản được thảo luận và chấp nhận, có thể tiến hành chốt sơ bộ giao dịch.

Bước thứ 6: **Thành công Hợp đồng chính thứ**c và **Chốt giao dịch**- “Thành công” hoặc “Thất bại”

* Tiến hành lên hợp đồng chính thức với các điều khoản cụ thể và chi tiết hơn.
* Khi hợp đồng được ký kết và chốt, giao dịch được coi là thành công.

Trường hợp khách hàng không phù hợp, công ty vẫn lưu trữ thông tin khách hàng Deal được gọi là “Thất bại”

Vậy với **Quy trình Xử lý Khách hàng mới** và **Chốt Giao dịch trên**, chúng ta có thể mô tả bằng workflow trên phần mềm Luklak như sau:&#x20;

Khi mô tả quy trình làm việc này lên Luklak, chúng ta thấy rõ rằng quy trình này đường đi nước bước như thế nào, các bước cần làm khi đến giai đoạn tiếp theo. Với 1 quy trình này, người làm dù đang ở giai đoạn nào cũng định hướng được công việc của mình cần phải làm.&#x20;

Workflow bán hàng được mô tả rõ, giúp giảm thiểu lỗi phát sinh trong quy trình bán hàng, tạo ra kết quả chính xác và đáng tin cậy hơn. Một workflow bán hàng hiệu quả không chỉ tăng cường trải nghiệm cho khách hàng mà còn tối ưu hóa quy trình làm việc nội bộ và cung cấp thông tin cần thiết để định hình chiến lược kinh doanh.

Vậy chúng ta hãy cùng xem workflow này được thiết lập như thế nào trên Luklak khi tham khảo phần 2 các thuật ngữ liên quan và phần 3 hướng dẫn sử dụng phần mềm sau.

#### **2, Các thuật ngữ liên quan**

Màn hình tạo mục việc sẽ gồm các phần:

* Space (mảng việc): chọn xem mục việc cần nằm ở chỗ nào trong cơ cấu bộ phận, phòng ban.&#x20;
* Issue type (loại mục): trong mỗi space có thể có các loại việc khác nhau tương ứng với các chức năng và quy trình làm việc khác nhau đã được định nghĩa trước. Khi tạo thì cần chọn đúng loại việc cần làm.
* Issue title (tiêu đề): nhập tên công việc
* Custom field (trường dữ liệu): là các trường dữ liệu, thông tin cụ thể cần có, phục vụ cho công việc đó.

Các thuật ngữ khác

* Workflow (tiến trình): thể hiện các trạng thái công việc khác nhau (status) và các bước chuyển (transition) quy định đường đi từ trạng thái này sang trạng thái khác.Mỗi loại việc (issue) sẽ có một quy trình, quy chuẩn làm việc tương ứng. Workflow của Luklak với Status và Transition dùng để tạo một quy trình trực quan, bao gồm các trạng thái và các bước chuyển.
* Status (Trạng thái): thể hiện trạng thái công việc đó đang ở giai đoạn nào.
* Transition (Bước chuyển): là các hành động để kết nối, chuyển công việc đó từ trạng thái này sang trạng thái khác.
* Phòng làm việc: [Tại đây](https://docs.google.com/document/d/1sBbgwc9MC7OluZyWQPRcW3jsPf0ZMM87U1vYSKGP9C4/edit?usp=sharing)
* Bộ lọc: [Tại đây](https://docs.google.com/document/d/16NsV6c-i9voxoNHueyzA-kLc4x-JeAqWtBPB2qvOMGQ/edit?usp=sharing)
* Báo cáo: [Tại đây](https://docs.google.com/document/d/1Yp3UOH8xpG2Rvr-7I0eX3t-H3pO5B2JlLjA4vLYu2cQ/edit?usp=sharing)

#### 3, Giao diện màn hình, HDSD

Ví dụ dưới đây về một đầu việc "xin nghỉ phép", với workflow được thiết kế theo quy trình xin nghỉ. Nhân sự khi xin nghỉ phép thì mọi thông tin hiển thị trên màn hình và tiến trình sẽ chạy giống nhau như sau:

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXfeQxJ94P4yHM1fCqG4fkXUzeAk1MqIaTGLyvg5fsPgy4g0GES4u0KZNVxE_k-nwnI-nQq_V09dDz6ue66Kod8EfuDiufqOCoRPxGQkiW_X0x7CJLIWRuZ2MuYRkXHahsEOOotpYwnz9xFFyDGqJaimmtFS?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

Màn hình mục việc xin nghỉ

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXfMI49U5uLY69UOC3XKVhQBcVHYVBfZjO6Ml_k60gGHbReLr5_4rNWd38modg78uChQzqcLv3PhvH8sXDDIQyHW3iRSK_zFBm-LrDYWdOmCfdmwRRyXGQDblYvWzZ_1DSQ1ti6fpys6rqdaI_a8t8MzGHO0?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

**Tiến trình xin nghỉ**

Màn hình của mục việc xin nghỉ hiển thị đầy đủ các thông tin liên quan để người phê duyệt có thể nắm bắt và thực hiện phê duyệt cho nhân viên. Thông tin được cập nhật để người làm đơn biết rằng đơn của mình đã được chấp nhận hay chưa. Thông tin lưu lại trên hệ thống để những người liên quan ví dụ như bộ phận nhân sự nắm bắt được và dễ dàng thống kê được nhân viên trong tháng đã nghỉ bao nhiêu ngày, tổng số ngày nghỉ theo từng loại nghỉ là bao nhiêu.

Hoặc tiến trình bán hàng cho một khách hàng, đã nêu ở ví dụ trước. Workflow như này sẽ có những giá trị sử dụng như sau:&#x20;

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXeHL1qvh5qll-hJrJV77hEa6vkuufDIncb3uDVMRtffoIL1qDJHDrioTGioT6p9qQuux3jaSK-L0RIF_1-qnNSeMhXCEmGCh2FiwI9o7xqsg6rlb7kKWS1Co6u1hYx-DWU4WQlpW4liXw4ouFy-1XnjeK4b?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

* Thể hiện trực quan, rõ ràng các bước trong tiến trình, giúp nhân sự nhìn vào hiểu được đường đi nước bước, cách làm của công việc.
* Khi thực tế làm việc thì cũng báo cáo, hành động trên tiến trình đó, làm đến đâu chuyển trạng thái đến đó để cả mình hoặc quản lý, người liên quan nắm được công việc đang ở đâu, như thế nào
* Các trạng thái này sẽ được đưa vào Bộ Lọc & Báo Cáo (Filter & Dashboard) để tổng hợp, phân tích, nắm bắt tổng thể tình hình công việc.

Bên trên là những tính năng đã có sẵn dùng được ngay với Tiến Trình (Workflow), hiện tại Luklak đang phát triển thêm những tính năng tiếp theo như:

* Tự động chuyển người làm (Assignee) sang người khác thi thay đổi Trạng Thái (Status) trong Tiến Trình.
* Các chức năng Automation, khi có sự thay đổi nào đó trong Workflow thì sẽ tự định nghĩa được các hành động phát sinh tiếp theo như nào.

\=>Những tính năng này sẽ được dùng ở loại tiến trình Workflow loại 2: standard - tiêu chuẩn, Workflow loại 3: advance - nâng cao\


#### **3, Các thao tác cần làm với một Workflow sẽ bao gồm:**

**A, Tạo tiến trình:**

Chi tiết hướng dẫn: [Tại đây](https://docs.google.com/document/d/1bJc3HOJtZvGE7puDINU7KbNSVyHXO2fk/edit#heading=h.4d34og8)

**B. Chuyển trạng thái/ tiến trình**

* Mỗi mục việc (issue) được tạo từ một issue type nhất định đều có tiến trình & các trạng thái (workflow & status) của nó, thể hiện rõ quy chuẩn công việc đó sẽ có những bước như nào.&#x20;
* Người làm (assignee), người giám sát cần chuyển trạng thái phản ánh đúng tình hình công việc, ví dụ như chưa làm, đang làm, đã xong, đóng huỷ…
* Chuyển đúng trạng thái giúp chính cá nhân đó tổng hợp được tình hình công việc, nắm bắt được những đầu việc mình đang làm cùng lúc như nào, để sắp xếp và lên kế hoạch công việc phù hợp hơn. Bên cạnh đó, điều này cũng giúp cấp trên và người liên quan dễ nắm bắt tình hình và phối hợp, tương tác.

Ngoài nút chuyển trạng thái ở trên cùng tương tự như tất cả các app khác, thì luklak là bên duy nhất đẩy mạnh trải nghiệm người dùng bằng cách đẩy luôn các trạng thái vào ngay trên ô chat trao đổi về đầu việc. việc này có giá trị:

* Nâng cao nhận thức của người dùng, lúc nào cũng biết công việc đang ở trạng thái nào, vì thường xuyên chat trao đổi.
* Thúc đẩy cập nhật chuyển trạng thái đúng tiến trình, vì đang chat thì có thể click chuyển trạng thái ngay được, rất tiện.

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXfiHIEPCpugkYlNW7Lcnl3VDAzial80xW33IN1TU4mMXCuXngWqKK0dgzPF0eBT0U6gDINsOQq6k960fvV35IMCi3FybW21-tJEi48OVQsQOi-Gs1vZL1HB0K38ICPJi-_ouNVZ2403rF2W8b8taKu924IG?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

\
\


**C, Xem báo cáo theo status**

&#x20;   Người dùng hoàn toàn có thể xem báo cáo danh sách các mục việc theo nhóm status hoặc theo status dạng Kanban, để có cái nhìn về bức tranh công việc một cách tổng thể.

* Kanban theo nhóm status:

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXe_y-j30NKbtRa7rp58LXYdozDAEfhd2Djv6xKZFeU0iU5d79pAKAGbNnjrkO3ggaqlRuhpll1H-TkLx1JtYize3iemuOolUi7ZeZqLk-X0GPe8vNXYdnWG1SHVNu4WV2FbURyR24AdbprUM8tSZ-iDLQnc?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

Status được phân nhóm thành nhiều loại như:

* Kế hoạch
* Mở
* Hoạt động
* Hoàn thành
* Tạm dừng
* Đóng hủy

Khi tạo 1 status, người dùng sẽ lựa chọn được status đó thuộc nhóm trạng thái nào, ví dụ: Cần làm là nhóm Mở, Đang làm là nhóm hoạt động, Hoàn tất là nhóm hoàn thành và Đóng hủy sẽ thuộc nhóm Đóng hủy.&#x20;

Việc phân nhóm này giúp quản lý các mục việc dễ dàng hơn, dựa vào các nhóm, người dùng biết được những mục nào đang ở nhóm mở, lên kế hoạch, mục việc nào đang làm, mục việc nào đã xong, mục việc nào tạm dừng/đóng hủy và có thể mở lại.

Khi theo dõi mục việc dựa trên nhóm trạng thái của Luklak, người dùng hoàn toàn có thể dùng báo cáo dạng cột Kanban để có một bức tranh tổng quan, thống kê toàn bộ các mục việc đang ở tiến độ nào.

Đứng dưới góc độ chi tiết của 1 quy trình, người dùng cũng có thể xem báo cáo Kanban theo từng trạng thái như sau:

* Kanban theo từng status

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXesyNlpVtems4jBQCzQJYyYrDqzBUnP-NCRnaKv1UwssgioX9GRs453-fyQXhqFgp52mf450xOz4FagvIfUMoN6aMa2pqmrt6235NGrGQAtdvZZ8jFHSstOYSav7JLfy0rE5t3fo4lT0cckzP4WvIt9lXE?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

Với tính năng này, người dùng có thể nắm bắt được các đầu công việc đang đến giai đoạn nào, có bao nhiêu công việc cần làm, đang làm và đã xong. Ngoài ra, người dùng hoàn toàn có thể xem chi tiết mục việc bằng cách click vào ngay mục việc đó và cập nhật trạng thái của tiến trình bằng cách kéo thả các mục việc từ cột này sang cột kia của Kanban mà không cần vào hẳn mục việc để thay đổi.



**D, Tạo bộ lọc theo Status**

Người dùng cũng có thể dùng bộ lọc theo dạng status (trạng thái) để thống kê danh sách công việc theo trạng thái, ví dụ xem những công việc nào đã hoàn thành, công việc nào đang làm, tạm hoãn… hoặc các công việc lọc theo từng trạng thái người dùng đã thiết lập trên workflow.

Người dùng có thể lọc theo status hoặc nhóm status thông thường. Để thao tác nhanh, có thể dùng ngay thanh công cụ lọc tiêu chuẩn ở màn hình giao diện danh sách mục việc.,,k,,,

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXfuAe22YY68h9bnTIgqBtyilN_hVOJeWYcBb_BvcRa5dlnYR49q0a3W5liH97qi9Pg-Kj7nMHOuJYSm8OY28Sc5ME5t_IR7dOS93T3DxIpKk3kMJSH6JQERPzMbiJY-td-wM9icPW1F2oGqmg4TZuwAwFBt?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

**VD:** lọc những công việc đang lên kế hoạch, để sắp xếp thời gian tiến hàng làm.

Người dùng cũng hoàn toàn có thể phối hợp thêm các điều kiện lọc khác, hoặc áp dụng thêm nhiều tiêu chí lọc nâng cao hơn. Kết hợp giữa lọc theo trạng thái và các điều kiện lọc mong muốn.

![](https://lh7-us.googleusercontent.com/docsz/AD_4nXdyxwOqa889McdpGpdo7HjKzAXzpu_2w-PPSSQUeKfXdQ8BVwMJnd4qRGziWPleP66Bdf19I4yt7v0PekgsKhY-msg-uC-CSBe7p9COR01PLusxKUXgqP-gSRtC0Gr0BHerMp0Zj6eUz-BprFxM-JVKAfrk?key=Pj5SQn1IP1YRt0MtCTTbqw)

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXfFMAnIAEReCX7nAM6g7YgKEJurzGpx5mzct_pr_IfIUE_JUtJpDCNh1OcPWYeLcqA14DBo6mChWWRcUCQuAYnZAfsT6iGcREwbcviYhNKLpHuf-K5l72SSkjz1B_gJwD6ShCB7S--9_ZJeEQdLdcp4Yy7k?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>



Hoặc người dùng có thể tạo các bộ lọc riêng, kết hợp tiêu chí lọc theo trạng thái.

**VD:** Thống kê những đơn hàng có trạng thái là “hoàn thành” với giá trị > 100 triệu đồng.

![](https://lh7-us.googleusercontent.com/docsz/AD_4nXcLyas33-p-bjSdqh5kGx_tgDVmTIYugvjY8tM7UiZzfobYHwDI9We2T-GPYX2rwWd1qUzAzUkKwQJJYXdQeJWGTWeShNJAaiu-L3QoXPdj9IhDSmeEz4wkWBCmdEA8rPvWL0NcOAm9lDf91XY7A5PNhF9-?key=Pj5SQn1IP1YRt0MtCTTbqw)![](https://lh7-us.googleusercontent.com/docsz/AD_4nXero81FK9-KxH_zYdscZx2OkFjclu1QWB16eL-0sHOJnfAEq1z15GKfG77OSse2UXy3j7RcBiU6bg_nUIg1FhpNR-FqqdZIqf8iWpOfc_Z7iA-2ac75XHnRVUTNo0sbKnCFkqbKMB5TPckt2-c6fXpPHs5L?key=Pj5SQn1IP1YRt0MtCTTbqw)

Với workflow thông thường, ngoài việc theo dõi luồng tiến trình thực hiện trực quan dễ dàng, người dùng vừa tiết kiệm thời gian, vừa giảm thiểu chi phí khi quản lý công việc, mà thao tác cũng rất dễ dùng và đơn giản.&#x20;

Ngoài luồng workflow trên, phần mềm đã và đang phát triển thêm tính năng nâng cao hơn, nhiều luồng tự động hơn đáp ứng linh hoạt nhiều tình huống hoạt động trong doanh nghiệp của khách hàng với loại Workflow 2 và 3 dưới đây, mời mọi người cùng tham khảo.

### Workflow loại 2: Standard - Tiêu chuẩn

#### **1,  Ví dụ thực tế**

![](https://lh7-us.googleusercontent.com/docsz/AD_4nXdyp5fGAwtuXAycebg6D4N8hSUb1IhJmrPEm6Tu5VP0MUE8X7r-2hajk8onnILwzTwKKHlDRueN4kuiIbR084nGeKtEHXZTMj4qkCZOQLegMsqeS1FKxKaoZff7rZ8O842ehpT2UPF5NqDg3etlx0osVTE?key=Pj5SQn1IP1YRt0MtCTTbqw)![](https://lh7-us.googleusercontent.com/docsz/AD_4nXeX6G6ryIydmNzTWbqn7d4vtJ3rqD9GkFuPdfCkxpmuh9FGBsrd_eJHDL9Cmqy8bMcv-PBEwXgUX1hQ0nAJQGwbqzQr8RvOXxGb6bUu6Nv7CtaTkJcsUZ6MATraGQPcaRwSqOIwD9Oz-r6kq3zIEQ2SQSsC?key=Pj5SQn1IP1YRt0MtCTTbqw)

Ví dụ về một quy trình quản lý kho như trên, tiến trình công việc được thể hiện thành một Workflow standard như bên cạnh. Các giai đoạn, công việc xuất hiện trong quy trình sẽ được thể hiện dưới dạng các trạng thái và được đánh số thứ tự để người dùng có thể thấy được thứ tự các công việc cần thực hiện một cách rõ ràng, minh bạch.

Như đã nói ở phần Workflow basic, Workflow standard sẽ có thêm các tính năng mới và một trong số đó là đưa ra các điều kiện về người chuyển, các trường thông tin và các mục liên kết phải thỏa mãn những yêu cầu đã được đặt trước đó để cho phép chuyển trạng thái.&#x20;

Ví dụ như ở trạng thái 6 là Kiểm tra, người dùng có thể cài đặt điều kiện người có quyền chuyển trạng thái là trưởng phòng phòng HC-KT (lúc này chỉ một mình trưởng phòng mới chuyển được trạng thái kiểm tra) và các trường dữ liệu như Số lượng thực nhận phải bằng, lớn hay nhỏ hơn một số lượng đã được cài đặt sẵn. Khi chuyển trạng thái, hệ thống sẽ kiểm tra các điều kiện và khi thỏa mãn tất cả mới cho phép chuyển trạng thái như hình dưới.



<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXdOU6kcvcjwwMweR8K5rmHxRe3tS-41WeROhY2DQGgDJsWqABxA5nYFvA8TCIIQikAXFFZJb6SKAQ6X5eJn4Isd2QoacqW0nT18MIfq3ezqDtaMTBk4LGk0Rzf32G3vSYRrQ5T0XSooHJXboXXU_DfjyNM?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

Bên cạnh đó, mỗi giai đoạn trong công việc đều có nhu cầu nhập liệu, quản lý những dữ liệu khác nhau. Điều này sẽ gây bất tiện nếu như đến mỗi trạng thái, người dùng phải tìm kiếm những trường dữ liệu tương ứng cần điền hay cập nhật khi thay đổi trạng thái công việc trên màn hình chung (nơi chứa tất cả các trường dữ liệu trong công việc cần quản lý). Hiểu được điều này, Workflow standard đã cho ra giải pháp bằng cách hiển thị pop up màn hình gồm những trường dữ liệu cần điền hay cập nhật khi người dùng chuyển trạng thái.&#x20;

Ví dụ khi người dùng chuyển trạng thái từ Tiến hành mua sang Kiểm tra, màn hình của trạng thái Kiểm tra sẽ hiển thị các trường dữ liệu cần nhập hay cập nhật tại trạng thái đó như Người kiểm tra, Số lượng đạt, Số lượng không đạt, … như hình dưới.



<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXe3rU7RB29bIpufHhrAjwYEx3aCvqyuzwUiMTVQuX9F-WNXJf7bDyw8TojOSQRvzVv6DM0Dbb_WuIop4TM2L7pbuMlivsKwazPMyc9KyLf2TIIh14ihB9VsGVE-xv5RUs3Dr4NZ89m94EPvHPVyDTMtdNkk?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

Không chỉ dừng lại ở đó, một trong những tính năng hỗ trợ người dùng nhiều nhất đó là tính năng tự động. Áp dụng tính năng này sẽ hỗ trợ người dùng tự động điền các trường dữ liệu, các thông tin cần quản lý ở từng trạng thái theo những quy tắc đã được đặt ra trước đó.&#x20;

Ví dụ khi chuyển trạng thái từ Lựa chọn nhà cung cấp sang Phê duyệt, người dùng có thể cài đặt sẵn người làm là một trong những người đã được chọn và trường dữ liệu Ngày phê duyệt là 2 ngày sau khi chuyển trạng thái không tính ngày thứ 7 và chủ nhật. Nếu có thể áp dụng được tính năng này một cách linh hoạt và phù hợp với quy trình làm việc của doanh nghiệp sẽ hỗ trợ rất nhiều về mặt thời gian quản lý công việc và độ chính xác của các thông tin khi nhập liệu lên hệ thống.&#x20;



<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXdbs7PfqNixn7eXEA9knNpU0zNyRs8XKVWGJoynLvLGuGwnZUACv0u7bGoNDRznQfobwzGX12ZKJh90UC01IpmS9xdTmIt51c1EPhm6WJcEf5wfq-U6D9a45lM7K7NJ6jDfrykSVc5ZxVQvC26owETU7mY?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

Đó chỉ là số ít những điều mà Workflow standard có thể làm được. Để có thể tìm hiểu đầy đủ và chi tiết về các tính năng tiện lợi của Workflow standard, người dùng có thể xem chi tiết ở dưới đây.

#### **2, Mục đích sử dụng, tính ứng dụng**

Workflow standard là một workflow gồm các status (trạng thái) sẽ chỉ đi theo một đường thẳng, tuần tự các bước, số thứ tự được đánh trên các status (và sẽ có các tính năng sau đó ăn vào số thứ tự của status). Bên cạnh đó Workflow standard cũng sẽ cung cấp thêm các tính năng mới hỗ trợ người dùng trong việc quản lý và thực hiện công việc. Các transition (bước chuyển) sẽ định nghĩa đường đi và kết nối các status, thể hiện mối quan hệ giữa các status được nối với nhau.

Workflow standard hứa hẹn sẽ đem đến cho doanh nghiệp một trải nghiệm làm việc thuận tiện trên luklak với các tính năng mới được cập nhật dưới đây:&#x20;

**Điều kiện:**&#x20;

* Mục đích sử dụng: Cho phép người dùng đưa ra/cài đặt các yêu cầu, điều kiện cho công việc ở mỗi giai đoạn của tiến trình công việc mà chỉ khi đáp ứng đầy đủ các điều kiện đó, hệ thống mới cho phép chuyển trạng thái.&#x20;

**Tác dụng:**&#x20;

* Đảm bảo công việc của doanh nghiệp ở từng giai đoạn được hoàn thành một cách đầy đủ, chính xác và hoàn chỉnh nhất có thể nhờ những điều kiện được cài vào trước đó
* Phân quyền rõ ràng cho những người thực hiện công việc, đảm bảo chỉ những người được cho phép mới có thể chuyển trạng thái trên issue



**Nhập liệu**

* Mục đích sử dụng: Ở mỗi giai đoạn của công việc, doanh nghiệp đều cần quản lý, nhập liệu các thông tin khác nhau, thay vì phải nhập liệu tất cả các thông tin trên cùng một màn hình như Workflow basic thì ở Workflow standard, mỗi trạng thái sẽ có có một màn hình riêng gồm những trường dữ liệu, thông tin mà doanh nghiệp cần quản lý. Khi chuyển trạng thái hay nhấp chọn vào trạng thái trên Workflow thì màn hình của trạng thái đó sẽ hiển thị các trường thông tin cần điền hoặc cập nhật ở trạng thái đó.

**Tác dụng:**&#x20;

* Việc nhập liệu thông tin công việc được tách biệt rõ ràng, minh bạch và không bị loạn&#x20;
* Giảm thiểu sai sót khi phải nhập liệu trên một màn hình gồm quá nhiều trường dữ liệu.&#x20;



**Tự động:**

* Mục đích: Tự động luôn là một tính năng đa dụng và hỗ trợ người dùng rất nhiều trong công việc. Người dùng có thể cài đặt trước các yêu cầu cần hệ thống thực hiện ở từng trạng thái và hệ thống sẽ tự động thực hiện các yêu cầu mà người dùng đưa ra ở trạng thái đó.&#x20;

**Tác dụng:**&#x20;

* Tinh giảm quy trình rườm rà, tự động hóa công việc nhập liệu thông tin sẵn có, thay vì người dùng phải tự nhập tay hay tính toán số liệu sau đó nhập lên Luklak.
* Tối ưu hiệu suất làm việc, rút gọn thời gian nhập liệu thông tin lên hệ thống để nhân sự tập trung làm những công việc quan trọng hơn

#### **3, Giao diện màn hình, HDSD**

Để ứng dụng được những tính năng phía trên vào trong phần mềm, phục vụ nhu cầu của người dùng, dưới đây, Luklak đưa ra hướng dẫn sử dụng chi tiết cho người có thể tự cấu hình. Những tính năng được bôi vàng đang được hoàn thiện và sẽ ra mắt sau 2 tuần nữa.

**Bước 1:** Ở thanh Menu, chọn vào phần Mở rộng, ấn chọn Chức năng. Sau đó lựa chọn chức năng muốn cấu hình và thêm tiến trình với lựa chọn Cấu hình là Tiến trình tiêu chuẩn.

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXfcGUYZ1LdmTZHjj_Vk5Jfr3GD8syKAn0Ad9z7wYTupwnbyaWopEsH4Ip5YyHpfgkbJniSuGMvuphWk_OXTgMAASE540OuCHZoGWJPVeD4p3nr5n4x8w7dzuO8zbZ2XEgvDYoSNMwyspZbHO4sBCL-xKCrB?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

**Bước 2:** Người dùng vẽ tiến trình và lựa chọn trạng thái muốn thiết lập tính năng

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXdNegShvVE2Ru1TiTh6fQ8ErjQdsV3kPsodQqp1ICbkTcZd0oCFfgPbkl6Qn8v1a4aCRJqzQ7-pUORE6OCt-ThTYlUx-1jQ9cYKT7SC4mUAayJ537MRjiKVBdZwwQFDhjgcgQo5M_34xE3BvucIVsI6N1Bu?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

**Bước 3:** Nhấn chọn Cấu hình và tiến hành cấu hình cho trạng thái

**Điều kiện:** cài đặt các điều kiện để hệ thống đối chiếu rồi đưa ra quyết định chuyển trạng thái. Dưới đây là các loại điều kiện mà người dùng có thể cài đặt:&#x20;

* Người được chuyển: những ai được chuyển với từng trạng thái và chỉ những người được cài đặt quyền chuyển trạng thái thì mới có thể chuyển trạng thái (admin/owner hoặc người được gán vào issue mà không nằm trong người được chuyển cũng không chuyển được trạng thái).&#x20;
* Có thể cấp điều kiện người ở 3 mức: dữ liệu trên issue field (assignee, supervisor...); dữ liệu ở space (component lead/member); dữ liệu từ tổ chức (nhập user, group cụ thể). Cài đặt này áp dụng linh hoạt cho từng trạng thái nhất định, bám sát chặt chẽ theo quy trình của doanh nghiệp.
* Các trường dữ liệu: cài đặt điều kiện ở từng trạng thái dựa trên dữ liệu của mục, ví dụ người dùng cài đặt Số lượng thực nhận lớn hơn 1000 thì khi giá trị được nhập ở trường dữ liệu Số lượng thực nhận phải đáp ứng được yêu cầu đó thì người dùng mới chuyển được trạng thái.
* Mục con/Mục kiểm: Những phiên bản trước đây của LUKLAK, subtask và checklist sẽ được gắn chung vào giao diện mục việc. Với bản cập nhật mới, subtask/checklist có thể gắn riêng vào từng trạng thái trong quy trình công việc. Điều này giúp người dùng biết rõ mỗi status sẽ có các mục con, mục kiểm nào thuộc về công đoạn đó. Từ đó sẽ ra được điều kiện cho chuyển trạng thái là: các subtask/checklist thuộc status hiện tại hoặc các status trước đó phải hoàn thành hết hoặc đặt ra mức bao nhiêu cái cần xong nhất định thì mới cho chuyển.
* Mục kết nối: Những mục được liên kết với đầu công việc đó phải ở một trạng thái nhất định mới chuyển được trạng thái của mục việc.&#x20;

_**Lưu ý:**_ khi người dùng cài đặt các điều kiện ở trạng thái nào thì trước khi chuyển sang trạng thái đó, hệ thống sẽ kiểm tra xem đã đáp ứng các điều kiện cài đặt chưa. Nếu đã đáp ứng thì sẽ cho chuyển trạng thái.

**Nhập liệu:** cài đặt màn hình cho từng trạng thái, mỗi trạng thái sẽ bao gồm những trường dữ liệu và liên kết nào.

**Tự động:** cài đặt các trường dữ liệu sẽ tự động cập nhật sau khi chuyển trạng thái. Các trường thông tin mà người dùng có thể yêu cầu hệ thống tự động thực hiện bao gồm:&#x20;

* Trường người: assignee, supervisor....
* Trường ngày: start date/ due date, any date
* Trường số:
* Trường text:
* Issue link: thêm và xóa

Các hành động mà chức năng tự động có thể thực hiện:&#x20;

Các cập nhật này đều có khả năng:

* Lấy nguồn dữ liệu từ issue khác điền vào
* Biến đổi dữ liệu kiểu thêm bớt, cộng trừ nhân chia…

**Tự động tạo:**

* Subtask
* Checklist\


<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXeJBLUQZYszlPAhlxNn8LyD9nLYE681quzb_XvaAVIkRuEKp7G9pZ9DjMyQDv4XcdfnHU8kPkFWKeXotGJxPE01hriXIefdG14P1yiG2ncjGmsM6u6sHnQ_AvIZSKi0wR9pihAg776HR8G6iUzkA9BGYA5x?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

**Bước 3.1**: cài đặt Điều kiện

* **Người được chuyển:** Chọn ra những người được quyền chuyển trạng thái

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXeLvCzjTdsSwihRoO1sy4W0tPM5Y2HFyI6JTUYCYYqfVX1nZddkkwYG_t91jeoXN9mMNuympbVXJwSAeMJ5UtU2ZlmPGDE3Mg9Smd12xo_yKaAMpdubVa6JkUOCK_zKpPdI5RXDCWNvJ4iwYu4dH2-wdYZC?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

* **Trường dữ liệu:** chọn ra các trường dữ liệu và đặt điều kiện cho những trường dữ liệu đó

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXf9UqefUCdt0BlVEluf1KI1GnX5r6KFnp-PppI6vuY-daHTK330zVvsaA_8ZVgi9zfsQ_kkRlYNZfkVLm0OyGp0GjkNAWu72a12YyGznJcS8OpVwojbCO3-AzA7bgOYM5czT3BwTdTRoCg50Ag-ljWbxG5n?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

* **Điều kiện mục kiểm:** kiểm tra số lượng các mục kiểm đã được hoàn thành hay chưa hoàn thành. Nếu số lượng đó đáp ứng yêu cầu mà người dùng đưa ra thì cho phép chuyển trạng thái. Các điều kiện có thể cài đặt bao gồm:&#x20;
* **Trạng thái ngay trước:** yêu cầu số lượng các mục kiểm ở trạng thái ngay trước trạng thái được cài đặt phải được hoàn thành đúng với số lượng người dùng yêu cầu mới cho phép chuyển trạng thái

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXenddUwNgaFyYdKCWq0vrH3uRNkFqV_t1gdEaOmGs_TbBbUmvmp_WeLa0JCo5CJ1H1xcTfRt4QdisFfmmt7spWN0o38EAe8A8jZzTvY0yh5yAAzMBQxmw0Qtm5xcrwNjSS9Jlbu1CPnREK9t38EyNyU_98f?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

* **Tất cả các trạng thái trước:** yêu cầu số lượng các mục kiểm ở tất cả các trạng thái trước đó đều phải đạt số lượng hoàn thành đúng với yêu cầu của người dùng mới cho phép chuyển trạng thái

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXdy7uwyiUd1W6TNPcs_hmxuRey7jr9BsB59TgG8qSU7-c583uDfKtkxCJDfNxCVAbkU_-QcAiGsJKLGMqEcBiL4VUtqrVbVVZ6Ie9YvHEPVj9jmZE4cUqkWPgMzntseVbuQTW08Pi6EwH5QuI7J0AeA8CjA?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

Về các cách đưa ra số lượng mục kiểm hoàn thành hay không hoàn thành sẽ dựa vào cách cấu hình người dùng bao gồm:

* **Tất cả các mục kiểm hoàn thành:** yêu cầu tất cả các mục kiểm phải được hoàn thành mới cho phép chuyển trạng thái
* **Cài đặt nâng cao:** người dùng có thể đưa ra các yêu cầu để tính toán số lượng của mục kiểm cần hoàn thành thông qua việc cài đặt các yếu tố bao gồm:&#x20;
* Trạng thái mục kiểm

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXcnnmXih6TEG25-SUhJ6I9MilpPPKjB53SYK1uvHs2fpBImjvRwr_HwJs80qcgdwIDdZ2HhmsEyspMwqtFaJvMVQWh8VK64x5v4EA9G8h46EydUsnxGgfh9e2qA2St3E8W2qnIBDRl0v9WDRpA2Ijk72dA?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

* Các so sánh&#x20;

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXf1HgV_7md7ZGF2nMtMrnSpZ0wJZUBuo1bBt7gyIFcPgvJ7iqZXlenmv2EerSliXvJnqO0jOGTMsY3jZJQAi_Vr0H5GW_fAvzF3msEjr0BE8LoAXhRYHEgRKp-iev3-DMWWNogZ3oi7FU7HxdMIcuWQGKz6?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

\


* Số lượng

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXdIikDXOxpiQSsBF36yuWYRKIwAsPVVGM0TeE-I6m8uD1LBWhrMaG4zkBYXPMptu3Qy-KUcFxwaKvTtsmgraM_ZEDwrmtvUoApIbFDP2bqNjtxxjgmpZEhkWn597TJbkpb3NYnmQShyizw0z7xI1v_6lwgj?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

\


* Đơn vị tính

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXeGIkckhqgZrmomWOE6O13jSE8GGpX-ScvWBqYrN_h9O3seZGYYUdsMvzOUixsmD3iNGwGfmTrSDnDanUiJAeBqd_nsan93s5H9bk3NqTcksDnPukgNPxKC9Nm9wOTZF-T8M7Kim64nCFhyelvWJsrt0Ifc?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

Như ví dụ ở như hình dưới, số lượng các mục kiểm ở tất cả các trạng thái trước đều phải hoàn thành 100% thì mới cho phép chuyển trạng thái&#x20;

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXec5wjKL3gGRMCfGr7Qy8oJxu0JM6mMZj_KdcebTmDcFXROP15LptnIxvmmEUxERMF7S4XiTzVUeRvEWoZrHO9MKohETFWkrWIloPJpsho2efJkBCB_wirRzAs5SncaqUJm4dSHMDdIC_nCONAgINj19yzg?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

\


* **Điều kiện mục việc con:** Kiểm tra số lượng mục việc con đáp ứng được các điều kiện mà người dùng đạt ra. Nếu số lượng đúng với yêu cầu của người dùng thì cho phép chuyển trạng thái. Các điều kiện người dùng có thể cài đặt bao gồm:&#x20;
* **Trạng thái ngay trước:** yêu cầu các mục con của trạng thái ngay trước phải đáp ứng các điều kiện mà người dùng đưa ra và số lượng phải đạt yêu cầu của người dùng thì mới cho phép chuyển trạng thái
* **Tất cả các trạng thái trước:** yêu cầu mục con ở tất cả các trạng thái trước phải đáp ứng các điều kiện mà người dùng đưa ra và số lượng phải đạt yêu cầu của người dùng thì mới cho phép chuyển trạng thái



Về các cách đưa ra số lượng mục con đáp ứng yêu cầu sẽ dựa vào cách cấu hình của người dùng bao gồm:

* **Tất cả mục con:** tất cả các mục con phải đáp ứng yêu cầu đặt ra thì mới cho phép chuyển trạng thái.
* **Cài đặt nâng cao:** người dùng có thể cài đặt các yêu cầu để hệ thống lọc ra mục con. Nếu số lượng mục con đạt với yêu cầu về số lượng của người dùng đưa ra thì cho phép chuyển trạng thái. Các yêu cầu của người dùng về mục con sẽ được thể hiện thành các yếu tố trong tiêu chí lọc.&#x20;

&#x20;hoạt động giống với bộ lọc issue bình thường, người dùng sẽ đưa ra các tiêu chí và hệ thống sẽ dựa vào các tiêu chí đó để lọc ra các issue thỏa mãn

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXcwKk3qc6TgoyRVu-Q_Pbynsh8lPF74iPO0vCEjpSzAKsBauR63aPAxGjJsoec8HeJ1_KId160BD6i5uWUDzPYj1AFbD19_BHvYLg6X0ZZiQT6x349OFMcmhTVFIYOUKYg5SAcZ1uvQmqW_rE1rl9Fu-zI?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

Để có thể đưa ra yêu cầu về số lượng các loại mục con, người dùng cấu hình tại phần “Số mục lọc” bao gồm các yếu tố:&#x20;

* Cách so sánh&#x20;
* Số lượng
* Đơn vị

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXdHT0v9o-FwZl3PTo8Vz87a3QvaRIhEGI9fRuy1wuTX840fUV8G7XMNFswGybyrvlcdXfiNpeMRDk8NN5-NSuoAhf46WruN-7S29XOKxRh37FX0ear__LJUWdp18IzWo1qAy1tx_7Lxefu7nhVY5AHOFsc?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

Kết hợp 2 thành phần “Tiêu chí lọc” và “Số mục lọc” ở trên, điều kiện mà người dùng cài đặt ở đây có thể hiểu là mục con phải đáp ứng các yêu cầu: đang ở trạng thái hoàn thành, trường Số lượng theo chứng từ có giá trị lớn hơn 100, Hình thức làm việc là Fulltime, Người kiểm tra là Huy nguyễn và Hộp kiểm đơn đã được đánh dấu. Nếu số lượng mục con đạt đầy đủ các điều kiện đó thì sẽ cho phép chuyển trạng thái.&#x20;



* **Điều kiện mục kết nối:** Kiểm tra các mục kết nối có loại kết nối đã được người dùng lựa chọn và đạt các điều kiện người dùng đưa ra. Nếu các mục kết nối thỏa mãn các điều kiện và số lượng đặt ra của người dùng sẽ cho phép chuyển trạng thái. Các điều kiện người dùng có thể đặt ra bao gồm:&#x20;
* **Tất cả các mục kết nối:** tất cả các mục kết nối phải đáp ứng điều kiện mới được chuyển trạng thái.
* **Cài đặt nâng cao:** người dùng có thể cài đặt các yêu cầu lọc ra mục kết nối. Nếu số lượng các mục kết nối đạt yêu cầu về số lượng của người dùng đưa ra thì cho phép chuyển trạng thái. Các yêu cầu của người dùng về mục kết nối sẽ được thể hiện thành các yếu tố trong tiêu chí lọc.  &#x20;

Tiêu chí lọc hoạt động giống với bộ lọc issue bình thường, người dùng sẽ đưa ra các tiêu chí và hệ thống sẽ dựa vào các tiêu chí đó để lọc ra các issue thỏa mãn

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXcHkZESTsntuIuSxKk1s4YK68HD-ThAGyyP9ZYtFNBfwEpn3t_li_BOj1sl8rf9I0bYVFr0nncBzIHxtw3wOxUdGgXn_iHeXjtfxfPd3Na5DhMI6vHXpl5HvVpVwIXUr7QnCw8JQKxJTsrbvNKBSr0UfieD?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

Để có thể đưa ra yêu cầu về số lượng các loại mục kết nối, người dùng cấu hình tại phần Số mục lọc bao gồm các yếu tố:&#x20;

* Cách so sánh&#x20;
* Số lượng
* Đơn vị

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXdMtFwqJ0xOrViRURvEmP9Qu6qAshZEeFjeOBRUpFOytV8h91156DwF3IBKsy8xWAG5jInN8Bza9TjSO5a-6ZXS0ZUIUaqILq-XO3HK-CdZyVEtIk8pX2cxtG4mw71YJYIhTzZjOfS1-Unsb5pwssHWD9Lu?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

Kết hợp 2 thành phần Tiêu chí lọc và Số mục lọc ở trên, điều kiện mà người dùng cài đặt ở đây có thể hiểu là các mục liên kết phải đáp ứng các yêu cầu: đang ở trạng thái thuộc nhóm hoàn thành, các trường dữ liệu Người đề xuất, Sản phẩm không được để trống và các trường dữ liệu Số lượng đặt, Đơn giá, Thành tiền phải lớn hơn 0. Nếu số lượng các mục liên kết đạt đủ các yêu cầu trên đạt 50% tổng số lượng thì hệ thống sẽ cho phép chuyển trạng thái.



#### Bước 3.2: cài đặt Nhập liệu:

* Cập nhật trường: Người dùng cài đặt những trường dữ liệu muốn điền hay cần cập nhật ở trạng thái nhất định thì khi chuyển trạng thái, màn hình sẽ hiển thị lên các trường dữ liệu đó.&#x20;

Ví dụ như ở Trạng thái Kiểm tra, người dùng cần nhập liệu hay cập nhật các trường dữ liệu như Người kiểm tra, Số lượng đạt, Số lượng không đạt. Để làm được điều này, người dùng nhấn chọn trạng thái Kiểm tra trên workflow và cấu hình phần Nhập liệu. Sau đó thực hiện các bước như hình dưới để đến khi chuyển trạng thái sang Kiểm tra, hệ thống sẽ hiển thị màn hình trạng thái Kiểm tra gồm các trường dữ liệu đã được người dùng lựa chọn để nhập liệu hay cập nhật.&#x20;

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXeScayFG54DjrNWbYD4nu5XluKn492cc4wiw91xTBEJzWOceyiuc8Vm2odjVnnrpnsGyHJv0-YorUPPbsa44awnUtvMd316ML-JUwUULwjEwHoW5E4k9Jv-FP8IDoHIB_p4QbB6UJeWxCaRKzfcmPVHPKKM?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

\


* **Thêm kết nối:** Đưa ra một danh sách các issue đã được chọn lọc dựa trên các điều kiện mà người dùng đã cài đặt bao gồm:
* **Loại mục nguồn:** đưa ra các loại mục hiện đang nằm trong chức năng đang cấu hình và qua đó cũng lọc ra các loại liên kết có thể tạo ra từ mục nguồn đã chọn.
* **Loại kết nối:** có thể được hiểu là kiểm kết nối, là cách thức mà loại mục nguồn kết nối đến các mục khác.
* **Tiêu chí lọc:** Tiêu chí lọc sẽ hỗ trợ người dùng có thể sàng lọc kỹ hơn các issue có thể kết nối.&#x20;

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXcm8z7LfYN2SKusFV7F3zBuxTo3QD5BEmLgRg3NkHXpcOiKzLELJDTPA7N3nE3q0450oifPZNHAo8M1vJaebtHCB6G44a33T0jc_EAaM2el2SRJL38WIdkCXv7zXbB795jAdMxrKmjF85syoXzLgZ4PdloC?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

Như ví dụ dưới đây, sau khi đã cài đặt các yêu cầu tại phần nhập liệu của trạng thái Kiểm tra phê duyệt, khi chuyển sang trạng thái này, màn hình nhập liệu sẽ xuất hiện và hiển thị các issue có loại có thể được kết nối từ lại mục nguồn là Task với loại kết nối là Đề xuất.

#### Bước 3.3: cài đặt Tự động:

**Trường dữ liệu:** Thêm các trường dữ liệu mà người dùng muốn hệ thống thực hiện tự động theo yêu cầu đã được cài đặt trước đó

* **Trường người**: Tự động điền trường dữ liệu người mà người dùng đã cài đặt dựa trên tập hợp người đã được lựa chọn trước đó tùy theo Điều chỉnh theo tiêu chí nào và Cách chia ra sao. Các cách chia bao gồm:&#x20;
* **Chọn ngẫu nhiên:** Chọn ra ngẫu nhiên 1 người trong tập hợp người mà người dùng chọn ra để tự động điền vào
* Chọn theo vòng tròn
* Chọn người ít mục nhất

Các cách điều chỉnh bao gồm:&#x20;

* Điều chỉnh theo mục kích hoạt hành động: chọn một người từ mục/mảng việc/tổ chức của mục chuyển trạng thái được người dùng lựa chọn từ trước để điền vào trường dữ liệu được cấu hình theo Cách chia đã được chọn.

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXfHpbUHCtvUGyK7KO1D-Kvrp-UB-yV1h3nfkZxBT5pCV5aMCb_f8SXlUV7lwq8-u0n18gahi34PXS-s_XEh6uaKpuFiTMWYuO41pP8fpj2HBCAVIcDcrsMCGyCeAArxTpUWSMcJb4WdSSBmw3BDNlLM1D-4?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

* Điều chỉnh theo mục cha: lấy một trong những trường người từ mục cha/mảng việc/tổ chức của mục chuyển trạng thái được người dùng lựa chọn từ trước để điền vào trường dữ liệu được cấu hình theo Cách chia đã được chọn.

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXfhTAFL5lu3kXlOd5UnpZ0DgYEFj3UYQX_9jegRMKC52PRdj9e1kowIeWUgeNrUCvw49UfoziT2jU6uop5Yh1BP-Ub_chNGs8wPFEabRx3KS5qI3q29czrLP3YfkM-7I7ByJggiCBGFrOHx1uXlQY-H6-Gc?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

* Điều chỉnh theo mục hiện tại
* Điều chỉnh theo mục đích đến
* Trường ngày: Tự động điền trường dữ liệu ngày mà người dùng đã cài đặt dựa vào Điều chỉnh theo tiêu chí. Các Tiêu chí bao gồm:&#x20;
* Đặt giá trị cụ thể: lựa chọn một ngày cụ thể để điền vào trường dữ liệu

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXeP5SIz84mXSAXF965WJ6l5QvJLs524j773zysyYcJmOrRQRtbisnzcoP0JUoMIub4TlzgKIuArnjOAP-6BEa4gvW6KvMBI69lwcaL25HYvZVSbaQFcBLlUtB2c2zUMPR3Z081QwKXr5ETW_xg62EGFtp4?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

* Điều chỉnh theo điều kiện: Lấy mốc thời gian thực hiện hành động, cộng/trừ số ngày lựa chọn để đưa ra gán giá trị ngày cho trường

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXcjrJsAEYiXpl8FB-tdxk-IL74_NSc_9SMGbCKN3PoJSX_LVn0F7AfkY0QFLuz1Ku8i8ImFsNKp9ZF1R7ChKXJCYYyoGljL-HYY8iRn7gaTDbtdAktpmdPi55Rd8SvGvrcNpArDM0TVx6YpRiRxeLT-z6DT?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

* Điều chỉnh theo mục đích kích hoạt hành động: Lấy Trường Nguồn làm mốc, khi trường nguồn thay đổi sẽ cộng/ trừ số thời gian đã nhập để gán giá trị cho trường

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXeBkb6q-crrrxcdc0Ms4MpIWX7DKu29JEMJmeCtkAiKd91dz6MvOizrlLUH84AKKzDCIFZbyPdNeAD6q1wZpNkW6Fk4FtdH3ONiy-PoWldZ6dNVtnE8xRZQ8jPydLh4noh_CDe7N4dsF13hxs1HjND60iaW?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

* Điều chỉnh theo mục cha: Lấy Trường Nguồn từ mục cha làm mốc, cộng/ trừ số thời gian đã nhập để gán giá trị cho trường

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXeiBoMvhT80bf0LZ3CcKQFeE7L2qxfuYVvpZDH18xuxlgjuPpS3yf5GZC8Zewrn3mA6KPRS4_XOD4G357-hyPRoQVPM8hIvgRjleuirdlJoDeRsjoTxGpl7taHiusVOdaILTp_mBNIp6RlGTC3jcVeYW_yH?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

* Điều chỉnh theo thời điểm kích hoạt hành động: Lấy mốc là thời gian thực hiện hành động, cộng trừ số thời gian đã nhập để gán giá trị cho trường

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXdJPZ6tH1yzEe2UfS4dH6Qqmhdz2MXu_UuMojDeETRqmX9BLzhpXi4R8wdA5AB1Gsi4q-TKHarIe-yYYfMpxgoew7hR1BY6QoRs-ReRlEilz5mJxiNUkYC1jz_wCfWeZdMwqWRAqXWe9J82xZZleoqpGtsc?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

* Điều chỉnh theo mục hiện tại
* Điều chỉnh theo mục đích đến

\* _Nếu mục Bỏ qua ngày chọn Chủ nhật hay Thứ 7 & Chủ nhật thì nếu ngày lựa chọn đúng vào Chủ nhật hay Thứ 7 và Chủ nhật thì hệ thống sẽ tự động bỏ qua những ngày đó và chọn ngày kế tiếp để điển vào trường dữ liệu người dùng đã cài đặt_

* **Trường số:** Tự động điền trường dữ liệu số số liệu cố định, bằng dữ liệu từ một trường dữ liệu dạng số khác hoặc bằng phép tính của nhiều trường dữ liệu dạng số với nhau (các trường dữ liệu được chọn phải thuộc mục đang cấu hình)

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXej5Y6HFeK3vN9JK0F0hR3ye27xEY5RaD5fLxrh2ps_pTGaaH7T0_whj9wjUjQHHeoKt0qWR05IosCepuBGCfywN4IwNGMPGi54aCj49XRYWsZd9CvK-ayuQGwQYVfC46M3hl03KkZ38G-lhbzYMeDz8mc?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

* **Trường chữ:** Lựa chọn 1 chuỗi văn bản cụ thể để điền vào trường giá trị hoặc có thể kết hợp chuỗi văn bản tự nhập và giá trị của các trường dữ liệu khác với nhau để điền vào trường giá trị đang cấu hình (các trường giá trị được lựa chọn phải thuộc mục đang cấu hình)

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXfsXQjvzj-lZbLTGVUcR9t7h5EA5QMGQO9qcV3TseEZ3AdpXTkRLgNZRQh5PwvVndO_ImIOiYWaGFHqnkEFOuRrOWoGxDzh9DAjcA-u1h1bwm2MMJXzu4jnIaC3tDspS131gSXCWfG_mAdXUSFe-WnKoMTZ?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

* **Thêm liên kết:** Tự động thêm các mục liên kết đáp ứng đầy đủ các tiêu chí mà người dùng cài đặt vào mục khi chuyển đến trạng thái được cấu hình. Các tiêu chí báo gồm:
* **Chọn giá trị cụ thể:** chọn ra các issue cụ thể, đã tồn tại trên hệ thống trong danh sách các issue được lọc ra từ các điều kiện về Loại lục nguồn và Loại kết nối để liên kết&#x20;

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXfRaatqzgI3um6qluJK1CVTmurrKc-QzYJaY79KNiiHLhilKLr2GOl0Mf2UweyZfw6M5ovFQuZKSWd-gp3bmKYMpbdLAsYhahM2Oa807GWRw68PuzKnraZ1A9rQWOeFagqZogRG-6j8vyWT-BKGiq9mPVs3?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

* **Dùng bộ lọc:** người dùng đưa ra các điều kiện về Loại mục nguồn, Loại kết nối và các Tiêu chí lọc, hệ thống sẽ dựa vào đó liên kết tất cả các issue vào issue thuộc loại mục đang được cấu hình

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXcNStpSyF0EuJguPrsAf8vwLDHC0T4dyeXifWu8PpT54WsPkZK0l2lVs1l7r71fTK_tzafAxpHi3GtKfwkNOF0dKraqdiArEaXmHx7Qa4bxkXoEScr2QCRgO5YoDotFWKU1M4HATHI9LK6vvEnuFsFYngl7?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

* **Sao chép:** dựa vào nguồn mà người dùng muốn sao chép và điều kiện “Sao chép từ” để sao chép toàn bộ các issue mà mục nguồn liên kết để kết nối đến issue thuộc loại mục đang cấu hình. Các điều kiện Sao chép từ bao gồm:&#x20;
* **Mục cha:** sao chép toàn bộ các issue đã liên kết với issue cha để liên kết với issue thuộc loại mục đang cấu hình (issue con)

![](https://lh7-us.googleusercontent.com/docsz/AD_4nXdeR-a2Oca7mGrYG8OeSSsHTHiDRsh_THnoSguyMW6w5LrAvyXkiOyCoLMBOEnJ0nrgRwh0I7rkTr-HIJu0RAibG6SNTBbGxRpnz_4fFZJ9KNg3wn_oPSq7nhR7R3ta-mZzawBam-ffQ8c40uIKO7FC1lpl?key=Pj5SQn1IP1YRt0MtCTTbqw)

* Mục kích hoạt hành động
* Mục hiện tại
* Mục đích đến
* **Xóa kết nối:** người dùng đưa ra các điều kiện về Loại mục nguồn, Loại kết nối và các Tiêu chí lọc, hệ thống sẽ dựa vào đó xóa tất cả các liên kết đạt yêu cầu

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXfIO6EgM8hT2uyjwZ-3j62BqXhS0My9tdRqMJdlCNgi9Y2QhUhNlWJzTnIFez27nDuNJEjsmrpM9m-tfTtrMXcnPR515AkVitaV51AE_MbjYrq6TkPq-8dibzhSnn7gBszOw2DSqFawO8jvwIw7lFdKKQU?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

**Tạo mục:** Tự động tạo các mục mới khi chuyển đến trạng thái đang cấu hình dựa vào các điều kiện mà người dùng đặt ra bao gồm:&#x20;

Thông tin cơ bản:&#x20;

* **Mảng việc:** mảng việc mà người dùng muốn tạo mục&#x20;
* **Loại mục:** lựa chọn loại mục mà người dùng muốn tạo. Loại mục phải thuộc mảng việc mà người dùng đã chọn ở trên
* **Tiêu đề:** tiêu đề của issue được tạo mới
* **Mô tả:** mô tả của issue được tạo mới

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXdRcDpAX7-wgRXXhE878BDMVDNKKUJiUq8gVaIoFODwFXKdpsl-qJjbELj3N8Y1okp13c4tSdJbgPPlxThH9pgYgFOb0QgzePvI519_qDnbYg5a5t7ECJnUSopW6EsqoMgo68sDZWjYc15b_G_ePAJDBBs1?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

**Thông tin nâng cao:**&#x20;

* Tự động thêm dữ liệu vào các trường dữ liệu có trong màn hình của mục được tạo tự động tương tự với phần Trường dữ liệu đã viết ở Bước 3.3: Cài đặt tự động
* Tự động thêm các mục liên kết tương tự với phần Thêm liên kết đã viết ở Bước 3.3: Cài đặt tự động

**Bước 4:** Cài đặt Đầu việc:&#x20;

* **Mục kiểm:** người dùng có thể tạo sẵn các mục kiểm cho từng trạng thái để khi chuyển đến những trạng thái đó, các mục kiểm sẽ tự động hiển thị lên màn hình mục việc.
* **Mục việc con:** hệ thống sẽ tạo các mục con của mục đang cấu hình. Người dùng có thể cài đặt Thông tin cơ bản, Thông tin nâng cao và Điều kiện của mục con được tạo
* **Thông tin cơ bản:**&#x20;

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXeWS9nGeZm7jm08dDGsOdommDYtPki0yGTADe1L2_XjnqQsfniW14bpfza5RvGEfpLTVmTrYyCmmSl5X1CQH51WY4nssQqhkhldll-d5qsXrXI-8uDYtyvsR7fdwHwXSfpVBNs897oQI2rwHYBBoOMv-eM?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

**Thông tin nâng cao:**&#x20;

* Tự động thêm thông tin vào các trường dữ liệu có trong màn hình của mục con được tạo tự động tương tự với phần Trường dữ liệu đã viết ở Bước 3.3: Cài đặt tự động

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXcAkJXn6x9VmESy16G4h9rrk552N8V7jCFCOM7gg9alUa17j_hvjTINUoC2bgctDQBNTGklw3TAn6lBtisF7kRQ6mQP6xVS18lIiB3kXFksmrYrBD2BfTu5C7fSI28zFUQ_guXbBF-Rv8PYxPEUr7xQVPdA?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

* Tự động thêm các mục liên kết tương tự với phần Thêm liên kết đã viết ở Bước 3.3: Cài đặt tự động

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXeohCXQ8Ot54MEvce9Xu1eyhe-WJ0hHiCOK3QLubYgVlfn6OdXmmz9impNB-9FedY-KcEOPILpzC4F4l4-lbeL0uMEiLh7ivGbV-CQzYtNJkIncnzF0U7VLSA4iaGHra1iAnnLftA2IJnGlxRBYI3H5jBW-?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

* **Điều kiện:** người dùng đưa ra các điều kiện về Điều kiện dữ liệu, Mục kiểm, Mục con, Loại kết nối. Nếu khi chuyển trạng thái, issue đáp ứng đầy đủ các điều người dùng đưa ra, hệ thống sẽ cho phép chuyển trạng thái.&#x20;

\
\


<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXf57PsRoaDRD1CTLThWWCATHfgFYCyB9pJG8_CMVR4sBVv0-z6zTdmrQjMAPEprxrXV0jeqZFnBYnyfc2gKrBIdeMNuuPQXic2aQ-pLueJo9alqGT2r5EvdeVQAeVgwZf8PXXV9MqQgBiNvaSCCJ0nQ830?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

\
\
\
\
\
\
\


### Workflow 3: Advance - Nâng cao (sắp ra mắt)

1, Mục đích sử dụng, tính ứng dụng

2, Các thuật ngữ liên quan

3, Giao diện màn hình, HDSD

4, Ví dụ thực tế

\
\
\
\
\
\
\
\
\
\
