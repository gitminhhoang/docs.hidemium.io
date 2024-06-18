# 电子表格 (Spreadsheet)

电子表格node可帮助您从 Excel 文件或 Google sheets中读取数据。

## 节点字段解释

<figure><img src="../../.gitbook/assets/image (29).png" alt=""><figcaption></figcaption></figure>

**本地文件：**

* 文件链接：选择计算机上可用的 Excel 文件。
* 范围：Excel 文件中的一组单元格。例如，如果要 读取数据从单元格 A1至单元格 E5，我们将在“范围”字段中输入 A1:E5。该范围字段只能输入大写字母。
* 工作表名称：Excel 工作表的名称。如果将此框留空，第一个工作表名称将默认为默认值。
* 第一行作为键：勾选此复选框时，我们会将 Excel 的第一行视为数据列的名称。未选中该复选框时，各行相等。
* 保存到：将获得的值保存到变量中
* 预览：预览节点从文件中读取的数据。
* 地图键：

**情况 1：当选择第一行作为键复选框时，我们有以下数据表：**

<figure><img src="../../.gitbook/assets/image (35).png" alt=""><figcaption></figcaption></figure>

选择预览时，会显示以下内容：

<figure><img src="../../.gitbook/assets/image (36).png" alt=""><figcaption></figcaption></figure>

在这种情况下，我们将输入：

\[0]\[“Email”] ：结果将是电子邮件值 abc@gmail.com

\[1]\[“Email”] ：结果将是电子邮件值 so1@gmail.com

同样，如果我们想获取密码，我们输入：

\[0]\[“Password”]​​：会得到值a123123

\[1]\["Password"] : 将得到值 abcd123

**情况 2：当未选中“第一行作为键”复选框时，我们有以下数据表：**

<figure><img src="../../.gitbook/assets/image (37).png" alt=""><figcaption></figcaption></figure>

当您点击预览时，将显示以下内容：

<figure><img src="../../.gitbook/assets/image (38).png" alt=""><figcaption></figcaption></figure>

然后我们将输入：

\[0]\[0] ：将获取值 abc@gmail.com

\[0]\[1]：将获取值a123123

\[1]\[0]：将获取值so1@gmail.com

\[1]\[1] ：将获取值abcd123

## **读取与每个资料匹配每一行的说明**

<div align="center">

<figure><img src="../../.gitbook/assets/image (39).png" alt=""><figcaption></figcaption></figure>

</div>

我们有以下脚本：

<figure><img src="../../.gitbook/assets/image (40).png" alt=""><figcaption></figcaption></figure>

在这情况，我们将创建一个值为 1 的变量 ${index}。

我们输入的节点如下：

<figure><img src="../../.gitbook/assets/image (41).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (42).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (43).png" alt=""><figcaption></figcaption></figure>

根据上面的数据表，在 for 节点我们将运行 10 次循环。在每个循环中，由于设置变量节点，我们将遍历 Excel 文件的每一行，该节点在每次循环后将索引变量的值增加 1。当这个变量增大时，每次循环的Spreadsheet节点的Range字段将是A1:B1、A2:B2、A3:B3等。像这样重复时，我们将使用 if 节点作为条件来对比Profile\_id带有 excel 文件 uuid 的运行资料。如果 Profile\_id 与 Excel 文件的 uuid 匹配，则停止循环并将该行的数据写入变量以供下一个节点使用。

下面是文件读取节点的示例脚本。此示例将依次读取每一行并对应于您运行的每个账号资料。您必须将 uuid 列中的数据替换为要运行资料的 uuid。
