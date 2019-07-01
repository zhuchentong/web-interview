#### 前端笔试题-初级
---

1.  在CSS的样式选择器中，正确的优先级顺序是

    a. id选择器 > 标签选择器 > 类选择器

    b. 标签选择器 > 类选择器 > id选择器

    c. id选择器 > 类选择器 > 标签选择器

    d. 标签选择器 > id选择器 > 类选择器

> 答案为 c

> 解析: css选择器的优先级为ID选择器 > 类选择器 > 标签选择器


---

2. 关于CSS的position的属性，以下说法错误的是？

    a. static没有定位出现在整正常的流中

    b. fixed生成绝对定位的元素,相对于父元素

    c. relative：生成相对定位的元素，相对于元素本身正常位置进行定位

    d. absolute：生成绝对定位的元素，相对于 static 定位以外的第一个祖先元素进行定位。

> 答案为  b

> 解析: fixed生成绝对定位元素，是相对于浏览器窗口进行定位

---

3. 下面的程序正确的输出结果是?

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

4. 如何获得以下select标签区域的文本

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

5. 下面的描述正确的是?

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

6. 下面对css的link和@import之前的区别描述错误的是？

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

7. 下面代码的作用是？

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

8. 以下描述正确的是:

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


9. 以下哪些阶段属于DOM事件流:

a. 事件捕获阶段

b. 处于目标阶段

c. 事件冒泡阶段

d. 事件监控阶段


>  答案为 A B C

>  解析: 事件流包括三个阶段：事件捕获阶段、处于目标阶段、事件冒泡阶段

---

10. 和换行相关的样式是哪些?

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






