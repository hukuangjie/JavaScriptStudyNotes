### 编译和解释 ###

    var a = 0;
	console.log(a);
	var b = "abc";

编译： 一次性把代码转换成 CPU 可以看懂的语言，一行一行执行；

解释：一行一行解析，解析一行执行一行；



> C、 C++、 C#、 Java 属于编译型语言。

在速度方面编译型语言更快，所以 JavaScript 存在性能问题，但是因为计算机性能越来越好，所以 JavaScript 存在的性能问题几乎被忽略了。

JavaScript 是脚本语言：不需要编译，直接运行时边解析边执行的语言；

JavaScript 是一种客户端的脚本语言。


### Script 标签的属性 ###

1. type="text/javascript"

2. src=""

3. defer="defer"

4. async=""async

> async: 异步，多个人同时做多件事
>  
> sync: 同步，一个人有序的做多件事。

如果 Script 标签中存在 async，则异步执行。值可以省略,`<script async></script>`，立即异步下载外部 js，下载完毕后立即执行。

defer: 异步下载JavaScript，等全部代码都执行完才执行