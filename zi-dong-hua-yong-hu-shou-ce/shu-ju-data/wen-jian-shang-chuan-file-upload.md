# 文件上传 (File upload)

您可以将文件上传到您想要的网站。网站文件上传按钮需要有一个带有 type="file" 的 Input 标签。

请注意，有些网站有一个带有 type="file" 的 Input 标签，但具有此 Display: none 属性，因此您无法获取此输入类型的选择器，您必须获取 Input 标签上方的 Label 标签的选择器。

<figure><img src="../../.gitbook/assets/image (8) (1).png" alt=""><figcaption></figcaption></figure>

<table><thead><tr><th width="258">参数</th><th>说明</th></tr></thead><tbody><tr><td>Select element</td><td>输入要上传元素的 CSS 选择器</td></tr><tr><td>Element order</td><td>根据元素在页面上出现的顺序选择元素</td></tr><tr><td>Path to the file</td><td>"本地文件：选择要上传的本地文件。 文件夹文件随机：选择一个文件夹，并在文件夹中随机上传文件。 网络文件：要上传网络文件，请输入以 http/https 开头的 URL。"</td></tr><tr><td>Timeout waiting</td><td>最长等待时间。例如：30000。如果 30 秒内未成功执行此步骤，则直接执行下一步。</td></tr></tbody></table>
