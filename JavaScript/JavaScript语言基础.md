# JavaScript语言基础


JavaScript是一种通用的，跨平台，**基于对象**和**事件驱动**的**客户端脚本语言**
```txt
特点：解释性
	 嵌套在HTML中
	 弱数据类型
	 跨平台
	 基于对象
	 基于事件驱动
```
```txt
规范：浏览器解析js脚步时会忽略空白字符
	 每条语句独占一行，以‘；’结束
	 代码要缩减，以增强层次感
```
```txt
JavaScript脚本不仅能嵌入到HTML页面中，还能以独立文件的形式进行存放。
在页面中使用JavaScript脚本的形式有以下三种：
     行内JavaScript脚本
     内部JavaScript脚本
     外部JavaScript脚本
```
#### 脚本的形式
##### 1.行内
```html
    <img src="images/girl3.jpg" onclick="alert('你选择了三号种子选手')"/>  
    <a href="javascript:alert('请等待评选结果，谢谢');">查看评选结果</a>  
```
##### 2.内部
```html
<head>
    <script type="text/javascript">
	alert("head中的JavaScript");
    </script>
</head>
 <body>
    <script type="text/javascript">
	alert("body中的JavaScript");
    </script> 
</body>
```
##### 3.外部脚本
```html
// test.js文件
alert("外部JavaScript脚本，导入成功。");
```
```html
<script type="text/javascript" src="js/test.js"></script>
```
#### JavaScript拥有有自身的数据类型、运算符、表达式及语法结构。

##### 标识符
```txt
标识符（identifier）用来命名变量、函数或循环中的标签，命名规范如下：
	 标识第一个字母必须是字母、下划线、或美元符号
	 标识符区分字母的大小写，推荐使用小写形式或骆驼命名法
	 标识符由数字、字母、下划线（_）、美元符号（$）构成
	 标识符不能与JavaScript中的关键字相同
```

```txt
合法的标识符				非法的标识符
 varName 			    Var Name      //包含空格；
 _varName			    9 varName     //以数字开头；
 var_Name			    a+b           //加号“+”不是字母和数字
 $varName
 _9Name
```
##### 关键字
```txt
关键字（Reserved Words）是指JavaScript中预先定义的、有特别意义的标识符。
而保留关键字是指一些关键字在JavaScript中暂时未用到，可能会在后期扩展时使用。
关键字或保留关键字都不能用作标识符（包括变量名、函数名等）。
```
##### 数据类型
```txt
在JavaScript中变量的类型可以改变，但某一时刻的类型是确定的
常见的数据类型有String，Boolean，Array，Bumber和Undefinded等类型
```

| **数据类型** | **描 述**                                                    |
| ------------ | ------------------------------------------------------------ |
| String       | 字符串是由双引号（"）或单引号（'）括起来的0~n个字符          |
| Boolean      | 布尔类型包括true和false两个值                                |
| Null         | 表明某个变量的值为null                                       |
| Undefined    | 当声明的变量未初始化时，默认值是undefined                    |
| Array        | 一系列变量或函数的集合，可以存放类型相同的数据，也可以存放类型不同的数据 |
| Number       | 数值类型可以是32位的整数，也可以是64位的浮点数；而整数可以是十进制、八进制或十六进制等形式 |
| Function     | 函数是一种特殊的对象数据类型，可以被存储在变量、数组或对象   |
| Object       | 通过属性和方法定义的对象；常见的对象有String、Date、Math和Array等 |
|||

##### 变量的定义
```txt
变量是程序存储数据的基本单位，用来保存程序中的数据。
变量名是标识符中的一种，应遵循标识符的命名规范。
```
在使用变量之前，可以通过关键字**var**对变量进行声明。
```js
var name,age;
var type="student";
var major="软件外包";
school="JSU软件学院";
```

##### 变量的类型
```txt
JavaScript中的变量时若数据类型；
在声明变量时不需要指明变量的数据类型，通过关键字var进行声明；
在变量的使用过程中变量的类型可以动态改变，类型由所赋的值确定；
通过typeof运算符或者typeof（）函数来获取变量当前的数句类型；
```

##### 变量的类型作用域
```txt
变量的作用域是指变量的有效范围，根据作用域变量可以分为全局变量和局部变量
	 （1）全局变量：定义在函数之外的变量或者未定义直接使用的变量
	 （2）局部变量：函数内部声明的变量，仅仅对当前函数体有效
```
**局部变量会覆盖与其同名的全局变量**
##### 注释
JavaScript有单行注释和多行注释
```txt
	// 单行注释
	/* 多行注释
	   多行注释*/
```
##### 运算符
```txt
	赋值
	算数
	比较
	逻辑
	三元
```

**= =与= = =的区别在于：**
```txt
 = = 支持自动类型转换，只要前后两个变量的值相同就返回true，而忽略数据类型的比较
 = = = 需要两个变量的值相同并且数据类型一致时才返回true
```

| **运算符** | **描 述**                                                    |
| ---------- | ------------------------------------------------------------ |
| >          | 大于，左侧的值大于右侧的值时，则返回true；否则返回false      |
| >=         | 大于等于，左侧的值大于等于右侧的值时，则返回true；否则返回false |
| <          | 小于，左侧的值小于右侧的值时，则返回true；否则返回false      |
| <=         | 小于等于，左侧的值小于等于右侧的值时，则返回true；否则返回false |
| !=         | 不等于，左侧与右侧的值不相等时，则返回true；否则返回false    |
| ==         | 等于，左侧与右侧的值相等时，则返回true；否则返回false        |
| !==        | 严格不等于，左侧与右侧的值不相等或数据类型不同时，返回true；否则返回false |
| ===        | 严格等于，左侧与右侧的值相等，并且数据类型相同时，返回true；否则返回false |
|||
**逻辑运算符**
```txt
逻辑运算符用于对布尔类型的变量（或常量）进行操作；
	 与（&&）：两个操作数同时为true时，结果为true；否则为false
	 或（||）：两个操作数中同时为false，结果为false；否则为true
	 非（！）：只有一个操作数，操作数为true，结果为false；否则结果为true
```
**三元运算符**
```txt
expression ? value1 : value2;
```
**流程控制**
```txt
流程控制是指通过控制程序执行的顺序，来完成一定的功能：
	 分支结构（if和switch）
	 循环结构（while、do while和for等）
	 break、continue、return等转移语句
```
```js
for in循环是JavaScript提供的一种特殊循环
        可以对字符串、数组、对象集合、对象属性等进行遍历
        
        但是这个东西部分浏览器支持不够好
        
for (property in object){
	statement;
}
```
**转移语句**
```txt
使用转移语句来控制程序的执行方向，包括break语句、continue语句和return语句。
（1）  break语句
	 在switch结构中，遇到break语句时，就会跳出switch分支结构
	 在循环结构中，遇到break语句时，立即退出循环，不再执行循环体中的任何代码



（2）continue语句
 	 当程序执行过程中遇到continue时，仅仅退出当前本次循环，
	 然后判断是否满足继续下一次循环的条件
```

**函数**
```txt
函数是一组延迟动作集的定义，可以在事件触发或在其他脚本中进行调用。
在JavaScript中，函数分为**预定义函数**和**用户定义函数**。
预定义函数是指JavaScript引擎中预先定义的內建函数，用户无需定义便可以直接使用 。
```

对象函数的定义

```txt
JavaScript还提供了Function类，用于定义函数，参数都是字符串，前面传参，最后为函数体
```

```JavaScript
var FunctionName = new Function([parameters],statements)
```

