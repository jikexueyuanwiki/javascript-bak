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
      
    > 提示：JavaScript 语句和 JavaScript 变量都对大小写敏感。	虽然JavaScript可以不需定义即可直接使用变量，但不建议这么做。

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
		
1. 定义并创建对象的实例		
例：				
```javascript
var currentDay = new Date();
person={firstname:"John",lastname:"Doe",age:50,eyecolor:"blue"};
```
2. 使用函数来定义对象，然后创建新的对象实例		
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
### 5.1 DOM 简介

**HTML DOM （文档对象模型）：**通过 HTML DOM，可访问 JavaScript HTML 文档的所有元素。		
当网页被加载时，浏览器会创建页面的文档对象模型（Document Object Model）。HTML DOM 模型被构造为对象的树。			
**HTML DOM 树：**

![Image of DOM%E6%A0%91]
(https://github.com/sammulyuan/javascript/blob/master/DOM%E6%A0%91.png)

- JavaScript 能够改变页面中的所有 HTML 元素
- JavaScript 能够改变页面中的所有 HTML 属性
- JavaScript 能够改变页面中的所有 CSS 样式
- JavaScript 能够对页面中的所有事件做出反应

**查找 HTML 元素方法**	
	
1. 通过 id 找到 HTML 元素：在 DOM 中查找 HTML 元素的最简单的方法		
例：		
```javascript
var x=document.getElementById("hello");
```			
如果找到hello元素，则x返回hello元素；否则返回null		
2. 通过标签名找到 HTML 元素		
例：		
```javascript
var x=document.getElementById("main");
var y=x.getElementsByTagName("p");
```		
凭id找main元素，在找main元素中的所有`<p>`元素
3. 通过类名找到 HTML 元素

> 提示：通过类名查找 HTML 元素在 IE 5,6,7,8 中无效。

### 5.2 DOM HTML
- **改变 HTML 输出流：**document.write() 可用于直接向 HTML 输出流写内容。
例：

```javascript
<!DOCTYPE html>
<html>
<body>
<script>
document.write(Date());
</script>
</body>
</html>
```
> 提示：绝不要使用在文档加载之后使用 document.write()。这会覆盖该文档。

- **改变 HTML 内容：**修改 HTML 内容的最简单的方法时使用 innerHTML 属性。	
	
```
document.getElementById(id).innerHTML=new HTML
```			   
例：

```javascript			
<html>
<body>
<p id="p1">Hello World!</p>
<script>
document.getElementById("p1").innerHTML="New text!";
</script>
</body>
</html>
```			
此句输出的是New text！不是Hello World！
- **改变 HTML 属性**

```
document.getElementById(id).attribute=new value
```
### 5.3 DOM CSS
**改变 HTML 样式**

```
document.getElementById(id).style.property=new style
```			
例：

```javascript
<p id="p2">Hello World!</p>
<script>
document.getElementById("p2").style.color="blue";
</script>
```			
输出后Hello World！字体为蓝色
### 5.4 DOM 元素
**创建新的 HTML 元素：**向 HTML DOM 添加新元素，必须首先创建该元素（元素节点），然后向一个已存在的元素追加该元素。 	
	  
- **创建新的`<p>`元素：**		
```javascript
var para=document.createElement("p");
```		
- **创建文本节点，向 `<p>` 元素添加文本：**			
```javascript
var node=document.createTextNode("这是新段落。");
```
- **向 `<p>`元素追加文本节点：**			
```javascript
para.appendChild(node);
```
- **向一个已有的元素追加新元素：**				
```javascript
var element=document.getElementById("div1");
```
- **向已有的元素追加新元素：**			
```javascript
element.appendChild(para);
```

**删除已有的 HTML 元素：**删除 HTML 元素，必须首先获得该元素的父元素：		

- 从父元素中删除子元素：		
```javascript
parent.removeChild(child);
```      
- 在不引用父元素的情况下删除某个元素：找到希望删除的子元素，然后使用其 parentNode 属性来找到父元素：		
例：		
```javascript
var child=document.getElementById("p1");
child.parentNode.removeChild(child);
```

## 6 JS 浏览器BOM
浏览器对象模型（Browser Object Model）尚无正式标准。	
由于现代浏览器已经（几乎）实现了 JavaScript 交互性方面的相同方法和属性，因此常被认为是 BOM 的方法和属性。		
### 6.1 JavaScript Window
所有浏览器都支持 window 对象。它表示浏览器窗口。所有 JavaScript 全局对象、函数以及变量均自动成为 window 对象的成员。	
全局变量是 window 对象的属性。全局函数是 window 对象的方法。
甚至 HTML DOM 的 document 也是 window 对象的属性之一：

```javascript
window.document.getElementById("header");
```

- **Window 尺寸：**有三种方法能够确定浏览器窗口的尺寸（浏览器的视口，不包括工具栏和滚动条）。
对于Internet Explorer、Chrome、Firefox、Opera 以及 Safari：
```
window.innerHeight - 浏览器窗口的内部高度		
window.innerWidth - 浏览器窗口的内部宽度
```				
对于 Internet Explorer 8、7、6、5：
```
document.documentElement.clientHeight	
document.documentElement.clientWidth	
```		
或者		
```
document.body.clientHeight		
document.body.clientWidth
```		
- **一些其他方法：**		
```
window.open() - 打开新窗口		
window.close() - 关闭当前窗口		
window.moveTo() - 移动当前窗口		
window.resizeTo() - 调整当前窗口的尺寸
```		

### 6.2 JavaScript Window Screen
**Window Screen：**window.screen 对象在编写时可以不使用 window 这个前缀。		

```
screen.availWidth - 可用的屏幕宽度
screen.availHeight - 可用的屏幕高度
```

- **Window Screen 可用宽度：**screen.availWidth 属性返回访问者屏幕的宽度，以像素计，减去界面特性，比如窗口任务栏。
- **Window Screen 可用高度：**screen.availHeight 属性返回访问者屏幕的高度，以像素计，减去界面特性，比如窗口任务栏。
- **函数：**alert，confirme，prompt，open，close

### 6.3 JavaScript Window Location
**Window Location：**window.location 对象在编写时可不使用 window 这个前缀。		

```          
location.hostname 返回 web 主机的域名		
location.pathname 返回当前页面的路径和文件名		
location.port 返回 web 主机的端口 （80 或 443）	
location.protocol 返回所使用的 web 协议（http:// 或 https://）
```

- **Window Location Href：**location.href 属性返回当前页面的 URL。
- **Window Location Pathname：**location.pathname 属性返回 URL 的路径名。
- **Window Location Assign：**location.assign() 方法加载新的文档。

### 6.4 JavaScript Window History
**Window History：**window.history 对象在编写时可不使用 window 这个前缀。为了保护用户隐私，对 JavaScript 访问该对象的方法做出了限制。

```         
history.back() - 与在浏览器点击后退按钮相同
history.forward() - 与在浏览器中点击按钮向前相同
```

- **Window History Back：**history.back() 方法加载历史列表中的前一个 URL。
- **Window History Forward：**history forward() 方法加载历史列表中的下一个 URL。

### 6.5 JavaScript Navigator
**Window Navigator：**window.navigator 对象在编写时可不使用 window 这个前缀。

- **浏览器检测：**		
由于 navigator 可误导浏览器检测，使用对象检测可用来嗅探不同的浏览器。		
由于不同的浏览器支持不同的对象，您可以使用对象来检测浏览器。	
例如，由于只有 Opera 支持属性 "window.opera"，可以据此识别出 Opera。		
例：		
```javascript
if (window.opera) {...some action...}
```

### 6.6 JavaScript 弹窗
- **警告框：**警告框经常用于确保用户可以得到某些信息。	
当警告框出现后，用户需要点击确定按钮才能继续进行操作。

```
alert("文本")
```
- **确认框：**确认框用于使用户可以验证或者接受某些信息。	
当确认框出现后，用户需要点击确定或者取消按钮才能继续进行操作。

```
confirm("文本")
```
如果用户点击确认，那么返回值为 true。如果用户点击取消，那么返回值为 false。

- **提示框：**提示框经常用于提示用户在进入页面前输入某个值。	
当提示框出现后，用户需要输入某个值，然后点击确认或取消按钮才能继续操纵。

```
prompt("文本","默认值")
```
如果用户点击确认，那么返回值为输入的值。如果用户点击取消，那么返回值为 null。

### 6.7 JavaScript 计时事件
**avaScript 计时事件：**通过使用 JavaScript，我们有能力作到在一个设定的时间间隔之后来执行代码，而不是在函数被调用后立即执行。我们称之为计时事件。		

方法:

```
setTimeout()：未来的某时执行代码
clearTimeout()：取消setTimeout()
```
- **setTimeout()**		

```
var t=setTimeout("javascript语句",毫秒)
```		

setTimeout() 方法会返回某个值。		
第一个参数是含有 JavaScript 语句的字符串。这个语句可能诸如 `alert('5 seconds!')`，或者对函数的调用，诸如 `alertMsg()`。

- **clearTimeout()**

```
clearTimeout(setTimeout_variable)
```

### 6.8 JavaScript Cookies
cookie 是存储于访问者的计算机中的变量。每当同一台计算机通过浏览器请求某个页面时，就会发送这个 cookie。你可以使用 JavaScript 来创建和取回 cookie 的值。
		
- **创建和存储cookie**		

例：创建一个可在 cookie 变量中存储访问者姓名的函数

```javascript
function setCookie(c_name,value,expiredays)
{
var exdate=new Date()
exdate.setDate(exdate.getDate()+expiredays)
document.cookie=c_name+ "=" +escape(value)+
((expiredays==null) ? "" :";expires="+exdate.toGMTString())
}
```

## 7 事件和事件监听
### 7.1 JavaScript事件处理（DOM 事件）
- **onBlur：**在select、text、password、textarea失去焦点时被触发；
- **onChange：**在select、text、textarea的值被改变且失去焦点时被触发；		
onchange 事件常结合对输入字段的验证来使用。
- **onClick：**出现在一个对象被鼠标选中时被触发（button,checkbox,radio,reset,submit,text,textarea等）
- **onFocus：**在一个对象获得焦点，select、text、text area时被触发；
- **onLoad：**出现在一个文档完成对一个窗口的载入用户进入页面时被触发；
- **onMouseOver：**鼠标被移动到一个超连接上时被触发；	
onmouseover 事件可用于在用户的鼠标移至 HTML 元素上方时触发函数。
- **onMouseOut：**鼠标从一个超连接上移开时被触发；		
onmouseout 事件可用于在用户的鼠标移出元素时触发函数。
- **onSelect：**当form对象中的内容被选中时被触发，视情况可以对一个对象组合使用这些事件处理；
- **onSubmit：**出现在用户通过提交按钮提交一个表单时被触发；
- **onUnload：**当用户退出一个文档离开页面时被触发；      

> 注意：onmousedown, onmouseup 以及 onclick 构成了鼠标点击事件的所有部分。		
首先当点击鼠标按钮时，会触发 onmousedown 事件，当释放鼠标按钮时，会触发 onmouseup 事件，最后，当完成鼠标点击时，会触发 onclick 事件。

**HTML 事件的例子：**

1. 当用户点击鼠标时
2. 当网页已加载时
3. 当图像已加载时
4. 当鼠标移动到元素上时
5. 当输入字段被改变时
6. 当提交 HTML 表单时
7. 当用户触发按键时

### 7.2 JavaScript异常处理
**JavaScript 抛出错误：**当错误发生时，当事情出问题时，JavaScript 引擎通常会停止，并生成一个错误消息。		
描述这种情况的技术术语是：`JavaScript 将抛出一个错误`		
**JavaScript 测试和捕捉：**	
	
- **try 语句：**允许我们定义在执行时进行错误测试的代码块。
- **catch 语句：**允许我们定义当 try 代码块发生错误时，所执行的代码块。

JavaScript 语句 try 和 catch 是成对出现的。

```
try
{
   //在这里运行代码
}
catch(err)
{
   //在这里处理错误
}
```

- **Throw 语句：** throw 语句允许我们创建自定义错误。	
正确的技术术语是：`创建或抛出异常（exception）`	

如果把 throw 与 try 和 catch 一起使用，那么您能够控制程序流，并生成自定义的错误消息。

```
throw exception
```
> 注意：异常可以是 JavaScript 字符串、数字、逻辑值或对象。

### 7.3 onClick 和 onLoad
- onload 和 onunload 事件可用于处理 cookie。		
- onload 事件可用于检测访问者的浏览器类型和浏览器版本，并基于这些信息来加载网页的正确版本。

```
<body onload="checkCookies()">
```

### 7.4 DOM 事件监听
**添加监听：**在JavaScript中，我们使用如下的方式为元素添加事件监听：

```
element.addEventListener(<event-name>, <callback>, <use-capture>);
```

- **event-name(string):**这是你想监听的事件的名称或类型。	
它可以是任何的标准DOM事件（click, mousedown, touchstart, transitionEnd,等等），当然也可以是你自己定义的事件名称（我们会在后面介绍自定义事件相关内容）。
- **callback(function)（回调函数）：**这个函数会在事件触发的时候被调用。相应的事件(event)对象，以及事件的数据，会被作为第一个参数传入这个函数。
- **use-capture(boolean)：**这个参数决定了回调函数(callback)是否在“捕获(capture)”阶段被触发。

```javascript
var element = document.getElementById('element');
function callback() {
  alert('Hello');
}
// Add listener
element.addEventListener('click', callback);
```
**移除监听：**使用`element.removeEventListener()`方法来移除事件监听：

```
element.removeEventListener(<event-name>, <callback>, <use-capture>);
```

> 注意：必须要有这个被绑定的回调函数的引用。简单地调用element.removeEventListener('click');是不能达到想要的效果的。
         
不能使用匿名函数作为回调函数。			
例：		
```javacript
var element = document.getElementById('element');
function callback() {
alert('Hello once');
element.removeEventListener('click', callback);
}
// Add listener
element.addEventListener('click', callback);
```

**Element对象**	
	
![Image of Element]
(https://github.com/sammulyuan/javascript/blob/master/Element.png)

## 8 JavaScript 调试
### 8.1. Firebug
Firebug是网页浏览器 Mozilla Firefox 下的一款开发类扩展，现属于Firefox的五星级强力推荐扩展之一。		
它集HTML查看和编辑、Javascript控制台、网络状况监视器于一体，是开发JavaScript、CSS、HTML和Ajax的得力助手。		
Firebug如同一把精巧的瑞士军刀，从各个不同的角度剖析Web页面内部的细节层面，给Web开发者带来很大的便利。		
Firebug是一个除错工具。用户可以利用它除错、编辑、甚至删改任何网站的 CSS、HTML、DOM 以及JavaScript 代码。	
	
- **主要功能：**		
CSS调试		
CSS尺标		
网络监视器		
JS调试器		
Console 控制台		
修改HTML		
DOM查看器		

## 9 创建智能化表单
### 9.1 访问表单元素

- 表单对象Form属性：

```
action 、elements、method、name、target  
```   
- 表单提交的方法：

```
Get  Post   name    target           
```
- 表示打开表单的url：

```
_self    _parent    _blank    _top
```
- 表单元素：

```
document.forms[索引].elements[索引].属性  
document.forms[索引].elements[索引].方法（参数）  
document.forms[索引].属性  
document.forms["表单名称"].属性  
document.表单名称.元素名称.属性   
document.表单名称.元素名称.方法（参数）
```
### 9.2 表单提交
**表单提交的一般方式：**

```
1. .....<input type="submit" onclick="return validate();">     
2. .....<form action="...." name="...." onsubmit="return validate(this);">     
3. .....<input type="button" onclick="validate(this)">
```

### 9.3 隐藏和显示表单
**validate()函数** 	
	
```
function validate(obj){  
obj.submit() 
}
```
## 10 JavaScript 库
### 10.1 JavaScript库的介绍
JavaScript 库 - jQuery、Prototype、MooTools。
### 10.2 JavaScript jQuery
**jQuery：**jQuery 是目前最受欢迎的 JavaScript 框架。		
它使用 CSS 选择器来访问和操作网页上的 HTML 元素（DOM 对象）。	
jQuery 同时提供 companion UI（用户界面）和插件。	
许多大公司在网站上使用 jQuery：Google、Microsoft、IBM、Netflix 

- **jQuery 描述：**主要的 jQuery 函数是 $() 函数（jQuery 函数）。如果您向该函数传递 DOM 对象，它会返回 jQuery 对象，带有向其添加的 jQuery 功能。		
jQuery 允许通过 CSS 选择器来选取元素。		
在 JavaScript 中，可以分配一个函数以处理窗口加载事件：
	
例：		
JavaScript 方式：

```javascript
function myFunction()
{
  var obj=document.getElementById("h01");
  obj.innerHTML="Hello jQuery";
}
onload=myFunction;
```		
等价的 jQuery 是不同的：		
jQuery 方式：
		
```javascript
function myFunction()
{
  $("#h01").html("Hello jQuery");
}
$(document).ready(myFunction);   
```                                                                                                                                                                                      
### 10.3 JavaScript Prototype
**Prototype：**Prototype 是一种库，提供用于执行常见 web 任务的简单 API。

- API 是应用程序编程接口（Application Programming Interface）的缩写。它是包含属性和方法的库，用于操作 HTML DOM。
- Prototype 通过提供类和继承，实现了对 JavaScript 的增强。

### 10.4 JavaScript MooTools
**MooTools：**MooTools 也是一个框架，提供了可使常见的 JavaScript 编程更为简单的 API。

MooTools 也含有一些轻量级的效果和动画函数。
### 10.5 JavaScript AJAX的使用
**AJAX** 即“Asynchronous JavaScript and XML”（异步 JavaScript 和 XML），也就是无刷新数据读取。

**http 请求**		
GET 用于获取数据。GET 是在 URL 中传递数据，它的安全性低，容量低。		
POST 用于上传数据。POST 安全性一般，容量几乎无限。

**ajax 请求：**	
	
ajax 请求一般分成 4 个步骤：		
**1.创建 ajax 对象**		
在创建对象时，有兼容问题：

```javascript
var oAjax = new XMLHttpRequest();   //for ie6 以上
var oAjax = new ActiveXObject('Microsoft.XMLHTTP'); //for ie6
```		
合并上面的代码：

```javascript
var oAjax = null;
if(window.XMLHttpRequest){
  oAjax = new XMLHttpRequest();
}else{
  oAjax = new ActiveXObject('Microsoft.XMLHTTP');
}
```		

**2.连接服务器：**会用到 open() 方法。

- open() 方法有三个参数：		
第一个参数是连接方法即 GET 和 POST，		
第二个参数是 URL 即所要读取数据的地址，		
第三个参数是否异步，它是个布尔值，true 为异步，false 为同步。

```javascript
oAjax.open('GET', url, true);
```

**3.发送请求：**send() 方法。

```javascript
oAjax.send();
```

**4.接收返回值**		
onreadystatechange 事件。当请求被发送到服务器时，我们需要执行一些基于响应的任务。每当 readyState 改变时，就会触发 onreadystatechange 事件。

 ```    
readyState：请求状态，返回的是整数（0-4）。
  0（未初始化）：还没有调用 open() 方法。
  1（载入）：已调用 send() 方法，正在发送请求。
  2（载入完成）：send() 方法完成，已收到全部响应内容。
  3（解析）：正在解析响应内容。
  4（完成）：响应内容解析完成，可以在客户端调用。
status：请求结果，返回 200 或者 404。
200 => 成功。
404 => 失败。
```
## 11 JavaScript 实例
### 11.1 JavaScript 对象实例
极客课程链接：[JavaScript内置对象](http://www.jikexueyuan.com/course/195.html)
### 11.2 JavaScript 浏览器对象实例
极客课程链接：[JavaScript浏览器对象](http://www.jikexueyuan.com/course/208.html)
### 11.3 JavaScript HTML DOM 实例
### 11.4 JavaScript 总结
jQuery 是一个 JavaScript 库。		
jQuery 极大地简化了 JavaScript 编程。		
HTML DOM 定义了访问和操作 HTML 文档的标准方法。		
HTML DOM 独立于平台和语言，可被任何编程语言使用，比如 Java、JavaScript 和 VBscript。		
AJAX = 异步 JavaScript 和 XML。		
AJAX 不是一种新的编程语言，而是一种使用现有标准的新方法。		
通过与服务器进行数据交换，AJAX 可以在不重新加载整个网页的情况下，对网页的某部分进行更新。		
接下来要学好HTML5。
