# removeProp(name)

## 概述

用来删除由.prop()方法设置的属性集

随着一些内置属性的DOM元素或window对象，如果试图将删除该属性，
浏览器可能会产生错误。P 第一次分配undefined值的属性，
而忽略了浏览器生成的任何错误

### 示例 1
>设置一个段落数字属性，然后将其删除。

HTML 代码:
```
<p> </p>
```

P 代码
```
var Ppara = P("p");
Ppara.prop("luggageCode", 1234);
Ppara.append("The secret luggage code is: ", String(Ppara.prop("luggageCode")), ". ");
Ppara.removeProp("luggageCode");
Ppara.append("Now the secret luggage code is: ", String(Ppara.prop("luggageCode")), ". ");
```

结构返回
```
The secret luggage code is: 1234. Now the secret luggage code is: undefined. 
```
