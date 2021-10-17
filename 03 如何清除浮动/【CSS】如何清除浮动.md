# 如何清除浮动

## 为什么要清除浮动
css布局经常使用到浮动属性，而浮动会影响整体布局，要避免浮动对其他元素布局的影响，需要清除浮动。
例如下面代码：
``` html
<div class="parent clearfix">
    <div class="flt_l child"></div>
    <div class="flt_r child"></div>
</div>
被影响的元素
<p>也是被影响的元素</p>
```
样式为：
```html
<style type="text/CSS">
    .flt_l{
        float: left;
        width: 200px;
        height: 200px;
        background-color: rgb(7, 146, 18);
    }
    .flt_r{
        float: right;
        width: 100px;
        height: 270px;
        background-color: rgb(112, 231, 128);
    }
    .parent{
        border:4px coral solid;
    }
</style>
```
![2个绿色的div设置了浮动.png](http://tva1.sinaimg.cn/large/003Dkuxqgy1gvingzolatj60hs0a9t9c02.jpg)

两个绿色的DIV因为设置了浮动，所以父元素没有高度，边框为一条线，而且影响了后面的文字和p标签。

我们想要的显示效果是这样的：
![清除浮动后的布局.png](http://tva1.sinaimg.cn/large/003Dkuxqgy1gvini8qo5gj60hz0av0to02.jpg)

清除浮动有以下四种方法：


## 一 父元素给定高度
当父元素不给高度的时候，内部元素不浮动时会撑开,而浮动的时候，父元素高度就变成0，所以给父元素设定了高度可以消除子元素浮动带来的影响。
``` css
    .parent{
        height:270px;
    }
```
这种方法的**优点**：简单直接，
**缺点**：不够灵活
## 二 加一个空div
在最后一个浮动的标签后，添加一个空标签，并给标签加上`clear:both`样式，空元素清除浮动后父元素会自动检测子元素的最大高度，“撑起”到最大高度。
```html
<div class="parent clearfix">
    <div class="flt_l child"></div>
    <div class="flt_r child"></div>
    <div style="clear:both"></div>
</div>
```
这种方法的**优点**：简单直接，
**缺点**：引入多余的标签，不符合语义化标准。
## 三 overflow:hidden
给父元素添加`overflow:hidden`属性，触发BFC（Block Formatting Context：块级格式化上下文）模式 。实现清除浮动。
*[什么是BFC](https://www.cnblogs.com/realjianghao/p/13695250.html)*

```
.parent{
    overflow: hidden; 
}
```
这种方法的**优点**：代码简单，**缺点**：子元素浮动内容增多的时候容易造成不会自动换行，导致内容被隐藏掉，无法显示全部子元素内容。

## 四 利用伪元素(推荐使用)
利用伪元素`:after`清除浮动，伪元素是行内元素，是浏览器清除浮动的方法
``` css
.clearfix:after{
    clear: both;
    content: "";
    height: 0;
    display: block;
    visibility: hidden;
}
```
这种方法的**优点**：符合闭合浮动思想，结构语义化正确代码简单，**缺点**：有的浏览器不支持伪元素。
