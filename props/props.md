# 现代 css 属性

## transition

transition-property 过渡属性的名称。可以是 none,all,property  
transition-duration 过渡动画的持续时间，默认是 0，所以一定要指定。  
transition-timing-function 过渡属性播放速率函数。  
transition-delay 过渡属性的播放延迟。

## box-shadow && text-shadow

四个常用属性分别指定
x 偏移量 y 偏移量 模糊半径 阴影颜色

```css
box-shadow: 10px 5px 5px black;
```

例如

```css
.btn:hover {
	box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
}
.btn:active {
	box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
}
```

通过设置按钮在悬浮/激活时的 box-shadow 属性来通过改变按钮阴影营造按钮由近到远的按压效果

## animation

animation-name 指定关键帧动画的名称  
 animation-duration 动画持续时间  
 animation-timing-function 动画播放速率函数  
 animation-delay 播放延迟  
 animation-iteration-count 动画播放次数，可以指定 infinite  
 animation-direction 动画是否反向播放 normal/reverse/alternate(交替)/alternate-reverse  
 animation-fill-mode 动画在执行之前和之后如何将样式应用于其目标 none/forwards(最后一个关键帧)/backwards(第一个关键帧)/both  
 animation-play-state 动画是否运行或者暂停 running/paused

## skew()

函数定义了一个元素在二维平面上的倾斜转换,结果用于 transform

## resize

允许用户通过拖拽方式调整元素宽高，属性值有 vertical/horizontal/both，分别代表了纵向/横向/全部
通常需要overflow:auto 使含有内部元素的容器生效
设置为 none 可以让 textarea 等可缩放元素禁止缩放

## aspect-radio
让盒子保持一个横纵比，值为 h / v 的格式，可以让元素保持更好的自适应性

## pointer-events
在目标为非svg元素时有两个属性 none/auto
auto为未指定样式时的默认行为
none为目标不触发事件，其后代元素会触发事件

## display:flow-root
创建一个块级上下文，是最只管的创建bfc的方式

## outline

类似 Border，但不占据空间，且通常为矩形
outline 可以配合 outline-offset 设置边框与元素之间的间隙

## backgound-clip

背景显示范围  
值可以是 border-box/padding-box/content-box/text
