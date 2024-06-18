# IMAP（阅读邮件) (Read mail)

该节点用于读取发送到您邮箱的邮件内容。

<figure><img src="../../.gitbook/assets/image (108).png" alt=""><figcaption></figcaption></figure>

1. Email service：您需要选择您要阅读的电子邮件服务。支持的服务包括：Gmail、Outlook/Hotmail、Yahoo、自定义。

* Gmail：您需要输入您需要读取的邮箱地址以及您邮箱的申请密码。对于应用程序密码，您需要创建一个应用程序密码，您可以参考如何创建应用程序密码 [在此](https://support.google.com/mail/answer/185833?hl=en)。
* Outlook/Hotmail：您需要输入您的电子邮件和密码。
* Custom：您可以自定义支持除电子邮件和 Outlook/Hotmail 之外的 Imap 的邮件服务。选择自定义时，需要输入您要读取的邮件服务的IMAP主机和IMAP端口。

2. Mailbox：默认为 INBOX。当进入收邮箱时，邮件收件箱部分的邮件将会被读取。此外，您还可以通过在“邮箱”字段中输入“\[Gmail]/垃圾邮件”来阅读 Gmail 垃圾邮件部分中的电子邮件。对于hotmail，您还可以通过在“邮箱”字段中输入“JUNK”来阅读“垃圾邮件”中的邮件。
3. 复选框：

* Unseen mail only：选择此选项时，您将以未读状态阅读邮件，最多阅读 5 封邮件。
* Mark mail as read：选择此选项后，当您阅读完处于未读状态的电子邮件时，会将这些电子邮件标记为已读。
* Get latest mail：选择此项时，将显示最新的电子邮件。当您取消选中此选项时，将出现发件人电子邮件包含字段。
* Sender email contains：取消获取最新邮件时会出现此字段。您可以在此输入您要阅读的邮件主题，系统将检索最近 5 封主题与您输入的主题相符的邮件。

<figure><img src="../../.gitbook/assets/image (109).png" alt=""><figcaption></figcaption></figure>

4. Content mail contains：此字段用于输入regex以 检索数据。
5. Read mail timeout (milliseconds)：最长等待时间。例如：30000：如果该步骤在30秒内没有执行成功，则直接执行下一步。
6. Output variable：输入变量名称以存储从 regex 获取的数据。
7. Preview：点击该按钮时，会显示该节点可以读取的邮件，并显示通过输入的regex获取的数据。

