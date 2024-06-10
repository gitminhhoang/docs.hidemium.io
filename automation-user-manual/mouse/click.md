# Click

### Giới thiệu tổng quan

True to its name, this button is used to automatically click the mouse on the element you select and put it in the "select element" box. \
\
Đúng như tên gọi của nó, nút này dùng để tự động click chuột vào phần tử bạn chọn và cho vào ô “select element”.&#x20;

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

| parameter         | illustrate                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| ----------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Click type        | <p>Left: left click on the selected element Right: right click on the selected element Midle: click on the element of your choice and open it in a new tab. Click down: Click and hold the mouse button at the same time. Click up: Release the mouse button at the element you select.</p><p></p><p>Left: click chuột trái vào phần tử đã chọn<br>Right: click chuột phải vào phần tử đã chọn<br>Midle: click vào phần tử bạn chọn và mở phần tử đó trong một tab mới.                                           Click down: Click đồng thời thực hiện giữ chuột Click up: Thực hiện việc thả chuột tại phần tử mà bạn chọn</p> |
| Button click type | <p>Click: click once on the selected element Double click: double click on the selected element</p><p></p><p>Click: click một lần vào phần tử đã chọn<br>Double click: click đúp vào phần tử đã chọn</p>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Selector          | <p>Enter the CSS selector of the element you want to click on.</p><p></p><p>Nhập CSS selector của phần tử mà bạn muốn thực hiện click</p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Element order     | <p>Which element of the website to choose: Fixed value: select a fixed element Random value: random a random value within a set range</p><p></p><p>Chọn thành phần nào của trang web:<br>Fixed value: chọn một phần tử cố định<br>Random value: random một giá trị ngẫu nhiên trong khoảng đã đặt</p>                                                                                                                                                                                                                                                                                                                            |
| Coordinates       | <p>Enter the x,y coordinates of the element you want to click</p><p></p><p>Nhập tọa độ x,y của phần tử bạn muốn click</p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



### Hướng dẫn sử dụng

For example, if you want to drag components to the artboard as shown below, you can do the following:

Ví dụ bạn muốn kéo các thành phần vào artboard như hình dưới đây thì bạn có thể làm như sau:

<figure><img src="../../.gitbook/assets/Screenshot_1.png" alt=""><figcaption></figcaption></figure>



First, enter the selector of the element you want to drag to the artboard, and select Click down:

Đầu tiên bạn nhập selector của phần tử mà bạn muốn kéo vào artboard, và chọn Click down:

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Right after the click down button, add another click button and enter the selector of the element you want to drop them into, and select Click up:

Ngay sau node click down thì bạn thêm một node click nữa và nhập selector của phần tử mà bạn muốn thả chúng vào, và chọn Click up:

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

And below is the video:

Và dưới đây là video:

{% file src="../../.gitbook/assets/1.mp4" %}

Ví dụ 2: Bạn cũng có thể sử dụng node click để nhấn và giữ chuột:

Khi bạn muốn nhấn và giữ chuột trong một khoảng thời gian thì bạn là như sau:

Bước 1: Khi bạn muốn click để nhấn chuột thì bạn chọn click down, và nhập selector của phần tử mà bạn muốn giữ chuột

<figure><img src="../../.gitbook/assets/image (1) (1).png" alt=""><figcaption></figcaption></figure>

Cũng tại node này bạn nhập thời gian giữ chuột, ví dụ bạn muốn giữ chuột trong 5s thì bạn nhập thời gian vào phần Sleep time trong setting.

Bước 2: Sau đó bạn sử dụng thêm 1 node click nữa để thả chuột. Ở đây bạn chọn click up để thả chuột, bạn cần nhập selector của phần tử như ở bước 1

<figure><img src="../../.gitbook/assets/image (1) (1) (1).png" alt=""><figcaption></figcaption></figure>



Như vậy là bạn đã có thể nhấn và giữ chuột thành công.
