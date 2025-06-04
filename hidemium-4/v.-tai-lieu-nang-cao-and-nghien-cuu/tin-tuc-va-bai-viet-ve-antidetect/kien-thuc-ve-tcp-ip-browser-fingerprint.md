# Kiến thức về TCP/IP browser fingerprint

Bộ giao thức Internet TCP/IP, là một tập hợp các giao thức truyền thông được sử dụng trên Internet và các mạng máy tính. Dấu vân tay TCP/IP là một phương pháp phát hiện từ xa các đặc điểm của việc triển khai ngăn xếp giao thức TCP/IP.

Với việc sử dụng phương pháp này, máy chủ web có thể xác định xem máy khách đang kết nối với nó là máy Linux, Mac hay Windows. Điều này đạt được bằng cách phân tích kích thước của các gói mạng.

<figure><img src="../../../.gitbook/assets/image (182).png" alt=""><figcaption></figcaption></figure>

&#x20;

Các hệ thống của các sàn thương mại điện tử có thể dựa vào điều này phát hiện ra rằng bạn có đang sử dụng proxy hay không. Vì vậy với các hệ thống detect chặt chẽ như amazon, ebay, etsy… các bạn nên sử dụng proxy có chất lượng tốt và tìm hiểu xem proxy bạn đang dùng phù hợp với config browser nào. Dưới đây mình sẽ đưa ra cho bạn các trang có thể check TCP/IP fingerprint:

![](https://browserleaks.com/favicon.ico)[BrowserLeaks](https://browserleaks.com/ip)



**My IP Address**

The main tools for checking IP address privacy. Showing Your IP Address, Reverse IP Lookup, Hostname, and HTTP Request Headers, Your Country, State, City, ISP/ASN, and Local Lime, Whois Lookup, TCP/IP OS fingerprinting, WebRTC Leak Test, DNS Leak…

<figure><img src="../../../.gitbook/assets/image (183).png" alt=""><figcaption></figcaption></figure>

&#x20;

[https://tcpip.incolumitas.com/classify](https://tcpip.incolumitas.com/classify)

<figure><img src="../../../.gitbook/assets/image (184).png" alt=""><figcaption></figcaption></figure>



[http://witch.valdikss.org.ru/ ](http://witch.valdikss.org.ru/)

<figure><img src="../../../.gitbook/assets/image (185).png" alt=""><figcaption></figcaption></figure>



&#x20;

Việc bạn sử dụng proxy có thể làm thay đổi kết quả Fingerprint TCP/IP.\
Ví dụ: một proxy có thể dễ dàng sửa đổi kết quả vì dấu vân tay của trình duyệt TCP/IP sẽ là hệ điều hành của proxy

<figure><img src="../../../.gitbook/assets/image (186).png" alt=""><figcaption></figcaption></figure>



&#x20;

Vì vậy dựa vào đây dù config profiles có ngon như nào mà proxy đưa ra kết quả khác với OS browser thì cũng ra tỷ lệ xịt như bình thường. Vì vậy nhiều người đưa ra giải pháp cài máy ảo hoặc VPS để đưa về dạng TCP/IP khớp với nhau. Nhưng với mình thì khi dùng proxy chỉ cần lấy config trùng vs OS của TCP/IP fingerprint của con proxy đó là có thể yên tâm về mặt config profiles.

<figure><img src="../../../.gitbook/assets/image (187).png" alt=""><figcaption></figcaption></figure>

&#x20;

<figure><img src="../../../.gitbook/assets/image (188).png" alt=""><figcaption></figcaption></figure>

&#x20;

Mình đã gặp rất nhiều người nói với mình rằng cái này không quan trọng, không cần chuẩn cái đấy làm vẫn được. Nhưng mà các bạn không biết rằng tất cả các thông tin đấy hệ thống đó có thể check được và chảm bạn bất kỳ lúc nào họ muốn.

Sau đây là bài test TCP/IP với sàn Ebay

<figure><img src="../../../.gitbook/assets/image (189).png" alt=""><figcaption></figcaption></figure>



[Hi](https://www.youtube.com/watch?v=6R3SRwrsSsg)[demium và Tầm quan trọng của TCP/IP với các sàn thương mại điện tử](https://www.youtube.com/watch?v=6R3SRwrsSsg)

Với mình để nuôi 1 tài khoản giá trị cao trên antidetect browser, hãy nên trạng bị cho bản thân kiến thức tốt nhất để đạt được max value profits.
