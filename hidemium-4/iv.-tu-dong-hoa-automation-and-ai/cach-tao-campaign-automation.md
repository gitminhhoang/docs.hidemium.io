# CÁCH TẠO CAMPAIGN AUTOMATION

**Cách để chúng ta tạo một campaign chạy auto hoàn chỉnh như sau :**&#x31;. Từ màn “Work flow” của automation, click vào biểu tượng mũi tên màu xanh này, di chuột qua cũng đã nhìn thấy nội dung là “Create Campagin” .

![](http://education.hidemium.io/wp-content/uploads/2024/05/Transfer-1.png)

2\. Tạo tên campaign và click “Ok”

![](http://education.hidemium.io/wp-content/uploads/2024/05/Untitled-4.png)

3\. Input là phần để chỉnh các giá trị của biến trong script, cũ là mỗi lần chạy mà muốn thay các giá trị thì cần phải mở script ra rồi chỉnh thì giờ đây ta có thể chỉnh các giá trị của biến ngay tại màn “input” của tạo campgain này

![](http://education.hidemium.io/wp-content/uploads/2024/05/Untitled-5.png)

4\. Profile là phần chọn profile để chạy, tại đây có các option như chọn lần lượt profile hoặc chọn folder, hoặc chạy với 1 danh sách custom UUID khác thì cũng sẽ được bổ sung ở bên cạnh 2 mục ” profile” và ” folder” này.

![](http://education.hidemium.io/wp-content/uploads/2024/05/Untitled-6.png)

**5.** Tại mục setting, bạn có thể chỉnh

* số luồng chạy cùng lúc của campaign đó ở phần **Automation processing,**
* chỉnh thời gian delay mở giữa các profile ở **Delay open (Seconds)**
* **Screen arrangement** là chỉnh số hàng và số cột để sắp xếp profile theo.
* **Auto scale screen** là chỉnh % to nhỏ của toàn bộ profile, bạn có thể tắt auto scale và để 100% nhé.
* **Screen size** mới là phần resize profile to nhỏ nếu bạn muốn các profile chạy với size màn giống nhau. Lưu ý là chỉ có thể nhập size nhỏ hơn size profile mặc định nhé.

![](http://education.hidemium.io/wp-content/uploads/2024/05/Untitled-7.png)

&#x20;  Hidemium mới cập nhật thêm 1 số tính năng để việc tạo campaign của mọi người trở lên linh động và dễ dàng hơn :

* **Auto set window size :** Bạn bật chức năng này thì profile sẽ chạy với chính xác size profile được tạo. Bạn tắt chức năng này thì mặc định profile sẽ lấy size gần nhất được dùng ví dụ như dùng từ sync action hay dùng từ các lần chạy auto trước.

![](https://i.imgur.com/3WUBKit.png)

&#x20;

* Ở màn profiles, bạn có thể chọn add profile theo uuid, mỗi dòng là một uuid.

![](https://i.imgur.com/929nlAI.png)

**6.** Schedule là phần setup lịch chạy của campaign, bạn có thể chọn chạy ngay lập tức nếu click vào option ONCE => Create And Run. Hoặc chạy lặp lại nhiều lần theo thời gian hoặc theo ngày, theo tuần, theo tháng. Phần này bạn có thể đọc kĩ hơn tại **https://docs.hidemium.io/automation-user-manual/how-to-start-script-auto#ii.-cac-cach-co-the-run-script-auto-voi-cac-profile** mục **II. Các cách có thể run script auto với các profiles.**

![](http://education.hidemium.io/wp-content/uploads/2024/05/Untitled-8.png)

**=> như vậy là chúng ta đã tạo xong 1 campaign automation và chỉ cần chờ đúng thời gian và cách chạy đã setup thì campaign sẽ bắt đầu.**
