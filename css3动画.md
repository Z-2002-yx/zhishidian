#### 动画属性

##### animation

> animation-name  规定@keyframes 动画名称
>
> animation-duration  规定动画完成需要多少秒
>
> animation-timing-function  规定动画速度
>
> animation-delay  规定动画何时开始
>
> animation-iteration-count 动画播放次数
>
> animation-direction 规定动画下一周期逆向播放
>
> animation-play-state  规定动画是否开始运行
>
> animation-fill-mode  动画不播放的样式



##### @keyframes

> ```css
> @keyframs 起个名字{
>     form{
>         // 刚开始的样式
>     }
>     to{
>         // 结束时的样式
>     }
> }
>  
> // 或者
> @keyframs 起个名字{
>     0%{
>         // 动画刚开始执行的样式
>     }
>     25%{
>         // 执行到1/4时的样式
>     }
>     50%{
>         
>     }
>     75{
>         
>     }
>     100%{
>         
>     }
> }
> ```



#### 改变元素位置

##### transform

> 参数总结
>
> ```css
> transform: translate(); x y 轴的偏移距离，px结尾
> transform: scale(); 改变宽高大小，倍数
> transform: rotate(); 旋转度数 deg结尾
> transform: skew(); 改变盒子的倾斜角度
> ```
> 



