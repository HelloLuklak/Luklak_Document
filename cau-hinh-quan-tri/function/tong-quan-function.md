# Tổng quan function

<figure><img src="../../.gitbook/assets/image (504).png" alt=""><figcaption></figcaption></figure>

### 1. Định nghĩa Chức Năng trong LUKLAK

Chức Năng (Function)

* Là **đơn vị lõi** để người dùng định nghĩa, tạo ra các cách làm việc khác nhau trên luklak. Một chức năng đại diện cho một công việc/mảng việc. Ngoài ra, mỗi chức năng có thể chứa một hoặc nhiều mảng việc khác nhau nhưng có cùng tính chất, quy trình công việc.&#x20;
* Ví dụ như chức năng Marketing sẽ giúp bạn tạo ra mảng việc Marketing HN, Marketing SG... Các cấu hình bên trong chức năng Marketing như tiến trình công việc, danh sách trường dữ liệu, phân quyền sẽ được thể hiện ở các mảng việc tạo ra từ chức năng.
* Người dùng không làm việc trực tiếp trên Chức Năng (không thể tạo mục, sửa mục, giao việc..) mà sẽ làm việc thông qua mảng việc bên trong chức năng. Một Chức Năng được vận hành hành trong một mảng việc nào đó và thường được tạo nên bởi các quy chuẩn công việc cụ thể bên trong.&#x20;

**Ví dụ:** với Chức Năng Quản lý nhân sự sẽ có các loại mục cụ thể bên trong như:

1. Hồ sơ nhân sự: lưu trữ toàn bộ thông tin về 1 nhân sự
2. Thủ tục nhân sự nghỉ: Khi nhân sự nghỉ phải trải qua một quy trình thực hiện thủ tục
3. Các đề xuất nhân sự: nhân sự cũng thường có các đề xuất như tăng lương, thăng tiến, đánh giá,...

* Khi có bất kỳ sự thay đổi nào trong tiến trình, hệ thống sẽ thông báo tới những người liên quan về cập nhật mới nhất của tiến trình.                                                                                                         &#x20;
* Cập nhật, thay đổi cấu hình các function khi đã có các mục (issue) sử dụng function đó.

Mỗi một chức năng sẽ tùy biến, người dùng có thể điều chỉnh các cấu hình dưới đây:

* Loại mục: thể hiện quy trình vận hành của công việc
* Vai trò: quy định các chức danh cho người dùng như trong doanh nghiệp.
* Phân quyền: quy định những ai (user/group/role) sẽ được phép làm gì trong mảng việc chứa chức năng đó.
* Thông báo: tùy chỉnh xem những thay đổi gì diễn ra trên issue đó thì những ai (user/group/role) sẽ nhận được thông báo.
* Thành viên: phân quyền cho những ai (user/group/role) được phép chỉnh sửa, cấu hình chức năng.
* Automation (tự động hóa) (tính năng này đang được phát triển)&#x20;

### 2. Các thành phần trong Chức Năng

#### Issue Type (Loại mục)

* **Loại mục được sử dụng** để cấu hình cho các chức năng. Các Loại mục phân biệt các loại công việc khác nhau theo những cách riêng và giúp xác định, phân loại về công việc của bạn trên LukLak
* **Mỗi Chức Năng (function)** có các Loại Mục (issue type) khác nhau để quản lý các loại đối tượng thông tin khác nhau, mỗi đối tượng này có cấu trúc thông tin dữ liệu (custom field) khác nhau.
* **Mỗi issue type** đại diện cho một loại công việc, với tính chất, quy chuẩn làm việc riêng biệt, được định nghĩa/vận hành thông qua 2 yếu tố:
* **Workflow (tiến trình):** quy trình, tiến trình các bước thực hiện công việc đó.
* **Custom field (trường dữ liệu):** các trường thông tin dữ liệu cần thiết về công việc đó để đáp ứng chức năng - nhu cầu công việc.

**a. Workflow (Tiến trình):**

Bất kỳ công việc nào cũng sẽ có Workflow (Tiến trình) thể hiện quy trình các bước diễn ra của công việc đó.

Workflow (Tiến trình) được tạo nên từ 2 yếu tố:

1. **Status (Trạng thái):** thể hiện trạng thái công việc đó đang ở giai đoạn nào.
2. **Transition (Bước chuyển):** là các hành động để kết nối hay chuyển công việc đó từ trạng thái này sang trạng thái khác.

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXfZaQrnjM1RvZMdtlbOD9qn71rhGNVecOtHLUZ7tSqmc-r-fqJlo7DlgZgDxfwPlE19s4DoADuE43aoSYirPEZkUAbQ7ky8ueiXmx4KrNA7D7Daa5ouIFbVEZznLPnx56wj2RUoaUK-P3pgizYr-F-TAFU?key=4y3BlDYugpQrPp29TmS3tA" alt=""><figcaption></figcaption></figure>

Người dùng có thể dễ dàng kéo thả và tạo ra các status, transition và workflow này phù hợp với quy trình công việc theo nhu cầu của mình, giúp người dùng dễ dàng trong việc quản lý, nắm rõ công việc:

* Thể hiện trực quan, rõ ràng các bước trong tiến trình, rõ ràng các bước trong tiến trình, giúp nhân sự nhìn vào nhìn vào hiểu được đường đi nước bước, cách làm của công việc
* Khi vào việc thực tế thì cũng làm việc trên tiến trình đó, làm đến đâu chuyển trạng thái đến đó để người làm, người liên quan và quản lý đều nắm được công việc đang diễn ra như thế nào.

Cập nhật bản hướng dẫn workflow mới nhất: [https://docs.google.com/document/d/1LlCA4V55pozZfRfbYqTv0RybN-1QpuCzqd6ZBrIxcJg/edit?usp=sharing](https://docs.google.com/document/d/1LlCA4V55pozZfRfbYqTv0RybN-1QpuCzqd6ZBrIxcJg/edit?usp=sharing)

**b. Custom field (trường dữ liệu):**

Khi thực hiện một công việc sẽ cần nhiều thông tin dữ liệu đi kèm với nó. LukLak cho phép người dùng tự tạo trường dữ liệu này gán vào các Issue Type (loại mục) khác nhau.

Luklak có 14 loại trường dữ liệu sau:

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXeNsjHqahrFjpYeaNGvnhsuzKL2LnTUCH2r10z9H-SNLmm9JFKQSgTyMGZYjJL_K_yDOUZE-gJVS7qW_EkC_UG6dOjqLMdLvsNMfpjvymOPSQ3ldKR0au28XdfCnjoxYtI1NFS76PIXFZbUfH5R5Bb575A2?key=4y3BlDYugpQrPp29TmS3tA" alt=""><figcaption></figcaption></figure>

#### Automation

Hướng dẫn sử dụng: [Tại đây](https://docs.google.com/document/d/1kyEoD-649B4sPiSSKlQTTOCRibRpfO41iWg1ePqDe7Q/edit#heading=h.35y7vexh9d31)

#### Vai trò

Sử dụng vai trò tương tự các chức danh trong công ty

**Ví dụ:** Trưởng phòng, Kiểm soát viên... Người nắm giữ vai trò có thể thay đổi, nhưng quyền của vai trò trong từng mảng việc vẫn cố định.

Vai trò sẽ được thêm vào các khu vực và mảng việc dùng để cấp quyền và thông báo cài đặt.

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXfFm7-1Swic0N-sKhhDQOIDKBMcMtHUbNdvL4i8g5Ejlzuh3Li7bfL-01DQz7KKzygguq0SPB4fV5XPyFY1d_51C57hMp4_2-4f90VO8H8sPDjY53DXixD7LsqQKZZEXzPvXExGxri0O90glTZlKftFUUk?key=4y3BlDYugpQrPp29TmS3tA" alt=""><figcaption></figcaption></figure>

#### Permission (phân quyền)

Các chức năng công việc trong công ty không bao giờ là mặc định mọi người trong công ty đều xem được tất cả các thông tin đó.

Nếu bình thường các phần mềm phổ thông chỉ có 3 mức phân quyền đơn giản nhất là các quyền: xem, sửa, xóa thì Luklak cung cấp khả năng phân quyền cực kỹ lưỡng sâu rộng, tách riêng thành hơn 20 sự kiện phân quyền như dưới đây, và người dùng hoàn toàn tự chủ - thay đổi và lựa chọn các mức độ khác nhau tinh chỉnh để chi tiết của 20 mức phân quyền này, để tạo thành một bộ phương án phân quyền phù hợp với tính chất của một Chức Năng đang làm.

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXeIe2qMd3TLeRnEHgNusAtiggKy5oH4ajVrJQD-DE3HFA09WMRYWQKcMoTJk-coq_G9mlvoBxtFsfk99ihKz1AkGKGnIK42_ow5_PRjcQsPw5lKk_ihWW_3p-4sq1v9c0CzP3c3lUHzaLs2iFIYV0gbbEZ9?key=4y3BlDYugpQrPp29TmS3tA" alt=""><figcaption></figcaption></figure>

Mỗi quyền ở trên có thể cấp quyền chi tiết hơn cho những đối tượng người dùng muốn cấp.  Luklak cung cấp 3 nhóm cấp quyền:

* **Vai trò (role):** mỗi mảng việc tạo ra đều có 3 vai trò (role) là Member, Manager, Admin và sẽ gán các user vào các vai trò khác nhau này. Và khi bộ phân quyền cấp quyền qua vai trò (role) này thì các user tương ứng với vai trò đó sẽ nhận được quyền.
* **Nhóm (group):** một cách phân quyền rất phổ biến là thông qua các Nhóm (Group). Mỗi nhân sự tùy theo vị trí công việc sẽ được gán vào các nhóm nhất định, ví dụ như Nhóm Kinh Doanh, Kỹ Thuật,... Các nhóm này đã phân quyền sẵn ngay từ đầu vào nhiều khu vực/mảng việc khác nhau. Nên khi có một nhân sự mới thì không cần gán thủ công nhân sự đó vào mảng việc mà chỉ cần gán vào đúng nhóm của nhân sự đó thì tự động sẽ có quyền vào các mảng việc.
* **Người dùng (user):** thường ít dùng phổ biến vì sẽ mất nhiều thời gian nếu phân quyền trực tiếp cho từng nhân sự, đặc biệt là cấp cho nhân viên số lượng lớn, vào ra nhiều. Phân quyền thẳng vào User thường áp dụng với số lượng ít những nhân sự cấp cao.

3 đối tượng phân quyền ở trên khi gán vào thì sẽ có quyền trên toàn bộ mảng việc cũng như áp dụng với tất cả các mục (issue) trong mảng việc đó.&#x20;

Trong nhiều trường hợp, trong một mảng việc có nhiều mục (issue) sẽ có nhu cầu phân quyền chi tiết tới mức issue, nghĩa là một người A có thể xem được issue số 1,2,3 mà người đó trực tiếp liên quan, nhưng không xem được các issue 4,5,6.

Khi đó sẽ dùng các đối tượng phân quyền là Trường dữ liệu người dùng, Trường dữ liệu nhóm người dùng. Đây chính là các trường dữ liệu xuất hiện trên từng được định nghĩa bởi mỗi issue type.

Bên cạnh việc người dùng có thể tự tạo bộ phương án phân quyền, LukLak có 4 phương án phân quyền mặc định sau:

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXeswoS6BeceTWSU_-6m3cmDGcGoNo_tS74ZSM63H-w6S5Q--xM-6eqfoF4FyMemxhPMOe5XEHUkAN7ZoTPgzr0XHocxIuSvbDRQaDWmHo8yCvTjodt2mk0pELsiGNalMeR60onULCpdMrd3NthqIVE6B_A?key=4y3BlDYugpQrPp29TmS3tA" alt=""><figcaption></figcaption></figure>

Trong chức năng, bạn có thể chọn một phương án phân quyền (đã được định nghĩa chung cho tổ chức) và thêm chi tiết phân quyền khác tùy theo nhu cầu của bạn cho phương án phân quyền này.

#### Notification (thông báo)

Tính năng Thông Báo (notification) giúp những người dùng liên quan sẽ ngay lập tức nhận được thông báo, cập nhập về một việc gì đó đang diễn ra. Việc hoàn toàn chủ động định nghĩa được thông báo này là rất quan trọng:&#x20;

* Các thông tin quan trọng cần được nhận liên tục để kịp thời nắm bắt và xử lý công việc.
* Các thông tin không quan trọng không nên thông báo liên tục sẽ làm loạn, trôi mất thông tin quan trọng.

Notification của Luklak cung cấp khả năng tùy biến, định nghĩa chi tiết, người dùng có thể tạo một phương án thông báo mới,  tùy chỉnh chi tiết 13 sự kiện thông báo, gửi tới cho ai cụ thể:

![](https://lh7-us.googleusercontent.com/docsz/AD_4nXfucJlUZxSOkuh9giYOJ-WTXoKJvktE4wMAZ7EB8jEiggITqogMmAhud88Qty4s3-sIEBHRZRbHZ76H9YSxYAY_JgOUdmVf7F-F80e5KKAHbCmTGwRomNk5Pp5pf2m-BJMUrea7jbwe-lSFPcYBEMs6tOEy?key=4y3BlDYugpQrPp29TmS3tA)![](https://lh7-us.googleusercontent.com/docsz/AD_4nXfXX_Tbc9TbC2ppmJAa-S9Xbag7UmN6bSxpPwuwBY1iESpV_m671gI6hT-AHRI5UntZAVtpWWZC9InBAE0-l7pt9AdJHHryIuZCeWO-ysPzEE9AqShD4HDE9P9w0b_SLokvbjc3SMAnK_O9UziuUWM5mgQ?key=4y3BlDYugpQrPp29TmS3tA)

Sử dụng phương án thông báo để xác định ai nhận được thông báo gì trong từng mục, từng mảng việc của tổ chức.&#x20;

**Ví dụ:** chỉ những người là Người làm mới nhận thông báo khi có sự thay đổi ở mục. LUKLAK có 3 phương án thông báo có sẵn:

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXfDKk1os0x7X0yROduZfcyS6CWm4WAmN64P5TmlgWiljAxcGSYhzLD78SdS3RZWEhAh_LOu_SmVDSkdFaGZYL-CYWz4mrh0PBPW7XlAbQthNL9J_UmyUTnwMlSY-c9GgLBDYjjTDvZYmc82Ios_G74runJs?key=4y3BlDYugpQrPp29TmS3tA" alt=""><figcaption></figcaption></figure>

Trong Chức Năng, bạn có thể chọn một Phương án thông báo có sẵn và thêm chi tiết cho phương án thông báo này.

#### Thành viên (phân quyền chức năng):&#x20;

Phân quyền chức năng cho phép người dùng:

* Admin và Owner phân quyền cho nhân sự/nhóm quyền cấu hình Chức Năng trong phạm vi cho phép mà không cần cấp quyền Admin toàn hệ thống.
* Người dùng thành viên khi được cấp quyền có thể cấu hình, chỉnh sửa lại Chức năng.

\


Xem hướng dẫn chi tiết [TẠI ĐÂY](https://drive.google.com/file/d/19FgQmtnAL7pt2JzWxDE31D7nMT9aEbaO/view?usp=sharing)
