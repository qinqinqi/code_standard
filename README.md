# 一、文件/资源命名规范

### 1、通用规则

文件名语义化，尽量避免使用拼音

字母全部小写多个字母用下划线分隔（识别率比驼峰高）

如需缩写单词，应使用约定俗成的缩写方式，不能自造单词以免引起歧义

需要合理的将文件分类到不同的目录，避免一个文件下存放存放大量的文件

压缩版的文件要加上`.min`后缀

### 2、图片命名

图标类--------加icon_前缀

背景类--------加bg_前缀

雪碧图--------加_sprite后缀





# 二、HTML规范

### 1、基础规范

引入的css和js一般不需要指定type属性

除特殊场景外，css写在<head>标签内，js写在</body>前

body里不要写样式，避免闪屏

特殊符号用html实体

html要保持简洁，不要套太多层

### 2、属性顺序

* class
* id、name
* data-*
* src、for、type、href、value
* placeholder、title、alt
* aria-*、role
* required、readonly、disabled

### 3、id/class命名规则

* 多个单词用"-"连接，不能使用下划线和驼峰命名法
* 不可自造缩写
* 避免使用广告拦截词汇
  * ad、ads、adv、banner、sponsor、gg、guangg、guanggao等。

### 4、标签使用-----？？

​	1）img标签必须加alt，尤其是logo、商品图片等关键图片信息，对SEO友好

​	2）减少标签的数量

​	3）所有的标签必须带有结束符，<img/>、<col/>、<base/>、<link/>、<meta/>、<input/>除外。<? br要不要结束标签 ?>



### 5、注释规范

使用注释划分结构快，并与css的注释达成统一格式。



### 6、缩进---？？？

缩进使用1个Tab（占4个空格）;

不要使用Tab和空格混搭额缩进方式



### 7、渲染模式

指定使用最高版本的IE渲染页面。

```<meta http-equiv="X-UA-Compatible" content="edge" />```

国内常见的双核浏览器，指定使用极速模式（webkit内核）来渲染页面。（目前仅360支持）

```<meta name="renderer" content="webkit">```



# 三、css规范

### 1.属性顺序

* 位置（position、display、float等）
* 大小（width、height、、padding、margin等）
* 文字（font、line-height、letter-spacing、color、text-align等）
* 背景（background、border等）
* 其他（opacity、animation、transition等）

### 2.选择器

不得为id、class 加类型选择器进行限制，例如：

`````
/* 推荐 */
#error,
.danger-message {
   font-color: #000;
}

/* 不推荐*/
dialog#error,
p.danger-message {
  font-color: #000;
}
`````

### 3.媒体查询的位置

媒体查询放在相关规则后面或者统一放在稳当底部，若统一放在稳当底部的时候，顺序应按照正常样式进行排布且注释统一。

### 4.简写和省略

* 颜色16进制用小写字母，可以简写到的要简写；
* 如果是小数，省略小数点前边的0；
* 如果是0省略单位；

### 5.前缀

* 同个属性不同前缀的写法需要在垂直方向上保持对齐；
* 无前缀的属性要写在有前缀的属性后边；
* 尽量不要手写前缀属性，推荐使用自动化巩固处理

### 6.空格

* 属性值前加空格，例如：color: #000;
* 选择器>、+、~前后要加空格
* 属性值中的,后加空格
* 每行行末不要有多余的空格
* {前加空格

### 7.换行---？？

* {后和}前要换行，如果只有一条属性规则例外，无需换行；
* 每个属性独占一行；
* 多个选择器的分隔符，后要换行；
* 相邻的两段样式之间 要用一个空行隔开；
* 属性组之间需要有一个空行隔开。

```
/* 不推荐*/
.style
{color: red;background-color: black;}
/* 推荐*/
.style {
  color: red;
  background-color: black;
}

/* 不推荐*/
.style {
  width: 100px;
}
/* 推荐*/
.style {width: 100px;}

/*不推荐*/
.item1, .item2 {
	...
}
/* 推荐*/
.item1,
.item2 {
  ...
}
```

### 8.引号

* 最外层统一使用双引号;
* 属性选择器中的属性值要加引号；
* url的内容要加引号；
  * url加引号的好处降低内容路径被XSS注入风险；避免浏览器的兼容问题。



### 9.其他

后代选择器、子选择器不要超过4层;

慎用 !important;

尽量少用*选择器；



# 四、JS规范

### 1、空格

* 二元运算符法两侧必须有空格
* 一元运算符与操作对象之间不允许有空格

```
var a = !arr.length;
a++;
a = b + c;
```



* ` {`前必须有一个空格
* if/else/for/while/function....关键字后，必须有一个空格

```
//不推荐
if(flag) { 
}
(function () {
}) ();

//推荐
if (flag) {
}
(fuunction () {
  
}) ();
```

* 对象属性的`:`之后必须有空格，之后不允许有空格

```
//不推荐
var obj = {
  a : 1,
  b:2,
  c :3
}

//推荐
var obj = {
  a: 1,
  b: 2,
  c: 3
}
```

* 函数声明、具名函数表达式、函数调用中，函数名和（直接按不允许有空格

```
//不推荐
function funcName () {}
var funName = function funcName () {};
funcName ();

//推荐
function funcName() {}
var funcName = function funcName() {};
```

* `,`和`;`前不允许有空格

```
//不推荐
callFunc(a , b) ;

//推荐
callFunc(a, b);
```

### 2、换行

### 3、简写代码

* 能少写就少写

```
//不推荐
let seatDiscount = 100;
if(seat < 5) {
    seatDiscount = 90;
} else if(seat < 10) {
    seatDiscount = 80;
} else {
    seatDiscount = 70;
}

//推荐
let seatDiscount = seat < 5 ? 90 : 
                           seat < 10 ? 80 : 70;
```

* 使用箭头函数取代简单的函数

```
//不推荐
setTimeout(function () {
	window.location.reload(true);
},1000);

//推荐
setTimeout(() => window.location.reload(true);,1000);
```

* 代码不要嵌套的太深
* 选择器的性能问题（同个父元素尽量减少大量的全局查找）

```
//不推荐
$(".page ul").addClass("show");
$(".page .page-number").addClass("show");
....

//推荐
var $page = $(".page");
$page.find("ul").addClass("show");
$page.fin(".page-number").addClass("show");
...

```

* 尽量不要在`js`里写`css`





