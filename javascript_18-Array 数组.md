#### 数组 ####

数组-引用类型，JavaScript中的内置对象

Array对象的属性

- length 获取数组的长度（元素个数）

 检测数组

- instanceof 
- Array.isArray() //h5新增

常用方法

- concat()  //把参数拼接到当前数组
- slice() // 从当前数组中截取一个新的数组，不影响原来的数组，参数start从0开始，end从1开始
- splice() // 删除或替换当前数组的某些项目，参数start，deleteCount，options（要替换的项目）
位置方法
- indexOf()、lastIndexOf() //如果没找到返回-1

迭代方法 不会修改原数组 html5
- every()、 filter() 、forEach() 、map()、some()


#### instanceof 检测对象类型 ####

    // instanceof 关键字 是否是谁的对象

    var o =[];

    console.log(o instanceof Array);

    function f1(arr){
        //检测参数是否合法
        arr = arr || [];
        //检测arr是否是一个数组
        if (!(arr instanceof Array)) {
            return; //如果为false 就跳出
        }
    }

join

    var array = [3,5,7,8,9];
    console.log(array.toString());//3,5,7,8,9
    //toString 内部调用了join()
    console.log(array.join()); //3,5,7,8,9
    console.log(array.join("|")); //3|5|7|8|9


#### typeof和instanceof 的区别 ####

1. typeof可以获取任意变量的类型
    - 任意类型的对象使用typeof获取到的都是object
2. instanceof只能判断对象的类型

	    var o = new Array();
	    console.log(typeof o);
	    console.log(o instanceof Array);