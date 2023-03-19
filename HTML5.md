<a name="G1nSp"></a>
## 1.H5简介
![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1679135053606-c1def8df-3ed1-4c1a-8602-041b6de0ab37.png#averageHue=%23f7f6f6&clientId=uaf385daf-e458-4&from=paste&height=577&id=ua24ae331&name=image.png&originHeight=793&originWidth=1047&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=290616&status=done&style=none&taskId=u79800191-2cca-41a6-be37-485392bdde1&title=&width=761.4545454545455)<br />![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1679135612305-1a50bff6-baa9-4ce5-9ec8-fd5e3f424b8d.png#averageHue=%23e7e1d7&clientId=uaf385daf-e458-4&from=paste&height=168&id=u53ba15cb&name=image.png&originHeight=231&originWidth=1090&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=103358&status=done&style=none&taskId=ub871fa23-8b6a-4034-a32c-d693c59f9b7&title=&width=792.7272727272727)
<a name="wk3jv"></a>
## 2.H5新增布局标签

- 主要掌握前6个

![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1679135806794-186c3305-89c7-41fa-b2b9-f6f82a92fa1b.png#averageHue=%23f7f7f6&clientId=uaf385daf-e458-4&from=paste&height=624&id=uf1791d4a&name=image.png&originHeight=858&originWidth=1055&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=299959&status=done&style=none&taskId=u897e2b66-d503-43e5-a4f2-ff96fda7390&title=&width=767.2727272727273)
<a name="G49SG"></a>
## 3.H5新增状态标签
![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1679137476497-e2111a14-02d4-42ef-a909-b214d959783b.png#averageHue=%23f6f6f6&clientId=uaf385daf-e458-4&from=paste&height=615&id=uf50ae01c&name=image.png&originHeight=845&originWidth=1088&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=224065&status=done&style=none&taskId=u290ce3b8-a578-4f61-bda7-87c77558b8d&title=&width=791.2727272727273)
```html
<!DOCTYPE html>
<html lang="zh-CN">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>
  	<!-- 可以调宽高 -->
    <!--我optimum：区间low到high之间为正常值，其他为警告 -->
    <!--有optimum： 区间被low和high划分，optimum所在的区间为正常值，剩下的划分为警告和危险 -->
    手机电量：
    <meter max="100" min="0" value="70" low="40" optimum="90"></meter><br>
    <!-- progress只有两个属性max和value -->
    当前进度
    <progress max="100" value="50"></progress>
</body>

</html>
```
![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1679137428679-6e29ee29-6991-4057-91f1-00e9767b0874.png#averageHue=%23f3f2f2&clientId=uaf385daf-e458-4&from=paste&height=72&id=u58590755&name=image.png&originHeight=99&originWidth=415&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=2703&status=done&style=none&taskId=u42436497-c498-4792-80bc-49de280a62d&title=&width=301.8181818181818)
<a name="RCQJ0"></a>
## 4.H5新增列表标签
![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1679146012946-4f2958c5-4643-4a22-9fdc-5a95a59da94a.png#averageHue=%23f6f6f5&clientId=uaf385daf-e458-4&from=paste&height=479&id=udcedce64&name=image.png&originHeight=659&originWidth=1015&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=200069&status=done&style=none&taskId=u8f1546a1-aee0-4be7-94ff-591beec62ee&title=&width=738.1818181818181)
```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>
<body>
    <!-- 不同浏览器呈现的样式不一样 -->
    <form action="#">
        <input type="text" list="mydata">
        <button>搜索</button>
    </form>
    <!-- 通过id和inpout输入框绑定 -->
    <datalist id="mydata">
        <option value="周杰伦">周杰伦</option>
        <option value="周冬雨">周冬雨</option>
        <option value="马冬梅">马冬梅</option>
        <option value="温兆伦">温兆伦</option>
    </datalist>、
    <hr>
    <!-- details用于展示问题和答案，或对专有名词做解释 -->
    <!-- summary写在details里面，用于指定问题或专有名词 -->
    <details>
        <summary>如何一夜暴富</summary>
        <p>来到尚硅谷学前端</p>
    </details>
</body>
</html>
```
<a name="lhqXg"></a>
## 5.H5新增文本标签
> http://www.aies.cn/pinyin2.htm

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>
<body>
    <!-- ruby展示拼音 -->
    <ruby>
        <span>魑魅魍魉</span>
        <rt>chi mei wang liang</rt>
    </ruby>
    <hr>
    <ruby>
        <span>魑</span>
        <rt>chi</rt>
    </ruby>
    <!-- mark建议搜索栏中关键字 -->
    <p>Lorem ipsum,<mark>dolor</mark> sit amet consectetur adipisicing elit. Impedit quidem debitis minima minus
        delectus voluptatum libero est consequuntur sapiente, officiis at tempora, vel accusamus fuga repellat quasi?
        Suscipit, perspiciatis odit!</p>
</body>
</html>
```
![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1679146430680-8aa8d3cf-87f2-4613-b371-59d12f5c4722.png#averageHue=%23f9f9f9&clientId=uaf385daf-e458-4&from=paste&height=505&id=ueba52520&name=image.png&originHeight=694&originWidth=1098&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=166908&status=done&style=none&taskId=udb1d4c57-0d7c-4ddb-bd7a-c2e938c124c&title=&width=798.5454545454545)
<a name="eNSMC"></a>
## 6.H5表单相关新增
```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>
<body>
    <form action="#">
        <!-- placeholder：占位符，提示，用于文字输入的控件-->
        <!-- required：必填的看，加在单选择项里，表示从里面选一个，多选里表示必须选择 -->
        <!-- autofocus：自动对焦，冲突则选择先选的那个-->
        <!-- autocomplete：on|off 自动提示历史记录，需要浏览器开启保存地址-->
        <!-- pattern="正则表达式"，！注意，在不写required时也能提交-->
        账号：<input type="text" name="account" placeholder="请输入6位账号" required autofocus autocomplete="on" pattern="\w{6}">
        <br>
        密码：<input type="password" name="pwd" placeholder="请输入密码" required>
        <br>
        性别：
        <input type="radio" name="gender" id="" value="male" required>男
        <input type="radio" name="gender" id="" value="female">女
        <br>
        爱好：
        <input type="checkbox" name="hobby" id="" value="smoke">抽烟
        <input type="checkbox" name="hobby" id="" value="drink" required>喝酒
        <input type="checkbox" name="hobby" id="" value="prem">烫头
        <br>
        其他：<textarea name="ouher" id="" cols="30" rows="10" placeholder="其他……"></textarea>
        <br>
        <button>提交</button>
    </form>
</body>
</html>
```
![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1679147749826-cbdf7e81-192d-42de-8f22-91b0c6e1e5c9.png#averageHue=%23f7f6f6&clientId=uaf385daf-e458-4&from=paste&height=369&id=ubb28af5e&name=image.png&originHeight=508&originWidth=1072&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=233109&status=done&style=none&taskId=u8f7eca55-21dd-4f15-9f20-048fabf0345&title=&width=779.6363636363636)
<a name="lasuo"></a>
## 7.H5新增input的type值
> url转码：http://www.wetools.com/url-encode

![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1679148986672-9be1167a-dae2-4829-9884-1c28c707a20b.png#averageHue=%23f8f8f7&clientId=uaf385daf-e458-4&from=paste&height=649&id=uc1e4abaa&name=image.png&originHeight=892&originWidth=978&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=438031&status=done&style=none&taskId=uc243f1d0-d63c-4ea9-a056-7303a0a6515&title=&width=711.2727272727273)
```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>
<body>
<!-- novalidate:表单提交不校验   -->
    <form action="#" novalidate>
        邮箱：<input type="email" name="email"><br>
        url：<input type="url" name="url" id=""><br>
        <!-- step:步数，输入必须时step的倍数 -->
        数值：<input type="number" name="number" step="2" min="0" max="100"><br>
        <!-- 可以快速删除输入框中的数据，语义化 -->
        搜索：<input type="search" name="keyword"><br>
        <!-- 用在移动端 -->
        电话：<input type="tell"></input><br>
        <!-- 不能显示数值 -->
        范围：<input type="range" name="range" min="0" max="100" value="0"><br>
        <!-- 提交为16进制 -->
        颜色：<input type="color" name="color"><br>
        <!-- type=date|month|week|time|datetime-local -->
        日历：<input type="date" name="date"><br>
        <button>提交</button>
    </form>
</body>
</html>
```
<a name="R4bcT"></a>
## 8.H5新增多媒体标签
![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1679149784406-412ab1ac-93d8-4476-9370-668320f9c969.png#averageHue=%23faf9f9&clientId=uaf385daf-e458-4&from=paste&height=573&id=u918fb307&name=image.png&originHeight=788&originWidth=1030&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=293357&status=done&style=none&taskId=u7cf1de90-8796-44aa-b7d6-0d7d97d74bc&title=&width=749.0909090909091)
<a name="d1Ybi"></a>
## 9.H5新增音频标签
![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1679150368964-36dfae85-043a-4955-b3b1-f39e5c7917c3.png#averageHue=%23f9f8f8&clientId=uaf385daf-e458-4&from=paste&height=463&id=uacb4e06a&name=image.png&originHeight=636&originWidth=1062&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=198616&status=done&style=none&taskId=u41a6c79c-2830-4092-89e1-39334e264fb&title=&width=772.3636363636364)
<a name="nsKhv"></a>
## 10.H5新增全局属性
![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1679150399326-682a89b2-af58-44f5-a5de-038794ba113c.png#averageHue=%23f8f8f7&clientId=uaf385daf-e458-4&from=paste&height=455&id=u9f182c9e&name=image.png&originHeight=625&originWidth=1026&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=164795&status=done&style=none&taskId=u27b6f2e9-80a9-4a28-88e0-94c644c9bf0&title=&width=746.1818181818181)

<a name="Yk969"></a>
## 11.H5兼容性问题
![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1679152152795-1c175045-6e8c-40bb-bb05-abed3d7cdc74.png#averageHue=%23dbd7cd&clientId=uaf385daf-e458-4&from=paste&height=615&id=uf613d088&name=image.png&originHeight=846&originWidth=1179&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=268400&status=done&style=none&taskId=u3e95e25b-78d8-4e4b-a373-d5017f2e606&title=&width=857.4545454545455)![image.png](https://cdn.nlark.com/yuque/0/2023/png/32617700/1679152549352-b103134f-fa7a-489c-9ad6-f950557611b2.png#averageHue=%23ddd8cd&clientId=uaf385daf-e458-4&from=paste&height=193&id=u392a1283&name=image.png&originHeight=266&originWidth=548&originalType=binary&ratio=1.375&rotation=0&showTitle=false&size=113628&status=done&style=none&taskId=uf94db887-df6a-4f66-9aba-4f5eb6546d9&title=&width=398.54545454545456)
