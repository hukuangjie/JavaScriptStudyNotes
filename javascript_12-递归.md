### 递归 ###

    // function f1(){
    //     console.log("hello");
    //     f1();
    // }
    // f1();

    // 给递归添加结束的条件
        var i = 0; //如果把这行代码放到函数体里，会无限循环。
        function f1() {
            console.log("从前有座山，山上有个庙....");
            i++;
            if (i < 10) {
                f1();
            }
        }
        f1();

求n个数的累加

    // 5+getSum(4)
    // 5+4+getSum(3)
        function getSum(n) {
            if (n <= 0) {
                return 0;
            }
            if (n === 1) {
                return 1;
            }
            return n + getSum(n - 1);
        }

一个数的各位数之和

        // 123
        // 123 %10 =3   123/10=12.3
        // 12%10=2      12/10=1.2
        // 1%10=1       1/10=0.1

        function getSum(n) {
            // 结束的条件
            if (n < 10) {
                return n;
            }
            // 123第一个余数3 + 12 各个数字之和
            return n % 10 + getSum(parseInt(n / 10));
        }
		//getSum(1234);
		//4 + getSum(123);
		//4 + 3 + getSum(12);....

求Fibonacci 的第n个数

            // 1 1 2 3 5 8 13 21
            function getF(n) {
                // if (n<=0) {
                //     return -1;
                // }
                if (n == 1 || n == 2) {
                    return 1;
                }
                return getF(n - 1) + getF(n - 2);
            }
            console.log(getF(5));