```html
<!-- 
    animation: name duration timing-function delay iteration-count direction state;
                动画执行名称            animation-name
                动画完成时间            animation
                速度曲线
                延迟时间
                执行次数
                动画方向
                动画状态





    1.  name  动画执行名称
    2.  duration 动画完成时间
    3.  timing-function 速度曲线
    4.  delay 延迟时间
    5.  iteration-count 执行次数 默认1次，也可以指定次数，永动infinite   
    6.  direction 动画方向
                            1.normal              正常
                            2.reverse             倒放
                            3.alternate           先正放，结束后倒放
                            4.alternate-reverse   先倒放，结束后正放
    7.  state 动画状态 
                            1. running           播放动画
                            2. paused            暂停播放     

      定义关键帧
    @keyframes name{

    }
   -->
   <style>
    .box{
      width: 100px;
      height: 100px;
      background-color: #ace;
      animation: myanimation 1s ease 0s infinite alternate running;
      animation: myanimation 1s ease 0s infinite reverse running;
      animation: myanimation 1s ease 2s 1 normal paused;
      /* 
      animation-fill-mode 规定动画在播放之前或之后，其动画效果是否可见 
                          none        不改变默认行为。（默认）
                          forwards    当动画完成后，保持最后一个属性值
                          backwards   所指定的一段时间内（指的是设置delay
                                      延迟时间，不设置默认是0），在动画显示之前，应用开始属性值
                          both        向前和向后填充模式都被应用。

                                      注意：
                                      如果动画无延迟，forwards 和 both 表现出来的效果是相同的
                                        开始时 both 会应用 backwards（第一帧定义的状态） 的效果
      */                  
      /* animation-fill-mode: forwards; */
      /* animation-fill-mode: backwards; */
      animation-fill-mode: both;
    }
    /* 定义动画关键帧 */
    @keyframes myanimation {
      0%{
        background-color: #ea99;
      }
      50%{
        transform: rotateZ(180deg);
      }
      100%{
        /* transform: rotateX(180deg); */
        transform: translateX(180px);
        background-color: #ae9;
        opacity: 0.2;
      }
    }
   </style>
   <div class="box"></div>
   <button onclick="running()">运行</button>
   <button onclick="paused()">暂停</button>
   <script>
    var box = document.querySelector('.box')
    function running(){
      // console.log(onclick);
      box.style.animationPlayState = 'running' ;
    }
    function paused(){
      box.style.animationPlayState = 'paused' ;
    }
   </script>
```

