```html

  <style>
    .center{
      width: 200px;
      height: 200px;
      background-color: #a11;
      position: fixed;
      left: 50%;
      top: 50%;
      transform: translate(-50%, -50%);
    }
  </style>
  <div class="center">元素水平垂直居中</div>
  <h4>translate平移</h4>
  <!-- 2d
  转换，表现负载文档流上面，实际会占据文档流 -->
  <style>
    .box{
      width: 100px;
      height: 100px;
      background-color: #ace;
      transform: translate(100px, 100px);
      transform: translateX(100px);
      transform: translateY(100px);
      /* 
        trannsform: translate3d(x, y, z);
        trannsform: translate3d(水平位置， 垂直位置， z轴位置);
        为开启硬件加速
        支持百分比%， 百分比根据自身宽高换算
      */
      transform: translate3d(100%, 100%, 0);
    }
  </style>
  <div class="box"></div>
  <div style="width: 100px; height:100px; background-color: red;"></div>

  <h4>rotate旋转</h4>
  <style>
    .rotate{
      width: 100px;
      height: 100px;
      background-color: #ace;
      /* 
        transform: rotate(0deg)
        单位为deg
      */
      transform: rotate(45deg);
      transform: rotateX(0deg);
      transform: rotateY(0deg);
      transform: rotateZ(0deg);
      transform: rotateX(0deg) rotateY(0deg) rotateZ(0deg);
      /* 
        改变注册点，元素左上角为0 0
        transform-origin: 水平位置  垂直位置;
      */
      transform-origin: 200% 0;
      transition: all 9s;
    }
    .rotate:hover{
      transform: rotate(32000deg) translate3d(200%, 300% ,0);
    }
  </style>
  <div class="rotate"></div>


  <h4>scale缩放</h4>
  <style>
    .scale{
      width: 50px;
      height: 50px;
      border-radius: 50%;
      background-color: #ae1;
      /* 
        transform: scale(x, y)
          1为不变，2为放大两倍

          x轴方向缩放
          transform: scaleX(1);

          y轴方向缩放
          transform: scaleY(1);

          z轴方向缩放
          transform: scaleZ(1);

      */
      transform: scale(0.5, 0.5);
      transform: scaleX(0.5) scaleY(0.5);
      transform: scaleX(0.5);
      transform: scaleY(0.5);
      transform: scaleZ(100) rotateY(60deg);
      transform: scale3d(0.5, 0.5, 0.5);
      transition: all 1s;
    }
    .scale:hover{
      transform: scale3d(3, 3, 5);
    }
  </style>
  <div class="scale"></div>


  <h4>skew倾斜</h4>
  <style>
    .skew{
      width: 100px;
      height: 100px;
      background-color: #a959a9;
      /* 
          transform: skew(X轴角度, Y轴角度);


          x轴倾斜  
          transform: skewX(0deg);
          
          
          y轴倾斜
          transform: skewY(0deg);
          
          */
          transform: skew(0deg, 0deg);
          transform: skewX(0deg);
          transform: skewY(0deg);
        }
  </style>
  <div class="skew"></div>

  <h4>matrix矩阵</h4>
  <style>
    .matrix{
      width: 100px;
      height: 100px;
      background-color: #aed;
      /* 
        transform: matrix(a,b,c,d,e,f)

      a:  水平缩放   不缩放值 1     倍数
      b:  垂直倾斜   不倾斜值 0     弧度制   1rag = 57.14°
      c:  水平倾斜   不倾斜值 0     弧度制
      d:  垂直缩放   不缩放值为1    倍数
      e:  水平移动   不移动值0      像素    不需要带px单位
      f:  垂直移动   不移动值0      像素
      */
      transform: matrix(1,0,0,1,100,100);
      transition: all 1s;
    }
    .matrix:hover{
      transform: matrix(6,1,-1,6,300,300);
    }
  </style>
  <div class="matrix"></div>
```

