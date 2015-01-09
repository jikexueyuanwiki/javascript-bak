# JavaScript异常处理

## JavaScript 抛出错误

当错误发生时，当事情出问题时，JavaScript 引擎通常会停止，并生成一个错误消息。		

描述这种情况的技术术语是：`JavaScript 将抛出一个错误`		
## JavaScript 测试和捕捉
	
- **try 语句：**允许我们定义在执行时进行错误测试的代码块。

- **catch 语句：**允许我们定义当 try 代码块发生错误时，所执行的代码块。

JavaScript 语句 try 和 catch 是成对出现的。

```
try
{
   //在这里运行代码
}
catch(err)
{
   //在这里处理错误
}
```

- **Throw 语句：** throw 语句允许我们创建自定义错误。		
正确的技术术语是：`创建或抛出异常（exception）`	

如果把 throw 与 try 和 catch 一起使用，那么您能够控制程序流，并生成自定义的错误消息。

```
throw exception
```

> 注意：异常可以是 JavaScript 字符串、数字、逻辑值或对象。
