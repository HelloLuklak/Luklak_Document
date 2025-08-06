# Role

**Vai trò (role)** thể hiện các vai trò công việc khác nhau trong tổ chức cũng được dùng để

**Global role:** cài đặt tổng thể ở admin. mặc định hệ thống có những role tạo sẵn dưới đây, admin có thể tạo thêm:

* Thành viên
* Quản lý
* Quản trị

**Function role:** tạo thêm ở function, và chỉ có tác dụng với function đó và các space tạo ra từ function đó.

**sử dụng:**

* Role được dùng làm object nhận quyền action và notification khi cài đặt permission/ notification scheme. các scheme này sẽ được dùng cài đặt trong function.
* **Khi space được tạo ra từ function,** thì sẽ gán các user/ group cụ thể vào các role áp dụng cho space đó, và sẽ ăn vào phương án phân quyền/ thông báo ở trên.
