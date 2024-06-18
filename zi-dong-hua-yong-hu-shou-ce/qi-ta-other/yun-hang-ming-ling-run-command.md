# 运行命令 (Run command)

该节点用于打开文件夹中的文件

<figure><img src="../../.gitbook/assets/image (134).png" alt=""><figcaption></figcaption></figure>

* Command line：输入要打开的文件的文件名或完整链接。例如，您可以输入以下内容：D:\test\3.mp4 或输入 3.mp4
* Dir：写入包含您需要打开的文件的链接。如果在“命令行”字段中输入要打开的文件的完整链接，如下所示：D:\test\3.mp4，则在“Dir”字段中应将其留空。如果您在命令行字段中输入 3.mp4，则在Dir字段中您需要输入 D:\test
* Time Skip：是等待命令运行的进程导出的时间，如果进程没有返回导出，则在超时时间后，它将继续到另一个节点，并且状态=成功。如果超时= 0并且进程不返回，就不会继续到另一个节点。更简单的说，当运行node run命令打开几个文件时，文件打开成功，但是下一个节点无法运行。此时需要输入Timeskip，这样在你输入的时间之后，才会运行下一个节点。例如，如果您需要打开txt、excel文件...，那么您需要输入“时间跳过”。

例如，如果打开txt文件，则需要输入以下内容：

<figure><img src="../../.gitbook/assets/image (135).png" alt=""><figcaption></figcaption></figure>

因此，当文件成功打开时，3秒后将运行下一个节点。
