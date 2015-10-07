# toggleClass(class|fn[,sw])

## 概述

如果存在（不存在）就删除（添加）一个类。

## 参数
function(index, class,switch)[, switch]
>1:用来返回在匹配的元素集合中的每个元素上用来切换的样式类名的一个函数。接收元素的索引位置和元素旧的样式类作为参数。
 2: 一个用来判断样式类添加还是移除的 boolean 值。

### 示例 1 参数class 描述:
>为匹配的元素切换 'selected' 类

P 代码
```
P("p").toggleClass("selected");
```

### 示例 2 参数class,switch 描述:
>每点击三下加上一次 'highlight' 类

HTML 代码:
```
<strong>P 代码:</strong>
```

P 代码:
```
var count = 0;
  P("p").click(function(){
      P(this).toggleClass("highlight", count++ % 3 == 0);
  });
```
### 示例 3 回调函数 描述:
>根据父元素来设置class属性

P 代码:
```
var count = 0;
  P('div.foo').toggleClass(function() {
  if (P(this).parent().is('.bar') {
    return 'happy';
  } else {
    return 'sad';
  }
});
```
