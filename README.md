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
**ECMAScript，**描述了该语言的语法和基本对象。	
**文档对象模型（DOM），**描述处理网页内容的方法和接口。			
**浏览器对象模型（BOM），**描述与浏览器进行交互的方法和接口。   
 
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

- **TestSwarm：**是Mozilla实验室推出的一个开源项目，它旨在为开发者提供在多个浏览器版本上快速轻松测试自己JavaScript代码的方法。
- **Minimee：**在网络上，速度是很重要的，Minimee能帮助你将CSS和JavaScript文件进行自动压缩和打包。
- **Doctor JS：**Doctor JS 是一款帮你分析 JavaScript 代码的工具，测试你的代码在多态、原型、异常和回调方面写得怎么样。
- **Remy Sharp’s JSConsole：**一个在线的 JavaScript 控制台工具，对于测试、调试和演示非常有用。
- **JavaScript Library Boilerplate：**JavaScript Library Boilerplate 帮助你随时随地创建自己的 JavaScript 库。
- **Jsdoc-toolkit：**JsDoc Toolkit 是一款辅助工具，你只需要根据约定在 JavaScript 代码中添加相应的注释，它就可以根据这些注释来自动生成API文档。
- **Jasmine  BDD for your JavaScript：**Jasmine 是一个有名的javascript单元测试框架，它是独立的“行为驱动开发”框架。
- **ObfuscateJS: JavaScript compressor：**一款 JavaScript 混淆工具，去除空白和注释，重命名变量等。
- **PEG.js：**PEG.js 是一个JavaScript的表达式语法解析器，它使您能够轻松地建立复杂的数据或计算机程序语言的快速分析器。
- **JSONView：**JSONView 是一款帮助你在浏览器中查看JSON文档的Firefox插件。
- **JSonduit：**JSonduit 是一个将网页内容转换为 JSON 格式订阅器的工具。
- **Jsplumb：**JsPlumb 为开发者提供了可视化链接元素到页面的方法，可以结合jQuery、MooTools 和 YUI3使用。
- **Helma:** Helma 是一个用来开发快速、稳定的Web应用程序的开源框架，它使用JavaScript 来作为服务端脚本环境，从而可以省略编译周期。
- **HTML + JSON Report：**一款将 JSON 数据转换为可读性更高的HTML格式内容的在线工具。
- **JSON Editor：**这个编辑器可以帮助你方便的编辑 JSON 字符串。

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
    
> 提示：JavaScript 语句和 JavaScript 变量都对大小写敏感。		
虽然JavaScript可以不需定义即可直接使用变量，但不建议这么做。
2. 变量的作用范围：
 	1. 在一个函数（function）之外定义一个变量，那它叫作全局变量
	2. 在 function 内部定义的变量则叫局部变量，它只作用于函数内
	
**声明（创建）JavaScript 变量**

在 JavaScript 中创建变量通常称为“声明”变量。
		
- **使用 var 关键词来声明变量：**`var name`;		
- 变量声明之后，该变量是空的（它没有值）。如需向变量赋值，请使用等号：`carname=“Hello"`;	
- **也可以在声明变量时对其赋值：**`var name=“Hello”`；	
- **一条语句，多个变量：**语句以 var 开头，并使用逗号分隔变量即可：`var name="Hello", age=22, job="CEO"`;
- **声明也可横跨多行：**		
例：

```javascript				
var name="Hello",		
age=22，		
job="CEO";
```
- 在计算机程序中，经常会声明无值的变量。未使用值来声明的变量，其值实际上是 undefined。
- 在执行过以下语句后，变量 name 的值将是 undefined：`var name`;

**重新声明 JavaScript 变量**		
如果重新声明 JavaScript 变量，该变量的值不会丢失：	
在以下两条语句执行后，变量 name 的值依然是 “Hello"：	

例：	

```javascript
var carname="Volvo";		
var carname;
```

### 3.4 JavaScript 运算符  
**JavaScript算数运算符**		

运算符 | 描述  | 标注 | 例子 | 结果		 
------  | ------ | ------ | ----- | ------	
+ | 加 | 二元运算符，返回操作数相加结果 | 2+3 | 5
- | 减 | 二元运算符，返回操作数相减结果 | 3-2 | 1
* | 乘 | 二元运算符，返回操作数相乘结果 | 2*3 | 6
/ | 除 | 二元运算符，返回操作数相除结果 | 9/3 | 3
% | 取余 | 二元运算符，返回整数除法的余数 | 12%5 | 2
++ | 累加 | 一元运算符，操作对象加一；如果是x++返回增量后的值；如果是++x返回增量前的值 | 例：x=3	| x=x++=4		x=++x=3
-- | 递减 | 同上面，操作对象递减1| 例：x=3	| x=x--=3		x=--x=2

**JavaScript 赋值运算符**		

是将右边的操作数赋予左边的操作对象，如 x=y 为将 y 赋予 x。

给定 x=10 和 y=5，下面的表格解释了赋值运算符：

运算符 | 例子 |  等价于 |  结果
----- | ---- | ----- | -----
= |  x=y | |  x=5
+= | x+=y | x=x+y | x=15
-= | x-=y | x=x-y | x=5
*= | x*=y | x=x*y | x=50
/= | x/=y | x=x/y | x=2
%= | x%=y | x=x%y | x=0
^= | x^=y | x=x^y按位异或，不同为1，true，相同为0，false | x=15

**JavaScript 字符串运算符**		
用于字符串值连结的运算符（+）将两个字符串值连结在一起。		
例如：“我的”+“计算机”就返回“我的计算机”		
如果把数字与字符串相加，结果将成为字符串。		
例：			
```
txt1="What a very";
txt2="nice day";
txt3=txt1+txt2;
txt3 包含的值是 "What a verynice day"。
```
要想在两个字符串之间增加空格，需要把空格插入一个字符串之中：		
例：		
```
txt1="What a very ";
txt2="nice day";
txt3=txt1+txt2;
```
或者把空格插入表达式中：		
例：		
```
txt1="What a very";
txt2="nice day";
txt3=txt1+" "+txt2;
```
在以上语句执行后，变量 txt3 包含的值是："What a very nice day"

- 取子集函数：`substring(index1,index2)`		
- 取长度属性：`length`		
- 取字符串中的某一个字符的函数：`charAt(index)`
- 查找字符在字符串中的位置：(函数要注意大小写)		
	从左往右找`indexOf(string)`		
    从右往左找`lastIndexOf(string)`
          
### 3.5 JavaScript 比较  		
**JavaScript 比较运算符**		
比较它的操作对象并返回一个逻辑值（true 或 false）。	
操作对象即可以是数字也可以是字符串值。		
给定 x=1 和 y=2，下面的表格解释了比较运算符： 
	
运算符 | 描述 | 标注 | 实例 | 结果 		
----- | ---- | --- | ---- | ----   
== | 等号 | 如果操作对象相等返回true，如果两个操作对象不为同一类型，javascript尝试转换它们为一个适当的类型 | 3 == x  	“3”== y	3== ‘3’ | false false true  
!= | 不等于 | 同上面相反，两个操作水箱不相等返回true | x!= 4	y != 2 | true	false
=== | 绝对相等 | 如果操作对象相等并且类型相等返回true | 3===‘3’	x===1 | false	true
!== | 绝对不等 | 同上面相反，如果操作对象或不是同一类型返回true | 3!==  ‘3’	 x!== 1 | true	false
\> | 大于 | 如果左边的操作对象大于右边操作对象返回true | x > y | false
\>= | 大于或等于 | 如果左边的操作对象大于或等于右边的操作对象返回true | y >= x | true
< | 小于 | 如果左边的操作对象小于右边操作对象返回true | x < y | true
<= | 小于或等于 | 如果左边的操作对象小于或等于右边的操作对象返回true | y <= x | false
		
**JavaScript 逻辑运算符**		
返回一个布尔值	
	
运算符 | 用法 | 描述		
----- | --- | ----		
&& | 表达式1&&表达式2 | 逻辑与，如果两个表达式都为真，&&返回true，否则返回false
\|\| | 表达式1\|\|表达式2 | 逻辑或，如果两个表达式都为真，\|\|返回true，其中一个表达式为真，\|\|返回true，否则返回false

**JavaScript 特殊运算符：条件运算符**

其语法为：条件?A:B			
如果条件为真，结果值为 A，否则为 B	
例：			
```
name=(age==“22”)?"Jessica":"Dear ";		
如果变量 age 中的值是 “22"，则向变量 name 赋值 "Jessica "，否则赋值 "Dear"。
```
**运算符的优先级**		
是复合运算进行计算时的先后顺序，对于所有的二元运算都是从左到右进行计算，用圆括号来忽略优先级：

![Image of youxianji]		
(https://github.com/sammulyuan/javascript/blob/master/youxianji.png)

### 3.6 JavaScript 条件语句和循环
#### 3.6.1 JavaScript If...Else

- **If 语句：**只有当指定条件为 true 时，该语句才会执行代码。

```
if (条件)
{
    只有当条件为 true 时执行的代码
}
注意：请使用小写的 if。使用大写字母（IF）会生成 JavaScript 错误！
```
- **If...else 语句：**如果条件为 true，则执行 if 段语句，若为 false 则执行 else 段语句，用法如下：

```
if (条件) {
      当条件为 true 时执行的代码
}else {
      当条件不为 true 时执行的代码
} 
```

> 条件可以是任何结果值为 true 或 false 的 JavaScript 表达式，语句可以是任何可执行的 JavaScript 语句	
		
它还可以任意层地被嵌套，如果条件语句后面是单条语句，那么就不需要大括号 {}。请看下例代码：
例：		
```javascript
<SCRIPT>
function checkData () {
if (document.form1.three.value.length == 3)
    alert("OK!");
else {
    alert("请输入三个字符，" + document.form1.three.value + "无效！");
    return false；
}
</SCRIPT>
<form name="form1"><center>
<input type="text" name="three" onChange="checkData()">
</center>
</form>
```

- **If...else if...else 语句：**使用 if....else if...else 语句来选择多个代码块之一来执行

```
 if (条件 1)
{
   当条件 1 为 true 时执行的代码
}
else if (条件 2)
{
   当条件 2 为 true 时执行的代码
}
else
{
   当条件 1 和 条件 2 都不为 true 时执行的代码
}
```

#### 3.6.2 JavaScript switch 语句

- **switch 语句：**switch 语句允许程序给表达式求值，并用 case 标记来匹配表达式可能的值；如果匹配成立，程序将执行相应的语句，用法如下：

```
switch (表达式){
case : 语句;
	break;
case : 语句;
	break;
...
default : 语句;
}
```

- **通过 switch 语句执行流程如下：**
	1. 求表达式的值并依次序查看 case，直到找到一个匹配；
	2. 如果 case 的值等于表达式的值，则执行它相应的语句；继续执行，直到遇到一个 break 语句，或者 switch 语句结束。		
这意味着如果没有使用一个 break 语句，则多个 case 块被执行。
	3. 如果没有 case 等于表达式的值，则跳转到 default；如果没有 default 情况，则跳转到最后一步；继续执行紧接 switch 代码块末尾的语句。
	
例：			
```	javascript
var day=new Date().getDay();					
switch (day){					
case 0:					
   x="Today it's Sunday";			
   break;			
case 1:			
   x="Today it's Monday";			
   break;			
case 2:			
   x="Today it's Tuesday";			
   break;			
case 3:			
   x="Today it's Wednesday";		
   break;			
case 4:				
   x="Today it's Thursday";				
   break;			
case 5:			
   x="Today it's Friday";			
   break;			
case 6:			
   x="Today it's Saturday";			
   break;			
}			
```

#### 3.6.3 JavaScript for 循环

- **for 语句：**一个 for 语句进行循环直到条件为 false，用法如下：

```
for ([初始表达式]; [条件]; [增量表达式]) {
     被执行的代码块；
}
```
**初始表达式：** 在循环（代码块）开始前执行，该表达式只在执行循环前被执行一次；	
	
> 初始表达式是可选的，也就是说不使用也可以，可以在初始表达式中初始化任意（或者多个）值		
								
**条件：** 定义运行循环（代码块）的条件，是一个 Boolean 表达式；如果是 true，则语句被执行，如果为 false，则循环结束；	
	
> 如果省略了条件，那么必须在循环内提供 break。否则循环就无法停下来。这样有可能令浏览器崩溃	

**增量表达式：** 在循环（代码块）已被执行之后执行；
	
> 增量表达式也是可选的。增量可以是负数 (i--)，或者更大 (i=i+15)。可以省略（比如当循环内部有相应的代码时）	
	
**被执行的代码块：** 为 true 时，要执行的语句，它可以是复合(多条)语句。				
例：

```javascript
myarray = new Array();
for (i = 0; i < 10; i++)
{
    myarray[i] = i;
}
```

- **For/In 循环：**JavaScript for/in 语句循环遍历对象的属性：

例:
```javascript
var person={fname:"John",lname:"Doe",age:25};
for (x in person)
{
    txt=txt + person[x];
}
```

#### 3.6.4 JavaScript while 循环

- **while 循环：**While 循环会在指定条件为真时循环执行代码块，执行一个语句，直到指定的条件为 false。

```
while (条件)
{
   需要执行的代码
}
```

> 该语句与 do...while 语句不同的是，它将在语句执行开始检查条件是否为 true，如是 false，它将根本不会执行下面的语句

- **do...while 语句：**do/while 循环是 while 循环的变体。该循环会执行一次代码块，在检查条件是否为真之前，然后如果条件为真的话，就会重复这个循环。用法如下：

```
do {
    需要执行的代码;
} while (条件)
```

> 首先执行一个语句块，然后重复循环的执行该语句块，直到条件表达式等于 false

#### 3.6.5 JavaScript Break 和 Continue 语句
- **break 语句：**可用于跳出循环		
break 语句跳出循环后，会继续执行该循环之后的代码（如果有的话）

例:
```javascript
for (i=0;i<10;i++)
{
  if (i==3) break;
  x=x + "The number is " + i + "<br>";
}
```

- **Continue 语句：** continue 语句中断循环中的迭代，如果出现了指定的条件，然后继续循环中的下一个迭代。 

例:
``` javascript
<script>		
function myFunction(){		
	var x="",i=0;		
	for (i=0;i<10;i++){		
		if (i==5){		
		continue;		
	}		
	x=x + "The number is " + i + "<br>";		
	}			
}		
</script> 		
```
输出后会跳过5执行		
**continue 语句**（带有或不带标签引用）只能用在循环中。	
**break 语句**（不带标签引用），只能用在循环或 switch 中。	
> 通过标签引用，break 语句可用于跳出任何 JavaScript 代码块

### 3.7 JavaScript函数和创建函数
#### 3.7.1 了解函数的用途
函数是由事件驱动的活着当它被调用时执行的可重复使用的代码块。
#### 3.7.2 JavaScript 函数定义
在JavaScript中使用函数时，必须先定义这个函数，然后才能对这个函数进行调用。下面先介绍函数的定义方式：

```
function 函数名（参数列表）
{
    代码块
}
利用function来定义一个函数
```

- **函数名：**调用函数时通过函数名进行调用。		
对于函数的命名，一般应该使用能够描述函数功能的单词进行描述，往往也可以使用多个单词组合进行命名，这样能够提高脚本的可读性。
- **参数列表：**参数列表是可选的，在必要的时候；可以使用参数列表向函数传递一些参数，以便在函数中可以使用这些参数。
- **代码块：**代码块中的代码包含在一对大括号中，通过代码块的执行完成函数的功能，如果需要返回一个值给调用函数的语句，应该在代码块中使用return语句。

#### 3.7.3 JavaScript 函数参数

- **调用带参数的函数：**在调用函数时，可以向其传递值，这些值被称为参数。	
这些参数可以在函数中使用。可以发送任意多的参数，由逗号 (,) 分隔：
`myFunction(argument1,argument2)`		
当您声明函数时，请把参数作为变量来声明：

```
function myFunction(var1,var2)
{
   这里是要执行的代码
}
```		
变量和参数必须以一致的顺序出现。第一个变量就是第一个被传递的参数的给定的值，以此类推。
#### 3.7.4 带返回值的函数

- 在使用 return 语句时，函数会停止执行，并返回指定的值。

```javascript
function myFunction()
{
   var x=5;
   return x;
}
```
上面的函数会返回值 5。	
	
> 注释：整个 JavaScript 并不会停止执行，仅仅是函数。JavaScript 将继续执行代码，从调用函数的地方。

#### 3.7.5 局部变量和全局变量

- **局部 JavaScript 变量**	
在 JavaScript 函数内部声明的变量（使用 var）是局部变量，所以只能在函数内部访问它（该变量的作用域是局部的）。			
可以在不同的函数中使用名称相同的局部变量，因为只有声明过该变量的函数才能识别出该变量。			
只要函数运行完毕，本地变量就会被删除。
- **全局 JavaScript 变量**	
在函数外声明的变量是全局变量，网页上的所有脚本和函数都能访问它。
- **JavaScript 变量的生存期**
JavaScript 变量的生命期从它们被声明的时间开始。		
**局部变量会在函数运行以后被删除。**		
**全局变量会在页面关闭后被删除。**	
	
如果把值赋给尚未声明的变量，该变量将被自动作为全局变量声明。这条语句：`carname="Volvo";`		
将声明一个全局变量 carname，即使它在函数内执行。

#### 3.7.6 JavaScript 函数调用
函数在定义好之后，不能自动执行，需要进行调用		
调用方式：		
1. 在`<script>`标签内调用  
例：		
```javascript
<script>
function demo(){
   var a=10;
   var b=20;
   var sum=a+b;
   alert(sum);
}
demo();//调用函数
</script> 
```		
2. 在HTML文件中调用

例：		
```javascript
<form>
<input type=“button” value=“按钮” onclick=“demo()”>
</form>
或<button onclick=“demo()”>按钮</button>
```
#### 3.7.7 JavaScript 闭包
**解释：** 一个拥有许多变量和绑定了这些变量的环境的表达式（通常是一个函数），因而这些变量也是该表达式的一部分。		
**闭包的特点：**
		
1. 作为一个函数变量的一个引用，当函数返回时，其处于激活状态。	
2. 一个闭包就是当一个函数返回时，一个没有释放资源的栈区。

**原因：**javascript允许使用内部函数---即函数定义和函数表达式位于另一个函数的函数体内。而且，这些内部函数可以访问它们所在的外部函数中声明的所有局部变量、参数和声明的其他内部函数。		
当其中一个这样的内部函数在包含它们的外部函数之外被调用时，就会形成闭包。	
	
例：		
```javascript
function closure(){
    var str = "I'm a part variable.";
    return function(){
    alert(str);
    }
}
var fObj = closure();
fObj();
```		
在上面代码中，str是定义在函数closure中局部变量，若str在closure函数调用完成以后不能再被访问，则在函数执行完成后str将被释放。	
但是由于函数closure返回了一个内部函数，且这个返回的函数引用了str变量，导致了str可能会在closure函数执行完成以后还会被引用，所以str所占用的资源不会被回收。这样closure就形成了一个闭包。
### 3.8 JavaScript 输出
可以使用 `document.getElementById(id)` 方法从 JavaScript 访问某个 HTML 元素；	
	
- 通过指定的 id 来访问 HTML 元素，并改变其内容：			
例：		
```javascript		
<!DOCTYPE html>
<html>
<body>
<h1>My First Web Page</h1>
<p id="demo">My First Paragraph</p>
<script>
document.getElementById("demo").innerHTML="My First JavaScript";
</script>
</body>
</html>
```

- 直接把 `<p>`元素写到 HTML 文档输出中：				
例：		
```javascript		
<!DOCTYPE html>
<html>
<body>
<h1>My First Web Page</h1>
<script>
document.write("<p>My First JavaScript</p>");
</script>
</body>
</html>
```	
	
> 注意：document.write() 仅仅向文档输出写内容，如果在文档已完成加载后执行 document.write，整个 HTML 页面将被覆盖。

### 3.9 JavaScript 语句

JavaScript 语句向浏览器发出的命令，语句的作用是告诉浏览器该做什么；	
	
- **分号** 		
用于分隔 JavaScript 语句。		
通常我们在每条可执行的语句结尾添加分号。		
使用分号的另一用处是在一行中编写多条语句。
		
> 提示：也可能看到不带有分号的案例，在 JavaScript 中，用分号来结束语句是可选的。
	
- **JavaScript 代码**
JavaScript 代码（或者只有 JavaScript）是 JavaScript 语句的序列。浏览器会按照编写顺序来执行每条语句。		
- **JavaScript 代码块**		
JavaScript 语句通过代码块的形式进行组合。		
块由左花括号开始，由右花括号结束。块的作用是使语句序列一起执行。	
> JavaScript 函数是将语句组合在块中的典型例子。

- **空格**		
JavaScript 会忽略多余的空格。你可以向脚本添加空格，来提高其可读性。
- **对代码行进行折行**		
可以在文本字符串中使用反斜杠对代码行进行换行。		
注意：这样不可以 

		document.write \
		("Hello World!");
		
### 3.10 JavaScript 数据类型

1. **整数类型**		
一个整数可以是十进制、十六进制和八进制数，一个十进制数由一串数字序列组成，它的第一个数字不能为0；如38，-25，+120，74286等都是十进制整数。		
如果第一个数字为0，则表示它是一个八进制数；如0，012，0377，04056等都是八进制整数，对应的十进制整数依次为0，10，255和2094。		
若为0x，则表示它为一个十六进制数；如0x0，0X25，0x1ff，0x30CA等都是十六进制整数，对应的十进制整数依次为0，37，511和4298。
2. **浮点数类型**		
浮点数的例子：
`3.1415,  -3.1E12,  0.1e12 和 2E-12`	
一个浮点数必须包含一个数字，一个小数点或“e”（或“E”）。
3. **布尔类型**		
Boolean 类型有两种值：true 和 false
4. **字符串类型**		
字符串是若干封装在双引号（“）或单引号（'）内的字符。如下：	
`
"fish"
'fish'
"5467"
"a line"
`		
可以在字符串中使用引号，只要不匹配包围字符串的引号即可：
`"He is called 'Bill'";`

5. **对象类型**		
用new声明一个新的对象			
例：
	
		var currentDay = new Date();		
		alert(currentDay.getDay());
对象由花括号分隔。在括号内部，对象的属性以名称和值对的形式 `(name : value)`来定义。属性由逗号分隔：		
例：

		var person={firstname:"Bill", lastname:"Gates", id:5566};
空格和折行无关紧要。声明可横跨多行：		
例：

		var person={
		firstname : "Bill",
		lastname  : "Gates",
		id        :  5566
		};
对象属性有两种寻址方式：		
例：

		name=person.lastname;
		name=person["lastname"];
		
6. Undefined 和 Null		
Undefined 这个值表示变量不含有值。		
可以通过将变量的值设置为 null 来清空变量。	
	
7. 数组类型
例：	
	
		var arr = new Array(3);
通过arr.length取得数组的长度


> 注意： JavaScript 变量均为对象。当您声明一个变量时，就创建了一个新的对象。

### 3.11 JavaScript 注释
- 单行注释以 // 开头。
- 多行注释以 /* 开始，以 */ 结尾。

### 3.12 JavaScript 保留字关键字
- **关键字：** 在javascript中，根据规定，关键字是保留的，不能用作变量名或函数名。

break | delete | function | return | type
----- | ---- | --- | ---- | ---- 
case | do | if | switch | var
catch | else | in | this | void
continue | finally | instance of | throw | while
default | for | new | try | with


- **保留字：** 保留字在某种意义上是为将来的关键字而保留的单词。因此保留字不能被用作变量名或函数名。
 
abstract | debugger | final | int | private | super
----- | ---- | --- | ---- | ---- | -----
boolean | double | float | interface | protected |synchronize
byte | enum | goto | long | public | throws
char | export | implements | native | short | transient
class | extends | import | package | static | volatile，const
### 3.13 JavaScript 验证
- **JavaScript 表单验证：**JavaScript 可用来在数据被送往服务器前对 HTML 表单中的这些输入数据进行验证。
被 JavaScript 验证的这些典型的表单数据有：		
	1. 用户是否已填写表单中的必填项目？
	2.  用户输入的邮件地址是否合法？
	3.  用户是否已输入合法的日期？
	4.  用户是否在数据域 (numeric field) 中输入了文本？	
- **E-mail 验证：** 输入的数据必须包含 @ 符号和点号(.)。同时，@ 不可以是邮件地址的首字符，并且 @ 之后需有至少一个点号。

## 4 类型和对象
### 4.1 什么是对象
JavaScript 中的所有事物都是对象：字符串、数值、数组、函数...	
JavaScript 允许自定义对象；		
JavaScript 提供多个内建对象，比如 String、Date、Array 等等。		
对象只是带有属性和方法的特殊数据类型。
		
- **访问对象的属性：**属性是与对象相关的值。		
例：		
```javascript
objectName.length
```
- **访问对象的方法：**方法是能够在对象上执行的动作。
- **创建 JavaScript 对象**		
方法：		
1.定义并创建对象的实例		
例：		
```javascript
var currentDay = new Date();
person={firstname:"John",lastname:"Doe",age:50,eyecolor:"blue"};
```
2.使用函数来定义对象，然后创建新的对象实例		
例：		
```javascript 
function person(firstname,lastname,age,eyecolor)
{
this.firstname=firstname;
this.lastname=lastname;
this.age=age;
this.eyecolor=eyecolor;
}
var myFather=new person("Bill","Gates",56
```

### 4.2 JavaScript Number 对象
JavaScript 只有一种数字类型，可以使用也可以不使用小数点来书写			
所有 JavaScript 数字均为 64 位.		

- **精度：** 整数（不使用小数点或指数计数法）最多为 15 位。		
小数的最大位数是 17，但是浮点运算并不总是 100% 准确：

- **八进制和十六进制：**如果前缀为 0，则 JavaScript 会把数值常量解释为八进制数，如果前缀为 0 和 "x"，则解释为十六进制数。

> 提示：绝不要在数字前面写零，除非您需要进行八进制转换。

**数字属性和方法**

- 属性：

```
MAX VALUE, NaN				
MIN VALUE, prototype		
NEGATIVE INFINITIVE, constructor		
POSITIVE INFINITIVE
```

- 方法：

```
toExponential(), toString()
toFixed(), valueOf()
toPrecision()
```
### 4.3 JavaScript Array（数组）
- **数组对象的作用是：**使用单独的变量名来存储一系列的值。
- **定义数组：**数组对象用来在单独的变量名中存储一系列的值。
使用关键词 new 来创建数组对象。		
例：		
```javascript
var myArray=new Array()
```
- **赋值：**		
例：		
```javascript
var mycars=new Array()
mycars[0]="Saab"
```
或		
```javascript
var mycars=new Array("Saab","Volvo","BMW")
```

### 4.4 JavaScript String
字符串对象用于处理已有的字符块。		
例： 		
```javascript
var txt="Hello world!"
document.write(txt.length)
document.write(txt.toUpperCase())
```			
输出12 HELLO WORLD!

### 4.5 JavaScript Date（日期）
- **定义日期：**Date 对象用于处理日期和时间，可以通过 new 关键词来定义 Date 对象。

```
var myDate=new Date()
```

> 注意：Date 对象自动使用当前的日期和时间作为其初始值。

### 4.6 JavaScript Boolean（布尔）
- **Boolean 对象：**可以将 Boolean 对象理解为一个产生逻辑值的对象包装器。		

Boolean（逻辑）对象用于将非逻辑值转换为逻辑值（true 或者 false）。

- **创建 Boolean 对象**		
使用关键词 new 来定义 Boolean 对象。下面的代码定义了一个名为 myBoolean 的逻辑对象：
			
``` 
var myBoolean=new Boolean()
```
> 注释：如果逻辑对象无初始值或者其值为 0、-0、null、""、false、undefined 或者 NaN，那么对象的值为 false。否则，其值为 true（即使当自变量为字符串 "false" 时）

### 4.7 JavaScript Math（算数）
- **Math 对象：**Math 对象提供多种算数值类型和函数。无需在使用这个对象之前对它进行定义。		
Math（算数）对象的作用是：执行普通的算数任务。
- **算数值：**JavaScript 提供 8 种可被 Math 对象访问的算数值及在 Javascript 中使用这些值的方法：

```
常数, Math.E
2 的自然对数, Math.LN2
圆周率, Math.PI
10 的自然对数, Math.LN10
2 的平方根, Math.SQRT2
以 2 为底的 e 的对数, Math.LOG2E
1/2 的平方根, Math.SQRT1_2
以 10 为底的 e 的对数, Math.LOG10E
```

- **算数方法**
	1. round 方法对一个数进行四舍五入
	2. random() 方法来返回一个介于 0 和 1 之间的随机数
          
### 4.8 JavaScript RegExp 对象
RegExp 对象用于规定在文本中检索的内容
RegExp 是正则表达式的缩写

- **定义 RegExp：**通过 new 关键词来定义 RegExp 对象。以下代码定义了名为 patt1 的 RegExp 对象，其模式是 "e"：

```
var patt1=new RegExp("e");
```
当使用该 RegExp 对象在一个字符串中检索时，将寻找的是字符 "e"。

**RegExp 对象的方法：**	test()、exec() 以及 compile()。

- **test() 方法：**检索字符串中的指定值。返回值是 true 或 false。
	
```javascript
var patt1=new RegExp("e");
document.write(patt1.test("The best things in life are free"));
```		
输出true，因为此字符串中含有“e”

- **exec() 方法：**检索字符串中的指定值。返回值是被找到的值。如果没有发现匹配，则返回 null。  

```javascript    
var patt1=new RegExp("e");
document.write(patt1.exec("The best things in life are free"));
```		
输出“e”

- **compile() 方法：**用于改变 RegExp。compile() 既可以改变检索模式，也可以添加或删除第二个参数。  

```javascript             
var patt1=new RegExp("e");
document.write(patt1.test("The best things in life are free"));
patt1.compile("d");
document.write(patt1.test("The best things in life are free"));
```		
输出truefalse，因为字符串里有“e”没有“d”
## 5 理解JavaScript HTML DOM

**HTML DOM （文档对象模型）：**通过 HTML DOM，可访问 JavaScript HTML 文档的所有元素。		
当网页被加载时，浏览器会创建页面的文档对象模型（Document Object Model）。HTML DOM 模型被构造为对象的树。			
**HTML DOM 树：**

![Image of DOM%E6%A0%91]
(https://github.com/sammulyuan/javascript/blob/master/DOM%E6%A0%91.png)

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
