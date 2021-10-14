# 在HTML中插入图标的方法

要在html中引入图标，除了使用本地或网络图片，还可以通过代码直接引入图标，这里分享2种方法从*阿里巴巴图标网站*[iconfont](http://www.iconfont.cn/)引入图标。

###  方法一 下载图标字体到本地使用

1.到[http://www.iconfont.cn/](http://www.iconfont.cn/)，找到图标，添加到项目

![把图标添加入库.png](http://tva1.sinaimg.cn/large/003Dkuxqgy1gvfdzsuhc7j604704haa202.jpg)

![将图标库中的图标加入项目中.png](http://tva1.sinaimg.cn/large/003Dkuxqgy1gvfeez6hbfj607b0gomxm02.jpg)

![选择Font class 下载至本地.png](http://tva1.sinaimg.cn/large/003Dkuxqgy1gvfg532wxbj60mw09yjt102.jpg)


2.下载图标素材到本地，解压将所有文件放入项目的“css”文件夹中
![文件放在css目录下.png](http://tva1.sinaimg.cn/large/003Dkuxqgy1gvfekmjrkpj60au072dhh02.jpg)

3.打开【iconfont.css】文件
代码如下：
``` css
@font-face {
  font-family: "iconfont"; /* Project id 2869079 */
  src: url('iconfont.woff2?t=1634235505991') format('woff2'),
       url('iconfont.woff?t=1634235505991') format('woff'),
       url('iconfont.ttf?t=1634235505991') format('truetype');
}

.iconfont {
  font-family: "iconfont" !important;
  font-size: 48px;
  font-style: normal;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

插入的图标class在这里，这里只有1个图标
.icon-shouye:before {
  content: "\e6e4";
}

```
在html中加入`<i class="iconfont icon-shouye"></i>`
html代码如下:
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <link rel="stylesheet" href="css/iconfont.css">
  <title>newproject</title>
</head>
<body>
  <span>  插入的图标<i class="iconfont icon-shouye"></i></span>
</body>
</html>
```
![引入效果.png](http://tva1.sinaimg.cn/large/003Dkuxqgy1gvffc5g5exj603c01pgli02.jpg)

###  方法二 cdn引入
1.到[http://www.iconfont.cn/](http://www.iconfont.cn/)，找到图标，添加到项目

![把图标添加入库.png](http://tva1.sinaimg.cn/large/003Dkuxqgy1gvfdzsuhc7j604704haa202.jpg)

![将图标库中的图标加入项目中.png](http://tva1.sinaimg.cn/large/003Dkuxqgy1gvfeez6hbfj607b0gomxm02.jpg)

2.生成css代码
![选择Font lass 生成代码.png](http://tva1.sinaimg.cn/large/003Dkuxqgy1gvffo3ef3bj60n30doq5r02.jpg)

3.将链接复制到html文件中，记得加上`http:`插入元素`<i class="iconfont icon-shouye"></i>`图标class 可访问[链接地址](http://at.alicdn.com/t/font_2869079_7c6ua4wkr86.css)http://at.alicdn.com/t/font_2869079_7c6ua4wkr86.css复制，引入成功。
![复制css连接到项目html中.png](http://tva1.sinaimg.cn/large/003Dkuxqgy1gvffp2o7i1j60nv0ehq6902.jpg)
![引入的效果.png](http://tva1.sinaimg.cn/large/003Dkuxqgy1gvffusb87ij60350143yc02.jpg)

代码如下：
``` html
<!DOCTYPE html>
<html lang="en">
<head>
  <link rel="stylesheet" href="http://at.alicdn.com/t/font_2869079_7c6ua4wkr86.css">
  <title>newproject</title>
</head>
<body>
  <span>  插入的图标<i class="iconfont icon-shouye"></i></span>
</body>
</html>
```