# Vì sao CreepJS thường chỉ hiện RAM 4GB hoặc 8GB trong fingerprint?

**1. Giá trị deviceMemory API trong trình duyệt bị giới hạn cứng**

* Trình duyệt (Chromium/Chrome/Brave) khi expose navigator.deviceMemory không trả ra số RAM thật, mà chỉ expose một giá trị rút gọn, vì lý do bảo mật fingerprinting (theo chuẩn W3C Privacy).
* Các giá trị hợp lệ Chromium expose chỉ là:\
  0.25, 0.5, 1, 2, 4, 8, 16
* Nghĩa là bạn có RAM 12GB, 24GB, hay 64GB, thì navigator.deviceMemory cũng chỉ hiện 4, 8 hoặc 16 thôi.
* Trong thực tế:
  * RAM 2GB trở xuống → 2
  * RAM 3GB–6GB → 4
  * RAM 7GB–12GB → 8
  * RAM 13GB+ → 16

**2. CreepJS và các tool fingerprint chỉ lấy từ navigator.deviceMemory**

CreepJS chỉ đơn giản gọi:\
\
javascript\
CopyEdit\
navigator.deviceMemory

* Và không thể đo RAM thực tế bằng cách khác, vì JS sandbox không cho phép đo thẳng hệ thống.
* Nếu user dùng máy yếu → CreepJS hiển thị 4GB.
* Nếu user dùng máy trung → CreepJS hiển thị 8GB.
* Nếu máy cực mạnh → CreepJS hiển thị 16GB.

**3. Vì sao thường xuyên chỉ thấy 4GB hoặc 8GB, hiếm thấy 16GB?**

* Đa số người dùng phổ thông:
  * Laptop/máy tính → 4–8GB RAM (theo thị trường phổ biến).
* Rất ít người dùng Chrome trên máy 16GB trở lên.
* Kết quả: Big fingerprint data cũng skew về 4GB/8GB.

**4. Trong stealth browser thì cần làm gì với deviceMemory?**

&#x20;Random theo phân bố tự nhiên:

| deviceMemory | Xác suất Gợi Ý |
| ------------ | -------------- |
| 4GB          | 55%            |
| 8GB          | 40%            |
| 16GB         | 5%             |
