``` html
E 代表HTML标签。
E#id 代表id属性。
E.class 代表class属性。
E[attr=foo] 代表某一个特定属性。
E{foo} 代表标签包含的内容是foo。
E>N 代表N是E的子元素。
E+N 代表N是E的同级元素。
E^N 代表N是E的上级元素。

div                 =>  <div></div>
a:link              =>  <a href="https://"></a>
br                  =>  <br>
script:src          =>  <script src=""></script>
form:get            =>  <form action="" method="get"></form>
label               =>  <label for=""></label>
input               =>  <input type="text">
inp                 =>  <input type="text"      name="" id="">
input:hidden        =>  <input type="hidden"    name="">input:h 也可以
input:email         =>  <input type="email"     name="" id="">
input:password      =>  <input type="password"  name="" id="">
input:checkbox      =>  <input type="checkbox"  name="" id="">
input:radio         =>  <input type="radio"     name="" id="">
select              =>  <select name="" id=""></select>
option              =>  <option value="">
btn                 =>  <button></button>
btn:s               =>  <button type="submit"></button>
btn:r               =>  <button type="reset"></button>

1. 文本操作符(Text)
如果想在生成元素的同时添加文本内容可以使用{}
div{这是一段文本}
<div>这是一段文本</div>
a{点我点我}
<a href="">点我点我</a>  

2.  属性操作符
div.test    => <div class="test"></div>
div#pageId  => <div id="pageId"></div>

  2.1.  隐式标签则会自动联想生成对应元素,根据配置规则不同生成的结果也是不同的.
    .class =>  <div class></div>
    em>.class  =>  <em><span class></span></em>
    table>.row>.col  =>
    <table>
        <tr class="row">
            <td class="col"></td>
        </tr>
    </table>

  2.2绑定多个类名用.符号连续起来即可
    div.test1.test2.test3   =>
    <div class="test1 test2 test3"></div>

3. 嵌套操作符
  子级:>
  通过>标识元素可以生成嵌套子级元素,可以配合元素属性进行连写
  div#pageId>ul>li 
  => 
  <div id="pageId">
      <ul>
          <li></li>
      </ul>
  </div>

  同级:+
  +字符表示生成兄弟级元素.
  div#pageId+div.child
  =>
  <div id="pageId"></div>
  <div class="child"></div>

  父级:^
  用于生成父级元素的同级元素,从这个字符所在位置开始,
  查找左侧最近的元素的父级元素并生成其兄弟级元素.
  div>p.parent>span.child^ul.brother>li
  =>
  <div>
      <p class="parent"><span class="child"></span></p>
      <ul class="brother">
          <li></li>
      </ul>
  </div>

  分组操作符(Grouping)
  分组使用()来实现缩写的分离.比如这个例子,
  如果不加括号那么a将作为span的子级元素生成.加上括号a将于()内的元素同级.
  div>(ul>li+span)>a
  =>
  <div>
      <ul>
          <li></li>
          <span></span>
      </ul>
      <a href=""></a>
  </div>

  乘法(Multiplication)
  使用N即可自动生成重复项.N是一个正整数.在使用时请注意N所在位置,位置不同生成的结果不同.
  ul>li*3
  =>
  <ul>
      <li></li>
      <li></li>
      <li></li>
  </ul>

  自动计数(numbering)
  这个功能挺方便的对于生成重复项时增加一个序号,只需要加上$符号即可.
  ul>li.item${item number:$}*3
  <ul>
      <li class="item1">item number:1</li>
      <li class="item2">item number:2</li>
      <li class="item3">item number:3</li>
  </ul>
  </ul>
  如果生成两位数则使用两个连续的$$,更多位数以此类推...
  使用@修饰符，可以更改编号方向（升序或降序）和基数（例如起始值）.注意这个操作符在$之后添加
  @-表示降序,@+表示升序,默认使用升序.
  @N可以改变起始值.需要注意的是如果配合升降序使用的话N是放到+-符后.
  ul>li.item$@-*3
  =>
  <ul>
      <li class="item3"></li>
      <li class="item2"></li>
      <li class="item1"></li>
  </ul>
  ---------------------------
  ul>li.item$@-10*3
  =>
  <ul>
      <li class="item12"></li>
      <li class="item11"></li>
      <li class="item10"></li>
  </ul>

  上述的操作是可以搭配使用进而得出酷炫的效果,使用时请注意空格的问题,缩写代码不要有空格否则是不会进行转换的.
模拟文本/随机文本
    在开发时经常要填充一些文本内容占位,Emmet内置了Lorem Ipsum功能来实现.
      loremN或者lipsumN,N表示生成的单词数,正整数.可以不填.
      lorem
      => Lorem ipsum dolor sit amet, consectetur
         adipisicing elit. Suscipit quia commodi 
         vero sint omnis fugiat excepturi reiciendis 
         necessitatibus totam asperiores, delectus saepe 
         nulla consequuntur nostrum! Saepe suscipit recusandae 
         repellendus assumenda.
      
      p>lorem4
      =>
      <p>Lorem ipsum dolor sit.</p>
      
      (p>lorem4)*3
      =>
      <p>Lorem ipsum dolor sit.</p>
      <p>Labore aperiam, consequuntur architecto.</p>
      <p>Quidem nisi, cum odio!</p>

      包装文本
        听起来可能有点绕,通俗点解释就是把一段指定的文本包装成我们想要的结构.
        注意这个功能需要编辑器的支持,举个大栗子:
        首页
        产品介绍
        相关案例
        关于我们
        联系我们
        而我们预期的效果是这样
      =>
      <ul>
        <li>首页</li>
        <li>产品介绍</li>
        <li>相关案例</li>
        <li>关于我们</li>
        <li>联系我们</li>
        <li>而我们预期的效果是这样</li>
      </ul>
      选中文本,按下ctrl+shift+p打开命令窗口输入ewrap
      选择Emmet:使用缩写进行包装(Wrap with Abbreviation)选项
      输入缩写字符nav>ul>li*按下回车键即可看到效果.
```
