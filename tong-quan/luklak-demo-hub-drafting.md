---
hidden: true
---

# Luklak Demo Hub (drafting)

{% @guidejar/embed guideId="ccb39e2f-66c2-43a9-b757-f578bbe20543" type="1" controls="on" url="https://www.guidejar.com/embed/ccb39e2f-66c2-43a9-b757-f578bbe20543?controls=on&type=1" %}

### heading 2

#### heading 3

````mermaid
```mermaid

flowchart TB

    subgraph LUKLAK["🔄 HỆ THỐNG LUKLAK"]

        WF[Quy trình nghiệp vụ]

        AUTO[Tự động hóa]

        OBJ[Đối tượng phổ quát]

        DASH[Báo cáo & Thống kê]

    end

  

    subgraph SHEET["📊 GOOGLE SHEET"]

        DS[Danh mục Vật tư]

        GIA[Bảng giá]

        BG[Báo giá chi tiết]

        PS[Quản lý Phát sinh]

    end

  

    subgraph N8N["⚙️ N8N"]

        SYNC[Đồng bộ dữ liệu]

    end

  

    LUKLAK <-->|Webhook/HTTP| N8N

    N8N <-->|Sheet API| SHEET

```
````



{% @guidejar/embed guideId="85bd23c8-b73f-4174-862d-d768b11676aa" type="1" controls="on" url="https://www.guidejar.com/embed/85bd23c8-b73f-4174-862d-d768b11676aa?controls=on&type=1" %}

{% @guidejar/embed guideId="1596e906-d27c-4d14-946b-abf2c9346dd1" type="1" controls="on" url="https://www.guidejar.com/embed/1596e906-d27c-4d14-946b-abf2c9346dd1?type=1&controls=on" fullWidth="false" %}

{% tabs %}
{% tab title="First Tab" %}
{% @guidejar/embed guideId="1596e906-d27c-4d14-946b-abf2c9346dd1" type="1" controls="on" url="https://www.guidejar.com/embed/1596e906-d27c-4d14-946b-abf2c9346dd1?type=1&controls=on" %}
{% endtab %}

{% tab title="Second Tab" %}

{% endtab %}
{% endtabs %}

