```html

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
</head>
<body>
  <!-- 
      BEM(block element modifier)
      是由俄罗斯Yandex团队提出
   -->
   <!-- 
    在css设置样式时，css选择器会对全局元素进行匹配
    css的作用域是全局，项目体量变大，命名可能会影响到其他
    导致代码可读性，维护性变差
    -->
    <!-- 
      css命名
        1.通常通过网站结构去命名（避免样式混乱）
        2.网站结构可以分为三层，分别是
                          block块层
                          element元素层
                          modifier修饰符层
     -->
     <!-- 
      BEM
        block： HTML内容的某个区块， 如header、nav、mian、footer等
        element： 表示block块中的某个元素
        modifier： 表示元素的修饰部分
      BEM命名规范：
          - 中划线：作为连接符，可以是块中子元素多单词之间的链接或者块的命名

          __ 双下划线：双下划线连接块和块的子元素

          -- 双横杠： 表示块或者子元素的状态
      BEM命名法的缺点：
        命名方式长，不太优雅
        css预处理器less或者sass可以解决
      -->
      <style>
        .header{
          height: 60px;
          background-color: #ace;
        }
        .header .logo{
          float: left;

        }
        .header .header__login{
          float: right;
        }
        .header__btn--primary{
          background-color: #ea9;
        }
        .header__btn--danger{
          background-color: #FF757F;
        }

      </style>
      <div class="header">
        <a href="#" class="logo">logo</a>
        <button class="header__login">登录</button>
        <span class="full-name">text</span>
        <button class="header__btn--primary">正常</button>
        <button class="header__btn--danger">失败</button>
        <button class="header__btn--hover">划过</button>
      </div>
</body>
</html>
```

