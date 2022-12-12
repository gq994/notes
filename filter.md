

​    filter()

​     (1)用于根据指定的条件筛选数组信息

​     (2)不会破坏原始数组，返回新数组

​      语法：

​      数组实例.filter(function(item,index,arr){

​       return item;

​      })

​     item 数组每项成员

​     index 数组成员的索引值

​     arr 当前循环的原始数组

​     return 符合条件的数据



  var fruit = [

   {id: 1, name: '苹果', price: 5, creatTime: '2022-12-12'},

   {id: 2, name: '橘子', price: 2, creatTime: '2022-12-12'},

   {id: 3, name: '香蕉', price: 3, creatTime: '2022-12-12'},

   {id: 4, name: '西瓜', price: 6, creatTime: '2022-12-12'},

   {id: 5, name: '葡萄', price: 10, creatTime: '2022-12-12'},

   {id: 6, name: '菠萝', price: 6, creatTime: '2022-12-12'},

   {id: 7, name: '橙子', price: 10, creatTime: '2022-12-12'},

   {id: 8, name: '西瓜', price: 6, creatTime: '2022-12-12'},

   {id: 9, name: '葡萄', price: 10, creatTime: '2022-12-12'},

   {id: 10, name: '菠萝', price: 6, creatTime: '2022-12-12'},

   {id: 11, name: '橙子', price: 10, creatTime: '2022-12-12'},

  ]

  var newarr = fruit.filter((item,index,arr)=>{

   return item.price > 5

  })

  console.log(newarr);