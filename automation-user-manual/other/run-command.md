# Run command

Node này dùng để mở một file trong folder

<figure><img src="../../.gitbook/assets/image (108).png" alt=""><figcaption></figcaption></figure>

* Command line: Nhập tên file hoặc đường dẫn đầy đủ của file cần mở. Ví dụ bạn có thể nhập như sau: D:\test\3.mp4 hoặc nhập 3.mp4
* Dir: Ghi đường dẫn chứa file mà bạn cần mở. Nếu trường **Command line** bạn đã nhập đầy đủ đường dần của file cần mở như thế này: D:\test\3.mp4 thì tại trường **Dir** bạn nên bỏ trống. Còn nếu trường **Command line** bạn nhập 3.mp4 thì ở trường **Dir** bạn cần nhập D:\test
* Time Skip: là thời gian chờ output của process chạy từ command, nếu process không return output thì sẽ next sang node khác sau thời gian timeout với status = success, nếu timeout = 0 và process không return thì sẽ không next sang node khác. Nói dễ hiểu hơn thì khi chạy node run command để mở một vài file, file đã được mở lên thành công nhưng không thể chạy node tiếp theo. khi đó bạn cần nhập Time skip để sau thời gian bạn nhập thì node tiếp theo sẽ được chạy. Ví dụ nếu bạn cần mở file txt, excel,... thì bạn cần nhập Time skip.



Ví dụ với trường hợp mở file txt, bạn cần nhập như sau:

<figure><img src="../../.gitbook/assets/image (109).png" alt=""><figcaption></figcaption></figure>

Như vậy là khi mở file thành công thì sau 3 giây thì node tiếp theo sẽ được chạy.
