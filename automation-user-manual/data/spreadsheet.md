# Spreadsheet

Node Spreadsheet giúp bạn đọc dữ liệu từ file excel hoặc google sheet.

<figure><img src="../../.gitbook/assets/image (14).png" alt=""><figcaption></figcaption></figure>

**Local file:** Khi bạn muốn đọc file excel hãy chọn Local file.

* Path to the file: Chọn file excel có sãn trong máy cảu bạn.
* Range: Một nhóm các ô trong file excel. Ví dụ bạn muốn đọc dữ liệu từ ô A1 đếm ô E5, ta sẽ nhập trường Range là A1:E5
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



Dưới đây là một script ví dụ của node đọc file, với ví dụ này sẽ đọc lần lượt theo từng hàng và tương ứng với từng profile mà bạn chạy.



{% file src="../../.gitbook/assets/Spreadsheet.txt" %}

