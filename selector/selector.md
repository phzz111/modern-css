# css 选择器

## 空格连接 表示后代选择器

```css
.parent span {
	color: aqua;
}
```

parent 的后代 li 不管嵌套多深的 dom 层级都会是浅绿色

## 逗号连接符

```css
.parent span,
.parent-1 {
	color: aqua;
}
```

浅绿色同时作用于逗号相连接的两个选择器选择的内容

## > 子代选择器

```css
.parent > span {
	color: aqua;
}
```

只有 parent 类下的直接子代 span 标签收到影响，parent 下其他嵌套的 span 不受影响

## + 相邻兄弟选择器

```css
.parent div + span {
	color: aqua;
}
```

写法上是 a+b ，其中 a 和 b 必须同一父节点，且 b 必须紧随 a 之后，样式将作用在 b 上。

## ~兄弟选择器

```css
.parent div ~ span {
	color: aqua;
}
```

例子中，div 后面的 span 兄弟都会受影响

## [attr] 属性选择器

```css
[title*='1'] {
	/* value包含1 */
	color: aqua;
}
```

[attr=value]或[attr]的方式匹配 dom 节点  
可以多种模式匹配

```css
[title^="1"]
/* 以1开头 */
[title$="1"]
/* 以1结尾 */
[title~="b"]
/* 空格分隔的值列表 至少有一个值为b */
```

## 伪类选择器

由一个冒号加伪类名称组成，例如常用的:hover

### nth-child 
其中 n 可以理解为 {0，1，2，3} 这样的一个集合

```css
/* 不做用于第一行 通常用于列表渲染 */
.my-ul li:nth-child(n + 2) {
	margin-top: 15px;
	background-color: #ddd;
}
```

### [first||last||nth]-of-type  
   parent :nth-of-type(n) 如果该类型为兄弟节点中第 n 次出现则匹配生效

```css
/* .parent下的div，它的子节点中第一个元素是span */
.parent :first-of-type {
	color: aqua;
}
```

### :is 
is选择器，接收选择器列表。选择器列表可容错，即不会出现列表中某一项匹配不到元素或书写错误导致整个列表无效。通常用于简化大型嵌套选择器

```css
/* 一个Mdn上的例子 */
/* 它可以匹配 ol|ul|menu|dir 下的 ol|ul|menu|dir 下的ul|menu|dir，如果不使用:is选择器而是完整列举将会是非常庞大的工作量（4*4*3） */
:is(ol, ul, menu, dir) :is(ol, ul, menu, dir) :is(ul, menu, dir) {
	list-style-type: square;
}
```

### :where 
   :where 选择器，功能同:is 选择器，但不会提高选择器的特殊性。where 的特殊性始终为 0，这可以让 where 定义的样式更容易被覆盖
### :has
:has选择器，同样接受选择器列表，返回包含选择器列表限制的元素

```css
/* 假设ul下有若干个li，那么只有最后一个li不会染色，因为它后面没有紧邻的li兄弟节点 */
:has(+ li) {
	color: aqua;
}
```
