```html

  <style>
    .container{
      /* 
        景深， 元素与屏幕距离
        给动画元素的父元素设置
      */
      perspective: 90px;
      width: 100px;
      margin: 0 auto;
    }
    .container:hover .box{
      transform: rotateX(360deg) rotateY(180deg);
    }
    .box{
      width: 100px;
      height: 100px;
      background-color: #ace;
      transform: rotateX(0deg) rotateY(0deg);
      /* 子元素保留3d位置 */
      transform-style: preserve-3d;
      transition: all 10s;
      /* 背面可见 */
      backface-visibility: visible;
      /* 背面隐藏 */
      backface-visibility: hidden;
    }
  </style>
  <div class="container">
    <div class="box"></div>
  </div>
```

