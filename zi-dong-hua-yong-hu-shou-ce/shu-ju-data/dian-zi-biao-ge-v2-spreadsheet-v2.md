# 电子表格 V2 (Spreadsheet V2)

节点电子表格是节点电子表格的版本 2。使用此 V2，您可以比使用电子表格节点更轻松地读取 excel 文件和 google sheet文件。

<figure><img src="../../.gitbook/assets/image (44) (1).png" alt=""><figcaption></figcaption></figure>

## 本地文件

* 文件链接：选择您要读取的文件。
* 范围：Excel 文件中的一组单元格。例如，如果要从单元格 A1至单元格 E5 读取数据，我们将在“范围”字段中输入 A1:E5。您也可以将此字段留空。范围必须以大写字母输入。
* 工作表名称：Excel 工作表的名称。如果将此框留空，第一个工作表名称将默认为默认值。
* 第一行作为标题（列名称）：选中此复选框时，我们将认为 Excel 的第一行作为数据列的名称（标题）。当未选中该复选框时，各行是相等的。
* 读取带有停止条件的行：当不选中此复选框时，节点将默认从第一行获取数据。当您选择此复选框时，您必须输入两个字段：Column to compare 和 Value to compare。Column to compare：在此字段中，您将输入要对比的列。Value to compare：在此字段中，您将输入要对比的值。当未选中此复选框时，使用多个资料运行时，所有资料都将获取第一行的数据。
* 行匹配条件：选择一个变量。该字段将返回与节点正在读取的行匹配的行号，并将其存储在您选择的变量中。您可以在 WriteSheet 节点上使用此变量将数据写入与正在读取的数据行对应的行。 例如我们有如下数据表：

<figure><img src="../../.gitbook/assets/image (45) (1).png" alt=""><figcaption></figcaption></figure>

对于此数据表：例如，正在读取第 4 行的数据，节点会将值 4 存储在您选择的变量中。

* 最后一行数据：显示文件中包含数据的最后一行。在 Excel 文件中，您还可以通过按 Ctrl + End 检查最后一行是否包含数据，例如，我们有以下数据表：

<figure><img src="../../.gitbook/assets/image (46) (1).png" alt=""><figcaption></figcaption></figure>

通过此数据表，我们将获取文件中包含最后数据的行号。这里我们有 10 行，节点将存储值 10，该值将存储在您选择的变量中。该字段不依赖于您输入的范围，这意味着当您输入范围 A1:B3 时，该字段仍会将该表中包含数据的最后一行的行号视为 10。

* 存储：包括2个字段：列名和保存到。在“列”字段中，我们必须输入数据列的正确名称。对于“保存到”字段，我们将从“列名称”读取的值保存到变量中。
* 预览：显示节点已读取的数据。

## Google sheet

<figure><img src="../../.gitbook/assets/image (47).png" alt=""><figcaption></figcaption></figure>

* Google 电子表格 ID：输入 Google sheet ID，您可以在此处获取 ID：

<figure><img src="../../.gitbook/assets/image (48).png" alt=""><figcaption></figcaption></figure>

* Credentials文件：选择下载的Json文件

获取Credentials文件的说明：

1. 访问链接 [https://console.cloud.google.com/](https://console.cloud.google.com/) 并登录
2. 登录成功后，我们新创建一个项目

\- 选择“选择一个项目”

<figure><img src="../../.gitbook/assets/image (49).png" alt=""><figcaption></figcaption></figure>

\- 选择新项目

<figure><img src="../../.gitbook/assets/image (50).png" alt=""><figcaption></figcaption></figure>

\- 输入项目名称并选择创建

<figure><img src="../../.gitbook/assets/image (51).png" alt=""><figcaption></figcaption></figure>

3. 启用Google表格API

\- 在搜索栏中输入 Google Sheets API。出现搜索结果，然后在 Marketplace 中选择 Google Sheet API

<figure><img src="../../.gitbook/assets/image (52).png" alt=""><figcaption></figcaption></figure>

\- 启用 Google 表格 API

<figure><img src="../../.gitbook/assets/image (54).png" alt=""><figcaption></figcaption></figure>

4. 创建Credentials

\- 成功启用Google Sheets API后，继续选择Credentials



<figure><img src="../../.gitbook/assets/image (55).png" alt=""><figcaption></figcaption></figure>

\- 选择创建Credentials，然后选择服务帐户

<figure><img src="../../.gitbook/assets/image (56).png" alt=""><figcaption></figcaption></figure>

\- 输入服务帐户名称，然后选择“完成”

<figure><img src="../../.gitbook/assets/image (57).png" alt=""><figcaption></figcaption></figure>

\- 新创建的帐户将出现在此处：

<figure><img src="../../.gitbook/assets/image (58).png" alt=""><figcaption></figcaption></figure>

\- 单击该帐户并选择“密钥”标签页：

<figure><img src="../../.gitbook/assets/image (59).png" alt=""><figcaption></figcaption></figure>

\- 选择添加密钥 -> 选择创建新密钥

<figure><img src="../../.gitbook/assets/image (60).png" alt=""><figcaption></figcaption></figure>

\- 选择 JSON -> 选择创建

<figure><img src="../../.gitbook/assets/image (61).png" alt=""><figcaption></figcaption></figure>

创建后，JSON 文件将自动下载，并将该文件添加到 Spreadsheet V2 节点的Credencial字段中。

<figure><img src="../../.gitbook/assets/image (62).png" alt=""><figcaption></figcaption></figure>

5. 与上述步骤中创建的帐户共享工作表

\- 复制在上述步骤中创建的电子邮件：

<figure><img src="../../.gitbook/assets/image (63).png" alt=""><figcaption></figcaption></figure>

\- 与上面的帐户共享工作表页面：

<figure><img src="../../.gitbook/assets/image (64).png" alt=""><figcaption></figcaption></figure>

这样我们就成功地执行了设置 Google Sheet 来提供 Google Sheet 上的阅读文件。下面的字段与本地文件类似。

## 详细说明

**如果选择第一行作为标题（列名称）复选框：**

我们有一个数据表如下：

<figure><img src="../../.gitbook/assets/image (65).png" alt=""><figcaption></figcaption></figure>

在电子表格节点中，输入以下内容：

<figure><img src="../../.gitbook/assets/image (66).png" alt=""><figcaption></figcaption></figure>

在这种情况下，当选择“第一行作为标题（列名称）”复选框时，我们会将您输入的范围的第一行作为列标题。在“要比较的列”、“列名称”字段中，我们必须输入正确的列标题，例如在本例中，列名称将是电子邮件和密码。当在节点中输入如上所示的字段时，我们得到的数据如预览所示。如果我们不选中“读取带有停止条件的行”复选框，则默认情况下将读取文件的第一行（标题行除外）。

**如果未选中第一行作为标题（列名称）复选框：**

<figure><img src="../../.gitbook/assets/image (67).png" alt=""><figcaption></figcaption></figure>

在这种情况下，当选择第一行作为标题（列名称）复选框时，第一行将不会被视为列标题。在“要比较的列”和“列名称”字段中，我们必须输入表的正确列名称，例如在本例中，列名称将为 A、B、C...。

**依次读取与每个运行配置文件匹配的 Excel 文件的每一行的示例：**

<figure><img src="../../.gitbook/assets/image (68).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (69).png" alt=""><figcaption></figcaption></figure>

要运行每个配置文件以匹配 Excel 文件的每个数据行，我们必须输入“要比较的列”和“要比较的值”字段。在“列”字段中，我们将输入包含每个配置文件的 uuid 的列的标题。在本例中，标题将为 uuid，在“要比较的值”字段中，我们将选择 ${PROFILE\_ID} 变量。如上输入，在运行profile时，我们可以将profile\_id与excel文件的uuid列的数据行匹配的正在运行的profile进行比较，并与对应的profile读取该行的正确数据。

在“列名称”字段中，我们只需输入要从 Excel 文件中读取的列的正确标题并将其保存到变量中即可。

您可以将下面的 Excel 文件替换为您将运行的配置文件的 uuid。

{% file src="../../.gitbook/assets/example 2.xlsx" %}

{% file src="../../.gitbook/assets/SPREADSHEET V2.txt" %}

**随机读取每个配置文件的 Excel 文件的每一行的示例：**

如果您想将 Excel 文件的行读取到每个配置文件中而不需要任何顺序。然后，您可以使用 Spreadsheet V2 节点前面的 Random 节点来随机化列索引。

<figure><img src="../../.gitbook/assets/image (70).png" alt=""><figcaption></figcaption></figure>

在这种情况下，我们将从 1 到 10 进行随机化。然后在电子表格节点的范围字段中，我们将输入以下 A${index}:B10 在这种随机情况下，我们不应选择“读取带有停止条件的行”复选框。 。

<figure><img src="../../.gitbook/assets/image (71).png" alt=""><figcaption></figcaption></figure>

然后，当使用多个运行中资料时，Excel 文件中的数据将随机获取，而不按任何顺序。

下面是一个不按顺序读取每个资料的随机行的脚本：

{% file src="../../.gitbook/assets/example 2 (1).xlsx" %}

{% file src="../../.gitbook/assets/Spreadsheet V2 random.txt" %}

**读取列的所有数据并写入变量的示例**

例如我们有如下数据表：

<figure><img src="../../.gitbook/assets/image (72).png" alt=""><figcaption></figcaption></figure>

当我们想要将 A 列（电子邮件）的所有数据读取到一个变量中时，我们有以下脚本：

<figure><img src="../../.gitbook/assets/image (73).png" alt=""><figcaption></figcaption></figure>

在变量节点，我们创建一个变量，即索引变量，其值为2（因为excel表格中的数据是从第2行开始的，但如果有数据是从第一行开始的，则输入1）。

<figure><img src="../../.gitbook/assets/image (74).png" alt=""><figcaption></figcaption></figure>

在电子表格 v2 节点中，输入以下内容：

<figure><img src="../../.gitbook/assets/image (75).png" alt=""><figcaption></figcaption></figure>

在第一个设置变量节点，您需要输入以下内容：

<figure><img src="../../.gitbook/assets/image (76).png" alt=""><figcaption></figcaption></figure>

每次循环，索引的值都会增加 1。每次循环，都会读取 Excel 中 1 行的值。

在第二个设置变量节点，需要输入以下内容：

<figure><img src="../../.gitbook/assets/image (77).png" alt=""><figcaption></figcaption></figure>

第二个节点集变量用于将值连接在一起。在“变量名称”字段中，您选择一个新变量，以便在执行数据串联时，串联的数据将保存在该变量中（此处为变量 b）。在变量或值字段中，如图所示输入，并带有 | 符号用于分隔值，也可以使用其他字符分隔；这里的变量 ${email} 将从节点电子表格 v2 中检索到各值。
