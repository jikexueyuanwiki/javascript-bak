# DOM 元素
## **创建新的 HTML 元素**
向 HTML DOM 添加新元素，必须首先创建该元素（元素节点），然后向一个已存在的元素追加该元素。 	
	  
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

## **删除已有的 HTML 元素**
删除 HTML 元素，必须首先获得该元素的父元素：		

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
