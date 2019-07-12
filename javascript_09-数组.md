### 数组 ###

	//数组
    // var array = new Array();
    // array[0]="zs";
    // array[1]="ls";
    var name = "ml"
    var array =["zs","ls","mw"];
    console.log(array[0]);
    console.log(array.length);
    
    for (let index = 0; index < array.length; index++) {
        const element = array[index];
        console.log(element);
    }


输入 0-100 的数组

    var array=[];
    console.log(array.length);
    for (let index = 0; index <=100; index++) {
        array[index] = index;
    }
    console.log(array);

#### 数组的 length ####

 数组中的值如果没有赋值，就是 undefined。

    //数组输出 0-100 的所有的奇数的数字
    //方法一：
    var array = [];
    var j = 0;
    for (let index = 1; index <= 100; index++) {
        if (i % 2 !== 0) {
            array[j] = i;
            j++;
        }
    }
    console.log(array);

    // 方法二
    //每当我们忘数组中新增一个项，都会更改length属性
    var array = [];
    for (let index = 1; index <= 100; index++) {
        if (i % 2 !== 0) {
            array[array.length] = i;
        }
    }

0-100 中能被 3 整除的数，输出出来，一共有多少个。

    var array=[];
    for (let index = 1; index <= 100; index++) {
        if (index %3 ==0) {
            array[array.length]=index; 

        }
    }
    console.log(array);
    console.log(array.length);
    
    array.length = 1;
    console.log(array);

> 第一次运行的时候 length = 0,也就是第一位是 index。第二次运行的时候，length = 1。

数组：数据的有序列表。可以存放任意类型的数据，数组的大小可以动态调整。

#### 创建数组两种方式： ####

方式1：数组字面量

	var arr1 = [];
	var arr2 = [1,2,3];

方式2：Array 的构造函数

	var arr3 = new Array(); //创建一个空数组
	var arr4 = new Array(10); //创建一个长度为 10 的数组
	var arr5 = new Array("a","b","c"); //创建一个包含 3 个字符串的数组 


一个数组 ["abc", "aaa", "aaa"];  输出 abc|aaa|aaa

	//abc|aaa|aaa
	var array = ["abc", "aaa", "aaa"];
	var sperator = "|";
	var str = array[0];
	for (let index = 1; index < array.length; index++) {
	    str += sperator + array[i];
	}
	console.log(str);

> 当需要合成一个新的数组的时候，可以巧妙的运用array.length 来避免造成数组的 index 未定义，出现 undefined。


  
一题经典的冒泡排序：

    var array = ["13", "43", "53", "1", "41", "65"]
    //控制循环次数
    var s = 0;
    var s1 = 0;
    //为什么isSort = true 不能写在外循环
    //因为 交换位置 isSort = false。 isSort 的值永远是 false。
    //我们要检测的是某一趟是否交换位置
    for (var i = 0; i < array.length - 1; i++) {
        var isSort = true; //假设排序ok
        //控制两两比较的次数
        for (var j = 0; j < array.length - 1 - i; j++) {
            //两两比较 从小到大
            var isSort = false;
            // 如果交换位置，说明还没有排序好，如果不交换位置，说明排序好
            if (array[j] > array[j + 1]) {
                //交换位置
                var tmp = array[j];
                array[j] = array[j + 1];
                array[j + 1] = tmp;
            }
            s++; //记录内循环次数
        }
        s1++; //记录外循环次数
        if (isSort) {
            //如果排序好了
            break;
        }
    }
    console.log(s);
    console.log(s1);
    console.log(array);
    console.log(array.length);

运用了一个检测是否排序完成的 isSort 来减少比较次数。