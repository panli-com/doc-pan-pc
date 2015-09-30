# get([index])

## 概述

取得其中一个匹配的元素。 num表示取得第几个匹配的元素。
这能够让你选择一个实际的DOM 元素并且对他直接操作，而不是通过 P 函数。P(this).get(0)与P(this)[0]等价。

## 参数
[index]
>取得第 index 个位置上的元素

get()
>取得所有匹配的 DOM 元素集合。


## 示例 1

HTML 代码:
```
<img src="p1.jpg"/> <img src="p2.jpg"/>
```
P 代码:
```
P("img").get(0);
```
结果返回:
```
[ <img src="p1.jpg"/> ]
```
