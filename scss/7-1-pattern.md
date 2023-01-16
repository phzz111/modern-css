# 7-1 pattern

该设计模式主要在于目录结构的区分。

-   base（基础）base 文件夹底下都会放 CSS Reset、或是字体的基础设置等都是属于该文件夹底下

-   components（组件）\_button.scss \_dropdown.scss \_alert.scss

-   layout（布局） \_header.scss \_footer.scss \_nav.scss

-   pages（页面）pages 的话通常会放一些只有这个页面才会使用的样式 \_index.scss \_content.scss

-   themes（主题） \_theme.scss \_admin.scss

-   utils（工具）utils 通常都是放一些工具类型，例如 p-1、mt-10 这类的生成工 \_helpers.scss \_mixin.scss \_function.scss

-   vendors（外部）vendors 通常都是放一些外部的第三方套件 \_bootstrap.scss \_swiper.scss

-   main or all 最后一个档案就是主要的引入档案，通常这一支里面只会有@import 而已

不必一定遵守，只是一种规范。常用的有 base,layout,components
> scss 在文件名开始处添加\_是为了表明该文件是 scss 代码片段，将被引入至其他 scss，不需要编译为 css。引入时不需要额外写*和.scss