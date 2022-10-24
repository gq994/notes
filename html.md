## html介绍

html是一门标记语言，用途是排版和组织页面，xhtml时代过渡到html时代。

html文档也叫web页面，是在浏览器中执行的。

>  html5文档声明
>
> > ``` html 
> > <!DOCTYPE html> 文档声明不区分大小写
> > 已下都对
> > <!doctype html>
> > <!doctype HTML>
> > <!DOCtype html>
> > ```
> >
> > 文件扩展名
> >
> > > .htm早些因为不支持超过3位数的扩展。
> > >
> > > .html是最推荐的html扩展名。



## 主流浏览器

| 浏览器             | 内核                                   |
| ------------------ | -------------------------------------- |
| Chrome谷歌（推荐） | 以前是Webkit，现在是Blink;             |
| firefox 火狐       | Gecko                                  |
| ie微软             | Trident（IE、360、搜狗)                |
| opera欧鹏          | 以前Presto>webkit,现在是blink          |
| Safari 苹果        | webkit                                 |
| 360 安全           | IE+Chrome双内核                        |
|                    | Trident（兼容模式）+webkit（高速模式） |



## html基础标签

``` html
1.身体<body></body>
默认外边距margin = 8px， 宽度是可视宽度， 高度是北荣的高度

2.标题 <h1>标题</h1>
- 有默认的上下边距，不同级别，大小不同
- 宽度自适应容器
- 高度是内容高度
- 不同标题级别字号不同
- 大部分搜索引擎规定一个页面h1标题只有一个
- 标题级别一共有六个h1-h6
快写指令：(h${$级标题})*6	
  <h1>1级标题</h1>
  <h2>2级标题</h2>
  <h3>3级标题</h3>
  <h4>4级标题</h4>
  <h5>5级标题</h5>
  <h6>6级标题</h6>

3.<p>段落</p>
- 有默认的上下边距16px
- p标签不能包裹标题标签、块级标签

4.<a href="#">链接</a>
- 没有盒型数据，行内元素，默认为蓝色加下划线
- #锚点链接，可以看做是空链接，也有返回浏览器顶部的功能
- 当#后面加值时，会寻找对应的id值得标签元素。例如：href=“#a" , 会寻找到当前页面中id=”a“的标签元素。

5.图像	<img src="">
- 图像的宽度是图片自身的宽高
- 图像是单标签
- 如果只设置图片高度/宽度， 图片的宽度/高度会等比例缩放

6.强制换行<br>
- 单标签

7.水平线<hr>
- 单标签


单标签(空标签)是指没有结束标签	 双标签是指具有结束标签
<br>强制换行					<div></div>
<hr>水平线						 <p></p>
<img src="">				   <a></a>
<meta>页面配置				    <title></title>	
<link>页面引入资源			   <ul></ul>
<input>						   <b></b>
							   <span></span>

空元素是指没有内容的元素       
<br>
<hr>
```

## 属性定义注意事项：

1. 属性名小写
2. 属性值要用双引号包裹
3. 属性名必须是字母开头，不能使用空格或者其他除下划线、中横杠以外的特殊字符
4. 如果是组合单词，建议使用中横杠连接
    <input get-age="20">

### 	公共属性

		- id定义唯一标识
		- class定义类名
		- name定义名称
		- style定义行内样式
		- title定义划过气泡提示

## SEO优化

 SEO优化的TDK

  1. T: 网页窗口标题

     ``` html
     <title>窗口标题</title>
     ```

2. D：description

   ``` html
   <meta name="description" content="一般描述30~50字">
   ```

3. K: keywords 关键词， 在浏览器所搜索关键字时，就会优先出现有这些关键字的网站

   ```html
    <meta name="keywords" content="关键词1，关键词2....,一般六到八个关键字 ">
   ```


4. 一个页面只用一个h1，要合理的使用标题级别标题使用过多、乱会被认为作弊，会被降权

5. 内链和外链优化，内链就是站内链接、外链就是和知名大流量网站交换链接

6. 软文推广，就是写一篇看似很有营养的文章，这些文章被大流量网站收录，文章里面植入了你网站链接，属于外链优化

7. 代码要语义化和代码结构简练，标题就是要标题，合理使用标签，不要乱用，比如一律全部用div，代码结构不要嵌套的太深，不然也影响收录

8. 少用图片、视频、音频，因为搜索引擎无法采集图片、视频等富媒体上的内容



## 文本格式化标签

1. 加粗 b 、strong、strong有强调语义

2. 倾斜i 、 em， em有语义强调

3. 下划线s、del， del有语义强调作用

4. 大小号文本small、big

5. 上角sup，下标sub

6. pre 预文本处理，

   ​	用途：用于保留源代码，支持换行和缩进、保留编辑器的格式

​	7.  code 内联代码 ，表示这是一段代码

  										实体代码`&lt;` <     `&gt`>

​	8. kbd键盘输入， 这是一个语义化标签

​      ```<kbd>ctrl + c</kbd>复制<br>```

​	

​	9.  abbr 缩写

​     ```<abbr title="完整内容">缩写内容</abbr>```



 10.  address 地址， 语义化标签

     ```<address>江西省南昌市青山湖区紫阳大道</address>```

 11. bdo 文字排列方向 

       dir属性：

     ​     ltr： 从左到右（默认）

     ​     rtl： 从右到左

 12. blockquote 长引用

​	```<blockquote>横眉冷对千夫指，俯首甘为贩子牛</blockquote>```

13. q短引

    ```鲁迅<q>我家门前有两棵树， 一棵树是枣树， 另一棵树也是枣树</q>```

14. 引证引用， 表示谁说的这句话     cite

``` <q>我家门前有两棵树， 一棵树是枣树， 另一棵树也是枣树</q>------<cite>鲁迅</cite>```

15. mark高亮 html5新特性

```<mark>理想</mark>```



## 标签分类

1. 块级标签：div、ul、li、p、pre、blockqute、

2. 行级标签：span、a、img、b、strong、u、ins、s、del、i、em、mark、canvas

3. 行块标签:   input、textarea、 select

块级标签

​    特点：

​     1.display:block(块级标签)

​     2.独占一行

​     3.宽度自适应

​     4.可以设置盒子属性(宽， 高， 边框， 填充， 边距)

 行级（内联）标签

​     特点：

​      1.display: inline

​      2.行级标签之间可以并排在一行

​      3.不能设置宽高，宽、高度由内容撑开

​      4.可以设置内填充，边框, 外边距也是生效的， 

​        padding的上下渲染会存在问题， margin的仅支持左右

 行块标签

​    特点：

​     1.display: inline-block

​     2.可以设置盒子属性

​     3.可以和行块元素并排一行

​     4.默认尺寸由它的内容撑开

注意：行块标签之间有间隙，这个间隙宽度大约3~4px，间隙是由标签之间的空格或者换行符造成的，我们可以通过删除之间的空格或者换行符，使得它们无缝连接，这种方式兼容性最好，甚至可以兼容到IE6，但是这样带来一个新的问题，代码不易读。



## 盒子模型

盒子模型是指将网页设计页面中的内容元素看作一个个装了东西的矩形盒子。每个矩形盒子都由内容（content）、内填充（padding）、边框（border）和外边距（margin）4个部分组成。除去内容部分，其余每个部分又分别包含上、下、左和右4个方向，方向既可以分别定义也可以统一定义。

 盒子模型分为：

  1.box-sizing：content-box（内容盒子），默认

  1.box-sizing：border-box（边框盒子） ， 

 默认情况（ 盒子）下元素的尺寸

​     content（内容） + padding（内填充）+ border（边框）

Content-box，元素的尺寸 = content + padding + border ，width和height设置的content				的尺寸 。往								外算

Border-box，元素的尺寸 = content + padding + border ，width和height设置的元素的总				尺寸，								content的尺寸会随border和padding的变化自适应。往里算

## 常用标签

####   div: 

​    1.块级标签,没有语义

​    2.没有任何默认样式，用于排版，容器

####   p标签

​    		1.块级标签

   		 2.默认的上下16像素 外边距

   		 3.p标签不能包裹块级标签

   			align属性:

​    					 left  左对齐

​    					 center  居中对齐

​     					right  右对齐

​    					 justify 两端对齐

####   span:

​    1.行级标签，没有语义

​    2.没有任何默认样式

​     用于包裹文本内容，也可以包裹文本修饰标签

####  a链接

​    1.行级标签

​    2.默认样式为蓝色下划线，点击时红色，点击过后为淡紫色

​    3.a可以去包裹除了自身的任意标签

 		  href属性：

  				   1.跳转的地址

  				   2.网页中的锚点，锚点与标签的id有一个映射关系

 				    3.文件的地址，

 			  download下载属性

   			target属性：

​    					 1._self  在当前窗口打开

​    					 2._blank  在新窗口打卡

​    					 3._parent  在父窗口打开

​     					4._top    顶级窗口

​     					5.自定义窗口  

​       							a链接的target的值与iframe的name的值有映射关系

​      								 点击a链接，会将a链接网页嵌入对应的iframe中去

## 锚点链接

特点:

​      1.不会刷新页面跳转

​      2.href属性值以#开头，通过标签的id值和href属性的#值相匹配

​      3.href的值为#是一个空链接，默认跳转到顶部

​    阻止a链接跳转

​    使用a链接做文字按钮

``` <!-- 阻止网页跳转的方法 -->
   <!-- 阻止网页跳转的方法 -->
  <a href="javascript:;">按钮</a>
  <a href="javascript:void(0);">按钮</a>
  <a href="javascript:alert('1111');">弹窗</a>
```

## 图像热区

使用a链接包裹图片时在IE10以下，会出现蓝色边框，

​    给img设置border属性，值为0即可

####    图像热区链接的使用：

   1.map标签的name与img的usemap相匹配，usemap属性以#开头

   2.使用map标签制热区，area标签绘制区域的形状

```html
   <map name="">

​    <area>

   </map>


    circle  绘制圆形区域
    <area shape="circle" coords="x,y,r" href="" > 
    x,y,r分别是圆心，半径

    rect  绘制矩形区域
    <area shape="rect" coords="x1,y1,x2,y2" href="" alt="">
    x1,y1为左上角坐标
    x2,y2为右下角坐标

    poly  绘制多变形
    <area shape="poly" coords="x1,y1,......xn,yn" href="" alt="">
    x1,y1为第一个点的坐标
    多边形就是将绘制的点连成一块区域
    最后一个点会与第一个点链接


<img border="1px solid" src="./img/map.jpg" usemap="#map" alt="" width="1500">
  <map name="map">
    <area shape="circle" coords="865,455,15" href="https://baike.baidu.com/item/%E5%8C%97%E4%BA%AC/128981?fr=aladdin" alt="">
    <area shape="rect" coords="753,700,842,776" href="https://baike.baidu.com/item/%E6%B9%96%E5%8D%97/228213?fromModule=lemma_search-box" alt="" target="_blank">
    <area shape="poly" 
    coords="
    164,367,
    290,344,
    309,281,
    344,289,
    370,242,
    444,224,
    549,384,
    434,515,
    212,504,
    176,427
    " href="https://baike.baidu.com/item/%E6%96%B0%E7%96%86/132263?fromModule=lemma_search-box" target="_blank" alt="">
    <!-- <area shape="default" coords="" href="" alt=""> -->
  </map>
```





  

