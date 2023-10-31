# Get URL

Khi bạn sử dụng node Get URL, bạn có thể lấy thông tin liên quan về các links trang web, lưu trữ thông tin liên quan trong một biến và gọi nó cho các hoạt động khác.

<figure><img src="../../.gitbook/assets/image (13).png" alt=""><figcaption></figcaption></figure>

Giả sử rằng URL được mở là: [https://www.etsy.com/search?q=book\&ref=search\_bar](https://www.etsy.com/search?q=book\&ref=search\_bar)

| parameter           | illustrate                                                                                                                     |
| ------------------- | ------------------------------------------------------------------------------------------------------------------------------ |
| Content: Full URL   | Lấy toàn bộ URL là: [https://www.etsy.com/search?q=book\&ref=search\_bar](https://www.etsy.com/search?q=book\&ref=search\_bar) |
| Content: Domain     | Lấy domain của URL là: www.etsy.com                                                                                            |
| Content: Search key | Khi nhập "q", lưu "book" vào biến. Khi nhập "ref", lưu "search\_bar" vào biến.                                                 |
| Output Variable     | Lưu giá trị lấy được vào biến                                                                                                  |

{% file src="../../.gitbook/assets/Get URL.txt" %}
