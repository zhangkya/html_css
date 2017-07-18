##第四章 HTML 图像

###4.1 图像标签

```
<img src="url" />
```
**源属性src**

**替换文本属性alt**

```
<img src="boat.gif" alt="Big Boat">
```
####4.1.1 背景图片
```
<html>
<body background="/i/eg_background.jpg">
<h3>图像背景</h3>
<p>gif 和 jpg 文件均可用作 HTML 背景。</p>
<p>如果图像小于页面，图像会进行重复。</p>
</body>
</html>
```
效果如下：

![](img/4.1.1.png)

####4.1.2 排列图片
```
<html>
<body>
<h2>未设置对齐方式的图像：</h2>
<p>图像 <img src ="/i/eg_cute.gif"> 在文本中</p>
<h2>已设置对齐方式的图像：</h2>
<p>图像 <img src="/i/eg_cute.gif" align="bottom"> 在文本中</p>
<p>图像 <img src ="/i/eg_cute.gif" align="middle"> 在文本中</p>
<p>图像 <img src ="/i/eg_cute.gif" align="top"> 在文本中</p>
<p>请注意，bottom 对齐方式是默认的对齐方式。</p>
</body>
</html>
```
效果如下：

![](img/4.1.2.png)

####4.1.3 浮动图像
```
<html>
<body>
<p>
<img src ="/i/eg_cute.gif" align ="left">
带有图像的一个段落。图像的 align 属性设置为 "left"。图像将浮动到文本的左侧。
</p>
<p>
<img src ="/i/eg_cute.gif" align ="right">
带有图像的一个段落。图像的 align 属性设置为 "right"。图像将浮动到文本的右侧。
</p>
</body>
</html>
```
效果如下：

![](img/4.1.3.png)

####4.1.4 调整图像尺寸
```
<html>
<body>
<img src="/i/eg_mouse.jpg" width="50" height="50">
<br />
<img src="/i/eg_mouse.jpg" width="100" height="100">
<br />
<img src="/i/eg_mouse.jpg" width="200" height="200">
<p>通过改变 img 标签的 "height" 和 "width" 属性的值，您可以放大或缩小图像。</p>
</body>
</html>
```
效果如下：

![](img/4.1.4.png)

####4.1.5 为图片显示替换文本
```
<html>
<body>
<p>仅支持文本的浏览器无法显示图像，仅仅能够显示在图像的 "alt" 属性中指定的文本。在这里，"alt" 的文本是“向左转”。</p>
<p>请注意，如果您把鼠标指针移动到图像上，大多数浏览器会显示 "alt" 文本。</p>
<img src="/i/eg_goleft.gif" alt="向左转" />
<p>如果无法显示图像，将显示 "alt" 属性中的文本：</p>
<img src="/i/eg_goleft123.gif" alt="向左转" />
</body>
</html>
```
效果如下：

![](img/4.1.5.png)
####4.1.6 制作图像链接
```
<html>
<body>
<p>
您也可以把图像作为链接来使用：
<a href="/example/html/lastpage.html">
<img border="0" src="/i/eg_buttonnext.gif" />
</a>
</p>
</body>
</html>
```
效果如下：

![](img/4.1.6.png)

####4.1.7 创建图像映射
```
<html>
<body>
<p>请点击图像上的星球，把它们放大。</p>

<img
src="/i/eg_planets.jpg"
border="0" usemap="#planetmap"
alt="Planets" />

<map name="planetmap" id="planetmap">

<area
shape="circle"
coords="180,139,14"
href ="/example/html/venus.html"
target ="_blank"
alt="Venus" />

<area
shape="circle"
coords="129,161,10"
href ="/example/html/mercur.html"
target ="_blank"
alt="Mercury" />

<area
shape="rect"
coords="0,0,110,260"
href ="/example/html/sun.html"
target ="_blank"
alt="Sun" />

</map>

<p><b>注释：</b>img 元素中的 "usemap" 属性引用 map 元素中的 "id" 或 "name" 属性（根据浏览器），所以我们同时向 map 元素添加了 "id" 和 "name" 属性。</p>

</body>
</html>

```
效果如下：

![](img/4.1.7.png)
####4.1.8 把图像转换为图像映射
```
<!DOCTYPE html>
<html>

<body>

<p>请把鼠标移动到图像上，看一下状态栏的坐标如何变化。</p>

<a href="/example/html/html_ismap.html">
<img src="/i/eg_planets.jpg" ismap />
</a>

</body>
</html>
```
效果如下：

![](img/4.1.8.png)
