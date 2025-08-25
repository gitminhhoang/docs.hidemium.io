---
description: Node này được dùnfg để đọc nội dung các mail được gửi đến mail của bạn.
---

# IMAP(Read mail)

<figure><img src="../../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

1. Email service: Bạn cần chọn dịch vụ mail mà bạn muốn đọc. Các dịch vụ được hỗ trợ bảo gồm: Gmail, Outlook/Hotmail, Yahoo, Custom.

* Gmail: Bạn cần nhập địa chỉ email mà bạn cần đọc và mật khẩu ứng dụng của email của bạn. Đối với mật khẩu ứng dụng, bạn cần tạo một mật khảu ứng dụng, có thể tham khảo cách tạo mật khảu ứng dụng [<mark style="color:blue;">TẠI ĐÂY</mark>](https://support.google.com/mail/answer/185833?hl=en).
* Outlook/Hotmail: Bạn cần nhập Email và password của mail của bạn.
* Custom: Bạn có thể tự custom một dịch vụ mail có hỗ trợ Imap khác với Email và Outlook/Hotmail. Khi chọn custom bạn cần phải nhập thêm IMAP host và IMAP port của dịch vụ mail mà bạn muốn đọc.

2. Mailbox: Mặc định sẽ là INBOX. Khi nhập là Inbox thì sẽ đọc mail nằm trong mục inbox của mail. Ngoài ra bạn cũng có thể đọc các mail nằm trong mục SPAM của Gmail bằng cách nhập <mark style="color:blue;">\[Gmail]/Spam</mark> tại trường Mailbox. Còn đối với hotmail cũng có thể đọc mail nằm trong Junk Email bằng cách nhập <mark style="color:blue;">JUNK</mark> tại trường Mailbox.
3. Các checkbox:

* Unseen mail only: Khi chọn cái này thì sẽ đọc mail ở trạng thái chưa xem, đọc tối đa 5 mail.
* Mark mail as read: Khi chọn cái này, khi đọc xong các mail ở trạng thái chưa xem thì đánh dấu các mail đó thành đã xem.
* Get latest mail: Khi chọn cái này thì sẽ các email gần nhất. Khi bỏ chọn cái này thì sẽ xuất hiện trường Sender email contains.&#x20;
* Sender email contains: Trường này xuất hiện khi bỏ chọn Get latest mail. Ở đây Bạn có thể nhập Subject của mail mà bạn muốn đọc, và sẽ lấy 5 mail gần nhất có Subject trùng với Subject mà bạn nhập vào.&#x20;

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

4. Content mail contains: Trường này dùng để nhập regex để lấy dữ liệu.
5. Read mail timeout (milliseconds): Thời gian chờ đợi tối đa. Ví dụ: 30000: Nếu bước này không được thực hiện thành công trong vòng 30 giây thì bước tiếp theo sẽ được thực hiện trực tiếp.
6. Output variable: Nhập tên biến để lưu dữ liệu lấy được từ regex.
7. Preview: Khi click vào button này thì sẽ hiển thị các email mà node đọc được và hiển thị dữ liệu lấy được thông qua regex đã nhập.
