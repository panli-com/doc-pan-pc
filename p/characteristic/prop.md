# prop(name|properties|key,value|fn)

## 概述

获取匹配的元素集中第一个元素的属性（property）值或设置每一个匹配元素的一个或多个属性。
随着一些内置属性的DOM元素或window对象，如果试图将删除该属性，
浏览器可能会产生错误。P 第一次分配undefined值的属性，而忽略了浏览器生成的任何错误

## 参数
name                        属性名称
properties                  作为属性的“名/值对”对象
key,value                   属性名称，属性值
key,function(index, attr)
1:属性名称。
2:返回属性值的函数,第一个参数为当前元素的索引值，第二个参数为原先的属性值。

### 示例 1 参数name 描述:
>选中复选框为true，没选中为false

P 代码
```
P("input[type='checkbox']").prop("checked");
```

### 示例 2 参数properties 描述:
>禁用页面上的所有复选框。

P 代码
```
P("input[type='checkbox']").prop({
  disabled: true
});
```
### 示例 3 参数key,value 描述:
>禁用和选中所有页面上的复选框。

P 代码
```
P("input[type='checkbox']").prop("disabled", false);
P("input[type='checkbox']").prop("checked", true);
```

### 示例 4 参数key,回调函数 描述:
>通过函数来设置所有页面上的复选框被选中。

P 代码
```
P("input[type='checkbox']").prop("checked", function( i, val ) {
  return !val;
});
```
