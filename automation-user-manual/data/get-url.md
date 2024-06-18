# Get URL

When you use the Get URL node, you can get relevant information about website links, store the relevant information in a variable, and call it for other operations.

Khi bạn sử dụng node Get URL, bạn có thể lấy thông tin liên quan về các links trang web, lưu trữ thông tin liên quan trong một biến và gọi nó cho các hoạt động khác.

<figure><img src="../../.gitbook/assets/image (13) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Let's assume that the URL being opened is: [https://www.etsy.com/search?q=book\&ref=search\_bar](https://www.etsy.com/search?q=book\&ref=search\_bar)

Giả sử rằng URL được mở là: [https://www.etsy.com/search?q=book\&ref=search\_bar](https://www.etsy.com/search?q=book\&ref=search\_bar)

| parameter           | illustrate                                                                                                                                                                                         |
| ------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Content: Full URL   | Lấy toàn bộ URL là: [https://www.etsy.com/search?q=book\&ref=search\_bar](https://www.etsy.com/search?q=book\&ref=search\_bar)                                                                     |
| Content: Domain     | <p>Get the domain of the URL: www.etsy.com</p><p></p><p>Lấy domain của URL là: www.etsy.com</p>                                                                                                    |
| Content: Search key | <p>When entering "q", store "book" in variable. When entering "ref", save "search_bar" in variable.</p><p></p><p>Khi nhập "q", lưu "book" vào biến. Khi nhập "ref", lưu "search_bar" vào biến.</p> |
| Output Variable     | <p>Save the obtained value into the variable</p><p></p><p>Lưu giá trị lấy được vào biến</p>                                                                                                        |

{% file src="../../.gitbook/assets/Get URL.txt" %}
