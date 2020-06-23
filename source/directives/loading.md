---
title: loading指令
---
# loading指令

通过给页面添加`v-miao-status`指令可以控制页面显示状态

使用：
```html
<div id="app" class="" v-miao-status="loadStatus" :err="errorMsg"></div>
```

| loadStatus值 | 作用
| :-: | :-:|
|0| loading状态 |
|1| 成功 | 
|2| 失败 |

当失败的时候，会通过元素接受的err属性获取失败信息显示在页面上。