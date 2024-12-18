# HTTP

此节点可能具有挑战性，特别是对于那些对 HTTP 知识有限的人。但是，对 HTTP 有很好的理解将使其更容易使用。本质上，此 HTTP 使用 GET 或 POST 方法向 API 发送请求，并在下面的标签页中显示响应。

<figure><img src="../../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

输入 URL：请求 URL 地址

请求方法：GET、POST、PUT、DELETE。

标头：请求的标头

Cookie：HTTP Cookie

选择内容类型：选择您的内容类型。

响应 body mapping：请求的响应

**示例 1：**&#x41;PI 有以下响应：

```
[
    {
        "value": 132,
        "label": "tag 1"
    },
    {
        "value": 136,
        "label": "tag 2"
    },
    {
        "value": 137,
        "label": "tag 3"
    },
    {
        "value": 138,
        "label": "tag 4"
    }
]
```

要获取“label”：“tag 3”的值，我们编写：2.value

<figure><img src="../../.gitbook/assets/image (13).png" alt=""><figcaption></figcaption></figure>

**示例 2**：我们有以下响应：



```
{
    "status": "success",
    "data": [
        {
            "id": 7,
            "email": "michael.lawson@gmail.com.",
            "first_name": "Michael",
            "last_name": "Lawson"
        },
        {
            "id": 8,
            "email": "lindsay.ferguson@gmail.com",
            "first_name": "Lindsay",
            "last_name": "Ferguson"
        },
        {
            "id": 9,
            "email": "tobias.funke@gmail.com",
            "first_name": "Tobias",
            "last_name": "Funke"
        }
    ]
    }
}
```

想获取 "first\_name"的邮件: "Michael", 我们编写 `data.0.email`

此外，如果您想获取整个 api 响应，您可以编写如下：

<figure><img src="../../.gitbook/assets/image (14).png" alt=""><figcaption></figcaption></figure>

在响应body中 mapping，输入响应并选择用于存储数据的变量，这样您就可以获取该 API 的整个响应。
