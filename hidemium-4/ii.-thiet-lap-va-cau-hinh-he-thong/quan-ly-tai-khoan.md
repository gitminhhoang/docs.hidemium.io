---
description: Tài khoản nền tảng
---

# Quản lý tài khoản

#### Một số lưu ý nhỏ:

* Hiện tại chỉ **core 143 chromium**, **fire fox 144, 145, 146** hỗ trợ chức năng account này
* Cloud và local sẽ sử dụng riêng danh sách account, payment, andress
* Khi thêm tài khoản trong **màn hình Profile**, tài khoản đó **sẽ không được thêm** vào **màn hình Platform Account**
* Khi chỉnh sửa tài khoản trong **màn hình Platform Account**, **tất cả các Profile** đang sử dụng tài khoản đó **đều sẽ được cập nhật theo**
* Khi chỉnh sửa tài khoản trong **màn hình Profile**, thông tin tài khoản ở **màn hình Platform Account sẽ không thay đổi**
* Giới hạn thêm Account, Payment, Andress giới hạn thêm vào profile cloud theo các khác nhau: **Basic: 5, Advanced: 20, Premium: 50, Businness:200, các gói local không giới hạn Account,** **Payment hoặc Andress** không phân biệt tag.
* Chức năng hiện chưa áp dụng đối với **import, export, move all profile cloud to local**

#### **I. Account**

&#x20;    **Chức năng tài khoản nền tảng của Hidemium** cho phép người dùng thêm nhiều tài khoản từ các nền tảng khác nhau và nhanh chóng gán chúng cho hồ sơ (profile) được chỉ định nhằm nâng cao hiệu quả quản lý. Trên giao diện Account, nhấn nút “Add Account” ở góc trên bên phải để thêm tài khoản mới. Bạn có thể lưu các thông tin như: URL nền tảng (bắt buộc), tên đăng nhập, mật khẩu, mã 2FA và ghi chú. Màn **Platform Account** gồm các button:

* **Add account:** Thêm account mới
* **Delete all:** Xóa các tài khoản. Chỉ xóa tài khoản, các profile đang sử dụng sẽ không bị thay đổi
* **Delete all related data:** Xóa tài khoản và xóa khỏi tất cả profile đang liên kết.

![](https://i.postimg.cc/dt09X6qY/Screenshot-3.png)

**Thêm 1 tài khoản:**

1. **Intelligent Recognition:** Bạn cần nhập thông tin tài khoản theo format

Account:password:2fa{note} Ví dụ bạn có thể nhập như sau: email@gmail.com:123123:ABCD123123{Đây là note} hoặc nếu bạn không có 2fa hoặc không muốn thêm note thì chỉ cần [email@gmail.com:123123 ](mailto:email@gmail.com:123123)cũng được. Sau khi nhập ở đây, hệ thống sẽ tự fill vào các trường bên dưới, sau đó bạn chỉ cần chọn nền tảng (platform) và ấn tạo.

2. **Platform:** Chọn nền tảng tài khoản.
3. **Account:**&#x4E;hập account của tài khoản, có thể là email, sđt, username ……
4. **Password:**&#x4E;hập pass của account
5. **2FA:**&#x4E;hập 2FA của tài khoản này sẽ được dùng tại extensions hidemium để lấy code luôn tại hồ sơ đã thêm

![](https://i.postimg.cc/15ZQQJyQ/Screenshot-1.png)

2. **Note:**&#x4E;hập note, giới hạn 500 kí tự
3. **Save & Add more:**&#x4B;hi click vào đây, tài khoản sẽ được tạo, và vẫn giữ nguyên ở màn này để bạn có thể thêm tài khoản khác
4. **Create:**&#x4B;hi click vào đây, tài khoản sẽ được tạo và màn hình sẽ quay lại màn danh sách.

![](https://i.postimg.cc/Zn0mQPkJ/Screenshot-4.png)

**Thêm nhiều tài khoản:**

1. **Account Information:** Điền thông tin tài khoản theo format, mỗi tài khoản 1 dòng. Tối đa 500 dòng
2. **Platform:** Chọn nền tảng tài khoản
3. **Parse:** Khi click vào đây, các tài khoản sẽ được fill xuống bản **Parsed Account** bên dưới
4. **Save & Add more:**&#x4B;hi click vào đây, tài khoản sẽ được tạo, và vẫn giữ nguyên ở màn này để bạn có thể thêm tài khoản khác
5. **Create:**&#x4B;hi click vào đây, tài khoản sẽ được tạo và màn hình sẽ quay lại màn danh sách
6. **Clear:** Khi click ở đây, tất cả các tài khoản ở bảng **Parsed Account** sẽ bị xóa
7. **Parsed Account:** Danh sách account được fill bởi **Parsed Account** bên trên.

![](https://i.postimg.cc/cHvZ9MGd/Screenshot-5.png)

**Hướng dẫn thêm các tài khoản vào profile:**

B1: Tại màn profile, click để thêm account vào profile.

![](https://i.postimg.cc/d07SgW3b/Picture2.png)

Tại đây bạn có thể thêm tài khoản mới hoặc chọn từ danh sách Tài khoản nền tảng

![](https://i.postimg.cc/yNwrKFSD/Picture3.png)

B2: sau khi thêm account vào profile xong, mở profile lên vào kiểm tra

![](https://i.postimg.cc/9MZgQrG9/Picture4.png)

#### **II. Payment và Andress tương tự như Accout**

```
```
