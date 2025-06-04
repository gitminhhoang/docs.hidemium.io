# 文件选择事件 (File choose event)

当页面触发文件选择事件时，将执行文件选择事件。并且该文件选择事件没有 type="file" 的 Input 标签，您可以使用文件选择事件node。

请注意，此文件选择事件应放在单击之前。

<figure><img src="../../.gitbook/assets/image (9) (1) (1).png" alt=""><figcaption></figcaption></figure>

<table><thead><tr><th width="258">参数</th><th>说明</th></tr></thead><tbody><tr><td>Choose selector type</td><td>"本地文件：选择本地文件上传到文件夹。 文件夹文件随机：选择一个文件夹，随机上传文件夹中的文件。 网络文件：要上传网络文件，请输入以http/https开头的URL。"</td></tr><tr><td>Timeout waiting</td><td>最长等待时间。例如：30000。如果30秒内此步骤未成功执行，则直接执行下一步。</td></tr></tbody></table>
