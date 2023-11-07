# Element exists

Chức năng này cho phép bạn kiểm tra xem phần tử bạn chọn có tồn tại hay không.&#x20;

Nếu phần tử không tồn tại thì nó sẽ đi ra đường màu đỏ:

<figure><img src="../../.gitbook/assets/image (41).png" alt=""><figcaption></figcaption></figure>

Nếu phần tử tồn tại thì nó sẽ đi ra đường màu xanh:

<figure><img src="../../.gitbook/assets/image (40).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/integrate.PNG" alt=""><figcaption></figcaption></figure>

| parameter       | illustrate                                                                                                                                                                                |
| --------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Select element  | Nhập CSS selector, chẳng hạn như #email, #global-enhancements-search-query                                                                                                                |
| Element order   | Chọn thành phần nào của trong web                                                                                                                                                         |
| Visible         | Nếu để true thì phần tử mà bạn chọn phải visible thì node mới chạy ra đường xanh. Còn nếu để false thì chỉ cần có phần tử đó (không quan tâm đến visible) thì node sẽ chạy ra đường xanh. |
| Timeout waiting | Thời gian chờ đợi tối đa. Ví dụ: 30000: Nếu bước này không được thực hiện thành công trong vòng 30 giây thì bước tiếp theo sẽ được thực hiện trực tiếp.                                   |

{% file src="../../.gitbook/assets/Element exists.txt" %}
