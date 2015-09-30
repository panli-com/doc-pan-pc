# removeAttr(name)

## 概述

从每一个匹配的元素中删除一个属性

### 示例 1
>将文档中图像的src属性删除

HTML 代码:
```
<img src="test.jpg"/>
```

p 代码
```
P("img").removeAttr("src");
```
结果返回
```
[ <img /> ]
```
