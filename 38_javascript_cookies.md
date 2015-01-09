# JavaScript Cookies

cookie 是存储于访问者的计算机中的变量。每当同一台计算机通过浏览器请求某个页面时，就会发送这个 cookie。你可以使用 JavaScript 来创建和取回 cookie 的值。
		
## 创建和存储cookie		

例：创建一个可在 cookie 变量中存储访问者姓名的函数

```javascript
function setCookie(c_name,value,expiredays)
{
var exdate=new Date()
exdate.setDate(exdate.getDate()+expiredays)
document.cookie=c_name+ "=" +escape(value)+
((expiredays==null) ? "" :";expires="+exdate.toGMTString())
}
```
