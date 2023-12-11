---
description: We have an English translation below.
---

# How to start script auto ?

## I. Cách Sử Dụng ô " Data" trong " Add Scheduele"





<figure><img src="../.gitbook/assets/Screenshot_117.png" alt=""><figcaption></figcaption></figure>

Như màn hình hiện tại thì mọi người có thể  thấy các nội dung khi viết theo format " Hidemium@gmail.com|passmail1|10 hệ thống tự hiểu vị trí của nội dung đó theo số thứ tự lần lượt 1 2 3 4 và được cách nhau bằng ký tự đặc biệt "|". Mỗi dòng là đại diện cho một profile. Phần data này sẽ dùng trong script dưới dạng biến như sau :&#x20;



<div>

<figure><img src="../.gitbook/assets/Screenshot_118.png" alt=""><figcaption></figcaption></figure>

 

<figure><img src="../.gitbook/assets/Screenshot_119.png" alt=""><figcaption></figcaption></figure>

</div>

Chính vì hệ thống tự hiểu thứ tự vị trí của từng nội dung nên trong script chỗ nào bạn cần sử dụng nội dung đó thì chỉ cần điền format của biến là **${}** và số thứ tự của nội dung đó ngoài bảng Data như 2 ảnh trên. Ví dụ node Send text kia phần content điền **${1}** thì khi bắt đấu chạy script b điền vào ô Data " **Hidemium@gmail.com|passmail1** thì script sẽ nhận dữ liệu của **${1}** là **Hidemium@gmail.com**. Tương tự node Type Text điền **${2}** thì dữ liệu script nhận được sẽ là **passmail1.**&#x20;

Có một lưu ý khi sử dụng tính năng này là người dùng phải tự tính toán được vị trí của dữ liệu mình muốn truyền vào trước để viết hoàn chỉnh trong script rồi sau đó khi mỗi lần chạy thì chỉ cần nhập data ở bảng " Data" là được.&#x20;



## II. Các cách có thể run script auto với các profile.
