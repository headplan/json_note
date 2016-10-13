# 数据类型

| 类型描述 |  |
| --- | --- |
| 数字型（Number） | JavaScript 中的双精度浮点型格式 |
| 字符串型（String） | 双引号包裹的 Unicode 字符和反斜杠转义字符 |
| 布尔型（Boolean） | true 或 false |
| 数组（Array） | 有序的值序列 |
| 值（Value） | 可以是字符串，数字，true 或 false，null 等等 |
| 对象（Object） | 无序的键:值对集合 |
| 空格（Whitespace） | 可用于任意符号对之间 |
| null | 空 |

### 数字

* JavaScript中的双精度浮点型格式,取决于实现;
* 不能使用八进制和十六进制格式;
* 在数字中不能使用NaN和Infinity.

**数字类型:整形,分数,指数.**

```js
var obj = {i:0,f:.9,e:6.23E12}
```

### 字符串

* 零个或多个双引号包裹的Unicode字符以及反斜杠转义序列;
* 字符就是只有一个字符的字符串,长度为1.

```js
var obj = {name:"bob"}
```

### 布尔

包含 true 和 false 两个值.

```js
var obj = {name: 'Amit', marks: 97, distinction: true}
```

### 数组

* 它是一个有序的值集合.
* 使用方括号闭合,这意味着数组以 \[ 开始, 以 \] 结尾.
* 值使用,\(逗号\)分割
* 数组索引可以以0或1开始
* 当键名是连续的整数时应该使用数组

```js
{
    "books": [
        { "language":"Java" , "edition":"second" },
        { "language":"C++" , "lastName":"fifth" },
        { "language":"C" , "lastName":"third" }
    ]
}
```

### 对象

* 它是一个无序的名\/值对集合.
* 对象使用大括号闭合,以 '{' 开始,以 '}' 结尾.
* 每个名称后面都跟随一个 ':'\(冒号\),名\/值对使用,\(逗号\)分割.
* 键名必须是字符串,并且不能同名.
* 当键名是任意字符串时应该使用对象.

```js
{
    "id": "011A",
    "language": "JAVA",
    "price": 500,
}
```

### 空格

可以在任意一对符号之间插入.可以添加用来让代码更可读.

### null

意味着空类型.

### JSON值

* 数字（整型和浮点型）
* 字符串
* 布尔值
* 数组
* 对象
* null

```js
String | Number | Object | Array | TRUE | FALSE | NULL
var i =1;
var j = "sachin";
var k = null;
```



