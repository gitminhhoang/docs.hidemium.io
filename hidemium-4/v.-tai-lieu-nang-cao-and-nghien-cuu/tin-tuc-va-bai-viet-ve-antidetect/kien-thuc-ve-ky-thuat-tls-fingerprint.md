# Kiến thức về Kỹ thuật TLS Fingerprint

Xin chào các bạn, nay team Hidemium chúng mình xin tạo một chủ đề về TLS Fingerprint có lẽ rất nhiều các bạn chưa hề để ý về nó. Vậy vấn đề đặt ra TLS Fingerprint là gì?

Ở [fingerprint.com](https://fingerprint.com/blog/what-is-tls-fingerprinting-transport-layer-security/) có giải thích rằng: Ở cấp độ cơ bản nhất, Bảo mật lớp vận chuyển (TLS) là một thuật toán mã hóa tất cả lưu lượng truy cập internet của bạn và giúp bạn luôn an toàn khi trực tuyến. Nói chính xác hơn, nó là một giao thức được sử dụng để mã hóa thông tin liên lạc dựa trên web giữa máy khách và máy chủ bằng cách sử dụng bộ thuật toán mã hóa. Trước khi TLS có thể được sử dụng trong giao tiếp, máy khách và máy chủ phải trải qua một quá trình được gọi là bắt tay TLS.

Một số cách sử dụng phổ biến của dấu vân tay TLS:

* Để thu thập thông tin về khách hàng trên web, chẳng hạn như hệ điều hành hoặc phiên bản trình duyệt.
* Phân tích lưu lượng TLS được mã hóa, ISP của bạn có thể đoán bạn đang sử dụng trang web nào và bạn thực hiện hành động nào khi truy cập web.
* Để thu thập thông tin về máy chủ từ xa, chẳng hạn như hệ điều hành hoặc phần mềm máy chủ.

Việc nhận dạng duy nhất một khách hàng cũng có thể hữu ích cho các trường hợp sử dụng chống lừa đảo, vì những kẻ ác ý thường cố gắng che giấu danh tính của họ để thực hiện nhiều hoạt động gian lận trên một trang web. Trong khi xác định người dùng bằng cách sử dụng cookie và dấu vân tay của trình duyệt, dấu vân tay TLS có thể là một lớp nhận dạng chính xác khác cho ngăn xếp chống gian lận của bạn.



<figure><img src="../../../.gitbook/assets/image (192).png" alt=""><figcaption></figcaption></figure>



Ta hiểu đơn giản rằng tín hiệu thông tin ở tầng web được gửi nhận 2 đầu sẽ có cơ chế mã hoá thông tin.\
Và việc gửi nhận thông tin này nếu dùng khác cơ chế Cer, OS, phiên bản trình duyệt, lõi trình duyệt sẽ đưa ra mã băm khác nhau. Chúng ta có thể check tại: [SSL/TLS Client Test – TLS Fingerprinting – BrowserLeaks ](https://browserleaks.com/tls)

Vì vậy khi ta triển khai giả lập fake phiên bản core trình duyệt windows và Macos sẽ phải có 2 TLS khác nhau.

Một số hệ thống phát hiện gian lận hiện nay cũng dùng cơ chế ssl fingerprint để kiểm tra multi-account của các bạn

<figure><img src="../../../.gitbook/assets/image (193).png" alt=""><figcaption></figcaption></figure>

Một vài ví dụ tới các hệ điều hành:\
Windows 10 – Chrome 119

<figure><img src="../../../.gitbook/assets/image (194).png" alt=""><figcaption></figcaption></figure>

&#x20;

Windows 11 – Chrome 119:\


<figure><img src="../../../.gitbook/assets/image (195).png" alt=""><figcaption></figcaption></figure>

Windows 11 – Chrome 118:\


<figure><img src="../../../.gitbook/assets/image (196).png" alt=""><figcaption></figcaption></figure>



Mac Os Ventura – Chrome 115

<figure><img src="../../../.gitbook/assets/image (197).png" alt=""><figcaption></figcaption></figure>



Với hidemium team chúng mình đã và đang xử lý được thuật toán noise TLS Fingerprint:



<figure><img src="../../../.gitbook/assets/image (198).png" alt=""><figcaption></figcaption></figure>

&#x20;

Để setup noise TLS Fingerprint các bạn chỉ việc vào Other Config và Enable mode SSL fingerprint để sử dụng option nào

<figure><img src="../../../.gitbook/assets/image (199).png" alt=""><figcaption></figcaption></figure>



Theo các bạn SSL fingerprint có quan trọng không? Hãy để lại bình luận của các bạn phía bên dưới nhé.&#x20;
