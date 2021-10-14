# html中css的四种应用方式

有以下html元素
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>email</title>
</head>
<body>
<p>学习科目

使用 HTML 和 CSS 构建乐谱。
请针对上述课题提供更多的信息。包括研究时长、所需资源，以及其它未尽事宜，谢谢。</p>
<p>波利尼西亚小鸡舞
一种古老、神秘但影响广泛的舞蹈,整个村庄围绕着一个小鸡形状的圈跳舞，祈祷牲畜肥美。</p>
<p>冰岛布尔曳步舞
在冰岛人学会用火取暖之前，舞蹈时人们在地上拥成一个圈，用极小极快的动作晃动身体。</p>
<p>北极机器人舞
一个有趣的历史误传，二十世纪六十年代的英国探险者宣称发现了一种像“机器人跳舞”的舞蹈</p>
</body>
</html>
```
显示效果如下：
![css01.png](http://tva1.sinaimg.cn/large/003Dkuxqgy1gve0fkp7uhj60ja075jxs02.jpg)


加入样式后显示为：![css02.png](http://tva1.sinaimg.cn/large/003Dkuxqgy1gve2v6gxxlj60j908uteq02.jpg)

### **引用方法**：
*参考原文：[语言中文网](http://c.biancheng.net/view/1293.html)*

**一、行内样式**
```
<body>
<p style="color:red;font-size:20px">学习科目
使用 HTML 和 CSS 构建乐谱。
请针对上述课题提供更多的信息。包括研究时长、所需资源，以及其它未尽事宜，谢谢。</p>
<p style="color:pink;font-size:26px">波利尼西亚小鸡舞
一种古老、神秘但影响广泛的舞蹈,整个村庄围绕着一个小鸡形状的圈跳舞，祈祷牲畜肥美。</p>
<p style="color:oringe;font-size:16px;font-weight:heavy;background-color: cornsilk">冰岛布尔曳步舞
在冰岛人学会用火取暖之前，舞蹈时人们在地上拥成一个圈，用极小极快的动作晃动身体。</p>
<p>北极机器人舞
一个有趣的历史误传，二十世纪六十年代的英国探险者宣称发现了一种像“机器人跳舞”的舞蹈</p>
</body>
```
 

**二、嵌入样式**
```
<head>
    <style type="test/CSS">
        p1{color:red;font-size:20px;}
        p2{color:pink;font-size:26px;}
        p3{color:orange;font-size:16px;font-weight:heavy;background-color:cornsilk;}
    </style>
    <title>email</title>
</head>
<body>
<p class="p1">学习科目
使用 HTML 和 CSS 构建乐谱。
请针对上述课题提供更多的信息。包括研究时长、所需资源，以及其它未尽事宜，谢谢。</p>
<p class="p2">波利尼西亚小鸡舞
一种古老、神秘但影响广泛的舞蹈,整个村庄围绕着一个小鸡形状的圈跳舞，祈祷牲畜肥美。</p>
<p class="p3">冰岛布尔曳步舞
在冰岛人学会用火取暖之前，舞蹈时人们在地上拥成一个圈，用极小极快的动作晃动身体。</p>
<p class="p4">北极机器人舞
一个有趣的历史误传，二十世纪六十年代的英国探险者宣称发现了一种像“机器人跳舞”的舞蹈</p>
</body>
```

**三、链接**
```
<head>
    <link type="text/css" href="method3Link.css" rel="stylesheet">
</head>
<body>
<p class="p1">学习科目
使用 HTML 和 CSS 构建乐谱。
请针对上述课题提供更多的信息。包括研究时长、所需资源，以及其它未尽事宜，谢谢。</p>
<p class="p2">波利尼西亚小鸡舞
一种古老、神秘但影响广泛的舞蹈,整个村庄围绕着一个小鸡形状的圈跳舞，祈祷牲畜肥美。</p>
<p class="p3">冰岛布尔曳步舞
在冰岛人学会用火取暖之前，舞蹈时人们在地上拥成一个圈，用极小极快的动作晃动身体。</p>
<p class="p4">北极机器人舞
一个有趣的历史误传，二十世纪六十年代的英国探险者宣称发现了一种像“机器人跳舞”的舞蹈</p>
</body>
```

**四、导入**

使用 import 命令导入外部css文件，此方法有6种等价表示法：
- `@import style.css`
- `@import 'style.css'`
- `@import "style.css"`
- `@import url(style.css)`
- `@import url('style.css')`
- `@import url("style.css")`
  
语句包含在`<head><style></style></head>`中

所以：
```
<head>
    <style>import style.css</style>
</head>
<body>
<p class="p1">学习科目
使用 HTML 和 CSS 构建乐谱。
请针对上述课题提供更多的信息。包括研究时长、所需资源，以及其它未尽事宜，谢谢。</p>
<p class="p2">波利尼西亚小鸡舞
一种古老、神秘但影响广泛的舞蹈,整个村庄围绕着一个小鸡形状的圈跳舞，祈祷牲畜肥美。</p>
<p class="p3">冰岛布尔曳步舞
在冰岛人学会用火取暖之前，舞蹈时人们在地上拥成一个圈，用极小极快的动作晃动身体。</p>
<p class="p4">北极机器人舞
一个有趣的历史误传，二十世纪六十年代的英国探险者宣称发现了一种像“机器人跳舞”的舞蹈</p>
</body>
```
  
***tips***
- style标签有标题“title”属性
- 样式控制的优先级：行内 > 嵌入 > 链接 ？导入


