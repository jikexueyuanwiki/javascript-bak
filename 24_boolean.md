# JavaScript Boolean（布尔）
## **Boolean 对象**
可以将 Boolean 对象理解为一个产生逻辑值的对象包装器。		

Boolean（逻辑）对象用于将非逻辑值转换为逻辑值（true 或者 false）。

## **创建 Boolean 对象**		
使用关键词 new 来定义 Boolean 对象。下面的代码定义了一个名为 myBoolean 的逻辑对象：
			
``` 
var myBoolean=new Boolean()
```
> 注释：如果逻辑对象无初始值或者其值为 0、-0、null、""、false、undefined 或者 NaN，那么对象的值为 false。否则，其值为 true（即使当自变量为字符串 "false" 时）