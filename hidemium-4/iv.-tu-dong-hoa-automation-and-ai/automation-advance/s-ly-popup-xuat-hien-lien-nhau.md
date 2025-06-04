# SỬ LÝ POPUP XUẤT HIỆN LIỀN NHAU

Use case vài Pop up xuất hiện liền nhau này xảy ra cực nhiều trong khi thực hiện việc connect các ví tiền điện tử khi thực hiện nhiệm vụ airdrop. Vậy các bạn đã biết cách xử lý và sắp xếp các node auto sao cho hợp lý chưa ? Cùng Hidemium tìm ra cách làm tối ưu và chính xác nhất nhé.\
Đầu tiên chắc chắn là phải cài extension ví trước rồi nhé. Bỏ qua các bước râu ria thì đến đoạn click vào connect wallet này. Chỗ này mình cứ nghĩ là dùng node CLICK đúng không ? Nhưng không nhé, Nếu click vào đây mà xuất hiện popup ví Metamask thì ta dùng luôn node SWITCH POPUP EXTENSION nhé, node này chính là sự kết hợp của ” click vào element + switch sang page popup ” cho nên chỉ cần nhập element mà click vào sẽ xuất hiện popup vào node SWITCH POPUP EXTENSION là được.

![](https://i.imgur.com/xWzCK2S.png)

&#x20;

<figure><img src="https://i.imgur.com/PLvys5S.png" alt="" height="485" width="896"><figcaption><p>Nhập vào xpath/css của button hay phần nào mà click vào sẽ show ra popup</p></figcaption></figure>

&#x20;

Sau khi switch thì xuất hiện popup nên các thao tác khác lại dùng như bình thường. Và dặc biệt khi popup 1 tắt đi thì các bạn phải switch về main page để thao tác tiếp nhé. Nếu sau đó tiếp tục là 1 lần click vào để hiện ra popup thì bạn lại nối thêm node switch popup extension vào switch như hướng dẫn bên trên. Nhưng cần switch về main page đã nhé.

![](https://i.imgur.com/84h0243.png)

&#x20;

Nếu trong trường hợp popup 1 không tắt đi, mà khi thao tác trên popup 1 xuất hiện luôn popup 2 thì bạn không cần switch về main page nữa, lúc này bạn switch luôn sang popup 2 bằng node Switch popup extension nhé. .

Còn trong trường hợp popup extension hiện ra khi không click vào đâu cả, bất ngờ hiện ra thì bạn sử dụng node SWITCH EXTENSION POPUP mà không cần nhập element nhé, chỉ cần điền timeout là được.
