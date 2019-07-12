### while 和 do while ###

- for 当循环次数已知
- while 先判断再执行
- do while 先执行一次再判断

		//1-100 之间所有数字的和
		
		//while
		// var i = 1;
		// var sum =0;
		// while(i<=100){
		// sum +=i;
		// i++;
		// }
		// console.log(sum);
		
		//do while
		var i =1;
		var sum =0;
		do{
		sum+=i;
		i++;
		}while(i<=100);
		console.log(sum);
		
#### while 的练习
任意输入一个整数，求它的位数
		
		var number = Number(prompt("请输入数字")); //如果使用parseInt(); 出现 123abc 也不会报错
		if(number){
		var i =1;
		while (number >= 10) {
		number = number/10; //可以不写parseInt();自动转型
		i++;
		}
		console.log(i);
		}else if(number===0){
		console.log("1");
		}else{
		console.log("重新来");
		
		}
		
####do while 练习
输入一个整数，翻转输出这个数的每一个数字.
		
	//判断用户输入的数字是否合法
	//翻转输出每一个数字
	
	var number =Number(prompt("请输入一个数字"));
	// 整数 0 NaN
	if (number) {
	number =parseInt(number);
	//翻转输出每一个数字
	do {
	var tmp =number%10;
	number = parseInt(number /10);
	console.log(tmp);
	
	} while (number != 0);
	} else if(number ===0){
	console.log("0");
	}else{
	console.log("重新来");
	
	}