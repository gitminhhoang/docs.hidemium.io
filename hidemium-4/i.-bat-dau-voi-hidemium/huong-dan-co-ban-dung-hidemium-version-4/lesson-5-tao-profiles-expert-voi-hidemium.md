# Lesson 5: Tạo profiles Expert với Hidemium

{% embed url="https://youtu.be/8bxLQw-UFIA" %}

Ở Lesson trước, chúng ta đã tạo thành công profiles thông qua giao diện Newbie. Trong lesson này, chúng ta sẽ tiến hành tạo profiles bằng giao diện Expert của Hidemium. Dưới đây là các bước hướng dẫn chi tiết:

Bước 1: Truy cập vào giao diện tạo profile Expert

<figure><img src="../../../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>



Trước tiên, nhấn vào nút Add Profiles, sau đó chọn nút Go to Expert.

<figure><img src="../../../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>



Giao diện Expert cung cấp nhiều tùy chọn hơn với 8 hạng mục chính:

1. Basic Info (Thông tin cơ bản)
2. Proxy
3. Cookies
4. Hardware (Phần cứng)
5. Bookmark
6. Extension (Tiện ích mở rộng)
7. Other (Khác)

Hãy cùng tìm hiểu chi tiết từng mục:

1. Basic Info (Thông tin cơ bản)

<figure><img src="../../../.gitbook/assets/image (13).png" alt=""><figcaption></figcaption></figure>



Trong phần Basic Info, bạn sẽ thấy các trường như Name, Folder, và Status. Bạn có thể tùy chỉnh các trường này theo yêu cầu của dự án hoặc công việc. Ở mục Platform, bạn chọn hệ điều hành phù hợp với mục đích sử dụng. Nếu bạn đang dùng bản app cài đặt trên Windows, nên ưu tiên chọn Windows để tối ưu hiệu suất giả lập. Tương tự, nếu dùng trên Mac, bạn nên chọn hệ điều hành Mac để tối ưu hóa.

* Platform Version: Giả lập các phiên bản hệ điều hành cụ thể như Windows 10 hoặc Windows 11.
* Browser: Lựa chọn trình duyệt bạn muốn giả lập, bao gồm Chrome, Opera, Edge, Brave, hoặc Safari.
* Browser Version: Chọn phiên bản trình duyệt để giả lập.
* Auto Fill User Agent: Dựa trên các thông tin trên, hệ thống sẽ tự động tạo mã User Agent phù hợp. Nếu bạn muốn tự tùy chỉnh User Agent, hãy bỏ tích chọn và nhập mã bạn muốn. Tuy nhiên, để cấu hình tốt nhất, bạn nên sử dụng tính năng Auto Fill User Agent.
* Port to Protect: Chúng tôi đã viết riêng một bài giải thích về tính năng này, vui lòng tham khảo tại:[ Port to Protect là gì? Nguyên lý hoạt động của Hidemium](https://forum.hidemium.io/t/ports-to-protect-la-gi-nguyen-ly-ho-t-d-ng-ports-to-protect-c-a-hidemium/81)
* Start URL: Chọn địa chỉ trang web mà trình duyệt sẽ mở đầu tiên.
* Max Touch Points: Định cấu hình số điểm chạm trên màn hình. Nếu màn hình không có cảm ứng, giá trị sẽ luôn bằng 0. Đối với các màn hình cảm ứng, cấu hình sẽ được thiết lập tương ứng với từng loại thiết bị có sẵn trên ứng dụng.
* Disable Image: Tắt hiển thị hình ảnh trên trình duyệt.
* Restore Session: Khôi phục phiên làm việc trước đó.
* Use Secure DNS: Bật hoặc tắt chế độ chuyển hướng DNS an toàn.

<figure><img src="../../../.gitbook/assets/image (14).png" alt=""><figcaption></figcaption></figure>



Ở màn Location, bạn sẽ thấy các chức năng chính sau:

* Giả lập múi giờ theo proxy
* Giả lập vị trí địa lý (Geolocation) theo proxy
* Cấu hình WebRTC theo proxy
* Cài đặt ngôn ngữ theo proxy

Tất cả các thiết lập này đều được cấu hình tự động dựa trên proxy mà bạn chọn. Bạn chỉ cần đảm bảo tích chọn đầy đủ các tùy chọn để có cấu hình chuẩn xác.

2. Proxy

<figure><img src="../../../.gitbook/assets/image (15).png" alt=""><figcaption></figcaption></figure>



Ở màn Proxy, bạn có nhiều tùy chọn để cấu hình proxy theo nhu cầu sử dụng, bao gồm:

* Chọn HTTP, SOCKS5, SSH hoặc Custom Proxy Config: Bạn có thể tùy chỉnh cấu hình proxy từ mục Proxy Config (ví dụ: đặt tên là ABC Proxy).
* Chức năng Select: Chọn lại các proxy đã thêm trước đó từ màn Proxy Manager (nút màu vàng).
* Chức năng Random: Tự động chọn ngẫu nhiên một proxy từ danh sách proxy trong Proxy Manager.
* Chức năng Delete: Xóa proxy đã được nhập trước đó trong form.

Kiểm tra Proxy trước khi khởi động Profile

* Check proxy before start profile: Khi tùy chọn này được bật, proxy sẽ được kiểm tra và cập nhật thông tin vào cấu hình trước khi mở profile. Việc này giúp đảm bảo rằng proxy được kiểm tra lại các thông tin như lat/long, WebRTC IP, hoặc ngôn ngữ trong trường hợp thông tin proxy thay đổi theo thời gian.
* Check Proxy: Nút này sẽ hiển thị toàn bộ thông tin chi tiết của proxy đang sử dụng.

3. Cookies

<figure><img src="../../../.gitbook/assets/image (16).png" alt=""><figcaption></figcaption></figure>



Tại màn Cookie, bạn có thể import cookie theo hai hình thức:

* Import cookie dạng text
* Import cookie từ file

Sau khi import thành công, cookie sẽ được hiển thị và quản lý tại: chrome://settings/content/all. Việc này giúp bạn dễ dàng kiểm soát các phiên hoạt động và dữ liệu đã lưu trên trình duyệt giả lập.

4. Hardware

<figure><img src="../../../.gitbook/assets/image (17).png" alt=""><figcaption></figcaption></figure>



Phần Hardware trong Hidemium cho phép bạn giả lập các thông số phần cứng của thiết bị, giúp tùy chỉnh cấu hình để đáp ứng các yêu cầu sử dụng khác nhau. Các tùy chọn chính bao gồm:

Screen Size (Kích thước màn hình)

* Giả lập kích thước màn hình: Tùy chỉnh kích thước màn hình của thiết bị. Kích thước này cũng là kích thước tối đa mà trình duyệt có thể mở được.

WebGL Metadata

* WebGL Vendor: Giả lập nhà cung cấp card màn hình của thiết bị.
* WebGL Renderer: Giả lập loại card đồ hoạ được sử dụng với cấu hình thiết bị đó.
* Enable Swift Shader (CPU-rendering): Kích hoạt chế độ sử dụng CPU để render thay vì GPU.
* Enable WebGL2: Cho phép sử dụng công nghệ WebGL2 nhằm cải thiện hiệu suất đồ họa.
* WebGL Image: Tùy chọn làm nhiễu hình ảnh được tạo bởi WebGL nhằm tăng cường bảo mật.

&#x20;Audio và Video

* Audio: Làm nhiễu tần số âm thanh phát ra từ profiles.
* Canvas: Chế độ làm nhiễu Canvas. Có thể hiểu Canvas được thiết kế để vẽ đồ họa thông qua JavaScript và HTML, cũng có thể được sử dụng để theo dõi trực tuyến thông qua dấu vân tay của trình duyệt. Kỹ thuật này dựa trên các biến thể trong cách hiển thị hình ảnh canvas trên các trình duyệt web và nền tảng khác nhau để tạo dấu vân tay kỹ thuật số được cá nhân hóa cho trình duyệt của người dùng.
* Client Rects: Làm nhiễu kích thước pixel chính xác của hình chữ nhật giới hạn của các phần tử HTML được hiển thị.

Thông số phần cứng khác

* Hardware Concurrency: Giả lập số lượng bộ xử lý logic có sẵn để chạy các luồng trên máy tính của người dùng.
* Device Memory: Giả lập dung lượng bộ nhớ RAM của thiết bị.
* Media Devices: Giả lập tên, mã và số lượng thiết bị media như Cameras, Microphones, và Speakers.
* Replace Battery State: Giả lập trạng thái pin, cho phép thiết lập mức độ pin, thời gian sạc và tình trạng sử dụng nguồn trực tiếp hoặc pin.
* Font: Giả lập toàn bộ các font chữ sử dụng trên profiles đó để tạo ra môi trường hoạt động giống như thiết bị thật.

5. Bookmark

<figure><img src="../../../.gitbook/assets/image (18).png" alt=""><figcaption></figcaption></figure>



Tại màn Bookmark, bạn có thể ghim sẵn các đường dẫn bookmark vào profile để tiện lợi trong việc truy cập nhanh các trang web quan trọng. Các bookmark được nhập vào theo định dạng sau:

* Cấu trúc: (Tên thư mục)::(Tên bookmark)::(Đường dẫn bookmark)
* Ví dụ:
  * Facebook::Facebook::https://www.facebook.com/
  * Facebook::Notifications::https://www.facebook.com/settings?tab=notifications
  * Facebook::Account Quality::https://www.facebook.com/accountquality
  * Facebook::Ads Manager::https://www.facebook.com/adsmanager/manage/campaigns
  * Facebook::Billing::https://www.facebook.com/ads/manager/account\_settings/account\_billing
  * Facebook::Business Manager::https://business.facebook.com/select

6. Extension

<figure><img src="../../../.gitbook/assets/image (19).png" alt=""><figcaption></figcaption></figure>



Phần Extension cho phép bạn lựa chọn và cài đặt các tiện ích mở rộng (extensions) trực tiếp từ bên ngoài hoặc từ thư viện có sẵn trong ứng dụng Hidemium. Điều này giúp bạn không cần phải lên các cửa hàng ứng dụng của trình duyệt để tải lại extension.

* Cài đặt extension: Bạn có thể chọn extension có sẵn hoặc tải thêm extension tùy chỉnh qua mục Extension trong quản lý profiles.

Nếu bạn muốn thêm hoặc tùy chỉnh extension, hãy truy cập vào phần Extension trong màn hình quản lý profiles để tải lên. Chi tiết về cách tải và custom extension sẽ được hướng dẫn trong bài viết tiếp theo.



7. Other

<figure><img src="../../../.gitbook/assets/image (21).png" alt=""><figcaption></figcaption></figure>



Mục Other bao gồm các tính năng nâng cao không được liệt kê ở các phần trước, giúp bạn tùy chỉnh chi tiết hơn cho profile của mình:

* Computer Name: Giả lập tên máy tính của thiết bị.
* MAC Address: Giả lập địa chỉ MAC của máy tính.
* Effective Type: Giả lập tình trạng kết nối mạng (Wi-Fi, 3G, 4G…).
* Bluetooth: Giả lập các thiết bị Bluetooth được kết nối.
* Do Not Track: Bật/tắt chế độ Không theo dõi. Tính năng này giúp tăng cường bảo mật bằng cách hạn chế việc thu thập dữ liệu khi duyệt web.
* Custom Launch Browser Parameters: Thêm tham số dòng lệnh trước khi trình duyệt được khởi chạy. Bạn có thể tham khảo thêm các dòng lệnh tùy chỉnh[ tại đây](https://peter.sh/experiments/chromium-command-line-switches/).
* Experimental QUIC Protocol: Cho phép bật/tắt chế độ QUIC (giao thức mạng mới của Google), cải thiện hiệu suất và bảo mật khi truyền tải dữ liệu trên Internet. QUIC vẫn đang trong giai đoạn thử nghiệm và chưa được triển khai rộng rãi.

Config Redirect URL: Cho phép chuyển hướng từ URL này sang URL khác (A -> B), thường được sử dụng để quản lý và điều chỉnh dữ liệu khách hàng.
