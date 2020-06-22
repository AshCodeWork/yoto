---
layout: default
title:  get请求
parent: request请求
nav_order: 1
---
# get请求

基本写法：

```js
let p = 需求请求的参数(对象类型)
this.request
    .get( 请求地址 , {
        params: p,
    })
    .then(res => {
        console.log(res)
    })
    .catch(err => {
        console.log(err)
    })
```

例子:

```js
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