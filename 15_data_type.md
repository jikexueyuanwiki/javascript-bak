# JavaScript 数据类型

## 整数类型
		
一个整数可以是十进制、十六进制和八进制数，一个十进制数由一串数字序列组成，它的第一个数字不能为0；如38，-25，+120，74286等都是十进制整数。		
如果第一个数字为0，则表示它是一个八进制数；如0，012，0377，04056等都是八进制整数，对应的十进制整数依次为0，10，255和2094。		
若为0x，则表示它为一个十六进制数；如0x0，0X25，0x1ff，0x30CA等都是十六进制整数，对应的十进制整数依次为0，37，511和4298。

## 浮点数类型	
	
浮点数的例子：
`3.1415,  -3.1E12,  0.1e12 和 2E-12`	
一个浮点数必须包含一个数字，一个小数点或“e”（或“E”）。

## 布尔类型		
Boolean 类型有两种值：true 和 false

## 字符串类型
		
字符串是若干封装在双引号（“）或单引号（'）内的字符。如下：	
`
"fish"
'fish'
"5467"
"a line"
`		
可以在字符串中使用引号，只要不匹配包围字符串的引号即可：
`"He is called 'Bill'";`

## 对象类型
		
用new声明一个新的对象			
例：

```javascript	
var currentDay = new Date();		
alert(currentDay.getDay());
```
		
对象由花括号分隔。在括号内部，对象的属性以名称和值对的形式 `(name : value)`来定义。属性由逗号分隔：		
例：

```javascript
var person={firstname:"Bill", lastname:"Gates", id:5566};
```

空格和折行无关紧要。声明可横跨多行：		
例：

```javascript
var person={
firstname : "Bill",
lastname  : "Gates",
id        :  5566
};
```

对象属性有两种寻址方式：		
例：

```javascript
name=person.lastname;
name=person["lastname"];
```
		
## Undefined 和 Null	
	
Undefined 这个值表示变量不含有值。		
可以通过将变量的值设置为 null 来清空变量。	
	
## 数组类型
		
例：	

```javascript	
var arr = new Array(3);
```

通过arr.length取得数组的长度

> 注意： JavaScript 变量均为对象。当您声明一个变量时，就创建了一个新的对象。
