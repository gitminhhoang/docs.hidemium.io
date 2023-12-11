# Extraction In Text

To extract specific values from a block of text, utilize regex ( Regular Expression) with rule A(.\*)\B. Example: you want to take a verify code in a message like "The authentication code is 128293. Please....." so you have a formula is "is(.\*)\\. Please" and the value returned to you is 128293. \
\
Để trích xuất các giá trị cụ thể từ một khối văn bản, hãy sử dụng biểu thức chính quy (Regular Expression) với quy tắc A(._)\B. Ví dụ: bạn muốn lấy mã xác minh trong thông báo như "Mã xác thực là 128293. Vui lòng...." vậy là bạn có công thức là "là(.). Vui lòng_" và giá trị trả về cho bạn là 128293.

<figure><img src="../../.gitbook/assets/image (4) (1) (1).png" alt=""><figcaption></figcaption></figure>

<table><thead><tr><th width="260">parameter</th><th>illustrate</th></tr></thead><tbody><tr><td>Data</td><td>Chọn biến chứa một đoạn text cần trích xuất</td></tr><tr><td>Extract rules</td><td>Nhập các biểu thức Regex để lấy dữ liệu</td></tr><tr><td>Index result</td><td>Nhập index của kết quả lấy được, nếu không nhập node sẽ tự lấy động lấy index số 0</td></tr><tr><td>Save to</td><td>Lưu giá trị vừa trích xuất được vào biến và giá trị này sẽ dựa vào index mà bạn chọn</td></tr><tr><td>Test</td><td>Khi click vào bạn có thể thấy kết quả mà bạn đã trích xuất được kèm theo index </td></tr></tbody></table>

Ví dụ ta có một đoạn dữ liệu như sau: "_We have the following websites https://www.facebook.com/ and other websites like https://www.youtube.com/ and https://www.etsy.com/_". Khi muốn lấy URL có trong đoạn dữ liệu này, tại node Extraction in text ta nhập như sau:&#x20;

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Tại&#x20;

{% file src="../../.gitbook/assets/Extraction In Text (2).txt" %}
