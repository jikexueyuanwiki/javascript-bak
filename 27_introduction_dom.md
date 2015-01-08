# DOM 简介

## **HTML DOM （文档对象模型）**
通过 HTML DOM，可访问 JavaScript HTML 文档的所有元素。		
当网页被加载时，浏览器会创建页面的文档对象模型（Document Object Model）。HTML DOM 模型被构造为对象的树。			
**HTML DOM 树：**

![Image of DOMtree]
(images/DOMtree.png)

- JavaScript 能够改变页面中的所有 HTML 元素
- JavaScript 能够改变页面中的所有 HTML 属性
- JavaScript 能够改变页面中的所有 CSS 样式
- JavaScript 能够对页面中的所有事件做出反应

## **查找 HTML 元素方法**	
	
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