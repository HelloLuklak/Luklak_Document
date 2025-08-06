# Smart value

## 1. Tổng quan

Sử dụng smart values để truy cập và thao tác với dữ liệu từ bên trong hoặc từ bên ngoài hệ thống

## 2. Phạm vi áp dụng

* Lấy giá trị từ trường
* Cập nhật trường sử dụng smart values
* Trong Action 'Kết nối mục': sử dụng trong lựa chọn 'Smart Values' hoặc 'Dùng bộ lọc'

## 3. Cấu trúc

Dữ liệu của issue được tổ chức theo dạng cây, một giá trị chứa nhiều yếu tố bên dưới

Các giá trị smart values bắt đầu các giá trị bằng dấu Dollar $, để phân biệt với các nội dung khác. Smart Values có  thể truy cập thông tin issue,field,... nên ta cần cung cấp vị trí và thuộc tính để truy cập dữ liệu mình cần.

Nếu muốn chuyển tới các elements bên trong, cần thêm dấu chấm vào trong giá trị của mình.&#x20;

Ví dụ $input.value

**a. Khi lấy giá trị dữ liệu các issue trong luklak:**

Để lấy dữ liệu từ issue, ta cần nhập smart values dưới dạng sau :&#x20;

<figure><img src="../../../.gitbook/assets/image (56).png" alt=""><figcaption></figcaption></figure>

**\[issue]:** vị trí issue muốn lấy dữ liệu

* Mục kích hoạt: _trigger_
* Mục hiện tại: _current_
* Mục cha mục kích hoạ&#x74;_: trigger.parent_
* Mục cha mục hiện tại: _current.parent_

**\[object]:** nhập đối tượng trong issue muốn lấy thông tin

* _id_: trả về id issue - [chi tiết](smart-value.md#id-2.1.-thong-tin-issue)
* _key_: trả về mã của issue (issue key) - [chi tiết ](smart-value.md#id-2.1.-thong-tin-issue)
* _url_: trả về url dẫn tới issue - [chi tiết](smart-value.md#id-2.1.-thong-tin-issue)
* _status_: truy cập thông tin trạng thái issue - [chi tiết](smart-value.md#id-2.3.-status)
* _space_: truy cập thông tin của space chứa issue - [chi tiết](smart-value.md#id-2.2.-space)
* _issuetype_: truy cập thông tin issue type - [chi tiết](smart-value.md#id-2.4.-issuetype)
* _fields_: truy cập thông tin các field trong issue&#x20;
* _createdBy_: truy cập thông tin người tạo issue - [chi tiết](smart-value.md#id-2.5.-createdby)
* _created_: truy cập thông tin thời gian tạo issue - [chi tiết](smart-value.md#id-2.6.-created)

**\[element]:** nhập thông tin muốn lấy từ các đối tượng truy cập vào bên trên

* Từ _space_: [link chi tiết](smart-value.md#id-2.2.-space)
* Từ _status_: [link chi tiết](smart-value.md#id-2.3.-status)
* Từ _issuetype_: [link chi tiết](smart-value.md#id-2.4.-issuetype)
* Từ _fields_: [link chi tiết](https://wiki.luklak.org/x/GLCZB)
  * user: [chi tiết](https://wiki.luklak.org/x/Sa6ZB)
  * group: [chi tiết](https://wiki.luklak.org/x/J6_ZB)
  * select: [chi tiết](https://wiki.luklak.org/x/366ZB)
  * checkbox: [chi tiết](https://wiki.luklak.org/x/n7KZB)
  * date, date time: [chi tiết](https://wiki.luklak.org/x/VrGZB)
  * email: [chi tiết](https://wiki.luklak.org/x/q7GZB)
  * phone number: [chi tiết](https://wiki.luklak.org/x/GLKZB)
  * text: [chi tiết](https://wiki.luklak.org/x/TLKZB)
  * number: [chi tiết](https://wiki.luklak.org/x/5LGZB)
* Từ _createdBy_: [link chi tiết](smart-value.md#id-2.5.-createdby)
* Từ _created_: [link chi tiết](smart-value.md#id-2.6.-created)

**b. Lấy thông tin từ automation:**

Có thể sử dụng Smart values để lấy thông tin liên quan tới Người kích hoạt hoặc Người thực thi của Automation đang sử dụng

* &#x20;**Người kích hoạt:&#x20;**_**$triggerUser**_
* **Người thực thi:&#x20;**_**$actorUser**_

Sau đó có thể truy cập các thuộc tính khác về Người kích hoạt, Người thực thi tương tự như các trường Chọn 1 người&#x20;

Ví dụ: Lấy tên hiển thị của Người kích hoạt automation&#x20;

```
$triggerUser.displayName
```

**c. Khi lấy giá trị từ dữ liệu bên ngoài**

* [**Webhook**](https://wiki.luklak.org/x/p6I-BQ#webhook)&#x20;
* [**HTTP Request** ](https://wiki.luklak.org/x/p6I-BQ#Webhook\&HTTPRequest-2.HTTPRequest)

## Các đối tượng khác <a href="#title-text" id="title-text"></a>

### 1. Tổng quan

Sử dụng smart values để lấy thông tin của issue hoặc từ space, status, issuetype, createdby, created liên quan tới issue.

### 2. Mô tả

#### 2.1. Thông tin issue

Ví dụ:

_issue ở mục kích hoạt với thông tin như sau:_

<table><thead><tr><th width="103">Id</th><th width="172">Key </th><th>id issue cha </th><th>url</th></tr></thead><tbody><tr><td>aaa-aaa</td><td>BUG-01</td><td>bbb-bbb</td><td><a href="https://app.luklak.live/org/orgcuaba/issue/BUG-01">https://app.luklak.live/org/orgcuaba/issue/BUG-01</a></td></tr></tbody></table>

**Lấy thông tin của issue**

<table><thead><tr><th width="156" align="center">Smart values</th><th width="240" align="center">Mô tả</th><th align="center">Ví dụ</th></tr></thead><tbody><tr><td align="center">Mặc định</td><td align="center">Smart values truy cập đến issue → mặc định trả về <strong>id issue</strong></td><td align="center"><pre><code>${trigger}
</code></pre><p>→ <strong>Giá trị trả về</strong>: aaa-aaa</p></td></tr><tr><td align="center">id</td><td align="center">Trả về id issue</td><td align="center"><pre><code>${trigger.id}
</code></pre><p>→ <strong>Giá trị trả về:</strong> aaa-aaa</p></td></tr><tr><td align="center"><strong>key</strong></td><td align="center">Trả về key issue</td><td align="center"><pre><code>${trigger.key}
</code></pre><p>→ <strong>Giá trị trả về:</strong> BUG-01</p></td></tr><tr><td align="center"><strong>url</strong></td><td align="center">Trả về url dẫn tới issue</td><td align="center"><p></p><pre class="language-javascript"><code class="lang-javascript">${trigger.url}
</code></pre><p>→ <strong>Giá trị trả về:</strong> <a href="https://app.luklak.live/org/orgcuaba/issue/ACT-1">https://app.luklak.live/org/orgcuaba/issue/BUG-01</a></p><p><br></p><p>Có thể thay tên hiển thị của url bằng việc thêm tên hiển thị vào trong dấu ngoặc vuông:</p><pre><code>[${trigger.key}]${trigger.url}
</code></pre><p>→ <strong>Giá trị trả về:</strong> <a href="https://app.luklak.live/org/orgcuaba/issue/ACT-1">BUG-01</a></p><pre><code>[link issue}]${trigger.url}
</code></pre><p>→ <strong>Giá trị trả về:</strong> <a href="https://app.luklak.live/org/orgcuaba/issue/ACT-1">link issue</a></p></td></tr></tbody></table>

#### 2.2. Space

Lấy thông tin từ _space_ chứa _issue_, từ đó có thể truy cập vào thông tin của _area_ và _function_ của _space_ đó

**Lưu ý:** cách xem id space, area hoặc function(tạm thời)

* Chọn space, area hoặc function cần xem id
* Id của space, area hoặc function hiển thị trên url
* space:&#x20;

<figure><img src="../../../.gitbook/assets/image (57).png" alt=""><figcaption></figcaption></figure>

* area:&#x20;

<figure><img src="../../../.gitbook/assets/image (58).png" alt=""><figcaption></figcaption></figure>

* function

<figure><img src="../../../.gitbook/assets/image (59).png" alt=""><figcaption></figcaption></figure>

Ví dụ :&#x20;

_space chứa issue ở mục kích hoạt với thông tin như sau:_\


<table><thead><tr><th width="187">Id space</th><th width="223">Tên space</th><th>Key</th><th>URL</th></tr></thead><tbody><tr><td>space-space</td><td>Kiểm thử</td><td>BUG</td><td><a href="https://app.luklak.live/org/orgcuaba/space/BUG">https://app.luklak.live/org/orgcuaba/space/BUG<br></a></td></tr></tbody></table>

Với thông tin về _area_ và _function_ của _space_ đó:

<table><thead><tr><th width="187">Id area</th><th>Tên area</th><th>Key</th><th>URL</th></tr></thead><tbody><tr><td>area-area</td><td>BP Phát triển Sản phẩm</td><td>AR3</td><td><a href="https://app.luklak.live/org/orgcuaba/area/AR3">https://app.luklak.live/org/orgcuaba/area/AR3</a><a href="https://app.luklak.live/org/orgcuaba/space/BUG"><br></a></td></tr></tbody></table>

<table><thead><tr><th width="187">Id function</th><th>Tên function</th><th>Key</th><th>status</th></tr></thead><tbody><tr><td>func-func</td><td>Kiểm thử phần mềm</td><td>KTPM</td><td>ACTIVE<a href="https://app.luklak.live/org/orgcuaba/space/BUG"></a></td></tr></tbody></table>

**a. Lấy thông tin từ space**

<table><thead><tr><th width="152">Smart values</th><th width="213" align="center">Mô tả</th><th align="center">Ví dụ</th></tr></thead><tbody><tr><td>id</td><td align="center">Trả về id space</td><td align="center"><pre><code>${trigger.space.id}
</code></pre><p>→ <strong>Giá trị trả về:</strong> space-space</p></td></tr><tr><td><strong>key</strong></td><td align="center">Trả về key của space</td><td align="center"><pre><code><strong>${trigger.space.key}
</strong></code></pre><p>→ <strong>Giá trị trả về:</strong> BUG</p></td></tr><tr><td>mặc định</td><td align="center">Smart values truy cập đến space → mặc định trả về id space</td><td align="center"><pre><code>${trigger.space}
</code></pre><p>→ <strong>Giá trị trả về</strong>: space-space</p></td></tr><tr><td><strong>name</strong></td><td align="center">Trả về tên hiển thị của space</td><td align="center"><pre><code>${trigger.space.name}
</code></pre><p>→ <strong>Giá trị trả về:</strong> Kiểm thử</p></td></tr><tr><td><strong>url</strong></td><td align="center">Trả về url dẫn tới space</td><td align="center"><pre><code><strong>${trigger.space.url}
</strong></code></pre><p>→ <strong>Giá trị trả về:</strong> <a href="https://app.luklak.live/org/orgcuaba/issue/ACT-1">https://app.luklak.live/org/orgcuaba/</a>space/BUG</p><p>Có thể thay tên hiển thị của url bằng việc thêm tên hiển thị vào trong dấu ngoặc vuông:</p><pre><code>[${trigger.space.key}]${trigger.space.url}
</code></pre><p>→ <strong>Giá trị trả về:</strong> <a href="https://app.luklak.live/org/orgcuaba/issue/ACT-1">BUG</a></p><pre><code>[trigger.space.name}]${trigger.url}
</code></pre><p>→ <strong>Giá trị trả về:</strong> <a href="https://app.luklak.live/org/orgcuaba/issue/ACT-1">Kiểm thử</a></p></td></tr></tbody></table>

**b. Lấy thông tin từ area**

<table><thead><tr><th width="152">Smart values</th><th width="213" align="center">Mô tả</th><th align="center">Ví dụ</th></tr></thead><tbody><tr><td>Mặc định</td><td align="center">Smart values truy cập đến area → mặc định trả về id area</td><td align="center"><pre><code>${trigger.space.area}
</code></pre><p>→ <strong>Giá trị trả về</strong>: area-area</p></td></tr><tr><td>id</td><td align="center">Trả về id area</td><td align="center"><pre><code>${trigger.space.area.id}
</code></pre><p>→ <strong>Giá trị trả về:</strong> area-area</p></td></tr><tr><td>name</td><td align="center">Trả về tên hiển thị của area</td><td align="center"><pre><code>${trigger.space.area.name}
</code></pre><p>→ <strong>Giá trị trả về:</strong> BP Phát triển Sản phẩm</p></td></tr><tr><td>url</td><td align="center">Trả về url dẫn tới area</td><td align="center"><pre><code>${trigger.space.area.url}
</code></pre><p>→ <strong>Giá trị trả về:</strong> <a href="https://app.luklak.live/org/orgcuaba/issue/ACT-1">https://app.luklak.live/org/orgcuaba/</a>area/AR3</p><p><br></p><p>Có thể thay tên hiển thị của url bằng việc thêm tên hiển thị vào trong dấu ngoặc vuông:</p><pre><code>[link area}]${trigger.apce.area.url}
</code></pre><p>→ <strong>Giá trị trả về:</strong> <a href="https://app.luklak.live/org/orgcuaba/issue/ACT-1">link area</a></p></td></tr><tr><td>key</td><td align="center">Trả về key của area</td><td align="center"><pre><code><strong>${trigger.space.area.key}
</strong></code></pre><p>→ <strong>Giá trị trả về:</strong> AR3</p></td></tr></tbody></table>

**c. Lấy thông tin từ function**

#### 2.3. Status

Lấy thông tin liên quan tới trạng thái hiện tại của _issue_

**Lưu ý:** cách xem id _status_ hoặc của _status category_

* Chọn _status_ hoặc của _status category_ cần xem id
* Id của space, area hoặc function hiển thị trên url

**Ví dụ:**

_statsus hiện tại của issue ở mục kích hoạt với thông tin như sau:_

<table><thead><tr><th width="187">Id status</th><th>Tên </th><th>Key</th><th>Description</th></tr></thead><tbody><tr><td>sta-sta</td><td>CẦN LÀM</td><td>todo</td><td>mô tả cần làm<a href="https://app.luklak.live/org/orgcuaba/space/BUG"></a></td></tr></tbody></table>

với thông tin về _category của status_ hiện tại của _space_ đó:

<table><thead><tr><th width="187">Id category</th><th>Tên </th><th>Key</th><th>Description</th></tr></thead><tbody><tr><td>cate-cate</td><td>Kế hoạch</td><td>planned</td><td>mô tả category<a href="https://app.luklak.live/org/orgcuaba/space/BUG"></a></td></tr></tbody></table>

**a. Lấy thông tin từ status**

<table><thead><tr><th width="152">Smart values</th><th width="213" align="center">Mô tả</th><th align="center">Ví dụ</th></tr></thead><tbody><tr><td>Mặc định</td><td align="center">Smart values truy cập đến status → mặc định trả về id status</td><td align="center"><pre><code>${trigger.status}
</code></pre><p>→ <strong>Giá trị trả về</strong>: sta-sta</p></td></tr><tr><td>id</td><td align="center">Trả về id space</td><td align="center"><pre><code>${trigger.status.id}
</code></pre><p>→ <strong>Giá trị trả về:</strong> sta-sta</p></td></tr><tr><td>name</td><td align="center">Trả về tên hiển thị của space</td><td align="center"><pre><code>${trigger.status.name}
</code></pre><p>→ <strong>Giá trị trả về:</strong> CẦN LÀM</p></td></tr><tr><td>key</td><td align="center">Trả về key của space</td><td align="center"><pre><code>${trigger.status.key}
</code></pre><p>→ <strong>Giá trị trả về:</strong> todo</p></td></tr><tr><td><strong>description</strong></td><td align="center">Trả về mô tả của trạng thái</td><td align="center"><pre><code>${trigger.status.description}
</code></pre><p>→ <strong>Giá trị trả về:</strong> mô tả cần làm</p></td></tr></tbody></table>

**b. Lấy thông tin từ category status**

<table><thead><tr><th width="152">Smart values</th><th width="213" align="center">Mô tả</th><th align="center">Ví dụ</th></tr></thead><tbody><tr><td>Mặc định</td><td align="center">Smart values truy cập đến category → mặc định trả về thông tin id loại trạng thái</td><td align="center"><pre><code><strong>${trigger.status.category}
</strong></code></pre><p>→ <strong>Giá trị trả về</strong>: cate-cate</p></td></tr><tr><td>id</td><td align="center">Trả về id category status</td><td align="center"><pre><code>${trigger.status.category.id}
</code></pre><p>→ <strong>Giá trị trả về:</strong> cate-cate</p></td></tr><tr><td>name</td><td align="center">Trả về tên của category status</td><td align="center"><pre><code>${trigger.status.category.name}
</code></pre><p>→ <strong>Giá trị trả về:</strong> Kế hoạch</p></td></tr><tr><td>key</td><td align="center">Trả về key của category status</td><td align="center"><pre><code>${trigger.status.category.key}
</code></pre><p>→ <strong>Giá trị trả về:</strong> planned</p></td></tr><tr><td><strong>description</strong></td><td align="center">Trả về description của category status</td><td align="center"><pre><code>${trigger.status.category.key}
</code></pre><p>→ <strong>Giá trị trả về:</strong> mô tả category</p></td></tr></tbody></table>

#### 2.4. Issuetype :&#x20;

Lấy thông tin liên quan tới loại mục (_issuetype_)của _issue_

**Ví dụ:**

_issuetype hiện tại của issue ở mục kích hoạt với thông tin như sau:_

| Id      | Tên       | Category  |
| ------- | --------- | --------- |
| ttt-ttt | Thông tin | ISSUE     |

**a. Lấy thông tin từ issuetype**

<table><thead><tr><th width="152">Smart values</th><th width="213" align="center">Mô tả</th><th align="center">Ví dụ</th></tr></thead><tbody><tr><td>Mặc định</td><td align="center">Smart values truy cập đến issuetype → mặc định trả về id issuetype</td><td align="center"><pre><code>${trigger.issuetype}
</code></pre><p>→ <strong>Giá trị trả về</strong>: ttt-ttt</p></td></tr><tr><td>id</td><td align="center">Trả về id issuetype</td><td align="center"><pre><code>${trigger.issuetype.id}
</code></pre><p>→ <strong>Giá trị trả về:</strong> ttt-ttt</p></td></tr><tr><td>name</td><td align="center">Trả về tên của issuetype</td><td align="center"><pre><code>${trigger.issuetype.name}
</code></pre><p>→ <strong>Giá trị trả về:</strong> Thông tin</p></td></tr><tr><td><strong>category</strong></td><td align="center"><p>Trả về tên loại của issuetype</p><p>(category có các gái trị: ISSUE, SUBTASK)</p></td><td align="center"><pre><code>${trigger.issuetype.category}
</code></pre><p>→ <strong>Giá trị trả về:</strong> ISSUE</p></td></tr></tbody></table>

#### 2.5. CreatedBy:

Lấy thông tin của người tạo ra _issue_

**Ví dụ:**

_Người tạo issue ở mục kích hoạt với thông tin như sau:_

| Tên hiển thị | Id      | Username   | Email                             |
| ------------ | ------- | ---------- | --------------------------------- |
| Nguyễn Văn A | aaa-aaa | nguyenvana | a@[gmail.com](https://gmail.com/) |

Khi Smart Values truy cập đến _createdBy_ → mặc định trả về **id người dùng**

_Ví dụ:_&#x20;

<pre><code><strong>${trigger.createdBy}
</strong></code></pre>

→ **Giá trị trả về**: aaa-aaa

#### 2.6. Created

Lấy thông tin về thời gian tạo ra issue

**Ví dụ :**&#x20;

_Thời gian tạo issue ở mục kích hoạt với thông tin như sau:_

| Giá trị          |
| ---------------- |
| 05.08.2024 09:00 |

Khi Smart Values truy cập đến _created_ → mặc định trả về **giá trị của trường**

_Ví dụ:_&#x20;

```
${trigger.created}
```

→ **Giá trị trả về**: 2024-08-05T00:09:00.000+07:00

## Fields

### 1. Tổng quan

Sử dụng smart values để lấy thông tin từ các trường dữ liệu của một issue

### 2. Mô tả

#### **1. Smart Values - List (các trường multi)** <a href="#fields-1.smartvalues-list-cactruongmulti" id="fields-1.smartvalues-list-cactruongmulti"></a>

Sử dụng smart values với các trường multi (Sổ xuống chọn nhiều, Nhiều hộp kiểm, Chọn nhiều người, Chọn nhiều nhóm): [**link mô tả**](smart-value.md#list-kieu-truong-multi)

#### **2. Smart Values - User** <a href="#fields-2.smartvalues-user" id="fields-2.smartvalues-user"></a>

Sử dụng smart values để lấy giá trị từ người dùng với các trường dạng người (Chọn một người, Chọn nhiều người): [**link mô tả**](https://wiki.luklak.org/x/Sa6ZB)

#### **3. Smart Values - Group** <a href="#fields-3.smartvalues-group" id="fields-3.smartvalues-group"></a>

Sử dụng smart values để lấy giá trị từ nhóm với các trường dạng nhóm (Chọn một nhóm, Chọn nhiều nhóm): [**link mô tả**](https://wiki.luklak.org/x/J6_ZB)

#### **4. Smart Values - Select** <a href="#fields-4.smartvalues-select" id="fields-4.smartvalues-select"></a>

Sử dụng smart values để lấy giá trị từ các trường dạng select (Sổ xuống chọn nhiều, Sổ xuống chọn một): [**link mô tả**](https://wiki.luklak.org/x/366ZB)

#### **5. Smart Values - Checkbox** <a href="#fields-5.smartvalues-checkbox" id="fields-5.smartvalues-checkbox"></a>

Sử dụng smart values để lấy giá trị từ các trường dạng dạng hộp kiểm (Nhiều hộp kiểm, Hộp kiểm đơn): [**link mô tả**](https://wiki.luklak.org/x/n7KZB)

#### **6.** Smart Values - Date, Date time <a href="#fields-6.smartvalues-date-datetime" id="fields-6.smartvalues-date-datetime"></a>

Sử dụng smart values để lấy giá trị từ các trường ngày, ngày giờ (Chọn ngày, Chọn ngày giờ): [**link mô tả**](https://wiki.luklak.org/x/VrGZB)

#### 7. Smart Values - Email <a href="#fields-7.smartvalues-email" id="fields-7.smartvalues-email"></a>

Sử dụng smart values để lấy giá trị từ các trường email (Một email, Nhiều email): [**link mô tả**](https://wiki.luklak.org/x/q7GZB)

#### 8. Smart Values - Phone number <a href="#fields-8.smartvalues-phonenumber" id="fields-8.smartvalues-phonenumber"></a>

Sử dụng smart values để lấy giá trị từ các trường Phone number: [**link mô tả**](https://wiki.luklak.org/x/GLKZB)

#### 9. Smart Values - Number <a href="#fields-9.smartvalues-number" id="fields-9.smartvalues-number"></a>

Sử dụng smart values để lấy giá trị từ các trường số (Số nguyên, Số thập phân, Công thức): [**link mô tả**](https://wiki.luklak.org/x/5LGZB)

#### 10. Smart Values - Text <a href="#fields-10.smartvalues-text" id="fields-10.smartvalues-text"></a>

Sử dụng smart values để lấy giá trị từ các trường chữ (Dòng chữ, Đoạn văn bản): [**link mô tả**](https://wiki.luklak.org/x/TLKZB)

#### 11. Smart Values - Issue picker <a href="#fields-11.smartvalues-issuepicker" id="fields-11.smartvalues-issuepicker"></a>

Sử dụng smart values để lấy giá trị từ các trường Chọn mục (Chọn một mục, Chọn nhiều mục): [**link mô tả**](https://wiki.luklak.org/x/JoLNBQ)

#### 12. Lưu ý <a href="#fields-12.luuy" id="fields-12.luuy"></a>

Với các trường thông tin đặc biệt liên quan đến việc tương tác, ghi nhận thời gian cuối sẽ không thể lấy thông tin, giá trị do các dữ liệu này **không được coi là một trường dữ liệu.**

* Cập nhật (updated)
* Tương tác (interacted)
* Trao đổi (dicussed)
* Chuyển trạng thái (statusChanged)
* Hoàn thành (completed)
* Kết luận (resolution)
* Người cập nhật
* Người theo dõi

### List (Kiểu trường multi)

Các smart values để truy cập tới một giá trị hoặc thay đổi kí tự phân tách khi liệt kê giá trị của các trường dạng Multi:

* Chọn nhiều người
* Chọn nhiều nhóm
* Sổ xuống chọn nhiều
* Nhiều hộp kiểm
* Nhiều email

**Một số lưu ý**:&#x20;

* Hiện tại khi cập nhật các trường dạng multi qua smart values có thể cập nhật bằng nhiều giá trị, các giá trị phân cách nhau bởi dấu phảy.
*   Ví dụ: khi cập nhật trường Người Quyền Cao qua smart values của Người Liên Quan: \


    ```
    ${trigger.fields.relatedUsers.join()}
    ```

    \
    → **Giá trị trả về:** aaa-aaa, bbb-bbb, ccc-ccc, ddd-ddd

2. Mô tả

**Ví dụ:**&#x20;

_Trường Người Liên Quan (key field: relatedusers) ở Mục kích hoạt có 4 giá trị Nguyễn Văn A, Nguyễn Văn B, Nguyễn Văn C, Nguyễn Văn D_



| Tên hiển thị | Id      | UserName   | Email                                      |
| ------------ | ------- | ---------- | ------------------------------------------ |
| Nguyễn Văn A | aaa-aaa | nguyenvana | [a@gmail.com](mailto:nguyenvana@gmail.com) |
| Nguyễn Văn B | bbb-bbb | nguyenvanb | [b@gmail.com](mailto:nguyenvana@gmail.com) |
| Nguyễn Văn C | ccc-ccc | nguyenvanc | [c@gmail.com](mailto:nguyenvana@gmail.com) |
| Nguyễn Văn D | ddd-ddd | nguyenvand | d[@gmail.com](mailto:nguyenvana@gmail.com) |

_Trường Lớp học (key field: class) ở Mục kích hoạt có 5 giá trị: Lớp 1, Lớp 2, Lớp 3, Lớp 4, Lớp 5_

| Key     | Giá trị |
| ------- | ------- |
| lop\_01 | Lớp 01  |
| lop\_02 | Lớp 02  |
| lop\_03 | Lớp 03  |
| lop\_04 | Lớp 04  |
| lop\_05 | Lớp 05  |

**Chi tiết**

Với các smart values để lấy một giá trị trong danh sách

* Với trường **Chọn nhiều người, Chọn nhiều nhóm**: trả về **id**
* Với trường **Sổ xuống chọn nhiều, Nhiều hộp kiểm, Nhiều email:** trả về **value**
* Sau đó có thể truy cập tiếp các thuộc tính của giá trị đó: **Chọn nhiều người** (_id, username, displayName, email_), **Chọn nhiều nhóm** (_id, name_), **Sổ xuống chọn nhiều** (_key, value_), **Nhiều hộp kiểm** (_key, value_)

<table><thead><tr><th width="175">Smart values</th><th width="192">Mô tả</th><th>Ví dụ</th></tr></thead><tbody><tr><td><strong>empty()</strong></td><td>Kiểm tra trường có trống hay không (trả về <em>true / false</em>)</td><td><pre><code>${trigger.fields.relatedusers.empty()}
</code></pre><p>→ <strong>Giá trị trả về:</strong> false</p></td></tr><tr><td><strong>first()</strong></td><td><p>Trả về giá trị đầu tiên trong danh sách các giá trị được chọn.</p><p><strong>(trả về kết quả dựa theo vị trí hiển thị trên issue, không theo thứ tự chọn)</strong></p></td><td><p>Trường <em>Chọn nhiều người:</em></p><pre><code>${trigger.fields.relatedusers.first()}
</code></pre><p>→ <strong>Giá trị trả về:</strong> aaa-aaa<br></p><p>Trường <em>Sổ xuống chọn nhiều:</em></p><pre><code>${trigger.fields.multiselect.first()}
</code></pre><p>→ <strong>Giá trị trả về:</strong> Lớp 01<br></p><p><strong>Truy cập tiếp các thuộc tính</strong> </p><pre><code>${trigger.fields.relatedusers.first().displayName} 
${trigger.fields.relatedusers.first().id}
${trigger.fields.relatedusers.first().username}
${trigger.fields.relatedusers.first().email}
</code></pre><p>→ <strong>Giá trị trả về:</strong></p><p>Nguyễn Văn A<br>aaa-aaa<br>nguyenvana<br>a@<a href="https://gmail.com/">gmail.com</a>                   </p><pre><code>${trigger.fields.multiselect.first().key}
${trigger.fields.multiselect.first().value}
</code></pre><p>→  <strong>Giá trị trả về:</strong></p><p>lop_01</p><p>Lớp 01</p></td></tr><tr><td>last()</td><td><p>Trả về giá trị cuối cùng trong danh sách các giá trị được chọn. </p><p><strong>(trả về kết quả dựa theo vị trí hiển thị trên issue, không theo thứ tự chọn)</strong></p></td><td><p>Trường <em>Chọn nhiều người:</em></p><pre><code>${trigger.fields.relatedusers.last()}
</code></pre><p>→ <strong>Giá trị trả về:</strong> ddd-ddd<br></p><p>Trường <em>Sổ xuống chọn nhiều:</em></p><pre><code>${trigger.fields.multiselect.last()}
</code></pre><p>→ <strong>Giá trị trả về:</strong> Lớp 5<br></p><p><strong>Truy cập tiếp các thuộc tính:</strong> tương tự <mark style="color:blue;"><strong>first()</strong></mark></p></td></tr><tr><td><strong>get(</strong><em><strong>position</strong></em><strong>)</strong></td><td><p>Trả về giá trị trong danh sách các giá trị được chọn theo vị trí</p><p><strong>Nhập</strong> <strong>vị trí của giá trị</strong> muốn lấy vào trong ngoặc, giá trị thứ <strong>n</strong> trong danh sách sẽ có vị trí <strong>n-1</strong> </p><p>Ngoài ra có thể nhập vị trí theo số âm để lấy theo giá trị tính từ cuối lên: giá trị cuối cùng sẽ ở vị trí <strong>-1</strong></p><p>Không nhập vị trí → Lỗi</p></td><td><p>Trường <em>Chọn nhiều người</em> có 4 giá trị, lấy giá trị thứ 2:</p><pre><code>${trigger.fields.relatedusers.get(1)}
${trigger.fields.relatedusers.get(-3)}
</code></pre><p>→ <strong>Giá trị trả về:</strong> bbb-bbb</p><p><br></p><p><em>Trường Sổ xuống chọn nhiều (Lớp) có 5 giá trị, lấy giá trị thứ 4:</em></p><pre><code>${trigger.fields.multiselect.get(4)}
${trigger.fields.multiselect.get(-2)}
</code></pre><p>→ <strong>Giá trị trả về:</strong> Lớp 4</p><p><br></p><p><strong>Truy cập tiếp các thuộc tính:</strong> tương tự <mark style="color:blue;"><strong>first()</strong></mark></p></td></tr><tr><td><strong>quantity()</strong></td><td>Trả về số lượng giá trị được chọn</td><td><p></p><pre><code>${trigger.fields.relatedusers.quantity()}
</code></pre><p>→ <strong>Giá trị trả về:</strong> 4</p><pre><code>${trigger.fields.multiselect.quantity()}
</code></pre><p>→ <strong>Giá trị trả về:</strong> 5</p></td></tr><tr><td><strong>contains(</strong><em><strong>'value'</strong></em><strong>)</strong></td><td><p>Kiểm tra xem có chứa giá trị đưa vào (trả về <em>true / false</em>)</p><p>Với trường <strong>Chọn nhiều người</strong> và <strong>Chọn nhiều nhóm</strong>: giá trị tìm kiếm là theo <strong>id</strong></p><p>Với trường <strong>Sổ xuống chọn nhiều, Nhiều hộp kiểm, Nhiều email</strong>: giá trị tìm kiếm là theo <strong>value</strong></p></td><td><pre><code>${trigger.fields.relatedusers.contains('fff-fff')}
</code></pre><p>→ <strong>Giá trị trả về:</strong> false</p><p></p><pre><code>${trigger.fields.multiselect.contains('lop_01')}
</code></pre><p>→ <strong>Giá trị trả về:</strong> true</p></td></tr><tr><td><strong>containsAll</strong><em><strong>('value1', 'value2'</strong></em><strong>)</strong></td><td><p>Kiểm tra xem có chứa các giá trị đưa vào (trả về <em>true / false</em>)</p><p>Giá trị tìm kiếm tương tự <strong>contains()</strong></p></td><td><pre><code>${trigger.fields.relatedusers.containsAll('aaa-aaa', 'fff-fff')}
</code></pre><p>→ <strong>Giá trị trả về:</strong> false</p><pre><code>${trigger.fields.multiselect.containsAll('lop_01', 'lop_02')}
</code></pre><p>→ <strong>Giá trị trả về:</strong> true</p></td></tr><tr><td><strong>Đổi kí tự phân tách</strong></td><td><p>Đổi kí tự ngăn cách giữa các giá trị mặc định: sử dụng <strong>join()</strong></p><p>Nhập kí muốn ngăn cách vào trong dấu nháy đơn → các giá trị sẽ phân cách nhau bởi kí tự nằm trong dấu nháy đơn</p><p></p><p></p><p></p><p></p><p><br>Đổi kí tự ngăn cách giữa các giá trị thuộc tính: thêm kí tự phân tách vào trong các smart values</p><p>Nhập kí muốn ngăn cách vào trong dấu nháy đơn → các giá trị sẽ phân cách nhau bởi kí tự nằm trong dấu nháy đơn</p><p><br></p></td><td><p><em>Khi không nhập gì, mặc định là dấu phảy</em></p><pre><code>${trigger.fields.relatedusers.join()}
</code></pre><p>→ <strong>Giá trị trả về:</strong> aaa-aaa, bbb-bbb, ccc-ccc, ddd-ddd</p><p><br></p><p><em>Khi nhập kí tự phân tách nằm trong nháy đơn:</em></p><pre><code>${trigger.fields.relatedusers.join('/')}
</code></pre><p>→ <strong>Giá trị trả về:</strong> aaa-aaa/bbb-bbb/ccc-ccc/ddd-ddd</p><p></p><p></p><p><em>Khi không nhập gì, mặc định là dấu phảy</em></p><pre><code>${trigger.fields.relatedusers.usernames()}
</code></pre><p>→ <strong>Giá trị trả về:</strong> nguyenvana, nguyenvanb, nguyenvanc, nguyenvand</p><p><br></p><p><em>Khi nhập kí tự phân tách nằm trong nháy đơn:</em></p><pre><code>${trigger.fields.relatedusers.usernames('/')}
</code></pre><p>→ <strong>Giá trị trả về:</strong> nguyenvana/nguyenvanb/nguyenvanc/nguyenvand</p></td></tr></tbody></table>

### User

1. Tổng quan

Sử dụng smart values để lấy giá trị từ các trường Người (Chọn một người, Chọn nhiều người)

2. Mô tả

**Lưu ý:** cách xem id người dùng (tạm thời)

* vào chat riêng, chọn user muốn xem id
* id của user hiển thị trên url

<figure><img src="../../../.gitbook/assets/image (60).png" alt=""><figcaption></figcaption></figure>

**2.1. Chọn một người (single user picker)**

**Ví dụ:**&#x20;

_Trường Người làm (key field: assignee) có giá trị Nguyễn Văn A với thông tin như sau:_

| Tên hiển thị | Id      | Username   | Email       |
| ------------ | ------- | ---------- | ----------- |
| Nguyễn Văn A | aaa-aaa | nguyenvana | a@gmail.com |

**Lấy thông tin từ trường**

<table><thead><tr><th width="185">Smart values </th><th width="211">Mô tả </th><th>Ví dụ</th></tr></thead><tbody><tr><td>Mặc định</td><td>Smart values truy cập đến mã trường (key field) → mặc định trả về <strong>id người dùng</strong></td><td><pre><code>${trigger.fields.assignee}
</code></pre><p>→ <strong>Giá trị trả về</strong>: aaa-aaa</p></td></tr><tr><td><strong>id</strong></td><td><p>Trả về id người dùng</p><p>(Sử dụng để cập nhật trường Chọn một người qua <strong>Smart values</strong>)</p></td><td><pre><code><strong>${trigger.fields.assignee.id}
</strong></code></pre><p>→ <strong>Giá trị trả về</strong>: aaa-aaa<br></p></td></tr><tr><td><strong>username</strong></td><td>Trả về username người dùng được chọn</td><td><pre><code>${trigger.fields.assignee.username}
</code></pre><p>→ <strong>Giá trị trả về:</strong> nguyenvana</p></td></tr><tr><td><strong>displayName</strong></td><td>Trả về tên hiển thị người dùng được chọn</td><td><pre><code>${trigger.fields.assignee.displayName}
</code></pre><p>→ <strong>Giá trị trả về:</strong> Nguyễn Văn A</p></td></tr><tr><td><strong>email</strong></td><td>Trả về email người dùng được chọn</td><td><pre><code><strong>${trigger.fields.assignee.email}
</strong></code></pre><p>→ <strong>Giá trị trả về:</strong> <a href="mailto:emailuser1@gmial.com">a@gmail.com</a></p></td></tr><tr><td><strong>mention()</strong></td><td>Nhắc đến người dùng được chọn</td><td><pre><code>${trigger.fields.assignee.mention()}
</code></pre><p>→ <strong>Giá trị trả về:</strong> <a href="mailto:emailuser1@gmial.com">N</a>guyễn Văn A</p></td></tr><tr><td><strong>empty()</strong></td><td>Kiểm tra trường có trống hay không (trả về <em>true / false</em>)</td><td><pre><code>${trigger.fields.assignee.empty()}
</code></pre><p>→ <strong>Giá trị trả về:</strong> false</p></td></tr></tbody></table>

2.2. Chọn nhiều người(multi user picker)

**Ví dụ**:

_Trường Người Liên Quan (key field: relatedusers) ở Mục kích hoạt có 3 giá trị Nguyễn Văn A, Nguyễn Văn B, Nguyễn Văn C_&#x20;

| Tên hiển thị | Id      | Username   | Email                                      |
| ------------ | ------- | ---------- | ------------------------------------------ |
| Nguyễn Văn A | aaa-aaa | nguyenvana | a@gmail.com                                |
| Nguyễn Văn B | bbb-bbb | nguyenvanb | [b@gmail.com](mailto:nguyenvana@gmail.com) |
| Nguyễn Văn C | ccc-ccc | nguyenvanc | [c@gmail.com](mailto:nguyenvana@gmail.com) |

**Lấy thông tin từ trường**

Smart values khi lấy danh sách các thuộc tính tương tự như trường single và thêm hậu tố '**s()**'

Các giá trị khi trả về mặc định **phân tách nhau bởi** **dấu phảy,** người dùng có thể chủ động đổi kí tự phân tách

<table><thead><tr><th>Smart values</th><th>Mô tả</th><th>Ví dụ </th></tr></thead><tbody><tr><td>Mặc định</td><td>Smart values truy cập đến mã trường (key field) → Mặc định trả về <strong>danh sách các id người dùng</strong></td><td><pre><code>${trigger.fields.relatedusers}
</code></pre><p>→ <strong>Giá trị trả về</strong>: aaa-aaa, bbb-bbb, ccc-ccc</p></td></tr><tr><td><strong>ids()</strong></td><td>Trả về id các người dùng được chọn</td><td><pre><code><strong>${trigger.fields.relatedusers.ids()}
</strong></code></pre><p>→ <strong>Giá trị trả về</strong>: aaa-aaa, bbb-bbb, ccc-ccc</p></td></tr><tr><td><strong>usernames()</strong></td><td>Trả về username các người dùng được chọn</td><td><pre><code>${trigger.fields.relatedusers.usernames()}
</code></pre><p>→ <strong>Giá trị trả về:</strong> nguyenvana, nguyenvanb, nguyenvanc</p></td></tr><tr><td><strong>displayNames()</strong></td><td>Trả về tên hiển thị các người dùng được chọn</td><td><pre><code>${trigger.fields.relatedusers.displayNames()}
</code></pre><p>→ <strong>Giá trị trả về:</strong> Nguyễn Văn A, Nguyễn Văn B, Nguyễn Văn C</p></td></tr><tr><td><strong>emails()</strong></td><td><p></p><p>Trả về email các người dùng được chọn</p><p><br></p></td><td><pre><code>${trigger.fields.relatedusers.emails()}
</code></pre><p>→ <strong>Giá trị trả về:</strong> <a href="mailto:emailuser1@gmial.com">a@gmail.com</a>, <a href="mailto:emailuser1@gmial.com">b@gmail.com</a>, <a href="mailto:emailuser1@gmial.com">c@gmail.com</a></p></td></tr><tr><td><strong>mention()</strong></td><td>Nhắc đến các người dùng được chọn</td><td><pre><code><strong>${trigger.fields.relatedusers.mention()}
</strong></code></pre><p>→ <strong>Giá trị trả về:</strong> Nguyễn Văn ANguyễn Văn BNguyễn Văn C</p></td></tr><tr><td><strong>Dạng list</strong></td><td>Do thuộc kiểu trường dữ liệu multi nên khi lấy giá trị từ <strong>trường Chọn nhiều người</strong> có thể sử dụng các <strong>smart values dạng list</strong>. Đọc thêm <a href="smart-value.md#list-kieu-truong-multi">Tại đây</a></td><td></td></tr></tbody></table>

### Group

1. Tổng quan

Sử dụng smart values để lấy giá trị từ các trường Nhóm

* Chọn một nhóm
* Chọn nhiều nhóm

2. Mô tả

**Lưu ý:** Cách xem id nhóm (tạm thời)

* Vào cài đặt admin / Nhóm
* Chọn nhóm muốn xem id
* Id nhóm hiển thị trên url

<figure><img src="../../../.gitbook/assets/image (61).png" alt=""><figcaption></figcaption></figure>

2.1. Chọn một nhóm(single group picker)

_**Ví dụ:**_&#x20;

_Trường Nhóm Thực Hiện (key field: nhom\_thuc\_hien) có giá trị Nhóm A_

| id      | Tên    |
| ------- | ------ |
| aaa-aaa | Nhóm A |

**Lấy thông tin của trường**

<table><thead><tr><th width="185">Smart values </th><th width="211">Mô tả </th><th>Ví dụ</th></tr></thead><tbody><tr><td>Mặc định</td><td>Smart values truy cập đến mã trường (key field) → mặc định trả về <strong>id nhóm</strong></td><td><pre><code><strong>${trigger.fields.nhom_thuc_hien}
</strong></code></pre><p>→ <strong>Giá trị trả về</strong>: aaa-aaa</p></td></tr><tr><td><strong>id</strong></td><td>Trả về id nhóm</td><td><pre><code>${trigger.fields.nhom_thuc_hien.id}
</code></pre><p>→ <strong>Giá trị trả về</strong>: aaa-aaa</p></td></tr><tr><td><strong>name</strong></td><td>Trả về tên hiển thị của nhóm</td><td><pre><code>${trigger.fields.nhom_thuc_hien.name}
</code></pre><p>→ <strong>Giá trị trả về:</strong> Nhóm A</p></td></tr><tr><td><strong>empty()</strong></td><td>Kiểm tra trường có trống hay không (trả về <em>true / false</em>)</td><td><pre><code>${trigger.fields.nhom_thuc_hien.empty()}
</code></pre><p>→ <strong>Giá trị trả về:</strong> false</p></td></tr></tbody></table>

2.2. Chọn nhiều nhóm(multi group picker)

Ví dụ:

_Trường Nhóm Liên Quan (key field: relatedgroups) ở Mục kích hoạt có 3 giá trị Nhóm A, Nhóm B, Nhóm C_

| Id      | Tên    |
| ------- | ------ |
| aaa-aaa | Nhóm A |
| bbb-bbb | Nhóm B |
| ccc-ccc | Nhóm C |

**Lấy thông tin của trường**

Smart values khi lấy danh sách các thuộc tính tương tự như trường single và thêm hậu tố '**s()**'

Các giá trị khi trả về mặc định **phân tách nhau bởi** **dấu phảy,** người dùng có thể chủ động đổi kí tự phân tách.

<table><thead><tr><th width="185">Smart values </th><th width="211">Mô tả </th><th>Ví dụ</th></tr></thead><tbody><tr><td>Mặc định</td><td>Smart values truy cập đến mã trường (key field) → mặc định trả về <strong>danh sách các id nhóm</strong></td><td><pre><code>${trigger.fields.relatedgroups}
</code></pre><p>→ <strong>Giá trị trả về</strong>: aaa-aaa, bbb-bbb, ccc-ccc</p></td></tr><tr><td><strong>ids()</strong></td><td>Trả về id các nhóm được chọn</td><td><pre><code>${trigger.fields.relatedgroups.ids()}
</code></pre><p>→ <strong>Giá trị trả về</strong>: aaa-aaa, bbb-bbb, ccc-ccc</p></td></tr><tr><td><strong>names()</strong></td><td>Trả về tên của các nhóm được chọn</td><td><pre><code>${trigger.fields.relatedgroups.names()}
</code></pre><p>→ <strong>Giá trị trả về:</strong> Nhóm A, Nhóm B, Nhóm C </p></td></tr><tr><td><strong>Dạng list</strong></td><td>Do thuộc kiểu trường dữ liệu multi nên khi lấy giá trị từ <strong>trường Chọn nhiều nhóm</strong> có thể sử dụng các <strong>smart values dạng list</strong>. Đọc thêm <a href="smart-value.md#list-kieu-truong-multi">Tại đây</a></td><td></td></tr></tbody></table>

### Select

1. Tổng quan

Sử dụng smart values để lấy giá trị từ các trường:

* Sổ xuống chọn một
* Sổ xuống chọn nhiều

2. Mô tả

2.1. Sổ xuống chọn một

Ví dụ:&#x20;

Trường lớp học (key field: class) ở Mục kích hoạt có giá trị 'Lớp 01' với thông tin như sau:

| Key     | Value  |
| ------- | ------ |
| lop\_01 | Lớp 01 |

**Lấy thông tin của trường**

<table><thead><tr><th>Smart values</th><th>Mô tả</th><th>Ví dụ</th></tr></thead><tbody><tr><td>Mặc định</td><td>Smart values truy cập đến mã trường (key field) → mặc định trả về <strong>giá trị của option</strong></td><td><pre><code>${trigger.fields.class}
</code></pre><p>→ <strong>Giá trị trả về</strong>: Lớp 01</p></td></tr><tr><td><strong>key</strong></td><td>Trả về Mã (key) của option được chọn</td><td><pre><code>${trigger.fields.class.key}
</code></pre><p>→ <strong>Giá trị trả về</strong>: lop_01</p></td></tr><tr><td><strong>value</strong></td><td>Trả về Giá trị (value) của option được chọn</td><td><pre><code>${trigger.fields.class.value}
</code></pre><p>→ <strong>Giá trị trả về</strong>: Lớp 01</p></td></tr><tr><td><strong>empty()</strong></td><td>Kiểm tra trường có trống hay không (trả về <em>true / false</em>)</td><td><pre><code>${trigger.fields.class.empty()}
</code></pre><p>→ <strong>Giá trị trả về:</strong> false</p></td></tr></tbody></table>

2.2. Sổ xuống chọn nhiều

_**Ví dụ**:_&#x20;

_Trường Lớp học (key field: class) ở Mục kích hoạt có đang chọn 3 giá trị: Lớp 1, Lớp 2, Lớp 3_

| Key     | Giá trị |
| ------- | ------- |
| lop\_01 | Lớp 01  |
| lop\_02 | Lớp 02  |
| lop\_03 | Lớp 03  |

Lấy thông tin của trường

Smart values khi lấy danh sách các thuộc tính tương tự như trường single và thêm hậu tố '**s()**'

Các giá trị khi trả về mặc định **phân tách nhau bởi** **dấu phảy,** người dùng có thể chủ động đổi kí tự phân tách

<table><thead><tr><th>Smart values</th><th>Mô tả</th><th>Ví dụ</th></tr></thead><tbody><tr><td>Mặc định</td><td>Smart values truy cập đến mã trường (key field) → Trả về <strong>danh sách tên các giá trị được chọn</strong></td><td><pre><code><strong>${trigger.fields.class}
</strong></code></pre><p>→ <strong>Giá trị trả về</strong>: Lớp 01, Lớp 02, Lớp 03</p></td></tr><tr><td><strong>keys()</strong></td><td>Trả về mã (key) của các option đang được chọn</td><td><pre><code>${trigger.fields.lua_chon.keys()}
</code></pre><p>→ <strong>Giá trị trả về</strong>: lop_01, lop_02, lop_03</p></td></tr><tr><td><strong>values()</strong></td><td>Trả về tên các option đang được chọn</td><td><pre><code>${trigger.fields.lua_chon.values()}
</code></pre><p>→ <strong>Giá trị trả về:</strong> Lớp 01, Lớp 02, Lớp 03</p></td></tr><tr><td><strong>Dạng list</strong></td><td>Do thuộc kiểu trường dữ liệu multi nên khi lấy giá trị từ <strong>trường Sổ xuống chọn nhiều</strong> có thể sử dụng các <strong>smart values dạng list</strong>. Đọc thêm <a href="smart-value.md#list-kieu-truong-multi">Tại đây</a></td><td></td></tr></tbody></table>

### Checkbox

1. Tổng quan

Sử dụng smart values để lấy giá trị từ các trường:

* Hộp kiểm đơn
* Nhiều hộp kiểm

2. Mô tả

2.1. Hộp kiểm đơn&#x20;

a. Lấy dữ liệu từ trường

_**Ví dụ:**_&#x20;

_Trường Xác nhận (key field: xac\_nhan) ở Mục kích hoạt đang được tick chọn_&#x20;

**Lấy thông tin của trường**

<table><thead><tr><th>Smart values </th><th>Mô tả</th><th>Ví dụ</th></tr></thead><tbody><tr><td>Mặc định</td><td>Smart values truy cập đến mã trường (key field) → mặc định trả về <strong>giá trị của trường (</strong><em><strong>true / false</strong></em><strong>).</strong> </td><td><pre><code>${trigger.fields.xac_nhan}
</code></pre><p>→ <strong>Giá trị trả về</strong>: true</p></td></tr></tbody></table>

2.2. Nhiều hộp kiểm

_**Ví dụ**:_&#x20;

_Trường Lớp học (key field: class) ở Mục kích hoạt có đang chọn 3 giá trị: Lớp 1, Lớp 2, Lớp 3_

| Key     | Giá trị |
| ------- | ------- |
| lop\_01 | Lớp 01  |
| lop\_02 | Lớp 02  |
| lop\_03 | Lớp 03  |

**Lấy thông tin của trường**

Các giá trị khi trả về mặc định **phân tách nhau bởi** **dấu phảy,** người dùng có thể chủ động đổi kí tự phân tách

<table><thead><tr><th>Smart values</th><th>Mô tả</th><th>Ví dụ</th></tr></thead><tbody><tr><td>Mặc định</td><td>Smart values truy cập đến mã trường (key field) → Mặc định trả về <strong>danh sách tên các giá trị được chọn</strong></td><td><pre><code>${trigger.fields.class}
</code></pre><p>→ <strong>Giá trị trả về</strong>: Lớp 01, Lớp 02, Lớp 03</p></td></tr><tr><td><strong>keys()</strong></td><td>Trả về mã (key) của các option đang được chọn</td><td><pre><code><strong>${trigger.fields.lua_chon.keys()}
</strong></code></pre><p>→ <strong>Giá trị trả về</strong>: lop_01, lop_02, lop_03</p></td></tr><tr><td><strong>values()</strong></td><td>Trả về tên các option đang được chọn</td><td><pre><code>${trigger.fields.lua_chon.values()}
</code></pre><p>→ <strong>Giá trị trả về:</strong> Lớp 01, Lớp 02, Lớp 03</p></td></tr><tr><td>Dạng list</td><td>Do thuộc kiểu trường dữ liệu multi nên khi lấy giá trị từ <strong>trường Nhiều hộp kiểm</strong> có thể sử dụng các <strong>smart values dạng list</strong>. Đọc thêm<a href="smart-value.md#list-kieu-truong-multi"> Tại đây</a></td><td></td></tr></tbody></table>

### Date - Date time

1. Tổng quan

Sử dụng smart values để lấy giá trị từ các trường:

* Chọn ngày
* Chọn ngày giờ

2. Mô tả

2.1. Chọn ngày

_**Ví dụ**:_&#x20;

_Trường Ngày làm (key field: ngay\_lam) ở Mục kích hoạt có giá trị như sau_

| Trường               | Giá trị    |
| -------------------- | ---------- |
| Ngày làm (ngay\_lam) | 05.08.2024 |

**Lấy thông tin của trường**

<table><thead><tr><th>Smart values</th><th>Mô tả</th><th>Ví dụ</th></tr></thead><tbody><tr><td>Mặc định</td><td><p>Smart values truy cập đến mã trường (key field) → mặc định trả về <strong>giá trị của trường</strong></p><p>(Sử dụng để cập nhật trường <strong>Chọn ngày</strong> qua <strong>Smart values</strong>)</p></td><td><pre><code>${trigger.fields.ngay_lam}
</code></pre><p>→ <strong>Giá trị trả về</strong>: 2024-08-05</p></td></tr><tr><td><strong>date()</strong></td><td>Trả về kết quả có định dạng</td><td><pre><code>${trigger.fields.class.ngay_lam.date()}
</code></pre><p>→ <strong>Giá trị trả về</strong>: 05/08/2024</p></td></tr><tr><td><strong>after('</strong><em><strong>value</strong></em><strong>')</strong></td><td>Kiểm tra giá trị của trường có sau giá trị đưa vào</td><td><pre><code>${trigger.fields.ngay_lam.after('04/08/2024')}
</code></pre><p>→ <strong>Giá trị trả về</strong>: true</p></td></tr><tr><td><strong>before('</strong><em><strong>value</strong></em><strong>')</strong></td><td>Kiểm tra giá trị của trường có trước giá trị đưa vào</td><td><pre><code>${trigger.fields.ngay_lam.before('04/08/2024')}
</code></pre><p>→ <strong>Giá trị trả về</strong>: false</p></td></tr><tr><td><strong>empty()</strong></td><td>Kiểm tra trường có trống hay không (trả về <em>true / false</em>)</td><td><pre><code><strong>${trigger.fields.ngay_lam.empty()}
</strong></code></pre><p>→ <strong>Giá trị trả về:</strong> false</p></td></tr><tr><td><strong>plusDays()</strong></td><td>Cộng thêm ngày, cộng thêm số nguyên</td><td><pre><code>${trigger.fields.ngay_lam.plusDays(5)}
</code></pre><p>→ <strong>Giá trị trả về:</strong> 2024-08-10</p><pre><code>${trigger.fields.ngay_lam.plusDays(${trigger.fields.so_luong})}
</code></pre><p>Giá trị trường Số lượng: 3</p><p>→ <strong>Giá trị trả về:</strong> 2024-08-08</p></td></tr><tr><td><strong>plusMonths()</strong></td><td>Cộng thêm tháng, cộng thêm số nguyên</td><td><pre><code>${trigger.fields.ngay_lam.plusMonths(5)}
</code></pre><p>→ <strong>Giá trị trả về:</strong> 2025-01-05</p><pre><code>${trigger.fields.ngay_lam.plusDays(${trigger.fields.so_luong})}
</code></pre><p>Giá trị trường Số lượng: 3</p><p>→ <strong>Giá trị trả về:</strong> 2024-11-05</p></td></tr></tbody></table>

2.2. Chọn ngày giờ

_**Ví dụ**:_&#x20;

_Trường Email khách (key field: email\_khach) ở Mục kích hoạt có giá trị như sau_

<table><thead><tr><th width="377">Trường</th><th>Giá trị</th></tr></thead><tbody><tr><td>Thời điểm (thoi_diem)</td><td>05.08.2024 09:00</td></tr></tbody></table>

**Lấy thông tin của trường**

<table><thead><tr><th width="187">Smart values</th><th>Mô tả</th><th>Ví dụ</th></tr></thead><tbody><tr><td>Mặc định</td><td><p>Smart values truy cập đến mã trường (key field) → mặc định trả về <strong>giá trị của trường</strong></p><p>(Sử dụng để cập nhật trường <strong>Chọn ngày giờ</strong> qua <strong>Smart values</strong>)</p></td><td><pre><code>${trigger.fields.thoi_diem}
</code></pre><p>→ <strong>Giá trị trả về</strong>: 2024-08-05T00:09:00.000+07:00</p></td></tr><tr><td><strong>datetime()</strong></td><td>Trả về kết quả có định dạng</td><td><pre><code>${trigger.fields.class.thoi_diem.datetime()}
</code></pre><p>→ <strong>Giá trị trả về</strong>: 05/08/2024 09:00</p></td></tr><tr><td><strong>after('</strong><em><strong>value</strong></em><strong>')</strong></td><td>Kiểm tra giá trị của trường có sau giá trị đưa vào</td><td><pre><code>${trigger.fields.thoi_diem.after('08/08/2024 09:00')}
</code></pre><p>→ <strong>Giá trị trả về</strong>: false</p></td></tr><tr><td><strong>before('</strong><em><strong>value</strong></em><strong>')</strong></td><td>Kiểm tra giá trị của trường có trước giá trị đưa vào</td><td><pre><code>${trigger.fields.thoi_diem.before('08/08/2024 09:00')}
</code></pre><p>→ <strong>Giá trị trả về</strong>: true</p></td></tr><tr><td><strong>empty()</strong></td><td>Kiểm tra trường có trống hay không (trả về <em>true / false</em>)</td><td><pre><code>${trigger.fields.thoi_diem.empty()}
</code></pre><p>→ <strong>Giá trị trả về:</strong> false</p></td></tr><tr><td><strong>plusHours()</strong></td><td>Cộng thêm giờ, cộng thêm số nguyên</td><td><pre><code>${trigger.fields.thoi_diem.plusHours(5)}
</code></pre><p>→ <strong>Giá trị trả về:</strong> 2024-08-10T00:14:00.000+07:00</p><pre><code>${trigger.fields.thoi_diem.plusDays(${trigger.fields.so_luong})}
</code></pre><p>Giá trị trường Số lượng: 3</p><p>→ <strong>Giá trị trả về:</strong> 2024-08-08T00:11:00.000+07:00</p></td></tr><tr><td><strong>plusDay()</strong></td><td>Cộng thêm ngày, cộng thêm số nguyên</td><td><pre><code>${trigger.fields.thoi_diem.plusDays(5)}
</code></pre><p>→ <strong>Giá trị trả về:</strong> 2024-08-10T00:09:00.000+07:00</p><pre><code>${trigger.fields.thoi_diem.plusDays(${trigger.fields.so_luong})}
</code></pre><p>Giá trị trường Số lượng: 3</p><p>→ <strong>Giá trị trả về:</strong> 2024-08-08T00:09:00.000+07:00</p></td></tr><tr><td><strong>plusMonths()</strong></td><td>Cộng thêm tháng, cộng thêm số nguyên</td><td><pre><code><strong>${trigger.fields.thoi_diem.plusMonths(5)}
</strong></code></pre><p>→ <strong>Giá trị trả về:</strong> 2025-01-05T00:09:00.000+07:00</p><pre><code>${trigger.fields.thoi_diem.plusDays(${trigger.fields.so_luong})}
</code></pre><p>Giá trị trường Số lượng: 3</p><p>→ <strong>Giá trị trả về:</strong> 2024-11-05T00:09:00.000+07:00</p></td></tr></tbody></table>

**Tính khoảng thời gian giữa 2 trường:**

Có thể sử dụng cú pháp sau để tính khoảng thời gian giữa 2 trường ngày giờ:

```
$trigger.fields.[key_field_1].diff($trigger.fields.[key_fields_2]).[abs].[unit_time]
```

trong đó:

* _\[key\_field\_1]:_ mã trường ngày giờ đích
* _\[key\_field\_2]:_ mã trường ngày giờ bắt đầu
* _\[abs]:_ có thể có hoặc không, giúp trả về giá trị tuyệt đối giữa 2 khoảng thời gian
* _\[unit\_time]:_ đơn vị thời gian muốn tính ra kết quả&#x20;
  * _millis_: mili giây
  * _seconds:_ giây
  * _minutes:_ phút
  * _hours:_ giờ
  * _days:_ ngày

_**Ví dụ**:_&#x20;

_Tính khoảng thời gian giữa 2 trường kiểu Ngày giờ là Thời điểm bắt đầu (start\_time) và Thời điểm kết thúc (end\_time) ở Mục kích hoạt:_

<table><thead><tr><th width="377">Trường</th><th>Giá trị</th></tr></thead><tbody><tr><td>Thời điểm bắt đầu (start_time)</td><td>05.08.2024 09:00</td></tr><tr><td>Thời điểm kết thúc (end_time)</td><td>05.09.2024 20:30</td></tr></tbody></table>

```
$trigger.fields.start_time.diff($trigger.fields.end_time).millis
$trigger.fields.start_time.diff($trigger.fields.end_time).seconds
$trigger.fields.start_time.diff($trigger.fields.end_time).minutes
$trigger.fields.start_time.diff($trigger.fields.end_time).hours
$trigger.fields.start_time.diff($trigger.fields.end_time).days
```

→ **Giá trị trả về:**&#x20;

2719800000\
2719800\
45330\
755\
31

### Email

1. Tổng quan

Sử dụng smart values để lấy giá trị từ các trường:

* Một email
* Nhiều email

2. Mô tả

2.1. Một email

_**Ví dụ**:_&#x20;

_Trường Email khách (key field: email\_khach) ở Mục kích hoạt có giá trị như sau_

<table><thead><tr><th width="377">Trường</th><th>Giá trị</th></tr></thead><tbody><tr><td>Email khách (email_khach)</td><td>a@gmail.com</td></tr></tbody></table>

**Lấy thông tin của trường**

<table><thead><tr><th>Smart values</th><th>Mô tả</th><th>Ví dụ</th></tr></thead><tbody><tr><td>Mặc định</td><td>Smart values truy cập đến mã trường (key field) → mặc định trả về <strong>id người dùng</strong></td><td><pre><code>${trigger.fields.email_khach}
</code></pre><p>→ <strong>Giá trị trả về</strong>: a@<a href="https://gmail.com/">gmail.com</a></p></td></tr><tr><td><strong>empty()</strong></td><td>Kiểm tra trường có trống hay không (trả về <em>true / false</em>)</td><td><pre><code>${trigger.fields.email_khach.empty()}
</code></pre><p>→ <strong>Giá trị trả về:</strong> false</p></td></tr></tbody></table>

2.2. Nhiều mail

<table><thead><tr><th width="377">Trường</th><th>Giá trị</th></tr></thead><tbody><tr><td>Email nhận (email_nhan)</td><td>a@<a href="https://gmail.com/">gmail.com</a>, b@<a href="https://gmail.com/">gmail.com</a>, c@<a href="https://gmail.com/">gmail.com</a></td></tr></tbody></table>

**Lấy thông tin từ trường**

Các giá trị khi trả về mặc định **phân tách nhau bởi** **dấu phảy,** người dùng có thể chủ động đổi kí tự phân tách

<table><thead><tr><th>Smart values</th><th>Mô tả</th><th>Ví dụ</th></tr></thead><tbody><tr><td>Mặc định</td><td>Smart values truy cập đến mã trường (key field) → Mặc định trả về <strong>danh sách các id người dùng</strong></td><td><pre><code>${trigger.fields.email_nhan}
</code></pre><p>→ <strong>Giá trị trả về</strong>: a@<a href="https://gmail.com/">gmail.com</a>, b@<a href="https://gmail.com/">gmail.com</a>, c@<a href="https://gmail.com/">gmail.com</a><br></p></td></tr><tr><td><strong>Dạng list</strong></td><td>Do thuộc kiểu trường dữ liệu multi nên khi lấy giá trị từ <strong>trường Nhiều email</strong> có thể sử dụng các <strong>smart values dạng list</strong>. Đọc thêm <a href="smart-value.md#list-kieu-truong-multi">Tại đây</a></td><td></td></tr></tbody></table>

### PhoneNumber

1. Tổng quan

Sử dụng smart values để lấy giá trị từ trường Số điện thoại

2. Mô tả

_**Ví dụ**:_&#x20;

_Trường Số liên hệ (key field: so\_lien\_he) ở Mục kích hoạt có giá trị như sau_

<table><thead><tr><th width="377">Trường</th><th>Giá trị</th></tr></thead><tbody><tr><td>Số liên hệ (so_lien_he)</td><td>8423124124</td></tr></tbody></table>

**Lấy thông tin của trường:**

<table><thead><tr><th>Smart values</th><th>Mô tả</th><th>Ví dụ</th></tr></thead><tbody><tr><td>Mặc định</td><td>Smart values truy cập đến mã trường (key field) → mặc định trả về <strong>giá trị của trường</strong></td><td><pre><code>${trigger.fields.so_lien_he}
</code></pre><p>→ <strong>Giá trị trả về</strong>: 8423124124</p></td></tr><tr><td><strong>empty()</strong></td><td>Kiểm tra trường có trống hay không (trả về <em>true / false</em>)</td><td><pre><code><strong>${trigger.fields.so_lien_he.empty()}
</strong></code></pre><p>→ <strong>Giá trị trả về:</strong> false</p></td></tr></tbody></table>

### Number

1. Tổng quan

Sử dụng smart values để lấy giá trị từ các trường:

* Số nguyên
* Số thập phân
* Công thức

2. Mô tả

2.1. Số nguyên

_**Ví dụ**:_&#x20;

_Trường Số lượng (key field: so\_luong) ở Mục kích hoạt có giá trị như sau_

<table><thead><tr><th width="377">Trường</th><th>Giá trị</th></tr></thead><tbody><tr><td>Số lượng (so_luong)</td><td>5</td></tr></tbody></table>

**Lấy thông tin của trường**

<table><thead><tr><th>Smart values</th><th>Mô tả</th><th>Ví dụ</th></tr></thead><tbody><tr><td>Mặc định</td><td>Smart values truy cập đến mã trường (key field) → mặc định trả về <strong>giá trị của trường</strong></td><td><pre><code>${trigger.fields.so_luong}
</code></pre><p>→ <strong>Giá trị trả về</strong>: 5</p></td></tr><tr><td><strong>empty()</strong></td><td>Kiểm tra trường có trống hay không (trả về <em>true / false</em>)</td><td><pre><code>${trigger.fields.so_luong.empty()}
</code></pre><p>→ <strong>Giá trị trả về:</strong> false</p></td></tr></tbody></table>

2.2. Số thập phân

_**Ví dụ**:_&#x20;

_Trường Chiều dài (key field: chieu\_dai) ở Mục kích hoạt có giá trị như sau_

| Trường                 | Giá trị | Hiển thị ngoài issue                                                                                  |
| ---------------------- | ------- | ----------------------------------------------------------------------------------------------------- |
| Chiều dài (chieu\_dai) | 0,5     | <p>Dạng Cơ bản: 0,5</p><p>Dạng Phần trăm: 50%</p><p>Dạng Tiền tệ: $ 0,5</p><p>Dạng Khoa học: 5E-1</p> |

**Lấy thông tin của trường**

<table><thead><tr><th>Smart values</th><th>Mô tả</th><th>Ví dụ</th></tr></thead><tbody><tr><td>Mặc định</td><td>Smart values truy cập đến mã trường (key field) → mặc định trả về <strong>giá trị của trường</strong></td><td><pre><code>${trigger.fields.chieu_dai}
</code></pre><p>→ <strong>Giá trị trả về</strong>: 0,5</p></td></tr><tr><td><strong>format()</strong></td><td>Hiển thị giá trị dưới định dạng đã chọn</td><td><pre><code>${trigger.fields.class.chieu_dai.format()}
</code></pre><p>→ <strong>Giá trị trả về</strong>:</p><p>Cơ bản: 0,5</p><p>Phần trăm: 50%</p><p>Tiền tệ: $ 0,5</p><p>Khoa học: 5E-1</p></td></tr><tr><td><strong>empty()</strong></td><td>Kiểm tra trường có trống hay không (trả về <em>true / false</em>)</td><td><pre><code>${trigger.fields.chieu_dai.empty()}
</code></pre><p>→ <strong>Giá trị trả về:</strong> false</p></td></tr></tbody></table>

2.3. Công thức

_**Ví dụ**:_&#x20;

_Trường Khoảng cách (key field: khoang\_cach) ở Mục kích hoạt có giá trị như sau_

| Trường                     | Giá trị | Hiển thị ngoài issue                                                                                    |
| -------------------------- | ------- | ------------------------------------------------------------------------------------------------------- |
| Khoảng cách (khoang\_cach) | 1,5     | <p>Dạng Cơ bản: 1,5</p><p>Dạng Phần trăm: 150%</p><p>Dạng Tiền tệ: $ 1,5</p><p>Dạng Khoa học: 1,5E0</p> |

**Lấy thông tin của trường**

<table><thead><tr><th>Smart values</th><th>Mô tả</th><th>Ví dụ</th></tr></thead><tbody><tr><td>Mặc định</td><td>Smart values truy cập đến mã trường (key field) → mặc định trả về <strong>giá trị của trường</strong></td><td><pre><code>${trigger.fields.khoang_cach}
</code></pre><p>→ <strong>Giá trị trả về</strong>: 1,5</p></td></tr><tr><td><strong>format()</strong></td><td>Hiển thị giá trị dưới định dạng đã chọn</td><td><pre><code>${trigger.fields.class.khoang_cach.format()}
</code></pre><p>→ <strong>Giá trị trả về</strong>:</p><p>Cơ bản: 1,5</p><p>Phần trăm: 150%</p><p>Tiền tệ: $ 1,5</p><p>Khoa học: 1,5E0</p></td></tr><tr><td><strong>empty()</strong></td><td>Kiểm tra trường có trống hay không (trả về <em>true / false</em>)</td><td><pre><code>${trigger.fields.khoang_cach.empty()}
</code></pre><p>→ <strong>Giá trị trả về:</strong> false</p></td></tr><tr><td><strong>if-else</strong></td><td>Sử dụng if-else để tính toán giá trị</td><td>Link tài liệu: <a href="https://velocity.apache.org/engine/1.7/user-guide.html#if-elseif-else">Apache Velocity Engine - User Guide</a></td></tr></tbody></table>

### Text

1. Tổng quan

Sử dụng smart values để lấy giá trị từ các trường:

* Dòng chữ (text field)
* Đoạn văn bản (text area)

2. Mô tả

2.1. **Dòng chữ (text field)**

_**Ví dụ**:_&#x20;

_Trường Lời nhắc (key field: loi\_nhac) ở Mục kích hoạt có giá trị như sau_

<table><thead><tr><th width="377">Trường</th><th>Giá trị</th></tr></thead><tbody><tr><td>Lời nhắc (loi_nhac)</td><td>Dòng chữ này</td></tr></tbody></table>

**Lấy thông tin của trường**

<table><thead><tr><th>Smart </th><th>Mô tả</th><th>Ví dụ</th></tr></thead><tbody><tr><td>Mặc định</td><td>Smart values truy cập đến mã trường (key field) → mặc định trả về <strong>giá trị của trường</strong></td><td><pre><code>${trigger.fields.loi_nhac}
</code></pre><p>→ <strong>Giá trị trả về</strong>: Dòng chữ này</p></td></tr><tr><td><strong>empty()</strong></td><td>Kiểm tra trường có trống hay không (trả về <em>true / false</em>)</td><td><pre><code>${trigger.fields.loi_nhac.empty()}
</code></pre><p>→ <strong>Giá trị trả về:</strong> false</p></td></tr></tbody></table>

#### **2. Đoạn văn bản (text area)** <a href="#text-2.doanvanban-textarea" id="text-2.doanvanban-textarea"></a>

_**Ví dụ**:_&#x20;

_Trường Nội dung (key field: noi\_dung) ở Mục kích hoạt có giá trị như sau_

<table><thead><tr><th width="377">Trường</th><th>Giá trị</th></tr></thead><tbody><tr><td>Nội dung (noi_dung)</td><td>Đoạn văn bản này</td></tr></tbody></table>

**Lấy thông tin của trường**

<table><thead><tr><th>Smart values</th><th>Mô tả</th><th>Ví dụ</th></tr></thead><tbody><tr><td>Mặc định</td><td>Smart values truy cập đến mã trường (key field) → mặc định trả về <strong>giá trị của trường</strong></td><td><pre><code>${trigger.fields.noi_dung}
</code></pre><p>→ <strong>Giá trị trả về</strong>: Đoạn văn bản này</p></td></tr><tr><td><strong>empty()</strong></td><td>Kiểm tra trường có trống hay không (trả về <em>true / false</em>)</td><td><pre><code>${trigger.fields.noi_dung.empty()}
</code></pre><p>→ <strong>Giá trị trả về:</strong> false</p></td></tr></tbody></table>

### Component

1. Tổng quan

Sử dụng smart values để lấy giá trị từ component

2. Mô tả

_**Ví dụ**:_&#x20;

_Thành Phần (component) ở Mục kích hoạt có giá trị như sau_

<table><thead><tr><th width="377">Id</th><th>Giá trị</th></tr></thead><tbody><tr><td>fd1c4882-1ef2-11ef-b517-005056be9d7b</td><td>Quan trọng</td></tr></tbody></table>

**Lấy thông tin của trường**

<table><thead><tr><th>Smart values</th><th>Mô tả</th><th>Ví dụ</th></tr></thead><tbody><tr><td>Mặc định</td><td>Smart values truy cập đến mã trường (key field) → mặc định trả về <strong>tên của thành phần được chọn</strong></td><td><pre><code>${trigger.fields.component}
</code></pre><p>→ <strong>Giá trị trả về</strong>: Quan trọng</p></td></tr><tr><td><strong>id</strong></td><td>Trả về id của thành phần được chọn</td><td><pre><code>${trigger.fields.component.id}
</code></pre><p>→ <strong>Giá trị trả về</strong>: fd1c4882-1ef2-11ef-b517-005056be9d7b</p></td></tr><tr><td><strong>name</strong></td><td>Trả về tên của thành phần được chọn</td><td><pre><code>${trigger.fields.component.name}
</code></pre><p>→ <strong>Giá trị trả về</strong>: Quan trọng</p></td></tr></tbody></table>

### Issue picker

1. Tổng quát

Sử dụng smart values để lấy giá trị từ các trường Nhóm

* Chọn một mục
* Chọn nhiều mục

2. Mô tả

2.1. **Chọn một mục (single issue picker)**\
&#xNAN;_**Ví dụ:**_&#x20;

_Trường Danh sách công việc (key field: danh\_sach\_cong\_viec) có giá trị là issue In tài liệu_



| Issue Key | Tiêu đề     | Người làm | Trạng thái |
| --------- | ----------- | --------- | ---------- |
| CV-01     | In tài liệu | Hải.T.V   | ĐANG LÀM   |

**Lấy thông tin của trường**

<table><thead><tr><th>Smart values</th><th>Mô tả</th><th>Ví dụ</th></tr></thead><tbody><tr><td>Mặc định</td><td>Smart values truy cập đến mã trường (key field) → mặc định trả về <strong>Issue key các issue được chọn</strong></td><td><pre><code>${trigger.fields.danh_sach_cong_viec}
</code></pre><p>→ <strong>Giá trị trả về</strong>: CV-01</p></td></tr><tr><td><strong>Truy cập vào issue được chọn</strong></td><td><p>Lấy thông tin của issue được chọn (space, area, custom field,...)</p><p><strong>Cấu trúc</strong>: <code>${[issue].fields.[key_field_picker].fields.[key_field]}</code></p><p>Ta có thể truy cập vào thuộc tính các field của issue được chọn, đọc thêm các thuộc tính cho các field <a href="smart-value.md#fields">tại đây</a></p></td><td><p></p><pre><code>${trigger.fields.danh_sach_cong_viec.fields.title}
</code></pre><p>→ <strong>Giá trị trả về</strong>: In tài liệu</p><p><br></p><pre><code>${trigger.fields.danh_sach_cong_viec.fields.assignee.displayName}
</code></pre><p>→ <strong>Giá trị trả về</strong>: Hải.T.V</p></td></tr><tr><td><strong>empty()</strong></td><td>Kiểm tra trường có trống hay không (trả về <em>true / false</em>)</td><td><pre><code>${trigger.fields.danh_sach_cong_viec.empty()}
</code></pre><p>→ <strong>Giá trị trả về:</strong> false</p></td></tr></tbody></table>
