# `Pan` 方法

## 谷歌统计-引入
```
Pan.googleCount();
```

### 信息框- alert
```
Pan.alert('Panli 欢迎您', {icon: 6});
```
> 代替原生 alter --- Pan.alert(a, b);  a=> 要弹出的文本内容，b => 图标 只需修改数字 1 - 7 即可, 分别代表不同的图标


### 信息框-confirm
```
Pan.confirm('确定要删除吗？', {icon: 3}, function (index){
    Pan.close(index);
    alert('删除成功');
});
```

### 信息框-msg || 基础
```
Pan.msg('Panli 欢迎您');
```

### 信息框-msg || 基础+图片
```
Pan.msg('不开心...', {icon: 5});
```

### 信息框-msg || 基础+闭包函数
```
Pan.msg('正在加载...', function(){
    //关闭后的操作
});
```

### 信息框-msg || 正上方
```
Pan.msg('我在上面', {
    offset: 0,
    shift: 6
});
```

### 页面层-open || 自定义
```
Pan.open({
  type: 1,
  title: false,
  closeBtn: false,
  shadeClose: true,
  skin: 'yourclass',
  content: '自定义HTML内容'
});
```
> content : 输入您编写好的弹出层的 html  列入： 首页要弹出一个 双11活动，把您切合的 弹出的html内容 直接放入 content 里；

### iframe层-父子级层
```
Pan.open({
  type: 2,
  area: ['700px', '530px'],
  fix: false, //不固定
  maxmin: true,
  content: 'http://blog.zanjs.com'
});
```

### iframe层-多媒体
```
Pan.open({
  type: 2,
  title: false,
  area: ['630px', '360px'],
  shade: 0.8,
  closeBtn: false,
  shadeClose: true,
  content: 'http://www.tudou.com/a/Ko7krCYz4w4/&iid=132541449&resourceId=0_04_05_99/v.swf'
});
```

### iframe层-禁滚动条
```
Pan.open({
  type: 2,
  area: ['360px', '500px'],
  skin: 'layui-Pan-rim', //加上边框
  content: ['http://PanLi.com', 'no']
});
```

### 加载层 loading -默认风格
```
Pan.load();
```
### 加载层 loading -风格2
```
Pan.load(1);
```

### 屏蔽浏览器滚动条
```
Pan.open({
    content: '浏览器滚动条已锁',
    scrollbar: false
});
```

### 弹出即全屏
```
var index = Pan.open({
    type: 2,
    content: 'http://www.panli.com',
    area: ['300px', '195px'],
    maxmin: true
});
Pan.full(index);
```

### 关闭窗口
```
 Pan.closeAll();
```
