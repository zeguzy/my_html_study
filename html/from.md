# form 表单

###功能：html 中的一个重要部分，负责采集用户和提交用户输入的信息
###分类：**表单标签** 和**表单控件** 两大类
1. 表单控件：表单域和按钮，常见的表单域:文本框，密码框，多行文本框，多行文本框，单选按钮，复选框，下拉选择框
2. 在表单域录入数据后，可通过表单的特殊控件（如提交按钮等）将数据传递给服务器端，由服务器接收表单数据并进行处理



**常见的服务器端语言有JSP、PHP、ASP.NET、NodeJS等**



### 表单标签

####是一个包含表单的区域可以包含表单控件和其他标签
**一个页面可以有多个表单标签  但是不能嵌套** 
**用户想服务器发送数据时一次只能提交一个表单中的数据** 
**需要同时提交多个标签的数据时需要用JavaScript中的异步交互方式来实现** 



| **属性**       | **描述**                                                                                   |
| -------------- | ------------------------------------------------------------                               |
| action         | 向谁提交                                                                                   |
| accept-charset | 服务器可处理的表单数据字符集                                                               |
| enctype        | 表单数据内容类型，可以为application/x-www-form-urlencoded、text/plain、multipart/form-data |
| id             | 表单对象的唯一标识符                                                                       |
| name           | 表单对象的名称                                                                             |
| target         | 打开处理URL的目标位置（不建议使用）                                                        |
| method         | 规定向服务器端发送数据所采用的方式，取值可以为get、post                                    |
| onsubmit       | 向服务器提交数据之前，执行其指定的JavaScript脚本程序                                       |
| onreset        | 重置表单数据之前，执行其指定的JavaScript脚本程序                                           |
---
#### get 和post的区别：get 将数据作为URL的一部分发送给服务器，URL与数据用? 数据与数据用&隔开  key=value  数据长度有限制  post：数据没有长度限制，因为post将数据隐藏在http数据流中进行传输，所以安全性高于get
### 表单域
#### 功能：多用于收集用户数据一般位于form标签里面
#### 包括：（主要）文本框 密码框 隐藏域 多行文本框 单选按钮 复选框 列表选择框 和文件选择框
**除了多行文本框和列表选择框外大部分表单域使用input标签创建** 

| **属性**  | **描述**                                                     |
| --------- | ------------------------------------------------------------ |
| id        | 设置当前控件的唯一ID，在界面设计时，CSS、JavaScript中可以引用 |
| name      | 设置当前控件的名称，在向服务器发送数据时，服务器根据name属性获取对应表单域的值 |
| value     | 设置表单域的初始值，网页加载过程中，默认显示该值             |
| type      | 该属性是必须的，用来说明当前控件的类型，取值可以是text、password、radio、checkbox、file、hidden、button、submit、reset、image等 |
| maxlength | 设置输入到文本框的最大字符数；输入达到最大数后，用户按下更多键，也不会添加新的字符 |
| size      | 设置文本输入控件的宽度，单位为字符                           |



##### 单行文本框 type=text
##### 密码选择框 type=password
##### 单选按钮   type=radio

| 属性                                                         | 描述                                         |
| ------------------------------------------------------------ | -------------------------------------------- |
| [accessKey](https://www.w3school.com.cn/jsref/prop_radio_accesskey.asp) | 设置或返回访问单选按钮的快捷键。             |
| [alt](https://www.w3school.com.cn/jsref/prop_radio_alt.asp)  | 设置或返回在不支持单选按钮时显示的替代文本。 |
| [checked](https://www.w3school.com.cn/jsref/prop_radio_checked.asp) | 设置或返回单选按钮的状态。                   |
| [defaultChecked](https://www.w3school.com.cn/jsref/prop_radio_defaultchecked.asp) | 返回单选按钮的默认状态。                     |
| [disabled](https://www.w3school.com.cn/jsref/prop_radio_disabled.asp) | 设置或返回是否禁用单选按钮。                 |
| [form](https://www.w3school.com.cn/jsref/prop_radio_form.asp) | 返回一个对包含此单选按钮的表单的引用。       |
| [id](https://www.w3school.com.cn/jsref/prop_radio_id.asp)    | 设置或返回单选按钮的 id。                    |
| [name](https://www.w3school.com.cn/jsref/prop_radio_name.asp) | 设置或返回单选按钮的名称。                   |
| [tabIndex](https://www.w3school.com.cn/jsref/prop_radio_tabindex.asp) | 设置或返回单选按钮的 tab 键控制次序。        |
| [type](https://www.w3school.com.cn/jsref/prop_radio_type.asp) | 返回单选按钮的表单类型。                     |
| [value](https://www.w3school.com.cn/jsref/prop_radio_value.asp) | 设置或返回单选按钮的 value 属性的值。        |

##### 复选框     type=checkbox
##### 文件选择框 type=file
##### 隐藏域     type=hidden
##### 多行文本框 **textarea标签**
##### 列表选择框 **select标签**
##### 按钮控件   type=submit|reset|button|image  提交按钮、重置按钮、图片按钮和普通按钮
##### 表单分组   fieldset标签可以看作表单的一个子容器，将所包含的内容以边框环绕方式显示 legend标签则是为fieldset边框添加相关的标题


