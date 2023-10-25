# Switch Frame

&#x20;Some pages have iframe and you have to use node Switch Frame to navigate. You have two choices Sub frame and main frame. If you choose a subframe you need to select the element of that frame and here you also set the timeout waiting. When you use other platform accounts to log into a platform, you may come across a situation like this: when you log into Tik Tok with a Google account, a new tab will appear outside the main tab to log in to your account. To control this sub-tab using a script, you need to use the Switch Frame node.\
\
Một số trang có iframe và bạn phải sử dụng nút Switch Frame để điều hướng. Bạn có hai lựa chọn Khung phụ và khung chính. Nếu chọn khung con bạn cần chọn element  của khung đó và ở đây bạn cũng đặt thời gian chờ. Giống như việc bạn đăng nhập vào một nền tảng thông qua các tài khoản nền tảng khác sẽ gặp trường hợp như thế này, VD: đăng nhập tik tok bằng tài khoản google thì nó sẽ hiện ra một tab ngoài tab chính để đăng nhập account google. Lúc này nếu muốn script điều khiển được tab phụ kia thì cần dùng node Switch Frame này.



<figure><img src="../../.gitbook/assets/Switch Frame (1).png" alt=""><figcaption></figcaption></figure>



| parameter                   | illustrate                                                                                                                                              |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Sub frame: Select element   | Nhập CSS selector, chẳng hạn như #email, #global-enhancements-search-query                                                                              |
| Sub frame: Timeout waiting  | Thời gian chờ đợi tối đa. Ví dụ: 30000: Nếu bước này không được thực hiện thành công trong vòng 30 giây thì bước tiếp theo sẽ được thực hiện trực tiếp. |
| Main frame: Timeout waiting | Thời gian chờ đợi tối đa. Ví dụ: 30000: Nếu bước này không được thực hiện thành công trong vòng 30 giây thì bước tiếp theo sẽ được thực hiện trực tiếp. |

{% file src="../../.gitbook/assets/Switch Frame.txt" %}
