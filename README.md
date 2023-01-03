# modern-css
  这是学习css过程中的一些总结笔记

# 理论知识
## css优先级
1. 重要性排序
   1. User !important declarations
   2. Author !important decalarations
   3. Author declarations
   4. User declarations
   5. Default browser declarations
2. 权重
   1. inline Styles
   2. IDs
   3. classes,pseudo-classes,attribute
   4. Elements,pseudo-elements
3. 代码排序  
   The last declaration in the code will override all other declarations and will be applied 

# 一些规范

## BEM 命名规范
Block Element Modifier

- 优点：
  1.  更清晰的结构
  2.  低优先级带来的可维护性
- 使用
    > \- 中横线用于连词符  
    > \_\_ 双下划线连接块与其子元素  
    > \_ 单下划线用于描述元素状态

## 基于rem构建的响应式网站
1. 1rem 总是和 html 的font-size相等
2. 如果我们在开发时将html的font-size设置10px（默认值为16px)，就可以轻松的将设计图中的px转为rem
3. 为了保持响应式与可缩放性，将font-size10px基于10/16=>0.625改为62.5%

## 7-1 pattern
该设计模式主要在于目录结构的区分。
- base（基础）base文件夹底下都会放CSS Reset、或是字体的基础设置等都是属于该文件夹底下

- components（组件）_button.scss _dropdown.scss _alert.scss

- layout（布局） _header.scss _footer.scss _nav.scss

- pages（页面）pages的话通常会放一些只有这个页面才会使用的样式 _index.scss _content.scss

- themes（主题） _theme.scss _admin.scss

- utils（工具）utils通常都是放一些工具类型，例如p-1、mt-10这类的生成工 _helpers.scss _mixin.scss _function.scss

- vendors（外部）vendors通常都是放一些外部的第三方套件 _bootstrap.scss _swiper.scss

- main or all 最后一个档案就是主要的引入档案，通常这一支里面只会有@import而已
  
  不必一定遵守，只是一种规范。常用的有base,layout,components

# 现代css属性

## transition

transition-property 过渡属性的名称。可以是 none,all,property  
transition-duration 过渡动画的持续时间，默认是 0，所以一定要指定。  
transition-timing-function 过渡属性播放速率函数。  
transition-delay 过渡属性的播放延迟。  

## box-shadow

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
通过设置按钮在悬浮/激活时的box-shadow属性来通过改变按钮阴影营造按钮由近到远的按压效果

## animation
 animation-name 指定关键帧动画的名称    
 animation-duration  动画持续时间  
 animation-timing-function  动画播放速率函数  
 animation-delay  播放延迟  
 animation-iteration-count  动画播放次数，可以指定infinite  
 animation-direction  动画是否反向播放 normal/reverse/alternate(交替)/alternate-reverse  
 animation-fill-mode 动画在执行之前和之后如何将样式应用于其目标 none/forwards(最后一个关键帧)/backwards(第一个关键帧)/both  
 animation-play-state 动画是否运行或者暂停 running/paused




  
