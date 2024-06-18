# 上传多张照片 (Upload multiple photos)

如果您想在一个文件夹中上传多张照片，这里有一个脚本供您参考。

首先我们有一个包含您要上传的图像的文件夹：

<figure><img src="../../.gitbook/assets/image (140).png" alt=""><figcaption></figcaption></figure>

在文件夹的邮件链接中，输入cmd并按Enter键

<figure><img src="../../.gitbook/assets/image (141).png" alt=""><figcaption></figcaption></figure>

出现 cmd 控制台，然后键入命令：dir /B /S>FolderList.txt 和命令 echo x>>FolderList.txt 并按 Enter

<figure><img src="../../.gitbook/assets/image (142).png" alt=""><figcaption></figcaption></figure>

然后你已创建一个名为FolderList的txt文件，其中包含文件夹中所有图像的链接：

<figure><img src="../../.gitbook/assets/image (144).png" alt=""><figcaption></figcaption></figure>

打开该txt文件，删除该文件的第一行并保存文件，它是包含文件夹链接的行，包含字母x的行必须保留，当读取文件到该行时，意味着所有照片都已上传：

<figure><img src="../../.gitbook/assets/image (145).png" alt=""><figcaption></figcaption></figure>

我们有以下脚本：我们将上传照片到 lightShot：

<figure><img src="../../.gitbook/assets/image (146).png" alt=""><figcaption></figcaption></figure>

在此脚本中：

* 要读取文件，请选择文件FolderList.txt，然后选择类型 Line by line 从上到下读取，读取完成后，值将保存在file\_anh变量中。

<figure><img src="../../.gitbook/assets/image (147).png" alt=""><figcaption></figcaption></figure>

* Node if 我们将比较变量 file\_anh 的值是否等于 x，这意味着文件已被读取并且所有图像已上传。如果file\_anh不等于x，则说明该文件夹中的所有图片还没有上传，那么我们将继续上传图片。

<figure><img src="../../.gitbook/assets/image (148).png" alt=""><figcaption></figcaption></figure>

* 节点文件选择事件我们将选择文件字段链接中的 file\_anh 变量

<figure><img src="../../.gitbook/assets/image (149).png" alt=""><figcaption></figcaption></figure>

* 节点点击我们将执行一次点击上传图片

下面是一个示例脚本：

{% file src="../../.gitbook/assets/Upload nhieu anh.rar" %}
