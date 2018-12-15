---
title: angular-cli
date: 2018-11-09 10:12:43
tags: 
 - angular命令
categories:
- angular
---
## 写在前面
  最近闲着没事，就折腾了一下angular-cli,官方文档[anguar-cli](https://cli.angular.io), 由于许多东西还在研究，后续持续更新...

## angular-cli 命令合集
### 项目生成
```bash
$ npm install -g @angular/cli   "全局安装"
$ ng new myProject   "创建新项目 myProject 是项目文件名"
$ cd myProject   "进入 myProject 文件夹"
$ ng server   "server/serve都可以，但是我碰到serve启动不成功的情况，这可能和版本更新有关。默认情况下ng会安装依赖，不需要npm install 就可以直接启动"
$ ng new myProject --routing   "这个命令可以直接生成带有路由的项目，一般都会用的到，当然除了--routing还有其他的参数--prefix组件的前缀"
```
### 创建项目具体模块
``` bash
$ ng generate class my-new-class              // 新建 class
$ ng generate component my-new-component      // 新建组件
$ ng generate directive my-new-directive      // 新建指令
$ ng generate enum my-new-enum                // 新建枚举
$ ng generate module my-new-module            // 新建模块
$ ng generate pipe my-new-pipe                // 新建管道
$ ng generate service my-new-service          // 新建服务
```
  简写(使用命令的好处是不用在文件来回引入，引入文件很多，很容易遗漏)
```
$ ng g cl my-new-class        // 新建 class
$ ng g c my-new-component     // 新建组件
$ ng g d my-new-directive     // 新建指令
$ ng g e my-new-enum          // 新建枚举
$ ng g m my-new-module        // 新建模块
$ ng g p my-new-pipe          // 新建管道
$ ng g s my-new-service       // 新建服务
```
##### 说明
***
    如果有多个模块，使用命令创建组件要指定组件所属的模块，不指定会默认创建app.module的组件，但是有时候可能会报错。
```bash
$ ng g c my-new-component --module=app-routing    // 创建属于路由模块的组件，在路由模块会自动引入该模块
$ ng g c my-new-component // 如果不指定模块默认所属在app.module模块中 
  
```
***






