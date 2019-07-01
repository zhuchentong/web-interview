#### 前端笔试题-初级
---

1.  以下CSS选择器优先级顺序错误的是

    a. 內联样式 > ID选择器 > 类选择器

    b. 类选择器 > 属性选择器 > 标签选择器

    c. ID选择器 > 伪类选择器 > 伪元素选择器	

    d. 內联样式 > 属性选择器 > 伪元素选择器

> 答案为 b

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
<img src="/img/img4.png" />
<img src="/img/img5.png" style="display:none"/>
</body>
```
a. 6

b. 0

c. 4

d. 3

> 答案为 

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

> 答案为

---
