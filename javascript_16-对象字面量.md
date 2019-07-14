
JSON与对象字面量相似，仅仅是属性需要使用双引号引号引起。
json是描述数据的一种规范

#### 什么是JSON ####

- JavaScript Object Notation (JavaScript 对象表示形式)
- JavaScript的子集

#### JSON和对象字面量的区别 ####

- JSON的属性必须用双引号引号引起来，对象字面量可以省略
- var o = {}; 对象字面量  {}JSON


        var arr = []; //数组的字面量

        var arr = new Array(); //使用构造函数创建数组

        //使用构造函数创建对象
        var o = new Object();
        //对象的字面量
        var o = {
            name: "hkj",
            age: 18,
            sex: "未知",
            salary: 100,
            dog: {},
            cats: {},
            sayHi: function () {
                console.log("大家好，我是" + this.name);
            },
        }

        var o = {
            "name": "hkj",
            "age": 19,
        };


        var arr = new Array();
        //输出对象的属性和方法
        //有些系统提供的对象的属性和方法无法遍历，原因属性和方法被设置为不可枚举
        for (var key in arr) {
            //key 是对象的属性 键
            console.log(key);
        }

        console.log(o);
        for (const key in o) {
            if (o.hasOwnProperty(key)) {
                console.log(key)
                console.log(o.key); //获取o对象的key属性，因为key属性未定义，所以输出undefined
                console.log(o[key]);

            }
        }

forin 练习

    var object = {};
    for (let index = 0; index < 10; index++) {
        object[index] = index * 2;
    }
    for (const key in object) {
        if (object.hasOwnProperty(key)) {
            console.log(key + "====" + object[key]);
        }
    }