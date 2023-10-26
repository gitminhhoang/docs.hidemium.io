# Spreadsheet V2

Node Spreadsheet là Version 2 của node Spreadsheet. Với V2 này, các bản có thể đọc file excel và file google sheet một cách dễ dàng hơn so với node Spreadsheet.

<figure><img src="../../.gitbook/assets/image (22).png" alt=""><figcaption></figcaption></figure>

### Local File

* Path to file: Chọn file mà bạn muốn đọc.
* Range: Một nhóm các ô trong file excel. Ví dụ bạn muốn đọc dữ liệu từ ô A1 đếm ô E5, ta sẽ nhập trường Range là A1:E5. Bạn cũng có thể bỏ trống trường này.
* Sheet name: Tên của excel sheet. Nếu bỏ trống ô này, sẽ mặc định lấy sheet name đầu tiên.
* First row as title (Column name): Khi tick vào checkbox này, ta sẽ coi hàng đầu tiên của excel là tên (tiêu đề) của các cột dữ liệu, khi không chọn checkbox thì các hàng đều ngang hàng nhau.
* Read row with stop condition: Khi bạn không chọn checkbox này thì node sẽ mặc định lấy dữ liệu của hàng đầu tiên. Khi bạn chọn checkbox này, bạn phải nhập 2 trường _Column to compare và Value to compare_**.** Column to compare: Trường này bạn sẽ nhập cột để so sánh . Value to compare : Trường này bạn sẽ nhập giá trị để so sánh.&#x20;
* Storage: Bao gồm 2 trường là _Column name và Save to._ Với trường Column ta sẽ phải nhập đúng tên của cột dữ liệu. Còn trường Save to ta sẽ lưu giá trị đọc được từ Column name vào một biến.
* Preview: Hiển thị dữ liệu mà node đã đọc được.

### Google sheet

* Google Spreadsheet ID: Nhập sheet ID của google sheet mà bạn muốn đọc dữ liệu. Google sheet của bạn phải ở trạng thái công khai.
* Các trường khác giống như phần Local file.

### Hướng dẫn chi tiết

**Trường hợp chọn checkbox First row as title (Column name):**

Ta có bảng dữ liệu như sau:

<figure><img src="../../.gitbook/assets/image (28).png" alt=""><figcaption></figcaption></figure>

Ở node Spreadsheet ta nhập như sau:

<figure><img src="../../.gitbook/assets/image (29).png" alt=""><figcaption></figcaption></figure>

Ở trường hợp này khi chọn checkbox First row as title (Column name), thì ta sẽ lấy hàng đầu tiên của Range mà bạn nhập là tiêu đề của cột. Và các trường Column to compare, Column name ta phải nhập đúng tên cột của bảng mà bạn đã đặt, ví dụ trong trường hợp này tên cột sẽ là email và password. Khi nhập vào các trường trong node như hình trên thì ta lấy được dữ liệu như hiển thị trong preview. Nếu khi ta không chọn checkbox Read row with stop condition thì mặc định sẽ lấy hàng đầu tiên của file ngoại trừ hàng đầu tiên được đặt làm tiêu đề.

**Trường hợp không chọn checkbox First row as title (Column name):**

<figure><img src="../../.gitbook/assets/image (30).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (31).png" alt=""><figcaption></figcaption></figure>

Ở trường hợp này khi chọn checkbox First row as title (Column name), thì sẽ không lấy hàng đầu tiên làm tiêu đề của cột. Và các trường Column to compare, Column name ta phải nhập đúng tên cột của bảng, ví dụ trong trường hợp này tên cột sẽ là A, B, C,... . Khi nhập vào các trường trong node như hình trên thì ta lấy được dữ liệu như hiển thị trong preview. Nếu khi ta không chọn checkbox Read row with stop condition thì mặc định sẽ lấy dữ liệu hàng đầu tiên.

Dưới đây là một script ví dụ của node đọc file, với ví dụ này sẽ đọc lần lượt theo từng hàng và tương ứng với từng profile mà bạn chạy.

File excel dưới đây bạn có thể thay thế bằng uuid của các profile mà bạn sẽ chạy.

{% file src="../../.gitbook/assets/example.xlsx" %}

{% file src="../../.gitbook/assets/Spreadsheet V2.txt" %}

