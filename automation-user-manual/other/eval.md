---
description: Node thực thi các lệnh JavaScript được miêu tả trong một chuỗi.
---

# Eval

Node eval để chạy code javascript trong ngữ cảnh trình duyệt và có thể trả kết quả lưu vào variable. Các bạn có thể tham khảo [<mark style="color:blue;">**tại đây**</mark>](https://www.w3schools.com/js/).

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

| parameter         | illustrate                                                     |
| ----------------- | -------------------------------------------------------------- |
| JavaScript        | Nhập code javascript                                           |
| Inject variavles  | Chọn biến được chèn, biến này có thể được sử dụng trong hàm js |
| Output variable   | Lưu giá trị được hàm tập lệnh Javascript trả về vào một biến.  |

Ta có ví dụ như sau: Khi bạn truy cập một trang web nào đó, bạn muốn thực hiện click vào một phần tử, thay vì sử dụng node click bạn cũng có thể sử dụng node Eval để thực hiện hành động click đó. Ta có script đơn giản như sau:

<figure><img src="../../.gitbook/assets/image (60).png" alt=""><figcaption></figcaption></figure>

Tại node Eval bạn nhập như sau để có thể click vào phần tử bạn mong muốn:

<figure><img src="../../.gitbook/assets/image (61).png" alt=""><figcaption></figcaption></figure>

Bằng cách này bạn cũng có thể click vào phần tử mong muốn mà không cần sử dụng node click.

{% file src="../../.gitbook/assets/Eval.txt" %}
