# 了解JavaScript代码的结构

- 通过在网页或工具中加入`<Script>…</Script>`标记JavaScript的开始和结束，将JavaScript代码放到`<Script>…</Script>`之间：

```
<SCRIPT LANGUAGE="JavaScript">
   <!--
     ......
   //-->
</SCRIPT>	                 
```		

（其中<!- - 和 - -> 标记，它为那些不支持 JavaScript 的浏览器提供了一个忽略它的方法，而 // 标记是一段注释的开始 ）		

也可以引入一个外部的JavaScript文件，外部文件通常包含被多个网页使用的代码，这个JavaScript文件一般以*.js作为扩展名，如需使用外部文件，请在 `<script> `标签的 `"src" `属性中设置该 .js 文件:

```
<SCRIPT LANGUAGE=“JavaScript” SRC=“*.js">
    ......
</SCRIPT>
```	

- 原则上，放在`<head></head>`和`<body></body>`之间。但视情况可以放在网页的任何部分；

- 一个页面可以有几个`<Script>…</Script>` ，不同部分的方法和变量，可以共享。
