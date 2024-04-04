# Spreadsheet V2

Node Spreadsheet là Version 2 của node Spreadsheet. Với V2 này, các bạn có thể đọc file excel và file google sheet một cách dễ dàng hơn so với node Spreadsheet.

<figure><img src="../../.gitbook/assets/image (2) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Local File

* Path to file: Chọn file mà bạn muốn đọc.
* Range: Một nhóm các ô trong file excel. Ví dụ bạn muốn đọc dữ liệu từ ô A1 đếm ô E5, ta sẽ nhập trường Range là A1:E5. Bạn cũng có thể bỏ trống trường này. Range bắt buộc phải nhập là chữ hoa.
* Sheet name: Tên của excel sheet. Nếu bỏ trống ô này, sẽ mặc định lấy sheet name đầu tiên.
* First row as title (Column name): Khi tick vào checkbox này, ta sẽ coi hàng đầu tiên của excel là tên (tiêu đề) của các cột dữ liệu, khi không chọn checkbox thì các hàng đều ngang hàng nhau.
* Read row with stop condition: Khi bạn không chọn checkbox này thì node sẽ mặc định lấy dữ liệu của hàng đầu tiên. Khi bạn chọn checkbox này, bạn phải nhập 2 trường _Column to compare và Value to compare_**.** Column to compare: Trường này bạn sẽ nhập cột để so sánh. Value to compare: Trường này bạn sẽ nhập giá trị để so sánh. Khi không chọn checkbox này, chạy với nhiều profile thì tất cả các profile đều lấy dữ liệu cảu hàng đầu tiên.&#x20;
* Row match conditions: Chọn một biến. Trường này sẽ trả về số của hàng khớp với hàng mà node đang đọc đến và lưu vào biến bạn chọn. Bạn có thể sử dụng biến này vào node WriteSheet để ghi dữ liệu vào hàng tương ứng với hàng dữ liệu đang được đọc.  Ví dụ ta có bảng dữ liệu sau:

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

&#x20;        Với bảng dữ liệu này: Ví dụ dữ liệu đang được đọc ở hàng số 4, thì node sẽ lưu giá trị 4 vào biến mà bạn chọn.

* Last row of datas: Hiển thị hàng cuối cùng chứa dữ liệu trong file. Tại file excel của bạn, bạn cũng có thể kiểm tra xem dòng cuối cùng có chứa dữ liệu bằng cách nhấn <mark style="color:blue;">**Ctrl + End**</mark> .Ví dụ ta có bảng dữ liệu sau:

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

&#x20;             Với bảng dữ liệu này thì ta sẽ lấy được số của hàng chứa dữ liệu cuối cùng trong file của bạn. Ở đây ta có 10 hàng, node sẽ lưu giá trị 10 sẽ được lưu vào biến mà bạn chọn. Trường này không phụ thuộc vào range mà bạn nhập, có nghĩa là khi bạn nhập range là A1:B3 thì trường này vẫn sẽ lấy số hàng cuối cùng chứa dữ liệu trong bảng đó là 10.

* Storage: Bao gồm 2 trường là _Column name và Save to._ Với trường Column ta sẽ phải nhập đúng tên của cột dữ liệu. Còn trường Save to ta sẽ lưu giá trị đọc được từ Column name vào một biến.
* Preview: Hiển thị dữ liệu mà node đã đọc được.



### Google sheet&#x20;

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

###

* Google Spreadsheet ID: Nhập ID của Google sheet, bạn có thể lấy ID tại đây:&#x20;

<figure><img src="../../.gitbook/assets/image (5) (1).png" alt=""><figcaption></figcaption></figure>

###

* Credential file: chọn file Json đã tải về

Hướng dẫn lấy file credential:

1\.      Truy cập link [https://console.cloud.google.com/](https://console.cloud.google.com/)  và đăng nhập

2\.      Sau khi đăng nhập thành công, ta tạo 1 project mới:

\-        Chọn Select a project

<figure><img src="../../.gitbook/assets/image (6) (1).png" alt=""><figcaption></figcaption></figure>

&#x20;

\-        Chọn new project

<figure><img src="../../.gitbook/assets/image (7) (1).png" alt=""><figcaption></figcaption></figure>

\-        Nhập tên project và chọn Create

<figure><img src="../../.gitbook/assets/image (8) (1).png" alt=""><figcaption></figcaption></figure>

3\.      Enable Google sheet API

\-        Tại thanh tìm kiếm nhập Google sheets API. Kết quả tìm kiếm hiện ra, sau đó tại Marketplace chọn Google sheet API

<figure><img src="../../.gitbook/assets/image (9) (1).png" alt=""><figcaption></figcaption></figure>

\-        Thực hiện enable Google sheets API

<figure><img src="../../.gitbook/assets/image (10) (1).png" alt=""><figcaption></figcaption></figure>

&#x20;

4\.      Tạo Credentials

\-        Sau khi enable Google sheets API thành công, tiếp tục chọn Credentials

<figure><img src="../../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>

&#x20;

\-        Chọn Create Credentials, sau đó chọn Service account

<figure><img src="../../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

\-        Nhập Service account name sau đó chọn Done

<figure><img src="../../.gitbook/assets/image (13).png" alt=""><figcaption></figcaption></figure>

\-        Account vừa tạo sẽ hiển thị ở đây:

<figure><img src="../../.gitbook/assets/image (14).png" alt=""><figcaption></figcaption></figure>

\-        Click vào account đó và chọn tab Keys:

<figure><img src="../../.gitbook/assets/image (15).png" alt=""><figcaption></figcaption></figure>

&#x20;

\-        Chọn Add key -> chọn Create new key:

<figure><img src="../../.gitbook/assets/image (16).png" alt=""><figcaption></figcaption></figure>

&#x20;

\-        Chọn JSON -> Chọn create

<figure><img src="../../.gitbook/assets/image (17).png" alt=""><figcaption></figcaption></figure>

&#x20;

Sau khi tạo xong sẽ tự động tải file JSON về, và các bạn thêm file đó vào trường Credencial trong node Spreadsheet V2

<figure><img src="../../.gitbook/assets/image (18).png" alt=""><figcaption></figcaption></figure>

5\.      Shared sheet với account tạo ở bước trên

\-        Copy email tạo ở bước trên:

<figure><img src="../../.gitbook/assets/image (19).png" alt=""><figcaption></figcaption></figure>

&#x20;

\-        Shared trang sheet với account ở trên:

<figure><img src="../../.gitbook/assets/image (20).png" alt=""><figcaption></figcaption></figure>

&#x20;

Như vậy ta đã thực hiện Setup Google sheet để phục vụ việc đọc file trên google sheet thành công. Các trường bên dưới vẫn tương tự như Local file.

### Hướng dẫn chi tiết&#x20;

**Trường hợp chọn checkbox First row as title (Column name):**

Ta có bảng dữ liệu như sau:

<figure><img src="../../.gitbook/assets/image (28).png" alt=""><figcaption></figcaption></figure>

Ở node Spreadsheet ta nhập như sau:

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Ở trường hợp này khi chọn checkbox First row as title (Column name), thì ta sẽ lấy hàng đầu tiên của Range mà bạn nhập là tiêu đề của cột. Và các trường Column to compare, Column name ta phải nhập đúng tiêu đề của cột, ví dụ trong trường hợp này tên cột sẽ là email và password. Khi nhập vào các trường trong node như hình trên thì ta lấy được dữ liệu như hiển thị trong preview. Nếu khi ta không chọn checkbox Read row with stop condition thì mặc định sẽ lấy hàng đầu tiên của file ngoại trừ hàng tiêu đề.

**Trường hợp không chọn checkbox First row as title (Column name):**

<figure><img src="../../.gitbook/assets/image (30).png" alt=""><figcaption></figcaption></figure>

Ở trường hợp này khi chọn checkbox First row as title (Column name), thì sẽ không lấy hàng đầu tiên làm tiêu đề của cột. Và các trường Column to compare, Column name ta phải nhập đúng tên cột của bảng, ví dụ trong trường hợp này tên cột sẽ là A, B, C,... .&#x20;

**Ví dụ về đọc lần lượt từng hàng của file excel khớp với từng profile đang chạy:**

<figure><img src="../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Để chạy từng profile khớp với từng hàng dữ liệu của file excel, ta phải nhập trường _Column to compare_ và _Value to compare._ Với trường Column ta sẽ nhập tiêu đề của cột chứa uuid của từng profile với trường hợp này tiêu đề sẽ là uuid, trường Value to compare ta sẽ chọn biến ${PROFILE\_ID}. Nhập như trên thì khi chạy profile ta có thể so sánh được profile đang chạy có profile\_id trùng với hàng dữ liệu của cột uuid file excel và đọc đúng dữ liệu của hàng với profile tương ứng. &#x20;

Trường Column name ta chỉ cần nhập đúng title của cột mà ta muốn đọc từ file excel và lưu vào biến.



File excel dưới đây bạn có thể thay thế bằng uuid của các profile mà bạn sẽ chạy.

{% file src="../../.gitbook/assets/example 2.xlsx" %}

{% file src="../../.gitbook/assets/SPREADSHEET V2.txt" %}

**Ví dụ về đọc random từng hàng của file excel cho từng profile:**&#x20;

Với trường hợp bạn muốn đọc các hàng của file excel vào từng profile mà không theo thứ tự nào. Khi đó bạn có thể sử dụng node Random ở trước node Spreadsheet V2 để random ra chỉ số của cột.&#x20;

<figure><img src="../../.gitbook/assets/image (1) (2).png" alt=""><figcaption></figcaption></figure>

Trong trường hợp này ta sẽ random từ 1 đến 10. Sau đó tại trường Range của node Spreadsheet ta sẽ nhập như sau  A${index}:B10, trong trường hợp random này thì ta không nên chọn checkbox Read row with stop condition.&#x20;

<figure><img src="../../.gitbook/assets/image (51).png" alt=""><figcaption></figcaption></figure>

Khi đó khi chạy với nhiều profile thì dữ liệu trong file excel sẽ được lấy một cách ngẫu nhiêu không theo một thứ tự nào cả.

Dưới đây là một script đọc random các hàng với mỗi profile mà không theo thứ tự:

{% file src="../../.gitbook/assets/example 2 (1).xlsx" %}

{% file src="../../.gitbook/assets/Spreadsheet V2 random.txt" %}

**Ví dụ về đọc toàn bộ dữ liệu của một cột và ghi vào 1 biến**

Ví dụ ta có bảng dữ liệu sau:

<figure><img src="../../.gitbook/assets/image (2) (1).png" alt=""><figcaption></figcaption></figure>

Khi muốn đọc tất cả dữ liệu của cột A (email) vào 1 biến ta có script như sau:

<figure><img src="../../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

Tại node Variables ta tạo 1 biến là biến index có giá trị là 2 (do bảng excel trên dữ liệu bắt đầu từ hàng thứ 2, còn nếu bạn nào dữ liệu bắt đầu từ hàng thứ nhất thì các bạn nhập là 1)

<figure><img src="../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

Tại node Spreadsheet v2 các bạn nhập như sau:

<figure><img src="../../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

Tại node Set variable thứ nhất, các bạn cần nhập như sau:

<figure><img src="../../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

Qua mỗi vòng lặp thì giá trị của index sẽ tăng lên 1, cứ mỗi 1 vòng lặp thì sẽ đọc được giá trị của 1 dòng trong excel.



Tại node set variable thứ 2, các bạn cần nhập như sau:

<figure><img src="../../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

Node set variable thứ 2 được dùng để nối các giá trị lại với nhau. Tại trường Variable name, bạn chọn một biến mới để khi thực hiện nối dữ liệu thì dữ liệu được nối đó sẽ lưu vào biến (ở đây là biến b). Tại trường Variable or value các bạn nhập như trên hình, dấu | dùng để phân cách các giá trị, các bạn cũng có thể sử dụng kí tự khác để phân cách; và biến ${email} ở đây sẽ lấy các giá trị được lấy ra từ node speadsheet v2.

