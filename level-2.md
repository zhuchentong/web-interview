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
