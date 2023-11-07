# Spreadsheet V2

Node Spreadsheet là Version 2 của node Spreadsheet. Với V2 này, các bạn có thể đọc file excel và file google sheet một cách dễ dàng hơn so với node Spreadsheet.

<figure><img src="../../.gitbook/assets/image (3) (1).png" alt=""><figcaption></figcaption></figure>

### Local File

* Path to file: Chọn file mà bạn muốn đọc.
* Range: Một nhóm các ô trong file excel. Ví dụ bạn muốn đọc dữ liệu từ ô A1 đếm ô E5, ta sẽ nhập trường Range là A1:E5. Bạn cũng có thể bỏ trống trường này. Range bắt buộc phải nhập là chữ hoa.
* Sheet name: Tên của excel sheet. Nếu bỏ trống ô này, sẽ mặc định lấy sheet name đầu tiên.
* First row as title (Column name): Khi tick vào checkbox này, ta sẽ coi hàng đầu tiên của excel là tên (tiêu đề) của các cột dữ liệu, khi không chọn checkbox thì các hàng đều ngang hàng nhau.
* Read row with stop condition: Khi bạn không chọn checkbox này thì node sẽ mặc định lấy dữ liệu của hàng đầu tiên. Khi bạn chọn checkbox này, bạn phải nhập 2 trường _Column to compare và Value to compare_**.** Column to compare: Trường này bạn sẽ nhập cột để so sánh. Value to compare: Trường này bạn sẽ nhập giá trị để so sánh. Khi không chọn checkbox này, chạy với nhiều profile thì tất cả các profile đều lấy dữ liệu cảu hàng đầu tiên.&#x20;
* Row data number: Chọn một biến. Trường này sẽ trả về số của hàng mà node đang đọc đến và lưu vào biến bạn chọn. Ví dụ ta có bảng dữ liệu sau:

<figure><img src="../../.gitbook/assets/image (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

&#x20;        Với bảng dữ liệu này: Dữ liệu đang được đọc ở hàng số 4, thì node sẽ lưu giá trị 4 vào biến mà bạn chọn.

* Total row datas: Hiển thị tổng số hàng dữ liệu trong bảng. Ví dụ ta có bảng dữ liệu sau:

<figure><img src="../../.gitbook/assets/image (2) (1) (1).png" alt=""><figcaption></figcaption></figure>

&#x20;             Với bảng dữ liệu này thì ta sẽ lấy tổng số hàng dữ liệu trong file của bạn. Ở đây ta có 10 hàng, node sẽ lưu giá trị 10 sẽ được lưu vào biến mà bạn chọn. Trường này không phụ thuộc vào range mà bạn nhập, có nghĩa là khi bạn nhập range là A1:B3 thì trường này vẫn sẽ lấy số hàng cuối cùng chứa dữ liệu trong bảng đó là 10.

* Storage: Bao gồm 2 trường là _Column name và Save to._ Với trường Column ta sẽ phải nhập đúng tên của cột dữ liệu. Còn trường Save to ta sẽ lưu giá trị đọc được từ Column name vào một biến.
* Preview: Hiển thị dữ liệu mà node đã đọc được.

### Hướng dẫn chi tiết

**Trường hợp chọn checkbox First row as title (Column name):**

Ta có bảng dữ liệu như sau:

<figure><img src="../../.gitbook/assets/image (28).png" alt=""><figcaption></figcaption></figure>

Ở node Spreadsheet ta nhập như sau:

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Ở trường hợp này khi chọn checkbox First row as title (Column name), thì ta sẽ lấy hàng đầu tiên của Range mà bạn nhập là tiêu đề của cột. Và các trường Column to compare, Column name ta phải nhập đúng tiêu đề của cột, ví dụ trong trường hợp này tên cột sẽ là email và password. Khi nhập vào các trường trong node như hình trên thì ta lấy được dữ liệu như hiển thị trong preview. Nếu khi ta không chọn checkbox Read row with stop condition thì mặc định sẽ lấy hàng đầu tiên của file ngoại trừ hàng tiêu đề.

**Trường hợp không chọn checkbox First row as title (Column name):**

<figure><img src="../../.gitbook/assets/image (30).png" alt=""><figcaption></figcaption></figure>

Ở trường hợp này khi chọn checkbox First row as title (Column name), thì sẽ không lấy hàng đầu tiên làm tiêu đề của cột. Và các trường Column to compare, Column name ta phải nhập đúng tên cột của bảng, ví dụ trong trường hợp này tên cột sẽ là A, B, C,... .&#x20;

**Ví dụ về đọc lần lượt từng hàng của file excel khớp với từng profile đang chạy:**

<figure><img src="../../.gitbook/assets/image (3) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (3) (1) (1).png" alt=""><figcaption></figcaption></figure>

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
