# CSS 页面布局管理

### 伪类

```txt
伪类选择器
 定义 ： 伪类和伪元素时预先定的，独立于文档元素的，能够被浏览器自动识别的元素。
 伪类 ： 处于特殊状态的元素称为伪类  例如： 被鼠标聚焦的按钮
 注意 ： “：”开始，前后不能有空格
```

|**伪类名*|**描述**|
|--------|--------|
|:active|向被激活的元素加样式|
|:focus|向拥有键盘焦点的元素添加样式|
|:hover|当鼠标悬浮在元素上方时，向元素添加样式|
|:link|向未被访问的标签添加样式，目前仅支持超链接|
|:visited|向已经访问过的元素添加样式，目前仅支持超链接|
|:readonly|向只读元素添加样式|
|:checked|向被选中的元素添加样式|
|:disabled|向被禁用的元素添加样式|
|:enable|向可用的元素添加样式|
|||
### 伪元素
```txt
伪元素：
 伪元素表示某元素的部分内容，虽然在逻辑上存在但在文档树中不存在与之对应的部分
```

|**伪元素**|**描述**|
|---------|--------|
|:first-line|向文本的首行添加特殊样式|
|:first-letter|向文本的第一个字母或汉字添加特殊样式|
|:before|在元素之前添加内容|
|:after|在元素的后面添加内容|
|||
![](/home/zegu/DATA/markdown/html_css_study/css/图片1.png)

```html
.box,a-box{
	width :200px;
	height:200px;
	background-color:red;
}
.a-box:hover:before{
	content:'';
	display:block;
	width: 0px;
	height:0px;
		border-top:100px solid transparent;
		border-left:400px solid green;
		border-bottom:100px solid transparent;
		position:relative;
	left:200px;
}
```


### 字体



![](/home/zegu/DATA/markdown/html_css_study/css/图片3.png)

```txt
字体属性
字体又称字型，是字母和符号的样式的集合。虽然字体之间会有一定的差异，但总体上特征基本相同；
```

|**功能**|**属性名**|**描述**|
|-------|------|------|
|字体颜色|color|设置文本颜色|
|字体类型|font-family|设置文本的字体|
|字体风格|font-style|设置字体样式，取值normal（正常）,italic（斜体）,oblique（倾斜)|
|字体变形|font-variant|设置小型大写字母，取值normal（正常），snall-caps（小型大写字母）|
|字体加粗|font-weight|设置字体的粗细，取值border（特粗体），blod（粗体），normal（正常），lighter（细体），或者100~900之间的9个等级|
|字体大小|font-size|设置文本的大小，值可以是绝对或相对值，其中绝对值从小到大依次xx-small、x-small、small、medium（默认）、large、x-large、xx-large；单位可以是pt或em，也可以采用百分比（%）的形式|
|行间距|line-height|设置文本的行高，即两行文本基线的距离|
|简写|font| font : font-style font-variant font-weight font-size/line-height font-family|
|||
### display
```txt
display 属性
	通过display属性可以将页面元素隐藏或者显示出来；
	通过display属性可以将元素强制改为块级或者内联元素；
```

|**功能**|**描述**|
|-------|--------|
|none|将元素设置隐藏状态|
|block|将元素显示为块级元素，此元和尿素前后会带换行符|
|inline|默认，次元素会被显示为内联元素，元素前后无换行符|
|||
### position
```txt
position：定位
(1）当position的属性设置为relative，absolute或者fixed时，可以使元素的偏移属性left，top，right和bottom进行重新定位
（2）当position的属性值设置为static时，会忽略left，top，right，bottom和z-index等相关属性的设置。
```

|**属性值**|**描述**|
|---------|--------|
|static|正常流（默认值），元素在页面中正常出现，并作为页面的一部分|
|relative|相对定位，相对于其正常位置进行定位，并保持器未定位前的形状所占的空间|
|absolute|绝对定位，相对于浏览器窗口进行定位，并将元素框从页面文档流中完全删除后重新定位。当拖拽页面滚动条时，该元素随其一起滚动|
|fixed|固定定位，相对于浏览器窗口定位，将元素框从页面中完全删除后，重新定位，当拖拽页面滚动时，该元素不会随之滚动|
|||

### 盒子模型
```txt
（1）.在页面布局中，为了敬爱那个页面元素合理有效的组织在一起，形成一套完整的，行之有效的原则和规范，称为盒子模型。
（2）.页面中的所有元素都可以看成一个盒子，并占据一定的页面空间，通过盒子间的嵌套叠加或并列，最终形成了页面。
（3）.盒子模型是由 内容（content），边框（border），内边距（padding），和外边距（margin）四部分组成。
```

#### 边框
```txt
（1）.边框（border）是指围绕元素的内容和内边距的一条或多条线，通过border-top-style、border-right-style、border-bottom-style       和border-left-style四个属性对“上右下左”四个方向的边框样式分别进行设置，每
（2）.条边框又有宽度、颜色、样式和圆角等特征：)元素的边框的样式包括宽度、样式和颜色等
（3）.可以通过border-width、border-style和border-color属性对边框进行统一设置
（4）.可以通过border-top-width、border-top-style和border-top-color等属性对某一条边进行设置
```
**四个参数**上 左 下 右
**三个参数**上 （左+右） 下 
**两个参数** （上+下） （左+右）
**一个参数** （上下左右）

#####　border-style
|**值**|**描述**|
|------|------|
|none|无边框|
|hidden|隐藏边框|
|dotted|定义点状边框|
|dashed|定义虚线边框|
|solid|定义实线|
|double|双线|
|groove|3D凹槽|
|ridge|3D菱形边框|
|inset|3D凹边|
|outset|3D凸边|
|||
##### 边框阴影
```txt
边框阴影（box-shadow）可以为元素的边框添加一个或多个阴影
box-shadow的属性可以由2~6个参数构成
h-shadow用于指定水平阴影的位置，该值允许取负值
v-shadow用于指定垂直阴影的位置，该值允许取负值
blur用于指定模糊距离
spread用于指定阴影的尺寸
color用于指定阴影的颜色
inset用于将外部阴影（outset）改为内部阴影
```
##### 内边距padding
```txt
内边距（padding）是指内容区与边框之间的距离
通过padding-top、padding-right、padding-bottom和padding-left属性对元素的“上右下左”四个方向的内边距进行设置
通过padding属性可以在一个样式声明中设置该元素的所有内边距
```

| **值**         | **描 述**            |
| -------------- | -------------------- |
| padding-top    | 设置元素上面的内边距 |
| padding-right  | 设置元素右侧的内边距 |
| padding-bottom | 设置元素下面的内边距 |
| padding-left   | 设置元素左侧的内边距 |
| padding        | 简写属性             |

#####　外边距magin
```txt
元素与元素之间的距离，即围绕在元素边框之外的空白区域，通过外边距可以为元素创建额外的“空间”。
外边距与内边距相似，可以对“上下左右”四个外边距分别进行设定，也可以统一进行设定。
```

| **值**        | **描 述**            |
| ------------- | -------------------- |
| margin-top    | 设置元素上面的外边距 |
| margin-right  | 设置元素右侧的外边距 |
| margin-bottom | 设置元素下面的外边距 |
| margin-left   | 设置元素左侧的外边距 |
| margin        | 简写属性             |