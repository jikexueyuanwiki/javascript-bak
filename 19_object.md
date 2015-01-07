# 什么是对象
JavaScript 中的所有事物都是对象：字符串、数值、数组、函数...	
JavaScript 允许自定义对象；		
JavaScript 提供多个内建对象，比如 String、Date、Array 等等。		
对象只是带有属性和方法的特殊数据类型。
		
## 访问对象的属性
属性是与对象相关的值。
		
例：		
```javascript
objectName.length
```
## 访问对象的方法
方法是能够在对象上执行的动作。
## 创建 JavaScript 对象	
	
方法：
		
- 定义并创建对象的实例
		
例：				
```javascript
var currentDay = new Date();
person={firstname:"John",lastname:"Doe",age:50,eyecolor:"blue"};
```

- 使用函数来定义对象，然后创建新的对象实例
		
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
