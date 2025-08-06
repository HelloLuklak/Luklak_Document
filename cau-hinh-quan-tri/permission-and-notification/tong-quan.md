# Tổng quan

### Phương án phân quyền (permission scheme)

Tính chất chung

* Khi cài đặt chức năng (function) sẽ có lựa chọn phương án phân quyền (permission scheme) phù hợp với tính chất công việc đó.
* Các phương án phân quyền được quản lý trong admin. có sẵn 4 phương án của hệ thống với mức độ phân quyền khác nhau, có thể dùng được luôn, nhưng không sửa được. người dùng có thể nhân bản/ tạo mới phương án và có thể tùy chỉnh được.
* Mọi mục việc (issue) ở mọi mảng việc (space) tạo ra từ chức năng sẽ áp dụng phương án phân quyền của chức năng đó
* Luklak cung cấp khả năng tùy chỉnh phân quyền sâu rộng và linh hoạt ở mức ít app nào khác có được, với 23 hành động (action) và 6 loại chủ thể khác nhau.



Logic của phần quyền là:

* **Object (các đối tượng hành động tác động vào):** các _mục việc (issue)_ nằm trong các mảng việc (space).
* **Action (các hành động có thể thực hiện trên object):** view, create, edit, edit, link, change status, chat...
* **Subject (người nhận được quyền có thể thực hiện action trên object):** user & user field, group & group field, role, org membership

<figure><img src="../../.gitbook/assets/image (125).png" alt=""><figcaption></figcaption></figure>

