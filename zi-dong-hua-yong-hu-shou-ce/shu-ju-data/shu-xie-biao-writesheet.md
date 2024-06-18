# 书写表 (WriteSheet)

## 节点字段说明

当你想将数据写入excel文件时，可以使用WriteSheet节点

<figure><img src="../../.gitbook/assets/image (78).png" alt=""><figcaption></figcaption></figure>

## 本地文件

* 文件链接：输入链接或选择包含 Excel 文件链接的变量。
* 工作表名称：输入 Excel 文件的工作表名称。如果将此字段留空，节点将自动取第一个sheet写入数据。
* Checkbox Append last row：选中该复选框时，节点将自动写入最后一行数据的下一行。例如，如果您的 Excel 文件中的数据到达第 20 行，则当您选此复选框时，该节点将自动写入下一行，即第 21 行。
* 单元位置：输入要记录数据的位置。当您不选择Append Last row复选框时，您必须输入需要写入数据的单元格，例如A1、B1、A2......，如果这些单元格有数据，则节点将覆盖数据。当你选中复选框时，你只需要输入列名A、B、C...，节点就会自动理解并写入包含数据的最后一行的下一行。
* 变量：输入要写入单元格的值。

## Google sheet

<figure><img src="../../.gitbook/assets/image (79).png" alt=""><figcaption></figcaption></figure>

* Google Spreadsheet ID：输入 GoogleSheet 文件的 ID

<figure><img src="../../.gitbook/assets/image (80).png" alt=""><figcaption></figcaption></figure>

* Credentical文件：选择下载的Json文件

**获取Credentical文件的说明：**

1. 访问链接 [https://console.cloud.google.com/](https://console.cloud.google.com/) 并登录
2. 登录成功后，我们新建一个项目：

\- 选择“选择一个项目”

<figure><img src="../../.gitbook/assets/image (81).png" alt=""><figcaption></figcaption></figure>

\- 选择新项目

<figure><img src="../../.gitbook/assets/image (82).png" alt=""><figcaption></figcaption></figure>

\- 输入项目名称并选择创建

<figure><img src="../../.gitbook/assets/image (83).png" alt=""><figcaption></figcaption></figure>

3. 启用Google sheet API

\- 在搜索栏中输入 Google Sheets API。出现搜索结果，然后在 Marketplace 中选择 Google Sheet API



<figure><img src="../../.gitbook/assets/image (84).png" alt=""><figcaption></figcaption></figure>

\- 启用 Google 表格 API

<figure><img src="../../.gitbook/assets/image (85).png" alt=""><figcaption></figcaption></figure>

4. 创建Credentical

\- 成功启用Google Sheets API后，继续选择Credentials

<figure><img src="../../.gitbook/assets/image (86).png" alt=""><figcaption></figcaption></figure>

\- 选择创建Credentical，然后选择服务帐户

<figure><img src="../../.gitbook/assets/image (87).png" alt=""><figcaption></figcaption></figure>

\- 输入服务帐户名称，然后选择“完成”

<figure><img src="../../.gitbook/assets/image (88).png" alt=""><figcaption></figcaption></figure>

\- 新创建的帐户将出现在此处：

<figure><img src="../../.gitbook/assets/image (89).png" alt=""><figcaption></figcaption></figure>

\- 单击该帐户并选择“密钥”标签页：

<figure><img src="../../.gitbook/assets/image (90).png" alt=""><figcaption></figcaption></figure>

\- 选择添加密钥 -> 选择创建新密钥：

<figure><img src="../../.gitbook/assets/image (91).png" alt=""><figcaption></figcaption></figure>

\- 选择 JSON -> 选择创建

<figure><img src="../../.gitbook/assets/image (92).png" alt=""><figcaption></figcaption></figure>

创建后，JSON 文件将自动下载，并将该文件添加到 WriteSheet 节点的 Credencial 字段中。

<figure><img src="../../.gitbook/assets/image (93).png" alt=""><figcaption></figcaption></figure>

5. 与上述步骤中创建的帐户共享工作表

\- 复制在上述步骤中创建的电子邮件：

<figure><img src="../../.gitbook/assets/image (94).png" alt=""><figcaption></figcaption></figure>

\- 与上面的帐户共享工作表页面：

<figure><img src="../../.gitbook/assets/image (95).png" alt=""><figcaption></figcaption></figure>

这样我们就成功地执行了设置 Google Sheet 来提供 Google Sheet 上的阅读文件。下面的字段与本地文件类似。

## **详细说明**

假设我们有如下数据表：

<figure><img src="../../.gitbook/assets/image (96).png" alt=""><figcaption></figcaption></figure>

* 如果要自动串行写入包含数据的最后一行的下一行，则填写以下内容：

<figure><img src="../../.gitbook/assets/image (97).png" alt=""><figcaption></figcaption></figure>

当我们输入这个时，节点会自动将数据写入第7行

* 或者，如果您不想串行写入，但想指定要写入数据的单元格，则可以输入以下内容：

<figure><img src="../../.gitbook/assets/image (98).png" alt=""><figcaption></figcaption></figure>

这样你就可以将数据写入你想要的单元格中。或者您可以输入已有数据的单元格，节点将覆盖您输入的单元格中的数据。

如果您想在读取数据后立即将数据写入 Excel 文件，并且想要准确写入每个相应的行，则可以使用 Spreadsheet V2 节点的行数据编号和总行数据字段。

假设我们有如下数据表：

<figure><img src="../../.gitbook/assets/image (99).png" alt=""><figcaption></figcaption></figure>

你想根据uuid读取每个对应的资料匹配的文件的每一行，那么进入Spreadsheet V2节点如下：

<figure><img src="../../.gitbook/assets/image (100).png" alt=""><figcaption></figcaption></figure>

您想要成功读取每一行并将其记录在相应的行中以了解该资料是否已成功读取您将使用 writeSheet 节点来记录：

<figure><img src="../../.gitbook/assets/image (101).png" alt=""><figcaption></figcaption></figure>

所以当我们成功读取一行时，在对应的行中我们会写上“成功”。

下面是成功读取文件后写入文件的示例脚本，请将要运行的资料的 uuid 更改为 excel 文件。

{% file src="../../.gitbook/assets/example (1).xlsx" %}

{% file src="../../.gitbook/assets/writesheet.txt" %}
