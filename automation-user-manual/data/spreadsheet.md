# Spreadsheet

Node Spreadsheet helps you read data from excel files or google sheets.

Node Spreadsheet giúp bạn đọc dữ liệu từ file excel hoặc google sheet.

### Giải thích các trường của node

<figure><img src="../../.gitbook/assets/image (14).png" alt=""><figcaption></figcaption></figure>

**Local file:**&#x20;

* Path to the file: Chọn file excel có sẵn trong máy của bạn.
* Range: Một nhóm các ô trong file excel. Ví dụ bạn muốn đọc dữ liệu từ ô A1 đếm ô E5, ta sẽ nhập trường Range là A1:E5. Trường range này chỉ có thể nhập chữ hoa.
* Sheet name: Tên của excel sheet. Nếu bỏ trống ô này, sẽ mặc định lấy sheet name đầu tiên.
* First row as keys: Khi tick vào checkbox này, ta sẽ coi hàng đầu tiên của excel là tên của các cột dữ liệu, khi không chọn checkbox thì các hàng đều ngang hàng nhau.
* Save to: Lưu giá trị lấy được vào biến
* Preview: Xem trước dữ liệu mà node đọc được từ file.
* Map key:&#x20;

&#x20;             **TH1: Khi chọn checkbox First row as keys, ta có bảng dữ liệu như sau:**&#x20;

<figure><img src="../../.gitbook/assets/image (16).png" alt=""><figcaption></figcaption></figure>

&#x20;        Khi chọn preview sẽ hiển thị như sau:

<figure><img src="../../.gitbook/assets/image (17).png" alt=""><figcaption></figcaption></figure>

Trường hợp này ta sẽ nhập map key:

&#x20;          \[0]\[“Email”]  : Thì kết quả sẽ lấy được giá trị email là abc@gmail.com

&#x20;          \[1]\[“Email”]  : Thì kết quả sẽ lấy được giá trị email là so1@gmail.com

Tương tự nếu muốn lấy password ra thì ta nhập map key :

&#x20;          \[0]\[“Password”]  : sẽ lấy được giá trị là a123123

&#x20;          \[1]\["Password"]  : sẽ lấy được giá trị là abcd123

&#x20;**TH2: Khi không chọn checkbox First row as keys, ta có bảng dữ liệu như sau:**&#x20;

<figure><img src="../../.gitbook/assets/image (18).png" alt=""><figcaption></figcaption></figure>

Khi click vào preview sẽ hiển thị như sau:

<figure><img src="../../.gitbook/assets/image (19).png" alt=""><figcaption></figcaption></figure>

&#x20;    Khi đó map Key ta sẽ nhập:

&#x20;                \[0]\[0]  : Sẽ lấy được giá trị là abc@gmail.com

&#x20;                \[0]\[1] : Sẽ lấy được giá tri là a123123

&#x20;                \[1]\[0]  : sẽ lấy được giá trị là so1@gmail.com

&#x20;                \[1]\[1]  : Sẽ lấy được giá trị là abcd123



### Hướng dẫn đọc từng hàng khớp với từng profile

<figure><img src="../../.gitbook/assets/image (34).png" alt=""><figcaption></figcaption></figure>

Ta có Script như sau:

<figure><img src="../../.gitbook/assets/image (33).png" alt=""><figcaption></figcaption></figure>

Với trường hợp này ta sẽ tạo một biến ${index} có giá trị là 1.&#x20;

Các node ta nhập như sau:&#x20;

<figure><img src="../../.gitbook/assets/image (35).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (36).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (37).png" alt=""><figcaption></figcaption></figure>

Với bảng dữ liệu như trên thì tại node for ta sẽ cho chạy 10 vòng lặp. Mỗi vòng lặp ta sẽ chạy qua từng hàng của file excel nhờ node Set variable, node làm giá trị của biến index tăng lên 1 sau mỗi vòng lặp. Khi biến này được tăng lên thì trường Range của node Spreadsheet qua mỗi vòng lặp sẽ lần lượt là A1:B1, A2:B2, A3:B3,....... Khi lặp như vậy ta sẽ sử dụng node if làm điều kiệm để so sánh Profile\_id của profile đang chạy với uuid của file excel. Nếu Profile\_id trùng với uuid của file excel thì dừng vòng lặp và ghi dữ liệu của hàng đó vào biến để sử dụng cho các node tiếp theo.

Dưới đây là một script ví dụ của node đọc file, với ví dụ này sẽ đọc lần lượt theo từng hàng và tương ứng với từng profile mà bạn chạy. Bạn phải thay dữ liệu trong cột uuid bằng uuid của các profile mà bạn muốn chạy.

{% file src="../../.gitbook/assets/example 2 (2).xlsx" %}

{% file src="../../.gitbook/assets/Spreadsheet.txt" %}
