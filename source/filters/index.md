---
title:  filters说明
---

# filters说明

filters文档中写的是自带的全局过滤器。根据实际业务需求肯定还要增加新的过滤器。

## 全局过滤器定义

### 第一步

全局过滤器都定义在`src/assets/js/filters`这个文件夹。在这个文件下下创建filter对应的js文件。我们假设叫`double.js`，

```js
// double.js
export default function (num) {
    return num * 2
}
```

### 第二步

将上一步新建的filter文件引入到该文件夹中`index.js`内并导出。

```js
// 以double为例
// 引入：
import double from './double.js'
// 导出：
export { double }
```

### 第三步

在`main.js`中引入,并使用`Vue.filter`注册。具体参考其他的全局filter。