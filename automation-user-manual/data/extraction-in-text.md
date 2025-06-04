# Extraction In Text

To extract specific values from a block of text, utilize regex ( Regular Expression) with rule A(.\*)\B. Example: you want to take a verify code in a message like "The authentication code is 128293. Please....." so you have a formula is "is(.\*). Please" and the value returned to you is 128293. \
\
Để trích xuất các giá trị cụ thể từ một khối văn bản, hãy sử dụng biểu thức chính quy (Regular Expression) với quy tắc A(.\*_)\B. Ví dụ: bạn muốn lấy mã xác minh trong thông báo như "Mã xác thực là 128293. Vui lòng...." vậy là bạn có công thức là "là(.\*). Vui lòng_" và giá trị trả về cho bạn là 128293.

<figure><img src="../../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

<table><thead><tr><th width="260">parameter</th><th>illustrate</th></tr></thead><tbody><tr><td>Data</td><td><p>Select the variable containing a piece of text to extract.</p><p>Chọn biến chứa một đoạn text cần trích xuất.</p></td></tr><tr><td>Extract rules</td><td><p>Enter Regex expression to get data.</p><p>Nhập biểu thức Regex để lấy dữ liệu.</p></td></tr><tr><td>Index result</td><td><p>Enter the index of the result, if you do not enter the node will automatically get index 0.</p><p>Nhập index của kết quả lấy được, nếu không nhập node sẽ tự lấy động lấy index 0.</p></td></tr><tr><td>Save to</td><td><p>Save the extracted value into a variable and this value will be based on the index you choose.</p><p>Lưu giá trị vừa trích xuất được vào biến và giá trị này sẽ dựa vào index mà bạn chọn.</p></td></tr><tr><td>Test</td><td><p>When you click, you can see the results you have extracted with the index.</p><p>Khi click vào bạn có thể thấy kết quả mà bạn đã trích xuất được kèm theo index.</p></td></tr></tbody></table>

For example, we have a piece of data like this: "_We have the following websites https://www.facebook.com/ and other websites like https://www.youtube.com/ and https://www.etsy. com/_". When you want to get the URL contained in this piece of data, at the Extraction in text node, enter the following:

Ví dụ ta có một đoạn dữ liệu như sau: "_We have the following websites https://www.facebook.com/ and other websites like https://www.youtube.com/ and https://www.etsy.com/_". Khi muốn lấy URL có trong đoạn dữ liệu này, tại node Extraction in text ta nhập như sau:&#x20;

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

In the **Index result** field, enter the number 1, we will get **https://www.facebook.com/** and store it in the **result** variable.

Tại trường **Index result** nhập số 1 ta sẽ lấy được <mark style="color:blue;">https://www.facebook.com/</mark> và lưu vào biến **result**.

{% file src="../../.gitbook/assets/Extraction In Text (2).txt" %}
