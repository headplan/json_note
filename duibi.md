# 对比

JSON和XML对比,他们都支持创建,读取和解码.

**冗余度**

XML比JSON更冗余,编写JSON更快.

**数组用法**

XML用来描述结构化数据,不包含数组.

**解析**

JS直接使用eval解析,返回描述的对象.

**XML和JSON的例子**

JSON:

```js
{
    "company": Volkswagen,
    "name": "Vento",
    "price": 800000
}
```

XML:

```js
<car>
   <company>Volkswagen</company>
   <name>Vento</name>
   <price>800000</price>
</car>
```



