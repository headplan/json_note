# JSON模式\(Schema\)

JSON 模式是一种基于 JSON 格式定义 JSON 数据结构的规范.

JSON模式:

* 描述现有数据格式
* 干净的人类和机器可读的文档
* 完整的结构验证,有利于自动化测试
* 完整的结构验证,可用于验证客户端提交的数据

### JSON模式验证库

http:\/\/json-schema.org\/implementations.html

下面是一个基本的JSON模式,其中涵盖了一个经典的产品目录说明:

```js
{
    "$schema": "http://json-schema.org/draft-04/schema#",
    "title": "Product",
    "description": "A product from Acme's catalog",
    "type": "object",
    "properties": {
        "id": {
            "description": "The unique identifier for a product",
            "type": "integer"
        },
        "name": {
            "description": "Name of the product",
            "type": "string"
        },
        "price": {
            "type": "number",
            "minimum": 0,
            "exclusiveMinimum": true
        }
    },
    "required": ["id", "name", "price"]
}
```

