# Dành cho admin

### I, TỔNG QUAN VỀ SƠ ĐỒ TỔ CHỨC PHÒNG BAN (KHU VỰC VÀ MẢNG VIỆC)



Trên thực tế cấu trúc của đơn vị chính là cách tổ chức bộ phận, phòng ban, công việc để vận hành. Trên phần mềm là một sơ đồ mà đơn vị muốn xây dựng nhằm quản lý đơn vị một cách dễ dàng và thuận tiện. Trên luklak, sơ đồ tổ chức là các khu vực và mảng việc, mở rộng ra có thể là các phòng làm việc. Trực quan hơn thì có thể hiểu là 1 cấu trúc được thiết lập để chứa những dữ liệu đầu vào của người dùng, để có thể phân nhóm - phân loại sát nhất với thực tế. Không mất đi tính cụ thể phân loại công việc theo từng phòng ban vốn có, mà vẫn có tính linh hoạt để là nơi tương tác và phối hợp các công việc mang tính quy trình liên phòng ban một cách hiệu quả.

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXdDK3kmP7FnCN_ARBPI_E1YbaZMsKvhVcOs9jaey_Ll8k1sZdKPloz-77d_xtcvwgqkVsBs6XBi1klI_zLYm1aNp3DrvpQ1t3dzZyNETMUSDHXCzL4XA7pmRsdrWR047CG2dYO_mMC3R9CZ7SIOjNIlyE4b?key=ndEebUs8Ex2KSDzNZxJ3QA" alt=""><figcaption></figcaption></figure>

\


&#x20; Chi tiết hướng dẫn về tổ chức phòng ban: [Tại đây](https://docs.google.com/document/d/1YAYP-K9wiYwyVBuynEw0Dv6aYT9R0DJCkZgO6H2RzHE/edit?usp=sharing)

### II, HƯỚNG DẪN TẠO CHỨC NĂNG&#x20;

&#x20;          Chi tiết về hướng dẫn tạo chức năng: [Tại đây](https://docs.google.com/document/d/1YulUz20m6OQz3RVNMAd6v5ct-O42RgSf34a6gR5gYhE/edit?usp=sharing)

{% content-ref url="function/cau-hinh-function.md" %}
[cau-hinh-function.md](function/cau-hinh-function.md)
{% endcontent-ref %}

### III, CÁC TÍNH NĂNG PHÂN QUYỀN

Phân quyền trên Luklak được tổ chức chặt chẽ và sâu rộng, điều này giúp cho các tổ chức và đơn vị linh hoạt được các quyền hạn của từng thành viên trong phần mềm và chia nhỏ các thao tác thiết lập sử dụng đến từng người, tránh tình trạng mọi việc thiết lập dồn lên 1 vài người hoặc 1 nhóm người và tránh tình trạng khi người dùng sử dụng muốn thay đổi bất kỳ thông tin gì trên phần mềm lại bị thụ động và đi qua nhiều cấp bậc thiết lập. Hơn nữa việc phân quyền chặt chẽ sẽ giới hạn các thao tác mà người dùng được phép làm, tránh tình trạng bị lộ thông tin không liên quan, hoặc sửa xóa nhầm thông tin đang sử dụng.

Chi tiết về hướng dẫn phân quyền: [Tại đây](https://docs.google.com/spreadsheets/d/1NZHMfojjTCwTYkiv_U0fevmOAEI1Tdp2R1s54KhK__I/edit?usp=sharing)

### IV, BỘ LỌC VÀ BÁO CÁO

#### 1, Bộ lọc

* **Bộ Lọc (Filter)** nằm ở menu Mở Rộng/ Bộ Lọc là tính năng mạnh mẽ, cho phép người dùng tạo sẵn các bộ lọc công việc theo các tiêu chí đa dạng theo nhu cầu. Chỉ cần thiết lập Bộ Lọc một lần là sau đó mọi ngày, mọi người khác nhau có thể có ngay các thông tin cần thiết cho nhu cầu công việc.
* **Thông báo cho bộ lọc:** là khả năng thông báo tự động cho bộ lọc: cài đặt những ai được nhận thông báo, và theo chu kì thời gian nào. Thông báo này sẽ được gửi về phần Hộp Tin (Inbox) của mỗi user.

**Ví dụ:**

* Ngày 1 đầu tháng  gửi danh sách các nhân sự có ngày sinh nhật trong tháng tới bộ phận nhân sự
* Thứ 2 đầu tuần gửi danh sách các khách hàng sắp đến hạn thanh toán.

**Cài đặt:**

* Vào menu Mở Rộng/ Bộ Lọc để tạo các bộ lọc đầu việc, dữ liệu theo nhu cầu
* Mở phần cài đặt của Bộ Lọc đã được tạo ra, ở tab Thông Báo sẽ có các cài đặt nhật thông báo này.

Chi tiết hướng dẫn tạo bộ lọc: [Tại đây](https://docs.google.com/document/d/16NsV6c-i9voxoNHueyzA-kLc4x-JeAqWtBPB2qvOMGQ/edit?usp=sharing)

#### 2, Báo cáo

Báo cáo trên phần mềm là sự tổng hợp các dữ liệu liên quan đến công việc thông qua các dạng bảng, đồ thị, hình ảnh trực quan. Từ đó giúp người dùng nhìn vào có thể dễ dàng nhận biết tiến độ, hiệu quả công việc. Mở rộng ra trên phần mềm Luklak là sự tùy biến linh hoạt, bất kỳ dữ liệu nào bạn nhập liệu vào phần mềm cũng có thể thống kê ra báo cáo, các báo cáo này không phải dạng fix cứng có sẵn, mà người dùng hoàn toàn có thể tùy biến tạo ra theo nhu cầu sử dụng.

Chi tiết hướng dẫn sử dụng phần Báo cáo: [Tại đây](https://docs.google.com/document/d/1Yp3UOH8xpG2Rvr-7I0eX3t-H3pO5B2JlLjA4vLYu2cQ/edit?usp=sharing)

### V. PHÒNG LÀM VIỆC

Workspace (phòng làm việc): workspace là một khái niệm cực kì thú vị và hữu ích của luklak, và rất ít app bên ngoài có tính năng này. Workspace cho phép bất kì người dùng cá nhân nào, từ rất nhiều đối tượng tổng chung của công ty (space, filter, dashboard) có thể chọn lọc ra những dữ liệu mình cần hoặc liên quan đến một phần việc nào đó, gom hết vào một nơi gọi là workspace. Để từ đó về sau khi làm phần việc đó thì chỉ cần mở đúng workspace đó ra là: vừa có đầy đủ các dữ liệu, đối tượng liên quan đến làm việc đó, lại vừa tập trung làm việc đó một cách hiệu quả vì không bị xen lẫn các dữ liệu khác không liên quan đến việc đang làm.

Chi tiết hướng dẫn sử dụng Phòng làm việc: [Tại đây](https://docs.google.com/document/d/1sBbgwc9MC7OluZyWQPRcW3jsPf0ZMM87U1vYSKGP9C4/edit?usp=sharing)

### VI. CÁC TÍNH NĂNG KHÁC

#### 1, Thêm thành viên và nhóm người dùng

&#x20;         Chi tiết hướng dẫn thêm thành viên và nhóm người dùng: [Tại đây](https://docs.google.com/document/d/1i2r3yeshtWsb96bFqkm9Q__7QVIUu5o6995nMLCm9lk/edit?usp=sharing)

#### 2, Thành phần và cấu hình

&#x20;         Chi tiết hướng dẫn Thành phần và cấu hình thành phần: [Tại đây](https://docs.google.com/document/d/1_gM1uAtNtNQ3v37MXt7AigXBQCJoXHL-ovgS-va4HmE/edit)

### VII. WORKFLOW HDSD VÀ GIỚI THIỆU&#x20;

Hướng dẫn chi tiết: [Tại đây](https://docs.google.com/document/d/1LlCA4V55pozZfRfbYqTv0RybN-1QpuCzqd6ZBrIxcJg/edit?usp=sharing)

### VIII. HDSD Automation

Hướng dẫn chi tiết: [Tại đây](https://docs.google.com/document/d/1kyEoD-649B4sPiSSKlQTTOCRibRpfO41iWg1ePqDe7Q/edit#heading=h.35y7vexh9d31)
