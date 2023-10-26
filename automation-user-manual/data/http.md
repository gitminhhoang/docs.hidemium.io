# HTTP

&#x20;This node can be challenging, especially for those with limited knowledge of HTTP. However, having a good understanding of HTTP will make it easier to use. In essence, this HTTP sends requests to the API using either the GET or POST method and displays the response in the tabs below.\
\
Node này có thể là một node khó, đặc biệt đối với những người có kiến ​​thức hạn chế về HTTP. Tuy nhiên, hiểu rõ về HTTP sẽ giúp sử dụng dễ dàng hơn. Về bản chất, HTTP này gửi yêu cầu tới API bằng phương thức GET hoặc POST và hiển thị phản hồi trong các tab bên dưới.



<figure><img src="../../.gitbook/assets/http1.jpg" alt=""><figcaption></figcaption></figure>





| parameter      | illustrate                                                                                                                                                                                                                                                                                                                                                  |
| -------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Enter url      | có tác dụng định danh các nguồn tài nguyên được yêu cầu bởi khách hàng, người dùng và bắt buộc phải có dấu “`/`”.                                                                                                                                                                                                                                           |
| Request method | Gồm 2 method là GET và POST                                                                                                                                                                                                                                                                                                                                 |
| Headers        | Yếu tố thứ hai góp phần làm hình thành HTTP Request đó là các header hay tiêu đề. Thông tin được bổ sung sẽ truyền tải giữa cả máy chủ và máy khách, chẳng hạn như cookie, thông tin về ủy quyền, tác nhân người dùng… Tương tự một HTTP Request, header sẽ phân biệt chữ thường và chữ hoa, theo sau đó là dấu “`.`” và một giá trị.                       |
| Body           | Khi chọn method là POST sẽ hiển thị Body. Máy chủ dùng nội dung thư để cung cấp những thông thông tin cần thiết nhất đến với máy khách. Massage body có chứa các dòng yêu cầu, thông tin, dòng trống, tiêu đề, và nội dung. Trong đó, yếu tố nội dung sẽ tùy chọn. Không phải tất cả các yêu cầu đều có nội dung nhưng sẽ dùng POST để phân phối tải trọng. |
| Cookies        | Cookie **HTTP** (cookie web, cookie trình duyệt) là một đoạn dữ liệu nhỏ mà máy chủ gửi đến trình duyệt web của người dùng. Trình duyệt có thể lưu trữ cookie và gửi nó trở lại cùng một máy chủ với các yêu cầu sau này. Thông thường, cookie HTTP được sử dụng để biết liệu hai yêu cầu có đến từ cùng một trình duyệt hay không                          |

{% file src="../../.gitbook/assets/Http.txt" %}
