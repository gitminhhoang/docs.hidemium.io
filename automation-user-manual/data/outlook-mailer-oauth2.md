---
description: >-
  Node này dùng để đọc hotmail, và host mail phải có định dạng sau:
  email|pass|refresh token|client id
---

# Outlook Mailer (oAuth2)



<figure><img src="../../.gitbook/assets/image (205).png" alt=""><figcaption></figcaption></figure>

| parameter              | illustrate                                                                                                                                                            |
| ---------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Auth type              | bao gồm : GRAPH API, IMAP (Read mail)                                                                                                                                 |
| Client id              | nhập client id của hotmail                                                                                                                                            |
| Refresh token          | Nhập refresh token của hotmail                                                                                                                                        |
| Mark mail as read      | đánh dấu mail là đã đọc                                                                                                                                               |
| Get latest mail        | Đọc mail mới nhất, nếu không chọn ô này thì sẽ lấy 5 mail mới nhất                                                                                                    |
| Subject email contains | nhập tiêu đề của mail muốn đọc                                                                                                                                        |
| Content mail contains  | Nhập đoạn regex để lấy 1 phần trong mail. nếu bỏ trống, node sẽ lấy toàn bộ nội dung của email và ghi vào biến                                                        |
| Output variable        | kết quả sẽ dược lưu vào biến này                                                                                                                                      |
| Timeout waiting        | <p></p><p>Thời gian chờ đợi tối đa. Ví dụ: 30000. Nếu bước này không được thực hiện thành công trong vòng 30 giây thì bước tiếp theo sẽ được thực hiện trực tiếp.</p> |
