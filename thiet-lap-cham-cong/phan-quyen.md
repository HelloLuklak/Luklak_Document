# Phân quyền

## 1. Tổng quan

Tính năng chấm công của Luklak được thiết kế với hệ thống phân quyền hai tầng, kết hợp giữa Hạng thành viên trong Doanh nghiệp (Business Membership) và Hạng thành viên của tính năng Chấm công (Object Membership).

Cách tổ chức này giúp doanh nghiệp vừa quản lý tập trung toàn hệ thống, vừa ủy quyền linh hoạt theo từng nhóm, từng quy tắc, đảm bảo bảo mật và rõ ràng trong phân trách nhiệm.&#x20;

## 2. Theo Object Membership

Ở mỗi Quy tắc chấm công có Hạng thành viên riêng, người dùng có thể gán người hoặc nhóm cụ thể vào quản lý, thiết lập các quy tắc

{% hint style="info" %}
**Lưu ý:**

* Các nhân sự được áp dụng theo Quy tắc, mặc định là Thành viên của Quy tắc
* Các Quy tắc có bypass với Hạng thành viên trong Doanh nghiệp (Business membership), [**xem chi tiết ở đây 📚**](phan-quyen.md#id-3.-theo-business-membership)
{% endhint %}

<table><thead><tr><th width="212"></th><th align="center">Quản trị viên (Admin)</th><th align="center">Quản lý (Manager)</th><th align="center">Thành viên (Member)</th></tr></thead><tbody><tr><td>Xem quy tắc</td><td align="center">✅</td><td align="center">✅</td><td align="center">✅</td></tr><tr><td>Sửa / Bật / Tắt</td><td align="center">✅</td><td align="center">✅</td><td align="center"></td></tr><tr><td>Xóa</td><td align="center">✅</td><td align="center"></td><td align="center"></td></tr><tr><td>Xem, Xuất báo cáo toàn bộ nhân sự trong quy tắc</td><td align="center">✅</td><td align="center">✅</td><td align="center"></td></tr><tr><td>Xem, Xuất báo cáo của bản thân theo quy tắc</td><td align="center">✅</td><td align="center">✅</td><td align="center">✅</td></tr></tbody></table>

## 3. Theo Business Membership

<table><thead><tr><th width="199"></th><th align="center">Chủ sở hữu (Admin)</th><th align="center">Quản trị viên (Admin)</th><th align="center">Quản lý ứng dụng (App manager)</th><th align="center">Thành viên (Member)</th></tr></thead><tbody><tr><td>Xem danh sách, thông tin Quy tắc</td><td align="center">✅</td><td align="center">✅</td><td align="center"></td><td align="center"></td></tr><tr><td>Tạo mới, Nhân bản Quy tắc</td><td align="center">✅</td><td align="center">✅</td><td align="center">✅</td><td align="center"></td></tr><tr><td>Sửa, Bật/tắt Quy tắc</td><td align="center">✅</td><td align="center">✅</td><td align="center"></td><td align="center"></td></tr><tr><td>Xóa Quy tắc</td><td align="center">✅</td><td align="center">✅</td><td align="center"></td><td align="center"></td></tr><tr><td></td><td align="center"></td><td align="center"></td><td align="center"></td><td align="center"></td></tr><tr><td>Xem danh sách, thông tin Lịch làm việc</td><td align="center">✅</td><td align="center">✅</td><td align="center">✅</td><td align="center">✅</td></tr><tr><td>Tạo Lịch làm việc</td><td align="center">✅</td><td align="center">✅</td><td align="center">✅</td><td align="center"></td></tr><tr><td>Sửa Lịch làm việc</td><td align="center">✅</td><td align="center">✅</td><td align="center">✅</td><td align="center"></td></tr><tr><td>Xóa Lịch làm việc</td><td align="center">✅</td><td align="center">✅</td><td align="center"></td><td align="center"></td></tr><tr><td></td><td align="center"></td><td align="center"></td><td align="center"></td><td align="center"></td></tr><tr><td>Xem danh sách, thông tin Địa điểm</td><td align="center">✅</td><td align="center">✅</td><td align="center">✅</td><td align="center">✅</td></tr><tr><td>Tạo Địa điểm</td><td align="center">✅</td><td align="center">✅</td><td align="center">✅</td><td align="center"></td></tr><tr><td>Sửa Địa điểm</td><td align="center">✅</td><td align="center">✅</td><td align="center">✅</td><td align="center"></td></tr><tr><td>Xóa Địa điểm</td><td align="center">✅</td><td align="center">✅</td><td align="center"></td><td align="center"></td></tr><tr><td></td><td align="center"></td><td align="center"></td><td align="center"></td><td align="center"></td></tr><tr><td>Xem, Xuất báo cáo của tất cả Nhân sự</td><td align="center">✅</td><td align="center">✅</td><td align="center"></td><td align="center"></td></tr><tr><td>Xem, Xuất báo cáo của bản thân</td><td align="center">✅</td><td align="center">✅</td><td align="center">✅</td><td align="center">✅</td></tr></tbody></table>

## 💡 FAQs
