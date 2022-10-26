# form表单

## 特征:

   1.表单主要用于收集用户输入的信息

   2.表单收集到的信息最终是提交给后端

   3.display：block块级元素

   4.一个页面可以有多个form

   5.form不能嵌套

## 属性：

### action属性： 

提交给后端处理的地址

### name属性： 

定义表单名称，通过js可以找到该表单

### method属性：

​		提交的方式

​          1. GET请求（默认的） 只需要获取后端数据，建议使用get请求

​                                1.提交的数据会显示在地址栏，不安全

​                                2.提交数据长度受url长度限制

​          2.  POST请求（推荐使用）

### enctype属性：

 请求文档编码类型

​           1.application/x-www-form-urlencoded(默认)      

​               username=xxx&password=123456

​           2.multipart/form-data  以表单数据形式提交

​               -----username：xxxxxx----

​               -----password：123456----

​           3.text/plain  纯文本格式

​           没有格式，一般是账户、密码、小型的数据

### target属性：  

​		提交后的打开方式

​           _self  (默认)，覆盖当前窗口

​           _parent 父窗口打开

​           _top   顶级窗口打开

​           _blank  新窗口打开

### autocomplete属性：  

​			自动完成， 相当于一个历史记录

​           off  关闭

​           on  打开 (默认)    

​           注意： 控件需要有name的条件下才能触发