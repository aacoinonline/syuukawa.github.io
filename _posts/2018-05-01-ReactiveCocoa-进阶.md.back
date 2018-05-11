---
layout:     post
title:      ReactiveCocoa 进阶
subtitle:   函数式编程框架 ReactiveCocoa 进阶
date:       2018-05-01
author:     BY
header-img: img/post-bg-ios9-web.jpg
catalog: true
tags:
    - iOS
    - ReactiveCocoa
    - 函数式编程
    - 开源框架
---
# 前言

# 常见操作方法介绍


#### 操作须知

所有的信号（RACSignal）都可以进行操作处理，因为所有操作方法都定义在RACStream.h中，因此只要继承RACStream就有了操作处理方法。
#### 操作思想

运用的是Hook（钩子）思想，Hook是一种用于改变API(应用程序编程接口：方法)执行结果的技术.

Hook用处：截获API调用的技术。

有关Hook的知识可以看我的这篇博客[《Objective-C Runtime 的一些基本使用》](http://www.jianshu.com/p/ff114e69cc0a)中的 *更换代码的实现方法* 一节,

Hook原理：在每次调用一个API返回结果之前，先执行你自己的方法，改变结果的输出。

#### 操作方法

#### **bind**（绑定）- ReactiveCocoa核心方法

**ReactiveCocoa** 操作的核心方法是 **bind**（绑定）,而且也是RAC中核心开发方式。之前的开发方式是赋值，而用RAC开发，应该把重心放在绑定，也就是可以在创建一个对象的时候，就绑定好以后想要做的事情，而不是等赋值之后在去做事情。

列如，把数据展示到控件上，之前都是重写控件的 `setModel` 方法，用RAC就可以在一开始创建控件的时候，就绑定好数据。