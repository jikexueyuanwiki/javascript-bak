#JavaScript Window

浏览器对象模型（Browser Object Model）尚无正式标准。

	
由于现代浏览器已经（几乎）实现了 JavaScript 交互性方面的相同方法和属性，因此常被认为是 BOM 的方法和属性。	

所有浏览器都支持 window 对象。它表示浏览器窗口。所有 JavaScript 全局对象、函数以及变量均自动成为 window 对象的成员。	

全局变量是 window 对象的属性。全局函数是 window 对象的方法。

甚至 HTML DOM 的 document 也是 window 对象的属性之一：

```javascript
window.document.getElementById("header");
```

## Window 尺寸

有三种方法能够确定浏览器窗口的尺寸（浏览器的视口，不包括工具栏和滚动条）。		
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
	
## 一些其他方法	
	
```
window.open() - 打开新窗口		
window.close() - 关闭当前窗口		
window.moveTo() - 移动当前窗口		
window.resizeTo() - 调整当前窗口的尺寸
```		
