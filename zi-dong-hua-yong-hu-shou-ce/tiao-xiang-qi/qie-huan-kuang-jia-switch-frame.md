---
description: >-
  有些页面带有iframe，需要使用node切换框架才能调向。您有两个选择：子框架和主框架。如果你选择子框架，则需要选择该框架的元素，在这里您还可以设置等待时间。当您使用其他平台账号登录平台时，您可能会遇到这样的情况：当你使用Google账号登录Tik
  Tok时，主标签页之外会出现一个新标签页来登录你的账号。要使用脚本控制这个子标签，您需要使用切换框架node。
---

# 切换框架 (Switch frame)

<figure><img src="../../.gitbook/assets/image (131) (1).png" alt=""><figcaption></figcaption></figure>

| 参数                        | 说明                                      |
| ------------------------- | --------------------------------------- |
| Sub frame: Select element | 输入框架的CSS选择器，即可对框架中的元素执行操作。              |
| Sub frame: Main frame     | 选择主框架时，其后面的步骤将影响网站主页。                   |
| Timeout waiting           | 最长等待时间。例如：30000：如果30秒内此步骤未执行成功，则直接执行下一步 |
