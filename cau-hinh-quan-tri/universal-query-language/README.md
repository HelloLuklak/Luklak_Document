# Universal Query Language

## Universal query language

Sự khác biệt lớn:

* Phần mềm thế hệ 2 (feature software) mỗi chức năng công việc lại được tách thành app/ module riêng với sql databse với các table/ column được định nghĩa riêng. dẫn tới để tổng hợp dữ liệu từ các chức năng khác nhau sẽ cần kiến thức kĩ thuật chuyên sâu về sql, cũng như quyền truy cập database bên dưới. đây đều là thứ mà khách hàng - người dùng không có, dẫn tới hàng ngày họ không tự chủ trong việc tổng hợp dữ liệu từ các phần mềm khác nhau được.
* Mọi chức năng, dữ liệu của luklak được tạo từ một đơn vị **universal object** đã được trừu tượng hóa xử lý mọi vấn đề phức tạp về kĩ thuật database sql bên dưới hệ thống, để bên trên người dùng có thể dễ dàng kéo thả sử dụng mà không cần động đến sql mà vẫn truy vấn, tổng hợp được mọi dữ liệu công việc của mình.
* Không còn cần đến hệ thống xử lý dữ liệu phức tạp với Data Warehouse/ ETL phức tạp và tốn kém nữa.

<figure><img src="../../.gitbook/assets/image (213).png" alt=""><figcaption></figcaption></figure>

_**UQL (universal query language)**_ cho phép truy vấn và tổng hợp mọi dữ liệu công việc nằm ở các chức năng đa dạng khác nhau,

Tính phổ quát của universal object và universal query language (UQL) mang lại tiện ích tiện lợi hàng ngày cho người dùng

* **Thanh lọc nhanh (quick search)**: ở trên cùng, quen thuộc cùng một giao diện và lọc được mọi dữ liệu chức năng khác nhau
* **Bộ lọc lưu sẵn (save fitler)**: tạo sẵn các tiêu chí lọc dữ liệu cho một nhu cầu công việc nào đó, lưu lại để dùng về sau và chia sẻ với người liên quan.
* **Dashboard tổng hợp**: dễ dàng kéo thả tự tạo các báo cáo tổng hợp được dữ liệu từ nhiều nơi, nhiều chức năng khác nhau về một nơi để phân tích.

