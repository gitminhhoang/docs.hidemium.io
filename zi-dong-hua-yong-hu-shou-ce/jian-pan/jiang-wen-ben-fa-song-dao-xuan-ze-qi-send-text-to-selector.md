# 将文本发送到选择器 (Send text to selector)

用户可以同时用此node执行两个操作。单击要向其发送一段文本的输入框，例如电子邮件、密码或关键字，并将其称为选择元素。我们上面谈到了如何获取正确的选择器。之后，我们需要在一行中输入单个内容；请在新行中输入多个内容，其中之一将被随机选择。示例：

内容一

内容二

或者单击橙色按钮，它将让您选择您输入的变量

<figure><img src="../../.gitbook/assets/image (139).png" alt=""><figcaption></figcaption></figure>

<table><thead><tr><th width="258">参数</th><th>说明</th></tr></thead><tbody><tr><td>Select element </td><td>输入要填充文本的元素的 CSS 选择器，例如 #email、#global-enhancements-search-query</td></tr><tr><td>Element order </td><td>选择网站的哪个元素</td></tr><tr><td>Content</td><td>输入内容，每内容 1 行。如果输入多行，node将自动随机化并随机取 1 行</td></tr><tr><td>Enter interval time</td><td>输入字符之间的间隔。例如：如果输入 100，则每个字符将间隔 100 毫秒输入</td></tr></tbody></table>
