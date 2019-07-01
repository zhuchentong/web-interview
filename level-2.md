#### 前端笔试题-初级

---

1.  以下 CSS 选择器优先级顺序错误的是

    a. 內联样式 > ID 选择器 > 类选择器

    b. 类选择器 > 属性选择器 > 标签选择器

    c. ID 选择器 > 伪类选择器 > 伪元素选择器

    d. 內联样式 > 属性选择器 > 伪元素选择器

> 答案为 b

> 解析: 优先级关系：内联样式 > ID 选择器 > 类选择器 = 属性选择器 = 伪类选择器 > 标签选择器 = 伪元素选择器

---

2. 下面程序会发送多少个图片请求:

```
<head>
<style>
#bg{
    background:url('/img/img1.jpg');
}
#test{
    background:url('/img/img2.jpg');
}
</style>
</head>
<body>
<div id="test"></div>
<img src="/img/img3.png"/>
<img src="/img/img3.png"/>
<img src="/img/img4.png" style="visibility:hidden"/>
</body>
```

a. 6

b. 0

c. 4

d. 3

> 答案为 d

> 解析: 未挂载的 css 不会产生请求(#bg);重复 url 只会产生一次请求(img3);img 标签样式设置为(visibility:hidden)也会产生请求

---

3. 以下代码的执行结果是

```
var name="李四";

(function(){
    var name;
    if(typeof name=== 'undefined'){
        name='张三';
        console.log('再见'+name);
    }
    else{
        console.log('你好'+name);
    }
})();
```

a. 你好张三

b. 你好李四

c. 再见张三

d. 再见李四

> 答案为 c

> 解析: if 查询 name 变量首先在当前作用于内进行查询，当无法找到是查询外部作用域，当前作用域内因为声明了对应的 name 变量但是没有赋值，所以值为 undefined

---

4. 下面有关 CSS sprites 说法错误的是？

a. 允许你将一个页面涉及到的所有零星图片都包含到一张大图中去

b. 利用 CSS 的“background-image”，“background-repeat”，“background-position”的组合进行背景定位

c. CSS Sprites 虽然增加了总的图片的字节，但是很好地减少网页的 http 请求，从而大大的提高页面的性能

d. CSS Sprites 整理起来更为方便，同一个按钮不同状态的图片也不需要一个个切割出来并个别命名

> 答案为 C

> 解析: CSS Sprites 能减少图片的字节。

---

5. 在创建 DOM 元素的时候如果带有 ID，那么会有什么副作用?

a. 会造成 DOM 树分支过多

b. 会增加内存负担

c. 会创建同名的全局变量

d. 会影响网页加载速度

> 答案为 C

> 解析：你可能认为只有 JavaScript 代码才能创建全局变量，并且习惯使用 typeof 或 .. in window 来检测全局变量。但是 HTML 页面中的内容也会产生全局变量(通过 ID)，并且稍不注意就很容易让全局变量检查错误百出。

---

6. 以下说法正确的有:

a. visibility:hidden;所占据的空间位置仍然存在，仅为视觉上的完全透明；

b. display:none;不为被隐藏的对象保留其物理空间；

c. visibility:hidden;与 display:none;两者没有本质上的区别；

d. visibility:hidden;产生 reflow 和 repaint（回流与重绘）；

> 答案为 A B

> 解析:

```
 display：none指的是元素完全不陈列出来，不占据空间，涉及到了DOM结构，故产生reflow与repaint
 visibility：hidden指的是元素不可见但存在，保留空间，不影响结构，故只产生repaint
```

---

7. 浏览器中有些默认的 inline-block 标签, 以下那个不是?

a. button

b. input

c. label

d. img

> 答案为:  C

>  解析:

```
1.常见的块级元素(dispaly: block, 自动换行， 可设置高宽 )有：
div, h1-h6, p, pre, ul, ol, li, form, table等 

2. 常见的行内元素（display: inline, 无法自动换行，无法设置宽高）有：    a, label , span, i（斜体）,em（强调）, sub(下标)，sup（上标）等。 

3. 常见的行块级元素(display: inline-block, 拥有内在尺寸，可设置高宽，不会自动换行 )有：      
(button,input, textarea,select), img等，这类元素也被称为置换元素。
```

---

8. 在 form 表单中对 input 元素的 readonly 与 disabled 属性描述正确的是？（ ）

a. Readonly 为真时，脚本无法修改 input 的值

b. Disabled 为真时，脚本无法修改 input 的值

c. Readonly 为真时，input 的值不会随着表单提交

d. Disabled 为真时，input 的值不会随着表单提交

> 答案为 D

> 设置 readonly = true，页面上无法修改内容，但是可以通过 JavaScript 修改,内容会被提交;设置 disabled = true,无法修改内容，也不会被提交


9. 一下代码的输出结果是:

```
test1()
function test1(){
    console.log("beijing")
}

test2()
var test2 = function(){
    console.log("thanks")
}
```

a. beijing, thanks

b. beijing, TypeError: test2 is not a function

c. TypeError: test1 is not a function, thanks

d. TypeError: test1 is not a function, TypeError: test2 is not a function

> 答案为 b

> 解析

```
本题考察变量提示, 函数声明会有一个函数声明提升的过程,test2 是函数表达式，函数位于一个初始化语句中，在执行函数所在语句之前变量test2中不会保存对函数的引用。
```



---

10. 以下哪行语句可以实现如下效果:

```
' a b c'  => 'abc'
```

a. str.replace(/\s*/g,"")

b. str.replace(/^\s|\s$/g,"")

c. str.replace(/^\s*/, "")

d. str.replace(/(\s*$)/g, "")
 

> 答案为 a

> 解析

```
本题考察正则表达式, b和d可以去除尾空格, c可以去除首空格,a可以去除字符串中的所有空管
```
---

11. 下面描述错误的是:

a. includes函数用于判断字符串中是否含有指定的子字符串

b. repeat函数将目标字符串重复N次，目标字符串被修改

c. startsWidth函数判断指定的子字符串是否出现在目标字符串头部位置

d. endWidth函数判断指定的子字符串是否出现在目标字符串尾部位置

> 答案为 d

> 解析:

```
repeat函数将目标字符串重复N次，会返回一个新的字符串，不影响目标字符串。
```

---

12. 下面针对Promise说法错误的是：

A、 三种状态分别是：pending初始状态、fulfilled成功、rejected失败

B、 pending初始状态可以状变成fulfilled成功

C、 rejected失败不可以状变成pending初始状态

D、 rejected失败可以状变成fulfilled成功


> 答案为 d

> 解析:

```
rejected失败和fulfilled成功之间不能相互转换
```

---

13. 关于css3的flexbox描述错误的是:

a. flex-grow设置元素的增长比例

b. flex-shrink设置元素的伸缩比例

c. align-self设置元素行在在主轴上的对齐方式

d. align-items设置vz行的在辅轴上的对齐方式

> 答案为 c

> 解析: 

```
align-self用于子元素自身，用来覆盖 align-items 的值
```

---

14. 以下代码的输出为:

```
function A(){}
function B(a){
　　this.a = a;
}
function C(a){
　　if(a){
    this.a = a;
　　}
}

A.prototype.a = 1;
B.prototype.a = 1;
C.prototype.a = 1;
  
console.log(new A().a);
console.log(new B().a);
console.log(new C(2).a);
```

a. undefined 1 2

b. 1 undefined 2

c. undefined 1 1

d. 1 undefined 1

> 答案为 b

> 解析:

```
console.log(new A().a);　　//new A()为构造函数创建的对象，本身没有a属性，所以向它的原型去找，发现原型的a属性的属性值为1，故该输出值为1；

console.log(new B().a);　　//new B()为构造函数创建的对象，该构造函数有参数a，但该对象没有传参，故该输出值为undefined;

console.log(new C(2).a);　　//new C()为构造函数创建的对象，该构造函数有参数a，且传的实参为2，执行函数内部，发现if为真，执行this.a = 2,故属性a的值为2；

故这三个的输出值分别为：1、undefined、2.　　
```

---



15. 以下哪些是CommonjS规范内置的变量

a. module

b. context

c. require

d. exports

> 答案为 a c d

> 解析:

```
commonjs没有内置context变量
```

---


16. 以下描述错误的是:

a. bundle是由webpack打包出来的文件，chunk是指webpack在进行模块的依赖分析的时候，代码分割出来的代码块。module是开发中的单个模块。

b. Loaders是用来告诉webpack如何转化处理某一类型的文件，并且引入到打包出的文件中

c. Tree-shaking是指在打包中去除那些引入了，但是在代码中没有被用到的那些死代码。

d. webpack-dev-server使用临时目录来存储webpack开发环境下的打包文件，并且可以使用模块热更新，他比传统的http服务对开发更加简单高效。


> 答案为 d

> 解析:

```
 webpack-dev-server是使用内存来存储webpack开发环境下的打包文件，而不是临时目录
```

---

17. 下面关于vue生命周期说法错误的是：

a. beforecreate : 可以在这加个loading事件，在加载实例时触发

b. created : 初始化完成时的事件写在这里，如在这结束loading事件，异步请求以及查询DOM也适宜在这里调用

c. updated : 如果对数据统一处理，在这里写上相应函数

d. nextTick : 更新数据后立即操作dom

> 答案为 b

> 解析 

```
初始化查询DOM的操作应在mounted中执行
```


---


 19. 下面代码的输出是

 ```
setTimeout(_ => console.log(4))

new Promise(resolve => {
  resolve()
  console.log(1)
}).then(_ => {
  console.log(3)
})

console.log(2)
```

a. 2 4 1 3

b. 2 1 3 4

c. 1 2 3 4

d. 1 2 4 3

> 答案为 c

> 解析

```
consoel.log(1)属于同步任务,
console.log(3)属于微任务
cosnole.log(4)属于宏任务
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

 var a = fun(0).fun(1).fun(2).fun(3);
```

a. undefined 0 0 0 

b. undefined 0 1 2 

c. undefined 0 1 1

d. undefined 0 0 1

> 答案为 b

> 解析

```
这是js闭包的考察，其中嵌套了三层fun函数，搞清楚每层fun的函数是那个fun函数尤为重要，链式调用每次更新了对应的o值

```
