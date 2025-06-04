# Handle Dialog

#### 1. Khái niệm cơ bản về DIALOG

**Dialog** (hộp thoại) là một giao diện người dùng mà ứng dụng sử dụng để tương tác với người dùng. Nó thường xuất hiện dưới dạng cửa sổ nhỏ và có thể chứa các thông báo, câu hỏi, hoặc yêu cầu thông tin từ người dùng.

Có một số loại Dialog phổ biến như sau:

&#x20;        **– Alert Dialog**

*
  * Hiển thị thông báo cho người dùng và thường có nút “OK” để đóng hộp thoại.
  * Ví dụ: Thông báo lỗi, cảnh báo, hoặc thông điệp thành công.

![](http://education.hidemium.io/wp-content/uploads/2024/09/Screenshot_1.png)

&#x20;

&#x20;      **– Confirm Dialog**

*
  * Cung cấp một câu hỏi với tùy chọn “OK” và “Cancel”.
  * Thường được sử dụng để xác nhận hành động của người dùng, như xóa tệp hoặc thoát ứng dụng.

![](http://education.hidemium.io/wp-content/uploads/2024/09/Screenshot_2.png)

&#x20;

&#x20;    **– Prompt Dialog**

*
  * Hiển thị một trường nhập liệu cùng với các nút “OK” và “Cancel”.
  * Dùng để thu thập thông tin từ người dùng, chẳng hạn như tên hoặc địa chỉ email.

![](http://education.hidemium.io/wp-content/uploads/2024/09/Screenshot_3.png)

&#x20;

#### 2. Giải thích các trường trong node Handle dialog

Khi Dialog hiện lên thì ta thường không thể thao tác được gì với trang web nếu không đóng Dialog. Khi đó ta cần sử dụng node Handle dialog để đóng hộp thoại được mở lên đó.

![](http://education.hidemium.io/wp-content/uploads/2024/09/Screenshot_4.png)

&#x20;

Tại node Handle dialog ta có 3 action:

– No handle: Sẽ không làm gì cả và dialog vẫn sẽ hiển thị trên trang web.

*
  * Save message to: Lưu message vào biến và bạn chọn.
  * Save type to: Lưu lại type của Dialog như Alert, Confirm, Prompt vào biến.
  * Save default value to: Lưu giá trị mặc định trong dialog vào biến.

–  Accept: Thường trong dialog sẽ có 2 button “OK” và “Cancel”, khi bạn chon action accept thì giống như việc bạn click vào button “OK” của dialog.

*
  * Prompt input: Trong **Prompt Dialog** thường sẽ hiển thị thêm một ô input để nhập dữ liệu. Khi bạn nhập vào trường Prompt input, giá trị mà bạn nhập vào sẽ được nhập vào ô input của dialog.
  * Save message to: Lưu message vào biến và bạn chọn.
  * Save type to: Lưu lại type của Dialog như Alert, Confirm, Prompt vào biến.
  * Save default value to: Lưu giá trị mặc định trong dialog vào biến.

– Dismiss: Thường trong dialog sẽ có 2 button “OK” và “Cancel”, khi bạn chon action Dimiss thì giống như việc bạn click vào button “Cancel” của dialog.

*
  * Save message to: Lưu message vào biến và bạn chọn.
  * Save type to: Lưu lại type của Dialog như Alert, Confirm, Prompt vào biến.
  * Save default value to: Lưu giá trị mặc định trong dialog vào biến.

**Lưu ý: node Handle dialog phải được sử dụng  trước khi dialog xuất hiện. Có nghĩa là khi click vào 1 button nào đó thì sẽ xuất hiện dialog, thì node Handle dialog sẽ được dùng trước node click.** &#x20;

&#x20;

#### 3. Ví dụ thực tế

&#x20;    **a. Alert dialog**

Bạn có thể tham khảo ví dụ thực tế về Alert Dialog tại đây:   [https://www.w3schools.com/jsref/tryit.asp?filename=tryjsref\_alert](https://www.w3schools.com/jsref/tryit.asp?filename=tryjsref_alert)

![](http://education.hidemium.io/wp-content/uploads/2024/09/Screenshot_5.png)

&#x20;

Khi muốn đóng Dialog này thì tại node Handle dialog bạn sẽ dùng như sau:

![](http://education.hidemium.io/wp-content/uploads/2024/09/Screenshot_6.png)

&#x20;

Action thì bạn chọn là Accept tương ứng với OK. Trường **Save message to** sẽ lưu “Hello! I am an alert box!” vào biến **message**. Trường **Save type to** sẽ lưu type của dialog là **alert**  vào biến **type**

&#x20;

&#x20;    **b. Confirm dialog**

Bạn có thể tham khảo ví dụ thực tế về Alert Dialog tại đây: [https://www.w3schools.com/jsref/tryit.asp?filename=tryjsref\_confirm3](https://www.w3schools.com/jsref/tryit.asp?filename=tryjsref_confirm3)

![](http://education.hidemium.io/wp-content/uploads/2024/09/Screenshot_2.png)

&#x20;

Khi muốn đóng Dialog này thì tại node Handle dialog bạn sẽ dung như sau:

*
  * Khi bạn muốn chọn OK tại Dialog :

![](http://education.hidemium.io/wp-content/uploads/2024/09/Screenshot_7.png)

&#x20;

*
  * Khi bạn muốn chọn **Hủy** tại dialog:

![](http://education.hidemium.io/wp-content/uploads/2024/09/Screenshot_8.png)

&#x20;

Trường **Save message to** sẽ lưu “Press a button!Either OK or Cancel.” vào biến **message**. Trường **Save type to** sẽ lưu type của dialog là **confirm**  vào biến **type.**

&#x20;

&#x20;    **c. Prompt dialog**

Bạn có thể tham khảo ví dụ thực tế về Alert Dialog tại đây: [https://www.w3schools.com/jsref/tryit.asp?filename=tryjsref\_prompt](https://www.w3schools.com/jsref/tryit.asp?filename=tryjsref_prompt)

![](http://education.hidemium.io/wp-content/uploads/2024/09/Screenshot_3.png)

&#x20;

Khi muốn đóng Dialog này thì tại node Handle dialog bạn sẽ dung như sau:

*
  * Khi bạn muốn chọn OK tại Dialog :

![](http://education.hidemium.io/wp-content/uploads/2024/09/Screenshot_10.png)

Prompt dialog này có 1 ô input, tại trường **prompt input** của node, ta có thể nhập giá trị khác vào thay thế cho giá trị mặc định của prompt dialog. Như trong ví dụ này ta sẽ thay thế Harry Potter bằng Nana.

Trường **Save message to** sẽ lưu “Please enter your name” vào biến **message**. Trường **Save type to** sẽ lưu type của dialog là **prompt**  vào biến **type.** Trường Save default value to sẽ lưu giá trị mặc định ban đầu của ô input trong dialog là “Harry Potter” vào biến **default\_value**

&#x20;

*
  * Khi bạn muốn chọn **Hủy** tại dialog:

![](http://education.hidemium.io/wp-content/uploads/2024/09/Screenshot_11.png)

&#x20;

Trường **Save message to** sẽ lưu “Please enter your name” vào biến **message**. Trường **Save type to** sẽ lưu type của dialog là **prompt**  vào biến **type.** Trường Save default value to sẽ lưu giá trị mặc định ban đầu của ô input trong dialog là “Harry Potter” vào biến **default\_value**
