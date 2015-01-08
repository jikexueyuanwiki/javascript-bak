# JavaScript Navigator
**Window Navigator：**window.navigator 对象在编写时可不使用 window 这个前缀。

## **浏览器检测**		
由于 navigator 可误导浏览器检测，使用对象检测可用来嗅探不同的浏览器。		

由于不同的浏览器支持不同的对象，您可以使用对象来检测浏览器。	
例如，由于只有 Opera 支持属性 "window.opera"，可以据此识别出 Opera。		

例：		

```javascript
if (window.opera) {...some action...}
```
