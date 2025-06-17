# Cách quản lý data ( dữ liệu ) theo file excel khi chạy automation.

**I. Khi chạy auto bạn muốn tất cả dữ liệu đọc sẽ lấy dữ liệu theo điều kiện là PROFILE\_NAME hoặc PROFILE\_UUID**

Bạn đã có sẵn file excel với cột A là Profile\_name hoặc Profile\_uuid để đánh dấu những data thuộc profile đó. Và bạn muốn khi chạy script sẽ ghi lại Email và Pass đúng vào hàng của profile mà nó đang chạy

![](http://education.hidemium.io/wp-content/uploads/2024/05/b1.jpg)

\*\* Sử dụng node SPREDSHEET V2

![](https://i.imgur.com/SpvDJ4x.png)

– Tích vào checkbox Read row with stop condition : tức là đọc hàng ngang với điều kiện dừng

Value to compare : Giá trị đẻ so sánh Column to compare : Cột để so sánh

Thì 1 profile có 2 giá trị độc nhất để xác định đó là một profile đó là PROFILE\_NAME và PROFILE\_UUID. Nếu bạn chọn PROFILE\_NAME tức là bạn muốn so sánh với tên của profile để script xác định xem lấy dòng nào trong excel dựa trên việc tìm thấy tên profile ở hàng đó Nếu bạn dùng PROFILE\_UUID tức là bạn muốn so sánh xem có UUID của profile đang chạy xuất hiện ở dòng nào trong excel thì script sẽ lấy data hàng đó. Ví dụ theo ảnh trên, tôi đã tạo cột A là Profile\_name. Vậy thì Column to compare tôi đã nhập tên cột là Profile\_name vào, và ở Value to compare chọn PROFILE\_NAME. Nếu tôi đang chạy profile có tên là Etsy 19 và script thấy tên profile xuất hiện ở dòng A2 thì script sẽ xác định làm việc với tất cả data ở hàng 2.

![](http://education.hidemium.io/wp-content/uploads/2024/05/b3.jpg)

– Tích vào checkbox ” First row as title (Column name)” thì ta sẽ lấy hàng đầu tiên của Range mà bạn nhập là tiêu đề của cột. Và các trường Column to compare, Column name ta phải nhập đúng tiêu đề của cột, ví dụ trong trường hợp này tên cột C sẽ là Email và tên cột D là Pass. Phần column name và save to tương đương với việc nhập tên cột trong excel và muốn lưu data trong cột đó có tên biến là gì để sử dụng trong script. Như ảnh dưới đây thì script sẽ lấy Email là Hidemium123@gmail.com và Pass là Hidemium123

![](https://i.imgur.com/EXji5Rs.png)

Như vậy là xong cách lấy data đúng với từng profile một

\
**II. khi chạy auto bạn muốn tất cả dữ liệu ghi sẽ ghi theo điều kiện là PROFILE\_NAME hoặc PROFILE\_UUID**

Nếu trong quá trình chạy script bạn muốn ghi vào file excel nhưng phải đúng từng hàng của profile, thì làm theo hướng dẫn dưới đây.\
Tạo node Spreadsheet giống dưới đây. Cũng xác định Column to compare và Value to compare giống cách đọc excel bên trên.

<figure><img src="../../../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>

Sau đó chúng ta để ý tới ô Row match condition : tức là hàng của điều kiện so sánh. Ví dụ script đọc được profile Etsy 19 ở dòng A2 thì script sẽ hiểu hàng 2 là của profile Etsy 19. Bạn đặt tên cho giá trị này là match hoặc bất kì biến nào cũng được. Ví dụ ảnh trên tôi đặt tên biến là match, thì lúc này match có giá trị là 2.

Ví dụ script là login gmail và sau khi login xong bạn muốn đánh dấu vào ô bên cạnh là đã login tài khoản này thành công, bạn sẽ nhập Cell location như sau

<figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

D là cột muốn nhập dữ liệu vào, và tôi chọn biến ${match} ở bên cạnh. Lúc này Cell location nghĩa là D2. Như giải thích ở bên trên, biến Match này là script lấy ra được số hàng của profile, Ví dụ tên profile ở hàng 3, thì D${match} lúc này là D3, script sẽ viết chữ “đã login thành công” vào ô D3\
Tương tự nếu muốn ghi thêm bất kì nội dung gì thì chỉ cần làm tương tự, xác định cột muốn ghi vào + biến đặt ở “Row match conditions” trong node SPREADSHEET\
Đây chính là cách giúp các bạn ghi dữ liệu vào excel đúng theo từng profile một



**III. Đọc nhiều hàng của 1 profile.**

Trong trường hợp 1 profile có nhiều hàng như ảnh dưới đây. Ví dụ có 2 hàng profile Etsy 19

<figure><img src="../../../.gitbook/assets/image (2) (1) (1).png" alt=""><figcaption></figcaption></figure>

Thì theo nguyên tắc nếu chạy với profile Etsy 19 này script sẽ lấy data dòng 2 trước. Cách để lấy data dòng thứ 3 kia là:

1. Khi chạy xong node SPREADSHEET để lấy data dòng 2 thành công, bạn dùng node WRITESHEET như sau:

<figure><img src="../../../.gitbook/assets/image (3) (1) (1).png" alt=""><figcaption></figcaption></figure>

Giải thích A${match} ở đây tức là trong file excel cột A là cột mình ghi tên profile, nếu bạn ghi tên profile ở cột khác thì điền cột đó vào nhé, match thì như đã giải thích ở II thì n là để xác định số hàng của profile đó, vậy A${match} ở đây là A2.

Ở bên Variable mình ghi ${PROFILE\_NAME}123 tức là để thay đổi tên profile ban đầu đi. Mục đích làm thay tên để lần 2 n sẽ bỏ qua dòng 2 vì tên khác với Profile name đang chạy và dùng data dòng 3 vì lúc này dòng 3 mới là dòng trùng điều kiện so sánh.

<figure><img src="../../../.gitbook/assets/image (4) (1) (1).png" alt=""><figcaption></figcaption></figure>

Cứ lần lượt làm như trên, dùng xong dòng profile nào thì thay tên đi tí để cho nó khác với điều kiện ban đầu.

**IV. Cách viết vào nhiều dòng hoặc viết nhiều data vào 1 ô**

1\. Nếu bạn muốn viết vào nhiều dòng thì làm tương tự như cách đọc nhiều dòng\
2\. Nếu bạn muốn viết nhiều lần vào 1 ô

Ví dụ bạn đang lấy dữ liệu từ một trang bán sản phẩm và mỗi lần lấy là được một màu. Nhưng rule của excel lần thứ 2 viết vào ô đã là sẽ bị viết đè lên các giá trị có trước đó, tức nó chỉ nhận giá trị ghi vào gần nhất.\
Vì vậy, chỗ này ta sẽ giải quyết bằng cách sử dụng thêm node SET VARIABLE nhé. Bước đầu, xác định biến chính lấy dữ liệu, ví dụ đặt 1 biến tên Color và n sẽ là biến lấy các giá trị màu sắc này.

Sau đó, đặt 1 biến tên All\_color để trống giá trị với mục đích sẽ chứa tất cả các giá trị của biến Color, dùng node SET VARIABLE như sau :

<figure><img src="../../../.gitbook/assets/image (5) (1) (1).png" alt=""><figcaption></figcaption></figure>

Tạo 1 biến All\_color ở đây

<figure><img src="../../../.gitbook/assets/image (6) (1) (1).png" alt=""><figcaption></figcaption></figure>

Node get text này đại diện cho node sẽ lấy được dữ liệu chính

<figure><img src="../../../.gitbook/assets/image (7) (1).png" alt=""><figcaption></figcaption></figure>

Concatenate tức là nối. Nó có nghĩa là nối biến. Thì ở đây ta sẽ nối lần lượt các giá trị của biến color kia vào. Ví dụ vòng 1 được màu xanh thì All\_color sẽ có giá trị là | màu xanh. Vòng 2 biến color lấy được thêm màu vàng thì biến All\_color sẽ có giá trị là | màu xanh | màu vàng,…. và cứ tương tự như vậy cho đến hết

<figure><img src="../../../.gitbook/assets/image (8) (1).png" alt=""><figcaption></figcaption></figure>

Và đương nhiên rồi, khi ghi vào file excel ta sẽ ghi giá trị của biến All\_color nhé

<figure><img src="../../../.gitbook/assets/image (9) (1).png" alt=""><figcaption></figcaption></figure>

#### **IV. CẬP  NHẬT MỚI TỪ NODE WRITESHEET**&#x20;

<figure><img src="../../../.gitbook/assets/image (10) (1).png" alt=""><figcaption></figcaption></figure>

**Nếu bạn không tích vào ô ” first row as title” ( tức : hàng đầu tiên là tiêu đề ) thì ở column name bạn nhập tên cột như A B C D, nếu muốn dùng thêm biến thì A${biến} B${biến} C${biến},……**

<figure><img src="../../../.gitbook/assets/image (11) (1).png" alt=""><figcaption></figcaption></figure>

Nếu bạn tích vào ô **” first row as title”** thì ở column name sẽ nhập tên của cột như : UUID, NAME, USERNAME,.. tương ứng với tên cột trong file excel của bạn, và **Row number** thì nhập số ô bạn cần ghi, có thể trực tiếp ghi 1 2 3 hoặc nhập biến vào đây, nếu như bạn muốn ghi vào hàng của profiles, thì bạn sẽ nhập biến mà bạn tạo ở phần **” row match condition”** ở node spreadsheet V2 nhé, nó khác ở bản writesheet cũ là tên cột và số hàng tách riêng ra như này. bản chất vẫn giống nhau.

<figure><img src="../../../.gitbook/assets/image (12).png" alt=""><figcaption><p>Biến ở mục này sẽ cho ra kết quả là số thứ tự mà ID hoặc Profile Name xuất hiện</p></figcaption></figure>



<figure><img src="../../../.gitbook/assets/image (13).png" alt=""><figcaption><p>Nhập biến đó vào đây sẽ cho ra kết quả ghi vào cột có tên Result và số hàng là trùng với ID hoặc Profile Name của bạn.</p></figcaption></figure>



