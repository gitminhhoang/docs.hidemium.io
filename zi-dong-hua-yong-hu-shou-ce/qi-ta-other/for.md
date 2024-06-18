# For

此按钮允许您选择循环类型：数据、元素、或在脚本中重复特定操作或处理特定次数。

## For Data

<figure><img src="../../.gitbook/assets/image (116).png" alt=""><figcaption></figcaption></figure>

<table><thead><tr><th width="258">参数</th><th>说明</th></tr></thead><tbody><tr><td>For from value</td><td>输入数值或选择包含有效值的变量</td></tr><tr><td>For to value</td><td>输入数值或选择包含有效值的变量</td></tr></tbody></table>

For to value 的值必须大于 For from value 的值

{% file src="../../.gitbook/assets/For_data.txt" %}

## For Elements

您可以输入要循环的元素的 CSS 选择器。您可以选择在每个循环中提取的内容并将其保存到变量中。

<figure><img src="../../.gitbook/assets/image (117).png" alt=""><figcaption></figcaption></figure>

**Selector element**：输入CSS选择器，例如#email、\[data-results-grid-container]>li

**Content**：选择提取类型，包括：

* Text：提取您选择的元素的文本
* HTML：提取您选择的元素的 HTML
* Attribute：提取元素的属性，输入要提取的属性。

**Loop object save to**：将每次循环提取的网页元素保存为变量。

**Loop index save to**：将每次循环中提取的网页元素的位置保存到变量中。请注意，循环中网页元素的位置（索引）从 0 开始。

{% file src="../../.gitbook/assets/for_element.txt" %}

## For Times

当选择For Times时，您可以输入您想要的迭代次数。

<figure><img src="../../.gitbook/assets/image (118).png" alt=""><figcaption></figcaption></figure>

<table><thead><tr><th width="258">参数</th><th>说明</th></tr></thead><tbody><tr><td>Times</td><td>输入所需的迭代次数，最多 99。</td></tr><tr><td>Loop index save to</td><td>将每次循环中提取的网页元素的位置保存到变量中。注意循环中网页元素的位置（索引）从1开始。</td></tr></tbody></table>

{% file src="../../.gitbook/assets/For_times.txt" %}
