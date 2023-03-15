<a name="Mg9Ek"></a>
## 3.css
<a name="JshyT"></a>
### 1.css简介
css全称：层叠样式表（Cascading Style Sheets）<br />css也是一种标记语言，用于给html结构设置样式，例如：文字大小/颜色/元素宽高等。<br />核心思想：实现了结构与样式的分离<br />层叠：一层一层“涂”上去<br />表：列表
<a name="V9ETr"></a>
### 2.css行内样式
```html
<!DOCTYPE html>
<html lang="zh-CN">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
		<!-- 缺点：书写复杂，写多了臃肿，不能体现结构与样式分离的思想，不能复用     -->
    <!-- 行内样式：在属性里加上style里，只对当前标签起效，
  css样式写在style里，以名值对的形式中间用;做分隔，大小写通用（推荐小写）
  常用在对当前标签添加简单样式时-->
    <h1 style="color:red;font-size: 32px;">今天天气真好啊！</h1>
</body>

</html>
```
<a name="EkGD1"></a>
### 3.css内部样式
```html
<!DOCTYPE html>
<html lang="zh-CN">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <!-- 内部样式：在head标签里写style标签，然后给想给添加样式的标签添加样式 -->
    <!-- 内部样式与行内样式相比，把样式和结构分开，样式可以复用了 -->
    <!-- 缺点，并没有实现结构与样式的完全分离，多个html页面无法复用 -->
    <style>
        h1 {
            color: red;
            font-size: 30px;
        }

        h2 {
            color: green;
            font-size: 28px;
        }

        div {
            height: 300px;
            width: 300px;
            background-color: #000;
        }
    </style>
</head>

<body>

    <h1>今天天气真好啊！</h1>
    <h2>今天学习了前端，真好啊！</h2>
    <div>div1</div>
</body>

</html>
```
<a name="FJVjY"></a>
### 4.css外部样式
```css
h1 {
  color: red;
  font-size: 30px;
}

h2 {
  color: green;
  font-size: 28px;
}

div {
  height: 300px;
  width: 300px;
  background-color: #000;
}
```
```html
<!DOCTYPE html>
<html lang="zh-CN">

  <head>
    <meta charset="UTF-8">
    <title>Document</title>
    <!-- 引用外部样式，rel：样式关系 -->
    <!-- 优势，样式可以复用，结构清晰，可以触发浏览器的缓存机制 -->
    <link rel="stylesheet" href="./01.css">
  </head>

  <body>

    <h1>今天天气真好啊！</h1>
    <h2>今天学习了前端，真好啊！</h2>
    <div>div1</div>
  </body>

</html>
```
<a name="OuXKS"></a>
### 5.css样式优先级
行内样式>内部样式=外部样式<br />看内部样式和外部样式谁后写<br />相同样式后面覆盖前面
<a name="tKHiv"></a>
### 6.css语法规范
选择器{声明块(声明(属性名:属性值);声明;)}<br />最后一组声明，理论上分号可以省略<br />选择器和声明块要加一个空格<br />冒号和属性值之间有空格<br />声明块里用/*注释*/
<a name="p4HaY"></a>
### 7.css代码风格
xxx.min.html,xxx.min.css压缩后的htnl和css文件（空格，回车都没有）
```html
<!DOCTYPE html>
<html lang="zh-CN">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
				/* 项目上线时我们会通过工具（webpack）将展开风格变成紧凑凤，减小文件体积，节约网络
      流量，同时使用户打开网页时更快*/
      
        /* 展开风格：开发时推荐，便于维护和调试 */
        h1{
            color: red;
        }
        /* 紧凑风格：上线时推荐，减小文件体积 */
        h2{color: blue;}
    </style>
</head>

<body>

    <h1>今天天气真好啊！</h1>
    <h2>今天学习了前端，真好啊！</h2>
    <div>div1</div>
</body>

</html>
```
<a name="T9WWT"></a>
### 8.css选择器
<a name="CC3hR"></a>
#### 8.1通配选择器
```css
* {
	margin: 0;
}
/*所有样式，一般用于清除样式 */
```
<a name="fyhNK"></a>
#### 8.2元素选择器
```css
h1 {
 color: red;
}
/*<h1>今天天气真好</h1>  */
```
<a name="RTcSw"></a>
#### 8.3id选择器
```css
#name {
	width: 30px;
}
/* 
一个元素只能有一个id选择器，多个选择器的id属性值不能相同
idshuxz尽量由:字母/数组/下划线/短杠组成，尽量由字母开头不要包含空格，区分大小写
一个属性可以同时有id和class属性
<div id="name">今天天气真好</div> 
*/
```
<a name="Ehyow"></a>
#### 8.4类选择器
```css
.root {
	width: 400px;
  height: 400px;
}
/*一个元素可以有多个类选择器
<div class="root">今天天气真好</div>
*/
```
<a name="wfOux"></a>
#### 8.5交集选择器
```css
/*紧紧连在一起的样式，表示且的关系，元素选择器必须写前面，不可能有两个元素选择器 
可以两个类名选择器，后声明的样式会把前面的覆盖*/
div.root1 {
	width: 400px;
  height: 400px;
}

/*
<div class="root1 root2">今天天气真好</div>
*/
```
<a name="E8coU"></a>
#### 8.6并集选择器
```css
.root1,root2 {
	width: 400px;
  height: 400px;
}
/*
<div class="root1">今天天气真好</div>
<div class="root2">今天天气真好</div>
*/
```
<a name="CrJFB"></a>
#### 8.7html元素之间的关系
父元素：直接包裹某个元素的元素，就是该元素的父元素，如ul>li中的ul。<br />子元素：被父元素直接包含的元素，如ul>li中的li。<br />祖先元素：父亲的父亲。。。，一直往外赵，都是祖先。<br />后代元素：儿子的儿子。。。，一直往里找，都是后代。<br />兄弟元素：具有相同父亲的元素，互为兄弟元素。
<a name="dFXNe"></a>
#### 8.8后代子代选择器
```html
<!DOCTYPE html>
<html lang="zh-CN">

  <head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
      /*
      后代可以重复嵌套
      后代选择器最终选择的是后代
      结构一定要满足html结构要求，例如：p标签中不能写h1-h6标签
      */
      /* ul的所有后代li */
      ul li {
        color: red;
      }

      /* ol的所有儿子li */
      ol>li {
        color: blue;
      }

      ol div li {
        color: gray;
      }
    </style>
  </head>

  <body>
    <ul>
      <li>抽烟</li>
      <li>喝酒</li>
      <li>烫头</li>
      <div>
        <li>踢球</li>
      </div>
    </ul>
    <hr>
    <ol>
      <li>张三</li>
      <li>李四</li>
      <li>王五</li>
      <div>
        <li>小猫</li>
      </div>
    </ol>
  </body>

</html>
```
<a name="QRFf5"></a>
#### 8.9兄弟选择器
```html
<!DOCTYPE html>
<html lang="zh-CN">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
        /* 通用兄弟选择器：div后面的兄弟 */
        div~p {
            color: aqua;
        }

        /* 相邻兄弟选择器div后面紧靠着的兄弟*/
        div+p {
            color: #ff0000;
        }
    </style>
</head>

<body>
    <div>尚硅谷</div>
    <p>前端</p>
    <p>java</p>
    <p>大数据</p>
    <p>ui</p>
</body>

</html>
```
<a name="UyEt3"></a>
#### 8.10属性选择器
```html
<!DOCTYPE html>
<html lang="zh-CN">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
        /* 1.选中具有title元素的 */
        [title] {
            color: red;
        }

        /* 2.选中具有title元素且属性值为atguigu2 */
        [title="auguigu2"] {
            color: blue;
        }

        /* 3.选中具有title元素且属性值以a开头 */
        [title^="a"] {
            font-size: 32px;
        }

        /* 4.选中具有title元素且属性值以3结尾 */
        [title$="3"] {
            font-weight: bold;
        }

        /* 5.选中具有title元素且属性值含4 */
        [title*="4"] {
            color: aqua;
        }
    </style>
</head>

<body>
    <div title="auguigu1">尚硅谷1</div>
    <div title="auguigu2">尚硅谷2</div>
    <div title="auguigu3">尚硅谷3</div>
    <div title="atguigu4">尚硅谷4</div>
</body>

</html>
```
<a name="gug7j"></a>
### 9.伪类选择器
<a name="QNN9m"></a>
#### 9.1伪类的概念
什么是伪类？<br />很像类，但不是类，是元素特殊状态的一种描述
<a name="NCbi7"></a>
#### 9.2动态伪类
动态即元素状态会发生改变
```html
<!DOCTYPE html>
<html lang="zh-CN">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
        /* 顺序为lvha：link和visited时a独有的元素，hover和active是所有元素都有的 */
        /* 未访问时color为brown */
        a:link {
            color: brown;
        }

        /* 访问过color为brown */
        a:visited {
            color: gray;
        }

        /* 鼠标悬浮时color为blue */
        a:hover {
            color: blue;
        }

        /* 激活时color为yellow */
        a:active {
            color: yellow;
        }
        /* 获取焦点时，focus只有表单类元素有 */
        input:focus {
            border: 3px solid rgb(255, 55, 0);
        }
    </style>
</head>

<body>
    <a href="https://www.baidu.com">百度</a>
    <a href="https://www.jd.com">京东</a>
    <input type="text">
</body>

</html>
```
<a name="dlTku"></a>
#### 9.3结构伪类
<a name="q2pR7"></a>
##### 9.3.1结构伪类1
```html
<!DOCTYPE html>
<html lang="zh-CN">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
        /* div第一个儿子且为p元素 */
        /* div>p:first-child {
            color: red;
        } */

        /* div第一个儿子 */
        /* div>:first-child {
            color: red;
        } */
        /* div中是第一个儿子的p元素，无论是谁都儿子 */
        /* div p:first-child {
            color: red;
        } */
        /* 是第一个儿子的p元素 */
        /* p:first{
            color: red;
        } */
    </style>
</head>

<body>
    <div>
        <p>张三：98分</p>
        <div>
            <p>李四：88分</p>
        </div>
        <p>王五：78分</p>
        <p>赵六：68分</p>
    </div>
</body>

</html>
```
<a name="q9i8S"></a>
##### 9.3.2结构伪类2
```html
<!DOCTYPE html>
<html lang="zh-CN">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
        /* 最后一个儿子且为p元素 */
        /* div>p:last-child {
            color: rgb(191, 0, 0);
        } */
        /*  */
        /* div第6个儿子且为p元素 */
        /* div>p:nth-child(6) {
            color: red;
        } */
        /* div的偶数的儿子且为p元素(even),奇数为2n+1(odd) */
        /* div>p:nth-child(2n) {
            color: red;
        } */
        /* div的儿子且为p元素的前5个元素，n必须写前面：an+b的形式 */
        /* div>p:nth-child(-n+5) {
            color: red;
        } */

     		/* 第一个p元素 */
        /* p:first-of-type {
            color: red;
        } */
        /*  div的儿子中第一个p元素*/
/*         div>p:nth-of-type(1) {
            color: red;
        } */
    </style>
</head>

<body>
    <div>
        <p>张三：98分</p>
        <p>李四：88分</p>
        <p>王五：78分</p>
        <p>赵六：68分</p>
        <p>赵七：58分</p>
        <p>老八：48分</p>
    </div>
</body>

</html>
```
<a name="MLZ2L"></a>
##### 9.3.3结构伪类3
```html
<!DOCTYPE html>
<html lang="zh-CN">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
        /* 倒数第一个div儿子且为p元素 */
        /* div>p:nth-last-child(1) {
            color: red;
        } */
        /* 没有兄弟的span元素
        span:only-child {
            color: red;
        } */
        /* 兄弟中只有一个span元素 */
        /* span:only-of-type {
            color: red;
        } */
        /* 整个html的根元素，也就是html*/
        /* :root {
            color: gray;
        } */
        /* 没有元素的div，没有内容的div */
        div:empty {
            width: 500px;
            height: 500px;
            background-color: red;
        }
    </style>
</head>

<body>
    <div>
        <span>测试</span>
        <p>张三：98分</p>
        <p>李四：88分</p>
        <p>王五：78分</p>
        <p>赵六：68分</p>
        <p>赵七：58分</p>
        <p>老八：48分</p>
    </div>
    <div></div>
</body>

</html>
```
<a name="YijbX"></a>
##### 9.3.4否定伪类
```html
<!DOCTYPE html>
<html lang="zh-CN">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
        /* :not()排除满足括号内的元素 */
        /* 选中div中的儿子p元素，排除类名为fail的元素，括号里可以是类/id/标签元素 */
        /* div>p:not(.fail) {
            color: red;
        } */
        /* 选中div中儿子p元素，排除第一个和不及格的 */
        /* div>p:not(.fail, :first-child) {
            color: red;
        } */

    </style>
</head>

<body>
    <div>
        <p>张三：98分</p>
        <p>李四：88分</p>
        <p>王五：78分</p>
        <p>赵六：68分</p>
        <p class="fail">赵七：58分</p>
        <p class="fail">老八：48分</p>
    </div>
    <div></div>
</body>

</html>
```
<a name="Kt5Vy"></a>
##### 9.3.5ui伪类
```html
<!DOCTYPE html>
<html lang="zh-CN">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
        /* 选中的是勾选的复选框或单选按钮 */
        input[type="checkbox"]:checked {
            width: 200px;
            height: 200px;
        }

        /*禁用的input元素  */
        input:disabled {
            background-color: cadetblue
        }

        /* 可用的input元素 */
        input:enabled {
            background-color: #9d4949;
        }
    </style>
</head>

<body>
    复选框<input type="checkbox">
    <input type="text">
    <input type="text" disabled>
</body>

</html>
```
<a name="x1iG1"></a>
##### 9.3.6目标伪类
```html
<!DOCTYPE html>
<html lang="zh-CN">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
        div {
            height: 400px;
            background-color: #ff7373;
            margin-bottom: 5px;
        }

        /*选中锚点指向的元素  */
        div:target {
            background-color: green;
        }
    </style>
</head>

<body>
    <a href="#one">去看第一个</a>
    <a href="#two">去看第二个</a>
    <a href="#three">去看第三个</a>
    <a href="#four">去看第四个</a>
    <a href="#five">去看第五个</a>
    <a href="#six">去看第六个</a>
    <div id="one">第一个</div>
    <div id="two">第二个</div>
    <div id="three">第三个</div>
    <div id="four">第四个</div>
    <div id="five">第五个</div>
    <div id="six">第六个</div>

</body>


</html>
```
<a name="vqIQW"></a>
##### 9.3.7语言伪类
```html
<!DOCTYPE html>
<html lang="zh-CN">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
        /* div lang="en" */
        div:lang(en) {
            font-size: 32px;
        }

        /* div lang="zh" */
        div:lang(zh) {
            color: blue;
        }

        /* 所有lang为en的元素 */
        :lang(en) {
            color: red;
        }
    </style>
</head>

<body>
    <div>尚硅谷</div>
    <div lang="en">atguigu</div>
    <p>前端学习</p>
    <span>今天天气真不错</span>
</body>


</html>
```
<a name="oDmO9"></a>
### 10.伪元素选择器
```html
<!DOCTYPE html>
<html lang="zh-CN">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>
<style>
    /* 伪元素：很像元素，但不是元素，是元素的一些特殊位置。一些单个冒号也可以 */
    /* 选中div里第一个文字 */
    div::first-letter {
        color: red;
        font-size: 32px;
    }

    /* div中第一行文字 */
    div::first-line {
        background-color: aquamarine;
    }

    /* div中被鼠标选择的文字 */
    div::selection {
        background-color: green;
    }

    /* 选中input元素中的提示文字 */
    input::placeholder {
        color: rgb(255, 140, 0);
    }

    /* p元素的内容之前，创建一个子元素，必须配合content使用 */
    p::before {
        content: "￥";
    }

    /* p元素内容之后，创建一个子元素，必须配合content使用 */
    p::after {
        content: ".00";
    }
</style>

<body>
    <!-- lorem:随机生成一段英文：常用于当作占位符 -->
    <div>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Perspiciatis cum maxime neque tempora inventore
        laudantium unde quidem maiores, perferendis voluptatum ea accusamus aliquid esse cupiditate iste voluptate.
        Labore, voluptatem unde!
    </div>
    <input type="text" placeholder="请输入用户名">
    <p>19</p>
    <p>19</p>
    <p>19</p>
</body>

</html>
```
<a name="aN4gF"></a>
### 11.css选择器优先级
（行内 >） id选择器 > 类选择器 > 元素选择器 > 配选择器
```html
<!DOCTYPE html>
<html lang="zh-CN">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
        /* 
        格式（a,b,c）a:id选择器的个数，b:类、伪类、属性选择器的个数，c:元素、伪元素选择器的个数，通配选择器(0,0,0)
            --比较：一位一位比较，如果相等遵循后来居上
            --(0,2,1)>(0,1,3)
      			--vscode鼠标放在选择器上会标出选择器权重
        */
        .container span.slogan {
            color: red;
        }

        div>p>span:nth-child(1) {
            color: rgb(166, 255, 0);
        }
				/* 加上!important权重最强，加在某个属性值上       */
        .slogan{
          color: purple !important;
    </style>
</head>

<body>
    <div class="container">
        <p>
            <span class="slogan">今天天气真不错</span>
            <br>
            <span>今天学习了css真开心</span>
        </p>
    </div>
</body>

</html>
```
<a name="Ofm84"></a>
### 12.css三大特性

1. 层叠性：如果发生了样式冲突，那么会根据一定的规则（选择器优先级），进行样式的层叠（覆盖）
> 什么是样式冲突：元素的同一个样式名，被设置了不同的值，这就是冲突。

2. 继承性：元素会自动拥有其父元素、或其祖先元素上所设置的某些样式
> 优先继承离得进的（`font-size`，关于文字的样式），不能继承的`background-color`

3. 优先级
> `!important`>行内>id选择器>类选择器>元素选择器>*>继承的样式
> 复杂的需要计算权重，并集选择器是分开计算的！

<a name="Rl304"></a>
### 13.css像素与颜色
<a name="Ssvjn"></a>
#### 13.1像素

- 不同的电脑1px不同，分辨率更高的设备默认缩放倍数也会增大。
- px是网页设计的基本单位。
<a name="ABse6"></a>
#### 13.2颜色名

- 能写的颜色名有限
- 表达的颜色不够精细

红色：`red`，绿色：`green`，蓝色：`blue`，紫色：`purple`<br />橙色：`orange`，灰色`gray`
<a name="pfLB0"></a>
#### 13.3rgb与rgba

- r:red，g:green，b:blue，光的三原色

全部写数字或者全部写百分比<br />（0-255，0-255，0-255）or（0-100%，0-100%，0-155%）

- a:透明度

范围：0-1，完全透明到完全不透明<br />取色器：qq ctrl+alt+a
<a name="mGQBp"></a>
#### 13.4颜色的第三种表示HEX和A
#0000000：前两位表示红色，中间两位表示绿色，最后两位表示蓝色<br />像#ffccee这种3组两两相同的可以简写成：#dce，最后一位透明度也要简写<br />十六进制表示：#000黑色，#fff白色，字母不区分大小写<br />最后再加两位表示透明度，同样是十六进制
<a name="nfabi"></a>
#### 3.13.5颜色的第四种表示HSL和HSLA
hsl(色相,饱和度,亮度)<br />hsla(色相,饱和度,亮度,透明度)<br />色相由角度表示，表示在色相环什么位置：deg表示度
> 0度Red，60度Yellow，120度Green，180度Cyan，240度Blue，300度Magenta

饱和度：0-100%<br />亮度：0-100%
<a name="Oivic"></a>
### 14.常用css属性
<a name="Dk1TA"></a>
#### 14.1字体

