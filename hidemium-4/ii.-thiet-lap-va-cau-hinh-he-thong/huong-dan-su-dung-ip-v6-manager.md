# Hướng dẫn sử dụng IP V6 Manager

**IP V6 Manager** là giao diện cho phép người dùng tạo và quản lý địa chỉ IPv6 trên thiết bị, phục vụ cho việc chạy profile.

***

### I. Lưu ý

* Nếu thiết bị hoặc mạng **không hỗ trợ IPv6**, hệ thống sẽ hiển thị lỗi
* Chỉ mở được profile khi tồn tại ít nhất một địa chỉ IPv6 ở trạng thái _Active_
* Nếu không có IPv6 _Active_, hệ thống sẽ hiển thị thông báo lỗi
* Chỉ áp dụng cho gói: **Premium, Business, Custom >= 1000 profile, Lifetime, Lifetime Pro**
* Chỉ khả dụng trên **phiên bản app > 4.2.0**
* Chỉ hoạt động trên **thiết bị và mạng hỗ trợ IPv6**
* Cho phép tạo tối đa **500 địa chỉ IPv6** active
* Địa chỉ IPv6 chỉ có hiệu lực trong **vòng đời của ứng dụng**. Khi ứng dụng đóng, tất cả IPv6 sẽ chuyển sang trạng thái _Inactive_ và không thể tiếp tục sử dụng
* Trong một vòng đời, có thể dùng nhiều địa chỉ IPv6 để đăng nhập nhiều tài khoản trên cùng thiết bị khi tài khoản phù hợp với yêu cầu (phiên bản, gói)
* Trạng thái IP: **Active**: IPv6 đang hoạt động, có thể dùng để tạo profile, **Inactive**: IPv6 đã bị vô hiệu hóa, không thể sử dụng
* Khi hết hạn gói thì vẫn dùng được IPV6 đã tạo trước đó chỉ không tạo mới được

### II. Tính năng



<figure><img src="../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>



Trong giao diện **IP V6 Manager**, người dùng có các nút chức năng sau:

1\. **Create IPv6**

* Chức năng: Tạo mới địa chỉ IPv6
* Người dùng có thể chọn số lượng IPv6 muốn tạo (tối đa 500 trong một lần)
* Sau khi tạo, địa chỉ sẽ hiển thị trong danh sách cùng với thông tin

2\. **Delete**

* Chức năng: Xóa địa chỉ IPv6 đã chọn trong danh sách
* Lưu ý: Khi xóa, địa chỉ IPv6 sẽ bị **xóa vĩnh viễn khỏi thiết bị** và không thể khôi phục

3\. **Rotate**

* Chức năng: thay đổi địa chỉ IP andress bạn đã chọn
* Khi bấm nút này, hệ thống sẽ tạo ra một IP andress mới thay thế cho IP andress đang dùng, giúp làm mới khi chạy profile.

4\. **Timer**

* Chức năng: Đặt hẹn giờ để xoay địa chỉ IP andress tự động khi không muốn xoay thì phải stop timer
* Người dùng có thể nhập số phút tùy chọn (ví dụ: 5 phút, 10 phút, 30 phút).
* Khi đến thời gian đã thiết lập, hệ thống sẽ tự động xoay IP andress

5\. **Stop Timer**

* Chức năng: Dừng hẹn giờ xoay IP andress
* Sử dụng khi không muốn hệ thống tự động xoay IP andress nữa và muốn giữ nguyên IP andress hiện tại

6\. **Refresh**

* Chức năng: Làm mới (reload) lại danh sách IPv6 đang hiển thị trên màn hình
* Giúp cập nhật trạng thái mới nhất của IP.

***

### III.Các bước tạo mới IPv6 và sử dụng IPv6

* Khi xóa một IPv6, địa chỉ đó sẽ bị **xóa vĩnh viễn khỏi thiết bị** và không thể khôi phục.



Bước 1: Trước khi tạo mới IPV6 vào virus & threat protecion settings -> chọn manager settings

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>



Bước 2: Chọn add or remove exclusions

<figure><img src="../../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

Bước 3: Chọn add an exclusions -> chọn folder

<figure><img src="../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

Bước 4: Chọn đường dẫn folder eg: C:\Users\hachitech solution\\.hidemium\_4

<figure><img src="../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

Bước 5: Mở app -> vào màn hình IP V6 Manager -> create IPv6

<figure><img src="../../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

Bước 6: Nhập số lượng IP muốn tạo -> chọn create

<figure><img src="../../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

Bước 7: chọn đồng ý

<figure><img src="../../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

Bước 8: Hiển thị danh sách và quản lý IP tại màn này

<figure><img src="../../.gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>

Bước 9: Các màn hình sử dụng IPV6 với profile

<figure><img src="../../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

![](https://i.postimg.cc/htwG7jdX/b10.png)

![](https://i.postimg.cc/0yrQQmbg/b11.png)
