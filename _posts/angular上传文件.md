---
title: angular上传文件
date: 2019-08-02 14:58:53
tags:
- angular
- 前端开发
---
##### 1.angular上传文件
```
var uploadFile=document.querySelector("#uploadFile").files[0];
//jquery获取$("#uploadFile").prop("files")[0];
var formData = new FormData();
formData.append('fileTypeId', fileType);//其他需要上传的字段
formData.append('file', uploadFile);//文件
 $http({
           url:ex.websitemonitor+"files/upload",
           method:"post",
           headers: {'Content-Type': undefined},//使用angular上传一定要加上这一句，不然传给后台的是空的。
           data: formData,
        }).success(function (result) {}

```
##### 2.ajax上传文件
```
var uploadFile=document.querySelector("#uploadFile").files[0];
//jquery获取$("#uploadFile").prop("files")[0];
var formData = new FormData();
formData.append('fileTypeId', fileType);//其他需要上传的字段
formData.append('file', uploadFile);//文件
$.ajax({
	url:"",
	type:"post",
	data:formData,
	success:function(){},
	error:function(){}
	})//没有什么特别需要注意的
```