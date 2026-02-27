# Hướng dẫn sử dụng SX proxy, TM proxy và Kiot proxy trong hidemium

### **I. Hướng dẫn sử dụng SX proxy với Hidemium**

1. Cách lấy API key của SX proxy

Bước 1: Các bạn truy cập trang [https://my.sx.org/](https://my.sx.org/) . Sau đó thực hiện đăng nhập tài khoản.

Bước 2: Sau khi đăng nhập thành công, các bạn vào phần API Documentation. Tại đây các bạn sẽ thấy API key của mình. Các bạn cần copy API key để có thể sử dụng trong Hidemium.

![](http://education.hidemium.io/wp-content/uploads/2025/08/photo_2025-08-25_14-41-29.jpg)

2\. Hướng dẫn sử dụng SX proxy trên Hidemium:

Bước 1:  Tại app hidemium, các bạn chọn Proxy config  -> Create config.

&#x20;

![](http://education.hidemium.io/wp-content/uploads/2025/08/photo_2025-08-25_14-54-26.jpg)

&#x20;

Bước 2: Tại popup Create config -> nhập tên của config -> Chọn type là API -> Chọn SX proxy -> Nhập API key của SX proxy.  Sau khi nhập API xong, các bạn có thể click vào Verify để kiểm tra xem API key có hợp lệ không. Sau đó các bận click Submit để lưu lại.

![](http://education.hidemium.io/wp-content/uploads/2025/08/photo_2025-08-25_14-55-30.jpg)

&#x20;

Bước 3: sau khi tạo xong config, các bạn muốn sử dụng proxy thì có thể thêm proxy vào profile như sau:

* Click vào Add profile để tạo profile mới

![](http://education.hidemium.io/wp-content/uploads/2025/08/photo_2025-08-25_14-56-15.jpg)

&#x20;

* Tại màn new, các bạn chọn phần proxy -> Chọn your proxy -> click chọn proxy type. Tại đây các bạn chọn đúng config của SX proxy mà bạn đã tạo ở Bước 2.

&#x20;

![](http://education.hidemium.io/wp-content/uploads/2025/08/photo_2025-08-25_14-57-03.jpg)

&#x20;

* Tại đây, sẽ có 2 tab đó là Proxy selected và List proxy. Proxy selected sẽ hiển thị proxy mà bạn đã chọn để sử dụng. Còn tab List proxy sẽ hiển thị danh sách proxy có sẵn của bạn.

![](http://education.hidemium.io/wp-content/uploads/2025/08/photo_2025-08-25_14-57-54.jpg)

&#x20;

* Nếu bạn muốn chọn proxy có sẵn trong danh sách, các bạn Click chọn tab List proxy và thực hiện chon proxy mà bạn muốn.

![](http://education.hidemium.io/wp-content/uploads/2025/08/photo_2025-08-25_14-58-51.jpg)

&#x20;

* Nếu như không muốn chọn proxy có sẵn, bạn có thể thực hiện tạo 1 proxy mới bằng cách click và button Create New Proxy để tạo 1 proxy mới, tại đây các bạn có thể tạo proxy mong muốn.

![](http://education.hidemium.io/wp-content/uploads/2025/08/photo_2025-08-25_14-59-51.jpg)

* Sau khi tạo proxy xong -> bạn có thể click vào button Check proxy để check proxy , sau đó click button Create profile

&#x20;

![](http://education.hidemium.io/wp-content/uploads/2025/08/photo_2025-08-25_15-00-38.jpg)

Như vậy là bạn đã hoàn thành việc tạo profile với config SX proxy.

&#x20;

### &#x20;

### II.**Hướng dẫn sử dụng SX proxy với Hidemium**

Bước 1: Vào màn Proxy Config -> Chọn Create Config  -> Điền tên config -> Chọn type là API -> Chọn TM proxy -> Chọn Submit

![](http://education.hidemium.io/wp-content/uploads/2025/08/Screenshot_1-1.png)

&#x20;

Bước 2: khi muốn sử dụng TM proxy cho profile, khi tạo profile mới, chọn tab Proxy -> chọn Your proxy -> tại proxy type chọn config TM proxy mới tạo

![](http://education.hidemium.io/wp-content/uploads/2025/08/Screenshot_2.png)

&#x20;

* Chọn Create new Proxy: Nhập API key vào và thực hiện create (lưu ý mỗi api key nên chỉ thêm vào 1 profile)

![](http://education.hidemium.io/wp-content/uploads/2025/08/photo_2025-08-25_15-27-35.jpg)

&#x20;

* nếu bạn không muốn tạo proxy mới, mà dùng proxy hiện tại của api key thì các bạn chọn **Get proxy**  -> sau đó nhập **API key** vào để lấy proxy của API key đó.

&#x20;

![](http://education.hidemium.io/wp-content/uploads/2025/08/Screenshot_3-2.png)

&#x20;

### III. Hướng dẫn sử dụng kiot proxy với Hidemium

Bước 1: đầu tiên các bạn tạo 1 config kiot proxy:![](http://education.hidemium.io/wp-content/uploads/2025/08/Screenshot_4.png)

Bước 2: Tạo mới proxy kiot

* Cách 1: Khi muốn tạo proxy mới thì chọn Create new proxy sau đó nhập API key vào có thể tạo nhiều proxy cùng lúc tại change proxy và có thể sử dụng cho nhiều profile

![](https://i.postimg.cc/pXCFJ0mc/Screenshot-6.png)

* Cách 2: thêm mới 1 proxy tại màn new profile

![](https://i.postimg.cc/XvRL62kM/Screenshot-7.png)

Bước 3:

* Cách 1: khi muốn sử dụng Kiot proxy cho profile, khi tạo profile mới, chọn Proxy -> chọn Your proxy -> tại proxy type chọn config Kiot proxy mới tạo -> thêm mới proxy

![](https://i.postimg.cc/ZqcFBTrd/Screenshot-5.png)

* hoặc có thể sử dụng list proxy đã thêm trước đó tại list proxy

![](https://i.postimg.cc/4NWg5tXT/Screenshot-4.png)

* Cách 2: khi muốn sử dụng Kiot proxy update cho nhiều profile chọn profile muốn update -> chọn proxy

![](https://i.postimg.cc/66DRQ7kX/Screenshot-3.png)

* chọn proxy config -> chọn config đã tạo trước đó -> có thể tạo mới prory hoặc chọn proxy tại danh sách proxy đã thêm trước đó

![](https://i.postimg.cc/hjTy5Fxg/Screenshot-2.png)

Video hướng dẫn sử dụng kiot proxy: [https://streamable.com/1ghbc3](https://streamable.com/1ghbc3)
