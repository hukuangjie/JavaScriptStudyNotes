### 函数 ###

    //定义函数 0-100 相加
    function getSum() {
        var sum = 0;
        for (let i = 1; i <= 100; i++) {
            sum += i;
        }
        console.log(sum);
    }
    //调用函数
    getSum();

    // 求 n-m 之间所有的数的和
    //n,m 形式参数

    function getSum1(n, m) {
        var sum = 0;
        for (let i = n; i <= m; i++) {
            sum += i;
        }
        console.log(sum);
    }
    //传入实参
    getSum1(10, 19);

    getSum1(undefined, 10);//0 undefined 会转换为 0

    // 两个数相加
    function getsum2(a, b) {
        //如果a是空（undefined,null,0,空字符串，NaN） 让a默认为0；
        if (!a) {
            a = 0;
        }
        a = a || 0;
        b = b || 0;
        //todo 判断a和b是否为数字
        console.log(a + b);

    }


#### 函数的参数和返回值 ####

	function getSum1(n, m) {
        var sum = 0;
        for (let i = n; i <= m; i++) {
            sum += i;
        }
		//返回计算的结果
		return sum;
		//console.log("hahah"); // 不会执行，函数返回，后续的代码不会执行。
    }
		var sum = getSum(1,20);
		console.log(sum);

		console.log(getSum(1,10));


#### 函数的几种形式 ####
- 有参数 无返回值
- 有参数 有返回值
- 无参数 无返回值
- 无参数 有返回值

#### 练习： ####

求圆的面积

    //pi*r*r
    function getArea(r) {
        //过滤掉undefined null 0 "" NaN
        r = r || 0;
        //todo 判断是否是数字
        var pi = 3.1415926;
        return pi * r * r;
    }
    var area = getArea(5);
    console.log(area);

#### 函数的三要素 ####

- 1 函数的功能
- 2 函数的参数
- 3 函数的返回值


 求面积
    
    function getArea1(r) {
        //pi Math.PI
        //Math.pow() //求平方
        r = r || 0;
        return Math.PI * Math.pow(r, 2);
    }

    //求2个数中的最大值
    function getMax1(a, b) {
        return a > b ? a : b;
    }
    console.log(getMax1(66, 22))
    //求3个数中的最大值
    // 方法一
    function getMax(a, b, c) {
        return (a > b ? a : b) > c ? (a > b ? a : b) : c
    }
    console.log(getMax(12, 43, 2));
    // 方法二
    function getArea2(a, b, c) {
        return getMax1(getMax1(a, b), c);
    }
    console.log(getArea2(323, 232, 111));

    //如果一个函数内部调用另一个函数，是怎么执行的 执行的过程
    // 当fun2 执行完毕之后，会回到fun1继续往下执行。
    function fun1() {
        console.log("fun1");
        fun2();
        console.log("over");
    }
    function fun2() {
        console.log("fun2");
    }
    fun1();

当函数没有写 return 的时候回返回 undefined

    function test(){
        var a = 5;
    }
    console.log(test() ); //undefined 

函数的返回值

1. 如果 return 后面跟内容了，返回 return 后面的内容
1. 如果 return 厚点没有跟内容，返回 undefined
1. 如果函数内部没有写return，返回 undefined


		//求一数组中的最大值
		var array = [3, 5, 46, 324, 21, 11];
		
		function getMax(array) {
		    array = array || [];
		    //todo 判断array是否是数组
		    if (array.length == 0) {
		        return; //undefined
		    }
		    var max = array[0];
		    for (let i = 0; i < array.length; i++) {
		        max = max < array[i] ? array[i] : max;
		
		    }
		    //返回最大值
		    return max;
		}
		console.log(getMax(array));


#### 函数的参数 ####

1. 形参——定义函数的时候，没有实际的值，给实参占位
1. 实参——调用函数的时候，有实际的值
1. 函数调用的时候，实参的个数可以不用和实参的个数相等
2. 当函数调用 getSum() 的时候，会把实参的a和b 赋值一份传递给getSum函数

#### 函数的返回值 ####

1. 如果 return 后面跟内容了，返回 return 后面的内容
1. 如果 return 后面没有跟内容，返回 undefined，return 后面的代码不被执行。
1. 如果函数内部没有写 return，返回 undefined
1. 推荐的做法是要么让函数始终都返回一个值，要么永远都不要返回值。

#### 函数内部可以调用其他函数 ####

- 执行的过程
 1. 函数执行内部调用的函数的时候，会执行内部的函数，当内部的函数执行完毕，会继续执行当前的函数。

   
#### 函数的参数练习： ####

	 function getSum(a, b) {
        a = 100;
        return a + b;
    }
    var a = 10;
    var b = 30;
    getSum(a, b); //当函数调用getSum的时候，会把实参的a和b 赋值一份传递给getSum函数。
    console.log(getSum(a, b));

    console.log(a);

    //在JavaScript 中实参的个数可以和形参的个数不一致
    function getSum(a, b, c) {
        a = a || 0;
        b = b || 0;
        c = c || 0;
        return a + b;
    }
    var sum = getSum(1, 2);
    console.log(sum);


- 在其他语言中，有重载的概念
- 重载，函数名字相同，但是参数个数不同
- JavaScript 中没有重载的概念。
- 下面的相同名称的函数会把上面的函数覆盖
- 在 JavaScript 中不允许出现同名的函数

        function f1(a, b) {
            return a + b;
        }
        function f1(a, b, c) {
            return a + b + c;
        }
        console.log(f1(1, 2)); //报错 NaN。就近原则，没有重载。

        //不弹框，alert方法会覆盖掉系统自带alert();
        function alert(a) {
            console.log(a);
        }
        alert("abc");


####  定义函数的两种方式 ####



1 函数声明

	//问题： 为什么先调用，再声明也可以使用?
	//答:预解析，function被提前了。
    console.log(fnName(1,2));
    function fnName(a,b){
        return a+b;
    }


2 函数表达式

    var a =5;
    //Uncaught TypeError: fnName is not a function
    // 问题：为什么出错？
    // 答： fnName被提前声明。然后fnName(1,2)调用了一个空的函数。
    console.log(fnName(1,2));
    var fnName =function (a,b){
        return a+b;
    }


#### 变量的作用域： ####


变量在什么位置可以使用?

####   全局作用域： ####

在任何位置都可以访问

    var name ="a"; //全局变量
    function f1(){
        console.log(name);
    }
    f1();
    
    //局部作用域：在函数内部声明一个变量，只能在函数内部使用
    function f1(){
        var name ="aaa";//局部变量
        console.log(name);
    }
    f1();
    console.log(name);//无法访问f1函数中的name="aaa";

- 当变量超出作用域之后，变量会被销毁。
- 能不用全局变量就不用全局变量，好处是一直不被释放，坏处是一直占用内存。
- 判断是否是全局变量，可以在函数内部输出一下，在函数外部输出一下。
- 不使用 var 定义的变量是全局变量
- 变量在退出作用域之后会销毁，全局变量在关闭网页或者浏览器才会销毁

#### JavaScript中没有块级作用域 ####
    
	// 块级作用域
    {
        //代码块
        //在其他语言中，在代码块中定义的变量，外部似乎访问不到的
        //但是JavaScript中没有块级作用域
        var name ="abc";
        console.log(name); //abc
    }
    console.log(name); //abc

> JavaScript 一般在 if 判断语句和 for 循环中会使用到块级作用域。


#### 匿名函数 ####

    function fnName() {

    }
    // 匿名函数
    var myFun = function () {

    }

        // function(){
        //     console.log("test");

        // }
        // 上述代码会报错

        // 自调用函数 只能执行一次
        (function () {
            console.log("test");
        })();

**什么时候是局部变量**

- 在函数内部使用 var 声明的变量

**什么时候是全局变量**

- 只要在`<script>`标签内部定义的变量是全局变量，不是用 var 声明直接使用的变量是全局变量

`<script>`var a=50`</script>`
	
`<script>`console.log(a)`</script>`

只要是script标签就是全局变量，所以显示50。




#### 变量提升 ####

定义变量的时候，变量的声明会被提升到作用域的最上面，变量的赋值不会提升。

#### 函数提升 ####

JavaScript解析器首先会把当前作用域的函数声明提前到整个作用于的最前面 

#### 闭包： ####
 
函数内部可以访问到函数外部的变量