# PHÂN BIỆT DÙNG DROP DOWN SELECTOR.



&#x20;

![](https://i.imgur.com/4ctOsaQ.png) ![](https://i.imgur.com/iOh7pU3.png)

Nhìn vào bức ảnh trên ta có thể thấy đây đều là những button show option chọn dữ liệu đúng không ? Tưởng trừng như sẽ đều dùng chung 1 node để giải quyết vấn đề chọn các option được đưa ra như này, nhưng không, trong đây hoàn toàn là 2 trường hợp dùng node khác nhau, Hidemium sẽ hướng dẫn bạn phân biệt khi nào nên dùng node DROPDOWN SELECTOR và khi nào không nhé.**1. Use case là discord**– Bạn có thể thấy element chọn giá trị ngày tháng năm ở đây chỉ là những thẻ và thuộc tính bình thường, nên ở đây bạn dùng node CLICK như bình thường vào giá trị mà bạn muốn.Ví dụ chọn tháng 7 thì mình sẽ click vào element này.

![](https://i.imgur.com/LICDb8e.png)

**2. Use case là ebay**Nếu như element của các option này là thẻ Select như ảnh dưới đây và có thuộc tính Value thì lúc này ta mới dùng node DROPDOWN SELECTOR

![](https://i.imgur.com/qc8ZyQP.png)

“Như vậy nhập element vào node **Drop-down selector** sẽ là element của thẻ select đó và value nhập vào **Selected value** là số thể hiện trong từng thuộc tính value. Như ảnh dưới đây thì mình nhập value kia là 2, tương đương với trong web show ra value 2 là “” Baseball Long Sleeve T Shirt””

![](https://i.imgur.com/VxNG8Eh.png)

&#x20;

**3. Một tips nâng cao cho mọi người là làm như thế nào để xác định được thẻ select đó có bao nhiêu value, nhỡ đâu value cố định không phải 1 2 3 như trên mà là 7 8 9 thì làm như nào để script tự get được các value và tự chọn value đó.**

Ở phần này mình sẽ sử dụng thêm node EVAL nhé. Node này sẽ để chạy các dòng code javascript.

Đầu tiên mình cần xác định element box bên ngoài, tìm element chung nha để có thể tự động tính toán cần phải chọn bao nhiêu cái. Như ở đây có 2 box, nên element mình tìm nó cũng phải đúng với cả 2 box. ![](https://i.imgur.com/t8UHDqL.png)

&#x20;

Sau đó cho vào vòng for, tạo biến output cho số lần lặp. Để mỗi lần tìm được element box ngoài này nó sẽ tự chạy quy trình chọn option bên trong. Giá trị của biến ” **Loop index save to”** là các số tự nhiên 1 2 3 đại diện cho số vòng lặp. đối với for element thì số thứ tự lặp lại bắt đầu từ 0 chứ không phải là 1 như lặp số lần, nên dùng thêm node  SET VARIABLE +1 sau mỗi vòng để cho đúng số thứ tự nhé.

&#x20;

![](https://i.imgur.com/gssmJtY.png) ![](https://i.imgur.com/Qg5x4RR.png)

&#x20;

Node thứ 3 là EVAL, phần này những người đã biết code js thì có thể sẽ làm đơn giản hơn, còn với những người không biết như mình thì mình hay dùng chat gpt với pormt ” Give me js code……. ( nhập việc mà bạn muốn nó xử lý ) .. I will run in devtool”. Như ở đây mình hỏi chat GPT là đưa tôi đoạn code để lấy được tất cả các giá trị trong element … rồi chọn random một giá trị trong số đó. Ví dụ ở đây element #mainContent div.x-msku\_\_box-cont là element chính ( bên trên có đề cập ) thì #mainContent div.x-msku\_\_box-cont:nth-child(1) sẽ là box 1, #mainContent div.x-msku\_\_box-cont:nth-child(2) sẽ là box 2, ký hiệu nth-child(index) chính là biểu thị element con, bạn có thể tìm hiểu về css thêm phần này nhé. vậy là chỉ cần thay đổi số 1 và 2 trong nth-child thì sẽ ra cái mình muốn, cho nên phần bên trong nth-child b để biến output của vòng for nhé. Cho nên phần eval code mới để ” #mainContent div.x-msku\_\_box-cont:nth-child(${index}) select option ”

&#x20;

![](https://i.imgur.com/fdTEtXj.png)

**Inject variables là** truyền biến vào, mình cần sử dụng biến index từ vòng for nên cần nhập biến indec ở ô **Inject variables** nhé. Còn biến **Output Variable** đương nhiên là để biểu thị giá trị của dòng return cuối cùng kia. Ví dụ bạn random ra được 5, thì muốn dùng số 5 này bạn phải đặt tên cho nó, chỗ output này là để đặt tên.

![](https://i.imgur.com/S44o08j.png)

&#x20;

Sau khi xong bước này, bạn node cuối là **Drop-down selector** thôi, element nhập vào thì để nguyên element như trong eval. **Selected value** thì chọn biến lấy ra được từ node eval trên, bên trên mình đặt tên là select cho nên ở đó là ${select}.

![](https://i.imgur.com/44Vn9ED.png)

&#x20;

Với công thức trên thì bạn không cần quan tâm trong trang đó có bao nhiêu box và trong box có bao nhiêu value nữa, script sẽ tự động tìm kiếm và random lựa chọn giá trị.&#x20;
