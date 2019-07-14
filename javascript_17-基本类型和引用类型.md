#### 基本类型 ####

直接存储值

- Number 、 String 、Boolean
- undefined、null


#### 引用类型 ####

存储引用

-Object、Array、Date、函数

包装基本类型——引用类型


    function Student(name,age,salary){
        this.name =name;
        this.age = age;
        this.salary =salary;
    }
    var s1 = new Student("zs",19,199);
    var s2 = s1;
    console.log(s2.name);

    s1.name = "hkj";
    console.log(s2.name);
    
    //基本类型和复杂类型作为函数的参数

    // 基本类型作为函数的参数
    // 当基本类型作为函数的参数的时候，函数内部对参数的修改，不会修改外部的变量
    function f1(a){
        a=100;
    }
    var x=1;
    f1(x);
    console.log(x); //1
    
    //复杂类型作为函数的参数

    function f2(stu){
        // var stu = new Student();
        stu.name="xxx";
    }
    var s= new Student("zs",18,100);
    f2(s);
    console.log(s.name); //xxx
