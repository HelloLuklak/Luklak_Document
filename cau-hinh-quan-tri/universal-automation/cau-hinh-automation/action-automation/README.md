# Action (Automation)

![](<../../../../.gitbook/assets/image (193).png>)

<figure><img src="../../../../.gitbook/assets/image (469).png" alt=""><figcaption></figcaption></figure>

### giới thiệu chung

#### tính chất chung

* tùy biến nội dung email
* gửi webhook/ http request
* gửi tin nhắn zalo gửi tin nhắn sms\


Một automation rule sau khi đã chạy qua bước trigger & condition sẽ lọc ra danh sách các mục dữ liệu (issue), và đưa vào thực hiện các hành động tự động (automated action).

Các hành động là cực kì đa dạng và phong phú, cho phép đáp ứng nhiều tính năng và nhu cầu sâu rộng.

Luklak với universal object (xem thêm tại [UNIVERSAL OBJECT FOR NOCODE &](https://www.notion.so/UNIVERSAL-OBJECT-FOR-NOCODE-LOWCODE-28d1a45d2ed249baa6df5c97ca17ff8d?pvs=21) [LOWCODE](https://www.notion.so/UNIVERSAL-OBJECT-FOR-NOCODE-LOWCODE-28d1a45d2ed249baa6df5c97ca17ff8d?pvs=21) trở nên mạnh mẽ vượt trội so với các phần mềm thế hệ 2 mỗi chức năng lại tách rời rạc thành các app khác nhau. khi mọi chức năng, mọi dữ liệu được tạo ra trên luklak đều là từ một thực thể phổ quát là universal object và các hành động tác động vào các tính năng dữ liệu ứng dụng khác nhau đều phổ quát và dễ thực hiện mà không bị chia nhỏ thành nhiều hành động khác nhau.

#### 2 loại hành động

Nội trong hệ thống luklak: tạo các mục việc, dữ liệu cũng như cập nhật các thông tin, trạng thái trên đó; gửi các nội dung chat kênh chat, mục việc và chat riêng\


<figure><img src="../../../../.gitbook/assets/image (574).png" alt=""><figcaption></figcaption></figure>

Kết nối tương tác với phần mềm ngoài: kết nối với các ứng dụng trao đổi giao tiếp như zalo, email, sms… và kết nối dữ liệu với các phần mềm khác qua webhook, api

<figure><img src="../../../../.gitbook/assets/image (573).png" alt=""><figcaption></figcaption></figure>

## Các action trong luklak

### Tạo mục tiêu chuẩn / create issue 

<figure><img src="../../../../.gitbook/assets/image (575).png" alt=""><figcaption></figcaption></figure>

Tạo mới mục việc/ dữ liệu mới và cập nhật các trường thông tin của nó

Chọn mảng việc (space) nơi sẽ chứa mục việc mới được tạo ra và điền các thông tin cơ bản như tiêu đề, mô tả

Chuyển sang tab THÔNG TIN NÂNG CAO để cập nhật, tính toán các trường dữ liệu điền vào mục mới tạo ra. phần cập này sẽ được mô tả cụ thể ở hành động update field bên dưới.

Ở đây sẽ thấy các trường text như tiêu đề, mô tả ngoài việc nhập text cố định đơn giản vào thì có thể tự động lấy các giá trị khác nhau trên hệ thống (smart value) để điền vào một cách linh hoạt, ví dụ như Đơn hàng của

${issue.assignee} tạo ngày ${issue.duedate} .&#x20;

chi tiết về cách cài đặt giá trị các trường xem ở phận action cập nhật trường bên dưới.

<figure><img src="../../../../.gitbook/assets/image (576).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../../.gitbook/assets/image (577).png" alt=""><figcaption></figcaption></figure>

### Cập nhật dữ liệu/ update field

<figure><img src="../../../../.gitbook/assets/image (81).png" alt=""><figcaption></figcaption></figure>

Trên các mục việc/ dữ liệu (issue) đều có sẵn các trường thông tin hệ thống (system field) và các trường do người dùng tự định nghĩa (custom field), và hành động ở đây sẽ chọn các trường dữ liệu đó ra để cập nhật.\


<figure><img src="../../../../.gitbook/assets/image (578).png" alt="" width="364"><figcaption></figcaption></figure>

Ngoài việc nhập thẳng các giá trị thông tin vào các trường thì luklak automation cho phép lấy thông tin từ nhiều dữ liệu khác nhau, biến đổi giá trị đó theo các công thức rồi điền vào (smart value). dưới đây là một số ví dụ.

#### Nguồn dữ liệu smart value

Smart value sẽ cho phép lấy dữ liệu từ:

Mục kích hoạt hành động (trigger issue) là issue mục đã phát ra các trigger event khởi chạy một automation rule. (xem thêm tại [TRIGGER FOR ](https://www.notion.so/TRIGGER-FOR-AUTOMATION-496f742f4cda4dafb0196639f4566d29?pvs=21) [AUTOMATION](https://www.notion.so/TRIGGER-FOR-AUTOMATION-496f742f4cda4dafb0196639f4566d29?pvs=21). một hành động tạo issue mới có thể lấy các giá trị từ trigger issue để điền vào

Mục cha (parent issue): lấy dữ liệu từ mục cha để điền vào mục con\
Mục hiện tại (current issue): khi ở trong một vòng lặp rẽ nhánh (branching) thì sẽ thực hiện với danh sách nhiều issue liên tục, thì current issue là issue hiện tại đang được xử lý.

Mục đích đến (target linked issue): khi kết nối (link issue) từ Mục A sang Mục B thì B là mục đích đến, và có thể gọi giá trị từ mục đó ra.

Từ các nguồn dữ liệu / issue kể trên, có thể lấy ra các trường thông tin dữ liệu (sysmtem field, custom field) để tính toán và điền vào các trường cần cập nhật.

\


<figure><img src="../../../../.gitbook/assets/image (580).png" alt=""><figcaption></figcaption></figure>

Một số ví dụ về việc tính toán, biến đổi dữ liệu smart value để cập nhật vào trường thông tin

Text field

<figure><img src="../../../../.gitbook/assets/image (583).png" alt=""><figcaption></figcaption></figure>

\


Number field

<figure><img src="../../../../.gitbook/assets/image (584).png" alt=""><figcaption></figcaption></figure>

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXcFQib53HxgMVl5zVujAtpcyPigWmGHrq3DGzt1mt1duXhpJgMTYKQ5lO30pDxBWBEOAbvoYRxuh-FN793KxIbe_hDHaH9zc8uLzAvdn7whZDEcN97kRVJDbHASGcFisb1EgArCvUYm3MwU7ZIK2O5XS5qeBvSa5lP_ZguJJQBx-2FiSjnWCQ?key=c73gA89g4qTngtb38YIV-A" alt=""><figcaption></figcaption></figure>

Date field

Chọn nguồn hoặc cách xác định giá trị trường ngày tháng

<figure><img src="../../../../.gitbook/assets/image (585).png" alt=""><figcaption></figcaption></figure>

Tính toán biến đổi giá trị dựa trên nguồn dữ liệu đã chọn ở trên. khi chọn chế độ giá trị tính toán thì tất cả các giá trị ngày/ giờ/ phút đều được tính cộng/ trừ dựa trên dữ liệu nguồn. nếu chọn chế độ giờ nhập tay thì chỉ có trường ngày được +/- trên nguồn dữ liệu, còn giờ/ phút sẽ được nhập tay cố định. chế độ giờ nhập tay hữu ích khi muốn đặt: giá trị ngày biến đổi - ví dụ 2 ngày sau đó; còn giá trị giờ/ phút luôn cố định - ví dụ luôn bắt đầu lúc 9h:00 sáng.

Còn linh hoạt và thấu đáo đến mức cho phép lựa chọn bỏ ngày thứ 7/ chủ nhật ra khỏi tính toán nếu đó không phải là ngày làm việc.\


<figure><img src="../../../../.gitbook/assets/image (586).png" alt=""><figcaption></figcaption></figure>

### Tạo mục con/ create sub-issue

**Universal object** [UNIVERSAL OBJECT FOR NOCODE & LOWCODE](https://www.notion.so/UNIVERSAL-OBJECT-FOR-NOCODE-LOWCODE-28d1a45d2ed249baa6df5c97ca17ff8d?pvs=21) của luklak sẽ hữu hành hóa thành standard issue type (loại mục tiêu chuẩn) và sub- issue type (loại mục con). sub-issue type luôn nằm dưới một standard issue type nào đó, kiểu như các subtask nằm dưới task vậy.

Action này cho phép tạo một loạt các mục con, kiểu như subtask hoặc các loại mục con khác được người dùng định nghĩa.

Ngoài màn hình tạo hàng loạt sub-issue như hình dưới, thì cấu hình cho các sub-issue mới được tạo ra thì cũng được cấu hình tương tự như action tạo issue mới ở trên (click vào icon setting ở bên phải của mỗi sub-issue để mở ra cấu hình)\


<figure><img src="../../../../.gitbook/assets/image (587).png" alt="" width="563"><figcaption></figcaption></figure>

<figure><img src="../../../../.gitbook/assets/image (588).png" alt="" width="476"><figcaption></figcaption></figure>

<figure><img src="../../../../.gitbook/assets/image (589).png" alt="" width="467"><figcaption></figcaption></figure>

### Tạo mục kiểm/ create checklist

Tạo mục kiểm / checklist bên trong một mục dữ liệu (issue) nào đó

<figure><img src="../../../../.gitbook/assets/image (590).png" alt="" width="472"><figcaption></figcaption></figure>

### Chuyển trạng thái/ change workflow status

Mỗi mục việc/ dữ liệu (issue) đều đi kèm một workflow phổ quát trong đó (xem thêm [UNIVERSAL WORKFLOW](https://www.notion.so/UNIVERSAL-WORKFLOW-eddca49d717c4225a6fca8303325bfde?pvs=21), trong đó định nghĩa:

Các status thể hiện tình hình, trạng thái của đầu việc\


Các transition là đường nối giữa các trạng thái với nhau, quy định tiến trình, thứ tự, các đường đi từ status này sang status khác.

<figure><img src="../../../../.gitbook/assets/image (591).png" alt="" width="266"><figcaption></figcaption></figure>

Hành động này cho phép tự động chuyển trạng thái của một mục dữ liệu (issue) từ trạng thái X sang trạng thái Y.

Có 3 cách chuyển trạng thái như hình dưới đây, tương đỗi rõ ràng dễ hiểu:

Chọn một trạng thái cụ thể đã được xác định trước

Nhảy bước: các trạng thái trong một workflow đều được đánh số thứ tự tăng dần, theo chiều dọc từ trên xuống. cách này cho phép nhảy bước 1,2, 5… bước) tính từ trạng thái hiện tại.

Sao chép từ mục: cho phép lấy giá trị trạng thái của mục khác để điền vào trạng thái mục đang xử lý.

### Kết nối mục/ link issue

Issue linked (kết nối mục) là tính năng rất mạnh của luklak:

Cho phép tạo ra các liên kết (link) giữa các mục việc khác nhau & có liên quan đến nhau để tạo ra bức tranh tổng thể rộng lớn hơn.

Các mục cụ thể như là các điểm (dots), và link sẽ như là connection. sự sáng tạo chính là connection the dots. khi có cả dots và connection như vậy sẽ tạo nên khả năng linh hoạt sáng tạo sâu rộng để tạo ra các chức năng đa dạng mạnh mẽ cho người dùng, doanh nghiệp

Hành động link issue này sẽ cho phép tạo sự kết nối từ issue đang xử lý sang issue khác, thể hiện sự liên quan và tạo ra bức tranh tổng thể lớn hơn.

Có 4 lựa chọn xử lý các giá trị kết nối như hình dưới đây:\


<figure><img src="../../../../.gitbook/assets/image (592).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../../.gitbook/assets/image (593).png" alt=""><figcaption></figcaption></figure>

#### Chọn giá trị cụ thể

Cho phép lọc và chọn ra các mục dữ liệu cụ thể và cố định để kết nối vào.

Loại mục nguồn: vì mỗi loại kết nối (link type) đều được định nghĩa rõ ràng loại mục nguồn & loại mục đích, nên việc đầu tiên luôn phải xác định loại mục nguồn. các link type này được cài đặt ở trong admin.

Loại kết nối: khi đã xác định được loại mục nguồn ở trên, thì có thể xổ xuống chọn những loại kết nối (link type) khả dụng với loại mục nguồn đó.

Mục kết nối: sau khi đã xác định loại mục nguồn, loại kết nối thì sẽ xổ xuống hiện ra danh sách các mục dữ liệu (issue) cụ thể khả dụng, và chọn một hoặc nhiều issue đó để tạo kết nối.

<figure><img src="../../../../.gitbook/assets/image (594).png" alt="" width="455"><figcaption></figcaption></figure>

#### Dùng bộ lọc mục (issue filtering) 

Các tùy chọn về Loại mục nguồn & Loại kết nối là đều giống như như phần ở trên, sự khác nhau chỉ nằm tùy chọn cuối cùng, ở đây là “Tiêu chí lọcˮ.

Ở đây dùng ngôn ngữ truy vấn dữ liệu của luklak là NQL  Natural Query Language (xem thêm tại [UNIVERSAL OBJECT FOR NOCODE & LOWCODE](https://www.notion.so/UNIVERSAL-OBJECT-FOR-NOCODE-LOWCODE-28d1a45d2ed249baa6df5c97ca17ff8d?pvs=21) để lọc ra ra các mục thỏa mãn điều kiện, dựa trên điều kiện của các trường dữ liệu cụ thể.

Tất cả các mục được lọc ra đó đều sẽ được tạo kết nối tới mục đang xử lý.

<figure><img src="../../../../.gitbook/assets/image (595).png" alt="" width="462"><figcaption></figcaption></figure>

<figure><img src="../../../../.gitbook/assets/image (596).png" alt="" width="505"><figcaption></figcaption></figure>

#### Sao chép từ mục

Lựa chọn các mục khác như hình, rồi sao chép toàn bộ giá trị issue link từ mục đó vào mục đang xử lý, bao gồm cả loại kết nối, và mục đích được kết nối đến.\


<figure><img src="../../../../.gitbook/assets/image (598).png" alt="" width="463"><figcaption></figcaption></figure>

#### Xóa kết nối mục

Các hành động trên đều là tạo issue link mới, còn riêng hành động này là lọc ra và xóa các issue link cụ thể nào đó.

Các tùy chọn ở đây cũng rõ ràng, tương tự như ý đã được diễn giải ở trên.

<figure><img src="../../../../.gitbook/assets/image (599).png" alt="" width="467"><figcaption></figcaption></figure>

<figure><img src="../../../../.gitbook/assets/image (600).png" alt="" width="500"><figcaption></figcaption></figure>

### Gửi tin nhắn chat 

Tất cả các action bên trên đều là xử lý các issue và các thông tin dữ liệu nằm trong issu. action này khác hoàn toàn, khi nó không phải là xử lý thay đổi dữ liệu, mà là gửi tin nhắn chat trao đổi.

Luklak có 3 tầng chat thì hành động này có thể gửi được vào cả 3

**Chat đầu việc:** chính là live chat trao đổi trực tiếp, tức thời trên từng issue. chat trên issue giữ cho cả thông tin dữ liệu có cấu trúc của công việc đó và thông tin phi cấu trúc chat trao đổi hợp nhất thông suốt ở một nơi. tránh tình trạng thông tin công việc ở một nơi, xong chat trao đổi lại chuyển qua nơi khác (app chat khác, nhóm chat chỗ khác)

**Kênh chat mảng việc:** chính là chat trao đổi các vấn đề chung theo cấu trúc khu vực, mảng việc, bộ phận phòng ban. cái này tương đương với các ứng dụng chat chuyên sâu dành cho doanh nghiệp, như slack và microsoft teams. các doanh nghiệp sâu rộng, nhiều công việc khác nhau thì cần có các kênh chat có cấu trúc như này. còn các phần mềm chat cá nhân miễn phí như zalo, messenger, telegram không có khả năng tổ chức tốt, chỉ có chat nhóm và chat 11, sẽ nhanh chóng lụt trong thông tin

**Chat riêng:** là chat với các cá nhân mà không nằm trong bối cảnh công việc này, bao gồm chat 11 và group chat. phần này của luklak tương đương với các phần mềm chat cá nhân miễn phí như zalo, messenger, telegram; cũng tương đương với các app chat được cung cấp trong bộ nhiều phần mềm thế hệ 2 như misa, base, 1office (cũng chỉ có chat 11 & group chat rời rạc, không nằm trong bối cảnh & cấu trúc công việc)\


<figure><img src="../../../../.gitbook/assets/image (601).png" alt=""><figcaption></figcaption></figure>

#### Gửi vào đầu việc

Sổ xuống và tìm chọn đầu việc (issue) cụ thể để gửi tin nhắn chat vào đó.

<figure><img src="../../../../.gitbook/assets/image (602).png" alt="" width="431"><figcaption></figcaption></figure>

#### Gửi vào kênh chat mảng việc

Sổ xuống và tìm chọn mảng việc (space) cụ thể để gửi tin nhắn chat vào đó\


<figure><img src="../../../../.gitbook/assets/image (603).png" alt="" width="428"><figcaption></figcaption></figure>

#### Gửi vào chat riêng

Chat riêng gửi tới 1 user hoặc nhóm chat nào đó, và có khá nhiều tùy chọn với dữ liệu thay đổi linh hoạt như hình dưới đây.\


<figure><img src="../../../../.gitbook/assets/image (604).png" alt="" width="470"><figcaption></figcaption></figure>

**Người:** có thể chọn người cụ thể nhất định, hoặc lấy smart value là các user field linh hoạt từ mục kích hoạt\


&#x20;![](<../../../../.gitbook/assets/image (605).png>)![](<../../../../.gitbook/assets/image (606).png>)

**Nhóm:** là tạo và gửi tin nhắn vào group chat, group chat trong phần Chat riêng này sẽ bao gồm các user được lấy ra từ các Nhóm cụ thể (các user group cài đặt ở admin) hoặc các trường thông tin dạng nhóm (group picker field) là smart value lấy từ mục kích hoạt (trigger issue)

<figure><img src="../../../../.gitbook/assets/image (607).png" alt=""><figcaption></figcaption></figure>

Tùy biến nội dung chat\


không chỉ là gửi một tin nhắn chat cố định cụ thể nào đó, mà luklak automation cho phép xử lý nhiều smart value để tạo ra các nộidung chat thay đổi linh hoạt với dữ liệu thay đổi tương ứng.

có **3 loại tùy chọn** để chèn các dữ liệu smart value vào nội dung chat như ảnh dưới.

<figure><img src="../../../../.gitbook/assets/image (608).png" alt="" width="464"><figcaption></figcaption></figure>

<figure><img src="../../../../.gitbook/assets/image (609).png" alt=""><figcaption></figcaption></figure>

**Nhắc đến người (mention user)** sẽ chọn những người cụ thể, và người đó sẽ nhận được thông báo (notification) nổi bật. có thể chọn người cụ thể, hoặc chọn smart value tư động lấy giá trị là các trường user field từ mục kích hoạt (trigger issue)\


<figure><img src="../../../../.gitbook/assets/image (610).png" alt=""><figcaption></figcaption></figure>

**Trường dữ liệu** (system field & custom field): chọn nguồn dữ liệu là mục kích hoạt (trigger issue) hoặc mục cha (parent issue) rồi chọn các system field & custom field trên đó

<figure><img src="../../../../.gitbook/assets/image (611).png" alt="" width="332"><figcaption></figcaption></figure>

**Đường dẫn**: chèn tên cũng như đường link dẫn tới các mục kích hoạt hành động (issue), mảng việc (space) kích hoạt hành động (space), hoặc khu vực (area) kích hoạt hành động.\


<figure><img src="../../../../.gitbook/assets/image (612).png" alt="" width="341"><figcaption></figcaption></figure>

### Các action ra bên ngoài

Ở phần trên là các hành động tác động vào các đối tượng đa dạng bên trong hệ thống luklak. dưới đây sẽ là các hành động kết nối ra ngoài, tác động vào các phần mềm, ứng dụng bên ngoài luklak.

### Gửi email

<figure><img src="../../../../.gitbook/assets/image (473).png" alt=""><figcaption></figcaption></figure>

Gửi email tới một địa chỉ email bất kì bên ngoài, với tiêu đề và nội dung có thể tùy biến thay đổi sử dụng smart value là các dữ liệu phát sinh và có trên hệ thống.\


Chọn người nhận email

Ngoài việc nhập địa chỉ email cụ thể định trước, thì smart value cho phép tùy biến tự điền các giá trị email linh hoạt hay đổi như hình ở dưới.\


<figure><img src="../../../../.gitbook/assets/image (613).png" alt="" width="481"><figcaption></figcaption></figure>

<figure><img src="../../../../.gitbook/assets/image (614).png" alt=""><figcaption></figcaption></figure>

**Email:** nhập email cụ thể, hoặc tự động lấy các trường email field từ mục kích hoạt (trigger issue)

<figure><img src="../../../../.gitbook/assets/image (616).png" alt=""><figcaption></figcaption></figure>

**Người (user):** tự động lấy địa chỉ email của các user, có thể là user cụ thể hoặc các user field từ mục kích hoạt (trigger issue)\


<figure><img src="../../../../.gitbook/assets/image (617).png" alt=""><figcaption></figcaption></figure>

**Nhóm (group):** lấy địa chỉ email của các user nằm trong group nào đó, có thể là group cụ thể được cài đặt trong admin, hoặc trường dữ liệu group picker field của mục kích hoạt hành động (trigger issue)

<figure><img src="../../../../.gitbook/assets/image (618).png" alt=""><figcaption></figcaption></figure>

**vai trò (role):** role là một tính năng khá đặc biệt được cài đặt trong các mảng việc (space) để thể hiện tính chất công việc và cài đặt cấp phân quyên (permission) và gửi thông báo (notification) tùy biến theo từng vai trò khác nhau. ở đây sẽ tự động lấy email của các user được gán vào role được chọn.\


<figure><img src="../../../../.gitbook/assets/image (619).png" alt=""><figcaption></figcaption></figure>

**Thành phần mảng việc (space component):** component là một tính năng đặc biệt dùng để phân loại, phân chia các mục dữ liệu (issue) trong đó thành các phần, loại, tính chất khác nhau. mỗi component (thành phần) của space sẽ được gán các user vào làm trưởng phần/ thành viên phần. ở đây sẽ lấy email của các user được gán vào trưởng phần/ thành viên phần được lựa chọn.

<figure><img src="../../../../.gitbook/assets/image (620).png" alt=""><figcaption></figcaption></figure>

#### Tùy biến nội dung email

![](https://lh7-us.googleusercontent.com/docsz/AD_4nXfV9Zv2EMwEiSTyB46GjvxA3O-Vj8YoZcBmgWApnE1YtKmhAHYtpzqeItk1dg-vPjGbQ32oGftn8UkoU6dPfWhYByKyDp6DiGhOno-b7yXyLZ2BUJFHzp3wB0U53LQ7614xulrHg6R_coEqLFqN3o4OKLsS2Fk5g0kWKcBs1MGuJLS_EKsPdqI?key=c73gA89g4qTngtb38YIV-A) Không chỉ là gửi một tin nhắn email cố định cụ thể nào đó, mà luklak automation cho phép xử lý nhiều smart value để tạo ra các nộidung email thay đổi linh hoạt với dữ liệu thay đổi tương ứng.

![](https://lh7-us.googleusercontent.com/docsz/AD_4nXd8UR3DBh0g6OGDtiexpjZ5psr-t52sbr2yYmfBbR5ro0Y6eFHBQu-n47vAGpuTG4NPq3JeVH2wG-VNfoGKkUs5hOfiMr_dX7FXaazdiGTDtDTRrlGe5hUgY36DOrIRbsgFM2O9nrg5w0OUSa70nDVCkLsYAJSjD8MlsN1WSyj1BTfxRuT0cm4?key=c73gA89g4qTngtb38YIV-A) Nhìn chung cấu hình tùy biến nội dung email email rất giống với cấu hình tùy biến nội dung chat ở phần trên, vui lòng kéo lên để xem. so với phần chat thì gửi email sẽ:

![](https://lh7-us.googleusercontent.com/docsz/AD_4nXd_GOITtEuV1MLUtcO9y8EVBufkUC7PXYE6ONMga0sAdgdlKlCeQsDvzIT6oT9m0cQ39rRPCMXovitIqNiOKQvDbS_S_bvXm6P8K2AA-HjVbcOuWip0OIPoj8QsQ8IiC_uct2C9i5AW_wM1ZfysGyeR3H86GpTUe-ZA0aKA2Ow4A860XvOkgQ?key=c73gA89g4qTngtb38YIV-A)  Không có phần Nhắc đến người

![](https://lh7-us.googleusercontent.com/docsz/AD_4nXfOm-pgCCvk-KWm14B7yxMMQthQxkkBS4wa4hKNUljLfnBmT-2mLf8UAY-zI-S3JZt2n8B5SezrjGbXKoEjqc5G5t2El94dt6I-jTAxLB1TXCjPRgHRnucqLZo5hzc1h3xFHje6ykEKnEOqcLOTN18ZhdtyizKUpvQYzlRl7P_dLjlwcYuoFGw?key=c73gA89g4qTngtb38YIV-A) Còn phần cài đặt Trường dữ liệu & Đường dẫn vào nội dung email là như ở phần cài đặt chat.\


<figure><img src="../../../../.gitbook/assets/image (621).png" alt=""><figcaption></figcaption></figure>

\


<figure><img src="../../../../.gitbook/assets/image (623).png" alt=""><figcaption></figcaption></figure>

### Gửi webhook/ http request

<figure><img src="../../../../.gitbook/assets/image (476).png" alt=""><figcaption></figcaption></figure>

có thể gửi webhook thẳng vào các phần mềm cụ thể bên ngoài

<figure><img src="../../../../.gitbook/assets/image (624).png" alt="" width="476"><figcaption></figcaption></figure>

Hoặc gửi vào n8n để từ đó kết nối tới rất nhiều ứng dụng đã được n8n tích hợp sẵn.\


<figure><img src="../../../../.gitbook/assets/image (625).png" alt="" width="563"><figcaption></figcaption></figure>

### **Functional Account / Tài khoản chức năng**

Markdown

```
functional-accounts.mdx
```

***

#### ENGLISH SOURCE

Functional Accounts: Secure, Auditable Automation

Why This Matters

Automations are powerful, but they must be reliable. If an automation rule is tied to a specific employee's User account, what happens when that person goes on vacation, changes roles, or leaves the company? The automation can fail, creating process gaps and security risks.

The Functional Account solves this. It's a secure, impersonal system entity that "owns" and executes automations, ensuring your business processes run continuously, securely, and with a clear audit trail, independent of any single user.

The Big Picture: Two Types of Executors

Every automation rule in Luklak must be "executed by" a specific account. This executor determines the rule's permissions and how its actions are recorded. You have two choices:

1. User Account: This is your personal account (e.g., `manager@company.com`). When an automation runs as you, it uses _your_ permissions. Any action it takes (like creating an `🧊 Object` or posting a message) will appear as if _you_ did it personally.
2. Functional Account: This is a technical, system-level account created specifically for executing automations. It has no password and cannot be used to sign in. Its permissions are configured by an administrator (P2-Architect) to ensure it has the _exact_ access needed for its job—no more, no less.

Here is a side-by-side comparison:

| **Feature** | **User Account**                                         | **Functional Account**                 |
| ----------- | -------------------------------------------------------- | -------------------------------------- |
| Identity    | Tied to a specific person.                               | A technical system entity.             |
| Execution   | Actions are logged as that user.                         | Actions are logged as "Automation".    |
| Permissions | Limited by that user's role.                             | Defined specifically for its tasks.    |
| Lifecycle   | Tied to employment. Fails if user is deactivated.        | Permanent. Independent of any user.    |
| Best For    | Personal, low-risk automations (e.g., "Remind _me_..."). | Business-critical process automations. |

Decision Guide: Which Executor Should You Use?

As a (P3-Manager) building a rule, follow this simple logic:

* Use a User Account when...
  * The automation is _for your personal benefit_.
  * Example: "When an `🧊 Object` is assigned to _me_, update its status to 'In Progress'." The action is explicitly tied to you as an individual.
* Use a Functional Account when... (Recommended)
  * The automation is part of a _team or company business process_.
  * Example: "When a new 'Sales Lead' `🧊 Object` is created, assign it to the next available agent."
  * This is a system-level action, not a personal one. Using a Functional Account ensures this rule _always_ runs, regardless of who built it or who is on the sales team.

Đoạn mã

```
# How to Select the Executor for Your Automation

This guide shows you where to select the executing account when building a new automation rule.

## Section 1: Finding the Executor Setting

! Important: You must have permission to build automations in the `⏹️ Space` or `📋 Function`.

1.  Navigate to the automation builder for your `📋 Function` or `⏹️ Space`.
2.  Create your **Trigger** (e.g., "When Object is Created").
3.  Create your **Action** (e.g., "Update Field").
4.  Look for the **"Execute As"** (or "Run as") configuration setting. This is typically near the top of the automation rule editor.
    ![A conceptual screenshot showing a dropdown labeled "Execute As" in the automation builder UI](https://example.com/placeholder-automation-executor.png)

## Section 2: Selecting the Account

1.  Click the "Execute As" dropdown.
2.  You will see two primary options:
    * **User Account** (Will show your name)
    * **Functional Account**
3.  **Select "Functional Account"** for all standard business process automations.
    * Tip: This ensures your automation remains active and secure even if your personal account permissions change.
```

What's Next?

* [Build Your First Automation Rule](https://www.google.com/search?q=https://claude.ai/chat/path/to/automation-builder)
* [Understanding Permission & Notification Schemes](https://www.google.com/search?q=https://claude.ai/chat/path/to/permissions)

***

### Tài khoản Chức năng: Tự động hóa Bảo mật & Có thể Truy vết

{% hint style="warning" %}
Tự động hóa rất mạnh mẽ, nhưng chúng phải đáng tin cậy. Nếu một quy tắc tự động hóa bị ràng buộc vào Tài khoản Người dùng của một nhân viên cụ thể, sẽ có nguy cơ tạo ra các lỗ hổng quy trình và rủi ro bảo mật.
{% endhint %}

{% hint style="success" %}
Tài khoản Chức năng giải quyết vấn đề này. Đó là một thực thể hệ thống bảo mật, phi cá nhân, dùng để thực thi các tự động hóa, đảm bảo các quy trình nghiệp vụ của bạn chạy liên tục, an toàn và có dấu vết kiểm toán rõ ràng, độc lập với bất kỳ người dùng đơn lẻ nào.
{% endhint %}

#### Bức tranh Toàn cảnh: Hai loại Tài khoản Thực thi

_Mọi quy tắc tự động hóa trong Luklak phải được "thực thi bởi" một tài khoản cụ thể. Tài khoản thực thi này xác định các quyền của quy tắc và cách các hành động của nó được ghi lại. Bạn có hai lựa chọn:_

1. Tài khoản Người dùng: Đây là tài khoản cá nhân của bạn (ví dụ: `giangnguyen@company.com`). Khi một tự động hóa chạy với tư cách là bạn, nó sử dụng quyền _của bạn_. Bất kỳ hành động nào nó thực hiện (như tạo `🧊 Object` hoặc gửi chat) sẽ xuất hiện như thể _chính bạn_ đã làm điều đó.
2. Tài khoản Chức năng: Đây là một tài khoản kỹ thuật, cấp hệ thống, được dùng để thực thi Tự động hóa với phân quyền bảo mật. Tài khoản này không có mật khẩu và cũng không thể dùng để đăng nhập hay làm việc được. Các quyền của nó được quản trị viên/chủ sở hữu định cấu hình để đảm bảo nó có quyền truy cập _chính xác_ cần thiết cho công việc của mình—không hơn, không kém.

Đây là bảng so sánh song song:

| **Tính năng** | **Tài khoản Người dùng**                                                                                                                                                                                | **Tài khoản Chức năng**                     |
| ------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------- |
| Định danh     | Gắn liền với một người cụ thể.                                                                                                                                                                          | Một thực thể kỹ thuật của hệ thống.         |
| Thực thi      | Hành động được ghi lại dưới tên người dùng đó.                                                                                                                                                          | Hành động được ghi lại là "Tự động hóa".    |
| Phân quyền    | Bị giới hạn bởi vai trò của người dùng đó. _Nếu quá ít quyền, không đủ để thực thi action. Nếu quá nhiều quyền, người cấu hình có thể vượt quyền để thực hiện một số hành vi nguy hại cho doanh nghiệp_ | Được xác định cụ thể cho các tác vụ của nó. |
| Phù hợp nhất  | Tự động hóa cá nhân, rủi ro thấp (ví dụ: "Nhắc _tôi_...").                                                                                                                                              | Tự động hóa quy trình nghiệp vụ quan trọng. |





\
