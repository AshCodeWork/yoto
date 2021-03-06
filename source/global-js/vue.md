---
layout: default
title:  vue上的全局方法
parent: 全局js
nav_order: 2
---

# vue上的全局方法

vue上的全局方法是指可以使用`this`直接调用的，挂载在Vue.prototype上的方法

## 请求部分

### this.request

发送请求的方法，详情见request章节

```js
// 例如获取一个列表
this.request
    .get('mock/list', {
        params: {
            page: 1,
        },
    })
    .then(res => {
        console.log(res)
    })
    .catch(err => {
        console.log(err)
    })
```

### this.getApiUrl

获取定义的请求地址的url, 详情见request章节

```js
/*
* config/api.js
*/
const apiCore = {
    mockList: 'mock/list'
}

this.request
    .get(this.getApiUrl('mockList'), {
        params: {
            page: 1,
        },
    })
    .then(res => {
        console.log(res)
    })
    .catch(err => {
        console.log(err)
    })
```
## 埋点部分

### $countlyAddEvent

埋点提交。通过调用这个方法可以上报一个埋点事件。详情见埋点

```js
/**
 * eventName 事件名称 String
 * args 事件携带的参数 Object
 * count 数量 Number
*/
this.$countlyAddEvent(eventName, args, count)
```