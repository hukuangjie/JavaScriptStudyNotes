#### 什么是对象 ####

生活中的对象，一个车、一个手机
对象具有特性和行为

#### 面向对象和基于对象 ####

面向对象：可以创建自定义的类型、很好的支持继承和多态。面向对象的语言有 c++ 、Java、 C# ...

- 面向对象的特征：封装、继承、多态
- 万物皆对象：世间的一切事物都可以用对象来描述

基于对象：无法创建自定义的类型、不能很好的支持继承和多态。基于对象的语言 JavaScrip t。

#### JavaScript中的对象 ：无序属性的集合。（属性包括方法）####

- 其属性可以包括基本值、对象或函数。对象就是一组没有顺序的的值。我们可以把JavaScript中的对象想象成键值对，其中值可以是数据和函数。

        // 1 内存开辟空间，存储新创建的对象
        // 2 会把this设置为当前对象
        // 执行函数内部的代码，设置对象的属性和方法
        // 4 返回新创建的对象
        var s1 = new Student("zs", 19, 1, 100);
        s1.sayHi();

        console.log(s1.name);
        console.log(s1["name"]);

        // 对象：无序属性的集合，我可以把对象看成键值对。
        var o =new Object();
        o["name"] = "zs";
        console.log(o.name);
        
        for (let i = 0;  i < 10;i++) {
            // 动态给对象增加属性
            o["n"+i] = i;
        } 

#### new Object() ####

- new 后面调用函数，我们称之为构造函数。
- Object() 我们把它视为一个构造函数，构造函数的本质就是一个函数，只不过构造函数的目的是为了创建新对象，为新对象进行初始化（设置对象的属性）。

自定义构造函数 --- 构造函数：构造一个对象，并且返回的函数

调用构造函数 new Object();
    
        function Student(name, age, sex, score) {
            this.name = name;
            this.age = age;
            this.sex = sex;
            this.score = score;
            //对象的方法
            this.sayHi = function () {
                console.log("大家好，我是" + this.name);
            }
        }

#### this ####

- 谁调用，this 就是谁 
 
		function test(){
            // 此时this是window，因为是window调用的此函数。
            console.log(this);
	    }
        test();
        window.test();// 一样的效果