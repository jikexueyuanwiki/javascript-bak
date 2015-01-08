# JavaScript 计时事件
**JavaScript 计时事件：**通过使用 JavaScript，我们有能力作到在一个设定的时间间隔之后来执行代码，而不是在函数被调用后立即执行。我们称之为计时事件。		

## 方法

```
setTimeout()：未来的某时执行代码
clearTimeout()：取消setTimeout()
```
- **setTimeout()**		

```
var t=setTimeout("javascript语句",毫秒)
```		

setTimeout() 方法会返回某个值。		
第一个参数是含有 JavaScript 语句的字符串。这个语句可能诸如 `alert('5 seconds!')`，或者对函数的调用，诸如 `alertMsg()`。

- **clearTimeout()**

```
clearTimeout(setTimeout_variable)
```
