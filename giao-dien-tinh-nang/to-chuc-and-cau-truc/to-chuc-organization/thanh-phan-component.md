# Thành phần (Component)

### I.Tổng quan:

**Thành phần (Component)** là một trường hệ thống của mảng việc và được sử dụng để nhóm các vấn đề trong một dự án thành các nhóm nhỏ hơn. Khác với Issue Type (chỉ admin mới có thể cấu hình được) thì Thành Phần mang lại sự linh hoạt khi thiết lập ở Mảng Việc , và bất kì ai có quyền quản lý Mảng Việc cũng có thể cấu hình được thêm bớt được.

Người quản lý có thể:

* Tạo các thẻ thành thành phần ở Luklak theo cấp độ Mảng việc
* Phân quyền mặc định Người làm ( theo cá nhân, nhóm, vai trò) và Người giám sát với từng thẻ Thành phần
* Tạo các báo cáo kanban theo thẻ thành phần

Cấu trúc của thẻ thành phần bao gồm : Trưởng phần, Thành viên phần. Người dùng khi tạo thẻ thành phần, có thể gán Trưởng phần và thành viên phần ( với thành viên phần, ta có thể gán theo người dùng cá nhân, nhóm hoặc vai trò) ; sau đó phân quyền Người làm và Người giám sát theo hai trường đã gán ở trên.

Khi tạo thẻ thành phần, bạn sẽ được yêu cầu phân quyền Người làm và Người giám sát mặc định ở các trạng thái khi tạo hoặc chỉnh sửa mục việc. Sau đó, bạn có thể gán chúng vào các đầu việc, lúc này hệ thống sẽ tự động bổ nhiệm người làm và người giám sát như những gì bạn phân quyền ở thẻ thành phần. ( Ví dụ: khi gán Thẻ Thành Phần A có người làm là 5 nhân sự, khi tạo một việc mới, hệ thống sẽ tự động random 1 trong 5 nhân sự được gán làm người làm)

### II.Chức năng&#x20;

#### 1.Phân quyền mặc định “Người làm”, “Người giám sát”

1. #### Tạo không gian riêng và dễ dàng đo lường hiệu suất khi chia nhỏ thành team

Việc gán người làm và người giám sát theo thẻ thành phần thay vì theo cách thức thông thường giúp quản lý có thể chia nhỏ nhân sự của mình thành nhiều team. Mỗi team lại phụ trách một chức năng riêng theo thẻ thành phần; từ đó đo lường hiệu suất làm việc của nhân sự khi làm việc theo nhóm hay theo cá nhân

Ví dụ: “Thẻ thành phần” có thể được sử dụng trong việc Quản lý các tệp khách hàng để chia thành các nhóm nhỏ theo loại khách “Khách được giới thiệu”, “Khách Marketing”, “Khách đăng ký” hay theo trạng thái “Đã ký”, “Cân nhắc”, “Từ chối” từ đó phân bổ nhân sự trong team vào các nhóm nhỏ như đã chia.

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXeQHkAIfwqtEGhuhqIw3LOoAQucvET7japa_9cS_iWTysxJLc2__Lt5wLjdMDZaQPhZXisJck8McySLx1A2tyrsYzSPPb24endvgCrcxs1u1Q764mFFRpAl723Fh_QWvPkP80rJMljzrgQue1Jwn_l1gvM?key=HBksSiQRyjbWR-J4bXvERA" alt=""><figcaption></figcaption></figure>

&#x20;Tính năng này giúp tạo không gian riêng cho leaders có thể dễ dàng điều chỉnh, phân bổ và quản lý nhân sự theo cách của mình, mà không cần phải thay đổi quy trình chung ( các workflow) của toàn công ty.

2. #### Chuẩn hóa quy trình làm việc với nhiều lớp duyệt

Để đảm bảo chất lượng công việc, một quy trình công việc thường trải qua nhiều các cấp độ phê duyệt ( từ team leader -> trưởng phòng -> giám đốc) hay sự tham gia, phối hợp của nhiều phòng ban ( phòng kinh doanh - phòng kế toán) mà workflow của một công việc lại chỉ thể hiện các trạng thái để thực hiện đầu công việc đó. Do đó với tính năng thẻ thành phần, người dùng có thể chuyển người làm tương ứng khi trạng thái thay đổi bằng cách thay đổi thẻ thành phần của mục việc.



**Use cases:**

Quy trình sau đây được thực hiện bởi các Nhân viên tư vấn khi khách hàng ở trạng thái cần Tư vấn , khi tư vấn thành công, việc thiết lập hợp đồng sẽ được phê duyệt bởi nhân viên Kế Toán.

\=> **Sử dụng thẻ thành phần:** Khi ở trạng thái tư vấn, mục việc “Khách hàng A” trên sẽ được gán với thẻ thành phần ‘Tư vấn khách bị động’. Khi trạng thái chuyển sang hợp đồng, thẻ thành phần sẽ được đổi thành “Kế toán thu khách bị động” và lúc này người làm sẽ được chuyển cho bộ phận kế toán và chỉ có bộ phận kế toán mới được chuyển sang trạng thái “Duyệt” cho hợp đồng này.

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXePTgAUQWRhK4UML2U_QfJR2AsrbTv-z01mj3kIg5WxBJLSHoabvbyw1mKskKBbSsC62SCvdZw_vCzBLELkwstERsd1kS0IXcIGz8_lI-ttKClHbG1IV37KhDmNcdjmmPKkROhgIwwcMNDwOFWo4qgndrhg?key=HBksSiQRyjbWR-J4bXvERA" alt=""><figcaption></figcaption></figure>

3. **Trực quan hóa báo cáo Kanban bằng các “label” sinh động**

Bên cạnh chức năng gán người làm và người giám sát,  Thành Phần cũng có thể được sử dụng như các nhãn (label). Với tính năng này, người quản lý có thể chia nhỏ và đánh dấu bằng các nhãn màu sắc khác cho các đầu công việc trong một mảng việc, qua đó giúp dễ dàng có một cái nhìn tổng thể hơn về khối lượng công việc mà không ảnh hưởng chung tới quy trình chung của công ty

Ngoài ra, người dùng hoàn toàn có thể biểu đạt các Thành Phần trên báo cáo kanban của mình. Việc quan sát báo cáo kanban theo tiến trình công việc hay theo các thẻ thành phần giúp người dùng có cái nhìn đa chiều hơn về tổng thể công việc cần theo theo dõi.

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXehtiIE5dM2HCCjUVAsXWMmSpgs_LGUb8nxhQyrMhrTsutVhUTeIKJSLzPgccoFJ9j9EZGVkYyDI_tcCHySQsKbc5ZrjtZd-ucyAP-77ioLBAz3DnjOItUfs6uMihf1oX4MyzMLx5wLPzYOQ3_ozed_fQXZ?key=HBksSiQRyjbWR-J4bXvERA" alt=""><figcaption></figcaption></figure>

### III. Hướng dẫn sử dụng chi tiết

1. #### Tạo Thẻ Thành Phần trong mảng việc

Chọn một mảng việc cần tạo, Hover chuột Mảng Việc đó , ấn menu 3 chấm và chọn "Xem chi tiết" để đi đến phần cấu hình Mảng Việc đó, sẽ có một tab mới được tạo tên là Thành Phần, vào đó để cấu hình thêm bớt các thành phần.

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXdKlIEkUEnLz-C9nV5t5p0WFTZNZ_iaNAQtFVhBakW8PT5osVKFiPanImwPMfipmOz-8Xmb7rfPeupGi9_3vg2-oIJldvRxX0CCqpLAVR74u8IzRTwnYWBmyNmJqAz8Buw9UGXmqiB2KjLsFl_2XS91kwoQ?key=HBksSiQRyjbWR-J4bXvERA" alt=""><figcaption></figcaption></figure>

![](https://lh7-us.googleusercontent.com/docsz/AD_4nXcDN6kgMlAnMNET4G1WGo-hiZ2dMo2IKTOE6a7OHL8bcYapWWVCKaPi8Rc-LaCJFTOUBdCNppc2hvuuvpj6dSYAh_H_7a6kxOXeUcHXsCA4HF3RLtt0ce2iiGSur-FXC_AHxiLTuiA7cbk2oRcMZlvForAq?key=HBksSiQRyjbWR-J4bXvERA)

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXccvP9X_OrqAV8dPP6-RMOSQof4z0Xpd0yd3NeiAvR0OWjOLe7j0BnHKt9wZiZ7wy6eZji_RJJFsgPRHAH-23IwJDE4T76KE-vc0pb9YKXN--LD4eUoHbHTrHbthNgfVF1nmvS_Yd2wb8YpgaNFHUtfFiRw?key=HBksSiQRyjbWR-J4bXvERA" alt=""><figcaption></figcaption></figure>

2. #### Sử dụng Thẻ Thành Phần với các mục việc
3. **Khi tạo mục việc mới, chọn trường Thành Phần ( không bắt buộc để điền) để điền**&#x20;

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXcj3dIM8esTXuEz83-6RcjKN3dA1SmNJCHxVtgANjaVChLbqdKH_-Vii33Vg12VJbDNDmUefsi5b_U3yJec8DD8knXmaOorjbZbgTGbfiUTtkL79--0ezfKvvIujZVm_fcd8PS7nwX2VRaQwo9oh_ykwdI?key=HBksSiQRyjbWR-J4bXvERA" alt=""><figcaption></figcaption></figure>

### **IV. Lựa chọn chế độ xem theo các Thành Phần**

Bên cạnh chế độ hiển thị theo Loại mục, giờ đây người dùng có thể thêm chế độ hiển thị theo các Thành Phần

* Nhấp chuột vào “Cột” để thêm “Thành Phần” hiển thị trên màn hình&#x20;

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXfkMYszAtknKkHxSOKJMM7TP0ypqy4NAkFEvhhJeZmOAqKL1BeNTO5Q_1Yd28zcvyjBpl3NmkNd6nwiSHANxAUSKj9lM47O_g7j4LWYKD8UvrDPXvRQ6qaxN_l44iX5Q5_fBQQbCJEipYHyba_GJCfsjb3a?key=HBksSiQRyjbWR-J4bXvERA" alt=""><figcaption></figcaption></figure>

\


* Move chuột để sắp xếp lại vị trí các cột&#x20;

<figure><img src="https://lh7-us.googleusercontent.com/docsz/AD_4nXePQ6igFjOJL7eecWhpzJI-qR2TWkJ89YQTvfNCKV-ZBjV5T6Tr-HXGUJC6RHxnyr9Hx9-vtt85dKtNlT-N9LlLXSpS_yCHuyrqbpKbM1zfco6Lfou4bqJdajj_C1IiHHCFnxqXhYKvwarZUIf-vOkLkLcp?key=HBksSiQRyjbWR-J4bXvERA" alt=""><figcaption></figcaption></figure>

\
