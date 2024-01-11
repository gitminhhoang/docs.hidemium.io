# File upload

Bạn có thể tải tệp lên trang web mà bạn mong muốn. Các button upload file của trang web cần có thẻ **Input** với **type="file".**&#x20;

Lưu ý có một vài trang web có thể **Input** với **type="file"** nhưng lại có thuộc tính **Display: none** này thì bạn không thể lấy selector của thể input này được, mà bạn phải lấy selector của thẻ **Label** bên trên thẻ **Input.**

<figure><img src="../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/File upload.png" alt=""><figcaption></figcaption></figure>

| parameter        | illustrate                                                                                                                                                                                                         |
| ---------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Select element   | Nhập CSS selector của phần tử cần upload                                                                                                                                                                           |
| Element order    | Chọn các thành phần dựa trên thứ tự chúng xuất hiện trên trang                                                                                                                                                     |
| Path to the file | <p>Local file: chọn một tệp cục bộ để tải lên<br>Folder file random: chọn một thư mục và tải lên ngẫu nhiên một tệp trong thư mục.<br>Network file: để tải lên tệp mạng, hãy nhập URL bắt đầu bằng http/https.</p> |
| Timeout waiting  | Thời gian chờ đợi tối đa. Ví dụ: 30000. Nếu bước này không được thực hiện thành công trong vòng 30 giây thì bước tiếp theo sẽ được thực hiện trực tiếp.                                                            |

{% file src="../../.gitbook/assets/File upload.txt" %}
