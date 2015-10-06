# removeClass(class|fn)

## 概述

从所有匹配的元素中删除全部或者指定的类。

## 参数
class
>一个或多个要删除的CSS类名，请用空格分开

function(index, class)
>此函数必须返回一个或多个空格分隔的class名。
接受两个参数，index参数为对象在这个集合中的索引值，class参数为这个对象原先的class属性值。

### 示例 1 参数class
>从匹配的元素中删除 'selected' 类

P 代码
```
P("p").removeClass("selected");
```
### 示例 2 参数class
>删除匹配元素的所有类

P 代码
```
P("p").removeClass();
```

### 示例 3 回调函数
>删除最后一个元素上与前面重复的class

P 代码
```
P('li:last').removeClass(function() {
    return P(this).prev().attr('class');
})
```
