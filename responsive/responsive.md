# 基于 rem 构建的响应式网站

1. 1rem 总是和 html 的 font-size 相等
2. 如果我们在开发时将 html 的 font-size 设置 10px（默认值为 16px)，就可以轻松的将设计图中的 px 转为 rem
3. 为了保持响应式与可缩放性，将 font-size10px 基于 10/16=>0.625 改为 62.5%