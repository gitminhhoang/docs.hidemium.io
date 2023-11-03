# WriteSheet

### Giải thích các trường trong node

Khi bạn muốn ghi dữ liệu vào trong file excel thì có thể sử dụng node WriteSheet

<figure><img src="../../.gitbook/assets/image (44).png" alt=""><figcaption></figcaption></figure>

* Path to the file: Nhập đường dẫn hoặc chọn biến chứa đường dẫn của file excel của bạn.
* Sheet name: Nhập sheet name của file excel. Nếu bạn bỏ trống trường này, node sẽ tự động lấy sheet đầu tiên để ghi dữ liệu.
* Checkbox Append last row: Khi chọn checkbox này, node sẽ tự động ghi vào dòng tiếp theo của hàng cuối dữ liệu. Ví dụ dữ liệu trong file excel của bạn đến dòng 20 thì khi chọn checkbox này node sẽ tự ghi vào dòng tiếp theo là dòng thứ 21.&#x20;
* Cell location: Nhập vị trí mà bạn muốn ghi dữ liệu. Khi bạn không chọn checkbox Append last row thì bạn phải nhập ô cần ghi dữ liệu ví dụ A1, B1, A2,..... và nếu các ô đó đang có dữ liệu thì node sẽ ghi đè dữ liệu. Còn khi bạn chọn checkbox thì bạn chỉ cần nhập tên cột là A, B, C… thì node sẽ tự hiểu vào ghi vào dòng tiếp theo của hàng cuối  cùng chứa dữ liệu.
* Variable: Nhập giá trị mà bạn muốn ghi vào ô.

### Hướng dẫn chi tiết

Giả sử ta có bảng dữ liệu sau:

<figure><img src="../../.gitbook/assets/image (45).png" alt=""><figcaption></figcaption></figure>

* Nếu bạn muốn tự động ghi nối tiếp vào hàng tiếp theo của dòng cuối chứa dữ liệu, thì ta điền như sau:&#x20;

<figure><img src="../../.gitbook/assets/image (46).png" alt=""><figcaption></figcaption></figure>

Khi ta nhập thế này thì node sẽ tự ghi dữ liệu vào dòng số 7

* Hoặc nếu bạn không muốn ghi nối tiếp mà bạn muốn chỉ định ô để ghi dữ liệu bạn có thể nhập như sau:

<figure><img src="../../.gitbook/assets/image (47).png" alt=""><figcaption></figcaption></figure>

Như vậy bạn có thể ghi dữ liệu vào vào các ô mà mình mong muốn. Hoặc bạn có thể nhập ô đã có dữ liệu, node sẽ ghi đè dữ liệu vào các ô mà bạn nhập.

Trường hợp bạn muốn ghi dữ liệu vào một file excel ngay sau khi đọc xong, và bạn muốn ghi đúng vào từng hàng tương ứng bạn có thể sử dụng trường Row data number và Total row datas của node Spreadsheet V2.

Giả sử ta có bảng dữ liệu sau:&#x20;

<figure><img src="../../.gitbook/assets/image (48).png" alt=""><figcaption></figcaption></figure>

Và bạn muốn đọc từng hàng của file khớp với từng profile tương ứng theo uuid, thì node Spreadsheet V2 ta nhập như sau:&#x20;

<figure><img src="../../.gitbook/assets/image (49).png" alt=""><figcaption></figcaption></figure>

Bạn muốn khi đọc thành công từng hàng thì sẽ ghi lại để biết profile đó có đọc thành công hay không thì bạn sẽ sử dụng node writeSheet để ghi lại:

<figure><img src="../../.gitbook/assets/image (50).png" alt=""><figcaption></figcaption></figure>

Như vậy khi đọc thành công 1 hàng thì tại hàng tương ứng ta sẽ ghi chữ "Thành công" để đánh dấu.
