---
title: ng-bind-html和.的使用
date: 2019-08-02 15:02:37
tags:
- angular
- 前端开发
---
##### 1.ng-bind-html的使用

![这里写图片描述](https://imgconvert.csdnimg.cn/aHR0cDovL2ltZy5ibG9nLmNzZG4ubmV0LzIwMTcwNzIwMTczMzIxNjUx)
ng-bind-html:可以插入带标签的字符串。但是需要配合$sce使用。（缺点：标签里面不能带有angular的指令）

-------------------

<!--more-->
##### 2.$compile的使用：可以解决插入带有angular指令的字符串。

![这里写图片描述](https://imgconvert.csdnimg.cn/aHR0cDovL2ltZy5ibG9nLmNzZG4ubmV0LzIwMTcwNzIwMTczODA2NjY2)
通过$compile服务可以编译html字符串或dom对象或jqLite对象，然后得到一个编译函数，再传入$scope，就会在当前作用域进行编译，返回编译好的jqLite对象，这时就可以直接添加到文档中了（也可以先添加到文档再编译）。
编译的实质其实就是对dom对象解析，使dom对象与scope进行耦合，通过绑定可以实现数据的更新

