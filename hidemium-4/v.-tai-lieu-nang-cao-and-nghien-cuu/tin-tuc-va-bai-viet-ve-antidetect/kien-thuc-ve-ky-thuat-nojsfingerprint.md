# Kiến thức về Kỹ thuật NojsFingerprint

Hôm nay mình sẽ giới thiệu cho các bạn một kỹ thuật check fingerprint **không thông qua js và cookie** đó chính là noscriptfingerprint.

Vậy noscriptfingerprint là gì? Nó được định nghĩa là: cách nhận dạng trình duyệt mà không cần sử dụng cookie hoặc lưu trữ dữ liệu. Được tạo bằng các thuộc tính như ngôn ngữ và phông chữ được cài đặt, vân tay của bạn vẫn giữ nguyên ngay cả khi trình duyệt của bạn ở chế độ ẩn danh.

Kỹ thuật này sẽ dựa vào css và HTTP header để kiểm tra các phần tử, ta có ví dụ sau đây:

![](<../../../.gitbook/assets/image (190).png>)\


Mỗi loại trình duyệt máy tính chúng ta sẽ có những thông số:

* **Font**: Font dùng trong máy tính
* **Media queries**: cho phép bạn áp dụng các kiểu CSS tùy thuộc vào loại chung của thiết bị (chẳng hạn như in so với màn hình) hoặc các đặc điểm khác như độ phân giải màn hình hoặc chiều rộng khung nhìn của trình duyệt.
* **Truy vấn HTTP Header**: Language, Accepted encoding, Accept header for web page…

Dựa vào đây chúng ta thấy:

* Khi thay đổi trình duyệt => Media queries thay đổi => Mã băm thay đổi
* Khi thay đổi kích thước màn hình => Media queries thay đổi => Mã băm thay đổi
* Khi thay đổi font chữ => Font thay đổi => Mã băm thay đổi
* Khi thay đổi hệ điều hành => Font thay đổi => Mã băm thay đổi
* Khi thay đổi ngôn ngữ trình duyệt => Language header => Mã băm thay đổi\
  …

Dựa vào đây chúng ta có thể thấy nếu 1 số hệ thống khó tính họ có thể áp dụng điều này vào máy học để phát hiện ra rằng nếu chúng ta dùng không đúng bộ cấu hình mà trình duyệt đưa ra rất có thể chúng ta đang nằm trong vùng rủi do. Vì vậy nhận thức của chúng ta luôn phải biết rằng khi thay đổi resolution screen hoặc font chữ thì 2 trình duyệt anti detect phải trả về 2 mã băm khác nhau.
