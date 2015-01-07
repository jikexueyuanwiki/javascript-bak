# JavaScript 条件语句和循环
##JavaScript If...Else

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
## JavaScript switch 语句

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
## JavaScript for 循环

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

## JavaScript while 循环

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

## JavaScript Break 和 Continue 语句
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

