---
title: 在 ESLint 中配置 Vue.js 的语法
date: 2017-04-03 10:19:52
tags: 
 - "Vue.js"
 - "前端"
categories: 
 - "Vue.js"
---
1. 安装项目依赖 `npm install --save-dev eslint-config-vue eslint-plugin-vue`

2. 在项目根目录下创建 `.eslintrc` 文件

3. 在文件中添加如下字段
``` javascript
    "extends": "vue"
``` 