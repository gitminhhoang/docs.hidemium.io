# File choose event

File choose event được thực hiện khi page có sự kiện chọn file được kích hoạt. Và sự kiện chọn file đó không có thẻ **Input** với **type="file"** thì bạn có thể sử dụng node file choose event.&#x20;

Lưu ý node File choose event này nên để đằng trước node click vào button upload.

<figure><img src="../../.gitbook/assets/File choose event.png" alt=""><figcaption></figcaption></figure>

| parameter            | illustrate                                                                                                                                                                                                                      |
| -------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Choose selector type | <p>Local file: chọn một tệp cục bộ để tải lên một thư mục.<br>Folder file random: chọn một thư mục và tải lên ngẫu nhiên một tệp trong thư mục.<br>Network file: để tải lên tệp mạng, hãy nhập URL bắt đầu bằng http/https.</p> |
| Timeout waiting      | Thời gian chờ đợi tối đa. Ví dụ: 30000. Nếu bước này không được thực hiện thành công trong vòng 30 giây thì bước tiếp theo sẽ được thực hiện trực tiếp.                                                                         |

{% file src="../../.gitbook/assets/File choose event.txt" %}
