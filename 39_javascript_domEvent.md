# JavaScript事件处理（DOM 事件）

- **onBlur：**在select、text、password、textarea失去焦点时被触发；

- **onChange：**在select、text、textarea的值被改变且失去焦点时被触发；		
onchange 事件常结合对输入字段的验证来使用。

- **onClick：**出现在一个对象被鼠标选中时被触发（button,checkbox,radio,reset,submit,text,textarea等）

- **onFocus：**在一个对象获得焦点，select、text、text area时被触发；

- **onLoad：**出现在一个文档完成对一个窗口的载入用户进入页面时被触发；

- **onMouseOver：**鼠标被移动到一个超连接上时被触发；	
onmouseover 事件可用于在用户的鼠标移至 HTML 元素上方时触发函数。

- **onMouseOut：**鼠标从一个超连接上移开时被触发；		
onmouseout 事件可用于在用户的鼠标移出元素时触发函数。

- **onSelect：**当form对象中的内容被选中时被触发，视情况可以对一个对象组合使用这些事件处理；

- **onSubmit：**出现在用户通过提交按钮提交一个表单时被触发；

- **onUnload：**当用户退出一个文档离开页面时被触发；      

> 注意：onmousedown, onmouseup 以及 onclick 构成了鼠标点击事件的所有部分。		
首先当点击鼠标按钮时，会触发 onmousedown 事件，当释放鼠标按钮时，会触发 onmouseup 事件，最后，当完成鼠标点击时，会触发 onclick 事件。

## HTML 事件的例子

1. 当用户点击鼠标时

2. 当网页已加载时

3. 当图像已加载时

4. 当鼠标移动到元素上时

5. 当输入字段被改变时

6. 当提交 HTML 表单时

7. 当用户触发按键时
