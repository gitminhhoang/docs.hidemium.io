# Hướng dẫn sử dụng chức năng backup profiles local

### **I. Lưu ý quan trọng trước khi sử dụng tính năng Backup:**

Để tránh xảy ra lỗi trong quá trình sử dụng, bạn hãy đọc kỹ các lưu ý sau:

1. **Tính năng Backup profiles local sẽ chỉ áp dụng cho gói Lifetime pro.**
2. **Chỉ dùng trên phiên bản 4.0.28 trở lên:**\
   Tính năng Backup profiles local chỉ hoạt động ổn định từ bản 4.0.28 trở lên. Nếu bạn đã dùng bản 4.0.28 rồi sau đó quay lại dùng phiên bản cũ hơn thì sẽ dễ gặp lỗi.
3. **Sử dụng nhiều thiết bị (ví dụ: máy A và máy B) với cùng một tài khoản:**\
   Giả sử trước đó bạn đang sử dụng 2 thiết bị (máy A và máy B), và trên mỗi máy đều đã có sẵn một số profile trước đó.

Khi bạn thiết lập sao lưu trên máy A, **các profile thuộc tài khoản đó trên máy A** sẽ được sao lưu lên hệ thống lưu trữ (ví dụ: Drive, server). Sau đó, nếu bạn đăng nhập **cùng tài khoản đó** trên máy B , hệ thống sẽ tải profile đã sao lưu từ máy A xuống và  **ghi đè lên các profile cùng tài khoản đang có trên máy B**.

&#x20;    ⇒ Nếu máy B đang sử dụng **một tài khoản khác**, thì profile của tài khoản đó **sẽ không bị ảnh hưởng**.

&#x20;    ⇒ Vì vậy, nếu máy B có những profile quan trọng thuộc **cùng tài khoản với máy A** , hãy lưu ý để tránh mất dữ liệu do bị ghi đè.

4. **Nhớ đăng xuất hoặc tắt app khi chuyển thiết bị:**\
   Trước khi chuyển sang dùng máy khác, bạn cần xác nhận tất cả các profile đã được đóng và không có profile nào sync lỗi, sau đó đăng xuất khỏi tài khoản hoặc tắt ứng dụng để dữ liệu được đồng bộ lên drive hoặc server (tùy vào nơi bạn chọn để lưu trữ).

Nếu không, dữ liệu có thể bị mất.

Hãy chắc chắn rằng bạn đã đăng xuất tài khoản khỏi tất cả các thiết bị trước khi đăng nhập lại.

5. **Không nên tắt tính năng Backup sau khi đã bật:**\
   Nếu bạn đã bật tính năng Backup, hãy duy trì trạng thái đó. Nếu tắt đi, những profile bạn tạo sau đó sẽ không được lưu trên Drive và sẽ không xuất hiện khi bạn đăng nhập ở thiết bị khác.  **Mọi thao tác bạn thực hiện với profile** trong thời gian Backup tắt **cũng sẽ không được sync**, dẫn đến việc các thay đổi đó sẽ không được lưu trữ trên Drive hoặc server.
6. **Không đổi tên hoặc xóa thư mục Backup trên Drive hoặc server:**\
   Việc đổi tên hoặc xóa thư mục backup có thể gây lỗi đồng bộ hoặc làm mất dữ liệu.
7. **Dung lượng đầy:**\
   Nếu Nơi lưu trữ hết dung lượng, dữ liệu sẽ không được sao lưu.

Sau khi có thêm dung lượng hãy mở lại ứng dụng, và bật những profile chưa được đồng bộ để sao lưu lại.

Hãy kiểm tra dung lượng của drive thường xuyên.

&#x20;    **8. Đổi vị trí lưu trữ:**&#x20;

Nếu bạn đang sử dụng google drive làm nơi lưu trữ, thì các bạn không nên chuyển sang SFTP server để tránh việc bị mất dữ liệu. Nếu bạn thật sự cần phải chuyển nơi lưu trữ, thì sau khi chuyển sang SFTP server, bạn **bắt buộc** phải mở lại tất cả các profile cũ đang lưu trữ tại drive , do data của profile không thể tự chuyển từ drive sang server được.

&#x20;

### II. Hướng dẫn backup dữ liệu lên drive

Bước 1: Tại màn Backup local, bật Backup profiles local, sau click vào button Connect Google Drive

![](http://education.hidemium.io/wp-content/uploads/2025/04/Picture1.png)

Bước  2: Chọn tài khoản google của bạn

![](http://education.hidemium.io/wp-content/uploads/2025/04/Picture3.png)

Bước 3: Sau đó chọn Nâng cao -> chọn tiếp Đi tới Hidemium

![](http://education.hidemium.io/wp-content/uploads/2025/04/Picture4.png)

&#x20;

&#x20;

![](http://education.hidemium.io/wp-content/uploads/2025/04/Picture5.png)

Bước 4: Sau đó chọn tiếp tục

![](http://education.hidemium.io/wp-content/uploads/2025/04/Picture6.png)

Bước 5: Bạn cần chọn quyền mà Hidemium có thể truy cập, sau khi chọn xong click vào Tiếp tục

![](http://education.hidemium.io/wp-content/uploads/2025/04/Picture7.png)

Bước 6: Khi giao diện hiển thị thế này, có nghĩa là bạn đã connect thành công.

![](http://education.hidemium.io/wp-content/uploads/2025/04/Picture8.png)

&#x20;

Bước 7: Sau đó bạn cần quay lại app, sẽ có 1 popup hiện lên, các bạn nhớ đọc kỹ nội dung trong popup. Sau đó tick chọn “tôi đồng ý với các điều trên”   và sau đó click vào backup now.

![](http://education.hidemium.io/wp-content/uploads/2025/04/Screenshot_1.png)

&#x20;

**Một lưu ý khác mà các bạn cần biết đó là: Khi bạn đăng nhập trên một thiết bị mới**, sẽ xuất hiện một popup thông báo. Trong popup này sẽ hiển thị **thời gian và thiết bị cuối cùng đã sao lưu (backup) profile của bạn lên drive**.\
Hãy kiểm tra kỹ thông tin này:

* Nếu bạn thấy **thời gian sao lưu không đúng** hoặc **không phải thiết bị gần nhất bạn dùng**, **đừng vội nhấn “Accept synchronization” (Chấp nhận đồng bộ)**.
* Thay vào đó, hãy nhấn **“Check again” (Kiểm tra lại)**, rồi quay lại thiết bị trước đó và **đăng xuất đúng cách** để đảm bảo profile được sao lưu đầy đủ lên drive trước khi đồng bộ sang thiết bị mới.

&#x20;

![](http://education.hidemium.io/wp-content/uploads/2025/04/Screenshot_4-1.png)

&#x20;

### **III. Hướng dẫn sử dụng SFTP server để backup dữ liệu:**

Tại màn Backup local, bật Backup profiles local, sau đó bạn chọn SFTP server:

Các bạn cần nhập đầy đủ thông tin, hệ thống sẽ kiểm tra việc kết nối tới server có thành công hay không. Sau đó các bạn lưu thông tin lại.

![](http://education.hidemium.io/wp-content/uploads/2025/04/Screenshot_1-2.png)

&#x20;

&#x20;

**Một lưu ý khác mà các bạn cần biết đó là: Khi bạn đăng nhập trên một thiết bị mới**, sẽ xuất hiện một popup thông báo. Trong popup này sẽ hiển thị **thời gian và thiết bị cuối cùng đã sao lưu (backup) profile của bạn**.\
Hãy kiểm tra kỹ thông tin này:

* Nếu bạn thấy **thời gian sao lưu không đúng** hoặc **không phải thiết bị gần nhất bạn dùng**, **đừng vội nhấn “Accept synchronization” (Chấp nhận đồng bộ)**.
* Thay vào đó, hãy nhấn **“Check again” (Kiểm tra lại)**, rồi quay lại thiết bị trước đó và **đăng xuất đúng cách** để đảm bảo profile được sao lưu đầy đủ lên drive trước khi đồng bộ sang thiết bị mới.

![](http://education.hidemium.io/wp-content/uploads/2025/04/Screenshot_4-1.png)
