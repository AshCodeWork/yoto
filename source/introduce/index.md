---
title:  介绍
---

# 介绍

项目初衷：这个项目是用于快速构建移动端项目的，面对新项目的创建，我们希望在文档上有个统一的说明，开发的时候有个统一的工具。比如：项目中我们需要`axios`，需要使用拦截器进行进一步的封装，对新手来说是费时费力的，我希望在一开始这些基础功能就存在，免去重新搭建项目的麻烦，也统一了项目结构便于维护。


## 使用方法

### 第一步
由于是公司内部项目，项目请从公司wiki下载：[项目下载](https://wiki.miaomore.cn/pages/viewpage.action?pageId=42054476)

wiki中也有项目对应的git地址，对应git地址可以下载对应版本的模版。

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

开发环境构建

```
npm run build dev
```

测试环境构建

```
npm run build test
```
线上环境构建

```
npm run build prod
```