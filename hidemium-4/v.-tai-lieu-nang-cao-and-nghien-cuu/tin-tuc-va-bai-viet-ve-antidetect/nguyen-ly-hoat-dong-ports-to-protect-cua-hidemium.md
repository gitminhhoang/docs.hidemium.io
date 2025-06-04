# Nguyên lý hoạt động Ports to protect của hidemium?

Nhiều bạn khi trải nhiệm dùng [**Hidemium**](https://hidemium.io/) sẽ nhìn thấy chức năng **Ports to protect** trong màn **New Profiles**. Vậy các bạn đã hiểu thực sự về chức năng **Ports to protect** của chúng tôi hay chưa. Hãy theo dõi bài viết dưới đây của chúng tôi.

<figure><img src="../../../.gitbook/assets/image (23).png" alt=""><figcaption></figcaption></figure>





### Sơ lược về module Scan Port <a href="#s-lc-v-module-scan-port-1" id="s-lc-v-module-scan-port-1"></a>

**Scan Port** là một kỹ thuật thường được sử dụng bởi các chuyên gia tester và hacker để quét các máy chủ đang kết nối với internet và xác định các ứng dụng hoặc dịch vụ đang lắng nghe trên mạng, thường là để thực hiện các cuộc tấn công cụ thể. Thông thường, phần mềm bảo mật sẽ phát hiện quét cổng hoạt động và đánh dấu nó là mối nguy hiểm tiềm năng.

Hầu hết các router gia đình không có cổng mở nào, vì vậy việc quét địa chỉ IP của người dùng internet rất khó hoặc không trả về dữ liệu port nào cả. Tuy nhiên, nhiều người dùng chạy phần mềm trên máy tính của họ để lắng nghe trên các cổng vì nhiều lý do khác nhau – chơi game trực tuyến, chia sẻ phương tiện truyền thông và kết nối từ xa …

**Scan Port** có thể cung cấp thông tin về phần mềm bạn đang chạy trên trang web. Nhiều dịch vụ luôn default 1 vài port mặc định cho người dùng, vì vậy một danh sách các cổng mở sẽ xác định rõ dàng về các ứng dụng đang chạy. Ví dụ, **Steam** được biết đến chạy trên cổng **27036**, vì vậy một máy quét thấy cổng đó mở có thể tự tin rằng người dùng cũng đã mở Steam khi truy cập trang web hoặc tương tự một dịch vụ proxy nào đó bạn đang sử dụng (**922Proxy**, **PiaProxy**…) thường có những port gợi ý **30000** hoặc **40000**.

&#x20;

[![image](https://forum.hidemium.io/uploads/default/original/1X/0467905205204e2a5a7a797c703a31d9f37b624f.png)](https://forum.hidemium.io/uploads/default/original/1X/0467905205204e2a5a7a797c703a31d9f37b624f.png)

&#x20;

### Theo dõi Ebay Port Scan <a href="#theo-di-ebay-port-scan-2" id="theo-di-ebay-port-scan-2"></a>

Theo tôi được biết thì Threat Matrix cung cấp tính năng **Scan Port** này như một biện pháp kiểm tra phát hiện phần mềm độc hại cho khách hàng.

Tôi đưa ra ví dụ về ebay là một trang web sử dụng tính năng quét cổng. Tôi truy cập vào [**Hidemium**](https://hidemium.io/) vào tạo 1 profiles ngẫu nhiên. Tôi mở Devtool của Chrome và theo dõi dữ liệu của ebay được gửi đi và nhận lại. Ở các page đơn giản xem sản phẩm tôi không thấy dấu hiệu Scan Port nào. Nhưng khi tôi truy cập vào trang Create Account của Ebay:

<figure><img src="../../../.gitbook/assets/image (21).png" alt=""><figcaption></figcaption></figure>

&#x20;

Tôi nhìn thấy các request websocket 127.0.0.1 kèm theo port nó đã check.

wss://127.0.0.1:5900/\
wss://127.0.0.1:63333/\
wss://127.0.0.1:5901/\
wss://127.0.0.1:3389/\
wss://127.0.0.1:5903/\
wss://127.0.0.1:5902/\
wss://127.0.0.1:5950/\
wss://127.0.0.1:5931/\
wss://127.0.0.1:5944/\
wss://127.0.0.1:6040/\
wss://127.0.0.1:5939/\
wss://127.0.0.1:5938/\
wss://127.0.0.1:6039/\
wss://127.0.0.1:5279/\
wss://127.0.0.1:2112/\
wss://127.0.0.1:7070/

Ta có thể giải thích các port trên như sau:

* Cổng 5900 thường được sử dụng cho dịch vụ Điện toán mạng ảo (VNC), cho phép truy cập và điều khiển máy tính từ xa qua mạng. Nó thường được sử dụng để chia sẻ và khắc phục sự cố máy tính từ xa.
* Cổng 5901 thường được sử dụng để truy cập máy tính từ xa của VNC (Máy tính mạng ảo). Nó thường được sử dụng để quản trị từ xa và khắc phục sự cố của máy chủ và các thiết bị khác.
* Cổng 3389 thường được sử dụng cho các kết nối Giao thức máy tính từ xa (RDP) trên hệ thống Windows. Nó cho phép người dùng kết nối từ xa với một máy tính khác qua mạng.
* Cổng 5903 thường được sử dụng cho dịch vụ VNC (Máy tính mạng ảo). VNC cho phép truy cập và điều khiển từ xa một máy tính khác qua mạng.
* Cổng 5902 thường được sử dụng cho dịch vụ Máy tính mạng ảo (VNC). VNC là một hệ thống chia sẻ máy tính để bàn đồ họa cho phép người dùng điều khiển từ xa một máy tính khác.\
  …

Hầu hết các port được check được sẽ đưa ra kết luận rằng bạn có sử dụng phần mềm mà ebay ngăn chặn hay không hoặc có sử dụng VPS để remote nuôi đa số tài khoản hay không. Điều này sẽ kết luận rằng tài khoản của bạn thực sự là người dùng thật hay là người dùng giả mạo.

Nếu bạn là người dùng thường xuyên sử dụng VPS nuôi tài khoản, tôi khuyên bạn nên sử dụng tool Scan Port, hoặc truy cập browserscan để sử dụng chức năng check fingerprint và Scan Port để kiểm tra xem VPS của chúng ta đang leak những Port nào

<figure><img src="../../../.gitbook/assets/image (22).png" alt=""><figcaption></figcaption></figure>

&#x20;

Với [**Hidemium**](https://hidemium.io/) chúng tôi cung cấp cho người dùng giải pháp **Ports to protect** ngăn chặn các hệ thống có thể phát hiện ra máy tính bạn đang mở cổng đó. Để sử dụng bạn chỉ cần thêm Port đó vào ô dữ liệu và cách nhau bằng dấu phẩy.

<figure><img src="../../../.gitbook/assets/image (24).png" alt=""><figcaption></figcaption></figure>

&#x20;

Ngoài ra với dung lượng lưu trữ ổ C trên VPS thường rất ít hoặc không đủ dung lượng với 1 ổ đĩa thông thường, các hệ thống detect họ có thể phát hiện ra rằng máy tính của bạn đang là một máy ảo.

<figure><img src="../../../.gitbook/assets/image (25).png" alt=""><figcaption></figcaption></figure>

&#x20;

Với [**Hidemium**](https://hidemium.io/) chúng tôi đã giả lập dung lượng ổ cứng cho trình duyệt. Điều này sẽ an toàn cho các bạn đang nuôi trên hệ thống máy ảo VPS.

Để mua VPS nuôi account mời bạn mua VPS siêu rẻ tại: [VPSMMO](https://vpsmmo.vn/aff.php?aff=144)\
Để miễn phí trải nhiệm Hidemium mời bạn tải tại: [Download](https://hidemium.io/download)\
Mua gói Hidemium để trải nhiệm automation tại: [Pricing](https://hidemium.io/pricing)
