# File choose event

File choose event is performed when a page has a file choose event triggered. And that file selection event does not have an **Input** tag with **type="file"**, you can use node file choose event.&#x20;

Note that this **File choose event** should be placed before the **click** .



File choose event được thực hiện khi page có sự kiện chọn file được kích hoạt. Và sự kiện chọn file đó không có thẻ **Input** với **type="file"** thì bạn có thể sử dụng node file choose event.&#x20;

Lưu ý node File choose event này nên để đằng trước node click.

<figure><img src="../../../../.gitbook/assets/File choose event.png" alt=""><figcaption></figcaption></figure>

| parameter            | illustrate                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| -------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Choose selector type | <p>Local file: select a local file to upload to a folder. </p><p>Folder file random: choose a folder and randomly upload a file in the folder. </p><p>Network file: to upload a network file, enter a URL starting with http/https.</p><p></p><p>Local file: chọn một tệp cục bộ để tải lên một thư mục.<br>Folder file random: chọn một thư mục và tải lên ngẫu nhiên một tệp trong thư mục.<br>Network file: để tải lên tệp mạng, hãy nhập URL bắt đầu bằng http/https.</p> |
| Timeout waiting      | <p>Maximum waiting time. For example: 30000. If this step is not performed successfully within 30 seconds, the next step will be performed directly.</p><p></p><p>Thời gian chờ đợi tối đa. Ví dụ: 30000. Nếu bước này không được thực hiện thành công trong vòng 30 giây thì bước tiếp theo sẽ được thực hiện trực tiếp.</p>                                                                                                                                                 |

{% file src="../../../../.gitbook/assets/File choose event.txt" %}
