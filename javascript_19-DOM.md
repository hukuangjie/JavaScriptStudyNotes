 #### DOM ####

DOM: 文档对象模型（Document Object Model），又称为文档树模型。是一套操作HTML和XML文档的API。

DOM可以把HTML和XML描述为一个文档树。树上的每一个分支都可以视为一个对象，通过DOM可以添加、修改和移除文档上的某一部分。

#### DOM的相关概念 ####
- DOM就是把HTML视为一个层次结构（树形结构）的文档
- 文档（Document）：就是指HTML或者XML文件
- 节点（Node）：HTML文档中的所有内容都可以称之为节点
- 元素（Element）：HTML文档中的标签可以称之为元素
- 文档元素（根元素）：文档的第一个元素，HTML文档元素就是`<html>`
- 文本节点
- 属性节点


- 父节 点 parent
- 子节点 child
- 兄弟节点 silbing

DOM可以做什么

- 找对象（元素）
- 设置元素的属性
- 设置元素的样式
- 动态创建和删除元素
- 事件--触发响应
	- 事件源（事件的触发者）
	- 事件名称
	- 事件响应程序

DOM初体验


`<a onclick="alert('aaa'); return false"></a>` 取消a标签的默认行为。
找到id是link1的dom对象（a标签）

要等到标签生成之后，再来获取对应的dom对象。所以要注意`<script>`在文档中的位置。

	var link1 = document.getElementById("link1");
	
	//给link1注册单击事件
	//事件的三要素
		//事件源--事件的触发者link1
		//事件处理程序--onclick == 匿名函数
		//事件名称 click
	
	link1.onclick = function(){
		alert("hahah");
		//取消a标签默认行为的执行
		return false;
	}

给a标签注册多个事件

	//1 能够点击
		//获取页面上的a标签
		document.getElementById();

		var links =document.getElementsByTagName();
		for (var i = 0; i<links.length;i++){
			var link =links[i]; //获取每一个a标签
			//给link对象注册时间
			link.onclick = function(){

				//....
				//获取 要改变的dom元素对象
				//获取 要改变的动作
				//替换 
								
				//取消a的默认行为
				return false;
			}		
		}
	//2 改变图片
	
	//3 改变标题

 
