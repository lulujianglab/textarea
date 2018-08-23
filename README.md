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

对应的测试时间分别是原生js、jQuery、Vue,可以看出Vue的执行效率和渲染效率最快，同时它的数据双向绑定也能明显提高这类功能项目的开发效率



