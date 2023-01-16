# 清除浮动

1. 基于 BFC  
   将父级元素设置为 overflow:hidden 等方式触发 Bfc
2. 追加空元素，在浮动元素增加空的兄弟块元素，并 clear:both
3. 基于伪元素，原理同 2
4. 写一个工具类 clearfix
    ```css
    .clearfix {
    	content: '';
    	display: block;
    	clear: both;
    }
    ```