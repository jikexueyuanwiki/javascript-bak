# JavaScript AJAX的使用
**AJAX** 即“Asynchronous JavaScript and XML”（异步 JavaScript 和 XML），也就是无刷新数据读取。

## **http 请求**		
GET 用于获取数据。GET 是在 URL 中传递数据，它的安全性低，容量低。		
POST 用于上传数据。POST 安全性一般，容量几乎无限。

## **ajax 请求**	
	
ajax 请求一般分成 4 个步骤：		
**1.创建 ajax 对象**		
在创建对象时，有兼容问题：

```javascript
var oAjax = new XMLHttpRequest();   //for ie6 以上
var oAjax = new ActiveXObject('Microsoft.XMLHTTP'); //for ie6
```		

合并上面的代码：

```javascript
var oAjax = null;
if(window.XMLHttpRequest){
  oAjax = new XMLHttpRequest();
}else{
  oAjax = new ActiveXObject('Microsoft.XMLHTTP');
}
```		

**2.连接服务器：**会用到 open() 方法。

- open() 方法有三个参数：		
第一个参数是连接方法即 GET 和 POST，		
第二个参数是 URL 即所要读取数据的地址，		
第三个参数是否异步，它是个布尔值，true 为异步，false 为同步。

```javascript
oAjax.open('GET', url, true);
```

**3.发送请求：**send() 方法。

```javascript
oAjax.send();
```

**4.接收返回值**		
onreadystatechange 事件。当请求被发送到服务器时，我们需要执行一些基于响应的任务。

每当 readyState 改变时，就会触发 onreadystatechange 事件。

 ```    
readyState：请求状态，返回的是整数（0-4）。
  0（未初始化）：还没有调用 open() 方法。
  1（载入）：已调用 send() 方法，正在发送请求。
  2（载入完成）：send() 方法完成，已收到全部响应内容。
  3（解析）：正在解析响应内容。
  4（完成）：响应内容解析完成，可以在客户端调用。
status：请求结果，返回 200 或者 404。
200 => 成功。
404 => 失败。
```
