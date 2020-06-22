---
title:  介绍
---

# 介绍

项目初衷：这个项目是用于快速构建pc项目的，面对新项目的创建，我们希望在文档上有个统一的说明，开发的时候有个统一的工具。比如：项目中我们需要`axios`，需要使用拦截器进行进一步的封装，对新手来说是费时费力的，我希望在一开始这些基础功能就存在，免去重新搭建项目的麻烦，也统一了项目结构便于维护。

整个项目基于`vue-cli 4.x`的版本。添加了一些必备插件，新的vue-cli 拥有更多新的功能。

## 环境要求

>关于vue-cli旧版本

Vue CLI 的包名称由 vue-cli 改成了 @vue/cli。 如果你已经全局安装了旧版本的 vue-cli (1.x 或 2.x)，你需要先通过 npm uninstall vue-cli -g 或 yarn global remove vue-cli 卸载它。

> Node 版本要求

Vue CLI 需要 `Node.js 8.9` 或更高版本 (推荐 8.11.0+)。你可以使用 [nvm](https://github.com/nvm-sh/nvm) 或 [nvm-windows](https://github.com/coreybutler/nvm-windows) 在同一台电脑中管理多个 Node 版本。

[vue-cli 的文档说明](https://cli.vuejs.org/zh/guide/prototyping.html)

## 使用方法

### 第一步
由于是公司内部项目，项目请从公司wiki下载：
[项目下载](https://wiki.miaomore.cn/pages/viewpage.action?pageId=42054476)

### 第二步

进入项目根路径执行命令：

```
npm install
```

如果有报错，请联系项目负责人刘鑫

### 第三步

本地运行：

```
npm run dev
```

或

```
npm run serve
```

开发环境构建

```
npm run build:dev
```

测试环境构建

```
npm run build:test
```
线上环境构建

```
npm run build:prod
```