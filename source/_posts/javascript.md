title: javascript
date: 2012-10-12 15:11:10
updated: 2012-12-25 15:22:33
categories: [javascript, nodejs]
tags: [js, node, es6, grunt]
keywords: Javascript, NodeJS, ES6
description: 你好，你了解一个英雄孤独的内心吗？
---


# Apache Thrift - 可伸缩的跨语言服务开发框架
Apache Thrift 是 Facebook 实现的一种高效的、支持多种编程语言的远程服务调用的框架。本文将从 Java 开发人员角度详细介绍 Apache Thrift 的架构、开发和部署，并且针对不同的传输协议和服务类型给出相应的 Java 实例，同时详细介绍 Thrift 异步客户端的实现，最后提出使用 Thrift 需要注意的事项。

<!--more-->

## 前言：
目前流行的服务调用方式有很多种，例如基于 SOAP 消息格式的 Web Service，基于 JSON 消息格式的 RESTful 服务等。其中所用到的数据传输方式包括 XML，JSON 等，然而 XML 相对体积太大，传输效率低，JSON 体积较小，新颖，但还不够完善。本文将介绍由 Facebook 开发的远程服务调用框架 Apache Thrift，它采用接口描述语言定义并创建服务，支持可扩展的跨语言服务开发，所包含的代码生成引擎可以在多种语言中，如 C++, Java, Python, PHP, Ruby, Erlang, Perl, Haskell, C#, Cocoa, Smalltalk 等创建高效的、无缝的服务，其传输数据采用二进制格式，相对 XML 和 JSON 体积更小，对于高并发、大数据量和多语言的环境更有优势。本文将详细介绍 Thrift 的使用，并且提供丰富的实例代码加以解释说明，帮助使用者快速构建服务。


### 一个简单的 Thrift 实例
本文首先介绍一个简单的 Thrift 实现实例，使读者能够快速直观地了解什么是 Thrift 以及如何使用 Thrift 构建服务。
创建一个简单的服务 Hello。首先根据 Thrift 的语法规范编写脚本文件 Hello.thrift，代码如下：
清单 1. Hello.thrift

```
 namespace java service.demo 
 service Hello{ 
  string helloString(1:string para) 
  i32 helloInt(1:i32 para) 
  bool helloBoolean(1:bool para) 
  void helloVoid() 
  string helloNull() 
 }


 ```


# javascript
1 javascript javascript javascript
## javascript
2 javascript javascript javascript
### javascript
3 javascript javascript javascript
#### javascript
4 javascript javascript javascript
##### javascript
5 javascript javascript javascript
###### javascript
6 javascript javascript javascript
####### javascript
7 javascript javascript javascript