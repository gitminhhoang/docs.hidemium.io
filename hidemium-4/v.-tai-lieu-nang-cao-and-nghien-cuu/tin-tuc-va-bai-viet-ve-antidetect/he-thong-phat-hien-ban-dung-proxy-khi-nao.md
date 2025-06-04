# Hệ thống phát hiện bạn dùng Proxy khi nào?

Hôm nay, chúng ta hãy thảo luận về cách các hệ thống bảo mật cố gắng phát hiện chúng ta đang cố gắng ẩn kết nối proxy và cách tránh điều đó.

<figure><img src="../../../.gitbook/assets/image (10).png" alt=""><figcaption><p>Fraud analysis</p></figcaption></figure>



### Hệ thống phát hiện bạn dùng Proxy khi nào?

Hầu hết ngày nay các hệ thống tài chính, sàn thương mại điện tử, mạng xã hội, hệ thống crypto…. trên internet đều có hệ thống chống gian lận, vậy điều gì sẽ khiến bạn không thể làm việc hiệu quả trên các sân chơi này?

Bạn có thể ở trong “vùng rủi ro” nếu:

* IP của bạn gần đây đã bị lọt vào hệ thống chống lừa đảo
* Phát hiện bạn giả mạo DNS
* Fingerperint của trình duyệt sai, không chuẩn
* IP của bạn có Điểm gian lận cao
* IP của bạn đã được phát hiện thuộc về các mạng đáng ngờ. Tham khảo tại ([BAD ASN LIST](https://forum.hidemium.io/t/bad-asn-list-2024/98))
* Các yếu tố khác.

Càng có nhiều cờ đỏ thì tài nguyên web càng có nhiều khả năng cho rằng bạn đang kết nối thông qua proxy.

### Hậu quả của việc phát hiện proxy là gì?

Đối với tài nguyên web, hành vi của người có kết nối proxy khác với hành vi của người dùng thông thường và có thể gây ra những tổn thất nhất định cho dịch vụ, điều mà dịch vụ không muốn cho phép. Do đó, việc phát hiện hành vi như vậy là nguy hiểm và có thể bị từ chối dịch vụ. Thông thường điều này được thể hiện trong việc chặn tài khoản và kiểm tra bổ sung.

&#x20;

### Làm thế nào để ẩn proxy một cách đáng tin cậy?

Có rất nhiều lời khuyên về vấn đề này trên Internet, nhưng tất cả đều khuyên bảo các bạn nên “tạo cookie”, “sử dụng TOR”, “chuyển sang VPN”. Hãy tin tôi, làm theo những lời khuyên này, không phải lúc nào cũng có thể ẩn proxy một cách hiệu quả. Dưới đây là một số cách đã được thử nghiệm:

Trước hết, hãy sử dụng proxy chất lượng cao và sạch có hỗ trợ giao thức UDP và trình duyệt fake IP WebRTC.\_ Điều này rất quan trọng vì những dấu vân tay này đã được hệ thống chống lừa đảo theo dõi thành công. Nếu proxy không giả mạo UDP hoặc WebRTC, địa chỉ IP thực của bạn sẽ rất dễ bị phát hiện.

_Thực hiện kiểm tra rò rỉ DNS_ trước khi sử dụng mục đích chính. Nếu bạn sử dụng dịch vụ proxy tệ, cái gọi là Rò rỉ DNS có thể xảy ra. Trong trường hợp này, hệ thống chống lừa đảo sẽ thấy rằng các truy vấn DNS đến từ các thiết bị khác nhau, điều này tất nhiên sẽ gây nghi ngờ.

Không sử dụng DNS của Google, Cloudflare, Amazon\_ và các công ty lớn khác. Một vài năm trước, hệ thống chống lừa đảo không chú ý nhiều đến việc người dùng truy cập một trang web có DNS như vậy. Bây giờ các thuật toán đã thay đổi và như thực tế cho thấy, tốt hơn là sử dụng DNS của nhà cung cấp proxy.

_Xem sự ổn định của kết nối proxy._ Nếu thường xuyên bị ngắt kết nối với máy chủ proxy, trong trường hợp này cũng có nguy cơ “rò rỉ” địa chỉ IP và DNS thực của bạn. Đây có thể là tín hiệu cho hệ thống chống lừa đảo biết rằng bạn đang sử dụng proxy hoặc VPN.
