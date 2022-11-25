```js
   //for循环
    /*for(var i = 0; i < 10;   i++){
      //要循环的逻辑
    }
    */
  // for(var i = 0; i <= 5; i++){
  //   console.log(i);
  // }
  
  
  // 正序循环输出
  // for(var i = 0; i <= 5; i++){
  //   console.log(i);
  // }
  
  // 倒序循环输出
  // for(var i = 5; i >= 0; i--){
  //   console.log(i);
  // }
  
  // for(var i = 50; i >= 2; i--){
  //   if(i%2 == 0){
  //     console.log(i);
  //   }
  // }

  // for嵌套循环之冒泡
  // var arr = [7,6,9,5,2,4,3,1,66]
  // for(var i = 0; i < arr.length; i++){
  //   for(var j = 0; j < arr.length - 1 - i; j++){
  //     if(arr[j] > arr[j+1]){
  //       var temp = arr[j+1]
  //       arr[j+1] = arr[j]
  //       arr[j]  = temp
  //     }
  //   }
  //   console.log(arr);
  // }

  // break和continue
  // continue用于调出本次循环，继续下一次循环
  // break用于跳出整个循环

  // for(var i = 0; i < 5; i++){
  //   if(i == 3) continue
  //   console.log(i);
  // }

  // for(var i = 0; i < 5; i++){
  //   if(i == 3) break
  //   console.log(i);
  // }

  // while 循环， 条件可以使一个表达式
  // var age = 0
  // while(age < 22){
  //   console.log('您的年龄为：'+ age);
  //   age = age + 1
  // }

  // do.....while循环
  // 和while 相似， 唯一区别就是会先运行一次
  // var a = 1
  // do{
  //   console.log(a);
  //   a+=1 // 相当于 a = a + 1
  // }while(a<22)

    // for    in     用于循环对象的键名（key）
    // var person = {
    //   name: 'tony',
    //   age: 18,
    //   gender: '男'
    // }

    // console.log(person.name);
    // console.log(person['name']);

    // for( var key in person){
    //   console.log(key, person[key]);
    // }

    // var arr = [2, 3, 4, 5, 6]
    // for( var key in arr){
    //   console.log(key);
    // }

    // for of 用于循环数组、字符串
    // 循环数组拿到的是 数组成员
    // 循环字符串拿到的是字符串的每一项
    // var arr = [1, 2, 3, 4, 5, 6]
    // for( var item of arr){
    //   console.log(item);
    // }

    // var str = 'javascript'
    // for( var item of str){
    //   console.log(item);
    // }
```

