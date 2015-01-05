javascript
==========

## 1 应该知道
JavaScript 是世界上最流行的编程语言。	
这门语言可用于 HTML 和 web，更可广泛用于服务器、PC、笔记本电脑、平板电脑和智能手机等设备。
### 1.1 日常用途
1. 嵌入动态文本于HTML页面。
2. 对浏览器事件做出响应。
3. 读写HTML元素。
4. 在数据被提交到服务器之前验证数据。
5. 检测访客的浏览器信息。
6. 控制cookies，包括创建和修改等。
7. 基于Node.js技术进行服务器端编程。  
   
### 1.2 组成部分				
ECMAScript，描述了该语言的语法和基本对象。	
文档对象模型（DOM），描述处理网页内容的方法和接口。	
浏览器对象模型（BOM），描述与浏览器进行交互的方法和接口。   
 
## 2 开始
### 2.1 JavaScript导论 
JavaScript是一种脚本语言，其源代码在发往客户端运行之前不需经过编译，而是将文本格式的字符代码发送给浏览器由浏览器解释运行。  
直译语言的弱点是安全性较差，而且在JavaScript中，如果一条运行不了，那么下面的语言也无法运行。而其解决办法就是于使用`try{}catch(){}`︰		
![Image of trycatch]		
(https://github.com/sammulyuan/javascript/blob/master/trycatch.png)  

1. Javascript被归类为直译语言，因为目前主流的引擎都是每次运行时加载代码并解译。		
2. V8是将所有代码解译后再开始运行，其他引擎则是逐行解译（SpiderMonkey会将解译过的指令暂存，以提高性能，称为实时编译），但由于V8的核心部份多数用Javascript撰写（而SpiderMonkey是用C++），因此在不同的测试上，两者性能互有优劣。		
3. 与其相对应的是编译语言，例如C语言，以编译语言编写的程序在运行之前，必须经过编译，将代码编译为机器码，再加以运行。  
             
### 2.2 基本特点 

1. 是一种解释性脚本语言（代码不进行预编译）。
2. 主要用来向HTML（标准通用标记语言下的一个应用）页面添加交互行为。
3. 可以直接嵌入HTML页面，但写成单独的js文件有利于结构和行为的分离。
4. 跨平台特性，在绝大多数浏览器的支持下，可以在多种平台下运行（如Windows、Linux、Mac、Android、iOS等）。  
      
### 2.3 了解工具和应用

- TestSwarm：是Mozilla实验室推出的一个开源项目，它旨在为开发者提供在多个浏览器版本上快速轻松测试自己JavaScript代码的方法。
- Minimee：在网络上，速度是很重要的，Minimee能帮助你将CSS和JavaScript文件进行自动压缩和打包。
- Doctor JS：Doctor JS 是一款帮你分析 JavaScript 代码的工具，测试你的代码在多态、原型、异常和回调方面写得怎么样。
- Remy Sharp’s JSConsole：一个在线的 JavaScript 控制台工具，对于测试、调试和演示非常有用。
- JavaScript Library Boilerplate：JavaScript Library Boilerplate 帮助你随时随地创建自己的 JavaScript 库。
- Jsdoc-toolkit：JsDoc Toolkit 是一款辅助工具，你只需要根据约定在 JavaScript 代码中添加相应的注释，它就可以根据这些注释来自动生成API文档。
- Jasmine  BDD for your JavaScript：Jasmine 是一个有名的javascript单元测试框架，它是独立的“行为驱动开发”框架。
- ObfuscateJS: JavaScript compressor：一款 JavaScript 混淆工具，去除空白和注释，重命名变量等。
- PEG.js：PEG.js 是一个JavaScript的表达式语法解析器，它使您能够轻松地建立复杂的数据或计算机程序语言的快速分析器。
- JSONView：JSONView 是一款帮助你在浏览器中查看JSON文档的Firefox插件。
- JSonduit：JSonduit 是一个将网页内容转换为 JSON 格式订阅器的工具。
- Jsplumb：JsPlumb 为开发者提供了可视化链接元素到页面的方法，可以结合jQuery、MooTools 和 YUI3使用。
- Helma:Helma 是一个用来开发快速、稳定的Web应用程序的开源框架，它使用JavaScript 来作为服务端脚本环境，从而可以省略编译周期。
- HTML + JSON Report：一款将 JSON 数据转换为可读性更高的HTML格式内容的在线工具。
- JSON Editor：这个编辑器可以帮助你方便的编辑 JSON 字符串。

## 3 JavaScript核心语法
### 3.1 了解JavaScript代码的结构
- 通过在网页或工具中加入`<Script>…</Script>`标记JavaScript的开始和结束，将JavaScript代码放到`<Script>…</Script>`之间：

```
<SCRIPT LANGUAGE="JavaScript">
   <!--
     ......
   //-->
</SCRIPT>	                 
```		

（其中<!- - 和 - -> 标记，它为那些不支持 JavaScript 的浏览器提供了一个忽略它的方法，而 // 标记是一段注释的开始 ）		

也可以引入一个外部的JavaScript文件，外部文件通常包含被多个网页使用的代码，这个JavaScript文件一般以*.js作为扩展名，如需使用外部文件，请在 `<script> `标签的 `"src" `属性中设置该 .js 文件:

```
<SCRIPT LANGUAGE=“JavaScript” SRC=“*.js">
    ......
</SCRIPT>
```	

- 原则上，放在`<head></head>`和`<body></body>`之间。但视情况可以放在网页的任何部分；
- 一个页面可以有几个`<Script>…</Script>` ，不同部分的方法和变量，可以共享。

### 3.2 JavaScript基本 

1. JavaScript是一门弱类型的语言，所有的变量定义均以var来实现
2. JavaScript的变量必需先定义，再使用
3. 在JavaScript中区分大小写，变量名是大小写敏感的，还需注意它必须以字母或下划线开始。 
  
### 3.3 JavaScript 创建变量 

1. JavaScript 变量与代数一样，JavaScript 变量可用于存放值（比如 x=2）和表达式（比z=x+y）。
	1. 变量可以使用短名称（比如 x 和 y），也可以使用描述性更好的名称（比如 age, sum，totalvolume）。
	2. 变量必须以字母开头
    3. 变量也能以 $ 和 _ 符号开头（不过我们不推荐这么做）
    4. 变量名称对大小写敏感（y 和 Y 是不同的变量）  
    
	*提示：JavaScript 语句和 JavaScript 变量都对大小写敏感。*		
	虽然JavaScript可以不需定义即可直接使用变量，但不建议这么做。
2. 变量的作用范围：

 	1. 在一个函数（function）之外定义一个变量，那它叫作全局变量
	2. 在 function 内部定义的变量则叫局部变量，它只作用于函数内
	
**声明（创建）JavaScript 变量**

在 JavaScript 中创建变量通常称为“声明”变量。
		
- 使用 var 关键词来声明变量：`var name`;		
- 变量声明之后，该变量是空的（它没有值）。如需向变量赋值，请使用等号：`carname=“Hello"`;	
- 也可以在声明变量时对其赋值：`var name=“Hello”`；	
- 一条语句，多个变量:语句以 var 开头，并使用逗号分隔变量即可：`var name="Hello", age=22, job="CEO"`;
- 声明也可横跨多行：

```javascript				
var name="Hello",		
age=22，		
job="CEO";
```
- 在计算机程序中，经常会声明无值的变量。未使用值来声明的变量，其值实际上是 undefined。
- 在执行过以下语句后，变量 name 的值将是 undefined：`var name`;

3. 重新声明 JavaScript 变量		
如果重新声明 JavaScript 变量，该变量的值不会丢失：	
在以下两条语句执行后，变量 name 的值依然是 “Hello"：	

```javascript
var carname="Volvo";		
var carname;
```

### 3.4 JavaScript 运算符    
### 3.5 JavaScript 比较         
### 3.6 JavaScript 条件语句和循环
#### 3.6.1 JavaScript If...Else
#### 3.6.2 JavaScript switch 语句
#### 3.6.3 JavaScript for 循环
#### 3.6.4 JavaScript while 循环
#### 3.6.5 JavaScript Break 和 Continue 语句
### 3.7 JavaScript函数和创建函数
#### 3.7.1 了解函数的用途
#### 3.7.2 JavaScript 函数定义
#### 3.7.3 JavaScript 函数参数
#### 3.7.4 带返回值的函数
#### 3.7.5 局部变量和全局变量
#### 3.7.6 JavaScript 函数调用
#### 3.7.7 JavaScript 闭包
### 3.8 JavaScript 输出
### 3.9 JavaScript 语句
### 3.10 JavaScript 数据类型
### 3.11 JavaScript 注释
### 3.12 JavaScript 保留字关键字
### 3.13 JavaScript 验证
## 4 类型和对象
### 4.1 什么是对象
### 4.2 JavaScript Number 对象
### 4.3 JavaScript Array（数组）
### 4.4 JavaScript String
### 4.5 JavaScript Date（日期）
### 4.6 JavaScript Boolean（布尔）
### 4.7 JavaScript Math（算数）
### 4.8 JavaScript RegExp 对象
## 5 理解JavaScript HTML DOM
### 5.1 DOM 简介
### 5.2 DOM HTML
### 5.3 DOM CSS
### 5.4 DOM 元素
## 6 JS 浏览器BOM
### 6.1 JavaScript Window
### 6.2 JavaScript Window Screen
### 6.3 JavaScript Window Location
### 6.4 JavaScript Window History
### 6.5 JavaScript Navigator
### 6.6 JavaScript 弹窗
### 6.7 JavaScript 计时事件
### 6.8 JavaScript Cookies
## 7 事件和事件监听
### 7.1 JavaScript事件处理（DOM 事件）
### 7.2 JavaScript异常处理
### 7.3 onClick 和 onLoad
### 7.4 DOM 事件监听
## 8 JavaScript 调试
### 8.1. Firebug
## 9 创建智能化表单
### 9.1 访问表单元素
### 9.2 表单提交
### 9.3 隐藏和显示表单
## 10 JavaScript 库
### 10.1 JavaScript库的介绍
### 10.2 JavaScript jQuery
### 10.3 JavaScript Prototype
### 10.4 JavaScript MooTools
### 10.5 JavaScript AJAX的使用
## 11 JavaScript 实例
### 11.1 JavaScript 对象实例
### 11.2 JavaScript 浏览器对象实例
### 11.3 JavaScript HTML DOM 实例
### 11.4 JavaScript 总结
