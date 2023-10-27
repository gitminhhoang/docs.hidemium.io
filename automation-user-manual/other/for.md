# For

This node allows you to choose the type of loop: with data, with elements, or to repeat a certain action or process a certain number of times in the script.\
\
Nút này cho phép bạn chọn loại vòng lặp: với dữ liệu, với các phần tử hoặc lặp lại một hành động nhất định hoặc xử lý một số lần nhất định trong script.

### For Data

<figure><img src="../../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

| parameter      | illustrate                                            |
| -------------- | ----------------------------------------------------- |
| For from value | Nhập giá trị là số hoặc chọn biến chứa giá trị hợp lệ |
| For to value   | Nhập giá trị là số hoặc chọn biến chứa giá trị hợp lệ |

Giá trị của _For to value_ phải lớn hơn giá trị của _For from value_.

{% file src="../../.gitbook/assets/For_data.txt" %}

### For Elements

<figure><img src="../../.gitbook/assets/image (2) (1).png" alt=""><figcaption></figcaption></figure>

**Selector element :** Nhập CSS selector, chẳng hạn như #email, \[data-results-grid-container]>li

**Content :** Chọn kiểu trích xuất, bao gồm:

* Text: Trích xuất text của Select element
* HTML: Trích xuất đoạn HTML của Select element
* Attribute: Trích xuất thuộc tính của của Select element, nhập thuộc tính cần trích xuất.

**Loop object save to:** Lưu các thành phần trang web được trích xuất trong mỗi vòng lặp thành các biến.

**Loop index save to:** Lưu vị trí của thành phần trang web được trích xuất trong mỗi vòng lặp vào một biến. Lưu ý rằng vị trí (index) của thành phần trang web trong vòng lặp bắt đầu từ 0.

{% file src="../../.gitbook/assets/for_element.txt" %}

### For Times

Khi chọn For Times, bạn có thể nhập số lần lặp mà bạn mong muốn.

<figure><img src="../../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

| parameter          | illustrate                                                                                                                                                           |
| ------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Times              | Nhập số lần lặp mong muốn                                                                                                                                            |
| Loop index save to | Lưu vị trí của thành phần trang web được trích xuất trong mỗi vòng lặp vào một biến. Lưu ý rằng vị trí (index) của thành phần trang web trong vòng lặp bắt đầu từ 1. |

{% file src="../../.gitbook/assets/For_times.txt" %}
