# Outlook Mailer (oAuth2)

Để phục vụ cho việc đọc mail như hotmail và outlook thì các bạn có thể sử dụng node này.

![](http://education.hidemium.io/wp-content/uploads/2024/10/Screenshot_1.png)

1. Giải thích các trường có trong node

* Authentication type: Sẽ bao gồm email/password và refresh token. Khi bạn chọn email/password thì sẽ phải nhập email và pass của mail mà bạn muốn đọc. Còn khi chọn refresh token, bạn cần nhập refresh token của mail đó.
* Mailbox: Khi nhập giá trị ở đây thì sẽ thực hiện đọc mail ở phần mà bạn nhập. Ở đây có 2 giá trị hợp lệ mà bạn có thể nhập là INBOX và JUNK.
* Mark mail as read: khi bạn chọn tùy chọn này, khi đi đọc xong, các mail sẽ được đánh dấu là đã đọc.
* Get latest mail: Khi chọn tùy chọn này, mặc định sẽ lấy 5 mail mới nhất để đọc. Còn nếu không chọn thì sẽ có 1 trường là Subject email contains hiện ra, ở đây bạn có thể nhập tiêu đề của mail mà bạn muốn đọc, hệ thống sẽ tìm 5 mail mới nhất có tiêu đề phù hợp với giá trị bạn nhập vào để đọc.
* Content mail contains: Ở đây bạn sẽ nhập regex, hệ thống sẽ thực hiện tìm kiếm, nếu tìm thấy giá trị nào phù hợp với regex nhập vào thì sẽ lấy luôn giá trị đó vào lưu vào biến.
* Read mail timeout: Thời gian chờ tối đa, nếu hết thời gian chờ mà vẫn không đọc được mail nào thì sẽ tự động chuyển sang node kế tiếp.
* Output variable: Giá trị mà node đọc được sẽ được lưu vào biến mà bạn chọn.
* Refresh token variable: Lưu Refresh token vào biến và nếu bạn muốn đọc mail này lần nữa thì chỉ cần nhập lại refresh token này vào node mà không cần nhập email/pass nữa.

&#x20;

2\. Một số lưu ý

* Node sẽ không đọc được các email mà khi đăng nhập có bắt nhập mail khôi phục và mã code.
* Node chỉ đọc được các mail nằm trong phần INBOX và JUNKEMAIL, nên trường Mailbox chỉ chấp nhập giá trị tương ứng là INBOX và JUNK.
