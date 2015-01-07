# JavaScript RegExp 对象
RegExp 对象用于规定在文本中检索的内容
RegExp 是正则表达式的缩写

## **定义 RegExp**
通过 new 关键词来定义 RegExp 对象。以下代码定义了名为 patt1 的 RegExp 对象，其模式是 "e"：

```
var patt1=new RegExp("e");
```
当使用该 RegExp 对象在一个字符串中检索时，将寻找的是字符 "e"。

## **RegExp 对象的方法**	
test()、exec() 以及 compile()。

- **test() 方法：**检索字符串中的指定值。返回值是 true 或 false。

例：	
```javascript
var patt1=new RegExp("e");
document.write(patt1.test("The best things in life are free"));
```		
输出true，因为此字符串中含有“e”

- **exec() 方法：**检索字符串中的指定值。返回值是被找到的值。如果没有发现匹配，则返回 null。  

例：	
```javascript    
var patt1=new RegExp("e");
document.write(patt1.exec("The best things in life are free"));
```		
输出“e”

- **compile() 方法：**用于改变 RegExp。compile() 既可以改变检索模式，也可以添加或删除第二个参数。  

例：	
```javascript             
var patt1=new RegExp("e");
document.write(patt1.test("The best things in life are free"));
patt1.compile("d");
document.write(patt1.test("The best things in life are free"));
```		
输出truefalse，因为字符串里有“e”没有“d”