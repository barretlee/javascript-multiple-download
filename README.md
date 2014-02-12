javascript-multiple-download
============================

### 代码的封装以及相关 DEMO

DEMO：[javascript-multiple-download](http://rawgithub.com/barretlee/javascript-multiple-download/master/test/test.html)

### 接口的调用

提供了三个接口，支持单文件下载，多文件下载，多文件下载自定义命名。

1）单文件下载

	Downer("./file/test.txt");

2）多文件下载
	
	Downer(["./file/test.txt","./file/test.txt"]);

3）多文件下载自定义命名
	
	Downer({
		"1.txt":"./file/test.txt",
		"2.jpg":"./file/test.jpg"
	});	

文件的 URL 如 `./file/test.txt` 都可以改成 base64 或者其他格式。