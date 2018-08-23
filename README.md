# textarea

通过原生js、jQuery、vue三种方法实现移动端textarea字数的读取  测试其性能

web开发中性能测试的方法有很多，本demo用到的是最直接、最基本的技巧

分别是```console.time```和```console.timeEnd```这两个方法

测试从输入字符到页面字数更新的程序执行消耗的时间

这里简单的介绍下```console.time```和```console.timeEnd```

## console.time方法是开始计算时间，console.timeEnd是停止计时，输出脚本执行的时间

```js
// 启动计时器
console.time('testTime');

// (写一些测试用代码)

// 停止计时，输出时间
console.timeEnd('testTime');
```
## 本测试demo结果

![image](https://user-images.githubusercontent.com/26807227/44505399-c77d7b80-a6d3-11e8-9776-cec85c68c515.png)

对应的测试时间分别是原生js、jQuery、Vue,可以看出Vue的执行效率和渲染效率最高，同时它的数据双向绑定也能明显提高这类功能项目的开发效率

这里针对textarea做了一些默认样式的处理，包括取出默认边框，以及输入字符时的边框等，对input，button等也同样适用

## 去除textarea、input等默认样式
```
textarea {
  outline: none; /* 去掉输入字符时的默认样式 */
  FILTER: alpha(opacity=0); /*androd*/ 
  appearance:none;
  -webkit-appearance:none;
  -moz-appearance:none;
  background-color: white;
  text-shadow: none;
  -webkit-writing-mode: horizontal-tb !important;
  -webkit-tap-highlight-color:rgba(0,0,0,0);
  resize:none; /*禁止拉伸*/
}

.textarea{
   /*
   display: block;
   width: 100%;
   color: #ff45a8;
   */
   border: none; /*去掉默认边框*/
}
```




