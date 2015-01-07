# JavaScript 输出
可以使用 `document.getElementById(id)` 方法从 JavaScript 访问某个 HTML 元素；	
	
- 通过指定的 id 来访问 HTML 元素，并改变其内容：		
	
例：		
```javascript		
<!DOCTYPE html>
<html>
<body>
<h1>My First Web Page</h1>
<p id="demo">My First Paragraph</p>
<script>
document.getElementById("demo").innerHTML="My First JavaScript";
</script>
</body>
</html>
```

- 直接把 `<p>`元素写到 HTML 文档输出中：			
	
例：		
```javascript		
<!DOCTYPE html>
<html>
<body>
<h1>My First Web Page</h1>
<script>
document.write("<p>My First JavaScript</p>");
</script>
</body>
</html>
```	
	
> 注意：document.write() 仅仅向文档输出写内容，如果在文档已完成加载后执行 document.write，整个 HTML 页面将被覆盖。