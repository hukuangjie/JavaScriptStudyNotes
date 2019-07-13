### 函数经典面试题 ###

1、----------------------------

    // 解析器：
    // 预解析 全局作用域
    // 先找var 、function 和参数
    // 找到var和function之后，会把var和function提前
    //num fun
    // 从上到下一行一行执行代码
    // num = 10;
    // fun();
    // 执行到fun后，进入局部作用域
    // 预解析
    // num
    // 从上到下一行一行执行代码

    var num;
    function fun() {
        var num;
        console.log(num);
        num = 20;
    }
    num = 18;
    // var num = 10;
    // fun();
    // function fun() {
    //     console.log(num);
    //     var num = 20;
    // }



2、-------------------------------------------

    var a = 18;
    f1();
    function f1() {
        var b = 9;
        console.log(a);
        console.log(b);
        var a = '123';
    }

    var a;
    function f1() {
        var b;
        var a;
        b = 9;
        console.log(a);
        console.log(b);
        a = '123';
    }
    a = 18;
    f1();


    var a=18;
    function f1(){
        //先在当前作用域下找变量a，如果当前作用域没有变量a，会去上一级作用域找变量a。
        // 如果找到了，就获取a的值。如果都找不到，会显示a is not defined。
        console.log(a);
    }
    f1();

3、------------------------------------

    // 解析器
    // 全局作用域 预解析 var function 参数
        // 预解析
            // function f1()
        // 一行一行执行代码
            // f1() 局部作用域
                // 预解析
                    // var a;
                // 一行一行解析代码

    function f1(){
    // a 局部变量
    // b c全局变量
    var a;
    a=b=c=9;
    console.log(a);
    console.log(b);
    console.log(c);
    }
    f1();
    console.log(c);
    console.log(b);
    console.log(a);


    // f1();
    // console.log(c);
    // console.log(b);
    // console.log(a);
    // function f1(){
    //     var a=b=c=9;
    //     console.log(a);
    //     console.log(b);
    //     console.log(c);
    // }
