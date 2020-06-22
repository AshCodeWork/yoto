---
layout: default
title:  window上的工具js
parent: 全局js
nav_order: 1
---

# window上的工具js

## window.Global

### window.Global.env

用法：
```js
window.Global.env
```
返回当前的环境，来自环境变量`VUE_APP_ENV`

### window.Global.deviceType

用法：
```js
window.Global.deviceType //返回  1 苹果 2 安卓
```
返回当前的设备类型：1 苹果 2 安卓

## $开头的方法

### window.$getHashUrlQuery

获取hash模式下的url参数值

用法：

```js
// (name:string) => value:string
win.$getHashUrlQuery(参数值)
```
例如:

```js
// url: https:wwww.miaohealth.net/#/detail?id=123
win.$getHashUrlQuery('id') //123
```

### window.$getUrlQuery

获取非hash下的url参数值

用法：

```js
// (name:string) => value:string
win.$getUrlQuery(参数值)
```
例如:

```js
// url: https:wwww.miaohealth.net/detail?id=123
win.$getUrlQuery('id') //123
```

### window.$timer

自己封装的定时器。可以设置setInerval, setTimeout。可以获取当前已经使用这个方法开启的定时器

#### 获取Inerval定时器的所有key

使用：
```js
// () => number[]
window.$timer.intervalKeys()
```
#### 获取Timeout定时器的所有key

使用：
```js
// () => number[]
window.$timer.timeoutKeys()
```
### 设置setInterval定时器

使用方式同原生的一样，接受两个参数: 参数一：回掉方法，参数二，定时时长(ms)；返回这个定时器的key

例如：
```js
// 每隔1s 打印123
window.$timer.setInterval(()=> {
    console.log(123)
}, 1000)
```

### 设置setTimeoutl定时器

使用方式同原生的一样，接受两个参数: 参数一：回掉方法，参数二，定时时长(ms)；返回这个定时器的key

例如：
```js
// 1s 后打印123
window.$timer.setTimeout(()=> {
    console.log(123)
}, 1000)
```
### 清除`timeout`定时器

清除所有使用`$timer`创建的timeout定时器

```js
window.$timer.clearTimeout()
```

### 清除`interval`定时器

除所有使用`$timer`创建的interval定时器

```js
window.$timer.clearInterval()
```

### window.$setCookie 

设置cookie
```js
/**
* [setCookie description]
* @method setCookie
* @param {String} name Cookie键名
* @param {String} value Cookie键值
* @param {Int} days Cookie有效期天数
* @param {String} path Cookie有效路径
* @param {String} domain Cookie有效域
* @param {Boolean} secure 是否安全Cookie
*/
window.$setCookie(name, value, days, path, domain, secure)
```
例如：

```js
// 设置.miaoehealth.net域名下的key 为name，值为123的cookie，有效期10天

window.$setCookie('name' , 123, 10, '/', '.miaohealth.net', false);
```
### 获取cookie

获取cookie的值

```js
/**
* 获取cookie值
* @param name
* @returns {*}
*/
window.$getCookie(name)
```
例如：

```js
// 获取上例中存的cookie
window.$getCookie('name')
```

### 清除cookie

```js
/**
* @param {array} cookie的名字组成的数组
* @param {string} open_appid行业客户id
*/
window.$clearCookie([], open_appid)
```