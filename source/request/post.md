---
layout: default
title:  post请求
parent: request请求
nav_order: 2
---

# post请求

## 表单提交

post请求默认为form请求。会对参数进行表单处理成`key=value&key2=value2`这种格式。

基本写法：

```js
let p = 需求请求的参数(对象类型)
this.request
    .post( 请求地址 , p)
    .then(res => {
        console.log(res)
    })
    .catch(err => {
        console.log(err)
    })
```

例子:

```js
// 假如给mock/set接口，发送参数name：123. 表单提交
this.request
    .post('mock/set', {
        name: 123,
    })
    .then(res => {
        console.log(res)
    })
    .catch(err => {
        console.log(err)
    })
```
## body提交

有的时候服务端需要前端给的是JSON的格式，不是表单格式。这时候使用这种写法。

基本写法：

```js
// 第三个参数传入 { toJSON: true }
let p = 需求请求的参数(对象类型)
this.request
    .post( 请求地址 , p, { toJSON: true })
    .then(res => {
        console.log(res)
    })
    .catch(err => {
        console.log(err)
    })
```
例子：

```js
this.request
    .post(
        'mock/set',
        {
            name: 123,
        },
        { toJSON: true }
    )
    .then(res => {
        console.log(res)
    })
    .catch(err => {
        console.log(err)
    })
```

## 纯post提交

假设我们给拦截器做了配置，每个post请求都会带有类似于token的参数，但有的接口实际上是不需要这个参数的，它只是单纯的发一个请求。比如登录请求，这时候我们还没有token，给请求加token显然是不现实的。这个情况使用这种请求。

基本写法：

```js
// 第三个参数传入 { toJSON: true }
let p = 需求请求的参数(对象类型)
this.request
    .post( 请求地址 , p, { pure: true })
    .then(res => {
        console.log(res)
    })
    .catch(err => {
        console.log(err)
    })
```
例如：

```js
// 假设拦截器定义了一个时间戳，而我们想在请求上增加一个时间戳，不使用拦截器的
this.request
    .post(
        'mock/set',
        {
            name: 123,
            timestamp: new Date().getTime(),
        },
        { pure: true }
    )
    .then(res => {
        console.log(res)
    })
    .catch(err => {
        console.log(err)
    })
}
```