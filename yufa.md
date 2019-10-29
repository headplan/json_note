# 语法

JSON 的语法基本上可以视为JavaScript语法的一个子集:

* 数据使用名\/值对表示;
* 使用大括号保存对象,每个名称后面跟着一个 ':'\(冒号\),名\/值对使用','\(逗号\)分割;
* 使用方括号保存数组,数组值使用','\(逗号\)分割.

示例:

```js
{
    "book": [
        {
            "id":"01",
            "language": "Java",
            "edition": "third",
            "author": "Herbert Schildt"
        },
        {
            "id":"07",
            "language": "C++",
            "edition": "second"
            "author": "E.Balagurusamy"
    }]
}
```

JSON 支持以下两种数据结构:

* **名\/值对集合:**这一数据结构由不同的编程语言支持.
* **有序的值列表:**包括数组,列表,向量或序列等等.

