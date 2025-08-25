# 写入文件 (Write file)

该按钮允许您通过覆盖编辑文件、使用特殊字符附加到侧面或在新行上写入。要添加文件，请在指定的“文件链接”部分中输入其完整路径或从您的设备上传。然后，根据您在橙色变量节点中设置的变量选择要包含在文件中的数据，并选择文件格式。做出选择后，将出现其他选项，用于指定您输入的数据的位置。

例如，假设我有一个文件包含多个需要登录的 Google 帐户。要标记这些帐户，我可以使用“写入文件”功能。在橙色“变量”节点中，我将“登录”变量设置为“完成”，将“注销”变量设置为“拒绝”。接下来，我将使用 Node 的“元素退出”功能检查帐户是否已登录。如果某个帐户已成功登录，我将使用“写入文件”功能将其标记为“完成”（通过选择登录变量），然后指示该帐户。如果某个帐户尚未登录，我将使用“写入文件”功能将其标记为“拒绝”（通过选择注销变量）。或者您可以在使用此功能时标记哪个账号资料与您的文件中的哪一行数据相匹配，然后选择变量“PROFILE\_NAME”

<figure><img src="../../.gitbook/assets/image (11) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

<table><thead><tr><th width="258">参数</th><th>说明</th></tr></thead><tbody><tr><td>File path</td><td>您要写入数据的文件链接</td></tr><tr><td>Select input data from variable</td><td>选择包含数据的变量以将该数据写入文件</td></tr><tr><td>Selector type</td><td>选择您要写入的文件格式：TXT、CSV、JSON。</td></tr><tr><td>Select write mode: Overwrite</td><td>覆盖以前的数据</td></tr><tr><td>Select write mode: Append</td><td>添加到文件，在新行或同一行上写入</td></tr></tbody></table>
