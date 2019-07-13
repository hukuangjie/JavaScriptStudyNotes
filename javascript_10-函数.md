### 函数 ###

    //定义函数0-100相加
    function getSum() {
        var sum = 0;
        for (let i = 1; i <= 100; i++) {
            sum += i;
        }
        console.log(sum);
    }
    //调用函数
    getSum();

    // 求n-m之间所有的数的和
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

