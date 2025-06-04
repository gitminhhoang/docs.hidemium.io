# 文本提取 (Extraction in text)

要从文本块中提取特定值，请使用规则为 A(._)\B 的正则表达式 (Regular Expression)。例如：您想从“验证码是 128293。请......”这样的消息中获取验证码，因此公式为“是(._)。请”，返回给您的值是 128293。

<figure><img src="../../.gitbook/assets/image (19) (1) (1).png" alt=""><figcaption></figcaption></figure>

<table><thead><tr><th width="258">参数</th><th>说明</th></tr></thead><tbody><tr><td>Data</td><td>选择包含一段文本的变量进行提取。</td></tr><tr><td>Extract rules</td><td>输入Regex表式以获取数据。</td></tr><tr><td>Index result</td><td>输入结果的索引，如果不输入节点将自动获取索引0。</td></tr><tr><td>Save to</td><td>将提取的值保存到变量中，该值将基于您选择的索引。</td></tr><tr><td>Test</td><td>单击时，您可以看到使用索引提取的结果。</td></tr></tbody></table>

例如，我们有这样一段数据：“我们有以下网站 https://www.facebook.com/ 和其他网站，如 https://www.youtube.com/ 和 https://www.etsy. com/”。当你想获取这段数据中包含的 URL 时，在 Extraction in text 节点中输入以下内容：

<figure><img src="../../.gitbook/assets/image (20) (1) (1).png" alt=""><figcaption></figcaption></figure>

在 Index result 字段中输入数字 1，我们将得到 https://www.facebook.com/ 并将其存储在 result 变量中。
