<a name="sW2U2"></a>
### 1.html是什么？
全称：HyperType Markup Languang<br />翻译为：标记语言<br />超文本：暂且理解为“超级文本”，和普通文本相比，内容更加丰富<br />标记：文本想要变成超文本，需要借助各种标记符号<br />语言：每一个标记的写法。读音、使用规则
<a name="FWUGL"></a>
### 2.互联网发展史
IETF：Internet Engineering Task Force(国际互联网工程任务组，成立于1985年)<br />W3C：World Wide Web Consortium(万维网联盟，成立于1994年)<br />![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1678587496508-14f8e4ec-4c34-4ede-8640-8b8b46c19896.png#averageHue=%23474544&clientId=u3b45df95-5f9a-4&from=paste&height=643&id=ua3ac8488&name=image.png&originHeight=884&originWidth=1883&originalType=binary&ratio=1&rotation=0&showTitle=false&size=702461&status=done&style=none&taskId=u87f3ac48-db6c-4411-b6c6-eef730330d6&title=&width=1369.4545454545455)
<a name="RTDOO"></a>
### 3.html初体验
<a name="O45iV"></a>
#### 3.1html注释
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
#### 3.2文档声明
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
#### 3.3字符编码
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
#### 3.4设置网页语言
<a name="zDEk3"></a>
##### 3.4.1shift+刷新：强制刷新
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
#### 3.5html标准结构
<a name="wWoxY"></a>
##### 3.5.1快速删除多行ctrl+shift+k
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
### 5.html语义化标签
1.代码的可读性强<br />2.有利于爬虫检索<br />3.方便盲人阅读器、屏幕阅读器
<a name="Wevpy"></a>
### 6.块级元素和行内元素
shift+alt+上/下快速复制一行<br />1.块级元素：<br />--独占一行<br />--块内元素内块内元素和行内元素都能写<br />2.行内元素：<br />--不独占一行<br />--行内元素内只能有行内元素<br />3.特殊规则<br />--h1、h6不能互相嵌套<br />--p标签中不能写块元素<br />--marquee几乎不被使用了，废除了
<a name="F5u51"></a>
### 7.常用的文本标签
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
### 8.不常用的文本标签
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
### 9.图片标签
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
### 10.超链接
<a name="jRPtD"></a>
#### 10.1跳转页面
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
#### 10.2跳转文件
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
#### 10.3跳转锚点
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
#### 10.4超链接唤起指定应用
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
### 11.超文本
“超文本”是一种组织信息的方式，通过超链接将不同空间的文字、图片等各种信息组织在一起，能从当前阅读的内容，跳转到超链接所指方向的内容（页面、文件、锚点、应用）。
<a name="vxxMw"></a>
### 12.列表
<a name="i1KXG"></a>
#### 12.1列表的使用
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
<a name="sjlDW"></a>
#### 12.2列表使用的注意事项
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
### 13.表格
<a name="CE4Ff"></a>
#### 13.1表格结构
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
#### 13.2表格常用属性
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
#### 13.3表格跨行与跨列
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
<a name="ugXfD"></a>
#### 13.4补充常用标签
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
### 14.表单
<a name="Mf0Lh"></a>
#### 14.1表单的基本结构
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
<a name="ODfcE"></a>
#### 14.2常见表单控件
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
#### 14.2禁用表单控件
```html
<!-- disabled加入该属性禁用该标签 input,textera,button,select,option可以设置 -->
```
<a name="KR6GT"></a>
#### 14.3label控件
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
#### 14.4表单fieldset和legend
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
#### 14.5表单总结
![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1678717459956-886b01d7-8fee-467e-9ed1-56f8926ea026.png#averageHue=%23f6f6f6&clientId=ub4127b19-e86c-4&from=paste&height=530&id=ub46cbbc0&name=image.png&originHeight=729&originWidth=1530&originalType=binary&ratio=1&rotation=0&showTitle=false&size=436276&status=done&style=none&taskId=u2505be3c-219d-4529-a900-c12358e8520&title=&width=1112.7272727272727)
<a name="fRevu"></a>
### ![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1678717544911-2ba07d82-2563-4c5a-a62f-4d92bd3929c3.png#averageHue=%23faf9f9&clientId=ub4127b19-e86c-4&from=paste&height=357&id=u1242dec0&name=image.png&originHeight=491&originWidth=1532&originalType=binary&ratio=1&rotation=0&showTitle=false&size=272276&status=done&style=none&taskId=ueecca658-c5fc-41cf-96c2-99023a1ce0e&title=&width=1114.1818181818182)15.框架标签
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
### 16.html字符实体
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
### 17.全局属性
![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1678723005574-b90d62d9-987c-4b6c-82bd-1cbe239273f7.png#averageHue=%23f7f6f4&clientId=ub4127b19-e86c-4&from=paste&height=481&id=u376b0b5f&name=image.png&originHeight=662&originWidth=1310&originalType=binary&ratio=1&rotation=0&showTitle=false&size=351854&status=done&style=none&taskId=u40874a63-cb6f-48a5-aca4-fc3e427526e&title=&width=952.7272727272727)
<a name="ETyXQ"></a>
### 18.meta元信息
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
## <br />
