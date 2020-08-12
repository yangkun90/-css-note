# 深入css

## 选择器优先级

1. 判断css来源 一般来说有 浏览器给的默认样式，内联样式，行内样式，外联样式。
2. 内联>行内>=外联>默认。 继承样式优先级很小。比如a元素无法通过继承改变样式，需要指定修改。
3. 权限 内联>id>class >元素 。但是强烈建议不使用id，因为一个id大于n个class的组合，如果在很复杂的样式组合中，我们可能出现，修改class的样式，没有生效，在那里 找id找半天的情况。
4. ！import 同上。优先级会提到最高。注意：！import 对继承设置没有啥作用，！import只是作用于当前选中的元素，而不是继承的元素。
5. 所谓层叠性。就是如果几个权重一样的样式，选中相同的元素。谁在后面会覆盖前面的样式。因为css不可能存在两个下padding或者两个上padding，后面的会覆盖前面的设置。

## 继承

1. color font font-family  font-size  font-weight	font-variant  font-style	line-height	letter-spacing 	text-align	text-index	text-transform	white-space以及	word-spacing
2. list-style   list-style-type  list-style-position    list-style-image    border-collapse   border-spacing
3. 以上都可以被继承。字体，列表设置样式，表格的边框设置 。

## 特殊值

1. inherit 继承   比如设置color：inherit 表示从父元素继承颜色值。
2. initial 表示撤销元素的样式。 回归默认样式。

## 样式简写

1. 样式可以简写 比如 font:normal bold 18px/1.2 "微软雅黑"  实际上 font-style  font-weight font-size/line-height一次设置了。注意简写会覆盖之前设置的。如果我们单独设置某个样式必须在简写之后。
2. 简写的顺序 比如 border 设置的四个顺序是上右下左   三个是上   左和右   下    两个是上和下   左和右
3. background -position  设置的是第一个是水平方向第二个垂直方向的值。

## em和rm

1. 1em等于当前字体的字号。
2. em定义字号的时候 font-size：1.2em 表示为继承的样式字号的1.2倍。
3. 如果一个元素的字号em设置和其他样式也使用了em。会先计算字号em最后根据字号，再去渲染其他样式的em值。
4. em作用于多层继承字号上，会照成难以维护的问题。因为字体全部都是计算得来，你难以记忆。所以字号不用em设置最好。这里推荐使用rem。
5. rem 是根据html根节点设置的字号来计算的。这样有一个统一的确定值。
6. px  rem em 如何选择。字号 rem或者px  边框必须是px因为需要固定大小  em可以设置其他大多数样式。
7. 移动布局中如果要做根据屏幕不同伸缩大小，各大网站的解决方案中最好的就是rem。

## 视口

1. vh 视口高度的1/100
2. vw 视口宽度的 1/100
3. 比如视口宽度一半就是50vw  高度一半就是50vh
4. vmin vmax  表示视口最小和最大限度  ie支持很差，即使edge也是。 其实简单来说你可以看做是min-width max-width之类的。
5. calc() css函数，用于计算支持+ - * /  注意计算两边有空格   font-size:calc(0.5em + 1vw) 很强大
6. calc() 和视口单位实现了自动缩放的功能。缺点是必须要很新的浏览器才支持。

## 无单位样式

1. line-height 可以设置无单位 这个时候行高是字体的倍数  line-height：1.2 就是1.2倍
2. line-height 应该不使用em这种，因为如果行号小于字体大小会出现重叠的问题。
3. 实际上行高这类可以在body中统一设置无单位，然后后面有特殊需求后再设置。

## 你不知道的自定义属性

1. --main-font  有这个属性吗？ 没有！ 这个是自定义的，使用两个--进行区分。
2. 如何使用  --main-font:"微软雅黑"     font-family:var(--main-font) 即可调用
3. 自定义属性值可以修改，以达到动态改变的效果。
4. 使用js可以获取自定义变量动态改变样式。getComputedStyle 可以获取某个元素的样式，然后你可以去修改了
5. 自定义属性是css3的特性



