# each(callback)

## 概述

以每一个匹配的元素作为上下文来执行一个函数。意味着，每次执行传递进来的函数时，
函数中的this关键字都指向一个不同的DOM元素（每次都是一个不同的匹配元素）。
而且，在每次执行函数时，都会给函数传递一个表示作为执行环境的元素在匹配的元素集合中所处位置的数字值作为参数
（从零开始的整型）。 返回 'false' 将停止循环 (就像在普通的循环中使用 'break')。返回 'true' 跳至下一个循环
(就像在普通的循环中使用'continue')

### 示例 1
>迭代两个图像，并设置它们的 src 属性。注意:此处 this 指代的是 DOM 对象而非 P 对象。

HTML 代码:
```
<img/><img/>
```
P 代码
```
P("img").each(function(i){
   this.src = "panli" + i + ".jpg";
 });
```
结果:
```
[ <img src="panli0.jpg" />, <img src="panli1.jpg" /> ]
```

### 如果你想得到 大 `P` 对象，可以使用 P(this) 函数。

HTML 代码:
```
<button>Change colors</button>
<span></span>
<div></div>
<div></div>
<div></div>
<div></div>
<div id="stop">Stop here</div>
<div></div>
<div></div>
<div></div>
```
P 代码
```
P("img").each(function(){
  P(this).toggleClass("example");
});
```
### 你可以使用 'return' 来提前跳出 each() 循环。
HTML 代码:
```
<button>Change colors</button>
<span></span>
<div></div>
<div></div>
<div></div>
<div></div>
<div id="stop">Stop here</div>
<div></div>
<div></div>
<div></div>
```
P 代码
```
P("button").click(function () {
  P("div").each(function (index, domEle) {
    // domEle == this 
    P(domEle).css("backgroundColor", "yellow");  
    if ($(this).is("#stop")) {
      P("span").text("Stopped at div index #" + index);
        return false;
    }
  });
});
```
