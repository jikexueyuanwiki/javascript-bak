# JavaScript jQuery

## jQuery

jQuery 是目前最受欢迎的 JavaScript 框架。
		
它使用 CSS 选择器来访问和操作网页上的 HTML 元素（DOM 对象）。
	
jQuery 同时提供 companion UI（用户界面）和插件。	

许多大公司在网站上使用 jQuery：Google、Microsoft、IBM、Netflix 


## jQuery 描述

主要的 jQuery 函数是 $() 函数（jQuery 函数）。如果您向该函数传递 DOM 对象，它会返回 jQuery 对象，带有向其添加的 jQuery 功能。
		
jQuery 允许通过 CSS 选择器来选取元素。
		
在 JavaScript 中，可以分配一个函数以处理窗口加载事件：
	
例：		

**JavaScript 方式：**

```javascript
function myFunction()
{
  var obj=document.getElementById("h01");
  obj.innerHTML="Hello jQuery";
}
onload=myFunction;
```		

等价的 jQuery 是不同的：
		
**jQuery 方式：**
		
```javascript
function myFunction()
{
  $("#h01").html("Hello jQuery");
}
$(document).ready(myFunction);   
```                             
