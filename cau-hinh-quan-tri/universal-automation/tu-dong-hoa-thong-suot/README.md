# Tự động hóa thông suốt

## Tự động hóa thông suốt 100%

{% hint style="info" %}
Ví dụ tại CATURA - Thiết kế nội thất & thi công xây dựng: Xem luồng tự động hóa thông suốt, không rào cản qua các phòng ban Marketing, Sales, Thiết kế & Thi công, Kế toán, CSKH, Quản lí dự án... \[_+ phóng to để xem chú thích_]
{% endhint %}

{% @guidejar/embed guideId="DMbMfU3Mm0lLNFNNmSn7" type="1" controls="on" url="https://www.guidejar.com/embed/DMbMfU3Mm0lLNFNNmSn7?type=1&controls=on" %}

* Tự động xử lý logic và các tác vụ, kết nối dữ liệu tương tác giữa ở các nơi khác nhau dựa trên nguyên trác trigger - condition - action.
* Đây là _universal automation_, có tính phổ quát khả dụng trên toàn hệ thống, ở bất kì chỗ nào. khi cài đặt _function_ thì có _automation_ trong đó, ngoài ra ở những chỗ khác như _khu vực (area), mảng việc (space), thư mục (folder)_ cũng đều có automation.



Universal automation phổ quát trên toàn hệ thống chứ ko phải là một app automation/ process rời rạc như phần mềm thế hệ 2 (feature software). có thể tạo/ dùng được ở mọi nơi

* Gọi ra được từ workflow, tăng sức mạnh cho workflow
* Area
* Space
* Folder (global)

Kết nối tương dữ liệu từ mọi chức năng công việc khác nhau cho tương tác với nhau nguyên lý chung: trigger event - condition - flow logic - action

* Cả trigger & action đều có thể tương tác với dữ liệu bên trong luklak và các app bên ngoài
* Tương tác dữ liệu bên ngoài thông qua webhook (cả gửi & nhận - 2 chiều). với nhiều app phổ biến như google drive/ mail/ calendar (và rất nhiều app khác) nên kết nối qua trung gian n8n, đã đóng gói sẵn khả năng tích hợp đa dạng
* Giao tiếp kết nối bên ngoài: email, zalo, sms...
*   Action (update field, send chat, email...) có khả năng lấy dữ liệu động (smart value) từ các mục việc, biến đổi tính toán xử lý, sau đó điền vào

    functional account dùng làm actor cho automation rule, nâng cao tính bảo mật, ít phần mềm có mức này.
