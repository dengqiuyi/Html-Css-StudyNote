<a name="gJvpu"></a>
## 1.基础知识
<a name="Ide3o"></a>
### 1.1两位先驱
1）艾伦·麦序森·图灵：人工智能之父<br />2）约翰·冯·诺依曼：现代计算机之父
<a name="bceAF"></a>
### 1.2计算机基础
1）![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1678585234215-a2881116-a688-4d86-9bea-4d093e49673a.png#averageHue=%23444443&clientId=u3b45df95-5f9a-4&from=paste&height=657&id=u5cf0508b&name=image.png&originHeight=903&originWidth=1721&originalType=binary&ratio=1&rotation=0&showTitle=false&size=555464&status=done&style=none&taskId=u36fd4fc8-02e7-4d85-ad13-5525d856847&title=&width=1251.6363636363637)
<a name="tQpDp"></a>
### 1.3BS架构和CS架构
<a name="KwW0V"></a>
#### 1.3.1CS软件：先安装再去使用的软件
a.需要安装<br />b.不跨平台<br />c.偶尔更新<br />大型专业应用、安全要求较高的应用，还要采用C/S架构<br />![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1678585532111-c23b8c31-21a6-4606-b566-ac50ca434098.png#averageHue=%23524b4a&clientId=u3b45df95-5f9a-4&from=paste&height=119&id=u6cbf304c&name=image.png&originHeight=163&originWidth=413&originalType=binary&ratio=1&rotation=0&showTitle=false&size=69567&status=done&style=none&taskId=ucd469a6a-9813-42a2-8741-0217bbbae34&title=&width=300.3636363636364)
<a name="DbU8o"></a>
#### 1.3.2BS软件：直接在浏览器打开的软件（主）
a.无需安装<br />b.无需下载
<a name="VZnwU"></a>
#### 1.3.3大前端时代我们可以做什么
![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1678585730460-2b112344-9dfc-4c9b-81c0-e2aec51994a2.png#averageHue=%23333332&clientId=u3b45df95-5f9a-4&from=paste&height=175&id=udca8bc68&name=image.png&originHeight=241&originWidth=1831&originalType=binary&ratio=1&rotation=0&showTitle=false&size=176002&status=done&style=none&taskId=u33ed138b-ba6a-467b-994f-7a86de63ca4&title=&width=1331.6363636363637)
<a name="CjLwZ"></a>
### 1.4浏览器相关知识
<a name="z7hDE"></a>
#### 1.4.1主流浏览器
a.chrome、ie、firfox、safari、Opera
<a name="GRxRI"></a>
#### 1.4.2浏览器内核
1)内核是浏览器的核心，用于处理浏览器所得到的各种资源<br />2)主流浏览器所用的内核<br />Chrome：早期webkit内核，现在使用Blink内核<br />Safari：webkit内核<br />IE：Trident内核<br />Firefox：Gecko内核<br />Opera：早期使用Presto内核（已经放弃维护），现使用Blink内核<br />其他浏览器：在上述内核的基础上，加上一些精美的ui、实用的小功能
<a name="BUgTm"></a>
### 1.5网页相关知识
网页由结构、表现和行为组成<br />即html、css和javascript
<a name="JeIlY"></a>
## 2.HTML4
<a name="sW2U2"></a>
### 2.1html是什么？
全称：HyperType Markup Languang<br />翻译为：标记语言<br />超文本：暂且理解为“超级文本”，和普通文本相比，内容更加丰富<br />标记：文本想要变成超文本，需要借助各种标记符号<br />语言：每一个标记的写法。读音、使用规则
<a name="FWUGL"></a>
### 2.2互联网发展史
IETF：Internet Engineering Task Force(国际互联网工程任务组，成立于1985年)<br />W3C：World Wide Web Consortium(万维网联盟，成立于1994年)<br />![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1678587496508-14f8e4ec-4c34-4ede-8640-8b8b46c19896.png#averageHue=%23474544&clientId=u3b45df95-5f9a-4&from=paste&height=643&id=ua3ac8488&name=image.png&originHeight=884&originWidth=1883&originalType=binary&ratio=1&rotation=0&showTitle=false&size=702461&status=done&style=none&taskId=u87f3ac48-db6c-4411-b6c6-eef730330d6&title=&width=1369.4545454545455)
<a name="RTDOO"></a>
### 2.3html初体验
<a name="O45iV"></a>
#### 2.3.1html注释
```html
<html>
  <head>
    <title></title>
  </head>
  <body>
    <marquee loop="1">hhhh!</marquee>
    <!-- 我是注释,注释不允许嵌套，快速注释ctrl+/-->
    <input type="text"/>
  </body>
</html>
```
<a name="oIZ01"></a>
#### 2.3.2文档声明
```html
<!--大多数浏览器默认声明h5，少部分没有声明-->
<!--h5声明，写在html标签外面-->
<!DOCTYPE html>
<html>
  <head>
    <title></title>
  </head>
  <body>
  </body>
</html>
```
<a name="K2wX8"></a>
#### 2.3.3字符编码
ASCII=>大写字母、小写字母、数字、一些符号，共128<br />GB2312=>继续扩充，收录了6763个常用汉字。682个字符<br />GBK=>收录了20000+汉字，支持繁体中文<br />UTF-8=>收录了万国的语言与符号，万国码
```html
<!DOCTYPE html>
<html>
  <head>
    <!--告诉它用什么编码-->
    <meta charset="utf-8">
    <title></title>
  </head>
  <body>
  </body>
</html>
```
<a name="CfW9Y"></a>
#### 2.3.4设置网页语言
<a name="zDEk3"></a>
##### 2.3.4.1shift+刷新：强制刷新
![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1678590001959-6b21f049-c916-431d-be1f-10355b7c4544.png#averageHue=%23ecf4f0&clientId=u3b45df95-5f9a-4&from=paste&height=273&id=u2439f1bd&name=image.png&originHeight=375&originWidth=1192&originalType=binary&ratio=1&rotation=0&showTitle=false&size=191553&status=done&style=none&taskId=u644b1d32-a25b-46a0-a291-adcd3fce704&title=&width=866.9090909090909)
```html
<!DOCTYPE html>
<!--设置网页语言-->
<html lang="zh-CN">
  <head>
    <meta charset="utf-8">
    <title>设置语言</title>
  </head>
  <body>
    <marquee>520</marquee>
  </body>
</html>
```
<a name="jXTJ7"></a>
#### 2.3.5html标准结构
<a name="wWoxY"></a>
##### 2.3.5.1快速删除多行ctrl+shift+k
```html
<!DOCTYPE html>
<html lang="zh-CN">
<!--网页标签图片以.ico结尾，放在html上一目录下可直接显示在网页上-->
<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>
<body>

</body>
</html>
```
<a name="Gtu9K"></a>
### 2.4html排版标签
```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8">
    <title></title>
  </head>
	<body>
  	<h1>我是一级标题</h1>
    <h2>我是二级标题</h2>
    <h3>我是三级标题</h3>
    <h4>我是四级标题</h4>
    <p>我是一个段落</p>
    <!--p标签里不能有h1标签，p标签等-->
  </body>
</html>
```
<a name="ER4fc"></a>
### 2.5html语义化标签
1.代码的可读性强<br />2.有利于爬虫检索<br />3.方便盲人阅读器、屏幕阅读器
<a name="Wevpy"></a>
### 2.6块级元素和行内元素
shift+alt+上/下快速复制一行<br />1.块级元素：<br />--独占一行<br />--块内元素内块内元素和行内元素都能写<br />2.行内元素：<br />--不独占一行<br />--行内元素内只能有行内元素<br />3.特殊规则<br />--h1、h6不能互相嵌套<br />--p标签中不能写块元素<br />--marquee几乎不被使用了，废除了
<a name="F5u51"></a>
### 2.7常用的文本标签
```html
<!DOCTYPE html>
<html lang="zh-CN">
  <head>
    <meta charset="UTF-8">
    <title></title>
  </head>
	<body>
    <!--em:着重阅读的标签，斜体-->
  	<em>着重阅读的标签</em>
    <!--strong：十分重要的内容，语气比em更强-->
    <string>我是重要内容</string>
    <!--span：没有语义，用于包裹文字-->
    <span>hhhhh</span>
  </body>
</html>
```
<a name="B7BVa"></a>
### 2.8不常用的文本标签
```html
<!DOCTYPE html>
<html lang="zh-CN">
  <head>
    <meta charset="UTF-8">
    <title></title>
  </head>
	<body>
    <!--cide:作品如音乐、书籍的标题-->
  	<cide>音乐、书籍的标题</cide>
    <!--dfn：特殊术语，或专属名词-->
    <dfn>特殊术语</dfn>
    <!--del、ins：删除、插入的文本-->
    <del>hhhhh</del>
    <ins>hhhhh</ins>
    <!--sub、sup：下标文字和上标文字-->
    <!--code：一段代码-->
    <!--smap：设备输出如"标识设备输出"-->
    <!--kdb：按下键盘-->
    <!--abbr：缩写，加上title属性，标识缩写含义-->
    <!--i：字体图标-->
    <!--adress：地址信息-->
  </body>
</html>
```
<a name="GVFZ8"></a>
### 2.9图片标签
1.img元素是行内块元素
```html
<!DOCTYPE html>
<html lang="zh-CN">
  <head>
    <meta charset="UTF-8">
    <title></title>
  </head>
	<body>
    <!--src:图片路径、alt：图片说明-->
    <img src="./奥特曼.jpg">
  </body>
</html>
```
2.常见图片格式<br /> jpg：不支持透明背景、动态图，适用于对图片细节没有极高要求的场景、空间较小<br />png：支持透明背景、不支持动态图，只用于想要有图片背景，想呈现高质量的图片如：公司logo、重要配图等。<br />bmp：不支持透明背景、不支持动态图、色彩多、保留细节多，用于对图片要求极高的场景如：一些大型游戏需要，一般不用在网页中<br />jif：支持颜色较小、支持简单图片透明，支持动图<br />webp：具备上述几种的优点，但不太兼容，专门用于呈现网页中的图片，一旦使用务必解决兼容性问题<br />base64：把图片进行base64编码，形成一串文字，传统看图软件无法查看，不需要发请求照图片
<a name="djYIn"></a>
### 2.10超链接
<a name="jRPtD"></a>
#### 2.10.1跳转页面
```html
<!DOCTYPE html>
<html lang="zh-CN">
  <head>
    <meta charset="UTF-8">
    <title></title>
  </head>
	<body>
    <!--a标签可以包裹任何除它本身的标签-->
    <!--只有第一个空格或空行被解析成空格-->
    <!--当前页面打开，默认-->
    <a href="https://miaosa.jd.com" target="_self">去秒杀</a>
		<!--新标签页面打开-->
    <a href="https://miaosa.jd.com" target="_blank">去秒杀</a>
  </body>
</html>
```
<a name="n8nPD"></a>
#### 2.10.2跳转文件
```html
<!DOCTYPE html>
<html lang="zh-CN">
  <head>
    <meta charset="UTF-8">
    <title></title>
  </head>
	<body>
    <!--浏览器可以直接打开的文件点击跳转会直接播放-->
    <!--浏览器不可以直接打开的文件点击跳转会触发下载-->
    <!--浏览器可以直接打开的文件，给a标签添加download属性点进去可以触发下载-->
    <a href="./01.jpg" download>去下载图片</a>
  </body>
</html>
```
<a name="WYtlj"></a>
#### 2.10.3跳转锚点
```html
<!DOCTYPE html>
<html lang="zh-CN">

<head>
    <meta charset="UTF-8">
    <title></title>
    <style>
        p {
            font-size: 30px;
            display: inline-block;
            height: 25px;
        }
    </style>
</head>
<!--href属性前面加#说明是要跳转锚点，可以跳转到其他a标签name和href一样的位置，
  或者在其他标签添加id属性也一样-->
<body>
    <p><a name="one">第一段</a><br /><br /><br />我们是死者。我们思之为生活的东西，只是真正生活的睡眠，实际上是我们的死亡。<br /><br /><br />
        死就是新生，死者并不死。当我们以为自己活着的时候，我们已经死了。而我们死了的时候却活着。<br /><br /><br />
        存在于睡眠和生活之间的关系，同样是我们称之为生活以及死亡间的关系。我们睡着了，生活便是一个梦，这不是隐喻的诗歌的说法，生活的确是梦。<br /><br /><br />
        我们在碌碌无为的生活中视为重要的一切，都参与死亡，都是死亡。<br /><br /><br />
        理想——生活远远够不到；艺术——对生活的否定；雕塑——僵死的尸体，雕刻家不过是一心想把死亡凝固为不可腐烂的物体。愉快，这种似乎是使我们沉浸于生活的东西，我们沉寂其中的东西，是我们与生活间的隔阂，布满死亡的阴影。<br /><br />
        每一个我们享乐其中的新日子，都是我们生命失去的另一个日子。<br /><br /><br />
        人只是梦，是一些流浪的幻影穿越虚幻的森林，而这些树是我们的房子，居所，观念，理想以及哲学。<br /><br /><br />
        我从来没有找到过上帝，也不知上帝为何物！从一个世界到另一个世界，同样的幻想总是被同样的错误所宠幸。<br /><br /><br />
        <a href="#one">返回第一段</a><br /><br />从未有过真实和平静！
    </p>
  	<!--回到顶部-->
     <a href="#">回到顶部</a>
  	<!--刷新页面-->
 		 <a href="">刷新页面</a>
  	<!--跳转到其他页面具体位置-->
     <a hred="../xxx.html#atm">跳转到xxx页面id为atm的位置</a>
    <!--js脚本-->
     <a href="javascript:alert(666);">点我弹窗666</a>
</body>
</html>
```
<a name="cIdcm"></a>
#### 2.10.4超链接唤起指定应用
```html
<!DOCTYPE html>
<html lang="zh-CN">
  <head>
    <meta charset="UTF-8">
    <title></title>
  </head>
	<body>
    <!--拨打电话-->
    <a href="tel:123456">电话联系</a>
    <!--发送邮件-->
    <a href="mailto:xxx@qq.com">邮件联系</a>
    <!--发送短信-->
    <a href="sms:10086">短信联系</a>
  </body>
</html>
```
<a name="sCWEz"></a>
### 2.11超文本
“超文本”是一种组织信息的方式，通过超链接将不同空间的文字、图片等各种信息组织在一起，能从当前阅读的内容，跳转到超链接所指方向的内容（页面、文件、锚点、应用）。
<a name="vxxMw"></a>
### 2.12列表
<a name="i1KXG"></a>
#### 2.12.1列表的使用
```html
<!DOCTYPE html>
<html lang="zh-CN">
  <head>
    <meta charset="UTF-8">
    <title></title>
  </head>
	<body>
    <!--有序列表-->
    <h2>将大象放冰箱</h2>
    <ol>
      <li>把冰箱门打开</li>
      <li>将大象放进去</li>
      <li>将冰箱门关上</li>
    </ol>
    <!--无序列表-->
    <h2>我想去的几个城市</h2>
    <ul>
      <li>上海</li>
      <li>西藏</li>
      <li>重庆</li>
    </ul>
    <!--自定义列表-->
    <h2>如何更好的学习</h2>
    <dl>
      <dt>做好笔记</dt>
      <dd>笔记是我们以后复习的帮手</dd>
      <dt>多加联系</dt>
      <dd>只有敲出来的代码，才是自己的</dd>
      <dt>别怕出错</dt>
      <dd>错很正常，改正后并记住，就是经验</dd>
    </dl>
  </body>
</html>
```
2.12.2列表使用的注意事项
```html
<!DOCTYPE html>
<html lang="zh-CN">
  <head>
    <meta charset="UTF-8">
    <title></title>
  </head>
	<body>
    <!--
    列表的注意事项
      1.无论是ol还是ul子元素最好是li
      2.li最好不要单独使用
      3.列表可以嵌套
    	4.自定义列表中，一个dt可以有多个dd
    -->
    <!--有序列表-->
    <h2>将大象放冰箱</h2>
    <ol>
      <li>把冰箱门打开</li>
      <li>将大象放进去</li>
      <li>将冰箱门关上</li>
    </ol>
    <!--无序列表-->
    <h2>我想去的几个城市</h2>
    <ul>
      <li>上海</li>
      <li>西藏</li>
      <li>重庆</li>
    </ul>
    <!--自定义列表-->
    <h2>如何更好的学习</h2>
    <dl>
      <dt>做好笔记</dt>
      <dd>笔记是我们以后复习的帮手</dd>
      <dt>多加联系</dt>
      <dd>只有敲出来的代码，才是自己的</dd>
      <dt>别怕出错</dt>
      <dd>错很正常，改正后并记住，就是经验</dd>
    </dl>
  </body>
</html>
```
<a name="S3bHc"></a>
### 2.13表格
<a name="CE4Ff"></a>
#### 2.13.1表格结构
```html
<!DOCTYPE html>
<html lang="zh-CN">

<head>
    <meta charset="UTF-8">
    <title></title>
</head>

<body>
    <table border="1">
        <caption>标题</caption>
        <thead>
            <th>hhh</th>
            <th>hhh</th>
            <th>hhh</th>
        </thead>
        <tbody>
            <tr>
                <td>1</td>
                <td>2</td>
                <td>3</td>
            </tr>
            <tr>
                <td>1</td>
                <td>2</td>
                <td>3</td>
            </tr>
            <tr>
                <td>1</td>
                <td>2</td>
                <td>3</td>
            </tr>
        </tbody>
        <tfoot>
            <tr>
                <td>foot</td>
                <td>foot</td>
                <td>foot</td>
            </tr>
        </tfoot>
    </table>
</body>

</html>
```
<a name="de7CV"></a>
#### 2.13.2表格常用属性
```html
<!DOCTYPE html>
<html lang="zh-CN">

<head>
    <meta charset="UTF-8">
    <title></title>
</head>

<body>
    <table border="1" width="500" height="300" cellspacing="0">
        <!-- caption需要css调整样式 -->
        <caption>标题</caption>
        <!-- thead只能加高度height,align控制里面文字水平对齐方式，valign控制垂直对齐 -->
        <thead height="50" align="center" valign="top">
            <th>hhh</th>
            <th>hhh</th>
            <th>hhh</th>
        </thead>
        <!-- tbody -->
        <tbody height="250" align="center">
            <tr height="50" align="left">
                <td width="50">1</td>
                <td>2</td>
                <td>3</td>
            </tr>
            <tr>
                <td >1</td>
                <td>2</td>
                <td>3</td>
            </tr>
            <tr>
                <td>1</td>
                <td>2</td>
                <td>3</td>
            </tr>
        </tbody>
        <tfoot height="50" align="center">
            <tr>
                <td>foot</td>
                <td>foot</td>
                <td>foot</td>
            </tr>
        </tfoot>
    </table>
</body>

</html>
```
<a name="Z4Dch"></a>
#### 2.13.3表格跨行与跨列
```html
<!DOCTYPE html>
<html lang="zh-CN">

<head>
    <meta charset="UTF-8">
    <title></title>
</head>
<!-- 
    --跨行：colspan:x
    --跨列：rowspan:x
 -->

<body>
    <table border="1" width="500" height="300" cellspacing="0">
        <!-- caption需要css调整样式 -->
        <caption>标题</caption>
        <!-- thead只能加高度height,align控制里面文字水平对齐方式，valign控制垂直对齐 -->
        <thead height="50" align="center" valign="top">
            <th>hhh</th>
            <th>hhh</th>
            <th>hhh</th>
        </thead>
        <tbody height="250" align="center">
            <tr height="50" align="center">
                <td colspan="2">1</td>
                <td rowspan="2">3</td>
            </tr>
            <tr>
                <td>1</td>
                <td>2</td>
                <!-- <td>3</td> -->
            </tr>
            <tr>
                <td>1</td>
                <td>2</td>
                <td>3</td>
            </tr>
        </tbody>
        <tfoot height="50" align="center">
            <tr>
                <td>foot</td>
                <td>foot</td>
                <td>foot</td>
            </tr>
        </tfoot>
    </table>
</body>

</html>
```
2.13.4补充常用标签
```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>
<body>
<!--     换行标签 -->
  <br/>
<!--   分割线 -->
  <hr/>
<!--   按原文显示，保留原样式 -->
	<pre>
    I		LOVE		YOU
    	I LOVE YOU
  </pre>
  
</body>
</html>
```
<a name="BocnP"></a>
### 2.14表单
<a name="Mf0Lh"></a>
#### 2.14.1表单的基本结构
```html
<!DOCTYPE html>
<html lang="zh-CN">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <!-- 
        --重要属性：action、name
        --target:_self、_blank,默认—self
        --method:get、post,默认get
     -->
    <form action="https://www.baidu.com/s" target="_blank">
        <input type="text" placeholder="百度搜索" name="wd">
        <button type="submit">搜索</button>
    </form>
    <hr>
    <form action="https://search.jd.com/search">
        <input type="text" placeholder="京东搜索" name="keyword">
        <button type="submit">搜索</button>
    </form>
    <hr>
    <a href="https://search.jd.com/search?keyword=手机">搜索手机</a>

</body>

</html>
```
2.14.2常见表单控件
```html
<!DOCTYPE html>
<html lang="zh-CN">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <form action="#" target="_blank">
        <!-- 文本输入框 -->
        账号：<input type="text" name="username" placeholder="请输入用户名"><br>
        <!-- 密码输入框 -->
        密码：<input type="password" name="pwd" placeholder="请输入密码"><br>
        <!-- 单选框 -->
        性别：<input type="radio" name="genter" value="nale">男<input type="radio" name="genter" value="female"
            checked>女<br>
        <!-- 多选框 -->
        爱好：<input type="checkbox" name="hobby" value="smoke">抽烟
        <input type="checkbox" name="hobby" value="drink" checked>喝酒
        <input type="checkbox" name="hobby" value="perm">烫头<br>
        <!-- 隐藏域：用于提交表单时携带一些固定的数据 -->
        <input type="hidden" name="tag" value="123">
        <!-- 文本框 -->
        其他：<textarea name="other" cols="30" rows="10"></textarea><br>
        <!-- 下拉框 -->
        籍贯：<select name="place">
            <option value="sichuan">四川</option>
            <option value="jiagnxi">江西</option>
            <option value="hubei">湖北</option>
        </select>
        <br>
        <input type="submit" value="确认"></input>
        <!-- <button type="submit">确认</button> -->
        <button type="reset">重置</button>
        <!-- <input type="reset" value="重置"></input> -->
        <button>检查账户是否被注册</button>
    </form>
</body>

</html>
```
![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1678637665489-73fcf77d-c0e4-49a5-a097-0197cf1bcb3d.png#averageHue=%23f7f6f6&clientId=u4fa0f23f-8a87-4&from=paste&height=268&id=u495814d7&name=image.png&originHeight=368&originWidth=423&originalType=binary&ratio=1&rotation=0&showTitle=false&size=15280&status=done&style=none&taskId=ua5e06e06-88c2-48cb-881d-1471f3249a0&title=&width=307.6363636363636)
<a name="urWS7"></a>
#### 2.14.2禁用表单控件
```html
<!-- disabled加入该属性禁用该标签 input,textera,button,select,option可以设置 -->
```
<a name="KR6GT"></a>
#### 2.14.3label控件
```html
<!DOCTYPE html>
<html lang="zh-CN">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <form action="#" target="_blank">
        <!-- 文本输入框 -->
<!--    <!--label可以使账号等提示文字与控件绑定,有两种书写方式-->
        <!--1.label的for属性和控件id属性相对应-->
        <label for="username">账号：</label>
        <input disabled type="text" name="username" placeholder="请输入用户名" id="username"><br>
        <!-- 密码输入框 -->
        <!--2.或者将控件直接写到label里面，也是关联-->
        <label>
          密码：<input type="password" name="pwd" placeholder="请输入密码">
        </label>
        <br>
        <!-- 单选框 -->shux
        性别：<input type="radio" name="genter" value="nale">男<input type="radio" name="genter" value="female"
            checked>女<br>
        <!-- 多选框 -->
        爱好：<input type="checkbox" name="hobby" value="smoke">抽烟
        <input type="checkbox" name="hobby" value="drink" checked>喝酒
        <input type="checkbox" name="hobby" value="perm">烫头<br>
        <!-- 隐藏域：用于提交表单时携带一些固定的数据 -->
        <input type="hidden" name="tag" value="123">
        <!-- 文本框 -->
        其他：<textarea name="other" cols="30" rows="10"></textarea><br>
        <!-- 下拉框 -->
        籍贯：<select name="place">
            <option value="sichuan">四川</option>
            <option value="jiagnxi">江西</option>
            <option value="hubei">湖北</option>
        </select>
        <br>
        <input type="submit" value="确认"></input>
        <!-- <button type="submit">确认</button> -->
        <button type="reset">重置</button>
        <!-- <input type="reset" value="重置"></input> -->
        <button>检查账户是否被注册</button>
    </form>
</body>

</html>
```
<a name="omlDJ"></a>
#### 2.14.4表单fieldset和legend
```html
<!DOCTYPE html>
<html lang="zh-CN">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <form action="#" target="_blank">
        <!-- fieldset-legend用于对表单分区 -->
        <fieldset>
            <legend>主要分类</legend>
            <!-- 文本输入框 -->
            <label for="username">账号：</label>
            <input type="text" name="username" placeholder="请输入用户名" id="username"><br>
            <!-- 密码输入框 -->
            <label for="password">密码：</label>
            <input type="password" name="pwd" placeholder="请输入密码" id="password"><br>
            <!-- 单选框 -->
            性别：<input type="radio" name="genter" value="nale">男<input type="radio" name="genter" value="female"
                checked>女<br>
        </fieldset>
        <fieldset>
            <legend>附加信息</legend>
            <!-- 多选框 -->
            爱好：<input type="checkbox" name="hobby" value="smoke">抽烟
            <input type="checkbox" name="hobby" value="drink" checked>喝酒
            <input type="checkbox" name="hobby" value="perm">烫头<br>
            <!-- 隐藏域：用于提交表单时携带一些固定的数据 -->
            <input type="hidden" name="tag" value="123">
            <!-- 文本框 -->
            其他：<textarea name="other" cols="30" rows="10"></textarea><br>
            <!-- 下拉框 -->
            籍贯：<select name="place">
                <option value="sichuan">四川</option>
                <option value="jiagnxi">江西</option>
                <option value="hubei">湖北</option>
            </select>
            <br>

        </fieldset>
        <input type="submit" value="确认"></input>
        <!-- <button type="submit">确认</button> -->
        <button type="reset">重置</button>
        <!-- <input type="reset" value="重置"></input> -->
        <button>检查账户是否被注册</button>
    </form>
</body>

</html>
```
<a name="VrOI9"></a>
#### 2.14.5表单总结
![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1678717459956-886b01d7-8fee-467e-9ed1-56f8926ea026.png#averageHue=%23f6f6f6&clientId=ub4127b19-e86c-4&from=paste&height=530&id=ub46cbbc0&name=image.png&originHeight=729&originWidth=1530&originalType=binary&ratio=1&rotation=0&showTitle=false&size=436276&status=done&style=none&taskId=u2505be3c-219d-4529-a900-c12358e8520&title=&width=1112.7272727272727)
<a name="fRevu"></a>
### ![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1678717544911-2ba07d82-2563-4c5a-a62f-4d92bd3929c3.png#averageHue=%23faf9f9&clientId=ub4127b19-e86c-4&from=paste&height=357&id=u1242dec0&name=image.png&originHeight=491&originWidth=1532&originalType=binary&ratio=1&rotation=0&showTitle=false&size=272276&status=done&style=none&taskId=ueecca658-c5fc-41cf-96c2-99023a1ce0e&title=&width=1114.1818181818182)2.15框架标签
```html
<!DOCTYPE html>
<html lang="zh-CN">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
    <!-- 单独使用嵌入  -->
    <!-- frameborder:是否显示边框，只有0和1 -->
    <iframe src="https://www.bing.com" width="500" height="300" frameborder="0"></iframe>
    <br>
    <hr>
    <!-- 超链接target与嵌入配合使用 -->
    <a href="https://www.bing.com" target="tt">bing</a>
    <a href="https://www.taobao.com" target="tt">淘宝</a>
    <br>
    <!-- 表单target与嵌入配合使用 -->
    <form action="https://so.toutiao.com/search" target="tt">
        <input type="text" name="keyword">
        <button>搜索</button>
    </form>
    <iframe name="tt"></iframe>
</body>

</html>
```
<a name="LRdV0"></a>
### 2.16html字符实体
```html
<!DOCTYPE html>
<html lang="zh-CN">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>
<body>
    <!-- &nbsp;,&#160;：空格 -->
    <span>h&nbsp;&nbsp;&nbsp;h&nbsp;&nbsp;&nbsp;h</span><br>
    <span>h&#160;&#160;&#160;h&#160;&#160;&#160;h</span>
    <!-- &lt;:<  &gt;:> -->
    <div>&lt;h&gt;</div>
    <!-- &amp;:& -->
    <div>&amp;nbsp;</div>
    <!-- &yen;:￥ -->
    <div>199￥😁&yen;</div>
    <!-- &copy;:© -->
    <div>版权所有：&copy;</div>
    <!-- &times;:× -->
    <div>1 &times; 1 = 1</div>
    <!-- &div:& -->
    <div> 4 &div; 2 = 2</div>
</body>

</html>
```

- 字符实体查询网站：whawg.org

![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1678722731019-33bda778-7e1a-46fc-86f0-9183fe6857d0.png#averageHue=%23f7f6f5&clientId=ub4127b19-e86c-4&from=paste&height=674&id=u4dfdd85f&name=image.png&originHeight=927&originWidth=1363&originalType=binary&ratio=1&rotation=0&showTitle=false&size=283688&status=done&style=none&taskId=u56c7a918-5537-49ec-972b-85daf06b0ab&title=&width=991.2727272727273)
<a name="S90b5"></a>
### 2.17全局属性
![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1678723005574-b90d62d9-987c-4b6c-82bd-1cbe239273f7.png#averageHue=%23f7f6f4&clientId=ub4127b19-e86c-4&from=paste&height=481&id=u376b0b5f&name=image.png&originHeight=662&originWidth=1310&originalType=binary&ratio=1&rotation=0&showTitle=false&size=351854&status=done&style=none&taskId=u40874a63-cb6f-48a5-aca4-fc3e427526e&title=&width=952.7272727272727)
<a name="ETyXQ"></a>
### 2.18meta元信息
```html
<!DOCTYPE html>
<html lang="zh-CN">

<head>
    <!-- 字符编码 -->
    <meta charset="UTF-8">
    <!-- 针对ie浏览器的兼容性设置 -->
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <!-- 针对移动端设备配置 -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <!-- 网页关键字 -->
    <meta name="keywords" content="网上购物,电商购物,皮鞋,化妆品">
    <!-- 网页描述信息 -->
    <meta name="description" content="xxxxxxxxxxxxxxx">
		<!-- 针对爬虫设置   -->
    <meta name="robots" content="此处可见下拉列表">
    <title>Document</title>
</head>

<body>

</body>

</html\>
```
![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1678723491218-510c1b7c-9914-4958-9f30-0a8827619cda.png#averageHue=%23fcfbfb&clientId=ub4127b19-e86c-4&from=paste&height=619&id=u1a031bfd&name=image.png&originHeight=851&originWidth=1394&originalType=binary&ratio=1&rotation=0&showTitle=false&size=371075&status=done&style=none&taskId=ue01656c8-a648-4fa7-85ec-4da327573ea&title=&width=1013.8181818181819)<br />![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1678723727349-37861bfa-a640-4c10-a0c1-ab0e9f85c561.png#averageHue=%23fcfcfc&clientId=ub4127b19-e86c-4&from=paste&height=439&id=u8f890317&name=image.png&originHeight=604&originWidth=1553&originalType=binary&ratio=1&rotation=0&showTitle=false&size=223429&status=done&style=none&taskId=u2f44b85e-9e2d-4cc6-b502-12352649890&title=&width=1129.4545454545455)
<a name="Mg9Ek"></a>
## 3.css
<a name="JshyT"></a>
### 3.1css简介
css全称：层叠样式表（Cascading Style Sheets）<br />css也是一种标记语言，用于给html结构设置样式，例如：文字大小/颜色/元素宽高等。<br />核心思想：实现了结构与样式的分离<br />层叠：一层一层“涂”上去<br />表：列表
<a name="V9ETr"></a>
### 3.2css行内样式
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
### 3.3css内部样式
···
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
### 3.4css外部样式
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
### 3.5css样式优先级
行内样式>内部样式=外部样式<br />看内部样式和外部样式谁后写<br />相同样式后面覆盖前面
<a name="tKHiv"></a>
### 3.6css语法规范
选择器{声明块(声明(属性名:属性值);声明;)}<br />最后一组声明，理论上分号可以省略<br />选择器和声明块要加一个空格<br />冒号和属性值之间有空格<br />声明块里用/*注释*/
<a name="p4HaY"></a>
### 3.7css代码风格
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
### 3.8css选择器
<a name="CC3hR"></a>
#### 3.8.1通配选择器
```css
* {
	margin: 0;
}
/*所有样式，一般用于清除样式 */
```
<a name="fyhNK"></a>
#### 3.8.2元素选择器
```css
h1 {
 color: red;
}
/*<h1>今天天气真好</h1>  */
```
<a name="RTcSw"></a>
#### 3.8.3id选择器
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
#### 3.8.4类选择器
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
#### 3.8.5交集选择器
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
#### 3.8.6并集选择器
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
#### 3.8.7html元素之间的关系
父元素：直接包裹某个元素的元素，就是该元素的父元素，如ul>li中的ul。<br />子元素：被父元素直接包含的元素，如ul>li中的li。<br />祖先元素：父亲的父亲。。。，一直往外赵，都是祖先。<br />后代元素：儿子的儿子。。。，一直往里找，都是后代。<br />兄弟元素：具有相同父亲的元素，互为兄弟元素。
<a name="dFXNe"></a>
#### 3.8.8后代。子代选择器
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
#### 3.8.9兄弟选择器
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
#### 3.8.10属性选择器
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
### 3.9伪类选择器
<a name="QNN9m"></a>
#### 3.9.1伪类的概念
什么是伪类？<br />很像类，但不是类，是元素特殊状态的一种描述
<a name="NCbi7"></a>
#### 3.9.2动态伪类
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
#### 3.9.3结构伪类
<a name="q2pR7"></a>
##### 3.9.3.1结构伪类1
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
##### 3.9.3.2结构伪类2
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
##### 3.9.3.3结构伪类3
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
##### 3.9.3.4否定伪类
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
##### 3.9.3.5ui伪类
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
##### 3.9.3.6目标伪类
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
##### 3.9.3.7语言伪类
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
### 3.10伪元素选择器
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
### 3.11css选择器优先级
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
### 3.12css三大特性

1. 层叠性：如果发生了样式冲突，那么会根据一定的规则（选择器优先级），进行样式的层叠（覆盖）
> 什么是样式冲突：元素的同一个样式名，被设置了不同的值，这就是冲突。

2. 继承性：元素会自动拥有其父元素、或其祖先元素上所设置的某些样式
> 优先继承离得进的（`font-size`，关于文字的样式），不能继承的`background-color`

3. 优先级
> `!important`>行内>id选择器>类选择器>元素选择器>*>继承的样式
> 复杂的需要计算权重，并集选择器是分开计算的！

<a name="Rl304"></a>
### 3.13css像素与颜色
<a name="Ssvjn"></a>
#### 3.13.1像素

- 不同的电脑1px不同，分辨率更高的设备默认缩放倍数也会增大。
- px是网页设计的基本单位。
<a name="ABse6"></a>
#### 3.13.2颜色名

- 能写的颜色名有限
- 表达的颜色不够精细

红色：`red`，绿色：`green`，蓝色：`blue`，紫色：`purple`<br />橙色：`orange`，灰色`gray`
<a name="pfLB0"></a>
#### 3.13.3rgb与rgba

- r:red，g:green，b:blue，光的三原色

全部写数字或者全部写百分比<br />（0-255，0-255，0-255）or（0-100%，0-100%，0-155%）

- a:透明度

范围：0-1，完全透明到完全不透明<br />取色器：qq ctrl+alt+a
<a name="mGQBp"></a>
#### 3.13.4颜色的第三种表示HEX和A
#0000000：前两位表示红色，中间两位表示绿色，最后两位表示蓝色<br />像#ffccee这种3组两两相同的可以简写成：#dce，最后一位透明度也要简写<br />十六进制表示：#000黑色，#fff白色，字母不区分大小写<br />最后再加两位表示透明度，同样是十六进制
<a name="nfabi"></a>
#### 3.13.5颜色的第四种表示HSL和HSLA
hsl(色相,饱和度,亮度)<br />hsla(色相,饱和度,亮度,透明度)<br />色相由角度表示，表示在色相环什么位置：deg表示度
> 0度Red，60度Yellow，120度Green，180度Cyan，240度Blue，300度Magenta

饱和度：0-100%<br />亮度：0-100%
<a name="Oivic"></a>
### 3.14常用css属性
<a name="Dk1TA"></a>
#### 3.14.1字体


