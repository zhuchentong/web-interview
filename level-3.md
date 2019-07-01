1. 请选择一下浏览器分别使用哪些内核?

```
Firefox  IE   Safari   Chrome
```

a. trident  gcko webkit blink

b. gcko trident webkit blink

c. gcko trident blink webkit

d. trident gcko blink webkit


> 答案为 > b

> 解析

```
 IE: trident内核 
 Firefox：gecko内核 
 Safari:webkit内核
 Opera:以前是presto内核，Opera现已改用Google Chrome的Blink内核
 Chrome:Blink(基于webkit，Google与Opera Software共同开发) 
```

2. 以下那些是多域名存储网站资源的优势

a. CDN缓存更方便 

b. 突破浏览器并发限制 

c. 节约cookie带宽 

d. 实现负载均衡

> 答案为 a b c

> 解析:

```
网站多域名有如下优势：
CDN缓存更方便 
突破浏览器并发限制 
节约cookie带宽 
节约主域名的连接数，优化页面响应速度 
防止不必要的安全问题

```

3.  一下说法正确的是:

a. Webp图片压缩体积大约只有JPEG的2/3，并能节省大量的服务器带宽资源和数据空间.

b. APNG相比PNG，利用相邻像素的相似性使压缩率大大提高

c. CSS Sprites能很好地减少了网页的http请求，从而大大的提高了页面的性能

d. png8和png24主要是颜色位之间的差别

> 答案为 a b c

> 解析

```
png8和png24的根本区别，不是颜色位的区别，而是 存储方式不同。
```

4. 一下哪些方法有利于SEO?

a. 语义化书写HTML代码

b. 重要内容不要用JS输出

c. 尽少使用iframe框架

d. 为图片加上alt属性

> 答案为 a b c d

> 解析

```
以下技巧有利于网站的SEO:
1. 合理的title标签,突出重要的内容
2. 语义化书写HTML代码，符合W3C标准。
3. 利用布局，把重要内容HTML代码放在最前。
4. 重要内容不要用JS输出。
5. 尽少使用iframe框架。
6. 为图片加上alt属性
7. 利用CSS截取字符。
8. 伪静态设置。
```

---

5. 如果js请求被缓存，那么又可以与以下哪些因素有关?

a. cdn缓存

b. 浏览器缓存

c. cookie/session

d. 服务器缓存

> 答案为 a b d

> 解析:

```
一般情况下，dns缓存，cdn缓存，浏览器缓存，服务器缓存与请求js文件的缓存有关。
```

---

6. 以下关于Ajax状态码说法正确的是:

a. 205：没有新的内容，但浏览器应该重置它所显示的内容。用来强制浏览器清除表单输入内容

b. 304： 使用代理，必须通过代理访问资源， 代理的地址在Response 的Location中

c. 401：未授权，当前请求需要用户验证

d. 502：服务器作为网关或者代理时，为了完成请求访问下一个服务器，但该服务器返回了非法的应答

> 答案为: a c d

> 解析

```
304： 客户端有缓冲的文档并发出了一个条件性的请求。客户的缓存资源是最新的， 要客户端使用缓存
```
---

7. 如何在chrome中设置小于12px的中文

a. font-size:10px

b. -webkit-text-size-adjust:none

c. transform:scale(n);

d. translate:scale(n);

> 答案为 c

> 解析：

```
chrome默认是不支持12px以下的字体的。如果是小于会调整到12px,chrome27.0 版本以后已经不再支持`-webkit-text-size-adjust`,并且`-webkit-text-size-adjust`仅对英文有效, 推荐的方法是使用transform:scale(n)进行缩放
```

---

8. 浏览器将CORS请求分成两类：简单请求（simple request）和非简单请求（not-so-simple request），一下哪些请求是非简单请求:

a. GET请求,Content-Type为application/x-www-form-urlencoded

b. POST,Content-Type为application/x-www-form-urlencoded

c. GET请求, Content-Type为application/json

d. POST请求, Content-Type为application/json

> 答案为 c d

> 解析

```
满足一下调教则会发送简单请求：
（1) 请求方法是以下三种方法之一：
HEAD
GET
POST
（2）HTTP的头信息不超出以下几种字段：
Accept
Accept-Language
Content-Language
Last-Event-ID
Content-Type：只限于三个值application/x-www-form-urlencoded、multipart/form-data、text/plain
```

---

9. 以下错误的是:

a. 0 * -1 // 0

b. 0 * 1  // 0

c. 1/0    // Infinity

d. 1/-0   // Infinity

> 答案为 a d

> 解析

```
javascript中存在+0与-0,其中 1/-0 应为 -Infinity,0 * -1 也应为 -0, 而且1/0 === -1/0 也会返回false
```

10. 在javascript的严格模式下会报错的是:

a. x = 3.14;

b. var x = 3.14; delete x;   

c. var x = 010;

d. var x = \010;

> 答案为 a b c d

> 解析

```
在严格模式中，
a-不允许使用未声明的变量
b-不允许删除变量
c-不允许使用八进制
d-不允许使用转义字符
```

---

11. 下面针对Proxy说法错误的是

a、可以理解成在目标对象之前，架设一层“拦截”

b、Proxy的get 方法用于拦截某个属性的读取操作。

c、Proxy的set方法用于拦截对对象的写操作。

d、一旦对象设置Proxy代理后不可取消，所以要谨慎操作

> 答案为 d

> 解析

```
可以用Proxy.revocable( )来取消代理，并不是不可以取消的。
```

---

12.  下面针对Generator说法错误的是:

a.Generator函数，又称生成器函数

b. 声明Generator函数的关键字是：function*

c. Generator函数执行后得到的一个生成器

d. 使用return语句使Generator函数暂停执行，直到next方法的调用

> 答案为 d

> 解析:

```
使函数暂停执行的关键字是yield，不是return；return语句是使函数停止执行并退出。
```

---

13. 关于css的Grid描述错误的是:

a. grid-template用于设置布局结构

c.  grid-template-areas可是使用别名布局

c. grid-column-gap用于设置行间距

d. place-content用于设置布局方式

> 答案为 c

> 解析：

```
 grid-column-gap是用于设置列间距而不是行间距
```

---

14. 下面代码的输出是：

```
var a  = {foo:1}
var b = Object.create(a)

a.foo = 2
console.log(b.foo)
console.log(b.hasOwnProperty("foo"))

b.foo = 3
console.log(b.foo)
console.log(b.hasOwnProperty("foo))
```

a. 2 false 3 true

b. 1 false 3 true

c. 2 true 3 true

d. 1 true 3 true


> 答案为 a

> 解析

```
当b对象上不存在foo属性时，通过原型链进行查从查找，查找到a的 foo 属性，后面 b.foo = 3； b才拥有自己的 foo 属性，所以打印出来是3。
```

---


15. 以下说法正确的是:

a. CMD 推崇依赖就近，AMD 推崇依赖前置

b. CMD 推崇依赖前置，AMD 推崇依赖就近

c. CMD与AMD插件机制不同

d. AMD兼容CMD模块

> 答案为 a c

> 解析:

```
1. 定位有差异。RequireJS 想成为浏览器端的模块加载器，同时也想成为 Rhino / Node 等环境的模块加载器。Sea.js 则专注于 Web 浏览器端，同时通过 Node 扩展的方式可以很方便跑在 Node 环境中。

2. 遵循的规范不同。RequireJS 遵循 AMD（异步模块定义）规范，Sea.js 遵循 CMD （通用模块定义）规范。规范的不同，导致了两者 API 不同。Sea.js 更贴近 CommonJS Modules/1.1 和 Node Modules 规范。

3. CMD 推崇依赖就近，AMD 推崇依赖前置。
推广理念有差异。RequireJS 在尝试让第三方类库修改自身来支持 RequireJS，目前只有少数社区采纳。Sea.js 不强推，采用自主封装的方式来“海纳百川”，目前已有较成熟的封装策略。

4. 对开发调试的支持有差异。Sea.js 非常关注代码的开发调试，有 nocache、debug 等用于调试的插件。RequireJS 无这方面的明显支持。

5. 插件机制不同。RequireJS 采取的是在源码中预留接口的形式，插件类型比较单一。Sea.js 采取的是通用事件机制，插件类型更丰富。

```


---

16. 以下webpack流程执行顺序正确的是:

1. 从entry里配置的module开始递归解析entry依赖的所有module

2. 把所有Chunk转换成文件输出


3. 找到一个module，就会根据配置的loader去找对应的转换规则

4. 这些模块会以entry为单位分组，一个entry和其所有依赖的module被分到一个组Chunk

5. 对module进行转换后，再解析出当前module依赖的module

a. 1 5 3 4 2

b. 1 3 4 5 2

c. 1 3 5 4 2

d. 1  5 4 3 2

> 答案为 c

```
正确的顺序如下:

* 从entry里配置的module开始递归解析entry依赖的所有module
* 每找到一个module，就会根据配置的loader去找对应的转换规则
* 对module进行转换后，再解析出当前module依赖的module
* 这些模块会以entry为单位分组，一个entry和其所有依赖的module被分到一个组Chunk
* 最后webpack会把所有Chunk转换成文件输出
* 在整个流程中webpack会在恰当的时机执行plugin里定义的逻辑
···

---


17. 以下说法错误的是

a. active-class 是 vue-router 模块的 router-link 组件的属性

b. vue-router有全局导航钩子,组件内钩子两种钩子

c. vuex包括5中属性分别是 state、getter、mutation、action、module

d. vue生命周期8个阶段：创建前/后、载入前/后、更新前/后、销毁前/后

> 答案为 b

> 解析 

```
vue-router 有三种导航钩子，分别是
* 全局导航钩子
* 组件内钩子
* 单独路由独享组件
```

---

18. 以下说法错误的是:

a. Keys 是 React 用于追踪哪些列表中元素被修改、被添加或者被移除的辅助标识。

b. shouldComponentUpdate 允许我们手动地判断是否要进行组件更新，根据组件的应用场景设置函数的合理返回值能够帮我们避免不必要的更新。

c. createElement 函数是 JSX 编译之后使用的创建 React Element 的函数，而 copyElement 则是用于复制某个元素并传入新的 Props。

d. Refs 是 React 提供给我们的安全访问 DOM 元素或者某个组件实例的句柄

> 答案为 c

> 解析

```
cloneElement 是用于复制某个元素并传入新的 Props。
```


---

19. 下面代码输出的结果是

```
setTimeout(functoin(){
    console.log('C')
},0)

console.log(D)

new Promise(function(reslove){
    console.log(E)
    reslove()
    console.log(F)
}).then(function(){
    console.log(G)
})
console.log(H)
···

a. DEFHCG

b. DHEFCG

c. DEFHGC

d. DHEFGC

> 答案为 c

> 解析

```
不同的任务源会被分配到不同的 Task 队列中，任务源可以分为 微任务
（microtask） 和 宏任务（macrotask）。在 ES6 规范中，microtask 称为 jobs，
macrotask 称为 task。
setTimeout是宏任务，而Promise是微任务，所以按顺序来执行的话，宏任务被放在最后，微任务的then放在次后
```

---


20. 下面代码输出的值是

```
function fun(n,o) {
  console.log(o)
  return {
    fun:function(m){
      return fun(m,n);
    }
  };
}

 var a =  fun(0).fun(1);  
 c.fun(2); 
 c.fun(3);
```

a. undefined 0 0 0 

b. undefined 0 1 2 

c. undefined 0 1 1

d. undefined 0 0 1

> 答案为 c

> 解析

```
这是js闭包的考察，其中嵌套了三层fun函数，搞清楚每层fun的函数是那个fun函数尤为重要，a的o值为1

```