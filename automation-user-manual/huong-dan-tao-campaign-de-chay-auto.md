# Hướng dẫn tạo campaign để chạy auto

1. Tạo camp

Tại màn workflows -> chọn script mà bạn muốn chạy -> chọn run.  khi popup mở lên bạn nhập tên camp và ấn submit.

![](http://education.hidemium.io/wp-content/uploads/2026/02/photo_2026-02-27_10-39-40.jpg)

&#x20;

Sau Khi tạo campain xong thì sẽ được điều hướng sang màn campain. Tại đây các bạn có thể thực hiện setting các phần sau:

* Input: Đây là phần để chỉnh các giá trị của biến trong script, cũ là mỗi lần chạy mà muốn thay các giá trị thì cần phải mở script ra rồi chỉnh thì giờ đây ta có thể chỉnh các giá trị của biến ngay tại màn “input” của tạo campgain này.

![](http://education.hidemium.io/wp-content/uploads/2026/02/Screenshot_3.png)

&#x20;

* profiles: Profile là phần chọn profile để chạy, tại đây có các option như chọn lần lượt profile hoặc chọn folder, hoặc chạy với 1 danh sách  UUID.

![](http://education.hidemium.io/wp-content/uploads/2026/02/Screenshot_4.png)

&#x20;

*   Settings: Tại mục setting, bạn có thể chỉnh:

    Automation processing: số profile chạy cùng lúc của campaign đó

    Delay open (Seconds): chỉnh thời gian delay mở giữa các profile

    Screen arrangement là chỉnh số hàng và số cột để sắp xếp profile theo.

    Auto scale screen: nếu để off thì bạn có thể chỉnh % to nhỏ của toàn bộ profile, còn nếu để on thì app sẽ auto chỉnh cho bạn.

    Screen size: Ban có thể điều chỉnh kích thước màn khi chạy campaign bằng cách nhập kích thước theo định dạng width x height, hoặc bạn có thể để auto, thì khi chạy sẽ lấy theo kích thước của profile đó. Lưu ý là chỉ có thể nhập size nhỏ hơn size profile mặc định nhé.

    Write logs: khi chạy thì log của profile sẽ được ghi lạiNo overlapping profiles: Nếu như bạn bật option này thì các profile sẽ không chồng lên nhau, nhưng lưu ý là nó sẽ bị thoát ra khỏi màn hình do chạy nhiều profile và chúng không đè lên nhauClose Profile On Complete: Profile sẽ bị đóng khi chạy hết script.

    ![](http://education.hidemium.io/wp-content/uploads/2026/02/Screenshot_5.png)

&#x20;

* Schedule: Schedule là phần setup lịch chạy của campaign, bạn cần click vào button Create schedule , tại đây gồm có các option sau:

**Once**: Chạy 1 lần trong ngày. bạn có thể chọn ngày và giờ chạy.

![](http://education.hidemium.io/wp-content/uploads/2026/02/Screenshot_6.png)

&#x20;

&#x20;     **Interval:** Chạy trong khoảng thời gian từ start time đến end time. Bạn cần nhập Each time delay, trường này bạn cần nhập khoảng thời gian delay giữa các lần chạy. Ví dụ bạn nhập là 5 thì khi chạy xong một lần 5 phút sau mới chạy lần thứ 2, cứ thế cho đến hết end time.

![](http://education.hidemium.io/wp-content/uploads/2026/02/Screenshot_7.png)

&#x20;     **Daily:** Chạy hằng ngày. Ở đấy bạn cần chọn Execution time là thời gian chạy script trong khoảng từ start time đến end time.

![](http://education.hidemium.io/wp-content/uploads/2026/02/Screenshot_8.png)

&#x20;      **Weekly**: Chạy hàng tuần. Tại Execution time bạn có thể chọn thứ để chạy và giờ chạy. Và chọn thời gian bắt đầu và thời gian kết thúc.

![](http://education.hidemium.io/wp-content/uploads/2026/02/Screenshot_9.png)

&#x20;      **Monthly:** Chạy hàng tháng. Bạn có thể chọn ngày và giờ để chạy, chọn thời gian bắt đầu và thời gian kêt thúc. Ví dụ bạn chọn ngày 13 thì đến ngày 13 và đến giờ thì sẽ chạy profile.

![](http://education.hidemium.io/wp-content/uploads/2026/02/Screenshot_10.png)

Sau khi setting schedule xong thì bạn click chọn **create and run** để chạy luôn ( khi đến giờ chạy).
