# CÁCH ĐỂ SỬ DỤNG X THỎA MÃN 2 ĐIỀU KIỆN HOẶC THỎA MÃN MỘT TRONG NHIỀU ĐIỀU KIỆN BẰNG AUTOMATION

Chắc hẳn khi làm các script phức tạp thì bạn sẽ thắc mắc làm như nào để setup quy trình cho việc X thỏa mãn 2 hoặc nhiều điều kiện ( hay còn gọi là IF AND ) hoặc thỏa mãn 1 trong nhiều điều kiện ( IF OR ). Dưới đây sẽ là bài hướng dẫn chi tiết về việc này.

### I. X thỏa mã 2 hoặc nhiều điều kiện

Lấy 1 ví dụ đơn giản tìm X trong dãy 1 2 3 4 5, điều kiện là phải lớn hơn 2 và nhỏ hơn 4. Thì trong script chúng ta sắp xếp như sau

![](https://i.imgur.com/ZR51F3y.png)

Logic sẽ là cho lặp quy trình tìm X này đến khi ra đúng điều kiện mình cần. Đầu tiên là random x, rồi check IF X > 2 ( là điều kiện đầu tiên ), nếu thỏa mãn X > 2 ( đầu xanh ) thì check tiếp X < 4, nếu thỏa mãn tại đây thì ta nối đầu xanh vào STOP LOOP đẻ dừng quy trình tìm X này lại, nếu không thỏa mãi 1 trong 2 điều kiện trên thì nối đầu đỏ của 2 node IF trên vào for để lặp và random lại số X.

Kết quả Log sẽ như dưới đây:

![](https://i.imgur.com/oPmELot.png)

### II. X thỏa mãn 1 trong nhiều điều kiện

“Lấy ví dụ đơn giản là random X từ 1 đến 3. Nếu X = 1 thì làm hành động 1\
Nếu X = 2 thì làm hành động 2\
Nếu X = 3 thì làm hành động 3 ”

Sắp xếp script như dưới đây :

&#x20;

![](https://i.imgur.com/GJinL9X.png)

Logic là cho RANDOM X từ 1 đến 3. Nếu X = 1 thì New tab ( nối đầu xanh ), nếu X không bằng 1 thì sẽ nối đầu đỏ đến node IF thứ 2 để check tiếp, nếu X = 2 thì New tab, X lại không bằng 2 thì check điều kiện tiếp ( nối đầu đỏ)Nếu X =3 thì New tab, và node IF thứ 3 này không có đầu đỏ vì chỉ random từ 1 đến 3 cho nên nếu X đã không = 1 hoặc 2 rồi thì chắc chắn là 3. Không có trường hợp X khác 1 2 3 cho nên node IF thứ 3 không cần đầu đỏ.Bạn sẽ thấy Log là X chỉ cần thỏa mãn 1 trong 3 điều kiện là được

![](https://i.imgur.com/MzJMpLK.png)

### III. RANDOM X NHƯNG KHÔNG LẶP LẠI VÀ CÓ CHO LẶP LẠI GIÁ TRỊ ĐÃ LẶP ĐƯỢC

#### 1. Random X nhưng không lặp lại

Tức là ở đây bạn muốn lần 1 random ra X bằng 1 rồi thì lần 2 phải ngoại trừ cái số 1 này ra, nếu ra 1 thì random lại. Theo logic như vậy ta có scipt như sau

<figure><img src="../../../.gitbook/assets/image (161).png" alt=""><figcaption></figcaption></figure>



Cần phải xác định 2 tên biến sau, 1 là **sorandom**( số random) và **sokhongduoclap**( số không được lặp ). Lúc đầu cả 2 biến này đều rỗng và chưa có giá trị nào.Cho random **sorandom** từ 1 đến 3Nếu sokhongduoclapchứa **sorandom** thì random lại ( đầu xanh IF ), nếu không chứa thì SET VARIABLE **sokhongduoclap** nối với |${sorandom} và làm các hành động tiếp theo mình muốn ( tượng trưng là node ADD LOG )

![](https://i.imgur.com/ch8qqgz.png)

<figure><img src="../../../.gitbook/assets/image (160).png" alt=""><figcaption></figcaption></figure>

Ta có log sau :

![](https://i.imgur.com/pDrKdVk.png)

File script đây cho ai muốn tham khảo : https://drive.google.com/file/d/1j3tSBMWYIwGuWHMlcvkFbAgh7NCbaOS0/view?usp=sharing

#### 2. Random X có cho lặp lại 1 số giá trị nhất định và không cho lặp lại 1 số giá trị

Tiếp tục với ví dụ trên, ở đây ta cần xác định thêm 1 biến nữa là **soduoclap ( số được lặp).** Tổng cộng có 3 biến : **soduoclap – sokhongduoclap – sorandom**

Như vậy chắc chắn **sorandom** ra sẽ rơi vào 1 trong 2 trường hợp là được lặp hoặc không được lặp. Thì đến đây lại làm như bước II là thỏa mãn 1 trong 2 điều kiện là được, khác ở chỗ phương thức so sánh ở đây không phải < > = =/ nữa mà là **contains** là được.

&#x20;

<figure><img src="https://i.imgur.com/TJ1YZhu.png" alt="" height="462" width="734"><figcaption><p>Xác định trước 2 biến này</p></figcaption></figure>

&#x20;

<figure><img src="https://i.imgur.com/FZK5arI.png" alt="" height="454" width="812"><figcaption><p>Dùng Contains để so sánh</p></figcaption></figure>

&#x20;

<figure><img src="https://i.imgur.com/gfV1ybD.png" alt="" height="446" width="798"><figcaption></figcaption></figure>

\
