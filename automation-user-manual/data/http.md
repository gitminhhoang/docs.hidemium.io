# HTTP

&#x20;This node can be challenging, especially for those with limited knowledge of HTTP. However, having a good understanding of HTTP will make it easier to use. In essence, this HTTP sends requests to the API using either the GET or POST method and displays the response in the tabs below.\
\
Node này có thể là một node khó, đặc biệt đối với những người có kiến ​​thức hạn chế về HTTP. Tuy nhiên, hiểu rõ về HTTP sẽ giúp sử dụng dễ dàng hơn. Về bản chất, HTTP này gửi yêu cầu tới API bằng phương thức GET hoặc POST và hiển thị phản hồi trong các tab bên dưới.

<figure><img src="../../.gitbook/assets/image (94).png" alt=""><figcaption></figcaption></figure>

* Enter URL: Request URL address
* [<mark style="color:blue;">**Request method**</mark>](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods): GET, POST, PUT, DELETE.&#x20;
* Headers:[ **Header**](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers) of the request
* Cookies:  [**HTTP cookies**](https://developer.mozilla.org/en-US/docs/Web/HTTP/Cookies)
* Select content Type: Select your content type.&#x20;
* Response body mapping: Response of the request&#x20;



* Nhập URL: Địa chỉ URL yêu cầu
* [**Phương thức yêu cầu**](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods): GET, POST, PUT, DELETE.&#x20;
* Headers:[ **Header**](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers) được yêu cầu
* Cookies:  [**HTTP cookies**](https://developer.mozilla.org/en-US/docs/Web/HTTP/Cookies)
* Select content Type: Chọn loại nội dung của bạn.
* Response body mapping: Phản hồi của yêu cầu

1. Example 1: The <mark style="color:blue;">**API**</mark> has the following response:

&#x20;       Ví dụ 1:  [**API**](https://docs.hidemium.io/use-cases/api-automation/get-profile/4.-list-tag) có response như sau:

```json
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

To get the <mark style="color:blue;">`Value`</mark> of "label": "tag 3" we write as follows: <mark style="color:blue;">`2.value`</mark>

Để lấy được <mark style="color:blue;">`Value`</mark> của "label": "tag 3" ta viết như sau: <mark style="color:blue;">`2.value`</mark>

<figure><img src="../../.gitbook/assets/image (62).png" alt=""><figcaption></figcaption></figure>

2. Example 2: We have the following response:

&#x20;       Ví dụ 2: Ta có đoạn response sau:

```json
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

To get the <mark style="color:blue;">`email`</mark> of <mark style="color:blue;">`"first_name": "Michael"`</mark>, we write <mark style="color:blue;">`data.0.email`</mark>

Để lấy được <mark style="color:blue;">`email`</mark> của <mark style="color:blue;">"first\_name": "Michael"</mark> , ta viết <mark style="color:blue;">`data.0.email`</mark>



Additionally, if you want to get the entire api response, you can write as follows:

Ngoài ra nếu bạn muốn lấy toàn bộ response của api thì bạn có thể ghi như sau:

<figure><img src="../../.gitbook/assets/image (95).png" alt=""><figcaption></figcaption></figure>

In **Response body mapping**, enter response and select the variable to store the data, so you can get the entire response of that API.

Tại **Response body mapping** bạn nhập là response và chọn biến để lưu dữ diệu, như vậy là bạn đã có thể lấy toàn bộ response của API đó.



Lưu ý: Trong phần body, các bạn không được nhập comment ở đó, nếu có comment thì khi chạy sẽ bị lỗi.

{% file src="../../.gitbook/assets/Http.txt" %}
