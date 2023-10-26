# Write file

The button allows you to edit your file by overwriting, Append to the side with special characters, or write on new lines. To add a file, enter its full path or upload it from your device in the designated "file path" section. Then, choose the data you want to include in the file based on the variable you set up in the orange Variables node and select the file format. Once you've made your selections, additional options will appear for specifying the location of the data you entered.&#x20;

As an example, let's say I have a file containing multiple Google accounts that need to be logged in. To mark these accounts, I can use the "write file" function. In the orange "Variable" node, I will set the "Login" variable with a value of "Complete" and the "Logout" variable with a value of "Decline". Next, I will use the Node "Element Exits" function to check if the account has been logged in. If an account has been successfully logged in, I will use the "write file" function to mark it as "Complete" (by selecting the login variable) and then indicate the account. If an account has not been logged in, I will use the "write file" function to mark it as "Decline" (by selecting the logout variable). Or you can mark which profile matches which data line in your file when using this feature and select the variable "PROFILE\_NAME"\


Nút này cho phép bạn chỉnh sửa tập tin của mình bằng cách ghi data xử lý trong script ra ngoài file, Thêm ký tự đặc biệt nếu bạn muốn data đó vào bên cạnh data cũ hoặc viết thêm dòng mới . Để thêm tệp, hãy nhập đường dẫn đầy đủ của tệp hoặc tải tệp lên từ thiết bị của bạn trong phần "file path" được chỉ định. Sau đó, chọn dữ liệu bạn muốn đưa vào tệp dựa trên biến bạn thiết lập trong nút Biến màu cam và chọn định dạng tệp. Khi bạn đã thực hiện các lựa chọn của mình, các tùy chọn bổ sung sẽ xuất hiện để chỉ định vị trí của dữ liệu bạn đã nhập.&#x20;

Ví dụ: giả sử tôi có một tệp chứa nhiều tài khoản Google cần phải đăng nhập. Để đánh dấu các tài khoản này, tôi có thể sử dụng chức năng "Write file". Trong nút "Variable" màu cam, tôi sẽ đặt biến "Đăng nhập" có giá trị "Hoàn thành" và biến "Đăng xuất" có giá trị "Từ chối". Tiếp theo, tôi sẽ sử dụng chức năng "Element Exits" của Node để kiểm tra xem tài khoản đã được đăng nhập chưa. Nếu tài khoản đã đăng nhập thành công, tôi sẽ sử dụng chức năng "Write file" để đánh dấu là "Hoàn thành" (bằng cách chọn biến đăng nhập) và sau đó chỉ ra tài khoản. Nếu tài khoản chưa đăng nhập, tôi sẽ sử dụng chức năng "ghi file" để đánh dấu là "Từ chối" (bằng cách chọn biến đăng xuất). Hoặc bạn có thể đánh dấu profile nào khớp với dòng dữ liệu nào trong file của mình khi sử dụng tính năng này và chọn biến "PROFILE\_NAME"



<figure><img src="../../.gitbook/assets/Write file (1).PNG" alt=""><figcaption></figcaption></figure>

| parameter                       | illustrate                                          |
| ------------------------------- | --------------------------------------------------- |
| File path                       | Đường dẫn tệp để ghi dữ liẹu                        |
| Select input data from variable | Chọn dữ liệu đầu vào từ biến                        |
| Selector type                   | Chọn định dạng tệp: TXT, CSV, JSON                  |
| Select write mode: Overwrite    | Ghi đè lên dữ liệu trước đó                         |
| Select write mode: Append       | Ghi thêm vào tệp, ghi xuống dòng mới hoặc cùng dòng |



{% file src="../../.gitbook/assets/Write file.txt" %}
