##第二章 HTML CSS

###1.1 外部样式表
```
<head>
<link rel="stylesheet" type="text/css" href="mystyle.css">
</head>
```
###1.2 内部样式表
```
<head>
<style type="text/css">
  body {backgroud-color:red}
  p {margin-left:20px}
</style>
</head>
```
###1.3 内联样式
```
<p style="color:red;margin-left:20px">
```

###1.4 导入外部样式
```
<style type="text/css">@import"myStyle.css"</style>
```
###1.5 执行顺序和优先级

1. 相同导入方式下，同一对象用不同数量元素来描述时
```
h1{backgroup-color:red;}
#top h1{backgroup-color:blue;}
```
**css自有一套特殊性判定方式，特殊性越高的则优先级越高，而特殊性越一般情况下，描述越具体，则特殊性越高，像例子中加了div的id后，更能明确是哪一个div下的h1，则后一个优先级越高，所以最终应该是蓝色**

2. 相同导入方式下，同一个对象用不同元素来描述时
```
h1{backgroup-color:red;}
#myWay{backgroup-color:blue;}
```
**雷同于上一个对比，此对比中，id选择符或者class选择符的特殊性更高，所以最后应该是蓝色**

3. 内部样式和内嵌样式表
```
#myWay{backgroup-color:red;}
<div id="myWay" style="backgroup-color:blue;" />
```
**这种进行对比的时候，style元素比id选择符的优先级更高，所以最终会是蓝色**

4. 特殊性和起源都相同
```
#myWay{backgroup-color:red;}
#myWay{backgroup-color:blue;}
```
**这种进行比较的时候，以后一个为准，前一个表示被覆盖无法显现，则最终会是蓝色**

5. 执行重要性!important
```
#myway{backgroup-color:blue!important;}
<div id="myWay" style="backgroup-color:red" />
```
**当指定重要性的时候，优先级别是最高的，所以会是蓝色**

6. 文件内部样式和外界导入或者链入

**任何文件内的规则都比外界引用的规则优先级高**
