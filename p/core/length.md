# length

## 概述
  `p` 对象中元素的个数.
  当前匹配的元素个数。 <span title="Core/length">length</span> 将返回相同的值

## 示例 1
>计算文档中所有图片数量，记住length 后面不跟 `（）`,

HTML 代码:
```
<img src="p1.jpg"/> <img src="p2.jpg"/>
```
P 代码
```
P("img").length;
```
结果返回:
```
2
```
## 与size() 的区别

- 针对标签对象元素，比如数html页面有多少个段落元素<img /> 那么此时的 `P("img").size() == P("img").length`.
- 计算一个字符串的长度或者计算一个数组元素的个数那么此时只能用`length`而不能用`size()`.
