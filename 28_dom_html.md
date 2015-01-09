# DOM HTML

## 改变 HTML 输出流

document.write() 可用于直接向 HTML 输出流写内容。

例：

```javascript
<!DOCTYPE html>
<html>
<body>
<script>
document.write(Date());
</script>
</body>
</html>
```

> 提示：绝不要使用在文档加载之后使用 document.write()。这会覆盖该文档。

## 改变 HTML 内容

修改 HTML 内容的最简单的方法时使用 innerHTML 属性。	
	
```
document.getElementById(id).innerHTML=new HTML
```	
		   
例：

```javascript			
<html>
<body>
<p id="p1">Hello World!</p>
<script>
document.getElementById("p1").innerHTML="New text!";
</script>
</body>
</html>
```	
		
此句输出的是New text！不是Hello World！

## 改变 HTML 属性

```
document.getElementById(id).attribute=new value
```
