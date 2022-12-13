```js
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
  <style>
    table,th,td{
      border-collapse: collapse;
      border: 1px solid #000;
      padding: 10px;
    }
  </style>
</head>
<body>
  <p>
    <input 
    type="search" 
    placeholder="请输入水果名称" 
    autocomplete="off" 
    id="keywords"
    >
    <input type="number"  id="price1" placeholder="起始价格" style="width: 80px;">
    <input type="number"  id="price2" placeholder="最终价格" style="width: 80px;">
    <button onclick="search()">搜索</button>
  </p>
  <table>
    <thead>
      <th>编号</th>
      <th>水果名称</th>
      <th>水果单价</th>
      <th>创建日期</th>
    </thead>
    <tbody id="list">

    </tbody>
  </table>
  <script>
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
    function search(input){
      // 初始化搜索条件
      var condition = {
        keywords: document.getElementById('keywords').value.trim(),
        price1: document.getElementById('price1').value,
        price2: document.getElementById('price2').value
      }
      view(condition)
    }
    function view(condition){
      // 关键字
      var keywords = condition.keywords
      var price1 = condition.price1
      var price2 = condition.price2
      // 搜索之后的结果
      var searchData = fruit.filter((item)=>{
        return (keywords ? item.name.includes(keywords) : true) && 
               ((price1 ? item.price >= price1 : true)) &&
               ((price2 ? item.price <= price2 : true)) 
      })
      console.log(searchData);
      var temp = ''
      if(!searchData.length) {
        temp = `
        <tr>
          <td colspan="999">
            抱歉，没有搜索到相关内容
          </td>
        </tr>
        `
      }
      searchData.forEach((item)=>{
        temp+=`
        <tr>
          <td>${item.id}</td>
          <td>${item.name}</td>
          <td>￥${item.price.toFixed(2)}</td>
          <td>${item.creatTime}</td>
        </tr>
        `
      })
      list.innerHTML = temp
    }
    search()
  </script>
</body>
</html>
```

