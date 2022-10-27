##  label标签：

​    作用：扩大用户点击的范围

​       点击label相当于label帮你点击了label标签中的表单控件

 label

​     for属性：

​       匹配id值与for值相同的表单控件

​       点击label，相当于点击了id值与for值相同的表达控件

​     使用for的方式优先级高于包裹的方式

```html
  <form action="">
    <h2>label第一种使用方式</h2>
    性别：
    <label>
      <input type="radio" name="gender" id="">男
      <a href="">百度</a>
    </label>
    <label>
      <input type="radio" name="gender" id="">女
    </label>
      <h2>label第二种使用方式</h2>
    <label for="username">用户名:</label>
    <input type="text" name="username" id="username">
  </form>
```







