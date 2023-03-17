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
<a name="d9bal"></a>
##### 14.1.1字体族
```html
<!DOCTYPE html>
<html lang="zh-CN">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
        span {
            /* font-size:字体大小，浏览器默认的字体大小不相同，
            每个元素最好明确指出字体大小，通常给body设置font-size，
            这样所有元素都可以继承 */
            font-size: 24px;
            /* 字体：（微软雅黑，楷体，宋体……），字体名最好加上引号，多个字体可以形成字体族，
            字体族最好都是一种类型如：衬线、非衬线。从前到后找到能用的停止，一般最后写通用字体
            serif和sans-serif不用加引号*/
            /* 衬线字体(serif)：横竖撇捺有棱角，非衬线字体(sans-serif)：没有明显的棱角，
            一般用非衬线字体 */
            /* 字体最好写英文名，防止遇到兼容问题。Microsoft YaHei:微软雅黑，STHupo:华文琥珀，SimSun:宋体 */
            /* font-family: "宋体"; */
            font-family: "翩翩体-简", "宋体", "楷体", "微软雅黑", sans-serif;
        }
    </style>
</head>

<body>
    <span>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Officiis voluptatem nesciunt magnam modi molestias.
        Dolore ipsa laboriosam aliquid officia incidunt repellendus iure ex magnam repellat! Quod aliquid sunt
        praesentium debitis.</span>
</body>

</html>
```
<a name="G7fkQ"></a>
##### 14.1.2字体风格
```html
<!DOCTYPE html>
<html lang="zh-CN">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
        /* 
            font-style:
            --normal默认值|italic斜体|oblique斜体
            --italic：作者设置的倾斜字体，没有设置相当于oblique
            --oblique：在正常字体上强制倾斜
            （em是强调语义，不重在字体倾斜）
        */
        .atguuigu1 {
            font-size: 50px;
            font-style: normal;
        }

        .atguuigu2 {
            font-size: 50px;
            font-style: italic;
        }

        .atguuigu3 {
            font-size: 50px;
            font-style: oblique;
        }
    </style>
</head>

<body>
    <div class="atguuigu1">尚硅谷1</div>
    <div class="atguuigu2">尚硅谷2</div>
    <div class="atguuigu3">尚硅谷3</div>
</body>

</html>
```
<a name="xNJYJ"></a>
##### 14.1.3字体粗细
```html
<!DOCTYPE html>
<html lang="zh-CN">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
        /* 
            font-weight:lighter|normal|bold|bolder|数值
            --lighter   偏细
            --normal    正常
            --bold      偏粗
            --bolder    更粗，大部分字体样式默认只有3种粗细，这时效果与bold一样
            --数值      大部分字体样式默认只有3种粗细，100-300效果与lighter一样，400-500一般，600-900bold
        */
        div {
            font-size: 50px;
        }

        .atguuigu1 {
            font-weight: lighter
        }

        .atguuigu2 {
            font-weight: normal;
        }

        .atguuigu3 {
            font-weight: bold;
        }

        .atguuigu4 {
            font-weight: bolder;
        }

        .atguuigu5 {
            font-weight: 100;
        }
    </style>
</head>

<body>
    <div class="atguuigu1">尚硅谷1</div>
    <div class="atguuigu2">尚硅谷2</div>
    <div class="atguuigu3">尚硅谷3</div>
    <div class="atguuigu4">尚硅谷4</div>
    <div class="atguuigu5">尚硅谷5</div>
    <div class="atguuigu6">尚硅谷6</div>
</body>

</html>
```
<a name="JbeRD"></a>
##### 14.1.4字体复合属性
```html
<!DOCTYPE html>
<html lang="zh-CN">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
        /* 
            --开发中推荐使用复合属性，如果只调大小那就写font-size
            --必须按顺序，字体大小和字体族必写，其他属性值加在它们前面
            --font：字体粗细 字体大小 字体族;
        */
        .atguuigu1 {
            font: 30px "Microsoft YaHei", sans-serif;
        }

        .atguuigu2 {
            font: 30px "SimSun", serif;
        }

        .atguuigu3 {
            font: 30px "STHupo", sans-serif;
        }
    </style>
</head>

<body>
    <div class="atguuigu1">尚硅谷1</div>
    <div class="atguuigu2">尚硅谷2</div>
    <div class="atguuigu3">尚硅谷3</div>
</body>

</html>
```
<a name="yNwNe"></a>
#### 14.2文本属性
<a name="FifRu"></a>
##### 14.2.1文本颜色
`color: red;``color: rgb(255,0,0);``color: rgba(255,0,0,.5);``color: #ff000088;`<br />`color: #f00;``color: hsl(30edg,100%,50%);``color: hsla(30edg,100%,50%,.5);`
<a name="jAoHb"></a>
##### 14.2.2文本间距
```html
<!DOCTYPE html>
<html lang="zh-CN">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
        /* 
            可以有负值
            letter-spacing:单词间距
            word-spacing:单词间距，不管中文（按空格识别）

        */
        .div1 {
            background-color: #d87070;
        }

        .div2 {
            letter-spacing: 5px;
            background-color: #b5d870;
        }

        .div3 {
            word-spacing: 50px;
            background-color: #70bcd8;
        }
    </style>
</head>

<body>
    <div class="div1">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Ipsa, ut!</div>
    <div class="div2">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Ipsa, ut!</div>
    <div class="div3">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Ipsa, ut!</div>
</body>

</html>
```
<a name="BIHrg"></a>
##### 14.2.3文本修饰
```html
<!DOCTYPE html>
<html lang="zh-CN">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
        /* 
            text-decoration:overline|underline|linethrouth|none，
            复合属性没有顺序，一般为位置、样式、颜色
            位置
            --overline：上划线（常用
            --underline：下划线（常用
            --line-throuth：删除线
            --none：没有效果，用于删除效果
            样式：
            --dotted：虚线
            --wavy：波浪线
            --double：双实线
            颜色
            --red
            ins和del有效果，主要重语义
        */
        diV {
            font-size: 32px;
        }

        .auguigu1 {
            text-decoration: overline dotted;
        }

        .auguigu2 {
            text-decoration: underline wavy;
        }

        .auguigu3 {
            text-decoration: line-through double;
        }

        .auguigu4 {
            text-decoration: none;
        }
    </style>
</head>

<body>
    <div class="auguigu1"> 尚硅谷1</div>
    <div class="auguigu2"> 尚硅谷2</div>
    <div class="auguigu3"> 尚硅谷3</div>
    <div class="auguigu4"> 尚硅谷4</div>
    <ins>测试1：下划线</ins>
    <del>测试2：删除线</del>
</body>

</html>
```
<a name="lFNiu"></a>
##### 14.2.4文本缩进
`text-indent: 2em;/*首行缩进2格*/`
<a name="fVtNN"></a>
##### 14.2.5文本对齐
```html
<!DOCTYPE html>
<html lang="zh-CN">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
        /* 
            text-align:center|left(默认)|right        
        */
        div {
            text-align: center;
        }
    </style>
</head>

<body>
    <div>Lorem ipsum dolor sit amet consectetur adipisicing elit.</div>
</body>

</html>
```
<a name="vMwno"></a>
##### 14.2.6细说font-size
![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1678858308617-f0bd132d-7c42-48e2-ad25-8aada549a8b2.png#averageHue=%234a4948&clientId=ue8123a1f-cfc9-4&from=paste&height=300&id=u33e7bb70&name=image.png&originHeight=412&originWidth=1704&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=225330&status=done&style=none&taskId=udef44bd4-36f6-45a9-8855-f4b08714747&title=&width=1239.2727272727273)<br />![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1678858262531-eb65acac-96ff-4ee0-92f3-2114ff481cee.png#averageHue=%23515050&clientId=ue8123a1f-cfc9-4&from=paste&height=413&id=uea4de549&name=image.png&originHeight=568&originWidth=1879&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=252993&status=done&style=none&taskId=u91557227-001f-4f50-8091-877a2a22ddd&title=&width=1366.5454545454545)![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1678858272895-8dc6c1ac-f8d0-48c8-b956-66818f1d0d24.png#averageHue=%234b4a49&clientId=ue8123a1f-cfc9-4&from=paste&height=371&id=u6f243259&name=image.png&originHeight=510&originWidth=1896&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=282768&status=done&style=none&taskId=u9eb48110-58e1-4c9f-bd04-496a159e98b&title=&width=1378.909090909091)
<a name="DIVI9"></a>
##### 14.2.7文本行高
`line-height:30px`,鼠标选中的一行，蓝色背景部分高即是行高，行与行之间是紧密连接的。<br />`line-height: 1.5(常用)`最好是`font-size`的1.5倍-2倍,`line-height: 150%`

- 由于字体设置原因，文字在一行当中，并不是绝对垂直居中，若一行都是文字，不会太影响观感。
- 行高注意事项
1. 当`line-height=0px`时
- 多行文字都叠在一起              --文字间距为0                  
- 背景色消失                  
- 文字顶部部消失一小块           --因为文字站在中央，所以一部分会超出去
2. `line-height<0`时会被浏览器强制改为normal(无效属性)
3. 行高以一行中最高的字为主。
4. 子元素会继承父元素的行高，继承数值会按照font-size进行计算，px会为固定值不看font-size。
5. `line-height`和`height`有什么关系？
- `height`是盒子的高度，`line-height`是一行的高度
-  设置了`height`，`height`就是设置的值，没设置`height`就是`line-height`*行数
6. 行高的应用场景
- 多行内容时，调整行与行之间的间距
- 单行文字的垂直居中`height=line-height`
```html
<!DOCTYPE html>
<html lang="zh-CN">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
        /* 
            让height和line-height相同可使单行文本垂直居中  
        */
        div {
            font-size: 32px;
            background-color: #7fc8ff;
            height: 100px;
            line-height: 100px;
        }
    </style>
</head>

<body>
    <div>Lorem ipsum.尚硅谷</div>
</body>

</html>
```
<a name="cNE1r"></a>
##### 14.2.8文本垂直对齐

- 默认靠顶部对齐
- `height=line-height`中间对齐
- `line-height=2*height-font-size-x(x为根据字体族动态调整的值)`底部对齐（不推荐，后面用定位）
<a name="RZYbv"></a>
##### 14.2.9vertical-align
```html
<!DOCTYPE html>
<html lang="zh-CN">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
        /* 
            vertical用于控制元素所在那一行的垂直方向上的对齐方式
            vertical-align:top|bottom|baseline(默认值，基线对齐)|middle(使元素中部与父元素的基线加上父元素x-height的一半对齐)
            vertical-align不能控制块元素
        */
        div {
            font-size: 100px;
            height: 300px;
            background-color: #7fc8ff;

        }

        div span {
            font-size: 40px;
            background-color: orange;
            vertical-align: top;
        }
    </style>
</head>

<body>
    <div>
        尚硅谷X<span>X前端</span>
    </div>
</body>

</html>
```
<a name="RBiZd"></a>
#### 14.3列表相关属性
```html
<!DOCTYPE html>
<html lang="zh-CN">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
        /*
        列表符号样式：（ol、ul、li）
            list-style-type:none|lower-roman|upper-roman|decimal
            none:无样式
            lower-roman:小写符号
            upper-roman:大写符号数字
            decimal:符号变数字
            disc:圆形
            square:实心方块
         */
        /* 
        列表符号的位置：
            list-style-position:inside|outside
            inside:里面
            outside:外面
         */
        /* 
        自定义列表符号：
            list-style-image:url()
         */
        /* 
        符号复合属性：
        list-style: 无固定顺序
         */
        ul {
            list-style: none outside url(./专属顾问.png);
            /* list-style-type: upper-roman;
            list-style-position: outside;
            list-style-image: url(./专属顾问.png) */
        }

        li {
            background-color: rgb(199, 139, 255);
        }
    </style>
</head>

<body>
    <ul>
        <li>《震惊!两男子竟在教师做这种事情》</li>
        <li>《一夜暴富指南》</li>
        <li>《给成功男人的五条建议》</li>
    </ul>
</body>

</html>
```
<a name="wlluU"></a>
#### 14.4表格相关属性
```html
<!DOCTYPE html>
<html lang="zh-CN">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
        /* 
            border-style:solid(实线)|dotted(点)|dashed(虚线)
            border:2px green solid;
            边框相关的属性，不仅仅使表格能用，其他元素也能用
        */
        table {
            border: 2px green solid;
            /* border-style: solid;
            border-color: green;
            border-width: 2px; */
        }

        td,
        th {
            border: 2px orange solid;
        }

        h2 {
            border: 2px orange dashed;
        }
    </style>
</head>

<body>

    <h2>边框相关的属性，不仅仅使表格能用，其他元素也能用</h2>
    <table>
        <caption>人员信息</caption>
        <thead>
            <th>序号</th>
            <th>姓名</th>
            <th>年龄</th>
            <th>性别</th>
            <th>政治面貌</th>
        </thead>
        <tbody>
            <tr>
                <td>1</td>
                <td>张三</td>
                <td>24</td>
                <td>男</td>
                <td>党员</td>
            </tr>
            <tr>
                <td>2</td>
                <td>李四</td>
                <td>18</td>
                <td>男</td>
                <td>群众</td>
            </tr>
            <tr>
                <td>3</td>
                <td>王五</td>
                <td>22</td>
                <td>女</td>
                <td>党员</td>
            </tr>
        </tbody>
        <tfoot></tfoot>
    </table>
</body>

</html>
```
<a name="mVOg1"></a>
#### 14.5表格独有属性
```html
<!DOCTYPE html>
<html lang="zh-CN">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
        /* 
        表格独有属性：
            单元格列宽：
            table-layout:auto(根据文字调整)|fiexd(宽度统一)
            单元格间距：(单元格合并后间距不再生效)
            border-spacing:2px;
            合并相邻单元格边框：
            border-collapse:separate(不合并)|collapse(合并，颜色按单元格的)
            隐藏没有内容的单元格：(单元格合并后间距不再生效)
            empty-cells:hide(不展示)|show(展示)
            设置表格标题的位置：
            caption-side:bottom|top
        */
        table {
            border: 2px rgb(0, 0, 0) solid;
            width: 400px;
            table-layout: auto;
            border-spacing: 0;
            border-collapse: collapse;
            empty-cells: hide;
            caption-side: top;
        }

        td,
        th {
            border: 2px orange solid;
        }

        th:first-of-type {
            width: 30px;
        }
    </style>
</head>

<body>
    <table cellspace="0">
        <caption>人员信息</caption>
        <thead>
            <th>序号</th>
            <th>姓名</th>
            <th>年龄</th>
            <th>性别</th>
            <th>政治面貌</th>
        </thead>
        <tbody>
            <tr>
                <td>1</td>
                <td>张三</td>
                <td>24</td>
                <td>男</td>
                <td>党员</td>
            </tr>
            <tr>
                <td>2</td>
                <td>李四</td>
                <td>18</td>
                <td></td>
                <td>群众</td>
            </tr>
            <tr>
                <td>3</td>
                <td>王五</td>
                <td>22</td>
                <td>女</td>
                <td>党员</td>
            </tr>
        </tbody>
        <tfoot></tfoot>
    </table>
</body>

</html>
```
<a name="UENlq"></a>
#### 14.6背景相关属性
```html
<!DOCTYPE html>
<html lang="zh-CN">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
        div {
            border: 5px rgb(0, 0, 0) solid;
            width: 400px;
            height: 400px;
            /* 设置背景颜色，默认transparent(透明) */
            /* background-color: red; */
            /* 背景图片 */
            /* background-image: url(https://shijuepi.com/uploads/allimg/201222/1-2012221T114.jpg); */
            /* 设置背景图片的重复方式:repeat(默认重复)|no-repeat(不重复)|repeat-x|repeat-y*/
            /* background-repeat: repeat; */
            /* 控制背景图片的位置:水平 垂直，不写默认center，一个center（水平和垂直都是center） */
            /* background-position: left top; */
            /* 控制图片位置2（背景超出会隐藏）:相对于左上角 
            ----x
            |
            y
            */
            background-position: 10px 20px;
            /* 背景复合属性:没有固定顺序，！(没写颜色默认透明，可能把前面的覆盖) */
            background: repeat url(https://shijuepi.com/uploads/allimg/201222/1-2012221T114.jpg) center;
            font-size: 40px;
        }
    </style>
</head>

<body>
    <div>今天学习了css</div>
</body>

</html>
```
<a name="dEpRK"></a>
#### 14.7鼠标相关属性
```html
<!DOCTYPE html>
<html lang="zh-CN">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
        div {
            width: 400px;
            height: 400px;
            background-color: aquamarine;
            /* 鼠标悬浮效果：pointer(小手)|move(拖拽)|wait(等待)|crosshair(十字架)|help(问号)|url(),pointer */
            cursor: url("./鼠标.png"), pointer;

        }
    </style>
</head>

<body>
    <div>
        放入鼠标
        <input type="text">
        <a href="https://www.baidu.com">百度</a>
    </div>
</body>

</html>
```
<a name="BhMQK"></a>
#### 14.8盒子模型
<a name="NDatN"></a>
#####  14.8.1常用长度单位
```html
<!DOCTYPE html>
<html lang="zh-CN">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
        /* 
      	css中长度必须加单位，否则失效
        常用长度单位：
        --px(像素)
        --em(相对于当前元素font-size的倍数,font-size有默认字体大小)
        --rem(对于根元素font-size的倍数)
        --%(相对于父元素)
        */
        div {
            /* width: 400px;
            height: 400px; */
            /* width: 10em;
            height: 10em; */
            /* width: 10rem;
            height: 10rem; */
            width: 30%;
            height: 30%;
            font-size: 1rem;
            text-indent: 2em;
            background-color: rgb(88, 138, 224);
        }
    </style>
</head>

<body>
    <div>咕咕咕咕咕咕咕咕</div>
</body>

</html>
```
<a name="ksOma"></a>
##### 14.8.2元素的显示模式
`display:none(隐藏)|block|inline|inline-block;`<br />![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1678887835967-fd6fa91c-4bd2-4664-99ba-8a3ee4d98393.png#averageHue=%23dfe4dc&clientId=u2f1c48df-5935-4&from=paste&height=665&id=u9565293c&name=image.png&originHeight=914&originWidth=896&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=249415&status=done&style=none&taskId=u8fb95046-a480-4688-aa4a-5f877fbf83e&title=&width=651.6363636363636)<br />![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1678887914836-aff8b82a-ef85-4a6e-b1dd-cefccbcbb654.png#averageHue=%23e5e6da&clientId=u2f1c48df-5935-4&from=paste&height=604&id=u0732f5d0&name=image.png&originHeight=830&originWidth=1110&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=243279&status=done&style=none&taskId=ub942e011-c2ad-499e-98b4-5a1ff9f32dc&title=&width=807.2727272727273)
<a name="PAOG0"></a>
##### 14.8.3盒子模型的组成部分
![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1678890261808-1af083e1-ca73-427e-b375-ee23181a1b42.png#averageHue=%2393834d&clientId=u2f1c48df-5935-4&from=paste&height=660&id=u34030bbf&name=image.png&originHeight=908&originWidth=1775&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=1094357&status=done&style=none&taskId=u3f7bd158-1fd0-4308-9032-cbac9a4164c&title=&width=1290.909090909091)![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1678890725547-1b6df3fd-8271-435c-869a-daddf47640f8.png#averageHue=%23d8d7ce&clientId=u2f1c48df-5935-4&from=paste&height=652&id=u23456671&name=image.png&originHeight=897&originWidth=859&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=271667&status=done&style=none&taskId=ua39b76ca-8132-4ee7-8936-7be582562b5&title=&width=624.7272727272727)
<a name="N2YwE"></a>
##### 14.8.4内容区content
```html
<!DOCTYPE html>
<html lang="zh-CN">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
        div {
            /* 最小宽度 */
            min-width: 200px;
            /* 最大宽度 */
            max-width: 800px;
            /* 最小高 */
            min-height: 40px;
            /* 最大高 */
            max-height: 400px;
            background-color: #ff8383;
        }
    </style>
</head>

<body>

    <div>
        我是一个盒子
    </div>
</body>

</html>
```
<a name="gDXn9"></a>
##### 14.8.5关于默认宽度
所谓的默认宽度，就是不设置width属性时，元素所呈现出来的宽度。<br />**总宽度**=父的content-自身左右的margin<br />**内容区的宽度**=父的content-自身左右的margin-自身左右的border-自身左右的padding
<a name="SVOsi"></a>
##### 14.8.6盒子的内边距
![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1678892648751-5c6d32b5-a5f1-457e-9ca3-eaa59ce9b8b2.png#averageHue=%23f7f7f6&clientId=u2f1c48df-5935-4&from=paste&height=526&id=uaea9dd4e&name=image.png&originHeight=723&originWidth=967&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=242801&status=done&style=none&taskId=u0a6f607f-54a2-4b5f-a88d-36b3bf62b5f&title=&width=703.2727272727273)
<a name="h3mmN"></a>
##### 14.8.7盒子的边框
![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1678893229207-3b83f1f6-62e1-4106-b8bd-e8990441ade1.png#averageHue=%23fbfbfa&clientId=u2f1c48df-5935-4&from=paste&height=429&id=u8d69add5&name=image.png&originHeight=472&originWidth=932&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=140030&status=done&style=none&taskId=udb13c3b0-fe94-4410-a3ea-52ed2f2eb5f&title=&width=847.2727089085859)<br />![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1678893197054-3f9bbbf2-3bdd-4cde-96f5-4c902ba3ec42.png#averageHue=%23f8f7f7&clientId=u2f1c48df-5935-4&from=paste&height=688&id=uc4d38271&name=image.png&originHeight=757&originWidth=1091&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=178824&status=done&style=none&taskId=u2887cbb2-5213-4c8d-99c8-e36392d2bc8&title=&width=991.8181603211021)<br />![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1678893249153-63f7b678-6bfb-4b6c-a884-3c4ea7823cb4.png#averageHue=%23f0f5f0&clientId=u2f1c48df-5935-4&from=paste&height=93&id=ucddd3794&name=image.png&originHeight=102&originWidth=811&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=35722&status=done&style=none&taskId=u0b1e248f-f605-4bae-99b1-3df94620eac&title=&width=737.2727112927716)
<a name="qWmVp"></a>
##### 14.8.8盒子的外边框
注意事项

- 子元素的margin是参照父元素的content计算的
- 上margin、左margin会影响自身的位置，下margin、右margin会影响兄弟元素的位置
- 对于块级元素左右margin设置auto可以使该元素在父元素内水平居中
- margin可以设置负值

![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1678950059439-9aeb1a1f-ebba-4403-806d-f27af6d74b06.png#averageHue=%23e9e2d7&clientId=u2f1c48df-5935-4&from=paste&height=559&id=u70b0cc2b&name=image.png&originHeight=768&originWidth=1225&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=365691&status=done&style=none&taskId=u95f2571c-bb8a-4c40-9d93-25e08245aa7&title=&width=890.9090909090909)
<a name="AUXRm"></a>
##### 14.8.9margin塌陷问题
![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1678950726516-16faba8f-ad87-44d2-8559-d9174f8791c9.png#averageHue=%23f7f7f7&clientId=u2f1c48df-5935-4&from=paste&height=273&id=u9878f2cc&name=image.png&originHeight=376&originWidth=971&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=121503&status=done&style=none&taskId=u545c7b3c-7a48-4700-a428-c8ea8fe0c27&title=&width=706.1818181818181)<br />为什么会出现这种问题：

- 历史遗留
<a name="GMGl3"></a>
##### 14.8.10maring合并问题
什么是margin的合并？

- 上面兄弟元素的下外边距和下面兄弟的上外边距会合并，取一个最大的值，而不是相加

如何解决margin合并？

- 无需解决，布局的时候上下的兄弟元素，只有一个设置上下外边距就可以了
<a name="iqiQg"></a>
##### 14.8.11处理内容溢出
![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1678964425147-a7ecdc08-ab08-41a9-9b82-64cebd511ea9.png#averageHue=%23e5dbce&clientId=u2f1c48df-5935-4&from=paste&height=436&id=u0ad75268&name=image.png&originHeight=600&originWidth=1079&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=227959&status=done&style=none&taskId=u77409d16-c571-4794-a163-c42d3b892b6&title=&width=784.7272727272727)
```html
<!DOCTYPE html>
<html lang="zh-CN">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
        /* 
        overflow:visible(默认)|hidden(隐藏)|scroll(添加滚动条，无论有没有溢出)|auto(自动，超出添加滚动条)
        overflow-x:单独控制横向(不建议)
        overflow-y:单独控制纵向(不建议)
        */
        #div1 {
            height: 400px;
            width: 400px;
            background-color: gray;
            overflow: scroll;
        }

        #div2 {
            /* height: 400px; */
            width: 1000px;
            background-color: rgb(235, 162, 162);
        }
    </style>
</head>

<body>
    <div id="div1">Lorem ipsum dolor sit amet consectetur adipisicing elit. Reprehenderit consequuntur voluptatem natus
        distinctio
        eum magni vel omnis reiciendis. Quo rerum quam animi nihil! Architecto tempora corporis quos enim saepe cum?
        Similique consequatur voluptatibus, fugit laudantium nobis totam facere quasi fuga quo sed, voluptas accusamus.
        Neque beatae sint nemo dolorem dignissimos rerum nulla dicta, voluptatibus quo quod officia voluptate, ratione
        fugit.
        <div id="div2">Dignissimos, voluptas quasi explicabo quod qui fugit culpa labore in, officiis iure dolorum
            doloribus magni
            deleniti aliquam repudiandae quibusdam vitae ut aliquid numquam velit itaque ea quia suscipit tempora!
            Commodi!
            Reiciendis similique quibusdam ab facere veniam, rerum quas neque perferendis fuga sequi blanditiis
            consequuntur
            corrupti beatae quod natus provident distinctio nulla culpa! Error explicabo culpa consequuntur repellat
            similique cum voluptate?</div>
        Placeat reiciendis maiores magni nulla vel, aspernatur fuga voluptates quisquam architecto, odio quaerat,
        veritatis quas soluta facilis blanditiis qui nam magnam consectetur est deserunt. Rerum eos at aut fugit illo.
        Eligendi perspiciatis harum animi dolor, aperiam voluptatum aut et dolore officia porro error expedita ipsum rem
        autem maiores nesciunt deserunt nam voluptate unde, ut facilis quibusdam? Nisi repellendus ipsa iste?
        Possimus expedita, labore tempora sed ipsum, laudantium ullam laboriosam nostrum vel itaque odio aliquam
        aspernatur quod, deserunt optio laborum quisquam dolorem omnis at eos distinctio quidem odit recusandae
        voluptate? Consequatur?
        Illum dolores praesentium aliquam alias eaque cumque debitis, dolorum atque nobis itaque, voluptates repellat
        obcaecati ratione eum officia quo repellendus fuga autem consequuntur tenetur esse officiis nam, est eligendi!
        Architecto?
        Recusandae expedita aliquam labore error, animi earum libero voluptates, perferendis qui, ducimus quibusdam
        fugit vel laborum laudantium. Repellat possimus dolor quis blanditiis sequi, ipsam praesentium ut odit eius! Ab,
        porro.
        Commodi pariatur nostrum, recusandae a porro ea aliquam quae eum. At autem cum excepturi enim magni? Dicta,
        quaerat repudiandae nihil qui necessitatibus debitis quam quidem amet. Quo corporis exercitationem facilis.
    </div>

</body>

</html>
```
<a name="THSC5"></a>
#### 14.9隐藏元素的两种方式
![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1678964531995-abb6a456-d7ec-4cd5-a43f-3bcb5761e89a.png#averageHue=%23f6f6f5&clientId=u2f1c48df-5935-4&from=paste&height=332&id=u701af419&name=image.png&originHeight=457&originWidth=857&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=146017&status=done&style=none&taskId=uc077ed00-21b1-4814-85eb-c161f17e66e&title=&width=623.2727272727273)
<a name="P6Ka7"></a>
#### 14.10样式的继承
![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1678964971761-78c31e3c-35e3-46cc-b2ef-82d66c7b1581.png#averageHue=%23fafafa&clientId=u2f1c48df-5935-4&from=paste&height=327&id=ua05a9e60&name=image.png&originHeight=449&originWidth=1058&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=158202&status=done&style=none&taskId=u082eb593-0d5f-48a5-84e9-8648cf4d0f1&title=&width=769.4545454545455)
<a name="tCJ2d"></a>
#### 14.11元素的默认样式
![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1678965561369-8af15473-4b03-440f-88dc-04a1da908f6e.png#averageHue=%23fdfcfc&clientId=u2f1c48df-5935-4&from=paste&height=308&id=u450a3bf4&name=image.png&originHeight=423&originWidth=1020&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=163607&status=done&style=none&taskId=u0fd2be73-4816-4069-8dda-a192c685832&title=&width=741.8181818181819)
<a name="aGNI8"></a>
#### 14.12布局小技巧
![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1678966332772-af92c92a-582c-484a-9727-3b157afaea1e.png#averageHue=%23968b78&clientId=u2f1c48df-5935-4&from=paste&height=372&id=u1fa71465&name=image.png&originHeight=511&originWidth=521&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=2722&status=done&style=none&taskId=uebcd041b-4612-4cbe-8320-c7803043978&title=&width=378.90909090909093)
```html
<!DOCTYPE html>
<html lang="zh-CN">


<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
        /* 
            布局技巧1
        */
        .outer {
            width: 400px;
            height: 400px;
            background-color: gray;
            overflow: hidden;
        }


        .inner {
            margin: 150px auto;
            height: 100px;
            width: 200px;
            background-color: orange;
            line-height: 100px;
            text-align: center;
        }
    </style>
</head>


<body>
    <div class="outer">
        <div class="inner">
            inner
        </div>
    </div>


</body>


</html>
```

![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1678966698549-01b58b17-0396-4112-b254-ac931e727504.png#averageHue=%238a8886&clientId=u2f1c48df-5935-4&from=paste&height=378&id=u626883f5&name=image.png&originHeight=520&originWidth=517&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=3779&status=done&style=none&taskId=u6d37c867-12e8-4987-92a6-e703d56d2e0&title=&width=376)
```html
<!DOCTYPE html>
<html lang="zh-CN">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
        /* 
            布局技巧2
        */
        .outer {
            width: 400px;
            height: 400px;
            background-color: gray;
            overflow: hidden;
            line-height: 400px;
            text-align: center;
        }

        .inner {
            font-size: 32px;
            background-color: orange;
        }
    </style>
</head>

<body>
    <div class="outer">
        <span class="inner">
            inner
        </span>
    </div>

</body>

</html>
```
![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1678967578104-01740210-c04f-4127-8053-dbb8f881bfb4.png#averageHue=%239a9894&clientId=u2f1c48df-5935-4&from=paste&height=383&id=u3014082b&name=image.png&originHeight=527&originWidth=582&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=47224&status=done&style=none&taskId=u27dc0a22-d2c9-4638-b3a9-152d66e541e&title=&width=423.27272727272725)
```html
<!DOCTYPE html>
<html lang="zh-CN">


<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
        /* 
            布局技巧3
        */
        .outer {
            width: 400px;
            height: 400px;
            background-color: gray;
            overflow: hidden;
            line-height: 400px;
            text-align: center;
            font-size:0;
        }


        .inner {
            font-size: 32px;
            background-color: orange;
            vertical-align: middle;
        }


        img {
            width: 100px;
            height: 100px;
            vertical-align: middle;
        }
    </style>
</head>


<body>
    <div class="outer">
        <span class="inner">
            innerx
            <img src="./R.png" alt="">
        </span>


    </div>


</body>


</html>
```
![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1678967802784-0ba6eaea-e21c-4cb9-96c8-1aaabd98b405.png#averageHue=%23f9f8f7&clientId=u2f1c48df-5935-4&from=paste&height=572&id=u9ebe81e5&name=image.png&originHeight=786&originWidth=1385&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=495564&status=done&style=none&taskId=u7f85e4b5-a7bb-4d2f-8a00-6003b26918a&title=&width=1007.2727272727273)
<a name="A0Koz"></a>
#### 14.13元素间空白问题
![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1678968442243-6409a198-803c-4b9b-8363-943009300812.png#averageHue=%23f8f8f8&clientId=u2f1c48df-5935-4&from=paste&height=254&id=uba109826&name=image.png&originHeight=349&originWidth=1020&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=114532&status=done&style=none&taskId=u61d6d2c9-5a20-4480-8eb3-5e3e1695e23&title=&width=741.8181818181819)<br />![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1678968425880-a88735c8-3b18-4f52-b12d-4fdd2eed0a81.png#averageHue=%23848381&clientId=u2f1c48df-5935-4&from=paste&height=461&id=u827bb428&name=image.png&originHeight=634&originWidth=1273&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=55158&status=done&style=none&taskId=u340769b8-3182-4dbe-826e-e5a79ef9d18&title=&width=925.8181818181819)
```html
<!DOCTYPE html>
<html lang="zh-CN">


<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
        div {
            height: 500px;
            background-color: gray;
            font-size: 0;
        }


        span {
            font-size: 20px;
        }


        .s1 {
            background-color: skyblue;
        }


        .s2 {
            background-color: orange;
        }


        .s3 {
            background-color: purple;
        }


        img {
            width: 100px;
            height: 100px;
        }
    </style>
</head>


<body>
    <div>
        <span class="s1">性本善</span>
        <span class="s2">性相近</span>
        <span class="s3">人之初</span>
        <hr>
        <img src="./R.png" alt="">
        <img src="./R.png" alt="">
        <img src="./R.png" alt="">
    </div>
</body>
</html>
```
<a name="ft1iy"></a>
#### 14.14幽灵空白
![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1678969133945-9b55a5f5-0116-47db-b14a-af068144fe5b.png#averageHue=%23989490&clientId=u2f1c48df-5935-4&from=paste&height=219&id=u095a67c5&name=image.png&originHeight=301&originWidth=916&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=139496&status=done&style=none&taskId=u56093b3f-fd8a-4de0-93e4-d2c17d2bf1a&title=&width=666.1818181818181)
```html
<!DOCTYPE html>
<html lang="zh-CN">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
        /* 解决幽灵空白 */
        div {
            width: 600px;
            background-color: gray;
            /* 解决方法3 */
            font-size: 0;
        }

        img {
            height: 100px;
            /* 解决方法1 */
            vertical-align: top;
            /* 解决方法2,旁边没有其他元素时 */
            /* display:block; */
        }
    </style>
</head>

<body>
    <div>
        <img src="./R.png" alt="">xg
    </div>
</body>

</html>
```
<a name="v40eb"></a>
#### 14.15浮动
<a name="r2Yvz"></a>
##### 14.15.1浮动_简介
![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1678973014227-78a441c9-6179-48e8-a1fd-da90a4915139.png#averageHue=%23a3aaa2&clientId=u2f1c48df-5935-4&from=paste&height=407&id=uab9f68d0&name=image.png&originHeight=559&originWidth=907&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=437819&status=done&style=none&taskId=u424faa67-a455-4254-a387-dfb2208a91b&title=&width=659.6363636363636)
<a name="KEkNO"></a>
##### 14.15.2元素浮动后的特点
![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1678973618196-1636b52b-5398-4168-b664-4e1c6b9f1430.png#averageHue=%23f8f8f7&clientId=u2f1c48df-5935-4&from=paste&height=241&id=u051cef71&name=image.png&originHeight=331&originWidth=997&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=133314&status=done&style=none&taskId=ua58344fb-d355-4d37-bfd4-62fe399cfea&title=&width=725.0909090909091)
<a name="MELgN"></a>
##### 14.15.3浮动小练习
![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1678975081435-d2e67058-4c61-4386-afc2-df2ea4d5b811.png#averageHue=%23f7f7f7&clientId=u2f1c48df-5935-4&from=paste&height=514&id=u21f8287a&name=image.png&originHeight=707&originWidth=616&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=68431&status=done&style=none&taskId=ue3c82e51-63d2-4731-afbc-4c4a69708fd&title=&width=448)<br />![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1678975111030-be141a41-206e-44e4-b76f-97c1175cfb34.png#averageHue=%23fdfdfa&clientId=u2f1c48df-5935-4&from=paste&height=347&id=u7e4aacac&name=image.png&originHeight=477&originWidth=598&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=41932&status=done&style=none&taskId=uf07fb954-4575-4fc2-b10c-810ee9974fe&title=&width=434.90909090909093)
<a name="lJ8v2"></a>
##### 14.15.4浮动的影响
![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1678979625540-832e81f6-d7b7-4af9-9bc0-b7f5345b7f17.png#averageHue=%23f6f5f5&clientId=u2f1c48df-5935-4&from=paste&height=151&id=u91522233&name=image.png&originHeight=208&originWidth=1113&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=103238&status=done&style=none&taskId=u84b5b855-db8e-4c9a-943a-5568a70979d&title=&width=809.4545454545455)
<a name="BBYkH"></a>
##### 14.15.5解决浮动的影响
![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1678980758018-d02d5201-0e98-43d8-90f6-4345cd8a3a27.png#averageHue=%23f5f5f5&clientId=u2f1c48df-5935-4&from=paste&height=422&id=uef3d2bc6&name=image.png&originHeight=580&originWidth=1166&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=205866&status=done&style=none&taskId=ub6607210-9f8b-4481-babd-c26041615a8&title=&width=848)
<a name="QiTMB"></a>
##### 14.15.6浮动练习
![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1678981619326-439a3f77-e6ac-4bf9-b905-5f4453683a36.png#averageHue=%23eeeeee&clientId=u2f1c48df-5935-4&from=paste&height=582&id=ubb7a44b8&name=image.png&originHeight=800&originWidth=1287&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=60791&status=done&style=none&taskId=ueb659d91-61d4-4455-92fc-54594756c2e&title=&width=936)<br />![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1679017405127-c6cf95ef-02f4-4f59-961f-a7c44c876331.png#averageHue=%2381c294&clientId=u0c197160-2058-4&from=paste&height=561&id=u5d717006&name=image.png&originHeight=772&originWidth=1250&originalType=binary&ratio=1.25&rotation=0&showTitle=false&size=12522&status=done&style=none&taskId=ua94495ec-267d-41f0-bac3-f26c938cd6d&title=&width=909.0909090909091)
```html
<!DOCTYPE html>
<html lang="zh-CN">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
        * {
            box-sizing: border-box;
        }

        body {
            text-align: center;
        }

        .root {
            width: 960px;
            height: 610px;
            margin: 0 auto;
        }

        .title {
            width: 100%;
            height: 80px;
            line-height: 80px;

        }

        .title div {
            float: left;
        }

        .title::after {
            content: '';
            clear: both;
            display: block;
        }

        .logo {
            height: 100%;
            width: 200px;
            background-color: gray;
        }

        .banner2 {
            height: 100%;
            width: 200px;
            background-color: gray;
        }

        .banner1 {
            height: 100%;
            width: 540px;
            margin: 0 10px;
            background-color: gray;
        }

        .nav {
            width: 100%;
            height: 30px;
            line-height: 30px;
            margin-top: 10px;
            background-color: gray;
        }

        .body {
            line-height: 80px;
            margin-top: 10px;
        }

        .border {
            border: 1px solid #000;
        }

        .body::after {
            content: '';
            clear: both;
            display: block;
        }

        .left {
            margin-right: 10px;
            width: 370px;
            float: left;
        }

        .right {
            float: right;
        }

        .left-top {
            height: 200px;
        }

        .left-top-content {
            float: left;
            width: 370px;
            height: 200px;
            background-color: skyblue;
        }

        .left-top-content:first-of-type {
            margin-right: 10px;
        }

        .left-bottom {
            margin-top: 10px;
            width: 100%;
            height: 210px;
        }

        .left-bottom-content1,
        .left-bottom-content2 {

            width: 180px;
            height: 200px;
            background-color: skyblue;
        }

        .left-bottom-content1 {
            float: left;
        }

        .left-bottom-content2 {
            float: right;
        }

        .right-content {
            width: 200px;
            height: 130px;
            background-color: skyblue;
            margin-bottom: 10px;
        }

        footer {
            line-height: 80px;
            width: 100%;
            height: 80px;
            background-color: gray;
        }
    </style>
</head>

<body>
    <div class="root">
        <div class="title">
            <div class="logo">logo</div>
            <div class="banner1">banner1</div>
            <div class="banner2">banner2</div>
        </div>
        <div class="nav">菜单</div>
        <div class="body">

            <div class="left">
                <div class="left-top">
                    <div class="border left-top-content">栏目1</div>
                </div>
                <div class="left-bottom">
                    <div class="border left-bottom-content1">栏目</div>
                    <div class="border left-bottom-content2">栏目</div>
                </div>
            </div>
            <div class="left">
                <div class="left-top">
                    <div class="border left-top-content">栏目1</div>
                </div>
                <div class="left-bottom">
                    <div class="border left-bottom-content1">栏目</div>
                    <div class="border left-bottom-content2">栏目</div>
                </div>
            </div>
            <div class="right">
                <div class="border right-content">栏目</div>
                <div class="border right-content">栏目</div>
                <div class="border right-content">栏目</div>
            </div>
        </div>
        <footer>
            页脚
        </footer>
    </div>

</body>

</html>
```
<a name="wrKwL"></a>
#### 14.16相对定位
如果一个元素开启了定位，那么它的层级就比普通元素要，如果都开启了定位，那么按照后来居上原则。
```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
        /* 	position:relative 相对定位（相对于自己原本的位置，保留原本位置，没有脱离文档流）
            top/left/right/bottom
            left和right不能一起设置，top和bottom不能一起设置
      		使用场景：
      			--一般用于对元素位置进行微调，对其他元素没有影响
            --绝大多数条件下，相对定位会与绝对定位一起使用
            --相对定位不推荐和浮动一起使用
      */
        .outer {
            width: 500px;
            background-color: skyblue;
            padding: 20px;
        }
        .box {
            width: 200px;
            height: 200px;
        }
        .d1 {
            background-color: #888;
            position: relative;
            top: -20px;
        }
        .d2 {
            background-color: orange;
            position: relative;
            left: -20px;
        }
        .d3 {
            position: relative;
            bottom: 20px;
            background-color: green;
        }
    </style>
</head>
<body>
    <div class="outer">
        <div class="box d1">1</div>
        <div class="box d2">2</div>
        <div class="box d3">3</div>
    </div>
</body>
</html>
```
<a name="CN99R"></a>
#### 14.17绝对定位
定位元素：

1. 宽高默认被内容撑开
2. 宽高可以调整
3. 相对定位元素没有上述两特点
```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
        /*  position:absolute
            top|left|right|bottom
            --用了top、left，才能使用margin-top、margin-left，不推荐给绝对定位元素加上margin
      			--绝对定位不能和浮动一起写，绝对定位覆盖浮动
      			--无论什么元素(行内、行内快、块)设置绝对定位之后，都变成定位元素·
            --开启绝对定位会脱离文档流，不保留原位置，参考包含块
            包含块：
                1.没有脱离文档流的元素，父元素为包含块
                2.脱离文档流的元素，第一个开启定位的祖先元素
            使用：子绝父相
            	--用于一个元素盖在另一个元素身上
        */
        .outer {
            width: 500px;
            background-color: skyblue;
            padding: 20px;
            position: relative;
        }
        .box {
            width: 200px;
            height: 200px;
        }
        .d1 {
            background-color: #888;
        }
        .d2 {
            background-color: orange;
            position: absolute;
            top: 0;
        }
        .d3 {
            background-color: green;
        }
    </style>
</head>
<body>
    <div class="outer">
        <div class="box d1">1</div>
        <div class="box d2">2</div>
        <div class="box d3">3</div>
    </div>
</body>
</html>
```
<a name="QvU0G"></a>
#### 14.18固定定位
固定定位元素特点：

1. 脱离文档流，会对后面的兄弟、父元素拥有影响
2. left不能和right一起设置，top和bottom不能一起设置
3. 固定定位和浮动不能一起设置，同时设置以固定定位为主。
4. 固定定位的元素也能通过margin调整，但不推荐这样做
5. 无论什么元素（行内、行内块、块级）设置固定定位后，都变成了定位元素。
```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
        /*  
            固定定位：脱离文档流，相对于视口定位，
            position:fiex;
        */
        .outer {
            margin-top: 50px;
            width: 500px;
            height: 1000px;
            background-color: skyblue;
            padding: 20px;
        }
        .box {
            width: 200px;
            height: 200px;
        }
        .d1 {
            background-color: #888;
        }
        .d2 {
            position: fixed;
            top: 20px;
            left: 20px;
            background-color: orange;
        }
        .d3 {
            background-color: green;
        }
    </style>
</head>
<body>
    <div class="outer">
        <div class="box d1">1</div>
        <div class="box d2">2</div>
        <div class="box d3">3</div>
    </div>
</body>
</html>
```
<a name="bF7jg"></a>
#### 14.19粘性定位
top：参考离他最近的拥有滚动行为的祖先元素（默认body）<br />![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1679042684613-f46937ff-1b17-47da-bc99-bfad19f11bab.png#averageHue=%23fcfbfa&clientId=u0c197160-2058-4&from=paste&height=559&id=uba6be9e3&name=image.png&originHeight=769&originWidth=1272&originalType=binary&ratio=1.25&rotation=0&showTitle=false&size=486507&status=done&style=none&taskId=u990da3b3-2033-4e1f-92ef-8479d2d597e&title=&width=925.0909090909091)
```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
        * {
            margin: 0;
            padding: 0;
        }
        body {
            height: 2000px;
        }
        .header {
            height: 100px;
            background-color: orange;
            text-align: center;
            line-height: 100px;
            font-size: 20px;
        }
        .item {
            text-align: center;
            background-color: #888;
        }
        .first-item {
            /* 粘性定位 */
            position: sticky;
            top: 0;
            font-size: 40px;
            background-color: aqua;
        }
    </style>
</head>
<body>
    <div class="header">头部</div>
    <div class="content">
        <div class="item">
            <div class="first-item">A</div>
            <h2>A1</h2>
            <h2>A2</h2>
            <h2>A3</h2>
            <h2>A4</h2>
            <h2>A5</h2>
            <h2>A6</h2>
            <h2>A7</h2>
            <h2>A8</h2>
            <h2>A9</h2>
        </div>
        <div class="item">
            <div class="first-item">B</div>
            <h2>B1</h2>
            <h2>B2</h2>
            <h2>B3</h2>
            <h2>B4</h2>
            <h2>B5</h2>
            <h2>B6</h2>
            <h2>B7</h2>
            <h2>B8</h2>
            <h2>B9</h2>
        </div>
        <div class="item">
            <div class="first-item">C</div>
            <h2>C1</h2>
            <h2>C2</h2>
            <h2>C3</h2>
            <h2>C4</h2>
            <h2>C5</h2>
            <h2>C6</h2>
            <h2>C7</h2>
            <h2>C8</h2>
            <h2>C9</h2>
        </div>
    </div>
</body>
</html>
```
<a name="Fg0TN"></a>
#### 14.20css定位的层级
![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1679043829720-6dab6352-522b-4f22-bfff-10cb7194c71c.png#averageHue=%23fafafa&clientId=u0c197160-2058-4&from=paste&height=317&id=u707df2d8&name=image.png&originHeight=436&originWidth=1128&originalType=binary&ratio=1.25&rotation=0&showTitle=false&size=248315&status=done&style=none&taskId=udd18e70e-f419-426a-b7ae-78c6574ca1b&title=&width=820.3636363636364)
<a name="XqJRD"></a>
#### 14.21定位的特殊应用
![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1679044831113-2c778cc3-2463-4812-8f5a-702ed4915cc1.png#averageHue=%23f6f5f5&clientId=u0c197160-2058-4&from=paste&height=556&id=u579b8426&name=image.png&originHeight=765&originWidth=1225&originalType=binary&ratio=1.25&rotation=0&showTitle=false&size=300305&status=done&style=none&taskId=u38ca1c8c-c04d-4028-a2f4-8f29f57eafd&title=&width=890.9090909090909)![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1679045071327-57a9b2dd-ae63-4787-8a99-b143b4f49d40.png#averageHue=%23f9f9f9&clientId=u0c197160-2058-4&from=paste&height=209&id=u1f5aa1fa&name=image.png&originHeight=287&originWidth=1135&originalType=binary&ratio=1.25&rotation=0&showTitle=false&size=62397&status=done&style=none&taskId=u834bd0dd-5d83-4b65-8bbf-1ec9512fceb&title=&width=825.4545454545455)
<a name="kdgt7"></a>
### 14.22常用布局单词名
![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1679045873970-c151b92e-a0ff-4b41-abf1-a1e009f7fc94.png#averageHue=%23f8f8f7&clientId=u0c197160-2058-4&from=paste&height=391&id=u5914e078&name=image.png&originHeight=538&originWidth=1042&originalType=binary&ratio=1.25&rotation=0&showTitle=false&size=129017&status=done&style=none&taskId=u4eb73a7b-4aba-44e7-b6c0-78093404079&title=&width=757.8181818181819)
<a name="nK0Oe"></a>
### 14.23默认样式
![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1679046181774-6812f0c4-c568-46aa-a7ce-89b89d6d2535.png#averageHue=%23fcfcfc&clientId=u0c197160-2058-4&from=paste&height=639&id=u21220323&name=image.png&originHeight=878&originWidth=1267&originalType=binary&ratio=1.25&rotation=0&showTitle=false&size=305421&status=done&style=none&taskId=u2e3a0b7b-e14f-43a5-a7ae-aff98bc35a1&title=&width=921.4545454545455)<br />![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1679046436259-35efeff2-132f-4300-b978-8d5671ff8588.png#averageHue=%23fcfcfc&clientId=u0c197160-2058-4&from=paste&height=370&id=u7c503a82&name=image.png&originHeight=509&originWidth=1245&originalType=binary&ratio=1.25&rotation=0&showTitle=false&size=218100&status=done&style=none&taskId=ub8e53d6d-4aec-48a2-b3e2-eb233d5b2cc&title=&width=905.4545454545455)<br />![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1679046483332-ed112e67-c3c5-4379-8523-612989a558d0.png#averageHue=%23fdfcfc&clientId=u0c197160-2058-4&from=paste&height=193&id=udb423f99&name=image.png&originHeight=266&originWidth=1336&originalType=binary&ratio=1.25&rotation=0&showTitle=false&size=122867&status=done&style=none&taskId=ud685e567-4e04-4230-a922-762709ae0c0&title=&width=971.6363636363636)
