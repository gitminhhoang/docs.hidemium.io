# 获取 URL (Get URL)

使用获取 URL node时，您可以获取网站链接的相关信息，将相关信息存储在变量中，并调用它进行其他操作。&#x20;

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

假设打开的 URL 为：https://www.etsy.com/search?q=book\&ref=search\_bar

<table><thead><tr><th width="258">参数</th><th>说明</th></tr></thead><tbody><tr><td>Content: Full URL</td><td>获取所有URL：https://www.etsy.com/search?q=book&#x26;ref=search_bar</td></tr><tr><td>Content: Domain</td><td>获取 URL 的 domain：www.etsy.com</td></tr><tr><td>Content: Search key</td><td>输入“q”时，将“book”存储在变量中。输入“ref”时，将“search_bar”保存在变量中。</td></tr><tr><td>Output Variable</td><td>将获取的价值保存到变量中</td></tr></tbody></table>
