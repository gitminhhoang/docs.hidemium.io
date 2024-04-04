# File upload

You can upload files to your desired website. Website file upload buttons need to have an **Input** tag with **type="file"**.&#x20;

Note that there are some websites that have an **Input** tag with **type="file"** but have this **Display: none** attribute, so you cannot get the selector of this input type, you must get the selector of the **Label** tag above the **Input** tag.



Bạn có thể tải tệp lên trang web mà bạn mong muốn. Các button upload file của trang web cần có thẻ **Input** với **type="file".**&#x20;

Lưu ý có một vài trang web có thẻ **Input** với **type="file"** nhưng lại có thuộc tính **Display: none** này thì bạn không thể lấy selector của thể input này được, mà bạn phải lấy selector của thẻ **Label** bên trên thẻ **Input.**

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/File upload.png" alt=""><figcaption></figcaption></figure>

<table><thead><tr><th width="260">parameter</th><th>illustrate</th></tr></thead><tbody><tr><td>Select element</td><td><p>Enter the CSS selector of the element to upload</p><p></p><p>Nhập CSS selector của phần tử cần upload</p></td></tr><tr><td>Element order</td><td><p>Select elements based on the order they appear on the page</p><p></p><p>Chọn các thành phần dựa trên thứ tự chúng xuất hiện trên trang</p></td></tr><tr><td>Path to the file</td><td><p>Local file: select a local file to upload. </p><p>Folder file random: choose a folder and randomly upload a file in the folder. </p><p>Network file: to upload a network file, enter a URL starting with http/https.</p><p></p><p>Local file: chọn một tệp cục bộ để tải lên<br>Folder file random: chọn một thư mục và tải lên ngẫu nhiên một tệp trong thư mục.<br>Network file: để tải lên tệp mạng, hãy nhập URL bắt đầu bằng http/https.</p></td></tr><tr><td>Timeout waiting</td><td><p>Maximum waiting time. For example: 30000. If this step is not performed successfully within 30 seconds, the next step will be performed directly.</p><p></p><p>Thời gian chờ đợi tối đa. Ví dụ: 30000. Nếu bước này không được thực hiện thành công trong vòng 30 giây thì bước tiếp theo sẽ được thực hiện trực tiếp.</p></td></tr></tbody></table>

{% file src="../../.gitbook/assets/File upload.txt" %}
