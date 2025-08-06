---
hidden: true
---

# Page

### Chức năng (function)&#x20;

Là đơn vị tổ chức của nocode. mỗi một chức năng công việc của doanh nghiệp sẽ tạo 1 function ở luklak. VÍ DỤ: chức năng quản lý nhân sự HRM, chức năng quản lý bán hàng CRM; chức năng phê duyệt & đề xuất

#### Loại mục (issue type)

* Mỗi chức năng lớn sẽ chia thành các nghiệp vụ cụ thể bên trong, mỗi luồng đó là một issue type. issue type khác nhau do người dùng tạo ra và đặt tên, bên dưới đều là universal object.
* Mỗi loại mục sẽ định nghĩa trường dữ liệu (data field) và luồng việc (workflow) theo nhu cầu

VÍ DỤ chức năng HRM sẽ chia thành các loại mục:

1. **Employee:** hồ sơ nhân sự
2. **Onboard:** hội nhập nhân sự mới
3. **Offboard:** thủ tục nhân sự nghỉ
4. **Situation:** tình huống nhân sự phát sinh

#### &#x20;Tự động (automation)

* Tự động **xử lý logic** và các tác vụ, kết nối dữ liệu tương tác giữa ở các nơi khác nhau dựa trên nguyên trác trigger - condition - action.
* Đây là **universal automation**, có tính phổ quát khả dụng trên toàn hệ thống, ở bất kì chỗ nào. khi cài đặt function thì có automation trong đó, ngoài ra ở những chỗ khác như khu vực (area), mảng việc (space), thư mục (folder) cũng đều có automation.

#### &#x20;Vai trò (role)

* Định nghĩa các vai trò, cấp bậc khác nhau như thành viên, quản lý, quản trị
* Vai trò (role) sẽ được dùng để định nghĩa phân quyền (permission) và thông báo (notification)

#### &#x20;Thông báo (notification)

* Lựa chọn phương án thông báo (notification scheme) phù hợp với tính chất chức năng công việc
* Cho phép tinh chỉnh sâu rộng ai được nhận được thông báo khi có hành động gì diễn ra

#### &#x20;Phân quyền (permission)

* Lựa chọn phương án phân quyền (permission scheme) phù hợp với tính chất chức năng công việc
* Cho phép tinh chỉnh sâu rộng ai được phép làm gì
