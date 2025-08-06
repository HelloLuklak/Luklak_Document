---
description: >-
  cái section này nói về issue type và được tổng hợp từ file 04 và chỉ file 04
  mà thôi, tất cả những gì nói về issue type ở file 04 đều ở trong này
hidden: true
---

# Universal Object

## Issue type (loại mục)

Mỗi function có các issue type khác nhau để quản lý các loại đối tượng thông tin khác nhau, mỗi đối tượng này có cấu trúc thông tin dữ liệu (custom field) khác nhau.

Ví dụ: issue type khách hàng, issue type đơn hàng

## Issue type (Loại mục)

Một Chức Năng (Function) là một “cục” tương đối lớn và vận hành trọn vẹn được một mảng việc nào đó, và nó thường được tạo nên bởi các quy chuẩn công việc cụ thể bên trong. Ví dụ với Chức Năng (Function) Quản Lý Nhân Sự thì có thể chia thành quản lý các thứ cụ thể bên trong như sau:

* **Hồ sơ nhân sự:** lưu trữ toàn bộ các thông tin về một nhân sự như họ tên, ngày sinh, cấp bậc, vị trí,mức lương…
* **Hội nhập nhân sự mới:** khi chốt một nhân sự mới tuyển, sau khi tạo và lưu hồ sơ nhân sự như ở trên thì sẽ đi qua một tiến trình hội nhập nhân sự mới, phối hợp giữa bộ phận nhân sự và phòng ban liên quan
* **Thủ tục nhân sự nghỉ:** khi nhân sự nghỉ thì cũng trải qua một tiến trình, quy trình thực hiện các thủ tục nghỉ việc cho nhân sự.
* **Tình huống nhân sự phát sinh:** một phần thường xuyên của chức năng quản lý nhân sự đó là nhận diện, quản lý và xử lý các tình huống nhân sự phát sinh, ví dụ như mâu thuẫn va chạm nhân sự, tinh thần thái độ làm việc…
* **Các vấn đề đề xuất nhân sự:** nhân sự cũng thường có các đề xuất / request khác nhau, ví dụ như tăng lương, thăng tiến, đánh giá…

Thì mối một vấn đề, quy trình, quy chuẩn đó sẽ tương ứng với một Issue Type (Loại mục), có thể hiểu là nó là một loại việc. Đến lượt nó, Issue Type lại chứa trong nó các thuộc tính khác nhau có thể định nghĩa, thay đổi để đáp ứng một loại công việc riêng. Và tất nhiên, người dùng dễ dàng tự tạo ra các Issue Type .

Về cơ bản một issue type sẽ được định nghĩa bởi 2 thuộc tính:

* **Workflow:** là quy trình, tiến trình, quy chuẩn các bước thực hiện công việc đó.
* **Custom field:** là các thông tin dữ liệu cần thiết về công việc đó.

Workflow & custom field cũng chính là 2 trong số  tính năng cơ bản cốt lõi - các miếng lego phổ quát của Luklak, được mô tả kỹ hơn ở bên dưới.

Và ở đây, trong ví dụ về Chức Năng (Function) Quản Lý Nhân Sự, thì chúng ta sẽ lấy ví dụ về Issue type (loại mục) là Employee (Hồ sơ nhân sự) để lấy ví dụ minh hoạ cụ thể tiếp bên dưới.

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXcwZYBPmlfFVTqGXzacoFY4Y4hhCo0GGuB1pXw2xEr1Gcrrvyeo6DAahzV7dCkmAUOq72RXIOYvfC57-rt_SU4gZOSiexvV7QpU9R3i4mZQ_iaO6udAqbceK67MUNTYzmRhB9ZTk49yFJj94jwnDpoVCEGD?key=hX9TPFw-xpFJ1U1j27Vlqg" alt=""><figcaption></figcaption></figure>

### Issue (mục)

Với mỗi issue type sẽ tạo nhiều issue (mục), mỗi mục là một bản ghi với cấu trúc dữ liệu giống nhau, được định nghĩa bởi các column.

Ví dụ:

\- issue type "khách hàng" có các issue "Khách A", "Khách B", "Khách C"...

\- issue type "đơn hàng" có các issue "Đơn 1", "Đơn 2", "Đơn 3"

### Issue type là tầng thứ 3 của cấu trúc

* Trong một space (mảng việc)sẽ chia bên trong thành các issue type (loại mục).
* Trong mỗi issue type đó lại có thể định nghĩa tùy biến được các custom field (trường dữ liệu), có thể được dùng để chia tiếp - phân loại thành tầng 4 của cấu trúc tổ chức công việc.

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXfkNof0VMVxww2WXRtAfqRworUrIQnlfe3VCivEpR3VKbiiWk9jbnWRTfX-9ZdYbACOZkRE-PqHnlXcW92uuaukBMEJvSsiaGu6rj7tW_JGN2PB_Io0_xNvirsgWzpV9YAVJmN2uu_vq3xNXcDfYkrxP2cE?key=hX9TPFw-xpFJ1U1j27Vlqg" alt=""><figcaption></figcaption></figure>

Ví dụ với hình ở trên:

* Ở cấu trúc cứng, đang mở cấp 2 là space "Quản lý thời gian" -&#x20;
* Bottom bar sẽ hiện lên cấp 3 đó là các issue type (loại mục) bên trong, cụ thể có 5 loại:

1. Vắng mặt
2. Tình huống
3. Nghỉ ngày
4. Công tác
5. Tăng ca

### Sức mạnh tính năng nằm ở issue type

So sánh để hiểu rõ hơn thì:

* Nếu trên máy tính thì cấu trúc folder (thư mục) được tổ chức theo cấu trúc hình cây mẹ - con, mang tính chất là container (bộ chứa)  các file (tệp tin), bản thân folder không hề mang dữ liệu, mà dữ liệu chỉ có ở các file.
* Tương tự, area/ space (cấu trúc tầng 1-2) của luklak chỉ mang tính là bộ chứa các issue, area/ space không hề định nghĩa được dữ liệu, tính năng mà chỉ có issue mới làm được điều đó.

Issue là đơn vị cơ bản - cốt lõi của toàn hệ thống luklak, nó được gọi là universal data unit/ universal object và mọi thứ đều được xây dựng trên issue:&#x20;

* Một **task** công việc trong chức năng work management cũng là một issue.
* Một **contact** khách hàng trong CRM cũng là 1 issue.
* Một **applicant** hồ sơ ứng viên trong quản lý tuyển dụng cũng là 1 issue.

Với mỗi loại issue type như ở trên thì sẽ tùy biến, điều chỉnh các cấu hình dưới đây để tạo ra các chức năng, dữ liệu, workflow khác nhau:

* **Workflow (tiến trình):** định nghĩa chu trình, tiến trình, quy chuẩn của việc đó - issue type đó chạy như nào, qua các bước nào, với các điều kiện ra sao.
* **Custom field (trường dữ liệu):** issue type đó chứa các trường thông tin dữ liệu tùy chỉnh nào để đáp ứng chức năng - nhu cầu công việc đặc thù đó.
* **Permission scheme (phương án phân quyền):** quy định những ai (user/ group/ role) sẽ được phép làm gì trên issue type đó.
* **Notification scheme (phương án thông báo):** tùy chỉnh xem những sự kiện gì diễn ra trên issue đó thì những ai (user/ group/ role) sẽ nhận được thông báo.
* **Automation (tự động hóa)** (tính năng này đang được phát triển) sẽ cho phép tự tùy biến kết nối những việc diễn ra trên issue đó và các issue khác, theo mô hình  event - condition - action để tạo ra chuỗi các hành động tự động trên nhiều issue khác nhau.

các tùy chỉnh về issue type này không làm riêng lẻ trên từng issue type, mà thực ra nó là một phần trong việc cấu hình function (chức năng) của luklak, thường là làm ở admin. một khi có function định nghĩa các chức năng, tính năng, dữ liệu hoạt động như nào thì từ đó có thể tạo - nhân bản ra nhiều space nằm trong các area khác nhau nhưng có chức năng, tính năng giống hệt nhau, theo đúng function mà space đó được tạo ra.

\


<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXfK9CccYPtwO8eHoFGoLNlONLl1XZGg84wn0js2L7s6ADK9R9IHz9XDQaK17-vv4g1xbuWM6SEgoWNHNU0p9YkixA8Zyi__yeu4cP3TuXCT7baBtrPqzoRIK5hKyl1P20UX3xh9nFeZVzEkjQTUfQfgAXk?key=hX9TPFw-xpFJ1U1j27Vlqg" alt=""><figcaption></figcaption></figure>

\


\
