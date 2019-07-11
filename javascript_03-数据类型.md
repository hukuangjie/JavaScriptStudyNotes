### 数据类型 ###

JavaScript 和 Java 一样，也是有基本数据类型的。但也是有区别的。
#### JavaScript中的数据类型
#####简单（基本、值）数据类型
- number
- string
- boolean
- undefined、null
#####复杂（引用）数据类型
- Object、Array、Date 等

##### 查看当前变量的数据类型
-  typeof name
-  typeof (name)

#### 数值字面量

##### 字面量
固定的值，让你从“字面上”理解含义

数值字面量

    var age = 18; //数值字面量，18为字面量

#### number类型

十进制

十六进制
var num = 0xA

八进制

#### 浮点数
var n = 5e-324;

浮点数值的最高精确度是17位小数，在进行算术计算时，其精确度远远不如整数。

	var result = 0.1+0.2 //结果不是0.3 而是0.300000000000000004

	0.1+0.2 == 0.3 //false
	0.1+0.3 == 0.4 //true
	
	0.07 * 100 ；7.00000000000000001

想比较的话只能 0.1 * 10 ，然后 parseInt 转换，然后再相加比较。

> 永远不要测试某个特定的浮点数值是否相等。


#### 数值范围 ####

内存限制，ES无法保存世界上所有的数值

- 最小值：Number.MIN_VALUE,5e-324
- 最大值：Number.MAX_VALUE,1.7976931348623157e+308
- 无穷大：Infinity
- 无穷小：-Infinity

#### 数值检测 ####

NaN: not a number. 非数值

isNaN(); //是数字返回false;

    console.log(parseInt("abc"));//NaN
    
    console.log(parseInt("abc"/10));//NaN

    var num = prompt("请输入一个数字")
    if(isNaN(num)){
        console.log("不是一个数字");
    }else{
        console.log("是一个数字");
        
    }


#### String 类型 ####

字符串字面量

     var name = "zhangsan"; // "zhangsan"是字面量

 字符串用引号引起，单引号和双引号是一样的。

获取字符的长度用length

    var name="hukj"; alert(name.length); //4

#### 转移符 ####

	console.log("\"Ancona\"");
> \n 换行
> \t 制表符
> \b 空格
> \r 回车
> \f 进纸
> \\ 斜杠
> \' 单引号
> \" 双引号

#### 字符串的不可变 ####
    var str ="hello";
    str = str+"world";
    console.log(str);

当执行第二行代码时，会在内存空间中开辟新的栈，然后通过垃圾回收机制来清理原来的str。这就是所谓的字符串不可变。

#### 字符串拼接 ####

    var a ='100';
    var b =100; //b中的 number：100 会自动转型为str
    console.log(a+b); //100100
    console.log(a-b); //0

#### Boolean 类型 ####

Boolean 类型有两个字面量：true 和 false；
    var result = Boolean("a");
    console.log(result); //true

Boolean 当为空字符串，0，NaN，null，undefined 时，为false；

#### Undefined 类型 ####

undefined 是 Undefined 的字面量；表示变量未赋值。

    var message;
    console.log(message);// undefined

	var a;				//undefined
	if(a){				//false
		alert('有值')
	}else{
		alert('无值')	//显示
	}

a未赋值为undefined，undefined在Boolean中转换为false；