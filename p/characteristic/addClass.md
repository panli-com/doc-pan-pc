# addClass(class|fn)

## 概述

为每个匹配的元素添加指定的类名。

## 参数
- class
一个或多个要添加到元素中的CSS类名，请用空格分开
- function(index, class)
此函数必须返回一个或多个空格分隔的class名。接受两个参数，
index参数为对象在这个集合中的索引值，class参数为这个对象原先的class属性值。

### 示例 1 参数class 描述:
>为匹配的元素加上 'selected' 类

P 代码
```
P("p").addClass("selected");
P("p").addClass("selected1 selected2");
```

### 示例 2 回调函数:
>给li加上不同的class

HTML 代码:
```
<ul>
      <li>Hello</li>
      <li>Hello</li>
      <li>Hello</li>
</ul>
```
P 代码
```
P('ul li:last').addClass(function() {
  return 'item-' + P(this).index();
})
```
