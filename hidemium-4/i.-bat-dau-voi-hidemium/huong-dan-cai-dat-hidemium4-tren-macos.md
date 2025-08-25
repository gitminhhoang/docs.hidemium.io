# Hướng dẫn cài đặt Hidemium4 trên macOS

1. **Download Hidemium4 bản mới nhất dành cho Mac**

<figure><img src="../../.gitbook/assets/image (5) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

**2. Thực hiện cài đặt app**

B1: Sau khi download thành công, bạn thực hiện mở file .dmg

B2: Mở file .dmg và kéo biểu tượng Hidemium4 vào thư mục “Applications”



<figure><img src="https://docs.hidemium.io/~gitbook/image?url=https%3A%2F%2F699023340-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FiEhmc20xmuwcG5ThYMWS%252Fuploads%252FctNkmyb0IXmjhZkFjrYt%252Fimage.png%3Falt%3Dmedia%26token%3D96d04977-f29f-4ed9-bc28-d748b9b63af3&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=466e06e5&#x26;sv=1" alt=""><figcaption></figcaption></figure>



Lưu ý: Sau khi kéo biểu tượng Hidemium4 vào thư mục “**Applications**”, nếu xuất hiện popup này thì click vào **Replace** . Nếu là máy chưa cài Hidemium lần nào, hoặc đã bị gỡ khỏi máy thì sẽ không có popup này hiện lên.

<figure><img src="../../.gitbook/assets/Screenshot_1 (3).png" alt=""><figcaption></figcaption></figure>



B3: Sau khi hoàn thành xong bước 2, bạn đừng vội mở app. Bạn mở Terminal, Copy và dán dòng lệnh sau vào**Terminal** nhấn **Enter:**

```
xattr -cr /Applications/Hidemium4.app


```

<figure><img src="../../.gitbook/assets/image (6) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>



Lưu ý: Đối với những thiết bị chưa từng cài đặt hidemium 4, thì chỉ cần chạy xong lệnh **xattr -cr /Applications/Hidemium4.app** là các bạn có thể mở App và và sử dụng. Còn các máy mà trước đó đã từng cài đặt App Hidemium 4 thì cần chạy tiếp lệnh bên dưới



Sau đó bạn chạy tiếp lệnh:\
**Lưu ý: Các bạn nhớ thay ten\_may bằng tên máy của các bạn**

```
chmod -R +x /Users/ten_may/.hidemium_4
```

![](http://education.hidemium.io/wp-content/uploads/2024/08/Screenshot_1.png)

B4: Sau đó bạn có thể mở app Hidemium4 và dùng bình thường

