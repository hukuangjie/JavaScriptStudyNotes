### 流程控制 ###

程序的三种基本结构

顺序结构
选择结构
循环结构

#####判断语句 if

语法：

	if(condition){
		//todo
	}else if{
		//todo
	}else{
		//todo
	}


    var date = new Date(); //获取当前日期
    var week = date.getDay(); //获取星期，数字0-6 0-星期天
    if(week === 0){
        console.log("星期日");
    }else{
        console.log("星期"+week);
        
    }


##### 判断语句 switch
	var a="10";
    switch(a){ //a === 10 所以不匹配
        case 10:
            console.log("10");
        case 20:
            console.log("20");
        case 30: 
            console.log("30");
        default: 
            console.log("haha"); //显示 haha
            break; 
	}

	var a=10; //数字10
    switch(a){ //a === 10 所以不匹配
        case 10:
            console.log("10");
        case 20:
            console.log("20");
        case 30: 
            console.log("30");
        default: 
            console.log("haha"); //显示10 20 30 haha
            break; 
	}


判断是用全等于 === ，跳出用 break。

##### 三元运算符 #####

    var sex =1 ;
    sex === 1? "man" : "woman"

表达式1? 表达式2 : 表达式3;

#####循环语句 for

    for (let index = 0; index < 100; index++) {
        console.log(index);
		//0 1 …… 98 99
    }


九九乘法表

	//打印99乘法表
	document.write("<table border='1px' cellpadding='0' cellspacing='0'>");
	    for (let i = 1; i < 9; i++) {
	        //外循环 控制行
	        document.write("<tr>");
	            for (let j = 0; j <= i; j++) {
	                document.write("<td>");
	                    document.write(i+"*"+j +"="+i*j);
	                document.write("</td>");
	                
	            }
	        document.write("</tr>");
	    }
	    document.write("</table>");