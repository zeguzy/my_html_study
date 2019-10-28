# 框架frame

### 功能： 将浏览器界面划分成多个独立的窗格，每个窗格都有一个独立的HTML界面
### 优点： 用户可以加载或者重新加载单个界面而不需要加载浏览器窗口的全部内容
### 使用： 在HTML中用`<frameset>`划分界面使用rows（行数）cols（列数）说明frame所占的比例
```html
<frameset row="所占的行数或比例" cols="所占的列数或比例">
    <frame src="..."/>
    ...
</frameset>
```
### frameset 属性
| **属性**     | **描述**                                                     |
| ------------ | ------------------------------------------------------------ |
| rows         | 设置框架集中包含框架的行数，以及对应的高度                   |
| cols         | 设置框架集中包含框架的列数，以及对应的宽度                   |
| frameborder  | 设置框架集的边框是否显示，取值为1、0或yes、no，边框本身不能调整宽度 |
| bordercolor  | 设置框架集的边框的颜色                                       |
| framespacing | 框架与框架间的空白距离                                       |
### frame 属性
| **属性**     | **描述**                                                                                      |
|--------------|-----------------------------------------------------------------------------------------------|
| name         | 设置框架的名称用于标记                                                                        |
| src          | 设置显示界面的URL                                                                             |
| frameborder  | 设置frame边框是否显示取值0或1                                                                 |
| marginheight | 定义内容与框架的上下边缘高度，默认为1，frame，设置2独立本地页面观察效果，例如f1.html和f2.html |
| marginwedth  | 定义内容与框架的左右边缘宽度，默认为1，frame，设置2独立本地页面观察效果，例如f1.html和f2.html |
| scrolling    | 滚动条，yes no auto frame                                                                     |
| noresize     | 设置frame是否可调默认1                                                                        |


# 内联框架

## 优点: 语法更简洁 ，使用更灵活（不需要frameset标签包裹）直接iframe
```html
    <iframe src="......" name="..." width="..." heigth="..."></iframe>
```

| **属性**     | **描述**                                                     |
| ------------ | ------------------------------------------------------------ |
| align        | 设置iframe与周围文本对齐方式，取值可以是left、right、top、middle、bottom |
| frameborder  | 设置iframe的边框是否显示，取值0或1                           |
| marginheight | 定义iframe的顶部和底部的边距                                 |
| marginwidth  | 定义iframe的左侧和右侧的边距                                 |
| height       | 设置iframe的高度                                             |
| width        | 设置iframe的宽度                                             |
| scrolling    | 设置iframe中是否显示滚动条，取值yes、no、auto                |
| src          | 设置iframe中显示页面的URL                                    |
| name         | 设置iframe的名称                                             |