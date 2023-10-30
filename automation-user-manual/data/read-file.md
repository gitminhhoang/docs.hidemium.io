# Read file

This is an important node. To input your data, upload a text file. You can choose to arrange the data line by line or separated by a special character. If you select the latter option, you can also specify whether the script should randomly select certain lines or read each line in order and delete them as they are processed. Alternatively, you can leave these options blank  for sequential processing of each line without deletion, select the appropriate option above. When setting variables to map values, write the first value of the data, followed by the second value, and so on. For example, if you have Abc123@gmail.com|abc123|Xyz456@gmail.com, the format should be email|pass|recovery mail. Write each line separately, Like this : \
\
Đây là một nút quan trọng. Để nhập dữ liệu của bạn, hãy tải lên một tệp văn bản. Có thể lựa chọn sắp xếp dòng dữ liệu theo dòng hoặc cách nhau bằng ký tự đặc biệt. Nếu bạn chọn tùy chọn thứ hai, bạn cũng có thể chỉ định xem script nên chọn ngẫu nhiên một số dòng nhất định hay đọc từng dòng theo thứ tự và xóa chúng khi chúng được xử lý. Ngoài ra, bạn có thể để trống các tùy chọn này để xử lý tuần tự từng dòng mà không xóa chúng, hãy chọn tùy chọn thích hợp ở trên. Khi đặt biến thành map values, hãy ghi giá trị đầu tiên của dữ liệu, theo sau là giá trị thứ hai, v.v. Ví dụ: nếu bạn có Abc123@gmail.com|abc123|Xyz456@gmail.com thì định dạng phải là email|pass|recovery mail. Viết riêng từng dòng, Như thế này:

<figure><img src="../../.gitbook/assets/Read file.PNG" alt=""><figcaption></figcaption></figure>



| parameter                               | illustrate                                                                                                                                           |
| --------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- |
| Path to the file                        | Đường dẫn tệp                                                                                                                                        |
| Type: Line by line                      | Sắp xếp dữ liệu theo từng dòng từ trên xuống, sau khi đọc hết dòng nào thì sẽ xóa dòng đó khỏi file                                                  |
| Type:  Line by line (with delimiter)    | Khi muốn đọc dữ liệu theo dòng,và dữ liệu cách nhau bởi một dấu phân cách thì bạn có thế chọn cái này.                                               |
| Random                                  | Nếu chọn random, các dòng dữ liệu sẽ được đọc một cách ngẫu nhiêu, và sau khi đọc xong dữ liệu của file sẽ không bị xóa                              |
| Delete line after read                  | Xóa dữ liệu sau khi đọc xong                                                                                                                         |
| Variables map value (Ordering by index) | Nếu dữ liệu của bạn được phân cách bằng một dấu phân cách, bạn hãy nhập dấu phân cách tại đây và điền biến tương ứng với từng phần của dòng dữ liệu. |
| Output variable                         | Lưu các phần tử được trích xuất dưới dạng biến và nhập tên biến                                                                                      |

{% file src="../../.gitbook/assets/read file.txt" %}

{% file src="../../.gitbook/assets/SCRIPT READ FILE.txt" %}
