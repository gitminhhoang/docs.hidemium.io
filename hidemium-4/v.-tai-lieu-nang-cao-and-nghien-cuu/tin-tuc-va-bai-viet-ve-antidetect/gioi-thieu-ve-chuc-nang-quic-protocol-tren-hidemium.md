# Giới thiệu về chức năng QUIC Protocol trên Hidemium

Xin chào toàn thể anh em sử dụng Hidemium. Chắc hẳn anh em sử dụng hidemium ít để ý đến chức năng **Experimental QUIC protocol** ở tab **Other** trong chức năng **Create Profile**. Nay mình sẽ giải thích rõ dàng và trường hợp nào thì nên sử dụng chức năng này.

<figure><img src="../../../.gitbook/assets/image (6) (1).png" alt=""><figcaption></figcaption></figure>

&#x20;

Trước tiên đi vào sử dụng tôi xin giải thích sơ lược về các giao thức cơ bản từ trước tới giờ các hệ thống và trình duyệt xử lý:\
Link tham khảo: [Hypertext Transfer Protocol – Wikipedia tiếng Việt 1](https://vi.wikipedia.org/wiki/Hypertext_Transfer_Protocol)\
![image](https://forum.hidemium.io/uploads/default/original/1X/745aa83b071775668204085cce3b88da1cc302cd.png)

Hiện tại chủ yếu các dịch vụ sẽ sử dụng HTTP1.1, HTTP/2 và HTTP/3 và các giao thức nó hỗ trợ.\


<figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>



Trước tiên ta đi tìm hiểu Proxy UDP và TCP

### Hiểu UDP và TCP <a href="#hiu-udp-v-tcp-1" id="hiu-udp-v-tcp-1"></a>

UDP là một trong những giao thức cốt lõi trong bộ giao thức Internet, cùng với TCP (Giao thức điều khiển truyền dẫn). Không giống như TCP, UDP là giao thức không kết nối, nghĩa là nó không thiết lập kết nối trực tiếp giữa người gửi và người nhận trước khi truyền dữ liệu. Điều này cho phép truyền dữ liệu nhanh hơn bằng cách loại bỏ nhu cầu bắt tay ban đầu, điều này có thể làm chậm quá trình giao tiếp.

Ở phiên bản HTTP1.1 và HTTP/2 dùng TCP để truyền tải, giao thức này sẽ đi qua **Proxy Server** nên khi ta dùng Proxy để fake IP điều này có thể qua mặt được hệ thống

<figure><img src="../../../.gitbook/assets/image (3) (1) (1).png" alt=""><figcaption></figcaption></figure>



Còn với HTTP/3 thì sao? Ta sẽ quan sát hình mô tả dưới đây

<figure><img src="../../../.gitbook/assets/image (4) (1) (1).png" alt=""><figcaption></figcaption></figure>



Trước tiên ta cần hiểu về khái niệm QUIC Protocol:\
QUIC (Quick UDP Internet Connections) là một giao thức truyền mạng được phát triển bởi Google vào năm 2012. QUIC sử dụng UDP thay vì TCP như các giao thức truyền tải thông thường. Nó được thiết kế với mục đích giúp cải thiện tốc độ truyền tải dữ liệu, giảm độ trễ và tăng cường bảo mật trên kết nối Internet.

**QUIC Protocol Bảo vệ chống giả mạo IP**

Để loại bỏ mọi tấn công giả mạo IP, QUIC hỗ trợ xác minh địa chỉ trong quá trình bắt tay và yêu cầu bằng chứng địa chỉ đã ký thông qua việc sử dụng “mã thông báo địa chỉ nguồn”. Đó là các khối được xác thực, mã hóa của máy chủ, chứa địa chỉ IP của người dùng và dấu thời gian của máy chủ. Vì máy chủ chỉ phản hồi địa chỉ IP trong mã thông báo, ngay cả một cookie hoặc mã thông báo bị đánh cắp cũng có thể không giúp việc giả mạo IP thành công. Hơn nữa, do QUIC thiết lập mã thông báo địa chỉ nguồn tồn tại trong thời gian ngắn, khoảng thời gian cho một tấn công giả mạo IP thành công trong thực tế là gần như không thể.

Vậy để ngăn chặn phát hiện rò rỉ IP thật ta nên làm gì?

* Theo mình thì cũng chưa có phương án tốt nhất nhưng để không lộ IP thật ta nên disable QUIC Protocol, điều này sẽ không chắc chắn là tốt những sẽ không bị leak IP thật, nó cũng giống như việc bạn disable WEBRTC khi IP WEBRTC bị leak vậy.
* Hoặc phương án thứ 2 bạn dùng hoàn toàn Proxy US nếu IP thực của bạn là VN thì bạn có thể dùng qua 1 lớp VPN US, điều này sẽ làm giảm rủi do hơn vì 1 số hệ thống có thể chấp nhận được việc IP khác nhau nhưng country location giống nhau (tỷ lệ pass cao hơn)

Ở đây tôi sẽ lấy 1 số ví dụ thực tế

<figure><img src="../../../.gitbook/assets/image (5) (1) (1).png" alt=""><figcaption></figcaption></figure>





Ở google login hầu hết các request được sử dụng h3 có nghĩa là giao thức HTTP/3. Điều này có nghĩa rằng IP thực tế của bạn có thể bị google thu thập. Khi bạn thực hiện spam tạo tài khoản hoặc login hệ thống mà hiện captcha google mặc dù đổi IP liên tục, vì google sử dụng h3 để request captcha.

<figure><img src="../../../.gitbook/assets/image (6) (1) (1).png" alt=""><figcaption></figcaption></figure>



Ở hidemium, bạn có thể disable QUIC Protocol cho profile bằng cách vào tab Other chọn **Disable**

<figure><img src="../../../.gitbook/assets/image (7) (1).png" alt=""><figcaption></figcaption></figure>



Sau khi Disable QUIC Protocol tất cả các giao thức request đã được chuyển về h2

<figure><img src="../../../.gitbook/assets/image (8) (1).png" alt=""><figcaption></figcaption></figure>



Hiện tại một số dịch vụ Proxy cũng đã có phương thức auto Disable QUIC. Để kiểm tra dịch vụ proxy của bạn có hỗ trợ disable QUIC hay không hãy kiểm tra bằng cách nhấp chuột phải tại thanh header chọn Protocol và vào google để check xem giao thức với google đã được chuyển về h2 hay chưa

<figure><img src="../../../.gitbook/assets/image (9) (1).png" alt=""><figcaption></figcaption></figure>

Chúc các bạn trang bị kiến thức tốt để kiếm triệu đô.\
**Hidemium Team**
