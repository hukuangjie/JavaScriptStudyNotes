#### 一元运算符 ####

##### a++和++a 

	//5                2      3
    var a =1; var b = ++a + ++a; console.log(b)
    //4                 1     3
    var a =1; var b = a++ + ++a; console.log(b)
    //3                 1      2 
    var a =1; var b = a++ + a++; console.log(b)
    //4                2      2  
    var a =1; var b = ++a + a++; console.log(b)

    var a =1;
	++a; //先a=a+1 表达式返回a的值。
    a++; //先返回表达式的值a, 再a= a+1;

#### 逻辑运算符 ####

	&&  //有一个false，返回false
		//短路运算符，当前面的为false,直接返回false，这叫短路。
		var a = true && false;
		var b = "abc" && "bcd";
		var c = undefined && null; //undefined
		console.log(b);
	||  //有一个true,返回true
		var d = "abc" || "bcd" //返回abc，短路运算符。
		var e = undefined || null; //null
	!   //取反

##### && 
如果两个操作数都不是Boolean类型，如果两个值转换成Boolean类型都是true，返回第二个操作数，如果有一个操作数转换成，布尔类型是false，返回这个数。

如果两个数都是false，返回第一个操作数。

    sum(undefined,5);

    function sum(n1,n2){
        n1= n1 || 0;
        n2= n2 || 0;
        console.log(n1+n2); //5
        
    }
    function sum(n3,n4){
        console.log(n3+n4); //NaN
        
    }


#### 比较运算符 ####

== 	内容（值）相等

=== 值和类型都相等