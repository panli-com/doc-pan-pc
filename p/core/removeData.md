# removeData([name|list])

## 概述

在元素上移除存放的数据
与 P(...).data(name, value)函数作用相反

## 参数
[name]  存储的数据名
[list]  移除数组或以空格分开的字符串

### 实例 1
>从元素中删除之前添加的数据：

P 代码
```
p("#btn2").click(function(){
  p("div").removeData("greeting");
  alert("Greeting is: " + p("div").data("greeting"));
});
```
