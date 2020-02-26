### JQuery 
**搭建jQuery环境**

1. 引入jQuery库
```txt
jQuery不需要安装，只需要将下载的jQuery库放到站点的一个公共目录中，然后通过<script/> 引入
```
```html
<script type="text/javaScript" src="jQuery路径"></script>
```
2. jQuery简单测试
```txt
通过$()函数来获取页面中的元素，并对元素进行定位或效果处理， $("myDiv") == jQuery("myDiv")
```
| 区别项   | window.onload                | $(document).ready() |
|----------|------------------------------|---------------------|
| 执行时刻 | 页面全部加载完毕（包括图片） | 所以DOM树下载完毕时 |
| 执行次数 | 页面唯一，多个加载最后一个   | 可以多个            |
| 简写     | \                            | $()                 |


在js中通过getElementById() getElementByClassName() 和querySlector()等方法来获取页面中的HTML元素
```JavaScript
var menuDiv = document.getElementById("menuDiv");
var baseSpan= menuDiv.getElementByClassName("baseClass");
var span    = document.querySelector("#menuDiv");
```

jQuery对象是指通过jQuery库中提供的方法来获取元素对象;
jQuery对象本身不能直接调用DOM对象的方法，需要将其转化成DOM对象之后再调用DOM对象的方法

**DOM对象转化成jQuery对象**
使用jQuery库中的$()方法将DOM对象封装起来，并返回一个jQuery对象

```JavaScript
//获得DOM对象
var  domObject =document.getElementById("myDiv");
//获取DOM对象中的innerHTML属性值
alert(domObject.innerHTML);
//将DOM对象转化成jQuery对象
var jQueryObject=$(domObject);
//调用jQuery对象的html（）方法
alert(jQueryObject.html()i);
```
**jQuery对象转化成jQuery对象**
将jQuery对象转化成DOM对象时，可以把jQuery对象看成一个数组，通过索引[index]或者get(index)方法来获取DOM对象
```JavaScript
//获取jQuery对象（由页面中所有的DIV构成）
var jQueryObject=$("div");
//1.通过下标获取DOM对象
var domObject1=jQueryObject[0];
//2.通过get()方法
var domObject2=jQueryObject.get(0);
```

**jQuery选择器完全继承了css选择器的风格，将jQuery 选择器分为四类**

- 基本选择器
- 层次选择器
- 过滤选择器
- 表单选择器

**通过jQuery提供的选择器快速定位到页面的每个元素后，对元素可以进行各种**

- 属性操作
- 样式操作
- 内容操作

**属性操作**：

1. attr()方法

   获取所以匹配元素集合中的第一个元素的属性

   ```JavaScript
   attr(name);   //返回name属性
   attr(properties); //$("#myImage").attr(title:"我的照片");
   attr（key,value）;
   attr(key,function(index,oldAttr));
   ```

2. css()方法

   设置所匹配项的样式

   ```javascript
   css(attrName);
   css(key,value);
   css(properties);
   ```

3. removeAttr()方法

   删除匹配元素的指定属性

   ```JavaScript
   $("myDiv").removeAttr("title");T
   ```

**内容操作**

1. html()方法

   ```javascript
   html()
   html(htmlCode)
   html(function(index, oldHtmlCode))
   //---------------------------------------------------------------------
   //返回#mainContentDiv标签的HTML内容
   $("#mainContentDiv").html();
   //设置#mainContentDiv标签的HTML内容为红色标题格式的“漫步时尚广场”
   $("#mainContentDiv").html("<h1><font color='red'>漫步时尚广场</font><h1/>");
   //根据元素在集合中的位置不同，设定不同的HTML内容
   $("p").html(function(index,htmlCode){
            switch(index){
   	case 0 : return "<h1>"+htmlCode+"<h1/>";
   	case 1 : return "<h2>"+htmlCode+"<h2/>";
            }
   });
   ```

2. hover()方法

   悬停事件

   ```JavaScript
   使用hover()方法设置单元格悬停特效
   $("td").hover(
   	function(){
   		$(this).addClass("hover");
   	},function(){
   		$(this).removeClass("hover");
   	}
   );
   ```

   