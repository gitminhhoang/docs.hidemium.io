# COPY NHƯNG PASTE RA MỚI XUẤT HIỆN TEXT ?



![](https://i.imgur.com/AZhQtqh.png)

Rất nhiều trường hợp trang web xuất hiện button ” **Click to copy**” tức là phải click vào đó thì mới copy được nội dung chứ mình cũng không nhìn thấy trước nội dung là gì để thực hiện thao tác GET TEXT ( như ví dụ bên trên) . Thì ở trong trường hợp này, nếu bạn muốn lấy được nội dung đó thì cần thực hiện các node sau trong automation :

![](https://i.imgur.com/qm3zCic.png)

&#x20;

Dùng node **CLICK** vào element copy đó. Sau đó dùng **NEW TAB** mở tab : https://anotepad.com/

![](https://i.imgur.com/0PrStcb.png)

Sau đó dùng node **PRESS KEY** để làm thao tác **control v** để paste nội dung vào trang note

![](https://i.imgur.com/rqFWHWw.png)

&#x20;

Dùng GET VALUE để script tự động lấy được nội dung text trong ô input này

![](https://i.imgur.com/oHdIb2U.png)

&#x20;

kết quả khi chạy script sẽ được LOG như này nhé : Vậy là chúng ta đã lấy thành công đoạn link mà ẩn dấu trong phần Click to copy ban đầu.

&#x20;

![](https://i.imgur.com/roOkbDC.png)

&#x20;
