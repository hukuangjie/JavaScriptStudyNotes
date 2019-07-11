### 类型转换 ###

#### 掌握三种类型的转换 ####

- 转换成字符串类型
- 转换成数值类型
- 转换成布尔类型

#### 转换成字符串

1.几乎每一个值都有 toString() 方法,除了 null 和 undefined。

    var age =18;
    var ageString = age.toString();
    console.log(ageString); // "18"
    
    var a = true;
    var aString =a.toString();
    console.log(aString) // "true"

数据类型的 toString()，可以携带一个参数，输出对应进制的值

    var a =10;
    console.log(a.toString(2)); //"1010"
    console.log(a.toString(16)); //"a"
    ...

2.String() 函数，可以把 null 和 undefined 转换为字符串。

3.使用拼接字符串。

	var age = 18;
	str = age + "岁"
	console.log(str);

#### 转换成数值类型
三种把值转换成数值类型的函数：Number()、 parseInt()、 parseFloat()；
#### Number ####
Number() 可以把任意的值转为数值，如果要转化的字符串中有任意一个不是数值的字符，返回 NaN。

	var num1 = Number(true); //true返回1 ，false返回0；
	var num2 = Number(undefined); //返回NaN
	var num3 = Number("hello"); //返回NaN
	var num4 = Number(" "); //空字符串返回0
	var num1 = Number("abc123"); //返回NaN

只要字符串中有任意一个字符不是数值，就会返回 NaN。（没错，就是这么严格）

##### parseInt

把字符串转换为整数

    parseInt("12.3abc");//返回 12，如果第一个是数字会解析到第一个非数字后停止。
    parseInt("abc123"); //返回 NaN，如果第一个字符不是数字或符号就返回NaN；
    parseInt(" "); //空字符串返回NaN，Number("")返回0；

parseInt() 可以传递两个参数，第一个是要转换的字符串，第二个是要转换的进制。

    var num1 = parseInt("0xA"); //10
    var num2 = parseInt("A"); //NaN
    
    var num3 = parseInt("A",16); //10
    var num4 = parseInt("10",16); //16

#### parseFloat
parseFloat() 把字符串转换为浮点数

parseFloat() 和 parseInt 非常相似，不同之处在于

- parseFloat()会解析第一个 `.` ，遇到第二个`.`或者非数字结束
- parseFloat()不支持第二个参数，只能解析 10 进制数。
- 如果解析的内容只有整数，解析成整数。

#### 转换为 Boolean 类型

两种方式

- Boolean() 函数
- var b = Boolean("abc");//true

流程控制语句会把后面的值隐式转换成布尔类型。
例如：

     var message;
    if(message){ //会自动把message转换为false
    	//todo 	
    }

转换为 false 的值: false,"",0,null,undefined;

var b = !!"123"; //123为true, !"123" 为false， !!"123"为true。