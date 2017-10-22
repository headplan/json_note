# JSONP

> 代码测试内容在Learning\_JSONP中查看

Jsonp\(JSON with Padding\)是 json 的一种"使用模式" , 可以让网页从别的域名\(网站\)那获取资料 , 即跨域读取数据 . 为什么我们从不同的域\(网站\)访问数据需要一个特殊的技术\(JSONP \)呢 ? 这是因为同源策略 . 

> 同源策略 , 它是由Netscape提出的一个著名的安全策略 , 现在所有支持JavaScript的浏览器都会使用这个策略 .

> JSON是一种数据交换格式 , 而JSONP是一种依靠开发人员的聪明才智创造出的一种非官方跨域数据交互协议 . 一个是描述信息的格式 , 一个是信息传递双方约定的方法 .

这里用实例解释一下同源策略 : 

```
# 新建两个文件,创建两个域
php -S localhost:8881 8881.php
php -S localhost:8882 8882.php

# 8882.php中用jquery发起请求
<script src="http://apps.bdimg.com/libs/jquery/2.1.4/jquery.min.js"></script>
<script>
$.get("http://localhost:8881/", function (data) {
        console.log(data)
        $('body').html(data);
});
</script>
```

根据同源策略查看log , 很明显会悲剧了 . 浏览器会阻止 , 根本不会发起这个请求 : 

> No 'Access-Control-Allow-Origin' header is present on the requested resource.

所以JSONP是为了解决这个问题的 . 

#### Script标签的跨域能力

前面我们引入了jquery : 

```
<script src="http://apps.bdimg.com/libs/jquery/2.1.4/jquery.min.js"></script>
```

这种方式我们请求了百度的jquery文件 , 放在script标签里设置scr属性是可以的 . 这说明 , 利用script的跨域能力是可行的 , 这就是jsonp的基础 . 

#### 总结

* Ajax直接请求普通文件存在跨域无权限访问的问题 , 不管是静态页面、动态网页、web服务等等只要是跨域请求一律不准
* 有”src”这个属性的标签都拥有跨域的能力，比如&lt;script&gt;、&lt;img&gt;、&lt;iframe&gt;
* 跨域访问数据的方式显而易见了 , 那就是在远程服务器上设法把数据装进js格式的文件里 , 供客户端调用和进一步处理
* 一种非正式传输协议形成了 , 那就是JSONP , 该协议的一个要点就是允许用户传递一个callback参数给服务端 , 然后服务端返回数据时会将这个callback参数作为函数名来包裹住JSON数据 , 这样客户端就可以随意定制自己的函数来自动处理返回数据了 . 

总结一句话就是利用script标签绕过同源策略 , 获得一个类似这样的数据 , jsonp callback是页面存在的回调方法 , 参数就是想得到的json . 

#### 利用script获取不同源的json



