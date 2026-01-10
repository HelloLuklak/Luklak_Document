---
description: >-
  Đồng bộ dữ liệu thời gian thực với khả năng tính toán phần chênh lệch khi sửa
  trường số.
---

# Tính khoảng chênh lệch khi sửa trường dữ liệu

{% hint style="info" %}
Trong vận hành, dữ liệu thay đổi liên tục. Một phiếu kho cần sửa, một giờ công cần cập nhật, hay một khoản chi phát sinh—tất cả đều ảnh hưởng đến chỉ số tổng thể. Tự động hóa Phổ quát (Universal Automation) của Luklak giúp các chỉ số tổng hợp (Tổng chi, Tổng tồn, Tổng giờ làm) luôn chính xác 100% ngay tức thì. Thay vì tính toán lại toàn bộ lịch sử, hệ thống xử lý thông minh phần chênh lệch (Delta) của từng thay đổi nhỏ.
{% endhint %}

## Các Bối Cảnh Ứng Dụng Điển Hình

{% hint style="success" %}
Bằng cách tính toán Mức chênh lệch (Delta) và đẩy nó qua bất kỳ đường dẫn nào (Kết nối Đối tượng hoặc Object Picker), bạn biến các bản ghi tĩnh thành một hệ sinh thái sống động. Một thay đổi nhỏ ở bất cứ đâu cũng sẽ tự động làm đúng số liệu ở những nơi liên quan.
{% endhint %}



1. ### Xử Lý Đơn Hàng&#x20;
   * Nghiệp vụ: Bộ phận điều hành tạo `🧊 Đơn hàng` và nhập các `🧊 Khoản chi` (Vận hành, Thuê ngoài, Phát sinh...).
   * Tình huống: Nhân sự sửa lại phí vận chuyển từ 10 triệu xuống 5 triệu.
   * Kết quả: "Tổng chi" của Đơn hàng tự động giảm đúng 5 triệu mà không cần bấm nút tính lại.
2. ### Quản Lý Kho Hàng
   * Nghiệp vụ: `🧊 Kho tổng` quản lý số lượng tồn dựa trên các `🧊 Phiếu nhập/xuất`.
   * Tình huống: Thủ kho sửa số lượng trên phiếu nhập từ 100 cái thành 80 cái.
   * Kết quả: Tồn kho tại `🧊 Kho tổng` tự động trừ đi 20 cái.
3. ### Quản Lý Dự Án
   * Nghiệp vụ: `🧊 Dự án` theo dõi tổng giờ thực hiện từ các `🧊 Log thời gian` hàng ngày.
   * Tình huống: Nhân viên sửa lại log làm việc từ 2 giờ thành 4 giờ.
   * Kết quả: Tổng giờ của `🧊 Dự án` tự động cộng thêm 2 giờ.

***

### Nguyên Tắc Kỹ Thuật

{% hint style="info" %}
Nguyên Lý Cốt Lõi: "Tính Tại Nguồn - Cập Nhật Tại Đích"
{% endhint %}

1. Tính Khoảng chênh lệch tại chỗ: Xác định giá trị thay đổi trên đối tượng hiện tại (`.to` - `.from`).
2. Dò đường dẫn: Xác định đối tượng đích thông qua trường liên kết bất kỳ - `Cha-con`, `Liên kết` hoặc `Trường chọn mục`   &#x20;
3. Thực thi tác động (điều chỉnh tăng/giảm): Cộng/Trừ phần chênh lệch vào giá trị hiện có của đối tượng đích.

> Ví Dụ Minh Họa (Theo bối cảnh Đơn hàng):
>
> * Khoản chi cũ: 10 triệu (lưu trong `$fieldChanges.so_tien.from`)
> * Khoản chi mới: 5 triệu (lưu trong `$fieldChanges.so_tien.to`)
> * Chênh lệch: 5 - 10 = -5 triệu
> * Cập nhật: Hệ thống cộng -5 triệu vào Tổng chi của Đơn hàng (tức là giảm đi 5 triệu).

***

### Hướng Dẫn Cài Đặt Chi Tiết

{% hint style="info" %}
Thiết lập tự động hóa cho bối cảnh Quản lý Chi phí Đơn hàng.
{% endhint %}

```
# Thiết lập Automation: Cập nhật Chênh lệch Chi phí
Hướng dẫn cấu hình để Tổng chi đơn hàng luôn đúng khi nhân sự sửa đổi các khoản chi con.

## Phần 1: Thiết lập Sự kiện (Trigger)
! Điều kiện: 'Khoản chi' phải được kết nối với 'Đơn hàng' qua quan hệ Cha-con, Liên kết, hoặc Trường chọn mục

1. Tạo Quy tắc Mới
   Trong cài đặt `📋 Chức năng` Quản lý chi phí, vào Automation > Tạo quy tắc mới.
   Đặt tên: "Đồng bộ Tổng chi khi sửa đổi".

2. Chọn Sự kiện Kích hoạt
   Sự kiện: "Update Object" (Cập nhật đối tượng).
   * Mẹo: Thêm điều kiện để quy tắc chỉ chạy khi trường "Số tiền" thay đổi 

## Phần 2: Cấu hình Công thức Delta
Thiết lập logic tính toán chênh lệch để đẩy về Đơn hàng cha.

1. Sử dụng branching để tìm đến 🧊 Đơn hàng
   Tùy vào cách liên kết hiện tại, chọn cách tìm tương ứng. Ví dụ: Tìm mục cha. (Do 🧊 Đơn hàng là cha của 🧊 Khoản chi).
 Nếu liên kết hiện tại là object picker hoặc liên kết 2 chiều, bạn cũng có thể tìm được.
2. Cập nhật trường
   Tại trường "Tổng chi" của Đơn hàng, chuyển sang Điều chỉnh tăng/giảm
   Nhập công thức cho khoản chênh lệch:
   `({{$fieldChanges.so_tien.to}} - {{$fieldChanges.so_tien.from}})`

3. Hoàn tất
   Lưu và kích hoạt quy tắc.
   * Kiểm tra: Thử tạo một khoản chi 10đ, sau đó sửa thành 5đ. Tổng chi đơn hàng phải giảm tương ứng.
```

***

