#### 前端笔试题-初级
---

1.  以下CSS选择器优先级顺序错误的是

    a. 內联样式 > ID选择器 > 类选择器

    b. 类选择器 > 属性选择器 > 标签选择器

    c. ID选择器 > 伪类选择器 > 伪元素选择器	

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

> 解析: 未挂载的css不会产生请求(#bg);重复url只会产生一次请求(img3);img标签样式设置为(visibility:hidden)也会产生请求

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

> 解析: if查询name变量首先在当前作用于内进行查询，当无法找到是查询外部作用域，当前作用域内因为声明了对应的name变量但是没有赋值，所以值为undefined

---

4. 下面有关CSS sprites说法错误的是？

a. 允许你将一个页面涉及到的所有零星图片都包含到一张大图中去

b. 利用CSS的“background-image”，“background-repeat”，“background-position”的组合进行背景定位

c. CSS Sprites虽然增加了总的图片的字节，但是很好地减少网页的http请求，从而大大的提高页面的性能

d. CSS Sprites整理起来更为方便，同一个按钮不同状态的图片也不需要一个个切割出来并个别命名

> 答案为 

> 

---


5. 在创建DOM元素的时候如果带有ID，那么会有什么副作用?

a. 会造成DOM树分支过多

b. 会增加内存负担

c. 会创建同名的全局变量


> 答案为

> 

---

6. 以下说法正确的有:

a. visibility:hidden;所占据的空间位置仍然存在，仅为视觉上的完全透明；

b. display:none;不为被隐藏的对象保留其物理空间；

c. visibility:hidden;与display:none;两者没有本质上的区别；

d. visibility:hidden;产生reflow和repaint（回流与重绘）；

>答案为

>

---

7. 浏览器中有些默认的inline-block标签, 以下那个不是?

a. button

b. input

c. label

d. img

>

>

---


