# DOM 事件监听
## **添加监听**
在JavaScript中，我们使用如下的方式为元素添加事件监听：

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
## **移除监听**

使用`element.removeEventListener()`方法来移除事件监听：

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
(images/Element.png)
