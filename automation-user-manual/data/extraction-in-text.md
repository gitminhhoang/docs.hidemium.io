# Extraction In Text

To extract specific values from a block of text, utilize regex ( Regular Expression) with rule A(.\*)\B. Example: you want to take a verify code in a message like "The authentication code is 128293. Please....." so you have a formula is "is(.\*)\\. Please" and the value returned to you is 128293. \
\
Để trích xuất các giá trị cụ thể từ một khối văn bản, hãy sử dụng biểu thức chính quy (Regular Expression) với quy tắc A(._)\B. Ví dụ: bạn muốn lấy mã xác minh trong thông báo như "Mã xác thực là 128293. Vui lòng...." vậy là bạn có công thức là "là(.). Vui lòng_" và giá trị trả về cho bạn là 128293.

<figure><img src="../../.gitbook/assets/Extraction In Text.jpg" alt=""><figcaption></figcaption></figure>

<table><thead><tr><th width="260">parameter</th><th>illustrate</th></tr></thead><tbody><tr><td>Data</td><td>Chọn biến chứa một đoạn text cần trích xuất</td></tr><tr><td>Extract rules</td><td>Nhập các biểu thức Regex để lấy dữ liệu</td></tr><tr><td>Save to</td><td>Lưu giá trị vừa trích xuất được vào biến</td></tr></tbody></table>

{% file src="../../.gitbook/assets/Extraction In Text (2).txt" %}
