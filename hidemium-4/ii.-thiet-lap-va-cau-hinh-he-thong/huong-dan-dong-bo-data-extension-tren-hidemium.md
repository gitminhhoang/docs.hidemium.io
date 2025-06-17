# Hướng dẫn đồng bộ data extension trên Hidemium

Các extension cài ngoài từ store sẽ không đc đồng bộ vì vậy hãy sử dụng tính năng extension của hidemium.

Để extension được đồng bộ thì cần phải giữ được extension id

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>



Các extension muốn đồng bộ được thì cần phải có key, các extension từ ngoài store sẽ không có key nên các bạn cần bổ sung key vào trước khi import extension vào hidemium để sử dụng. Sau đây là hướng dẫn chi tiết:

Bước 1: Ví dụ bạn muốn import extension Ronin Wallet vào hidemium, tại chrome store bạn tìm kiếm extension Ronin, sau đó tải file zip của extension đó về máy, mà muốn tải file zip của extension thì bạn cần phải cài thêm extension **CRX Extractor/Downloader**

<figure><img src="../../.gitbook/assets/image (1) (1).png" alt=""><figcaption></figcaption></figure>



Sau đó bạn chọn Download as ZIP:

<figure><img src="../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>



Bước 2: Trước đó bạn hãy vào trang này để gen key : https://itero.plasmo.com/tools/generate-keypairs

Click vào Generate KeyPairs để gen key. Nếu có key thì extension sẽ giữ nguyên được id nếu không có key extension sẽ bị đổi key khi đường dẫn thay đổi vì vậy cần bổ sung key cho extension.  Sau khi click Generate KeyPairs, trang sẽ show key ra, bạn thực hiện copy Public Key

<figure><img src="../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

&#x20;

Bước 3: Sau khi tải file zip của extension về máy, bạn hãy giải nén file ra. Sau đó tìm đến file **manifest.json ,** thực hiện thêm key vào trong file manifest.json, nếu extension nào có key sẵn rồi thì không cần bổ sung key, có thêm import vào trong Hidemium để sử dụng luôn:

![](http://education.hidemium.io/wp-content/uploads/2025/06/Screenshot_7.png)



<figure><img src="../../.gitbook/assets/image (200).png" alt=""><figcaption></figcaption></figure>

Bước 4: Sau khi thêm key vào xong, bạn lưu lại và nén lại extension thành file zip, sau đó import vào hidemium để sử dụng bình thường.
