```js

    /*
      IIFE(立即执行函数)：
        function关键字在行首， js引擎会认为这是一句函数
                不会立即执行
        当function被()包裹， 或在function前添加+、-、！时，
        js引擎会认为这是一句表达式，会直接执行

      IIFE立即执行函数的作用：  
        可以写成匿名函数，所以不必为函数命名
        代码是写在函数内部，所以具有函数级作用域，避免了污染全局变量
	
      
    */
   (function fn(){
    console.log('立即执行');
   })()

   +function fn(){
    console.log('立即执行');
    }()

   -function fn(){
    console.log('立即执行');
    }()

   !function fn(){
    console.log('立即执行');
    }()

    var gq = (function(){
      var SUM;

      // 求和函数
      function sum(){
        SUM = 0
        var args = [...arguments]
        for(var i = 0; i < args.length; i++){
          SUM+=args[i]
        }
        return SUM
      }

      // 求平均值
      function average(){
        var len = arguments.length
        if(!SUM) this.sum(...arguments)
        return SUM/len
      }

      return {
        sum:sum,
        average: average
      }

    })()

    console.log(gq.sum(1,2,3));
    console.log(gq.average(1,2,3));
```

