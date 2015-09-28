# P(html,[ownerDocument])

## 概述

根据提供的原始 HTML 标记字符串，动态创建由 P 对象包装的 DOM 元素。同时设置一系列的属性、事件等。

你可以传递一个手写的 `HTML` 字符串，或者由某些模板引擎或插件创建的字符串，也可以是通过 `AJAX` 加载过来的字符串。但是在你创建 `input` 元素的时会有限制，
可以参考第二个示例。当然这个字符串可以包含斜杠 (比如一个图像地址)，还有反斜杠。当你创建单个元素时，请使用闭合标签或 `XHTML` 格式。例如，创建一个 `span` ，
可以用 `P("<span/>") 或 P("<span></span>") `，但不推荐 ` P("<span>")` 。在 `Panli` 中，这个语法等同于 `P(document.createElement("span"))`.

## 参数

#### html,[ownerDocument]
>html:用于动态创建DOM元素的HTML标记字符串
ownerDocument:创建DOM元素所在的文档

## 示例 1
> 动态创建一个 div 元素（以及其中的所有内容），并将它追加到 body 元素中。在这个函数的内部，
是通过临时创建一个元素，并将这个元素的 innerHTML 属性设置为给定的标记字符串，来实现标记到 DOM 元素转换的。
所以，这个函数既有灵活性，也有局限性。
```
P("<div><p>Hello Panli</p></div>").appendTo("body");
```

## 示例 2
>创建一个 <input> 元素必须同时设定 type 属性。因为微软规定 <input> 元素的 type 只能写一次。
```
// 在 IE 中无效:
P("<input>").attr("type", "checkbox");
// 在 IE 中有效:
P("<input type='checkbox'>");
```

## 示例 3
>动态创建一个 div 元素（以及其中的所有内容），并将它追加到 body 元素中。
在这个函数的内部，是通过临时创建一个元素，并将这个元素的 innerHTML 属性设置为给定的标记字符串，
来实现标记到 DOM 元素转换的。所以，这个函数既有灵活性，也有局限性。
```
P("<div>", {
  "class": "test",
  text: "Click me!",
  click: function(){
    P(this).toggleClass("test");
  }
}).appendTo("body");
```

## 示例 4
>创建一个 <input> 元素，同时设定 type 属性、属性值，以及一些事件。
```
P("<input>", {
  type: "text",
  val: "Test",
  focusin: function() {
    P(this).addClass("active");
  },
  focusout: function() {
    P(this).removeClass("active");
  }
}).appendTo("form");
```
