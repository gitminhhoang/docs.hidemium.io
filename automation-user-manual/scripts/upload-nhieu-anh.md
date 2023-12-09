# Upload nhiều ảnh

Nếu bạn muốn upload nhiều ảnh trong một Folder thì đây là một script để bạn có thể tham khảo.

Đầu tiên ta có một folder chứa các ảnh mà bạn muốn upload:

<figure><img src="../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

Tại đường dẫn thư của folder bạn nhập **cmd** và nhấn **Enter**

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Bảng điều khiển cmd hiện hiện lên, và gõ lệnh:   **dir /B /S>FolderList.txt** và lệnh                          **echo x>>FolderList.txt**   và nhấn Enter

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Sau đó một file txt có tên là FolderList chứa đường dẫn của tất cả các ảnh trong folder được tạo:

<figure><img src="../../.gitbook/assets/image (3) (1).png" alt=""><figcaption></figcaption></figure>

Mở file txt đó lên và xóa dòng đầu tiên của file và lưu file lại, chính là dòng chưa đường dẫn của Folder, dòng chứa chữ x bạn phải giữ lại, khi đọc file đến dòng đó có nghĩa là đã upload hết ảnh:

<figure><img src="../../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

Ta có Script như sau: Ta sẽ thực hiện upload ảnh lên lightShot:&#x20;

<figure><img src="../../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

Trong script này:

* Node read file bạn hãy chọn file FolderList.txt, và chọn type là Line by line để đọc từng dùng từ trên xuống, khi đọc xong thì sẽ lưu giá trị vào biến file\_anh

<figure><img src="../../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

* Node if ta sẽ so sánh nếu giá trị của biến file\_anh bằng x thì có nghĩa là đã đọc xong file, đã upload hết ảnh. Nếu file\_anh mà không bằng x có nghĩa là chưa upload hết ảnh trong folder, thì ta sẽ thực hiện upload ảnh tiếp.

<figure><img src="../../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

* Node File choose event ta sẽ chọn biến file\_anh tại trường path to the file

<figure><img src="../../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>

* Node click ta sẽ thực hiện click để uplaod ảnh

Dưới đây là script mẫu:

{% file src="../../.gitbook/assets/Upload nhieu anh.rar" %}
