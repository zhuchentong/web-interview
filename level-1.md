#### 前端笔试题-初级

1. 下面的程序正确的输出结果是?

```
function Test() {
    var i = 0;
    return function() {
        console.log(i++);
    }
}
 
var test1 = Test(),
    test2 = Test();

test1();
test1();
test2();
```

a. 0 1 0 

b. 0 1 2

c. 0 0 0

d. 0 0 2

> 答案为 a

> 解析: Test内部形成了闭包,定义的局部变量、子函数的作用域在函数内，所以test1,test2会访问不同的局部变量。

---

2. 如何获得以下select标签区域的文本

```
<form name="a">
<select name="a" size="1" id=”obj”>
    <option value="a">1</option>
    <option value="b">2</option>
    <option value="c">3</option>
</select>
</form> 
```

a. obj.options[obj.selectedIndex].text

b. obj.options[obj.selectedIndex].value

c. obj.value

d. obj.text

> 答案为 a

> 解析:显示的文本选择对应option的text,而不是select或option的value

---

3. 下面的描述正确的是?

```
var F=function(){};
Object.prototype.a = 1;
Function.prototype.b = 2;
var f = new F();
```

a. f能取到a，但取不到b

b. f能取到a,b

c. F能取到b，不能取到a

d. F能取到a，不能取到b

> 答案为 a

> 解析: 所有普通对象都源于这个Object.prototype对象，只要是对象，都能访问到a ，而f通过new 关键词进行函数调用，之后无论如何都会返回一个与F关联的普通对象, 普通对象无法取到b，F可以取到b
---

4. 下面对css的link和@import之前的区别描述错误的是？

a. link属于XHTML标签，而@import完全是CSS提供的一种方式

b. 当一个页面被加载的时候，link引用的CSS会同时被加载，而@import引用的CSS会等到页面全部被下载完再被加载

c. link在支持CSS的浏览器上都支持而@import只在5.0以上的版本有效

d. 当使用javascript控制dom去改变样式的时候，只能使用@import方式

> 答案为 d

> 解析:
1，@import url（）机制是不同于link的，link是在加载页面前把css加载完毕，而@import url（）则是读取完文件后在加载，所以会出现一开始没有css样式，闪烁一下出现样式后的页面(网速慢的情况下)。  
2，@import 是css2里面的，所以古老的ie5不支持。  
3，当使用javascript控制dom去改变样式的时候，只能使用link标签，因为@import不是dom可以控制的。
4，link除了能加载css外还能定义RSS，定义rel连接属性，@import只能加载css  

---

5. 下面代码的作用是？

```
<meta name="viewport" content="width=device-width, initial-scale=1">
```

a. 使得页面编码合乎要求

b. 表示支持响应式设计

c. 支持正常的绘制和缩放

d. 表示针对滚屏进行适当的适配

> 答案为 b


```
解析: viewport常用属性:
width - viewport的宽度 
height - viewport的高度
initial-scale - 初始的缩放比例
minimum-scale - 允许用户缩放到的最小比例
maximum-scale - 允许用户缩放到的最大比例
user-scalable - 用户是否可以手动缩放
```
---

6. 以下描述正确的是:

```
<head>
    <link href="main1.css" ref="stylesheet">
    <link href="main2.css" ref="stylesheet">
</head>
```

a. main1.css和main2.css同时开始加载，先加载完成的优先解析

b. 如果main1.css和main2.css中有相同的选择器规则，那么main2.css中的规则将合并main1.css的规则

c. main2.css只有在main1.css加载并解析后，才开始加载

d. 如果main1.css和main2.css中有相同的选择器规则，那么main2.css中的规则将被忽略

> 答案为 A B

> 解析: CSS规则合并，当有相同的属性时，就会发生后者覆盖前者的情况。link标签是同时开始加载的，先加载完的先解析


---


7. 以下哪些阶段属于DOM事件流:

a. 事件捕获阶段

b. 处于目标阶段

c. 事件冒泡阶段

d. 事件监控阶段


>  答案为 A B C

>  解析: 事件流包括三个阶段：事件捕获阶段、处于目标阶段、事件冒泡阶段

---

8. 和换行相关的样式是哪些?

a. word-break

b. letter-spacing

c. white-space

d. word-spacing

> 答案为 A C

> 解析:
```
letter-spacing 单词间距
word-spacing 字母间距
word-break :break-all 单词内换行
white-sapce:nowrap 不换行。除非碰到<br>
```

---

9. 下面代码的运行结果是:

```
if(! "foo" in window){
    var foo = 1;
}
alert(foo);
```

a. null

b. 1

c. undefined

d. 以上都不正确

>  答案为: c

> 解析:

```
本题考察的是变量提升, ES6之前的javascript是没有块级作用域的。函数是JavaScript中唯一拥有自身作用域的结构。所以var声明会提升到顶部，但不会执行赋值表达式
```
---


10. 提升web页面性能的方法包含以下以下哪些方式:

a. 合并静态资源请求

b. 静态资源使用 CDN 托管

c. 开启http缓存

d. 使用模块化开发

> 答案为 a b c

> 解析:

```
模块化开发更多的作用在于面向开发，代码解耦，实现项目工程化.
```
---


11. 下面说法错误的是:

a. const用于声明常量，声明后不可修改

b. 使用const不会发生变量提升现象

c. 不能使用const重复声明同一个变量

d. const可以先声明，不赋值。

> 答案为 d

> 解析:

```
使用const声明后必须赋值，负责程序会抛出异常。

```

12. 下面针对Set说法错误的是:

A、set方法用于添加成员

B、clear方法用于清除所有成员。

C、entries方法返回成员的位置索引和值的遍历器

D、values方法返回成员值的便利器

> 答案为 c

> 解析:

```
返回的是键名和键值的遍历器；特别注意的是：set结构的键名和键值是同一个值。
```

---

13. 关于css3的flexbox描述错误的是:

a. flex-direction设置元素排列的方向

b. order设置元素显示的顺序

c. flex-basis设置元素的默认大小

d. justify-content: center设置元素为水平居中
  

> 答案为 d

> 解析:

```
justify-content是设置元素的主轴对齐模式,如果主轴方向是竖直方向，则为竖直居中
```

---

14. 以下代码的输出为:

```
function f1(){}
typeof f1.prototype;
typeof Object.prototype;
typeof Function.prototype.prototype;
typeof f1.prototype.constructor
```

a. object object undefined function

b. object object object object

c. undefined object undefined function

d. undefined object object object

> 答案为 a

> 解析

```
基础的prototype知识的考察, 
f1.prototype.constructor是函数，而Function的prototype是一个对象,对象默认没有prototype所以为undefined
```

---

15. 下面的路径名哪些符合AMD规范

```
a. ../../foo/Boo/WoO;

b. foo/boo/Woo;

c. ./foo/boo/woo;

d. foo/boo/woo.js;

> 答案为 c

> 解析:
```
1,模块名是由一个或多个单词以正斜杠为分隔符拼接成的字符串
2,单词须为驼峰形式，或者"."，".."
3,模块标识不允许文件扩展名的形式，如".js"
4,模块名可以为 "相对的" 或 "顶级的"。如果首字符为"."或".."则为"相对的"模块名
5,顶级的模块名从根命名空间的慨念模块解析
6,相对的模块名从 "require" 书写和调用的模块解析
```


---



16. 以下哪些是webpack可以实现的功能:

a. 代码转换

b. 代码分割

c. 自动刷新

d. 代码校验

> 答案为 a b c d

> 解析:

```
webpack基本功能

代码转换：TypeScript 编译成 JavaScript、SCSS 编译成 CSS 等等
文件优化：压缩 JavaScript、CSS、HTML 代码，压缩合并图片等
代码分割：提取多个页面的公共代码、提取首屏不需要执行部分的代码让其异步加载
模块合并：在采用模块化的项目有很多模块和文件，需要构建功能把模块分类合并成一个文件
自动刷新：监听本地源代码的变化，自动构建，刷新浏览器
代码校验：在代码被提交到仓库前需要检测代码是否符合规范，以及单元测试是否通过
自动发布：更新完代码后，自动构建出线上发布代码并传输给发布系统。
```

---

17. 以下说法错误的是:

a. <keep-alive>是Vue的内置组件，能在组件切换过程中将状态保留在内存中，防止重复渲染DOM。

b. vue-loader是.vue文件的一个加载器，跟template/js/style转换成js模块。

c. 在vue对象的directive方法里面有两个参数，一个是指令名称，另外一个是函数。

d. afterRouteEnter是vue-router的后置路由守卫

> 答案为 d

> 解析:

```
afterEach是 vue-router的后置路由守卫
```

---


18. 下面说法错误的是

a. React DOM在渲染之前会默认过滤所有传入的值

b. React DOM在渲染过程中只会更新改变了的部分

c. 直接通过赋值更新React组件状态不会重新渲染组件，必须使用setState方法

d. JSX是JavaScript的一种语法扩展，React的使用依赖JSX

> 答案为 d

> 解析

```
React推荐使用JSX,但不一定必须使用JSX
```

---

18.前端框架 React 不具备的特性

a. 数据绑定

b. 组件化

c. 指令

d. 生命周期钩子函数

> 答案为 c

> 解析

```
同angular和Vue不一样，React 没有绑定指令，所以他的绑定，是直接引用和操纵对象的状态
```

---

19. 以下代码额输出是:

```
var x = 1;

setTimeout(function(){
    x = 2;
},0)

setTimeout(function(){
    x = 3;
},0)

setTimeout(function(){
    delete x;
},0)

console.log(x);
```

a. 1

b. 2

c. 3

d. undefined

> 答案为 a

> 解析

```
setTimeout属于宏任务，会在console.log(x)之后执行，不影响输出结果
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

 var a = fun(0); 
 a.fun(1); 
 a.fun(2); 
 a.fun(3)
```

a. undefined 0 0 0 

b. undefined 0 1 2 

c. undefined 0 1 1

d. undefined 0 0 1

> 答案为 a

> 解析

```
这是js闭包的考察，其中嵌套了三层fun函数，搞清楚每层fun的函数是那个fun函数尤为重要，a对象的o值为0

```


