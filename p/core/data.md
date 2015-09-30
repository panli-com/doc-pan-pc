# data([key],[value])

## 概述

在元素上存放数据,返回 `P` 对象。
如果`P`集合指向多个元素，那将在所有元素上设置对应数据。这个函数不用建立一个新的expando，
就能在一个元素上存放任何格式的数据，而不仅仅是字符串。
>data(obj) 可传入key-value形式的数据。

## 参数
key:存储的数据名
value:将要存储的任意数据
obj:一个用于设置数据的键/值对

### 示例 1
>在一个div上存取数据

HTML 代码:
```
<div></div>
```

P 代码
```
P("div").data("blah");  // undefined
P("div").data("blah", "hello");  // blah设置为hello
P("div").data("blah");  // hello
P("div").data("blah", 86);  // 设置为86
P("div").data("blah");  //  86
P("div").removeData("blah");  //移除blah
P("div").data("blah");  // undefined
```
### 示例 2
>在一个div上存取名/值对数据

HTML 代码:
```
<div></div>
```

P 代码
```
P("div").data("test", { first: 16, last: "pizza!" });
P("div").data("test").first  //16;
P("div").data("test").last  //pizza!;
```
