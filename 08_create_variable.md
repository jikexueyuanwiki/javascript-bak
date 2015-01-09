# JavaScript 创建变量 


1. JavaScript 变量与代数一样，JavaScript 变量可用于存放值（比如 x=2）和表达式（比z=x+y）。
	1. 变量可以使用短名称（比如 x 和 y），也可以使用描述性更好的名称（比如 age, sum，totalvolume）。
	2. 变量必须以字母开头
    3. 变量也能以 $ 和 _ 符号开头（不过我们不推荐这么做）
    4. 变量名称对大小写敏感（y 和 Y 是不同的变量）
      
    > 提示：JavaScript 语句和 JavaScript 变量都对大小写敏感。	虽然JavaScript可以不需定义即可直接使用变量，但不建议这么做。

2. 变量的作用范围：
 	1. 在一个函数（function）之外定义一个变量，那它叫作全局变量
	2. 在 function 内部定义的变量则叫局部变量，它只作用于函数内
	
## 声明（创建）JavaScript 变量

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

## 重新声明 JavaScript 变量	
	
如果重新声明 JavaScript 变量，该变量的值不会丢失：	
在以下两条语句执行后，变量 name 的值依然是 “Hello"：	

例：	

```javascript
var carname="Volvo";		
var carname;
```
