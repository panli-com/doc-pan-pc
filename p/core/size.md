# size()

## 概述
  `p` 对象中元素的个数.
  当前匹配的元素个数。 <span title="Core/size">size</span> 将返回相同的值

## 示例 1
>计算文档中所有图片数量

HTML 代码:
```
<img src="p1.jpg"/> <img src="p2.jpg"/>
```
P 代码
```
P("img").size();
```
结果返回:
```
2
```
