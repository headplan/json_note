# 对象

JSON 对象可以使用 JavaScript 创建.

### 创建简单的对象

* 创建一个空对像
  ```
  var JSONObj = {};
  ```

* 创建一个新对象
  ```
  var JSONObj = new Object();
  ```

* 创建一个bookname属性值为字符串,price属性值为数字的对象
  ```
  var JSONObj = { "bookname ":"VB BLACK BOOK", "price":500 };
  ```

  > 可以通过使用 '.' 运算符访问属性.


### 创建数组对象

```js
<html>
<head>
<title>Creation of array object in javascript using JSON</title>
<script language="javascript" >

document.writeln("<h2>JSON array object</h2>");

var books = {
    "Pascal" : [ 
        { "Name"  : "Pascal Made Simple", "price" : 700 },
        { "Name"  : "Guide to Pascal", "price" : 400 }
    ],                       
    "Scala"  : [
        { "Name"  : "Scala for the Impatient", "price" : 1000 }, 
        { "Name"  : "Scala in Depth", "price" : 1300 }
    ]    
}    

var i = 0
document.writeln("<table border='2'><tr>");
for(i=0;i<books.Pascal.length;i++)
{   
    document.writeln("<td>");
    document.writeln("<table border='1' width=100 >");
    document.writeln("<tr><td><b>Name</b></td><td width=50>"
    + books.Pascal[i].Name+"</td></tr>");
    document.writeln("<tr><td><b>Price</b></td><td width=50>"
    + books.Pascal[i].price +"</td></tr>");
    document.writeln("</table>");
    document.writeln("</td>");
}

for(i=0;i<books.Scala.length;i++)
{
    document.writeln("<td>");
    document.writeln("<table border='1' width=100 >");
    document.writeln("<tr><td><b>Name</b></td><td width=50>"
    + books.Scala[i].Name+"</td></tr>");
    document.writeln("<tr><td><b>Price</b></td><td width=50>"
    + books.Scala[i].price+"</td></tr>");
    document.writeln("</table>");
    document.writeln("</td>");
}
document.writeln("</tr></table>");
</script>
</head>
<body>
</body>
</html>
```

