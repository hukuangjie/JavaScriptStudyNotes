### break 和 continue ###

#### break ####
立刻退出循环

#### continue ####

立即退出当前循环，但退出循环后会从循环的顶部继续执行

    //求 200-300 之间的所有的偶数的和，用 continue 实现
    var sum = 0;
    for (let i = 200; i < 301; i++){
        if(i % 2 === 0){
            continue;
        }
        sum += i;
    }
    console.log(sum);
    
    //求 200-300 之间第一个能被 7 整除的数
    for (let index = 200; index < 301; index++) {
        if (index % 7 === 0 ) {
            console.log(index);
            break;
        }
    } 

