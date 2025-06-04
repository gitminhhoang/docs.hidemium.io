# Cơ chế phát hiện người hoặc robot

Theo lập trường cá nhân, hiện nay cuộc chiến giữa người và bot AI đang diễn ra hằng ngày đòi hỏi các hệ thống càng ngày càng detected chặt chẽ hơn, càng khó, càng phải chi tiết hơn trước. Chính vì thế chúng ta cần phải hiểu nguyên nhân gốc rễ vấn đề để tự mình nâng cao tầm hiểu biết, nâng cao chính bộ máy công nghệ của mình lên. Sau đây mình xin trình bày 1 số khái niệm check bot cơ bản có thể các bạn đã biết, bạn nào chưa biết thì xin 1 like!!

Với _Bot dựa trên web_ , tôi đề cập đến các bot giao tiếp chủ yếu qua giao thức `HTTP` và `HTTPS` bao gồm request http trong ngôn ngữ lập trình hoặc request trong trình duyệt thực tế ta có thể nhìn thấy được. Ở đây, tôi sẽ chỉ xem xét các bot có [phần tiên tiến](https://www.imperva.com/blog/bad-bot-report-2020-bad-bots-strike-back/) nghĩa là Good Bot hoặc bot Human. Nói cách khác, các Good Bot tận dụng các trình duyệt thực bằng cách sử dụng một số dạng tự động hóa trình duyệt như Playwright, Puppeteer, Selenium, PhantomJS và nhiều loại khác.

Các lập trình viên tạo _Bot dựa trên web_ vì vô số lý do kinh tế khác nhau:

* Tự động hóa các công việc liên tục để tiết kiệm sức lao động của con người
* Cào thông tin có giá trị từ các trang web (Công cụ tìm kiếm, Amazon, eBay, YouTube, …)

Hoặc những ứng dụng:

* Tự động tạo nội dung trên các nền tảng truyền thông xã hội (Twitter, TikTok, Instagram Bots)…
* Thực hiện auto click ads…
* Mạo danh Người dùng khác…

Để không bị phát hiện và đánh dấu là bot xấu, anh em cần giả lập hành vi, thông số gần gũi nhất với con người thật. Ở đây tôi sẽ trình bày một số khía cạnh mà các hệ thống cơ bản sẽ phát hiện:

**1. Lấy dấu vân tay của trình duyệt**\
Dấu vân tay của trình duyệt là cấu hình kỹ thuật của trình duyệt cho phép trang web nhận dạng và phân biệt người dùng truy cập.

Trình duyệt cung cấp rất nhiều thông tin cho các trang web mà chúng truy cập. Ví dụ: **`window.navigator`** trưng bày nhiều thông tin khác nhau cho phép lấy dấu vân tay của trình duyệt và tìm hiểu thêm về useragent của trình duyệt

<figure><img src="../../../.gitbook/assets/image (26).png" alt=""><figcaption></figcaption></figure>

&#x20;

Hiện nay tồn tại các thư viện JavaScript check fingerprint được sử dụng rộng rãi như [vân tay](https://github.com/fingerprintjs/fingerprintjs) , với mục đích duy nhất là thu thập càng nhiều biến cấu hình trình duyệt và đánh giá mức độ rủi do. Để có được dấu vân tay trình duyệt ổn định là một vấn đề chúng ta cần tối ưu:

1. Làm nhiễu càng chuẩn thông tin càng tốt. Cái nào không giả lập được giống thật thì tốt nhất nên tắt đi. (Ví dụ như canvas). Vậy nên hiện nay trên thị trường rất ít bên có thể fake được các nền tảng khác nhau mà pass xanh được tất cả các hệ thống check (Pixelscan, browserscan, browserleaks, creepjs …).
2. Nên dùng trên 1 thiết bị tránh làm thay đổi fingerprint, vì khi làm nhiễu thông tin thì con số làm nhiễu đó sẽ chỉ tồn tại trên máy đó. Khi mở ở máy khác thì số nhiễu đó sẽ bị chuyển đổi sang số khác nên cũng sẽ gây rủi do cho người dùng.

Các thông số lấy dấu vân tay của trình duyệt tốt nhất không nên thay đổi trong quá trình sử dụng, ví dụ:

* Múi giờ ( `"Europe/Berlin"` ) trình duyệt của bạn được định cấu hình trong:`window.Intl.DateTimeFormat().resolvedOptions().timeZone`
* Nền tảng ( `"Linux x86_64"` ) mà trình duyệt của bạn đang chạy:`navigator.platform`
* Sự tương tranh phần cứng ( `4` ) của trình duyệt:`navigator.hardwareConcurrency`
* Độ phân giải màn hình của bạn ( `[1920, 1080]` ):`[window.screen.width, window.screen.height]`
* Dung lượng bộ nhớ ( `4` ) mà thiết bị của bạn có:`navigator.deviceMemory`
* Codec âm thanh/video nào trình duyệt của bạn hỗ trợ
* Trình duyệt có kích hoạt màn hình cảm ứng hay không
* Và nhiều cái khác …

**Dấu vân tay của trình duyệt có liên quan như thế nào đến good bot?**\
Người tạo bot cố gắng giả mạo dấu vân tay duyệt web càng chung chung càng tốt. Chiến lược chính của họ là ẩn mình dưới radar và ngụy trang thành một khách truy cập có dấu vân tay duyệt web thông thường.

Một điểm quan trọng khác đối với người tạo bot là **không nói dối khi giả mạo dấu vân tay của họ** : Ví dụ: đặt Useragent iPhone nhưng không điều chỉnh Useragent cho phù hợp `navigator.userAgent` hoặc `navigator.appVersion` sẽ khiến các công ty chống bot phát hiện ra rằng trình duyệt có khả năng bị giả mạo.

Với Adspowser IO

<figure><img src="../../../.gitbook/assets/image (27).png" alt=""><figcaption></figcaption></figure>



<figure><img src="../../../.gitbook/assets/image (28).png" alt=""><figcaption></figcaption></figure>

&#x20;

Với [Hidemium](https://hidemium.io/) Iphone

<figure><img src="../../../.gitbook/assets/image (29).png" alt=""><figcaption></figcaption></figure>



<figure><img src="../../../.gitbook/assets/image (30).png" alt=""><figcaption></figcaption></figure>

&#x20;

Một lỗi rất phổ biến khác mà tôi thường thấy: Lập trình viên bot fake Useragent của họ trong tiêu đề HTTP nhưng lại quên làm như vậy trong thuộc `navigator` tính (Chủ yếu là `navigator.userAgent` và `navigator.appVersion` ).

**2. Các khía cạnh mạn**

<figure><img src="../../../.gitbook/assets/image (31).png" alt=""><figcaption></figcaption></figure>

&#x20;

Các Good Bot dùng proxy dân cư hoặc di động để thay đổi địa chỉ IP của chúng.\
Lý do tại sao họ làm điều này rất đơn giản: _Hầu hết các trang web đều sử dụng giới hạn tốc độ dựa trên IP. Nói cách khác: Khi bot của bạn xử lý hàng nghìn trang trong một khoảng thời gian ngắn, bot có thể bị chặn nhanh chóng do mỗi yêu cầu đều xuất phát từ cùng một địa chỉ IP_.\
Khi bạn mua proxy share dùng chung nhiều người, tốc độ proxy của bạn cũng sẽ không được tốt và tốc độ load trang cũng sẽ bị ảnh hưởng.

Hơn nữa, các loại Địa chỉ IP khác nhau có ISP khác nhau trên Internet. Ví dụ: các địa chỉ IP của Datacenter như địa chỉ IP của [Amazon AWS](https://aws.amazon.com/) hoặc [Google Cloud Functions ](https://cloud.google.com/functions) có mức độ trust khá thấp khi nói đến lưu lượng truy cập web. Lý do rất rõ ràng: Quản trị viên web không thích lưu lượng truy cập bắt nguồn từ ISP Datacenter vì khả năng lớn đó là lưu lượng truy cập tự động. _Người dùng bình thường định tuyến lưu lượng truy cập thông qua các máy chủ đám mây như thế nào?_

Địa chỉ IP di động có uy tín cao nhất. Hầu như không thể chặn lưu lượng truy cập bắt nguồn từ địa chỉ IP di động vì nhiều người dùng khác nhau trong cùng một khu vực di động chia sẻ cùng một địa chỉ IP trong mạng 4G.

Giải thích của các chuyên gia từ [proxyize.com ](https://proxidize.com/) :

> Proxy di động 4G/LTE mạnh đến mức chúng khiến các lệnh cấm IP truyền thống hoàn toàn vô dụng, điều này là nhờ vào công nghệ mới được các nhà cung cấp dịch vụ di động có tên là CGNAT sử dụng. Dịch địa chỉ mạng cấp nhà cung cấp dịch vụ là một khái niệm rất đơn giản, có nghĩa là IP hiện tại của bạn đang được chia sẻ bởi hàng trăm, nếu không muốn nói là hàng nghìn người thực. Các trang web biết rất rõ điều này và họ biết nếu họ cấm một IP duy nhất, họ có thể cấm hàng trăm người dùng thực. (Nguồn: [proxyize.com/full-guide/ ](https://proxidize.com/full-guide/))

_– Fingerprint TCP/IP_\
Một khía cạnh khác ít được biết đến hơn khi phát hiện bot là dấu vân tay TCP/IP. Bởi vì nhiều hệ điều hành có một dấu vân tay TCP/IP duy nhất (ví dụ: `window size` và `MTU` khác nhau giữa các hệ điều hành), nên có thể đưa ra phỏng đoán rất chính xác về hệ điều hành của máy chủ đang giao tiếp với máy chủ chỉ dựa trên dữ liệu đến đầu tiên. Gói TCP SYN. [p0f3](https://lcamtuf.coredump.cx/p0f3/) có lẽ là công cụ lấy dấu vân tay TCP/IP thụ động được sử dụng nhiều nhất hiện nay.

Để tham khảo rõ hơn mời bạn đọc bài [TCP/IP Fingerprint là gì](https://forum.hidemium.io/t/tcp-ip-browser-fingerprint-la-gi/69)

Tại sao điều này lại liên quan đến việc phát hiện bot?

<figure><img src="../../../.gitbook/assets/image (32).png" alt=""><figcaption></figcaption></figure>

&#x20;

Lý do rất rõ ràng: Nhiều lập trình viên bot đang sử dụng dịch vụ proxy thương mại để chuyển đổi và ẩn địa chỉ IP thực của họ. Tuy nhiên, khi bạn định cấu hình dấu vân tay trình duyệt của mình trông giống iPhone nhưng chữ ký gói TCP SYN trông giống như thuộc về hệ điều hành Linux, chỉ có hai cách giải thích hợp lý cho điều đó:

1. Lưu lượng truy cập đến từ người dùng iPhone hợp pháp sử dụng VPN/Proxy
2. Một lập trình viên bot độc hại đã quên giả mạo dấu vân tay TCP/IP của họ (hay chính xác hơn: máy chủ proxy ở giữa)

Phát hiện bot bằng dấu vân tay TCP/IP thụ động là một kỹ thuật có khả năng dẫn đến nhiều kết quả không chính xác. Do đó, nó có thể được sử dụng theo cách khác như:

> _Vào một ngày bình thường, 5% khách truy cập của tôi sử dụng VPN/Proxy. Nhưng sau hai giờ, 40% người dùng của tôi đột nhiên xuất hiện một số loại dấu vân tay TCP/IP mới. Hãy chặn lưu lượng truy cập đó một lúc và xem có ai phàn nàn không;)_

**3. Automation**

<figure><img src="../../../.gitbook/assets/image (33).png" alt=""><figcaption></figcaption></figure>

&#x20;

Các Good bot thường dựa trên [kịch bản automation puppeteer](https://github.com/puppeteer/puppeteer) hoặc [kịch bản automation playwright](https://github.com/microsoft/playwright) . Hệ thống automation đó sử dụng [Giao thức DevTools](https://chromedevtools.github.io/devtools-protocol/) , cho phép tự động hóa và kiểm soát các trình duyệt theo chương trình. Điều này có nghĩa là bạn có thể kiểm soát toàn bộ chức năng của trình duyệt bằng [API cấp cao](https://github.com/puppeteer/puppeteer/blob/main/docs/index.md) .

Ngay lập tức, Hệ thống automation web đó được cung cấp cùng với các tệp nhị phân của trình duyệt được biên dịch sẵn. Những tệp nhị phân đó thường được cấu hình hơi khác so với các tệp nhị phân của trình duyệt thông thường.

Có các plugin Node.js dành cho người remote automation, khắc phục [tình trạng detect automation](https://github.com/berstend/puppeteer-extra/tree/master/packages/puppeteer-extra-plugin-stealth#readme).

Tuy nhiên, người dùng thực sự remote trình duyệt của họ khá khác so với hành vi do sử dụng API của người remote automation. Ví dụ: người thực sự không đợi một số sự kiện nhất định xảy ra trước khi di chuyển chuột của mình (chẳng hạn như sự kiện `networkidle2` ).

Hơn nữa, vì các chương trình remote automation thường giao tiếp qua giao thức Web Socket nên có một độ trễ nhỏ giữa việc thực hiện các lệnh (hoặc độ trễ lớn hơn khi sử dụng [Giao thức DevTools từ xa](https://www.browserless.io/) ).

Thông thường, các hệ thống remote automation đó [không hỗ trợ tốt](https://github.com/puppeteer/puppeteer/issues/4378) cho việc tạo các chuyển động chuột hoặc sự kiện click thực tế.

**4. Cơ sở hạ tầng lưu trữ**

Các Good Bot cần được lưu trữ ở đâu đó. Chỉ các hoạt động bot quy mô nhỏ mới có thể được chạy từ máy tính cá nhân của các lập trình viên. Do đó, các bot dựa trên web thường được lưu trữ từ bên trong cơ sở hạ tầng đám mây.

Tuy nhiên, con người thực sự duyệt web từ máy tính cá nhân và điện thoại thông minh của họ. Với sự trợ giúp của JavaScript, thường có thể xác định loại môi trường máy tính nơi mã JavaScript được thực thi.

Bởi vì các lập trình viên bot muốn lưu trữ bot của họ một cách tiết kiệm nên họ **phân bổ ít tài nguyên CPU/Bộ nhớ khi cần thiết** . Điều này hoàn toàn trái ngược với người dùng bình thường sử dụng máy tính xách tay có bộ nhớ 16GB để truy cập các trang web đơn giản. Đây có thể là một phương pháp phỏng đoán khác có thể được sử dụng để đưa ra phỏng đoán có căn cứ xem Useragent có phải là bot hay không. [Hidemium](https://hidemium.io/) hỗ trợ anh em giả lập memory, ổ đĩa ổ cứng tăng lên so với các bên không hỗ trợ fake ổ cứng ổ đĩa

<figure><img src="../../../.gitbook/assets/image (34).png" alt=""><figcaption></figcaption></figure>



&#x20;

Trình duyệt cũng có thể làm rò rỉ thông tin về GPU và CPU của máy tính. Một thử nghiệm đơn giản là đo thời gian cần thiết để [hiển thị khối WebGL](https://bot.incolumitas.com/redpill/webgl.html) . Các thử nghiệm khác đo độ trễ giữa CPU và GPU. Trên hạ tầng cloud giá rẻ thường chỉ hỗ trợ GPU ảo nên độ trễ sẽ lớn hơn.

Một số VPS đám mây thường mở một số cổng mặc định nhất định. Có thể lấy dấu vân tay của các cổng đang mở vì [có thể quét cổng mạng bằng JavaScript trong trình duyệt](https://incolumitas.com/2021/01/10/browser-based-port-scanning/) . Do đó, một trang web có thể quét cổng mạng cục bộ của hệ điều hành bot của bạn và nếu nó giống như một VPS, hãy chặn bạn. Vì vậy tôi khuyên bạn nên chặn tất cả các cổng mà VPS có thể mở [Bạn có thể tham khảo tại đây ](https://nullsweep.com/why-is-this-website-port-scanning-me/)

* 5900: VNC
* 5901: VNC port 2
* 5902: VNC port 3
* 5903: VNC port 4
* 5279:
* 3389: Windows remote desktop / RDP
* 5931: Ammy Admin remote desktop
* 5939:
* 5944:
* 5950: WinVNC
* 6039: X window system
* 6040: X window system
* 63333: TrippLite power alert UPS
* 7070: RealAudio

[Hidemium](https://hidemium.io/) có chức năng block port, Nếu bạn nào chạy trên VPS hãy dùng nó block các cổng cơ bản trên VPS

**5. Lấy dấu vân tay hành vi**

Phương pháp phát hiện tốt nhất và khó nhất được đưa ra cuối cùng: Kỹ thuật phát hiện dựa trên hành vi.\
Hành vi con người thì rất là khó đoán nhưng nó cũng sẽ tuân theo một số rule cơ bản, Con người di chuyển chuột, bàn phím, màn hình cảm ứng và con lăn theo kiểu tự nhiên. Bot vẫn gặp khó khăn trong việc bắt chước chuyển động của chuột và thao tác chạm trên màn hình cảm ứng như người thật. Một số sự kiện JavaScript được quan tâm ở đây: `mousedown` , `mousemove` , `touchstart` , `touchmove` , `keydown` , …

<figure><img src="../../../.gitbook/assets/image (35).png" alt=""><figcaption></figcaption></figure>

&#x20;

Một quy trình đơn giản để phân biệt bot với người thật dựa trên dữ liệu hành vi có thể như sau:

1. Bước đầu tiên là thu thập hành vi của bạn.
2. Bước tiếp theo (và khó hơn) là phân loại tập dữ liệu giống con người hoặc giống bot (từ dữ liệu database đã có từ trước đó).
3. Bạn nên có một kiến thức về hành vi thao tác để viết ra bot automation phù hợp, thời gian click năn chuột sao cho giống người thật nhất có thể.

Có một số công ty như [biocatch](https://www.biocatch.com/) và [perimeterx](https://www.perimeterx.com/) đã sử dụng phương pháp này từ nhiều năm nay.

Nhưng chính xác thì điều gì tạo nên sự tương tác giữa chuột hoặc sự kiện chạm trong trình duyệt với _con người_ ? Các tính năng cực kỳ khó mô phỏng một cách máy móc là gì? Một số ý tưởng sơ bộ (thay thế _chuột_ bằng các sự kiện chạm trong trường hợp thiết bị di động):

* Con chuột được sử dụng để hỗ trợ việc đọc ( _bạn hãy tự quan sát_ ), lúc đọc văn bản chuột bạn thường để đâu và làm gì?
* Tốc độ bắt đầu và dừng chuột giữa các điểm ưa thích
* Quỹ đạo di chuyển của chuột
* Phân bố các sự kiện theo thời gian. Con người nhìn vào màn hình, xử lý thông tin một cách trực quan và phản ứng vật lý. Mô hình này lặp đi lặp lại mọi lúc. Độ trễ trong các kiểu phản ứng như vậy về bản chất là do con người.
* Khoảng thời gian giữa các lần click chuột
* Chuột đi theo điểm lấy nét của mắt
* Tốc độ cuộn tương quan với thời gian đọc
* Dữ liệu hành vi tăng đột biến khi một trang web yêu cầu tương tác
* Chuột di chuyển lên trên cùng (tab) khi điều hướng đi (không phải trên thiết bị di động)
* Chỉ dành cho thiết bị di động: đôi khi kích thước màn hình giảm mạnh 180 độ khi tự động xoay
* Khi không quan tâm, chuột chạy rất nhanh đến nút “đóng tab”
* Các lĩnh vực quan tâm trong văn bản được đánh dấu
* …?

Bài viết được dịch từ tác giả **incolumitas**\
Để miễn phí trải nhiệm hidemium mời bạn tải tại: [Download ](https://hidemium.io/download)\
Mua gói hidemium để trải nhiệm automation tại: [Pricing](https://hidemium.io/pricing)
