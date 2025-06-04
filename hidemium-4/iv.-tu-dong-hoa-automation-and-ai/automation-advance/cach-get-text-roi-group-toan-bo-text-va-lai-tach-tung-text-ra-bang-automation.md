# CÁCH GET TEXT RỒI GROUP TOÀN BỘ TEXT VÀ LẠI TÁCH TỪNG TEXT RA BẰNG AUTOMATION

Có rất nhiều trường hợp bạn cần sử dụng phương pháp nâng cao group text lại rồi lại phải tách ra để sử dụng trong các bước tiếp theo của script. Hôm nay Hidemum sẽ hướng dẫn một use case cụ thể và hy vọng từ ví dụ thực tế này bạn có thể tự sáng tạo theo cách riêngcủa mình nhé

Use case cụ thể lần này là tạo ví ronin.

OK. Bỏ qua các bước click và tạo pass, đến phần check “Recovery Phrase” chúng ta cần cop hết 12 chữ này ra, chính vì vậy ngoài biến get đừng chữ ra 1, ta cần có 1 biến tổng chứa tất cả chữ này. Trên script làm như sau :

<figure><img src="../../../.gitbook/assets/image (162).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (163).png" alt=""><figcaption></figcaption></figure>

Sơ đồ phân đoạn lấy text và nối text

<figure><img src="../../../.gitbook/assets/image (164).png" alt=""><figcaption></figcaption></figure>

Mình chọn lặp theo element. Đây là element để lấy chữ

<figure><img src="../../../.gitbook/assets/image (165).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (166).png" alt=""><figcaption></figcaption></figure>

Dùng SET VARIABLE tự động tăng thêm 1 khi lặp vòng mới.

<figure><img src="../../../.gitbook/assets/image (167).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (168).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (169).png" alt=""><figcaption></figcaption></figure>

Node chính là Get text, thì dùng luôn element lấy text đẻ trong vòng for đó, vị trí chính là biến được tăng kia, vì số thứ tự khi lặp theo element trong for là bắt đầu từ 0, mà vị trí element trong các node lại bắt đầu từ 1, cho nên phải + 1 trước khi dùng để get text. Ở đây nếu lặp vòng 2, tức là 1 rồi +1 =2, thì lúc này, element sẽ ở vị trí 2, kết quả là biến Key lấy được chữ ” fortune”

<figure><img src="../../../.gitbook/assets/image (170).png" alt=""><figcaption></figcaption></figure>

Sau đó tạo một biến mới “Recovery\_Phrase”, dùng SET VARIABLE nối với biến Key lấy đuộc từ node GET TEXT. Kết quả sau 12 vòng lặp sẽ là biến “Recovery\_Phrase” = danger fortune wash reduce defy slide essence post neutral sing travel razor\
\=> hoàn thành việc gộp các biến nhỏ vào 1 biến lớn.

<figure><img src="../../../.gitbook/assets/image (171).png" alt=""><figcaption></figcaption></figure>

Nhưng sau đấy đến bước tiếp theo ta vẫn cần tách biến này ra để “Confirm Seed Phrase”

<figure><img src="../../../.gitbook/assets/image (172).png" alt=""><figcaption></figcaption></figure>

Sơ đồ phân đoạn tách text và nhập

<figure><img src="../../../.gitbook/assets/image (173).png" alt=""><figcaption></figcaption></figure>

Tương tự như ở trên, đoạn này là tìm xem có bao nhiêu element đánh số thứ tự như này và rồi dùng SET VARIABLE cộng thêm 1

<figure><img src="../../../.gitbook/assets/image (174).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (175).png" alt=""><figcaption></figcaption></figure>

Cũng lại dùng GET TEXT và đặt tên là “insert\_key” và để vị trí thay đổi theo index2 ( biến từ vòng lặp ).

<figure><img src="../../../.gitbook/assets/image (176).png" alt=""><figcaption></figcaption></figure>

Ở đây là mình muốn lấy số 1 4 8 10 này. Cái này tương đương với vị trí của text trong đoạn coppy trên, cho nên cần lấy nó để xác định là nên nhập chữ ở vị trí số mấy

<figure><img src="../../../.gitbook/assets/image (177).png" alt=""><figcaption></figcaption></figure>

Tiếp theo đến node eval, node này chỉ xuất hiện trong ví dụ cụ thể này thôi nha vì Text lấy được là #2 #4 #8 #10 cho nên cần xử lý qua Eval để tách từ này ra thành # và 2, và chọn output ra số 2

<figure><img src="../../../.gitbook/assets/image (179).png" alt=""><figcaption></figcaption></figure>

code :&#x20;

```
var str = insert_key;
var matches = str.match(/(\D+)(\d+)/);
if (matches) {
var nonNumberPart = matches[1]; // “#”
var numberPart = matches[2]; // “2”
console.log(“Phần không phải số: ” + nonNumberPart);
return numberPart;
} else {
console.log(“Không tìm thấy kết quả phù hợp”);
```

\
Đến node EVAL này mới dùng để tách đoạn text kia ra. Logic là từ biến ok ( tức là biến sau khi tách # và 2, ok = 2 ) kia để xác định từ sẽ lấy trong biến “Recovery\_Phrase”, nên chỗ này Inject 2 biến “ok” và “Recovery\_Phrase” vào. Và output là kết quả từ được lấy trong đoạn này.

<figure><img src="../../../.gitbook/assets/image (180).png" alt=""><figcaption></figcaption></figure>

CODE:

```
function findWordAtIndex(sentence, index) {
let words = sentence.split(” “);
if (index >= 0 && index < words.length) {
return words[index];
} else {
return “Vị trí không hợp lệ”;
}
}
let sentence = Recovery_Phrase; // Câu cần tìm từ
let index = ok; // Vị trí của từ
let word = findWordAtIndex(sentence, index);
return word; // In ra từ ở vị trí index trong câu sentence
```

Rồi dùng node SEND TEXT để nhập từ đã lấy thành công là xong. Cứ như vậy lặp lại quy trình này 4 lần là nhập thành công những từ cần xác minh để hoàn thành kịch bản auto tạo acc ronin.

<figure><img src="../../../.gitbook/assets/image (181).png" alt=""><figcaption></figcaption></figure>

II. Tách 1 cụm text thành từng từ một\
Ví dụ bạn có 1 biến Full\_text = danger fortune wash reduce defy slide essence post neutral sing travel razor. Sau đó muốn tách từng từ ra một. Thì tiếp tùng dùng eval nhé.
