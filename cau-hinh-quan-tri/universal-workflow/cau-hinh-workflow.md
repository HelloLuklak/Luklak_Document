# Cấu hình workflow

<figure><img src="../../.gitbook/assets/image (497).png" alt=""><figcaption></figcaption></figure>

### HƯỚNG DẪN SỬ DỤNG CHI TIẾT CÁC LOẠI WORKFLOW TRÊN LUKLAK

### Workflow loại 1: Cơ bản-basic (bộ cũ vẫn dùng)

#### **1, Ví dụ thực tế**

VD1: Quy trình “Xử lý Khách hàng mới” và “Chốt Giao dịch”

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXesePM_M_UDkckJz10y5PT4hwSjwjoM5W8gbVBMLKtexE0QGTVPoUmzvUjI5ApdxQGvtOjCY79aKhQMPl6YikT-X1xbkxefu6a3pkmfOCaZBFOfxMcqxyd2BjGAhEW2ZoQooNNJ10QmhbCbVWLCkYPf5PXs?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

Dưới đây là một ví dụ cụ thể về tiến trình tư vấn bán hàng thường gọi là tiến trình deal trong một đơn vị kinh doanh. (Đây là tiến trình gồm các bước cơ bản - Tiến trình này có thể thay đổi tùy vào đặc thù kinh doanh của từng đơn vị)\


**Trạng thái ban đầu:** Khách hàng mới

* **Khách hàng mới:** là nơi nhập các thông tin khách hàng đăng ký với doanh nghiệp hoặc tạo lên từ các nguồn như website hoặc qua các kênh khác.

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

Bước thứ 6: **Thành công Hợp đồng** chính thức và Chốt giao dịch- “Thành công” hoặc “Thất bại”

* Tiến hành lên hợp đồng chính thức với các điều khoản cụ thể và chi tiết hơn.
* Khi hợp đồng được ký kết và chốt, giao dịch được coi là thành công.

Trường hợp khách hàng không phù hợp, công ty vẫn lưu trữ thông tin khách hàng Deal được gọi là “Thất bại”

Vậy với Quy trình Xử lý Khách hàng mới và Chốt Giao dịch trên, chúng ta có thể mô tả bằng workflow trên phần mềm Luklak như sau:&#x20;

* Khi mô tả quy trình làm việc này lên Luklak, chúng ta thấy rõ rằng quy trình này đường đi nước bước như thế nào, các bước cần làm khi đến giai đoạn tiếp theo. Với 1 quy trình này, người làm dù đang ở giai đoạn nào cũng định hướng được công việc của mình cần phải làm.&#x20;
* Workflow bán hàng được mô tả rõ, giúp giảm thiểu lỗi phát sinh trong quy trình bán hàng, tạo ra kết quả chính xác và đáng tin cậy hơn. Một workflow bán hàng hiệu quả không chỉ tăng cường trải nghiệm cho khách hàng mà còn tối ưu hóa quy trình làm việc nội bộ và cung cấp thông tin cần thiết để định hình chiến lược kinh doanh.
* Vậy chúng ta hãy cùng xem workflow này được thiết lập như thế nào trên Luklak khi tham khảo phần 2 các thuật ngữ liên quan và phần 3 hướng dẫn sử dụng phần mềm sau.



#### **2, Các thuật ngữ liên quan**

Màn hình tạo mục việc sẽ gồm các phần:

* **Space (mảng việc):** chọn xem mục việc cần nằm ở chỗ nào trong cơ cấu bộ phận, phòng ban.&#x20;
* **Issue type (loại mục):** trong mỗi space có thể có các loại việc khác nhau tương ứng với các chức năng và quy trình làm việc khác nhau đã được định nghĩa trước. Khi tạo thì cần chọn đúng loại việc cần làm.
* **Issue title (tiêu đề):** nhập tên công việc
* **Custom field (trường dữ liệu):** là các trường dữ liệu, thông tin cụ thể cần có, phục vụ cho công việc đó.

Các thuật ngữ khác

* **Workflow (tiến trình):** thể hiện các trạng thái công việc khác nhau (status) và các bước chuyển (transition) quy định đường đi từ trạng thái này sang trạng thái khác.Mỗi loại việc (issue) sẽ có một quy trình, quy chuẩn làm việc tương ứng. Workflow của Luklak với Status và Transition dùng để tạo một quy trình trực quan, bao gồm các trạng thái và các bước chuyển.
* **Status (Trạng thái):** thể hiện trạng thái công việc đó đang ở giai đoạn nào.\

* **Transition (Bước chuyển):** là các hành động để kết nối, chuyển công việc đó từ trạng thái này sang trạng thái khác.
* **Phòng làm việc:** [Tại đây](https://docs.google.com/document/d/1sBbgwc9MC7OluZyWQPRcW3jsPf0ZMM87U1vYSKGP9C4/edit?usp=sharing)
* **Bộ lọc:** [Tại đây](https://docs.google.com/document/d/16NsV6c-i9voxoNHueyzA-kLc4x-JeAqWtBPB2qvOMGQ/edit?usp=sharing)
* **Báo cáo:** [Tại đây](https://docs.google.com/document/d/1Yp3UOH8xpG2Rvr-7I0eX3t-H3pO5B2JlLjA4vLYu2cQ/edit?usp=sharing)

#### 3, Giao diện màn hình, HDSD

Ví dụ dưới đây về một đầu việc "xin nghỉ phép", với workflow được thiết kế theo quy trình xin nghỉ. Nhân sự khi xin nghỉ phép thì mọi thông tin hiển thị trên màn hình và tiến trình sẽ chạy giống nhau như sau:

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXdsPfwihDvb3jMNtZDW0InX5s3zb2cjUgVjq8bOzLbYdhekOI2dS4q1udzRM1Dv7gu3pLcbO09j0D7x7wQ-eu38SJzWra_T3YZRFnZxO7vwchUBS_h4ry-jMaAkM34PYILJntYFjGFp5vXZ8d743jLj28FN?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

Màn hình mục việc xin nghỉ

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXdh_ZsoOiPkk7O-V_FbMU2d-SOejoEO3vSVTwKV_aDc1n8tQ-G8HVUPOsqSCjIrDjLmdGrZ8pAJI6KsrU9Pfi13Yyi6XqY3XRVbbLksNl7hYUeCBeS3JP-k3UV3VC-221tQlNhtcZPmqYtrX2jYIgdfELmJ?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

**Tiến trình xin nghỉ**

Màn hình của mục việc xin nghỉ hiển thị đầy đủ các thông tin liên quan để người phê duyệt có thể nắm bắt và thực hiện phê duyệt cho nhân viên. Thông tin được cập nhật để người làm đơn biết rằng đơn của mình đã được chấp nhận hay chưa. Thông tin lưu lại trên hệ thống để những người liên quan ví dụ như bộ phận nhân sự nắm bắt được và dễ dàng thống kê được nhân viên trong tháng đã nghỉ bao nhiêu ngày, tổng số ngày nghỉ theo từng loại nghỉ là bao nhiêu.

Hoặc tiến trình bán hàng cho một khách hàng, đã nêu ở ví dụ trước. Workflow như này sẽ có những giá trị sử dụng như sau:&#x20;

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXdxRMybKrsNssU2DIKa6pd8Yi6EO5Mi6Whg51_PqnkIP1CmVJ0cfUN-hwLRRvpl27evdvr9N00MjWQFBP58MuJwW-aGEwtH4r3ZSIpDc9UfySWAr9xvBk4iclwpKNscR8LGkqeo_QmoIyN9VsO6h2nLH62d?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

* Thể hiện trực quan, rõ ràng các bước trong tiến trình, giúp nhân sự nhìn vào hiểu được đường đi nước bước, cách làm của công việc.
* Khi thực tế làm việc thì cũng báo cáo, hành động trên tiến trình đó, làm đến đâu chuyển trạng thái đến đó để cả mình hoặc quản lý, người liên quan nắm được công việc đang ở đâu, như thế nào
* Các trạng thái này sẽ được đưa vào Bộ Lọc & Báo Cáo (Filter & Dashboard) để tổng hợp, phân tích, nắm bắt tổng thể tình hình công việc.

Bên trên là những tính năng đã có sẵn dùng được ngay với Tiến Trình (Workflow), hiện tại Luklak đang phát triển thêm những tính năng tiếp theo như:

* Tự động chuyển người làm (Assignee) sang người khác thi thay đổi Trạng Thái (Status) trong Tiến Trình.
* Các chức năng Automation, khi có sự thay đổi nào đó trong Workflow thì sẽ tự định nghĩa được các hành động phát sinh tiếp theo như nào.

\=>Những tính năng này sẽ được dùng ở loại tiến trình Workflow loại 2: standard - tiêu chuẩn, Workflow loại 3: advance - nâng cao



#### **3, Các thao tác cần làm với một Workflow sẽ bao gồm:**

A, Tạo tiến trình:

Chi tiết hướng dẫn: [Tại đây](https://docs.google.com/document/d/1bJc3HOJtZvGE7puDINU7KbNSVyHXO2fk/edit#heading=h.4d34og8)



B. Chuyển trạng thái/ tiến trình

* **Mỗi mục việc (issue)** được tạo từ một issue type nhất định đều có tiến trình & các trạng thái (workflow & status) của nó, thể hiện rõ quy chuẩn công việc đó sẽ có những bước như nào.&#x20;
* **Người làm (assignee)**, người giám sát cần chuyển trạng thái phản ánh đúng tình hình công việc, ví dụ như chưa làm, đang làm, đã xong, đóng huỷ…
* Chuyển đúng trạng thái giúp chính cá nhân đó tổng hợp được tình hình công việc, nắm bắt được những đầu việc mình đang làm cùng lúc như nào, để sắp xếp và lên kế hoạch công việc phù hợp hơn. Bên cạnh đó, điều này cũng giúp cấp trên và người liên quan dễ nắm bắt tình hình và phối hợp, tương tác.

Ngoài nút chuyển trạng thái ở trên cùng tương tự như tất cả các app khác, thì luklak là bên duy nhất đẩy mạnh trải nghiệm người dùng bằng cách đẩy luôn các trạng thái vào ngay trên ô chat trao đổi về đầu việc. việc này có giá trị:

* **Nâng cao nhận thức** của người dùng, lúc nào cũng biết công việc đang ở trạng thái nào, vì thường xuyên chat trao đổi.
* Thúc đẩy cập nhật chuyển trạng thái **đúng tiến trình**, vì đang chat thì có thể click chuyển trạng thái ngay được, rất tiện.

\


<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXdY-tppANu8E9RHipx6P4Evud0ZIfCt-INiMUA8QVBCo6wOiJoTpe4TPpftOIEu2x9SDXFI_FJJ2OGNRNqRWRRe57moOvFZYAgTVa3Ei-lsqlkbUv9UOiBD1PA_TC7hiQk2ZhatZP2o3oSJZnboiVQil4yW?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

C, Xem báo cáo theo status

Người dùng hoàn toàn có thể xem báo cáo danh sách các mục việc theo nhóm status hoặc theo status dạng Kanban, để có cái nhìn về bức tranh công việc một cách tổng thể.

* Kanban theo nhóm status:

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXcuDo8-vWW8z0QpRzab1reWx6mU2ZqfNuI-cMB2RzjJR4o8xy8wneN0q97H9BzYUhLSlChZ_6-BIlne6DvO0Lf-k85Imhg86SLDNT4ZKl_OHRkAWRELNMU6AZsoFMy4plsbrCrmvIq_IwzL4ERnXOc3bWSK?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

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

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXehqF0UyOlo5QO_qyyAYeW_G-fk6ACf0vx281qBQ0NFXoZb0eBy7shZUzH9i29MnlMgee3GlbRg7pMmMhV4NgGh8_c54UgspWI35J16BW3VghN6qLw_UG4Igysh84WF_lHY4C6x6ImkT-7zKoMWno41vPc?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

Với tính năng này, người dùng có thể nắm bắt được các đầu công việc đang đến giai đoạn nào, có bao nhiêu công việc cần làm, đang làm và đã xong. Ngoài ra, người dùng hoàn toàn có thể xem chi tiết mục việc bằng cách click vào ngay mục việc đó và cập nhật trạng thái của tiến trình bằng cách kéo thả các mục việc từ cột này sang cột kia của Kanban mà không cần vào hẳn mục việc để thay đổi.





D, Tạo bộ lọc theo Status

Người dùng cũng có thể dùng bộ lọc theo dạng status (trạng thái) để thống kê danh sách công việc theo trạng thái, ví dụ xem những công việc nào đã hoàn thành, công việc nào đang làm, tạm hoãn… hoặc các công việc lọc theo từng trạng thái người dùng đã thiết lập trên workflow.

Người dùng có thể lọc theo status hoặc nhóm status thông thường. Để thao tác nhanh, có thể dùng ngay thanh công cụ lọc tiêu chuẩn ở màn hình giao diện danh sách mục việc.,,k,,,

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXcDH5L89GqliB17NJK7iXvPw1tunbxxTf9eCCvksyGKnV0dUgqqueJWmdjWDbdaTh9AzSi4vVrUODrpwoJ1nspgvGZMchJbI9WrqgLNQXMiHHefEyS9AO69ZOFBLq52cxt944lkNTNQXYJd5gB9c9wb9knM?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

**VD**: lọc những công việc đang lên kế hoạch, để sắp xếp thời gian tiến hàng làm.

Người dùng cũng hoàn toàn có thể phối hợp thêm các điều kiện lọc khác, hoặc áp dụng thêm nhiều tiêu chí lọc nâng cao hơn. Kết hợp giữa lọc theo trạng thái và các điều kiện lọc mong muốn.

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXeTnVzFNclw5LLH9Jjwn9kWQZQhXpckl3QgUsMHOlwVpIgrwmMJzfjapxyjSIuD3xS-DQ7WxAGrLsX7xFRkb7PI5rLftZ_YxpANV4VzABXC_luoBKQbzgIb7l3NIDyaX_L54x87oRA5031siwynVJPyrnwe?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXc1uDZCTMLXbf1_d9n6E2GnZH7HuqXAQNzBymWiZfK03EgB1qYArtHYCPuRk8KoFew8L6qSE5ODydXbtNtqN1xTQSxW743XI7QHY0_h2ors7uSP3SeCsdqF8pG4rKJsrOpx1vjO2mi2jeCyS5SvLJK4sFb6?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>



Hoặc người dùng có thể tạo các bộ lọc riêng, kết hợp tiêu chí lọc theo trạng thái.

**VD**: Thống kê những đơn hàng có trạng thái là “hoàn thành” với giá trị > 100 triệu đồng.

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXe2htBNa7g1BsB82ezaiRfivQw54BHPyaAXlL3p6cyO1nfAegzNeCUkLIk5HQffF6eXGr5gU6dX2kVFyMVI37gMHPXS7HVrRZF_D8d_jxclUEb5V5StBvHKbOJY7lnWM6IvUvOJgzmKWrIhOUovOjXUekze?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (209).png" alt=""><figcaption></figcaption></figure>

Với workflow thông thường, ngoài việc theo dõi luồng tiến trình thực hiện trực quan dễ dàng, người dùng vừa tiết kiệm thời gian, vừa giảm thiểu chi phí khi quản lý công việc, mà thao tác cũng rất dễ dùng và đơn giản.&#x20;

Ngoài luồng workflow trên, phần mềm đã và đang phát triển thêm tính năng nâng cao hơn, nhiều luồng tự động hơn đáp ứng linh hoạt nhiều tình huống hoạt động trong doanh nghiệp của khách hàng với loại Workflow 2 và 3 dưới đây, mời mọi người cùng tham khảo.



### Workflow loại 2: Standard - Tiêu chuẩn

#### **1,  Ví dụ thực tế**

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXcOlSQT8h2l7zZh8XQFaeJ92sb_yfWkVRf01KQZ-TzKYQrTJSOFMxkj7POeVMd6GlAVUn1iNCZ4kBIsvqPRjfFXWdksOln0E6HXcsLFhJ7YV8NJT51k5TfF_V1_0uttSveUN720G5oqk6sM8wF4tUKKU84?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (210).png" alt=""><figcaption></figcaption></figure>

**Ví dụ** về một quy trình quản lý kho như trên, tiến trình công việc được thể hiện thành một Workflow standard như bên cạnh. Các giai đoạn, công việc xuất hiện trong quy trình sẽ được thể hiện dưới dạng các trạng thái và được đánh số thứ tự để người dùng có thể thấy được thứ tự các công việc cần thực hiện một cách rõ ràng, minh bạch.

Như đã nói ở phần Workflow basic, Workflow standard sẽ có thêm các tính năng mới và một trong số đó là đưa ra các điều kiện về người chuyển, các trường thông tin và các mục liên kết phải thỏa mãn những yêu cầu đã được đặt trước đó để cho phép chuyển trạng thái.&#x20;

Ví dụ như ở trạng thái 6 là Kiểm tra, người dùng có thể cài đặt điều kiện người có quyền chuyển trạng thái là trưởng phòng phòng HC-KT (lúc này chỉ một mình trưởng phòng mới chuyển được trạng thái kiểm tra) và các trường dữ liệu như Số lượng thực nhận phải bằng, lớn hay nhỏ hơn một số lượng đã được cài đặt sẵn. Khi chuyển trạng thái, hệ thống sẽ kiểm tra các điều kiện và khi thỏa mãn tất cả mới cho phép chuyển trạng thái như hình dưới.

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXfn47xi0cZOE89MVg4yq8YHbOtjorjRpnW_jgDOeUv5BaL0wDghRzohojiw5q0afHHc9kVmpBXG_mXSOgLyvu_wgDDeTW_7ggwxPz284C6xDLeKHXUdbw6ogaDbMsXxD_u35BInfvF2taHge3k67GNDAAg?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

Bên cạnh đó, mỗi giai đoạn trong công việc đều có nhu cầu nhập liệu, quản lý những dữ liệu khác nhau. Điều này sẽ gây bất tiện nếu như đến mỗi trạng thái, người dùng phải tìm kiếm những trường dữ liệu tương ứng cần điền hay cập nhật khi thay đổi trạng thái công việc trên màn hình chung (nơi chứa tất cả các trường dữ liệu trong công việc cần quản lý). Hiểu được điều này, Workflow standard đã cho ra giải pháp bằng cách hiển thị pop up màn hình gồm những trường dữ liệu cần điền hay cập nhật khi người dùng chuyển trạng thái.&#x20;

Ví dụ khi người dùng chuyển trạng thái từ Tiến hành mua sang Kiểm tra, màn hình của trạng thái Kiểm tra sẽ hiển thị các trường dữ liệu cần nhập hay cập nhật tại trạng thái đó như Người kiểm tra, Số lượng đạt, Số lượng không đạt, … như hình dưới.\


<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXeN3MJK_w4hBJSS5jru-f4MwIzmbVIcy13D6T10GDyq0lbcnMBBOutZ8uv2K9ySSNF6aCjjPjbMRqcMBz46SjsgFmZRn9xEwGiIfs46LTY1o6NHHZvbEEV3Tcz6AJeN0ZJug42QNzHqFJXmLkypXdfzfaDI?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

Không chỉ dừng lại ở đó, một trong những tính năng hỗ trợ người dùng nhiều nhất đó là tính năng tự động. Áp dụng tính năng này sẽ hỗ trợ người dùng tự động điền các trường dữ liệu, các thông tin cần quản lý ở từng trạng thái theo những quy tắc đã được đặt ra trước đó.&#x20;

Ví dụ khi chuyển trạng thái từ Lựa chọn nhà cung cấp sang Phê duyệt, người dùng có thể cài đặt sẵn người làm là một trong những người đã được chọn và trường dữ liệu Ngày phê duyệt là 2 ngày sau khi chuyển trạng thái không tính ngày thứ 7 và chủ nhật. Nếu có thể áp dụng được tính năng này một cách linh hoạt và phù hợp với quy trình làm việc của doanh nghiệp sẽ hỗ trợ rất nhiều về mặt thời gian quản lý công việc và độ chính xác của các thông tin khi nhập liệu lên hệ thống.&#x20;

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXf0mKo-LT1uu2DOZOi0QRKxF9bCdA3OrW1FLX01bU5-tzaMcM7CkpLQY2zBiSrgJn6eOWoSgGZp7Sl9GZnteop4r5WUHMCJcmQB-gC9ZnRrx3SPKySIz4gs5aCy-wjWsp1MuPzyoY1pSMV0SCcV9YKlWX8?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

Đó chỉ là số ít những điều mà Workflow standard có thể làm được. Để có thể tìm hiểu đầy đủ và chi tiết về các tính năng tiện lợi của Workflow standard, người dùng có thể xem chi tiết ở dưới đây.



#### **2, Mục đích sử dụng, tính ứng dụng**

Workflow standard là một workflow gồm các status (trạng thái) sẽ chỉ đi theo một đường thẳng, tuần tự các bước, số thứ tự được đánh trên các status (và sẽ có các tính năng sau đó ăn vào số thứ tự của status). Bên cạnh đó Workflow standard cũng sẽ cung cấp thêm các tính năng mới hỗ trợ người dùng trong việc quản lý và thực hiện công việc. Các transition (bước chuyển) sẽ định nghĩa đường đi và kết nối các status, thể hiện mối quan hệ giữa các status được nối với nhau.

Workflow standard hứa hẹn sẽ đem đến cho doanh nghiệp một trải nghiệm làm việc thuận tiện trên luklak với các tính năng mới được cập nhật dưới đây:&#x20;

Điều kiện:&#x20;

* Mục đích sử dụng: Cho phép người dùng đưa ra/cài đặt các yêu cầu, điều kiện cho công việc ở mỗi giai đoạn của tiến trình công việc mà chỉ khi đáp ứng đầy đủ các điều kiện đó, hệ thống mới cho phép chuyển trạng thái.&#x20;
* Tác dụng:&#x20;
  * Đảm bảo công việc của doanh nghiệp ở từng giai đoạn được hoàn thành một cách đầy đủ, chính xác và hoàn chỉnh nhất có thể nhờ những điều kiện được cài vào trước đó
  * Phân quyền rõ ràng cho những người thực hiện công việc, đảm bảo chỉ những người được cho phép mới có thể chuyển trạng thái trên issue



Nhập liệu

* Mục đích sử dụng: Ở mỗi giai đoạn của công việc, doanh nghiệp đều cần quản lý, nhập liệu các thông tin khác nhau, thay vì phải nhập liệu tất cả các thông tin trên cùng một màn hình như Workflow basic thì ở Workflow standard, mỗi trạng thái sẽ có có một màn hình riêng gồm những trường dữ liệu, thông tin mà doanh nghiệp cần quản lý. Khi chuyển trạng thái hay nhấp chọn vào trạng thái trên Workflow thì màn hình của trạng thái đó sẽ hiển thị các trường thông tin cần điền hoặc cập nhật ở trạng thái đó.
* Tác dụng:&#x20;
  * Việc nhập liệu thông tin công việc được tách biệt rõ ràng, minh bạch và không bị loạn&#x20;
  * Giảm thiểu sai sót khi phải nhập liệu trên một màn hình gồm quá nhiều trường dữ liệu.&#x20;



Tự động

* Mục đích: Tự động luôn là một tính năng đa dụng và hỗ trợ người dùng rất nhiều trong công việc. Người dùng có thể cài đặt trước các yêu cầu cần hệ thống thực hiện ở từng trạng thái và hệ thống sẽ tự động thực hiện các yêu cầu mà người dùng đưa ra ở trạng thái đó.&#x20;
* Tác dụng:&#x20;
  * Tinh giảm quy trình rườm rà, tự động hóa công việc nhập liệu thông tin sẵn có, thay vì người dùng phải tự nhập tay hay tính toán số liệu sau đó nhập lên Luklak.
  * Tối ưu hiệu suất làm việc, rút gọn thời gian nhập liệu thông tin lên hệ thống để nhân sự tập trung làm những công việc quan trọng hơn

\


#### **3, Giao diện màn hình, HDSD**

Để ứng dụng được những tính năng phía trên vào trong phần mềm, phục vụ nhu cầu của người dùng, dưới đây, Luklak đưa ra hướng dẫn sử dụng chi tiết cho người có thể tự cấu hình. Những tính năng được bôi vàng đang được hoàn thiện và sẽ ra mắt sau 2 tuần nữa.



**Bước 1:** Ở thanh Menu, chọn vào phần Mở rộng, ấn chọn Chức năng. Sau đó lựa chọn chức năng muốn cấu hình và thêm tiến trình với lựa chọn Cấu hình là Tiến trình tiêu chuẩn.

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXcpGwctOds2inDi-TC8bEXLTRvui5eM0zGCMtwztQupfIFX0yXR95IIkF40I3Io7-snG639TMrvBNqP7fjGXGIcP3PP3eBAc2mpPNLlYfb5A4MhSMOLzXDcbRUKec9AbExmQjmVrrB-7SOD3TLIs66HjniZ?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

**Bước 2:** Người dùng vẽ tiến trình và lựa chọn trạng thái muốn thiết lập tính năng

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXdINxQ2_aSA1wMngkCddc7FtEuR6D_eOKEBCM5QzX3SwoinFMoWCv1VdAws6Dt8igXYAzKtDaioRLA4S6waMUutBgZtbZDhaRAR0WpzndEjwdBmq8luR4VqoTrFfCt1wBYVbWkBYHUa42NWoIUYONo0AGVX?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

**Bước 3:** Nhấn chọn Cấu hình và tiến hành cấu hình cho trạng thái

Điều kiện: cài đặt các điều kiện để hệ thống đối chiếu rồi đưa ra quyết định chuyển trạng thái. Dưới đây là các loại điều kiện mà người dùng có thể cài đặt:&#x20;

* Người được chuyển: những ai được chuyển với từng trạng thái và chỉ những người được cài đặt quyền chuyển trạng thái thì mới có thể chuyển trạng thái (admin/owner hoặc người được gán vào issue mà không nằm trong người được chuyển cũng không chuyển được trạng thái).&#x20;
* Có thể cấp điều kiện người ở 3 mức: dữ liệu trên issue field (assignee, supervisor...); dữ liệu ở space (component lead/member); dữ liệu từ tổ chức (nhập user, group cụ thể). Cài đặt này áp dụng linh hoạt cho từng trạng thái nhất định, bám sát chặt chẽ theo quy trình của doanh nghiệp.
* Các trường dữ liệu: cài đặt điều kiện ở từng trạng thái dựa trên dữ liệu của mục, ví dụ người dùng cài đặt Số lượng thực nhận lớn hơn 1000 thì khi giá trị được nhập ở trường dữ liệu Số lượng thực nhận phải đáp ứng được yêu cầu đó thì người dùng mới chuyển được trạng thái.
* Mục con/Mục kiểm: Những phiên bản trước đây của LUKLAK, subtask và checklist sẽ được gắn chung vào giao diện mục việc. Với bản cập nhật mới, subtask/checklist có thể gắn riêng vào từng trạng thái trong quy trình công việc. Điều này giúp người dùng biết rõ mỗi status sẽ có các mục con, mục kiểm nào thuộc về công đoạn đó. Từ đó sẽ ra được điều kiện cho chuyển trạng thái là: các subtask/checklist thuộc status hiện tại hoặc các status trước đó phải hoàn thành hết hoặc đặt ra mức bao nhiêu cái cần xong nhất định thì mới cho chuyển.
* Mục kết nối: Những mục được liên kết với đầu công việc đó phải ở một trạng thái nhất định mới chuyển được trạng thái của mục việc.&#x20;

_**Lưu ý:** khi người dùng cài đặt các điều kiện ở trạng thái nào thì trước khi chuyển sang trạng thái đó, hệ thống sẽ kiểm tra xem đã đáp ứng các điều kiện cài đặt chưa. Nếu đã đáp ứng thì sẽ cho chuyển trạng thái._

**Nhập liệu:** cài đặt màn hình cho từng trạng thái, mỗi trạng thái sẽ bao gồm những trường dữ liệu và liên kết nào.

**Tự động:** cài đặt các trường dữ liệu sẽ tự động cập nhật sau khi chuyển trạng thái. Các trường thông tin mà người dùng có thể yêu cầu hệ thống tự động thực hiện bao gồm:&#x20;

* **Trường người:** assignee, supervisor....
* **Trường ngày:** start date/ due date, any date
* **Trường số:**
* **Trường text:**
* **Issue link:** thêm và xóa

Các hành động mà chức năng tự động có thể thực hiện:&#x20;

Các cập nhật này đều có khả năng:

* Lấy nguồn dữ liệu từ issue khác điền vào
* Biến đổi dữ liệu kiểu thêm bớt, cộng trừ nhân chia…

Tự động tạo:

* Subtask
* Checklist

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXcF6JiBb4Ibhv3eo3aoJQbdENAz1a7x5OOVW2P4ii6yCHWgetI5gLWqP21BwSIMCYPeu_fOQlZptrEgXjnbW_eJkGVi6hJoDYEBeblQE4CVPYS0RX7pQ_FZMXBzac1tOp9i2pv5S1YMEPqckImvXshugYVn?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

**Bước 3.1:** cài đặt Điều kiện

* **Người được chuyển:** Chọn ra những người được quyền chuyển trạng thái

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXfUj3Ci1SSbuTugw9E23LypRKUb-oapGPSqyGGOrNrMLaZK-cHxBhPVtchnATPOL5qWZ2Aehl-qFI7Tn00K2j7fZXXMT0ry2Wj9LJymqOcmoETPtEoLXlUhx1c0hAncy0LS72k5oEFSyLS-3eXfXUNOwcT4?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

* **Trường dữ liệu:** chọn ra các trường dữ liệu và đặt điều kiện cho những trường dữ liệu đó

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXclxz-SzXagN-HDML4XeOZC9akdWyO11nN-QhS4poEByX0H_B3LMS5nJjjDsv4T58tS0omKIcMg-0UrLt-wq-HGqb2wdjOD3qquss0h42ktZq9ouANT2vNGudxEeWsF897C8YpswFAlau9uOMZAEyTA2M_x?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

* **Điều kiện mục kiểm:** kiểm tra số lượng các mục kiểm đã được hoàn thành hay chưa hoàn thành. Nếu số lượng đó đáp ứng yêu cầu mà người dùng đưa ra thì cho phép chuyển trạng thái. Các điều kiện có thể cài đặt bao gồm:&#x20;
* **Trạng thái ngay trước:** yêu cầu số lượng các mục kiểm ở trạng thái ngay trước trạng thái được cài đặt phải được hoàn thành đúng với số lượng người dùng yêu cầu mới cho phép chuyển trạng thái

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXcdIeF0MEwGL4_iZKLsZicUVT9hrFc97MIJC1bFR6TK2LRsC1C5inxFVViubGIrffFYsGB8-Hk6wLzdbmOBfjPmwLruPrxulu1mEA3RBFH1xG5TqFTjp2e1Ng-1gGpMJEPxc7tKD41PVFx9nOrbNVLsLaTS?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

* **Tất cả các trạng thái trước:** yêu cầu số lượng các mục kiểm ở tất cả các trạng thái trước đó đều phải đạt số lượng hoàn thành đúng với yêu cầu của người dùng mới cho phép chuyển trạng thái

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXdT9T2uS5O80YXiwrMx1PnScjZPrAgRl4kZSNb-_M9oP1iU4xZ08nKEP4Y2Pp4ARMge-X1EF_JK3AtwccZrHApJJ4xXeWJiaTgCbql32S3HinhOWZKaeG3xXucC20GurAtLuENQ4qGaim5WVTdbDLJyt4vx?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

Về các cách đưa ra số lượng mục kiểm hoàn thành hay không hoàn thành sẽ dựa vào cách cấu hình người dùng bao gồm:

* **Tất cả các mục kiểm hoàn thành:** yêu cầu tất cả các mục kiểm phải được hoàn thành mới cho phép chuyển trạng thái
* **Cài đặt nâng cao:** người dùng có thể đưa ra các yêu cầu để tính toán số lượng của mục kiểm cần hoàn thành thông qua việc cài đặt các yếu tố bao gồm:&#x20;
* Trạng thái mục kiểm

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXfZ8hbSw0hqGAttNZJwsSOrtLx0xAZKGvEyiijNbsGq97YqpBMUNSTGS8eSioY-9NZJDH6gqcWKu11c8stwCcooVGugaU9sCMfhLcxxQzJTyWOiB-KRpJTSw-jwEyXUmenGPxTAI-eTWAsTQmGPAeSJB0E?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

* Các so sánh&#x20;

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXdYpI7e6dwaNKKilFh4XQcoy7Le2ahdNpf30y0fePOg23Dml1--YkDrV4UHZTpS7TgbVWZysuypBhaA6UyEKJThV-EWDdC7UKuv6tFue9VvxDDUiRvAXWyBRVl30I3TD1VO6hX2eXw8wpbkHYreInuBQpde?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

* Số lượng

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXfm2rAwb9zI7rta-1g_21I2cRqquP837YBP0F6l2Fcp_pWoY15moCqykZBb9gQ_a7fjXAaQWHb13EScZUtjcKY2sGGvitSiiHeEIKmUgkX8WLq1_A78CTt_vydN453qBq99OzVmWIClAoqd_nQP3Gn2-eHC?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

* Đơn vị tính

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXdZdDDfAYRS30OZuyPYRbUGVe9vIvs8X_jGkdmoMtKQjmzN43Ru_R7uTd8VBeByvFRY6f6TVWAQIBO7vV9uDp0m5BXxnHNVGXfS59kbtivlqFkZXTbQx-PbzwDgk0jrsy6jPwZgz6SRzaMoymFyzVifcSEn?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

Như ví dụ ở như hình dưới, số lượng các mục kiểm ở tất cả các trạng thái trước đều phải hoàn thành 100% thì mới cho phép chuyển trạng thái&#x20;

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXe0EcH-Qj1IQw3oIO184PPBQD1gUI1gRkSomvqdiVRN6d9sSMMdccWR4Mc9PdaIzoFbfsKB-_8wPBKQDZNa4ftGaRq0JXQG0ZLtZTicQD3RHWJHYZI-ZXMd0Ft2wKjek1a7W5XCPC8mefac3jI_tnN4xHge?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

* **Điều kiện mục việc con:** Kiểm tra số lượng mục việc con đáp ứng được các điều kiện mà người dùng đạt ra. Nếu số lượng đúng với yêu cầu của người dùng thì cho phép chuyển trạng thái. Các điều kiện người dùng có thể cài đặt bao gồm:&#x20;
* **Trạng thái ngay trước:** yêu cầu các mục con của trạng thái ngay trước phải đáp ứng các điều kiện mà người dùng đưa ra và số lượng phải đạt yêu cầu của người dùng thì mới cho phép chuyển trạng thái
* **Tất cả các trạng thái trước:** yêu cầu mục con ở tất cả các trạng thái trước phải đáp ứng các điều kiện mà người dùng đưa ra và số lượng phải đạt yêu cầu của người dùng thì mới cho phép chuyển trạng thái

Về các cách đưa ra số lượng mục con đáp ứng yêu cầu sẽ dựa vào cách cấu hình của người dùng bao gồm:

* **Tất cả mục con:** tất cả các mục con phải đáp ứng yêu cầu đặt ra thì mới cho phép chuyển trạng thái.
* **Cài đặt nâng cao:** người dùng có thể cài đặt các yêu cầu để hệ thống lọc ra mục con. Nếu số lượng mục con đạt với yêu cầu về số lượng của người dùng đưa ra thì cho phép chuyển trạng thái. Các yêu cầu của người dùng về mục con sẽ được thể hiện thành các yếu tố trong tiêu chí lọc.&#x20;

&#x20;hoạt động giống với bộ lọc issue bình thường, người dùng sẽ đưa ra các tiêu chí và hệ thống sẽ dựa vào các tiêu chí đó để lọc ra các issue thỏa mãn

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXfGQtxTQKOW5yi5tyv9YGPNxPw5-ozyhdpSW2IgT19Getq31VD67bXW6s3Kqy0R1-kqmNVasGAGSLe0gmfpIyt8VNAOf4U1lk8ptkOlROzCG93TSx2KVQxq6Gjeq4HTf3Wji3XUs2BFJxHkaePT4shM2Xs?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

Để có thể đưa ra yêu cầu về số lượng các loại mục con, người dùng cấu hình tại phần “Số mục lọc” bao gồm các yếu tố:&#x20;

* Cách so sánh&#x20;
* Số lượng
* Đơn vị

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXfMOJWsMECJN18FLsqhWjytFl2F5bowdGUSWJvyILQ3P5rj_UhVenkrIWurl8HEj_ESC1sy93p-QhP_asphup2NxNNZVHCSfVaAurV84830xOOn36QSRdrUuVDEA0o8YW1IJOXWNkVnprU4XJoeozzzRIc?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

Kết hợp 2 thành phần “Tiêu chí lọc” và “Số mục lọc” ở trên, điều kiện mà người dùng cài đặt ở đây có thể hiểu là mục con phải đáp ứng các yêu cầu: đang ở trạng thái hoàn thành, trường Số lượng theo chứng từ có giá trị lớn hơn 100, Hình thức làm việc là Fulltime, Người kiểm tra là Huy nguyễn và Hộp kiểm đơn đã được đánh dấu. Nếu số lượng mục con đạt đầy đủ các điều kiện đó thì sẽ cho phép chuyển trạng thái.&#x20;

* **Điều kiện mục kết nối:** Kiểm tra các mục kết nối có loại kết nối đã được người dùng lựa chọn và đạt các điều kiện người dùng đưa ra. Nếu các mục kết nối thỏa mãn các điều kiện và số lượng đặt ra của người dùng sẽ cho phép chuyển trạng thái. Các điều kiện người dùng có thể đặt ra bao gồm:&#x20;
* **Tất cả các mục kết nối:** tất cả các mục kết nối phải đáp ứng điều kiện mới được chuyển trạng thái.
* **Cài đặt nâng cao:** người dùng có thể cài đặt các yêu cầu lọc ra mục kết nối. Nếu số lượng các mục kết nối đạt yêu cầu về số lượng của người dùng đưa ra thì cho phép chuyển trạng thái. Các yêu cầu của người dùng về mục kết nối sẽ được thể hiện thành các yếu tố trong tiêu chí lọc.  &#x20;

Tiêu chí lọc hoạt động giống với bộ lọc issue bình thường, người dùng sẽ đưa ra các tiêu chí và hệ thống sẽ dựa vào các tiêu chí đó để lọc ra các issue thỏa mãn

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXezqLvqMhAKio4K0O2TuCLJwqbDxQDJM1lizGIi1GNdP7r9RZiryhbPw6Xw-1kCCrNbBLzg5PTSAe7xFfD1RKOf0Rvc8G01YzqjoYroCupjdBNaiDfRNSW_O-shlZyf2YvhGUlnR9pZtSh3X_Cyby3HdAOz?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

Để có thể đưa ra yêu cầu về số lượng các loại mục kết nối, người dùng cấu hình tại phần Số mục lọc bao gồm các yếu tố:&#x20;

* Cách so sánh&#x20;
* Số lượng
* Đơn vị

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXdr8tf7Gx4837BGymnIZZ9_RtxCkC-kTfz6aPXxwMWGZxtTLxfKpIwDXmNxa5B3Pjfu9yo3g8DZ8llpvGNxav0SvqUudhc5AvZTG3Fdq5f887trzcKcvh9nPaeYDcvbL7AHpXkkw3nCc9YABenUoUsn9tYZ?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

Kết hợp 2 thành phần Tiêu chí lọc và Số mục lọc ở trên, điều kiện mà người dùng cài đặt ở đây có thể hiểu là các mục liên kết phải đáp ứng các yêu cầu: đang ở trạng thái thuộc nhóm hoàn thành, các trường dữ liệu Người đề xuất, Sản phẩm không được để trống và các trường dữ liệu Số lượng đặt, Đơn giá, Thành tiền phải lớn hơn 0. Nếu số lượng các mục liên kết đạt đủ các yêu cầu trên đạt 50% tổng số lượng thì hệ thống sẽ cho phép chuyển trạng thái.

**Bước 3.2:** cài đặt Nhập liệu:

* **Cập nhật trường:** Người dùng cài đặt những trường dữ liệu muốn điền hay cần cập nhật ở trạng thái nhất định thì khi chuyển trạng thái, màn hình sẽ hiển thị lên các trường dữ liệu đó.&#x20;

Ví dụ như ở Trạng thái Kiểm tra, người dùng cần nhập liệu hay cập nhật các trường dữ liệu như Người kiểm tra, Số lượng đạt, Số lượng không đạt. Để làm được điều này, người dùng nhấn chọn trạng thái Kiểm tra trên workflow và cấu hình phần Nhập liệu. Sau đó thực hiện các bước như hình dưới để đến khi chuyển trạng thái sang Kiểm tra, hệ thống sẽ hiển thị màn hình trạng thái Kiểm tra gồm các trường dữ liệu đã được người dùng lựa chọn để nhập liệu hay cập nhật.&#x20;

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXdJjGKlbNSWL4iRH_elrp1-fG1Tqt7sjdRJYtY7kGY4rjLOAFBg6EaKOhiLwuWbox7WQiDbFewKyiMZ9fktB1e6xvAZN45jlybXQBKqvKeSaeh_6aisFI8xNqM_WvzsUzReLr7P_9bYCizLKhdar3fVoYTe?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

* **Thêm kết nối:** Đưa ra một danh sách các issue đã được chọn lọc dựa trên các điều kiện mà người dùng đã cài đặt bao gồm:
* **Loại mục nguồn:** đưa ra các loại mục hiện đang nằm trong chức năng đang cấu hình và qua đó cũng lọc ra các loại liên kết có thể tạo ra từ mục nguồn đã chọn.
* **Loại kết nối:** có thể được hiểu là kiểm kết nối, là cách thức mà loại mục nguồn kết nối đến các mục khác.
* **Tiêu chí lọc:** Tiêu chí lọc sẽ hỗ trợ người dùng có thể sàng lọc kỹ hơn các issue có thể kết nối.&#x20;

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXfIs35aI3-yOyhF63zAGarMjAHe5gmHW54N0t33ntJUZGA_PKIe4hRruJKqehoYZjc6iwtFKq1M02lw_c6ARvHjVT5u1H0wLNvHv1GGr6nkBnKQ_wxQ_C3d01amUQGDGMo8m7mJrDcQ78hkKiEBvqeo8YbF?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

Như ví dụ dưới đây, sau khi đã cài đặt các yêu cầu tại phần nhập liệu của trạng thái Kiểm tra phê duyệt, khi chuyển sang trạng thái này, màn hình nhập liệu sẽ xuất hiện và hiển thị các issue có loại có thể được kết nối từ lại mục nguồn là Task với loại kết nối là Đề xuất.



**Bước 3.3:** cài đặt Tự động:

**Trường dữ liệu:** Thêm các trường dữ liệu mà người dùng muốn hệ thống thực hiện tự động theo yêu cầu đã được cài đặt trước đó

* **Trường người:** Tự động điền trường dữ liệu người mà người dùng đã cài đặt dựa trên tập hợp người đã được lựa chọn trước đó tùy theo Điều chỉnh theo tiêu chí nào và Cách chia ra sao. Các cách chia bao gồm:&#x20;
* **Chọn ngẫu nhiên:** Chọn ra ngẫu nhiên 1 người trong tập hợp người mà người dùng chọn ra để tự động điền vào
* Chọn theo vòng tròn
* Chọn người ít mục nhất

Các cách điều chỉnh bao gồm:&#x20;

* **Điều chỉnh theo mục kích hoạt hành động:** chọn một người từ mục/mảng việc/tổ chức của mục chuyển trạng thái được người dùng lựa chọn từ trước để điền vào trường dữ liệu được cấu hình theo Cách chia đã được chọn.

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXdtknrDZRZBDUNAlGKg2gaFmW5Rmb4BDhODjNlARtgyrRyaX1id8IA3cthb8ysRu9cxHQZXBx-JU5_tOtkTd-cuzfwJu_kowRDWiEJ-AiF2B2A_0EZzh4WQG76ZEUX-0rstdkBlBT70B550nwcBdLHmiOpR?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

* **Điều chỉnh theo mục cha:** lấy một trong những trường người từ mục cha/mảng việc/tổ chức của mục chuyển trạng thái được người dùng lựa chọn từ trước để điền vào trường dữ liệu được cấu hình theo Cách chia đã được chọn.

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXduKB3vXYj116p0Xu8DSC55_j34Nstevfr5kRC782PrDr0H-_VyUkgdkE4wPtp69XHYvppE5xE-rMVEtYLJl0vSOtKBXbEAmp9foXsQxRrebrf_sGHtib6fi5qr4Tt6kUmXs79rZJf65YhsxMGljFmJ8jtL?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

* Điều chỉnh theo mục hiện tại
* Điều chỉnh theo mục đích đến
* **Trường ngày:** Tự động điền trường dữ liệu ngày mà người dùng đã cài đặt dựa vào Điều chỉnh theo tiêu chí. Các Tiêu chí bao gồm:&#x20;
* **Đặt giá trị cụ thể:** lựa chọn một ngày cụ thể để điền vào trường dữ liệu

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXfy6Rf54zPgLbGsMRgFmSwE8spYCuQnCXZVkcV2Hew5-WHOlGEFG1QI8Jp5o2Z_JoHp_9ULD5PiLi2UyGwW8VxykbmVV8ZlvZ1pU2yaIeumrdGOCnxG6kyJ5ZMku0aNWV6yacVAAFdUkh8BmGMBxiJHOVM?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

* **Điều chỉnh theo điều kiện:** Lấy mốc thời gian thực hiện hành động, cộng/trừ số ngày lựa chọn để đưa ra gán giá trị ngày cho trường

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXeifphgiC1AME6eEkRBYUR_SES02ypKBT_JFCnvvIgE3i7VLDGsl7gbNPwpH2omAgrKINg5-iqqh2rE3BfdcAvcc6L_gb_a4nHptzm-ACNL3VfHANAGtGeplHzzE6mbsmFCCyPUOdU4dJFWQU3mC_an7vek?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

* **Điều chỉnh theo mục đích kích hoạt hành động:** Lấy Trường Nguồn làm mốc, khi trường nguồn thay đổi sẽ cộng/ trừ số thời gian đã nhập để gán giá trị cho trường

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXeGCtgsWIrL9mSMm9cIjZK5MttXMnr3lDV5a6TS2ORWbJJjiTs6HseAlHU_rIZzM7TsfkNdAin7_PCpC3X8p6J4rpdlIurYXuWJ8zgchoZHb4xucBZUHFe8LZ0bcwgo9oO9l0tDWzb33mZnXw9PQzd0o2em?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

* **Điều chỉnh theo mục cha:** Lấy Trường Nguồn từ mục cha làm mốc, cộng/ trừ số thời gian đã nhập để gán giá trị cho trường

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXclB5L5lb98-DGl2u6oTJX7W0dnhDtdSJfFHlNw2qRn_1dBWcqcbJaWadajXiN6zcmuvvZbz7l0ApmLByuZK1JrokHA2jZ6b6-FzyVK_LULGmo9-poDqx05p2dMCWMnGZtmvEUqPD2AGPQ95rFulzjj8Rte?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

* **Điều chỉnh theo thời điểm kích hoạt hành động:** Lấy mốc là thời gian thực hiện hành động, cộng trừ số thời gian đã nhập để gán giá trị cho trường

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXeBZd3Q3Mob97e8n21uE7F-VtL-mvxsdmKymvYctubKZmDK7StLCf4k6qVA7tjkVISd2dCIY__EQpDZSOUjX2bY-TlGGc0chzTBvwmhYXK66OybDHcX23tjw60RE8wDIygODkwUALECpd1BA3yVAQ_B58UK?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

* Điều chỉnh theo mục hiện tại
* Điều chỉnh theo mục đích đến

_\* Nếu mục Bỏ qua ngày chọn Chủ nhật hay Thứ 7 & Chủ nhật thì nếu ngày lựa chọn đúng vào Chủ nhật hay Thứ 7 và Chủ nhật thì hệ thống sẽ tự động bỏ qua những ngày đó và chọn ngày kế tiếp để điển vào trường dữ liệu người dùng đã cài đặt_

\


* **Trường số:** Tự động điền trường dữ liệu số số liệu cố định, bằng dữ liệu từ một trường dữ liệu dạng số khác hoặc bằng phép tính của nhiều trường dữ liệu dạng số với nhau (các trường dữ liệu được chọn phải thuộc mục đang cấu hình)

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXcrvzdd81Jjz2jMPT07gGgepy4Cx1h4uO3OMf3TGfkXu7t2ctf20do0zbI9NRvM7UexACmMSVzCq6U4Q-KNysVmqMQ2eNeSOvaEjOV4ca1DnuQAiVQgB3XobhoifhSIxiEisX7MxuURhKvm3CyBMRtLbN0?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

* **Trường chữ:** Lựa chọn 1 chuỗi văn bản cụ thể để điền vào trường giá trị hoặc có thể kết hợp chuỗi văn bản tự nhập và giá trị của các trường dữ liệu khác với nhau để điền vào trường giá trị đang cấu hình (các trường giá trị được lựa chọn phải thuộc mục đang cấu hình)

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXeJyuyOK8R8RDYEBwyAYcmmkWZlUZZgFiKI95WskW8BOYlseS2TC2U7UhaLWNS4nknBHlRoUcD6q00TNytkjCNFw2OFk3WycqBlVAShBs_-lJzRRrjKpriwLdn8SX04w8iDjhwt-4fwm5PzKcawwnGVQg6r?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

**Thêm liên kết:** Tự động thêm các mục liên kết đáp ứng đầy đủ các tiêu chí mà người dùng cài đặt vào mục khi chuyển đến trạng thái được cấu hình. Các tiêu chí báo gồm:

* **Chọn giá trị cụ thể:** chọn ra các issue cụ thể, đã tồn tại trên hệ thống trong danh sách các issue được lọc ra từ các điều kiện về Loại lục nguồn và Loại kết nối để liên kết&#x20;

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXequcnaC1-z3dGkLS-IddqZVGl_-8THieendXmRBlSS8gq1woo5b8ALnIDB3T17ANRrfGK3ZU5xrG-ogIeJi8brVwT7H_F0vLf5PA_quoqUy0r-iV2oE95FjdT_hG4hAapEs5k_umd_YyQdmvzPKlbLtPGO?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

* **Dùng bộ lọc:** người dùng đưa ra các điều kiện về Loại mục nguồn, Loại kết nối và các Tiêu chí lọc, hệ thống sẽ dựa vào đó liên kết tất cả các issue vào issue thuộc loại mục đang được cấu hình

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXdymLsqc80GaTbNqhQhTUE3ugaK6lWIwvlhpTIhoxcMtOlv9STMdgW7LJIYflpcA_o8hRFMP-Qj4Nwy_MKoyjDAIPKh9KjoO-lEDuVhA9hfAN20ZVqqGLm-Cz1yoxvvj7B9nSzH8EgGN01N0iRtH1WVvDJH?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

* **Sao chép:** dựa vào nguồn mà người dùng muốn sao chép và điều kiện “Sao chép từ” để sao chép toàn bộ các issue mà mục nguồn liên kết để kết nối đến issue thuộc loại mục đang cấu hình. Các điều kiện Sao chép từ bao gồm:&#x20;
* **Mục cha:** sao chép toàn bộ các issue đã liên kết với issue cha để liên kết với issue thuộc loại mục đang cấu hình (issue con)

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXdxY52bs7AYPJxeZup_tphaYptcyYUR4TzQtf_yQTuVpWcxqlRUyrqkxaTUZhlww8pKy9EpRZn5TblXkYJ6KjEC3UHeA9U-MN5Os7reo4j4J2fEcWacOkhTM52QyPGY000mYRwzPc8O94ivIRTuB5KGW6DO?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

* Mục kích hoạt hành động
* Mục hiện tại
* Mục đích đến
* **Xóa kết nối:** người dùng đưa ra các điều kiện về Loại mục nguồn, Loại kết nối và các Tiêu chí lọc, hệ thống sẽ dựa vào đó xóa tất cả các liên kết đạt yêu cầu

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXca93ZfFW9-txBdsuMjs7XXe-9LpvHqCu8oWSYwqFQxSqs7lvCgBuXpa9fwpobOJULEfOJWnwYazl4CvlF2CLWs6o4-RxR9xSmGLHajSIc8fGyZDdcHNkSs8lYYiOgdsxsN_4pTVySffg2oCIb4cOW3CLw?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

**Tạo mục:** Tự động tạo các mục mới khi chuyển đến trạng thái đang cấu hình dựa vào các điều kiện mà người dùng đặt ra bao gồm:&#x20;

**Thông tin cơ bản:**&#x20;

* **Mảng việc:** mảng việc mà người dùng muốn tạo mục&#x20;
* **Loại mục:** lựa chọn loại mục mà người dùng muốn tạo. Loại mục phải thuộc mảng việc mà người dùng đã chọn ở trên
* **Tiêu đề:** tiêu đề của issue được tạo mới
* **Mô tả:** mô tả của issue được tạo mới

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXf3JZTRs3tK7W_EvBxpY89RPzoaBOPKr3WzD6NHalO8ZirZkRShJRpOYFYB3IkurSD69VmpWTzzmhM8REYsvYIQ8XS_zTViV783UZi4d_00nPH0SNi-CjYYJfangJQE0yZkgBH8Rs9LUNg1CNHSt3CMuaWe?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

**Thông tin nâng cao:**&#x20;

* Tự động thêm dữ liệu vào các trường dữ liệu có trong màn hình của mục được tạo tự động tương tự với phần Trường dữ liệu **đã viết ở Bước 3.3:** Cài đặt tự động
* Tự động thêm các mục liên kết tương tự với phần Thêm liên kết đã viết ở Bước 3.3: Cài đặt tự động

\


**Bước 4:** Cài đặt Đầu việc:&#x20;

* **Mục kiểm:** người dùng có thể tạo sẵn các mục kiểm cho từng trạng thái để khi chuyển đến những trạng thái đó, các mục kiểm sẽ tự động hiển thị lên màn hình mục việc.
* **Mục việc con:** hệ thống sẽ tạo các mục con của mục đang cấu hình. Người dùng có thể cài đặt Thông tin cơ bản, Thông tin nâng cao và Điều kiện của mục con được tạo

**Thông tin cơ bản:**&#x20;

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXcgU2D7vwmBoF7qFkQLDXz6qo-imzfCIk5b0_f9gyay7j1pfC8-ThjOMngZxyP00CdQkWhF_vTDGp1wZ9T-hMEtJXEViJtCrFH7OxNG5V2L_IznOlTChExz8ES0EFyJFEac7XsjaZV27cWdkxvFbfxM6fc?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

**Thông tin nâng cao:**&#x20;

* Tự động thêm thông tin vào các trường dữ liệu có trong màn hình của mục con được tạo tự động tương tự với phần Trường dữ liệu đã viết ở Bước 3.3: Cài đặt tự động

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXcg0iNfFTZfkdfjeNkgzs4vr7YohoGsovYcAHxjxPX0XDEifsb66bh_AphMKXu6cgJf9PgDfhJar2QKa2EBstS5ejrQ0j0NNKhLoGWzREhUHYee3Y8GSgP70FPAWAyjYPnm2Js6WNuGGSvERWEm7hsOCLf2?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

* Tự động thêm các mục liên kết tương tự với phần Thêm liên kết **đã viết ở Bước 3.3**: Cài đặt tự động

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXfkmjKOcDuRkfB1yksRh8q9_2cQee_ShFV5xkYCCLyAKJT_GWblZbFq6e8HliYG5pHjiyMWoqejkUGrHPOMIsusxhnlynWaeBJEPv91aOTgocP_GiMUMX5Jqa9EJVo6oYn6ghs0ya6mJpVd3NQDAoP-plGp?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

* **Điều kiện:** người dùng đưa ra các điều kiện về Điều kiện dữ liệu, Mục kiểm, Mục con, Loại kết nối. Nếu khi chuyển trạng thái, issue đáp ứng đầy đủ các điều người dùng đưa ra, hệ thống sẽ cho phép chuyển trạng thái.&#x20;

\
\


<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXel0g32W2YBJaLiZnwYVmnR-A5BFN_ulsrlK0-OFXLk1AiwDdJKipdU0IiyBjrPJ-J2SnTBR_DcFEuzEJ61RGjZsRaERfPtSyXLiCxDeBsdI8Fi-YjvgEb3z1jPh-IKSbX7j0xArn0VzCeDua9j5cvVzz4?key=Pj5SQn1IP1YRt0MtCTTbqw" alt=""><figcaption></figcaption></figure>

#### Workflow 3: Advance - Nâng cao (sắp ra mắt)

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
