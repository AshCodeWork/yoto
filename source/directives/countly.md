---
title: add-event指令
---
# add-event指令

名称：`add-event`

作用：带有这个指令的标签在点击的时候可以上报埋点。

用法：
```html
<button v-add-event="{event: 'btn_click', args:{ type: 123}}">点击</button>
```
上例中我们假设上报一个埋点，事件名为`btn_click`， 参数为 `type:123`。
详细的埋点细节规范参考公司内部wiki。