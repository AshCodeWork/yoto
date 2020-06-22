---
layout: default
title:  proxy代理配置
parent: request请求
nav_order: 3
---
# proxy代理配置

在本地运行的时候，我们访问接口往往是会跨域的。这个时候我们运用vue-cli自带的proxy功能进行了配置。

项目默认进行了proxy的配置，使用的是测试环境的域名。配置如下：

* 使用/api 可以代理到cms的接口域名
* 使用/mall 可以代理到商城的接口域名
* 使用/oldapi 可以代理到健管服务的接口域名

想修改配置的话可以在vue.config.js中进行修改
```js
proxy: {
    '/使用的代理地址': {
        target: 目标转换地址,
        changeOrigin: true,
        pathRewrite: {
            '^/使用的代理地址': '',
        },
    },
}
```