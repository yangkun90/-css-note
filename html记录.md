# html

### html常见元素

meta title	style link  script  base   结构相关

div/section/article/aside/header/footer  语义化标签

p     段落相关

span/em/strong	行内加强

table/thead/tbody/tr/td   表格

ul/ol/li/dl/dt/dd  列表

a  超链接

form /input/select/textarea/button    表单



`<meta charset="utf-8">`

`<meta name="viewport" content="width=device-width,initial-scale=1.0,maximum-scale=1.0,user-scalable=no">`

`<base href="/">`

### html重要属性

a[href,target]    

img[src,alt]  图片相关

table td[colspan,rowspan]  表格合并属性

form[target,method,enctype]  form表单

input[type,value]    输入框

button[type]   按钮

select>option[value]   下拉窗口

label[for]   表单标记



### html版本

一律html5对html4支持非常好



### html5新增内容

新的区块标签

section

article

nav

aside

表单增强

日期、时间、搜素

表单验证

placeholder  自动聚焦等

header /footer 头尾

section/article 区域

nav 导航

aside 不重要内容，侧边

em/strong 强调

i icon  等于图标

### html元素分类

* 按照默认样式分
  * 块级block
  * 行内inline
  * inline-block

### html元素嵌套关系

* 块元素可以包含 块
* 块级元素不一定可以包含块 比如p
* 行内元素一般不能包含块但是也有例外 比如a
* 为什么a可以包含块 ？ w3c是不合法的。实际上引擎计算布局的时候不计算a的。可以看做一个透明层。

### html元素默认样式

* 默认样式的意义
* 默认样式带来问题就是样式不和需求一样
* 一种直接置空reset.css  一种是Normalize.css ，这是一种轻量级的只是修改常见的不好样式

### html真题

1. doctype的意义是什么

   1. 让浏览器以标准模式渲染
   2. 让浏览器知道元素的合法性

2. html xhtml  html5的关系

   1. html属于sgml
   2. xhtml属于xml，是html进行xml严格化的结果

3. html5有什么变化

   1. 新的语义化元素
   2. 表单增强
   3. 新的api（离线，音频，图形，实时通信，本地存储，设备能力）

4. em和i区别

   1. em是语义化的标签，表强调
   2. i是纯样式标签，表斜体
   3. html5中i不推荐使用，一般作为图标

5. 语义化的意义是什么

   1. 开发者容易理解
   2. 机械结构
   3. 有助于seo
   4. semantic microdata

6. 那些元素可以自闭合

   1. 表单元素input
   2. 图片img
   3. br hr
   4. meta link

7. html和dom的关系

   1. html是死的
   2. dom由html解析而来，是活得
   3. js可以维护dom   dom实际是是浏览器解析html文档后生成dom数，存储在内存中，js修改内存的dom结构就是修改html结构了

8. property和attribute

   1. attribute是 死的  如果通过这个修改不会立即映射到property上的。

   2. property是 活得  比如你js修改value是可以直接修改成功。

      > 浏览器解析dom为对象存储到内存，这个时候对象中所有的属性都是property是灵活的
      >
      > attribute	本质上是property的一个子对象。比如attribute获取的dom上自定义的
      >
      > property本质上是标准元素的对象，只有标准对象的属性名

9. form的作用有哪些

   1. 直接提交表单
   2. 使用submit、rest按钮
   3. 便于浏览器保存表单
   4. 第三方库可以整体提取值
   5. 第三方库可以进行表单验证





