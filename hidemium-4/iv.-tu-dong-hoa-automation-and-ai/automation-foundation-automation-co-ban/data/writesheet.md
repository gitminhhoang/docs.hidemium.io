# WriteSheet

### Giải thích các trường trong node

Khi bạn muốn ghi dữ liệu vào trong file excel thì có thể sử dụng node WriteSheet

<figure><img src="../../../../.gitbook/assets/image (97) (1).png" alt=""><figcaption></figcaption></figure>

### Local file

* Path to the file: Nhập đường dẫn hoặc chọn biến chứa đường dẫn của file excel của bạn.
* Sheet name: Nhập sheet name của file excel. Nếu bạn bỏ trống trường này, node sẽ tự động lấy sheet đầu tiên để ghi dữ liệu.
* Checkbox Append last row: Khi chọn checkbox này, node sẽ tự động ghi vào dòng tiếp theo của hàng cuối dữ liệu. Ví dụ dữ liệu trong file excel của bạn đến dòng 20 thì khi chọn checkbox này node sẽ tự ghi vào dòng tiếp theo là dòng thứ 21.&#x20;
* Cell location: Nhập vị trí mà bạn muốn ghi dữ liệu. Khi bạn không chọn checkbox Append last row thì bạn phải nhập ô cần ghi dữ liệu ví dụ A1, B1, A2,..... và nếu các ô đó đang có dữ liệu thì node sẽ ghi đè dữ liệu. Còn khi bạn chọn checkbox thì bạn chỉ cần nhập tên cột là A, B, C… thì node sẽ tự hiểu vào ghi vào dòng tiếp theo của hàng cuối  cùng chứa dữ liệu.
* Variable: Nhập giá trị mà bạn muốn ghi vào ô.



### Google sheet

<figure><img src="../../../../.gitbook/assets/image (98) (1).png" alt=""><figcaption></figcaption></figure>



* Google Spreadsheet ID: Nhập vào ID của file GoogleSheet

<figure><img src="../../../../.gitbook/assets/image (102) (1).png" alt=""><figcaption></figcaption></figure>



* Credentical file: chọn file Json đã tải về

**Hướng dẫn lấy file Credential:**

1\.      Truy cập link [https://console.cloud.google.com/](https://console.cloud.google.com/)  và đăng nhập

2\.      Sau khi đăng nhập thành công, ta tạo 1 project mới:

\-        Chọn Select a project

<figure><img src="../../../../.gitbook/assets/image (6) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

&#x20;

\-        Chọn new project

<figure><img src="../../../../.gitbook/assets/image (7) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

\-        Nhập tên project và chọn Create

<figure><img src="../../../../.gitbook/assets/image (8) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

3\.      Enable Google sheet API

\-        Tại thanh tìm kiếm nhập Google sheets API. Kết quả tìm kiếm hiện ra, sau đó tại Marketplace chọn Google sheet API

<figure><img src="../../../../.gitbook/assets/image (9) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

\-        Thực hiện enable Google sheets API

<figure><img src="../../../../.gitbook/assets/image (10) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

&#x20;

4\.      Tạo Credentials

\-        Sau khi enable Google sheets API thành công, tiếp tục chọn Credentials

<figure><img src="../../../../.gitbook/assets/image (11) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

&#x20;

\-        Chọn Create Credentials, sau đó chọn Service account

<figure><img src="../../../../.gitbook/assets/image (12) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

\-        Nhập Service account name sau đó chọn Done

<figure><img src="../../../../.gitbook/assets/image (13) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

\-        Account vừa tạo sẽ hiển thị ở đây:

<figure><img src="../../../../.gitbook/assets/image (14) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

\-        Click vào account đó và chọn tab Keys:

<figure><img src="../../../../.gitbook/assets/image (15) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

&#x20;

\-        Chọn Add key -> chọn Create new key:

<figure><img src="../../../../.gitbook/assets/image (16) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

&#x20;

\-        Chọn JSON -> Chọn create

<figure><img src="../../../../.gitbook/assets/image (17) (1) (1).png" alt=""><figcaption></figcaption></figure>

&#x20;

Sau khi tạo xong sẽ tự động tải file JSON về, và các bạn thêm file đó vào trường Credencial trong node WriteSheet

<figure><img src="../../../../.gitbook/assets/image (100) (1).png" alt=""><figcaption></figcaption></figure>

5\.      Shared sheet với account tạo ở bước trên

\-        Copy email tạo ở bước trên:

<figure><img src="../../../../.gitbook/assets/image (19) (1) (1).png" alt=""><figcaption></figcaption></figure>

&#x20;

\-        Shared trang sheet với account ở trên:

<figure><img src="../../../../.gitbook/assets/image (20) (1) (1).png" alt=""><figcaption></figcaption></figure>

&#x20;

Như vậy ta đã thực hiện Setup Google sheet để phục vụ việc đọc file trên google sheet thành công. Các trường bên dưới vẫn tương tự như Local file.

### Hướng dẫn chi tiết

Giả sử ta có bảng dữ liệu sau:

<figure><img src="../../../../.gitbook/assets/image (45) (1) (1).png" alt=""><figcaption></figcaption></figure>

* Nếu bạn muốn tự động ghi nối tiếp vào hàng tiếp theo của dòng cuối chứa dữ liệu, thì ta điền như sau:&#x20;

<figure><img src="../../../../.gitbook/assets/image (46) (1) (1).png" alt=""><figcaption></figcaption></figure>

Khi ta nhập thế này thì node sẽ tự ghi dữ liệu vào dòng số 7

* Hoặc nếu bạn không muốn ghi nối tiếp mà bạn muốn chỉ định ô để ghi dữ liệu bạn có thể nhập như sau:

<figure><img src="../../../../.gitbook/assets/image (47) (1).png" alt=""><figcaption></figcaption></figure>

Như vậy bạn có thể ghi dữ liệu vào vào các ô mà mình mong muốn. Hoặc bạn có thể nhập ô đã có dữ liệu, node sẽ ghi đè dữ liệu vào các ô mà bạn nhập.

Trường hợp bạn muốn ghi dữ liệu vào một file excel ngay sau khi đọc xong, và bạn muốn ghi đúng vào từng hàng tương ứng bạn có thể sử dụng trường Row data number và Total row datas của node Spreadsheet V2.

Giả sử ta có bảng dữ liệu sau:&#x20;

<figure><img src="../../../../.gitbook/assets/image (48) (1).png" alt=""><figcaption></figcaption></figure>

Và bạn muốn đọc từng hàng của file khớp với từng profile tương ứng theo uuid, thì node Spreadsheet V2 ta nhập như sau:&#x20;

<figure><img src="../../../../.gitbook/assets/image (49) (1).png" alt=""><figcaption></figcaption></figure>

Bạn muốn khi đọc thành công từng hàng thì sẽ ghi lại vào hàng tương ứng để biết profile đó có đọc thành công hay không thì bạn sẽ sử dụng node writeSheet để ghi lại:

<figure><img src="../../../../.gitbook/assets/image (50) (1).png" alt=""><figcaption></figcaption></figure>

Như vậy khi đọc thành công 1 hàng thì tại hàng tương ứng ta sẽ ghi chữ "Thành công".

Dưới đây là một script ví dụ về việc ghi vào file sau khi đọc file thành công, bạn hãy thay uuid của profile mà bạn muốn chạy vào file excel.

{% file src="../../../../.gitbook/assets/example (1).xlsx" %}

{% file src="../../../../.gitbook/assets/writesheet.txt" %}
