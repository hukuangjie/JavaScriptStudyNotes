### 函数是一种数据类型 ###

函数是一种数据类型 function

    var num =60;
    // 1 函数是一种数据类型 function
    var myFun = function(){
        console.log("hello");
    };
    console.log(typeof myFun);

函数可以作为另一个函数的参数

    // 2 函数可以作为另一个函数的参数

    // 求两个数数学运算的结果
    function getResult(a, b, fn) {
        return fn(a, b);
    }
    var result = getResult(5, 6, function (a, b) {
        console.log(a + b); //11
        return a + b;
    });
    console.log(result); //undefined,result调用getResult中的fn(a,b)，没有返回
    

    function f1(n) {

    }
    f1(5);