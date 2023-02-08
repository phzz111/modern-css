## css 模块化脚本

基于Js的导入断言实现 css in js

```js
import triangle from '../geometry/triangle.css' assert { type: 'css' }

//编辑
triangle.insertRule("h1 p { color : green; }")
//插入
document.adoptedStyleSheets = [triangle]

```
