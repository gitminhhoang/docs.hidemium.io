# 元素存在 (Element exists)

此功能允许您检查所选元素是否存在。

如果元素不存在，则转到红线：

<figure><img src="../../.gitbook/assets/image (140).png" alt=""><figcaption></figcaption></figure>

如果元素存在，则转到蓝线：

<figure><img src="../../.gitbook/assets/image (141).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (142).png" alt=""><figcaption></figcaption></figure>

<table><thead><tr><th width="258">参数</th><th>说明</th></tr></thead><tbody><tr><td>Select element </td><td>输入要填充文本的元素的 CSS 选择器，例如 #email、#global-enhancements-search-query</td></tr><tr><td>Element order </td><td>选择 Web 的任何组件</td></tr><tr><td>Visible</td><td>如果设置为 true，则所选元素必须可见，node才能运行到绿线。如果设置为 false，只要该元素存在（无论可见性如何），node就会运行到绿线。</td></tr><tr><td>Timeout waiting</td><td>最长等待时间。例如：30000：如果此步骤在 30 秒内未成功执行，则直接执行下一步</td></tr></tbody></table>
