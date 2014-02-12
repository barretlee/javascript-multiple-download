JavaScript多文件下载
============================

### 代码的封装以及相关 DEMO

DEMO1：[javascript-multiple-download](http://rawgithub.com/barretlee/javascript-multiple-download/master/test/test.html) (HTTPS，第三个有bug)

DEMO2：[javascript-multiple-download](http://qianduannotes.duapp.com/demo/javascript-multiple-download/test/test.html) (HTTP，测试正常)
      
Bug 说明，经过一番细节处理之后，基本兼容各个浏览器，我把代码放在 https://raw.github.com 上托管，可能因为是 https 传输，第三个测试中报错了，报错的具体内容是：HTTPS 安全受到 http://rawgithub.com/barretlee/javascript-multiple-download/master/file/test.jpg 的威胁，而 test.txt 文件没有报错。放到 http 协议下测试运行结果是可观的。（这点我没有去深究，肯定是有深层安全方面原因的，难道就因为他是 jpg图片格式？）后面的 demo 我放在 BAE 上，没有问题，不过没测试 safari 和 opera。

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
