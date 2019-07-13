### 项目

1、setItem、getItem已经封装好，setItem这些传值只能用字符串,并且只能是异步调用
2、请求的get、post方法已经封装好
3、weex.requireMoudle()是用于weex调用外部方法的
4、emit是发布一个要做什么的事件，on是监听当前事件，并做什么；emit发布的事件所有页面都可以监听。
5、clipboard 获取或者设置剪贴板内容，即复制粘贴

6、bootPage 是启动页

7、貌似不支持  v-show，只能用 v-if；不要嵌套使用 v-if， 会有问题

8、图片使用 <image src=""/>，注意：图片必须给宽高，不然无法渲染

9、滚动组件 scroller 如果要清除滚动条，需要在 scroller 外层加(即包裹住scroller的那一层)

```
 position: absolute;
 top: 0;
 right: 0;
 bottom: 0;
 left: 0;
```

10、weex的input标签 password 与 text 切换显示与隐藏，安卓会有问题，是原生的问题(需要原生修改)

11、post请求传参数的问题，qs模块

12、要想层级高，要放在最后面

13、tab栏切换的问题

14、week中使用websorcket实现实时推送问题(需要安卓和ios原生实现)

15、ios端使用scroller搭配refresh组件当子元素不满屏是不能下拉刷新问题，在scroller组件加alwaysScrollableVertical=true

16、iPhone X 系列顶部导航跟底部的适配

17、安卓的websorcket按照官网的例子改的时候，监听事件on后面是回调函数，与官网的有差别
        例如： ws.opopen(function(e) {})

?        注意：此时的 this 的指向问题！！！！！！！！！！！！！

18、weex模板更建议把后端所有的数据返回，而不是把 data 返回（在http.js文件）

19、直接在 http.commom.js 中引入 router.commom.js 不能以 {push}这种方式引入，因为push是关键字，会没用

### css样式

1、Weex 盒模型的 box-sizing 默认为 border-box，即盒子的宽高包含内容、内边距和边框的宽度，不包含外边距的宽度。

2、在 Android 平台，Weex 只支持 `overflow:hidden`；在 ios平台，Weex 支持 overflow:hidden和owerflow: visible

3、文本溢出显示省略号需要下面两个配合使用（注意，当遇到空格，数字，英文字符串的时候不能显示省略号，目前暂时没有办法解决）                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   

```
lines:1;
text-overflow:ellipsis; 
```