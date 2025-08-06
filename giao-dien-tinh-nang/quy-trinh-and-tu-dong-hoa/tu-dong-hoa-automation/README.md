# Tự động hóa (Automation)

## Ví dụ thực tế

{% hint style="info" %}
Tìm hiểu cách hoạt động của Luklak Automation, với ví dụ là tự động gửi chat chúc mừng khi chốt khách thành công.
{% endhint %}

{% @guidejar/embed guideId="4ee39fc1-ce81-49bb-963f-dd87d5a14366" type="1" controls="on" url="https://www.guidejar.com/embed/4ee39fc1-ce81-49bb-963f-dd87d5a14366?type=1&controls=on" %}

## Mô hình Trigger - Condition - Action

{% @guidejar/embed guideId="2219847e-4891-4073-b3e5-25b128586a03" type="1" controls="on" url="https://www.guidejar.com/embed/2219847e-4891-4073-b3e5-25b128586a03?type=1&controls=on" %}

## 3 loại hình kích hoạt tự động hóa

{% hint style="info" %}
Cách kích hoạt đa dạng, bao gồm: (1) Tự động trên tiến trình, (2) Quy tắc chạy ngầm, (3) Hành động trên mục
{% endhint %}



{% @guidejar/embed guideId="1596e906-d27c-4d14-946b-abf2c9346dd1" type="1" controls="on" url="https://www.guidejar.com/embed/1596e906-d27c-4d14-946b-abf2c9346dd1?type=1&controls=on" %}

### I, MỘT SỐ KHÁI NIỆM VỀ AUTOMATION TRÊN LUKLAK

Automation một công cụ Luklak tạo ra để người dùng có thể cài đặt trước các quy tắc và dựa vào đó, hệ thống sẽ tự động thực hiện các hành động. Hỗ trợ người dùng không cần thực hiện các công việc lặp đi lặp lại theo quy tắc và hạn chế các sai sót không đáng có khi thực hiện các công việc này. Để sử dụng được chức năng automation của hệ thống thì người dùng cần tạo ra các quy tắc và cấu hình quy tắc đấy dựa trên các yếu tố kích hoạt (Trigger), điều kiện (Condition), hành động (Action). Vậy tất cả chúng là gì?&#x20;

#### 1, Quy tắc

Quy tắc có thể hiểu là tổng hợp các yếu tố bao gồm kích hoạt (Trigger), điều kiện (Condition), hành động (Action) mà khi kết hợp với nhau chúng sẽ thực hiện công việc một cách tự động theo yêu cầu, nhu cầu mà người dùng cài đặt&#x20;

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXcnemRSLMm5oQdhsAAaxTGf_pn_UPT-rL686FLJNQcrxF4a4LUvQu3y7ZIp_IvSmtC40RknEfS0I9F7Ex2xT1VIsfaCmKFBTBukDHUE26Hc3RTqmLJN6sKgdrLeO8PggAKRMVdxAOESk0iOaICfFz6N8kw?key=2ms7aSILnOUvzUjqc2G4lg" alt=""><figcaption></figcaption></figure>

#### 2, Cách kích hoạt (Trigger)

Kích hoạt (Trigger) là một hành động của người dùng trên hệ thống ví dụ như cập nhật mục, tạo mục hay chạy theo lịch trình được cấu hình,... mà dựa vào đó, hệ thống sẽ xác định để kích hoạt quy tắc hành động. Một hành động được coi là kích hoạt (Trigger) khi thỏa mãn các điều kiện được cấu hình trong kích hoạt (Trigger) đó

Các loại kích hoạt hiện tại Luklak đang cung cấp bao gồm

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXdA4ZcY38upbqr03lZhoh9y6eVYdrjfEAqINAz8fXB3LzsNg_fMoX6JJb2BMIctOdevBJnC6Ikx3vBmd6Qa_L6cXF7nQaaX4-5SIjY_FNPuDULr__r2K4ttkCc4bcHNn6wOC5BkD9INAs8h3opMs1-fGDyi?key=2ms7aSILnOUvzUjqc2G4lg" alt=""><figcaption></figcaption></figure>

* **Tạo mục:** kích hoạt khi người dùng tạo mục
* **Chuyển trạng thái:** kích hoạt khi người dùng chuyển trạng thái
* **Cập nhật trường:** kích hoạt khi người dùng cập nhật một trường thông tin trên mục
* **Lịch trình:** đưa ra lịch trình thời gian biểu để hệ thống dựa vào đó mà kích hoạt quy tắc
* **Kết nối mục:** kích hoạt khi người dùng thực hiện kết nối mục
* **Xoá mục:** kích hoạt khi người dùng thực hiện xoá mục
* **Xoá liên kết mục:** kích hoạt khi người dùng thực hiện xóa liên kết mục

#### 3, Điều kiện (Condition)

Sử dụng Điều kiện để thu hẹp phạm vi các mục thực hiện hành động. Ví dụ: Cài đặt điều kiện Tất cả mục kiểm hoàn thành, Nếu mục đó thỏa mãn điều kiện thì thực hiện Cập nhật trường.

Có 2 loại Điều kiện là If/ else và Multi-path

* If/else: thiết lập điều kiện rồi sẽ chạy theo 2 nhánh, nếu đúng chạy nhánh này, sai thì chạy nhánh còn lại

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXcLxN3t5QASzhNQGh3iswohY0bRsKNBlDq1JZSuHUgO1lgOKjCpDiw2zYDF_3-0HGrN3UwjxnR-uAWini_NE6dzjXJgtR283oQ-Ux_cqLQFOXJ1EChz-ruAL4TymXuvgjI1dzxkh2aUjmrN9ndLvOTtUAWA?key=2ms7aSILnOUvzUjqc2G4lg" alt=""><figcaption></figcaption></figure>

* Multi-path thiết lập điều kiện ở mỗi nhánh, nếu đúng điều kiện mới thực hiện các hành động tiếp

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXelznB41HVbdiwyxGw1A3Lf0CNXF4-vBDdPdVn5iOI4mFNEmjh4jMbgQHO0lCwW6SYMP32db_StTnHm2dQa4TwwIXOWHMn_KCxx9Mr8Q7g9BUR4sOm1os3EBW3z00N7mohHs0wMXXd30dcjJUfcmV1Ztz4?key=2ms7aSILnOUvzUjqc2G4lg" alt=""><figcaption></figcaption></figure>

Các điều kiện mà hiện tại luklak cung cấp bao gồm:&#x20;

* **Trường dữ liệu:** đặt điều kiện với một trường dữ liệu có trong mục kích hoạt hành động để sàng lọc ra các mục thực hiện hành động
* **Mục kiểm:** đặt điều kiện về các mục kiểm có trong mục kích hoạt hành động để sàng lọc ra các mục thực hiện hành động
* **Mục con:** đặt điều kiện về các mục con có trong mục kích hoạt hành động để sàng lọc ra các mục thực hiện hành động
* **Kết nối mục:** đặt ra điều kiện với các mục kết nối trong mục kích hoạt hành động để sàng lọc ra các mục thực hiện hành động

#### 4, Action (Hành động)

Có thể hiểu hành động (Action) ở đây chính là những hành động người dùng yêu cầu hệ thống tự động cập nhật sau khi đã thỏa mãn các yếu tố về kích hoạt (Trigger) và điều kiện (Condition)

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXdOcBwQUWDxymV2PuGKM9qflKhD-xKZ3GUufs9JhCVKl1fOq_1PT25DjOTzhZdFy7SUvhpLqgctBH6BPLqSXLwvfmAxcikLlgXpWdA7lzdpa1TwIXDeCtPARplQwUSmPUd4A1CJl5pvAHAR6H08FCzd8B9T?key=2ms7aSILnOUvzUjqc2G4lg" alt=""><figcaption></figcaption></figure>

Các loại hành động mà Luklak đang cung cấp bao gồm:&#x20;

* **Tạo mục:** tự động thực hiện tạo mục&#x20;
* **Tạo mục con:** tự động thực hiện tạo mục con
* **Tạo mục kiểm:** tự động thực hiện tạo mục kiểm
* **Chuyển trạng thái:** tự động chuyển trạng thái
* **Cập nhật trường:** tự động cập nhật giá trị trường thông tin được chọn
* **Kết nối mục:** tự động thực hiện kết nối mục theo cài đặt trước
* **Xoá mục:** tự động thực hiện xoá các mục được định trước thông qua yêu cầu của người dùng
* **Xoá liên kết:** tự động thực hiện xoá các liên kết mục định trước thông qua yêu cầu của người dùng
* **Gửi mail:** tự động thực hiện gửi email đến email được người dùng định trước
* **Chat:** tự động chat tương tác theo yêu cầu của người dùng

#### 5, Branching&#x20;

Sử dụng để rẽ nhánh sang hành động ở các mục được chọn trong bước cấu hình branching. Ví dụ: Trong Branching chọn mục con, thì hành động chuyển trạng thái, sẽ là chuyển trạng thái của các mục con của mục kích hoạt

Trong Branching không chọn được điều kiện If / Else hay Multi-path mà chỉ chọn được Action

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXdnZkENXr9UP0-lfbl8-uqru_ptlH-IXCrh4jImz8nG0RldmcqVePMPSJ_9-RIBs8SupFmr_vkc7L-7GXK11QMuDpJ_UFa8UZgAQ9Femn2zv5O1jn7VP7yBFY96naf0p3R3rRecI17hxc0NqhHLDO9MfilS?key=2ms7aSILnOUvzUjqc2G4lg" alt=""><figcaption></figcaption></figure>

#### 6, Người thực thi (Actor)

Người hoặc tài khoản chức năng được gán vào người thực thi phải có quyền thực hiện các hành động thì quy tắc mới chạy thành công.

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXdaKAO_JQC22ltH3og3j1qdotwGlkDRYLwBF-YA7peRHjp_tGBlWhR7xPSoA-rA7f1RK_frFMy0eEXyAiEZV3lM4He-TO7iUR8l7E1BhYYcXsX-DmfJgUdJnYqLybRhO0L4WvtIHJxrkvScitOBFAAQ54qH?key=2ms7aSILnOUvzUjqc2G4lg" alt=""><figcaption></figcaption></figure>

#### 7, Vị trí (Location)

Có 4 loại Vị trí cho Automation: Space, Area, Function, Folder

* **Automation trong chức năng:** các quy tắc được tạo ở đây sẽ ảnh hưởng và có tác dụng lên tất cả các mảng việc có sử dụng chức năng này

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXfKM0MmGL5bCJzeypipY6_U-jTRPYkL7Iq2jb22GgSKuyCtOkWszV_zq8YfT4Ey-oyCkznOcl-cgrGiJjdjCayCm8DOXUbuaN8iMrl_8KJp0z6Z58O6KFd9TzRBHjL_0KRplVmzoIrmZGV0opbPIiF-jAE?key=2ms7aSILnOUvzUjqc2G4lg" alt=""><figcaption></figcaption></figure>

* **Automation trong mảng việc (Space):** các quy tắc được tạo ra ở đây sẽ ảnh hướng đến tất cả các mục có trong mảng việc (Space) ấy

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXfyAe-mWTiaDfUHx0fRI3bZpYo7fN2iou1wPme-gY2vH7NX7PZoeYj7dWNEe5KKZpMuoK5MKXycu9_STuddXuJd9vExMA3DC6Uy-sc7ElAVPOfYZTQr-Pstfuw-JSR-r3uYNsZqd3IgKaqanqSCOx15iR0?key=2ms7aSILnOUvzUjqc2G4lg" alt=""><figcaption></figcaption></figure>

* **Automation trong khu vực (Area):** các quy tắc được tạo ra ở đây sẽ ảnh hướng đến tất cả các mục có trong khu vực (Area) ấy

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXcknhM3ZWIhlGdkecz9nvJEKZPP4Gr4yfY2wwWmUfWdU5i5H6ZwU19FsYaC-yXeASBN9ZtPo_xch3ep5KxZkLt9Erku77aPecqlw7ZIyVX7zZcCLJp2sYdCGYLd8OOWOpj8KNlFIY9ofHr-MqLSPdcEHXM?key=2ms7aSILnOUvzUjqc2G4lg" alt=""><figcaption></figcaption></figure>

* Automation trong folder

_**\*Lưu ý:** các Automation hoạt động độc lập với nhau, không phân biệt giống hay khác nhau nên người dùng lưu ý khi cài đặt, tránh trường hợp cấu hình 2 quy tắc (rule) có tác dụng giống nhau thì hệ thống vẫn sẽ kích hoạt cả 2 quy tắc (rule) đó_

#### 8, Trạng thái quy tắc

Quy tắc có đang hoạt động hay không phụ thuộc vào trạng thái của quy tắc đó.

Có 2 trạng thái là Bật và Tắt

Chỉ thực hiện quy tắc khi đang ở trạng thái Bật.

Nếu quy tắc đang ở trạng thái Tắt, cho dù các event có thỏa mãn cấu hình của quy tắc thì sẽ không thực hiện \


<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXcLE3V1V29bIED9mJfzqCZuJNVD_f23A5ylHGaVc8N9JenIFbVzt-dA5BuRzOXPTQ5MAWUv9J-rkC-naRAOcND9KeNYRA7OCgOO86XRZkc1XQFAwoi1L3lqt7QQduwFwBdCNtLID78dtKgLPbpg7QESyij-?key=2ms7aSILnOUvzUjqc2G4lg" alt=""><figcaption></figcaption></figure>

### II, HƯỚNG DẪN SỬ DỤNG CHI TIẾT

#### 1, Ví dụ thực tế

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXdnoHWWaH77cFbdpiRdYnbUK1OP_xGNHhECqd076Nn0ItBHidWbAQM7cbdm998mPbiehA6AA1-kLDvu-ZbR1wJyvl4mwPwoh_CDS582EoXn6_kgTeIp7GuIQ2ysdO8juLLRG7PMlTsoGM3EBffpQeQqp74?key=2ms7aSILnOUvzUjqc2G4lg" alt=""><figcaption></figcaption></figure>

Ví dụ như trên là một quy trình bán hàng được xây dựng dựa trên tiến trình tiêu chuẩn với màn hình gồm các trường dữ liệu sau:&#x20;

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXdr8y3jO34uAer1f2xv9HvsIjobgczml_Kq0QAZlAy7Lvvy9SfBvHLJ4Q54xtK4dtybzP9T6H3PE12BN-c0VK2N0u6r9V_xroxIwgtAU6L9vjeT67fuNIr0xPQIcKmK89Fld_4Vx6nG5hi1t_KwVl5Jg1s?key=2ms7aSILnOUvzUjqc2G4lg" alt=""><figcaption></figcaption></figure>

Ví dụ, trong việc tính toán số liệu hay cập dữ liệu trên hệ thống, nếu ngày trước người dùng phải tính toán các số liệu bên ngoài trước sau đó mới nhập các dữ liệu đó lên hệ thống. Cách thức làm việc này quá thủ công, rất tốn thời gian cũng như khó tránh khỏi các trường hợp sai sót trong quá trình tính toán số liệu hay nhập liệu lên hệ thống. Tuy nhiên, với sự ra đời của Automation mới, người dùng chỉ cần tiến hành cập nhật, chỉnh sửa, nhập liệu dữ liệu lên phần mềm và hệ thống sẽ làm những việc còn lại. Như ví dụ trên với các trường Số lượng yêu cầu, Số lượng thực nhận và Chênh lệch, người dùng chỉ cần nhập liệu các trường Số lượng yêu cầu, Số lượng thực nhận hệ thống sẽ tự động tiến hành tính toán trường Chênh lệch với công thức&#x20;

Chênh lệch = Số lượng yêu cầu - Số lượng thực nhận

Người dùng cũng có thể áp dụng Automation để cập nhật các kiểu dữ liệu khác có trong hệ thống&#x20;

Cấu hình

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXdKNYteBedpI6cFWFdNgzAYwo76yD1AIO906GQLmO8sckGaAf2JAU15OdOKK23Ojki_EDc8ekk8bIOj-cbiZoj5032QR52wwuhEVvSI1tIxpdcRJuXc4HZlBOr0k1oMRN6O1Tn4jEylS6lL5UjEBJb5S9sX?key=2ms7aSILnOUvzUjqc2G4lg" alt=""><figcaption></figcaption></figure>

Kết quả

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXfT-oUIn-iu3rJz8meZByK5je3wI_0Z2lUFQja9BZ3UG0gp85tnrH-e21iAsGDH70lI1563SedrohlJnY8RaBY-uMDZTzgicegrjw-N1p1FjWQ0Jh3sewrukSKquQJq7vloExxD7MAWHsg153zOWKMVa90?key=2ms7aSILnOUvzUjqc2G4lg" alt=""><figcaption></figcaption></figure>

Trong trường hợp khác, ở mỗi tiến trình, giai đoạn công việc, người dùng cũng có nhu cầu chia công việc thành các công việc con để phân công cho các thành viên khác hay tạo ra các tiêu chuẩn công việc cần đạt được ở giai đoạn này để mọi người cần đáp ứng và hoàn thành. Điều này sẽ khiến công việc trở nên dễ dàng hoàn thành, giám sát tiến độ công việc và doanh nghiệp cũng có thể tận dụng được triệt để nguồn lực về nhân sự mà mình có. Ví dụ như trong tiến trình công việc trên, khi chuyển đến trạng thái NHẬN HÀNG & KIỂM TRA, người dùng có thể tự động tạo thêm các mục kiểm có tác dụng như các điều kiện kiểm tra, hỗ trợ cho việc kiểm soát chất lượng sản phẩm nhận được một cách tốt hơn.

\


#### Cấu hình

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXfW1sgc-PVtLixfHhd3GN4i-7JTY2amOxeIRob4DWdtdpoAUhesV3MOX-lLUm1LunwKs_Qlg6oAoxF64t9miZ0BB--z0r6m_NBNdaIkR3QrEg7qCZSd74EGx9g9NTouHSoolk99FiWKYsPBfMvoofKkqOkj?key=2ms7aSILnOUvzUjqc2G4lg" alt=""><figcaption></figcaption></figure>

#### Kết quả

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXe6fiKCC6qu8alNGAHGPDr1FGdU3tlwi58vVNYshIdCpdqSBpI7Xk0IaXip6pCvzqrIhaZQ46OrxoMKj75QAoLZUxivjGQdXgUCHGDNGlxCUjgzwufcpIoxPHd3G9PwazQv5LimHflGuat_b49AsAAhJRQ?key=2ms7aSILnOUvzUjqc2G4lg" alt=""><figcaption></figcaption></figure>

Không chỉ dừng lại ở khả năng cập nhật các thông tin, các yếu tố trong hệ thống mà người dùng bây giờ đã có thể tương tác với các khách hàng, đối tác bên ngoài ngay trên Luklak với bước đi đầu tiên là gửi email theo yêu cầu. Ví dụ như sau khi thanh toán xong cho nhà cung cấp và chuyển trạng thái mục sang hoàn thành, hệ thống sẽ tự động gửi email xác nhận thanh toán đến nhà cung cấp hay khi nhận hàng không đủ theo yêu cầu, người dùng thường sẽ phải thống kê lại các số liệu, thông tin liên quan sau đó gửi email xác nhận thiếu hàng và yêu cầu nhà cung cấp giải trình và đưa ra phương án khắc phục. Tuy nhiên với Automation của Luklak, những công việc thủ công đó sẽ được hệ thống thực hiện một cách tự động. Người dùng chỉ cần tạo ra một quy tắc (rule) được kích hoạt khi chuyển sang trạng thái NHẬN HÀNG & KIỂM TRA, điều kiện nếu Chênh lệch > 0 (Chênh lệch = Số lượng yêu cầu - Số lượng thực nhận) thì hệ thống sẽ gửi email đến nhà cung cấp với nội dung yêu cầu nhà cung cấp giải thích kèm theo dữ liệu từ các trường thông tin Số lượng yêu cầu, Số lượng thực nhận, Chênh lệch, Lý do. Còn nếu điều kiện không đúng thì gửi email với nội dung đã nhận đủ hàng

#### Cấu hình

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXc2ZCKosUDWUAgFCYFViGBaJwpMxuWFIp5iGwlT7uFNR2Q1hKmx7tlcaKXxFXTzP1BJFXbuWxa3EsTAWZFmGWvjSR4ougOMtwmsMONlMC3tz8hnjphapS6lw4D7_bspsjGd9j5oqud6G8uJO_lDbv6BnA4?key=2ms7aSILnOUvzUjqc2G4lg" alt=""><figcaption></figcaption></figure>

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXd8Mm5U8LHMF-RFTXQIXj0Gd5sifC1ru3aYUte6axksg3Ijx8DBQ_mfuq7w5dnzomNVM2hBQfUMVe4Zjy1uYpY_pHYa5M0R_EyNxdJs1ftVLBqLGR5Am20PN8Bc-5HDyTAVtOXhzZq9LwPt0H1M4gIJ69GF?key=2ms7aSILnOUvzUjqc2G4lg" alt=""><figcaption></figcaption></figure>

#### Kết quả

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXc1xilnI9CTvdOdf141P9lyc1PwjO1rnII83Kvsw68JLWB9_gtCdDKZGi5qfR88rHB-eeMcRqSalyti1no1lQa7n960MHIaydrcH-Yk3tQ0pqA6x_DHpzMo9NV10EiKNSwSgG_KzL6rAFpUfKpMEEGUkY5b?key=2ms7aSILnOUvzUjqc2G4lg" alt=""><figcaption></figcaption></figure>

#### 2, Mục đích sử dụng và tính ứng dụng

**Mục đích sử dụng:** công cụ tự động luôn là một trong những công cụ hỗ trợ rất nhiều trong quá trình làm việc của doanh nghiệp. Với công cụ Automation, người dùng có thể tạo ra trước các quy tắc tuỳ vào yêu cầu của doanh nghiệp, yêu cầu của phòng ban hay các tiến trình công việc và qua đó, hệ thống sẽ tự động thực hiện các hành động theo quy tắc được cấu hình trước đó

**Tác dụng:**&#x20;

* Hạn chế các công việc thủ công lặp đi lặp lại trên hệ thống:&#x20;

Các công việc lặp đi lặp lại không thể tránh khỏi sẽ đem đến cho doanh nghiệp tiêu tốn nhiều thời gian, nguồn lực về người và của mà đáng lẽ có thể sử dụng để làm những công việc quan trọng, hữu ích và đem đến nhiều lợi ích hơn. Chính vì vậy, khi áp dụng Automation vào hệ thống để thực hiện các công việc lặp đi lặp lại theo quy trình làm việc sẽ làm giảm khối lượng công việc nhân sự cần phải làm và làm tăng chất lượng công việc được hoàn thiện khi hạn chế được các sai sót về mặt tính toán số liệu, sai lệch thông tin,... xảy ra khi ngày trước, nhận sự vẫn phải thực hiện những công việc này một cách thủ công

* Tăng khả năng cạnh tranh và gia tăng lợi nhuận một cách gián tiếp

Khi áp dụng Automation, người dùng thực hiện các công việc tốt hơn, tiết kiệm thời gian hơn và cũng tránh phạm phải các sai lầm không đáng có một các triệt để nhất vì lỗi con người thực hiện sẽ không còn nữa, chất lượng công việc cũng được đảm bảo và cải thiện, chi phí và công sức phải dành ra cho một công việc sẽ được giảm bớt đi rất nhiều. Qua đó doanh nghiệp có thể tận dụng tài nguyên vốn có của mình một cách triệt để và tạo ra nhiều lợi ích, doanh thu hơn so với trước kia, so với các đối thủ cạnh tranh trên thị trường

* Tăng độ linh hoạt, nhịp nhàng hơn trong việc phối hợp làm việc với các phòng ban trong tổ chức

Việc phối hợp nhịp nhàng giữa các phòng ban là một trong những yếu tố then chốt giúp doanh nghiệp có thể phát triển một cách bền vững và mạnh mẽ. Điều đó sẽ rất khó thực hiện khi bộ phận này đã thực hiện xong công việc nhưng đến khi bàn giao cho phòng ban khác thì lại gặp trục trặc, sai sót như quên thông báo, đã tiếp nhận công việc nhưng quên không tạo mục trên hệ thống, hay cung cấp và nhập liệu sai thông tin,...  Tuy nhiên, đến khi áp dụng Automation vào quy trình làm việc trong doanh nghiệp, các công việc liên kết, thông báo, tạo mục công việc,... giữa các phòng ban sẽ được hệ thống hỗ trợ ít nhiều, giảm thiểu rất nhiều các sai lầm cũng như hỗ trợ việc kết nối, làm việc liên phòng ban trở nên dễ dàng và tiện lợi hơn bao giờ hết

* Tuân thủ nhất quán quy trình làm việc

Khi đã áp dụng Automation vào tiến trình công việc trên hệ thống, các quy tắc người dùng đưa ra khi thực hiện công việc sẽ được hệ thống đảm bảo thực hiện mà không gặp phải một vấn đề hay tắc nghẽn nào. Chính vì vậy, nó tạo cho doanh nghiệp những tiến trình công việc theo luồng một cách thống nhất, quy củ nhất trong nội bộ hay liên phòng ban, tránh được các trường hợp mỗi người thực hiện công việc theo một ý khác nhau và khiến quy trình công việc rối loạn, ngắt quãng



#### 3, Giao điện màn hình và hướng dẫn sử dụng chi tiết

Để có thể sử dụng được chức năng automation của Luklak, người dùng phải tạo ra các Quy tắc để dựa vào đó, hệ thống sẽ thực hiện các công việc mà người dùng yêu cầu.

Người dùng có thể tạo quy tắc ở 4 vị trí với phạm vi ảnh hưởng khác nhau. Chúng bao gồm Automation trong chức năng (Function), trong mảng việc (Space), trong khu vực (Area), trong folder. Các cài đặt các quy tắc ở mỗi vị trí đều như nhau truy nhiên dựa vào mục đích sử dụng và phạm vi ảnh hưởng mong muốn, người dùng có thể cân nhắc xem tạo các quy tắc ở đâu để tránh các sai sót không đáng có.

### Hướng dẫn chi tiết tạo và cấu hình quy tắc

**Bước 1:** Người dùng di chuyển đến vị trí muốn áp dụng automation trên phần mềm sau. Nêu người dùng muốn tạo ở mảng việc hoặc khu vực thì cài đặt automation sẽ nằm trong phần Xem chi tiết -> Nhấp chọn Tự động -> Nhấp chọn Tạo quy tắc

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXdw2_8IjyzNHPxdwXfMcxj6If4Pq666dpYkLYefnKFSsPYGEEQbauf5yPE9F5138wFrzO2Bal1DiVZtUtqJVbW79P3FsSufqBVtWbnoiUAAZAd_cN7hfVSfFwbUhfPm_ZtYPcq0OqDovRwMMO-Tb5U5XD2B?key=2ms7aSILnOUvzUjqc2G4lg" alt=""><figcaption></figcaption></figure>

Còn nếu người dùng muốn cài đặt tự động trong chức năng, người dùng di chuyển đến vị trí cấu hình chi tiết cửa chức năng muốn cài đặt và nhấn chọn phần Tự đồng - > Nhấn chọn tạo quy tắc

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXcYzovpZ-bZpgpFloGKhfYKi9EkJi6i7HNXgdRKoaajhCgD_8mefEvezArkc8sgUoxYEJ2_Jdz-rrr06yXPYGtZBodBAx41k3rhMP_QwW_wgdgyJYSK6lj71qY14K-DQi-6C4jxJfFrlg8_lGbw_SNdk-4?key=2ms7aSILnOUvzUjqc2G4lg" alt=""><figcaption></figcaption></figure>

**Bước 2:** Sau khi nhập chọn Tạo quy tắc, hệ thống hiển thị giao diện Tạo quy tắc yêu cầu người dùng nhập các thông tin cần thiết và nhấn chọn Tạo

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXcxAjUncXOdIxZ26z-wwvhjNrb9BQhHRDnc6r3tBbhguoke94z21D6onf9RNk1hrE9FiKKb_3xLV1MSZrZXuaX3-yRK8wCE0eA9NyOss_pMOedaAVTRRYcZHzGC8KVb1CUQQFF48KJaJmh383NkJtQAJ90?key=2ms7aSILnOUvzUjqc2G4lg" alt=""><figcaption></figcaption></figure>

_**\* Lưu ý:** Ở đây có 2 lựa lựa chọn để tăng hoặc hạn chế phạm vi ảnh hưởng, tác động của quy tắc bao gồm:_&#x20;

Chọn để cho phép các hành động của quy tắc này kích hoạt quy tắc khác (1): Nếu tích chọn ở đây, người dùng sẽ cho phép các hành động được thực hiện tự động ở những quy tắc khác tác động đến quy tắc này

Chọn để cho phép các hành động của quy tắc khác kích hoạt quy tắc này (2): Nêu tích chọn ở đây, người dùng sẽ cho phép các hành động được tự động thực hiện ở những quy tắc này tác động, kích hoạt quy tắc khác

* **Ví dụ:** Quy tắc A thức hiện hành động Tạo mục, quy tắc B lấy hành động Tạo mục làm cách kích hoạt. Quy tắc A tích chọn phương án này (2) và B chọn phương án (1).  Nếu vậy khi quy tắc A được thực hiện cũng sẽ kéo theo quy tắc B được thực hiện

**Bước 3:** Người dùng tiến hành cấu hình quy tắc với yếu tố đầu tiên là Kích hoạt. Người dùng sẽ chọn ra các hành động thức hiện trên hệ thống để kích hoạt quy tắc. Bên cạnh đó, Luklak cũng cung cấp cho người dùng công cụ Điều kiện lọc để người dùng đưa ra các điều kiện mà hành động kích hoạt cần đáp ứng để kích hoạt quy tắc

Các kích hoạt phần mềm cung cấp bao gồm

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXcSQrErgiPCpgmMPiV6OWJnpbocl3px07mhdiBzGAR_Zx0X-RiRWbIFTpRYgeInMe1aPZcZYD26I3TPex9eFLcLV8Rik73oBAN0z2SqDx8bFOS1kmcWsryrAMZWWsN-JmOX_n0Wg1V6tbMlh0QH06A9JfOp?key=2ms7aSILnOUvzUjqc2G4lg" alt=""><figcaption></figcaption></figure>

* **Tạo mục**: Kích hoạt khi người dùng tạo một mục trên hệ thống. Người dùng có thể thêm điều kiện mà mục được tạo cần đáp ứng để kích hoạt quy tắc ở ngay trong Kích hoạt. Ví dụ Hành động tạo mục những mục được tạo phải là mục Bán hàng và tạo trong Mảng việc QL bán buôn - NC

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXfYri-8_TmnIzSW-Mh2z6kq95ufxzExngHEF_X1y_bCYb6PPhvSLyZQChmyNlepO9wCdW5OURX_Rr8HIhXua1ipG2QmtgdSR5EA-n2m3Byhsmsve8dpFXHOpstwDkf6Boop9pOk11G5v3yG7ftMqmY7hQHc?key=2ms7aSILnOUvzUjqc2G4lg" alt=""><figcaption></figcaption></figure>

* **Chuyển trạng thái:** Kích hoạt khi người dùng thực hiện hành động chuyển trạng thái trên hệ thống. Người dùng có thể cài đặt chuyển từ từ trạng trạng thái nào đến trạng thái nào hoặc từ loại trạng thái nào đến loại trạng thái nào thì hệ thống mới kích hoạt quy tắc.

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXdbpA2jFOy8cNaxaIpI7RQjNZ4W8OMk_zH6te6DCHsfPZQ7ys4qoqRxATnqWytdMelq8E3skA7lQ-dWCZHjRSg7S_7Qin-kM6L7Pbw6rK5A5L1D0W3e8HK_zYrBPRoeWyj_1HGE1ti7A8oReKx_DSeuvjT9?key=2ms7aSILnOUvzUjqc2G4lg" alt=""><figcaption></figcaption></figure>

* **Cập nhật trường:** Kích hoạt khi người dùng chỉnh sửa dữ liệu của các trường thông tin đã được lựa chọn để kích hoạt quy tắc. Người dùng có 2 lựa chọn để chọn ra trường thông tin kích hoạt bao gồm:
* **Bất kỳ trường nào:** Người dùng tác động đến dữ liệu của bất kì trường thông tin nào trong phạm vi tác dụng của automation và thoả mãn được điều kiện lọc đã câu hình trong điều kiện đều sẽ kích hoạt quy tắc
* **Trường cụ thể:** Người dùng lựa chọn ra các trường nằm trong phạm vi tác động của automation để đến khi tác động đến dữ liệu của các trường đó theo cách thức cập nhật đã lựa chọn thì sẽ kích hoạt quy tắc

Các cách cập nhật bao gồm:&#x20;

* Tất cả cập nhật
* Khi chỉ sửa
* Khi chỉ thêm
* Khi chỉ xoá
* Khi thêm và xoá&#x20;
* Khi thêm và sửa
* Khi sửa và xóa

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXdpC8f2UFIO_StB9TmKElB6fFTdEhPo8LWKQDnq0cUhnuNmQCPde2v_U98j8d5j7GtPR9aBdcvZghEwLoR7tmGh1yY_3qD1kY1Ds_yIeszwdAtqXjBd62z57-mwbhKHV7h_mZpYI1ig50eSPA-R_nNrO0L6?key=2ms7aSILnOUvzUjqc2G4lg" alt=""><figcaption></figcaption></figure>

\


* **Lịch trình:** người dùng cấu hình một thời gian biểu, lịch trình cố định để dựa vào đó, hệ thống sẽ dựa vào đó để kích hoạt quy tắc mỗi khi thời điểm kích hoạt đến. Ví dụ mỗi 15 phút thì kích hoạt quy tắc hay 8 giờ sáng mỗi thứ 2 hàng tuần sẽ kích hoạt quy tắc. Ở phần Kích hoạt Lịch trình này, người dùng sẽ cấu hình 3 phần:
* **Chọn lịch trình:** chọn ra lịch trình, các thời điểm để kích hoạt quy tắc. Người dùng có thể lựa chọn nhiều loại lịch trình để cấu hình ở đây bao gồm:&#x20;
* Theo phút

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXf_YQpZfsSRaNh0zinhkDI8D6FlEhhpcZgLcWBUglOb1bxEKnt8_M_DAFl-XqUQlp_gqpiEIwb2NAd5zwmajy_bfHKFvmwhmv3cXulZPXT6vvSiCL8-LoRKmtWBN0qJXDUxGjnUFWLdJExVmIArYyuu0v4?key=2ms7aSILnOUvzUjqc2G4lg" alt=""><figcaption></figcaption></figure>

* Theo giờ

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXfOTWP1BwYxna4xxNRTi2o_ui5OubSAhHB_DWX0-fxaBZAIaYEto7-ynfGhZbfi7bUxeIrhj1HvRn3VNbnIs_J6wn1ADtIk6fC6MAzMY5wRn5qgKVvR5y29q9N9wdFrMRo02XFKqZumOM7a0p8d0pA60rZL?key=2ms7aSILnOUvzUjqc2G4lg" alt=""><figcaption></figcaption></figure>

* Theo ngày

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXdUBeIpYeyCt0m2hU6pzjQKhbDim0D6GmtVM5Xy68hNJiuQaC7i6OWmDYf0VPh0XXb6mbluXRnmRGjWR1YIxd1N6KQrOCwr1HF84xbPnulxJIZ2SuIiCzbXTn6KL6oH33dG1_2E-F0h9Aj0EMC1CyGW5n8X?key=2ms7aSILnOUvzUjqc2G4lg" alt=""><figcaption></figcaption></figure>

* Theo tuần

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXfQrwoYoxeM3Z0iz0EAi7kFwMhUAO9vNmVQwKNRJNHxjsxKjIPsPdnlcsD_dmUj1sMAnArr9z99MAbtbyy9dYg2_g_UFF6GHnlywWLTJD9zfp8OCjfRFaIJIKfH3K0Wcm8zW_q_RrM2UX12ZC7xcJgFmX29?key=2ms7aSILnOUvzUjqc2G4lg" alt=""><figcaption></figcaption></figure>

* Ngày trong tháng

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXeZ0xCkr5fhs1IYV1qFP5NX64qQwR6RPXqhJMaUpiX5s43dAPU4MLIb83P7863AAQESV-CpqDzDIkhOGN_GPGOw6KBoVy4ic6Lh44MYXvfUV0BMpDSEDIaAOf4TxJv1cJTaJqhovEKj-wYeSRX9ThggkbI?key=2ms7aSILnOUvzUjqc2G4lg" alt=""><figcaption></figcaption></figure>

* Thứ trong tháng

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXcSOpqYIHuR4yXiZHc3fNlL65Gr0CfIoAQ9_nFaS7m4bXzDnPt1xAyJUDX7n3kM26yDTEH1u5Aabm7YGTjUZRKGMYdK4vDCTBjY3JsXPRNGyCcszjTX1DyeVzS3N5DTsgLMncjgnEkOEzuBbGbYoJpV1WZC?key=2ms7aSILnOUvzUjqc2G4lg" alt=""><figcaption></figcaption></figure>

* Tuần trong tháng

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXdOfETEF2T9xjIEzp_YGGC7_knQG1PO-dnnMaKQ8QocLZ3p6s7KrSvuDrxLq49wxq1uM3o7BUg3jD3UbmXJHySezJnHdf1DuPjOXJ-09nPc22yS1A-Y_7D7zdnox-TW5hERPoRRlp55W2uqmSLrTRpGwcia?key=2ms7aSILnOUvzUjqc2G4lg" alt=""><figcaption></figcaption></figure>

* **Điều kiện lọc:** đưa ra các điều kiện mà các hành động kích hoạt cần phải đáp ứng để kích hoạt quy tắc

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXekhBAT0NlLm6CrsqqA-XMKD38plwvEXdRqhhe6OyOy-EUHcUs2fMT0p1iP4m5r72s72jG4T4yrGhAdO29hnG0JIaO3ijvp-dK6EXdEMYErMoldWSRzUws-MRBFphcoGPrC64GXrnegLpTpFSRgIcnOU6h8?key=2ms7aSILnOUvzUjqc2G4lg" alt=""><figcaption></figcaption></figure>

* **Cách cắt chọn:** người dùng đưa ra số lượng các mục để hệ thống có thể thực hiện hành động khi quy tắc được kích hoạt. Người có thể chọn 1 trong 2 lựa chọn để chọn ra các mục có thể thực hiện hành động là&#x20;
* Tất cả các mục thoả mãn: hệ thống sẽ sắp xếp các mục đã đạt yêu cầu ở Điều kiện lọc và chọn ra 20 issue được cập nhật trong thời gian gần nhất để thực hiện hành động khi quy tắc được kích hoạt
* **Cài đặt nâng cao:** tại đay, người dùng có thể chọn ra cách sắp xếp các issue đã đạt yêu cầu ở Điều kiện lọc (sắp xếp theo trường dữ liệu nào, tăng dần hay giảm dần) và lựa chọn Số mục được chọn để thực hiện hành động (tối đa chỉ chọn được 20 mục). Hệ thống sẽ lấy các mục ở đầu danh sách sắp xếp cho đến khi đủ số lượng người dùng yêu cầu

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXdJWoNjNIoKj_gI41yDvzodu_rS2AQ4_1qBGVeKj36hv1Y75l9Re5jWWtiif-yGo0X9eF7RwK7QQRCUFRUv-DRZQnxITbqkgt2yGBm4FBcZlSrMwi05Rvx3vXiOlvDm1XGW3b5O5wQXkBxl0q0laTzgcG8?key=2ms7aSILnOUvzUjqc2G4lg" alt=""><figcaption></figcaption></figure>

* Kết nối mục:&#x20;
* Xoá mục
* Xoá liên kết mục

**Bước 3:** Cài đặt điều kiện

Hiện tại Luklak đang cung cấp cho người dùng 2 loại điều kiện với các cách thức hoạt động khác nhau là If/ else và Multi-path

* If/else: thiết lập điều kiện rồi sẽ chạy theo 2 nhánh, nếu đúng chạy nhánh này, sai thì chạy nhánh còn lại
* Multi-path thiết lập điều kiện ở mỗi nhánh, nếu đúng điều kiện mới thực hiện các hành động tiếp

**Bước 3.1:** cấu hình chi tiết điều kiện if/else

Người dùng nhấn chọn vào biểu tượng dấu chọn biểu tương If/Else để sử dụng loại điều kiện này

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXdf64BrdAsI0OSOQj39a80QwkIRtHyAhgBIcXSTKoG1o6bxmYfKpfxhbCye7rqzRrrPR3o7eVOVR0ZMc62vUcLD2IiGHnrAH11ohzx4ftxUJGq7LBiOHmJVTScMveAxELXmeYH9WbrCzGH_tTTqX2xBg6yB?key=2ms7aSILnOUvzUjqc2G4lg" alt=""><figcaption></figcaption></figure>

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXddCyiF-DIx-5ddoUYIGoDf_EZOUpAr3BHFvpWtyjB7O0V7MR6BY4Ey2_r9RYqg4HIiqp2lXxrHtOoKBYtyX1S9SiRkBFwRRuWt0x5iW0S4Nc9LUj63_7bg8Z0Y1SGX5SVsXLzjHoxUBEujE2sGdX3B6p0?key=2ms7aSILnOUvzUjqc2G4lg" alt=""><figcaption></figcaption></figure>

Người dùng nhấp Chọn điều kiện -> Chọn điều kiện muốn cài đặt -> Hệ thống hiển thị màn hình cài đặt -> Người dùng tiến hành cấu hình

&#x20;

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXf6S3ExXWau7mj1bOJDDlbgyzDFTQ-6WM3mtn_OeGM5l86VnTHI7ZOQL27azRRymmz0mPHAlCNVhzZOwqL6QAiCvsTTIwPdOKHnL5CMPplWq4WLCVXme1A7WCFPuw0VgUJvb9qMKukRzoloQkGip6rQZK8H?key=2ms7aSILnOUvzUjqc2G4lg" alt=""><figcaption></figcaption></figure>

Các điều kiện Luklak cung cấp cho người dùng cài đặt bao gồm:&#x20;

* **Trường dữ liệu:** sử dụng các trường dữ liệu có trong hệ thống để cài đặt điều kiện. Ví dụ các issue kích hoạt hành động hay được chọn ra phải đáp ứng các yêu cầu như trường Giá trị hợp đồng phải > 100000000 và trường Phòng tham gia có giá trị là Kế toán.&#x20;

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXe0i4WFnigwtGCOWkbsLzszJ6jV7XhUy1Fl2meybfD0nvR3wepEKryNNK8F4IjyAw-wE9cdsI0VcBKC-Fw4LDqmf5eQdtjEa4QhHF7MSsMc6fwEsCpXDJARlKHpsbSdh497rw7CxcNfeJhKMo4VTP2lO55C?key=2ms7aSILnOUvzUjqc2G4lg" alt=""><figcaption></figcaption></figure>

* **Mục kiệm:** cài đặt các điều kiện liên quan đến mục kiểm về mức độ hoàn thành. Ở mục kiểm, người dùng sẽ có 2 các cấu hình bao gồm:&#x20;
* **Tất cả các mục kiểm đã hoàn thành:** Yêu cầu tất cả mục kiểm đều đã được tích hoàn thành mới đạt điều kiện và cho phép hành động cấu hình phía sau được thực hiện

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXdBAON_FiHNqyW4CXYnVFUJRv0hu_8xpMngdebuqxQPFpxEQFucUeoa1eWYykst7et6AI6vTsbXYnu5zN2Mih6VWczkXLnYvuzu6JoSheyneFDRIGHQ86iqSZlJb43FwXjddMnp8GQimLyfHtu0ST_B_hZV?key=2ms7aSILnOUvzUjqc2G4lg" alt=""><figcaption></figcaption></figure>

* **Cài đặt nâng cao:** Người dùng có thể cài đặt điều kiện chi tiết hơn, yêu cầu chính xác số lượng hoặc phần trăm số lượng các mục kiểm ở trạng thái mà người dùng yêu cầu mới cho phép thực hiện hành động cấu hình phía sau. Ví dụ số lượng mục kiểm phải được hoàn thành trên 50% mới cho phép thực hiện hành động

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXdntpm4F-uXMW5nAwcgwVdf4yuQ5zeu4hxMcSdWvK-E4ruWv9StRwK6eCsz5lBkufBmo5ORr4N8y0AmAb5FWLo80S-14TfoChLDjNqpOU5LeAQjBcsEhIkE4FZt6vrxwIz18Gywh1ovrv0RJq3SNUG7q3Q?key=2ms7aSILnOUvzUjqc2G4lg" alt=""><figcaption></figcaption></figure>

* **Mục con:** cài đặt các điều kiện liên quan đến mục con về trạng thái của các mục con đó. Ở mục com, người dùng sẽ có 2 các cấu hình bao gồm:&#x20;
* **Tất cả các mục con đã hoàn thành:** Yêu cầu tất cả mục con đều đã được chuyển sang nhóm trạng thái HOÀN THÀNH rồi mới cho phép hành động cấu hình phía sau được thực hiện

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXeMnTlD5bmNMioECjp8jwJzUgwVRJRATGJDzv2BUCP7LeIq9e7CERyL2FLVlrqQb4ZKTMMwlm_TukfTW9gWocJmKVHuk8IKjsGZlJzyXHzOY_BSCmpIWzf-yq3hqPG2fDxwjbhbAsqagQXRufKUADWSEAW3?key=2ms7aSILnOUvzUjqc2G4lg" alt=""><figcaption></figcaption></figure>

* **Cài đặt nâng cao:** Người dùng có thể cài đặt điều kiện chi tiết hơn, yêu cầu chính xác số lượng hoặc phần trăm số lượng các mục con đạt các yêu cầu mà người dùng cài đặt ở Điều kiện lọc rồi mới cho phép thực hiện các hành động cấu hình phía sau. Ví dụ số lượng mục con có trạng thái ĐÓNG HUỶ < 10% mới cho phép thực hiện hành động cấu hình phía sau

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXdarVn7qHvEH-319nEV4zW2rGVYeMEVe26YEFVTWo8Y5aN-p9JWzeeuKKWYpEaeD_Dlhe4m7tgEvu54gXMWMRE4ChFGIGi7FF1F_ajFVMXc-zWVANooMpOHllzOIpIZPDey9eoZLMj6McmqHaiFB5GJc9_r?key=2ms7aSILnOUvzUjqc2G4lg" alt=""><figcaption></figcaption></figure>

* **Kết nối mục:** cài đặt các điều kiện liên quan đến các mục kết nối với mục kích hoạt. Ở mục kiểm, người dùng sẽ có 2 các cấu hình bao gồm Tất cả các mục kết nối đã hoàn thành và Cài đặt nâng cao. Tuy nhiên trước khi câu hình, người dùng cần chọn loại kết nối trước. Loại kết nối sẽ hiển thị danh sách tất cả kết nối người dùng có trên hệ thống.&#x20;

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXcq4yWmKzbhKHrN6dgC30c1ZOyFcEvSNizXnhYsjwkywChuf1nq500NdjTb6KmMhqZ0UyMo8ce-W9buIh9DEeGNI2s1HPgMs__7dzk7oumLfML6rwc4rAAxbjbSc0CrI7IuI4Xvd4L1IQ3Fh7_LsvAEA4_T?key=2ms7aSILnOUvzUjqc2G4lg" alt=""><figcaption></figcaption></figure>

* **Tất cả các mục kết nối đã hoàn thành:** Yêu cầu tất cả mục đã kết nối với mục kích hoạt đều đã được chuyển sang nhóm trạng thái HOÀN THÀNH rồi mới cho phép hành động cấu hình phía sau được thực hiện

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXcoS7AJHuyx-u2GxyPgBKrGig6bC60ENtBjKrS62nPwS5OMD82Adi3nTmWCERxLTqjwnd5zAdZYVdcC7sc23Zr7AV7jJcFsmOZpwU8hdyvtS2ygPtoJJF195T9MX5DyLe9PZSTqpBV7eNB2RaryVNPLXj2a?key=2ms7aSILnOUvzUjqc2G4lg" alt=""><figcaption></figcaption></figure>

* **Cài đặt nâng cao:** Người dùng có thể cài đặt điều kiện chi tiết hơn, yêu cầu chính xác số lượng hoặc phần trăm số lượng các mục kết nối với mục kích hoạt đạt các yêu cầu mà người dùng cài đặt ở Điều kiện lọc rồi mới cho phép thực hiện các hành động cấu hình phía sau. Ví dụ số lượng mục kết nối với loại kết nối Chăm sóc khách hàng/Xác nhận có trường Mức độ ưu tiên = cao và ở trạng thái thuộc nhóm HOÀN THÀNH >= 70% mới cho phép thực hiện hành động cấu hình phía sau

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXeoTaPaXn6FVxTgDlLDfzavdUIi-dx4AXa4Is4SK3gE6KdgQ9KokKgGakhEH7Z3xq9rg9Ij_AY_wCVw7OafYshCp4yWMiEc4XTp7BL89R_jrLSiCNLhe2MVnLR1SKFizoGjtNodcXM9qzO6r0fBkwjcKANN?key=2ms7aSILnOUvzUjqc2G4lg" alt=""><figcaption></figcaption></figure>

#### Bước 3.2. Tiến hành cấu hình chi tiết điều kiện Multi - paths

Nếu người dùng cần sử dụng nhiều điều kiện hơn, nhiều lựa chọn và phương án để thực hiện công việc mà If/else chỉ có thể đưa ra 2 lựa chọn là đúng và sai cho 1 điều kiện thì Multi - paths sẽ giải quyết vấn đề này. Với multi - paths, người dùng sẽ không bị giới hạn về các điều kiện hay phương án có thể đưa ra. Và với mỗi phương án, điều kiện đưa ra, người dùng cũng có thể đưa ra các hành động tương ứng với điều kiện, phương án đã đưa ra

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXfaMx5v5cUG5OnJc4u29y5L6jY7akkTfCfkuNBvolQOv6xgxnc890D-Y3E251XAChiakmJ7byUP3F37q7IJnG5siDWxLGJ_5hfWL03YvsmAYU4VLgp1WW_lnEWKqGubAsI17Ao-yW8eUJtkHMQeA03zVsY?key=2ms7aSILnOUvzUjqc2G4lg" alt=""><figcaption></figcaption></figure>

Để tiến hành cấu hình chi tiết Multi - paths, người người dùng nhấp chọn vào biểu tượng dấu cộng, nơi muốn sử dụng Multi - paths -> chọn Multi - paths

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXctrTYgThPyfWv-_Aw7cKpDKQGP1yLp99-KsxDlu_y7z0tgngXju0swZpDqe1WI4R90gEC5yiiMCRoS85bJoF2WaWuzy5mHjdy9liofjBhJZNymK8faHESu04vusCp9uMHJ6OJ_O498ReFoUeoNhzNN2Yye?key=2ms7aSILnOUvzUjqc2G4lg" alt=""><figcaption></figcaption></figure>

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXcLtu5lFT3K513oqwcVaSEPFea6TOYnON5mm1JIVo2YWsmxnreIIOSpdEH8gZouvmpy0-qm-lirqe3au6qR-guqZrFb1DI1zb6VyT_SjU_6jHOPfVHS5WGdoEQJMgxzRTGqNLYUXa2NBxlBqFUGT3BZa-o?key=2ms7aSILnOUvzUjqc2G4lg" alt=""><figcaption></figcaption></figure>

Sau khi lựa lựa chọn Multi - paths, hệ thống sẽ hiển thị màn hình 2 đường Paths. Với mỗi Paths, người dùng có thể cài đặt vào đó một điều kiện và một hành động tương ứng khi các issue kích hoạt thoả mãn điều kiện đã đặt ra trước đó. Người dùng có thể đặt ra thêm nhiều đường Paths với các điều kiện và hành động mong muốn. Để thêm đường Paths, người dùng nhấn vào AddPath để thêm đường Paths cho đến khi đủ yêu cầu của người dùng thì thôi.&#x20;

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXfIe2GzUTZ_WhGc8yNz_n5EPo6xu5AAcHJofd9Q1FHNvHe-0a1ixhl6g2V_5HacvFOozda8JX-cy8OfTgFNO42jpLW_5lqsSTwE7cBWGdTabwAzohvywiLFDkkOyc2P6EFpUdqmfgFdbHzEeEWYTIFwwm1W?key=2ms7aSILnOUvzUjqc2G4lg" alt=""><figcaption></figcaption></figure>

Ở phần cài đặt điều kiện với mỗi đường Paths, người dùng nhấn chọn Chọn điều kiện ở nút Path và lựa chọn điều kiện muốn cấu hình.&#x20;

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXceTvz6intXo4ljGOytB0JC-uY7fW-j5erKHhP3XxXNMvlptg7L34vQOJsRhy4sCwup3OhX7-fJxQBBDDIRpJqKH6Py_0_8GqUASIUTm-PppbZDm8bRQ5VzIzbIBl0m9jExOuoGGLTe685L3XAC9H8DsB9t?key=2ms7aSILnOUvzUjqc2G4lg" alt=""><figcaption></figcaption></figure>

Về cách cấu hình điều kiện chi tiết thì Multi - paths không khác gì với If/else, người dùng có thể xem phần cấu hình chi tiết điều kiện của If/else và thực hiện.&#x20;

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXcJhFjko7dYNhwAi_X0b9Xoofqc3a7gQ3ZkSUEuoptxjhG_bZEgZXn7Zhv-OCTx1Nqo3w07l850qRTHBaZqo2l9zCL_NWGPpzdJYC7rbi1JDoP4mYY9AeNzHXINgU8ziM8tuCzaJkaH1KgiXnzffglQpl1C?key=2ms7aSILnOUvzUjqc2G4lg" alt=""><figcaption></figcaption></figure>

Lấy một ví dụ như hình trên, ta có thể thấy được sự đa dụng và đa dạng trong việc đưa ra các điều kiện và các hành động. Như ví dụ trên, nếu trường Giá trị hợp đồng ở mục kịch hoạt hành động có giá trị < 100000000 thì hệ thống sẽ chạy theo đường Paths thứ nhất và thực hiện hành động chuyển trạng thái sang HOÀN THÀNH. Còn nếu trường Giá trị hợp đồng có giá trị > 100000000 và các mục kiểm đã được tích hoàn thành thì hệ thống sẽ chạy theo đường Paths thứ 2 và thực hiện hành động chuyển trạng thái sang HOÀN THÀNH. Với 1 trường hợp nếu trạng thái là THẤT BẠI thì sẽ chạy theo đường Paths thứ 3 và thực hiện hành động chat thông báo vào kênh chat mảng việc kích hoạt hành động.

Sau khi đã thực hiện cấu hình điều kiện hoàn tất, người dùng tiến tới cấu hình hành động (Action).&#x20;

#### Bước 4: Cài đặt hành động (Action)

Nếu người dùng có sử dụng điều kiện hay rẽ nhánh thì hệ thống sẽ hiển thị sẵn cho người dùng những nút hành động để người dùng có thể tiến hành cài đặt.

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXd9wbVN33gj7oLZVB5fU28s8H7V1EYJ0IWIze3FIjc2waNg3pXC3Ftc2w4MR0Xj8sBb0QgP-U0Twf9ljcE4KhIov-EyFe0KikA-_FLViJjZDNyShr0rPyrGeX6NkGGHa5qFKCeXkvbaqs0ErJkajGUShOV6?key=2ms7aSILnOUvzUjqc2G4lg" alt=""><figcaption></figcaption></figure>

Còn nếu không sử dụng điều kiện hay rẽ nhánh thì người dùng có thể nhấn vào biểu tượng dấu cộng -> nhấn chọn Action -> nhấn chọn Chọn hành động để tiến hành cấu hình hành động (Action)

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXfx2fZi15nBJjts5kqC5r_wh92xXLxZ0jWWVbs89MmCQRADGZRTVgOoPhsz14I_XA81XlCEaV3SH798BsPWDKRxPt2JpXZDubmrPfkNTNn6YDmLY0it6Scv_HakIHA7Ncy3pbXUK7aiY10_aJOD3IFUzG3q?key=2ms7aSILnOUvzUjqc2G4lg" alt=""><figcaption></figcaption></figure>

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXd_y9_Gct0PCAfky5NLHhDkIj4l_wHcXHsL_NTSkPqgJ_b_W4EyawAL7WK5-vSs9pkzVA0_q2M6QRd8Iefp0bs2oa-0ruVoJZwT3aLdyiLXLHGZaVMGb1YZOMopE4wZwNKD5SjC7ixgIXoK_rMfZCQzjQSB?key=2ms7aSILnOUvzUjqc2G4lg" alt=""><figcaption></figcaption></figure>

* **Tạo mục:** hệ thống thực hiện tạo mục theo các cài đặt mà người dùng đã cấu hình. Ở đây, người dùng sẽ tiến hành cấu hình ở 2 phần bao gồm
* **Thông tin cơ bản:** bao gồm các thông tin cơ bản về mục muốn hệ thống tự động tạo gồm thông tin về mảng việc nơi muốn tạo mục, mục muốn tạo là mục nào, mô tả của mục vừa tự động tạo và tiêu đề của mục đó

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXcbiSJF7cb2sl8l4ex_fPq_yhPF7zQzOOY6ckQZ85DJgJGQdAeu748jLi957oXgB3_DiY7D-paA__d5Dq3XfMF3vCphdX4X0GS2exZHwAQMUU0i2pBpzfiWZxhtf7jEuM3kKecPsM6uF3rr6eOznr1I3J2o?key=2ms7aSILnOUvzUjqc2G4lg" alt=""><figcaption></figcaption></figure>

* **Thông tin nâng cao:** cấu hình các trường dữ liệu mà mục vừa tạo có thể quản lý, nhập liệu. Ví dụ như mục được tạo có trường người làm, giá trị hợp đồng thì người dùng có thể cài đặt trước ở đây, để khi mục được hệ thống tự động tạo thì sẽ được điền sẵn các giá trị đã được cấu hình trước đó. Người dùng có thể tự đưa ra được giá trị để gán vào các trường dữ liệu cấu hình, vừa có thể lấy giá trị ở các trường dữ liệu từ mục kích hoạt hành động để gán vào các trường dữ liệu cấu hình. Hiện tại, người dùng đang cho phép người dùng có thể cấu hình các trường dữ liệu dạng số, dạng chữ, dạng chọn một người, dạng ngày.&#x20;

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXcpH5f1gZtfNK1SLwSg0O13qiu2wUPPzwHWbW75Jqj4Wqmuvo6YnHiHNZKPDJIWDBsyWT_QeIOCZxYjw4D-obRc4_s7W1Zdx48Rcar48j5LQWmmNgTuugKyu53GuvUo34AyPTLUasfv07h-chc3lUSOxdbC?key=2ms7aSILnOUvzUjqc2G4lg" alt=""><figcaption></figcaption></figure>

\


Như ví dụ trên, hệ sau khi đã được kích hoạt và đạt đủ điều kiện để thực hiện hành động, hệ thống sẽ tự động tạo một mục có cùng loại mục với mục kích hoạt hành động và ở mảng việc giống với mục kích hoạt hành động với tiêu đề Thông báo nội bộ, trường Giá trị hợp đồng lấy giá trị 100000000 và trường Người làm lấy giá trị Trúc Quỳnh.

* **Tạo mục con:** tự động tạo mục con cho mục kích hoạt hành động. Để tiến hàng tạo mục con, người dùng nhấn chọn Thêm mục việc con -> chọn Loại mục và nhập tiêu đề. Sau đó nhấn chọn vào biểu tượng bánh răng để tiến hành cài đặt Thông tin cơ bản và Thông tin nâng cao như ở phần Tạo mục

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXehXNe30Jl-fwXj0X5G2HqwauH5nbLBZPOl-sv6DP2KVUjs8Iz2DKaUA9t5ca_0qI6UIANkQwdoCot5WYweKDubUFqU4PCjwwTxJnILW52INlpNQ6n2-nnZ53l0Hi3mCalRDsNAPuYsjjRyypnXOE53z4Wf?key=2ms7aSILnOUvzUjqc2G4lg" alt=""><figcaption></figcaption></figure>

* **Tạo mục kiểm:** tự động tạo mục kiểm trong mục kích hoạt hành động. Người dùng nhấn Thêm mục kiểm để cấu hình thêm các mục kiểm đến khi đủ nhu cầu. Sau khi cấu hình xong một mục kiểm, người dùng nhấn Enter để tiếp tục cấu hình thêm mục kiểm tiếp theo

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXcLkloczleDPU2Prtjujs6mkqAB2QnkJB3osR1B0H73qbYTjDS7g-K-OUEuI8f0n6VwhuROBvVfmRFekuxSLFaKYrOLrheSGnEI34gtMMOFYmlzEximZSuzrD_BjjvzaAReaoMyyr9f4Cbf-1AVY66inGom?key=2ms7aSILnOUvzUjqc2G4lg" alt=""><figcaption></figcaption></figure>

* **Chuyển trạng thái:** hệ thống tự động chuyển trạng thái sang
* **Cập nhật trường:** hệ thống tự động cập nhật giá trị của trường dữ liệu theo cấu hình mà người dùng đã cài đặt trước đó
