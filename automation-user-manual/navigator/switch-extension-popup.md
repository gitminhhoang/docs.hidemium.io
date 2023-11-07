# Switch Extension popup

Một số trang có Extension popup và bạn phải sử dụng nút Switch Extension popup để điều hướng. Bạn có hai lựa chọn Extension popup page và Main page. Nếu chọn Extension popup page bạn cần chọn element  của khung đó và ở đây bạn cũng đặt thời gian chờ. Giống như việc bạn đăng ký vào một nền tảng thông qua các tài khoản nền tảng khác sẽ gặp trường hợp như thế này, VD: đăng ký twitter bằng tài khoản apple thì nó sẽ hiện ra một tab ngoài tab chính để đăng ký. Lúc này nếu muốn script điều khiển được tab phụ kia thì cần dùng node Switch Extension popup này.

<figure><img src="../../.gitbook/assets/Switch Extension popup.png" alt=""><figcaption></figcaption></figure>

| parameter                            | illustrate                                                                                                                                                       |
| ------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Extension popup page: Select element | Nhập CSS selector, chẳng hạn như #email, #global-enhancements-search-query. Sau khi chọn Extension popup page thì các node phía sau sẽ được hoạt động tại popup  |
| Extension popup page: Main page      | Khi ta muốn điều hướng các node phía sau trở lại trang chính của trang web sau khi chọn Extension popup page thì ta chọn Main page                               |
| Timeout waiting                      | Thời gian chờ đợi tối đa. Ví dụ: 30000: Nếu bước này không được thực hiện thành công trong vòng 30 giây thì bước tiếp theo sẽ được thực hiện trực tiếp.          |

{% file src="../../.gitbook/assets/Switch Extension popup.txt" %}
