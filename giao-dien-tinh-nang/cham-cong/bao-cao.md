# Báo cáo

<mark style="color:red;">**guidejar**</mark>

## 1. Tổng quan

Báo cáo tự động tổng hợp số liệu chấm công theo phòng ban, nhóm, cá nhân, giúp quản lý nắm bắt nhanh tình hình làm việc thực tế

{% hint style="info" %}
Dữ liệu hiển thị dựa vào quyền của người dùng, [**xem chi tiết tại đây 📚**](../../thiet-lap-cham-cong/phan-quyen.md)
{% endhint %}

## 2. Bản ghi chấm công

**Bản ghi chấm công** (Attendance records) là nơi ghi lại chi tiết từng thao tác chấm công (giờ vào, giờ ra) của từng nhân sự theo từng ngày và từng quy tắc được áp dụng.\
Báo cáo này giúp người quản lý hoặc người dùng kiểm tra, phân tích và xử lý dữ liệu chấm công một cách cụ thể, đặc biệt hữu ích khi cần theo dõi các trường hợp bất thường

### 2.1. Cột hiển thị

Mặc định chỉ hiển thị một số cột và thông tin chấm công theo khung đầu tiên, người dùng có thể chọn <img src="../../.gitbook/assets/image (2).png" alt="" data-size="line"> để thay đổi và lựa chọn các cột hiển thị theo mong muốn

<details>

<summary>Thông tin các cột</summary>

<table><thead><tr><th width="207">Cột</th><th>Mô tả</th></tr></thead><tbody><tr><td><strong>Nhân sự</strong></td><td>Tên tài khoản trong Luklak của nhân sự</td></tr><tr><td><strong>ID</strong></td><td>ID tài khoản của nhấn sự trong Luklak</td></tr><tr><td><strong>Ngày</strong></td><td>Ngày chấm công theo quy tắc</td></tr><tr><td><strong>Tên quy tắc</strong></td><td>Tên của Quy tắc chấm công đang được áp dụng tại bản ghi.</td></tr><tr><td><strong>Số giờ làm việc bắt buộc</strong></td><td>Tổng số giờ phải làm trong ngày theo quy tắc (không bao gồm thời gian nghỉ giữa giờ)</td></tr><tr><td><strong>Giờ chấm công vào bắt buộc</strong></td><td>Giờ vào quy định của khung</td></tr><tr><td><strong>Giờ chấm công vào thực tế</strong></td><td>Giờ nhân sự chấm công vào</td></tr><tr><td><strong>Số phút vào muộn</strong></td><td>Số phút nhân sự đi muộn hơn so với quy định</td></tr><tr><td><strong>Cảnh báo chấm công vào</strong></td><td>Hiển thị "<em>Có</em>" khi nhân sự chấm công sau mốc cảnh báo vào theo quy định</td></tr><tr><td><strong>Giờ chấm công vào bắt buộc</strong></td><td>Giờ ra quy định của khung</td></tr><tr><td><strong>Giờ chấm công ra thực tế</strong></td><td>Giờ nhân sự chấm công ra</td></tr><tr><td><strong>Số phút ra sớm</strong></td><td>Giờ phút nhân sự ra sơm hơn so với quy định</td></tr><tr><td><strong>Cảnh báo chấm công ra</strong></td><td>Hiển thị "<em>Có</em>" khi nhân sự chấm công trước mốc cảnh báo ra theo quy định</td></tr><tr><td><strong>Kết quả</strong></td><td>Kết quả chấm công của nhân sự: <em>Muộn, Đúng giờ, Không chấm công vào, Quên</em> </td></tr><tr><td><strong>Địa điểm</strong></td><td>Thông tin về vị trí, Wi-Fi (MAC address), địa chỉ IP của nhân sự khi chấm công</td></tr><tr><td><strong>Chấm công ngoài địa điểm</strong></td><td>Hiển thị "<em>Có</em>" khi nhấn sự chấm không đúng địa điểm quy định</td></tr><tr><td><strong>Link ảnh chấm công</strong></td><td>Livephoto của nhân sự khi chấm công</td></tr><tr><td><strong>Mục giải trình</strong></td><td>Mục mà nhân sự chọn để giải trình cho các bất thường khi chấm công</td></tr><tr><td><strong>Link ảnh giải trình</strong></td><td>Livephoto của nhân sự khi giải trình bất thường</td></tr><tr><td><strong>Ghi chú</strong></td><td>Nội dung nhân sự gửi khi giải trình bất thường</td></tr></tbody></table>



</details>

### 2.2. Bộ lọc

Người dùng có thể lọc các dữ liệu để xem các bản ghi theo mong muốn: **Thời gian, Người, Nhóm, Quy tắc chấm công, Các bất thường**

{% hint style="info" %}
Khi không có tiêu chí lọc nào, hệ thống sẽ hiển thị báo cáo tổng hợp của các Quy tắc mà người dùng có quyền&#x20;
{% endhint %}

### 2.3. Xuất báo cáo

Chọn nút <img src="../../.gitbook/assets/image (1).png" alt="" data-size="line"> để tải xuống file excel dữ liệu báo cáo

{% hint style="success" %}
**Gợi ý 💡:**&#x20;

* Nên lọc các dữ liệu mong muốn trước khi xuất dữ liệu
* Xuất báo cáo và lưu trữ lại thường xuyên vì dữ liệu chấm công chỉ lưu trên hệ thống 60 ngày kể từ ngày phát sinh
{% endhint %}

## 3. Báo cáo tổng hợp

**Báo cáo tổng hợp** (Summary report) giúp quản trị viên hay chính nhấn sự nhanh chóng nắm được tổng quan tình hình chấm công trong một khoảng thời gian cụ thể, đáp ứng cho việc theo dỗi việc chấm công, tính lương, đánh giá mức độ chuyên cần,...

### 3.1. Cột hiển thị

Mặc định chỉ hiển thị một số cột thông tin chấm công, người dùng có thể chọn <img src="https://open.gitbook.com/~gitbook/image?url=https%3A%2F%2F3530538507-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F9KrtNM7ofVLvcrDpn5Ls%252Fuploads%252FHSZJZFduC4H4YqoqdIwM%252Fimage.png%3Falt%3Dmedia%26token%3D92ab2af4-419f-4da4-ad10-1ef48563114c&#x26;width=151&#x26;dpr=4&#x26;quality=100&#x26;sign=4c80a786&#x26;sv=2" alt="" data-size="line"> để thay đổi và lựa chọn các cột hiển thị theo mong muốn

<details>

<summary>Thông tin các cột</summary>

<table><thead><tr><th width="179.99993896484375">Cột</th><th>Mô tả</th></tr></thead><tbody><tr><td><strong>Nhân sự</strong></td><td>Tên tài khoản trong Luklak của nhân sự</td></tr><tr><td>I<strong>D</strong></td><td>ID tài khoản của nhấn sự trong Luklak</td></tr><tr><td><strong>Quy tắc chấm công</strong></td><td>Tên quy tắc chấm công</td></tr><tr><td><strong>Số ngày có mặt</strong></td><td>Số ngày nhân sự có chấm công</td></tr><tr><td><strong>Số giờ làm việc tính lương</strong></td><td>Tổng số giờ thực tế có mặt tại nơi làm việc, tính trong khoảng giờ quy định và không bao gốm giờ nghỉ<br><strong>Lưu ý:</strong> nếu nhân sự quên chấm công thì giờ làm việc theo khung đó sẽ tính bằng 0</td></tr><tr><td><strong>Số ngày nghỉ</strong></td><td>Số ngày nhân sự nghỉ làm (không bao gồm các ngày được nghỉ)</td></tr><tr><td><strong>Số ngày quên chấm công vào</strong></td><td>Số ngày nhân sự không check-in trong thời gian cho phép</td></tr><tr><td><strong>Số ngày quên chấm công ra</strong></td><td>Số ngày nhân sự không check-out trong thời gian cho phép</td></tr><tr><td><strong>Số ngày vào muộn</strong></td><td>Số ngày nhân sự check-in sau giờ vào được quy định.</td></tr><tr><td><strong>Số ngày ra sớm</strong></td><td>Số ngày nhân sự check-out trước giờ ra quy định</td></tr><tr><td><strong>Số phút vào muộn</strong></td><td>Tổng số phút nhân sự đi muộn trong khoảng thời gian lựa chọn</td></tr><tr><td><strong>Số phút ra sớm</strong></td><td>Tổng số phút nhân sự đi muộn trong khoảng thời gian lựa chọn</td></tr><tr><td><strong>Số ngày Cảnh báo chấm công vào</strong></td><td>Số ngày nhân sự check-in sau mốc thời gian Cảnh báo chấm công vào</td></tr><tr><td><strong>Số ngày Cảnh báo chấm công ra</strong></td><td> Số ngày nhân sự check-out trước mốc thời gian Cảnh báo chấm công ra</td></tr><tr><td><strong>Số ngày chấm công ngoài địa điểm</strong></td><td>Số ngày nhân sự thực hiện chấm công từ Địa điểm không đúng theo quy định</td></tr></tbody></table>

</details>

### 3.2. Bộ lọc

Người dùng có thể lọc các dữ liệu để xem các bản ghi theo mong muốn: **Thời gian, Người, Nhóm, Quy tắc chấm công, Các bất thường**

{% hint style="info" %}
Khi không có tiêu chí lọc nào, hệ thống sẽ hiển thị báo cáo tổng hợp của các Quy tắc mà người dùng có quyền&#x20;
{% endhint %}

### 3.3. Xuất báo cáo

Chọn nút <img src="../../.gitbook/assets/image (1).png" alt="" data-size="line"> để tải xuống file excel dữ liệu báo cáo

{% hint style="success" %}
**Gợi ý 💡:**&#x20;

* Nên lọc các dữ liệu mong muốn trước khi xuất dữ liệu
* Xuất báo cáo và lưu trữ lại thường xuyên vì dữ liệu chấm công chỉ lưu trên hệ thống 60 ngày kể từ ngày phát sinh
{% endhint %}

## 💡 FAQs
