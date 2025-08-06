# User, Group, Role & Membership

<figure><img src="../../.gitbook/assets/image (70).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (503).png" alt=""><figcaption></figcaption></figure>

### BUSINESS MEMBERSHIP & ROLE

Luklak cung cấp khả năng cơ cấu tổ chức & phân quyền đa dạng sâu rộng, đáp ứng nhiều nhu cầu sử dụng khác nhau. các yếu tố dưới đây chia làm 2 loại chính:

* Phân quyền làm việc với mục việc - dữ liệu (issue): org membership, user account, , functional account, group,
* Phân quyền sử dụng các đối tượng tính năng (object như filter, dashboard, automation rule, folder): object membership

### Business membership

Hạng thành viên của Doanh nghiệp, thể hiện mức độ quyền cao thấp khác nhau, dùng để:

* Cài đặt cho permission scheme/ notification scheme từ đó sẽ định nghĩa phân quyền làm việc với dữ liệu - mục việc (issue)
* Quyền hạn sử dụng các tính năng khác nhau của ứng dụng luklak.

&#x20;

### Mỗi user account khi tạo ra sẽ thuộc về một trong các hạng thành viên sau:

* **Guest:** chỉ có quyền xem và chat trao đổi công việc, ko tạo và xử lý dữ liệu công việc được.
* **Member:** làm việc với issue theo permission scheem. có quyền tạo filter, dashboard, automation rule
* **App manager:** có quyền tạo các chức năng, mảng việc, thư mục
* **Admin:** có quyền truy cập mọi dữ liệu, dùng mọi tính năng. chỉ là ko tạo & xóa được user ở cấp owner.
* **Owner:** tất nhiên là quyền cao nhất, tối thượng, không có giới hạn gì. thường dành cho chủ doanh nghiệp.

Rất ít app có mức độ membership sâu rộng và tinh tế như này.

**Ví dụ** các app khác thường chỉ có quyền cao nhất là admin toàn quyền, đá được admin khác ra dẫn tới đôi khi chủ doanh nghiệp (ko biết kĩ thuật) cấp quyền cho người khác làm admin để cài đặt, xong rồi bị đá bay đi luôn. tách quyền owner ra khỏi admin sẽ đảm bảo an toàn tuyệt đối cho chủ sở hữu doanh nghiệp.

### Role

Vai trò (role) thể hiện các vai trò công việc khác nhau trong tổ chức cũng được dùng để

**Global role:** cài đặt tổng thể ở admin. mặc định hệ thống có những role tạo sẵn dưới đây, admin có thể tạo thêm:

1. Thành viên
2. Quản lý
3. Quản trị
4. Function role: tạo thêm ở function, và chỉ có tác dụng với function đó và các space tạo ra từ function đó.

**Sử dụng:**

* Role được dùng làm object nhận quyền action và notification khi cài đặt permission/ notification scheme. các scheme này sẽ được dùng cài đặt trong function.
* Khi space được tạo ra từ function, thì sẽ gán các user/ group cụ thể vào các role áp dụng cho space đó, và sẽ ăn vào phương án phân quyền/ thông báo ở trên.
