# attr(name|properties|key,value|fn)

## 概述
获取匹配的元素集合中的第一个元素的属性的值 或 设置每一个匹配元素的一个或多个属性。
当属性没有被设置时候，.attr()方法将返回undefined。若要检索和更改DOM属性,
比如元素的checked, selected, 或 disabled状态，请使用.prop()方法。

## 参数
name                        属性名称
properties                  作为属性的“名/值对”对象
key,value                   属性名称，属性值
key,function(index, attr)   
1:属性名称。
2:返回属性值的函数,第一个参数为当前元素的索引值，第二个参数为原先的属性值。

### 示例 1 参数name 描述:
>返回文档中所有图像的src属性值。

P 代码
```
P("img").attr("src");
```
### 示例 2 参数properties 描述:
>为所有图像设置src和alt属性。

P 代码
```
P("img").attr({ src: "test.jpg", alt: "Test Image" });
```

### 示例 3 参数key,value 描述:
>为所有图像设置src属性。

P 代码
```
P("img").attr("src","test.jpg");
```

### 示例 4 参数key,回调函数 描述:
>把src属性的值设置为title属性的值。

P 代码
```
P("img").attr("title", function() { return this.src });
```
