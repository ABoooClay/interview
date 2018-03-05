# 菜狗页面仔面经
>  2018新的开始，不要再混了

整理了一下最近面试谈到的问题

+ 基础知识
	+ http协议
	    + 各种HTTP Status Code：[http状态码常用对照表](http://tool.oschina.net/commons?type=5)
	+ Request、Response其中各种消息的含义
	+ 缓存机制
	+ tcp
	+ 页面渲染过程
		1. 渲染过程：[浏览器渲染过程与页面优化](https://segmentfault.com/a/1190000010298038  declaration)
		2. [css加载会造成阻塞吗？](https://www.cnblogs.com/chenjg/p/7126822.html)
	+ 重绘重排（参考上面渲染过程）
	+ xss、csrf的原理、如何防护
		1. [csrf是什么](https://zhuanlan.zhihu.com/p/22521378)
		2. 防范xss的关键是过滤所有的‘<’和‘>’字符，确保从后端而来的数据并不带有任何的html标签，xss的危险在于有不可预料的前端脚本，但是值得注意的是，不单只有script标签是可以运行脚本的，任何的html标签都可以加上类似onclick，onload这样的事件也都可以运行脚本，所以需要过滤所有的‘<’和‘>’字符。假如，从后端而来的数据一定需要带上html标签（比如编辑器的富文本），且内容并不能保证是安全的（并不是可靠的人员录入的），就需要有合适的规则去“净化”它们。这个有现成的工具，比如HTML Purifier。http://htmlpurifier.org/
		3. [通过session或token防护csrf攻击](https://www.zhihu.com/question/21385375/answer/20850443)
	+ 客户端存储
		1. [详细讲述Cookie,LocalStorge,SesstionStorge的区别和用法](https://segmentfault.com/a/1190000007506189)
		2. [session原理](https://segmentfault.com/a/1190000004627894)
		+ indexDB

+ Javascript
    + 原型链
		1. [JS重点整理之JS原型链彻底搞清楚](https://zhuanlan.zhihu.com/p/22787302)
		看完上面的再捋一遍下面的
		2. [JS 原型与原型链终极详解](https://www.jianshu.com/p/dee9f8b14771)
	+ 数组扩展
	+ 事件机制
		+ 冒泡捕获
		+ 移动端事件
		+ fastclick
			一般情况下移动端click都会有300ms延迟。移动浏览器上支持的双击缩放操作，以及IOS Safari 上的双击滚动操作，是导致300ms的点击延迟主要原因。FastClick的实现原理是在检测到touchend事件的时候，会通过DOM自定义事件立即出发模拟一个click事件，并把浏览器在300ms之后真正的click事件阻止掉。
			[解决移动端click事件300ms延迟(fastclick和几个其他方法)](https://www.jianshu.com/p/16d3e4f9b2a9)
		+ 一些常见兼容问题
	+ this、call、apply
		[js中this关键词详解](https://segmentfault.com/a/1190000003046071)
	+ 函数式编程
		[函数式编程入门教程 - 阮一峰](http://www.ruanyifeng.com/blog/2017/02/fp-tutorial.html)
	+ getter、setter
		1. [getter、setter方法有什么意义](https://www.zhihu.com/question/21401198)
		2. [由Vue引发的getter和setter思考](https://www.cnblogs.com/chinajins/p/5996835.html) 
		3.  [vue深入响应式原理](https://cn.vuejs.org/v2/guide/reactivity.html)
	+ es6、es7新特性
		+ promise、Generator 、async
		+ set、map
		+ class和原型链
		[ECMAScript 6 入门 - 阮一峰](https://github.com/ruanyf/es6tutorial)
	+ 一些常用算法
		+ 冒泡、快排、洗牌、递归、数组去重……
	+ jQuery的实现相关问题
		[jQuery源码剖析（一）——概览&工具方法](https://www.w3ctech.com/topic/256)
		[jQuery源码剖析（二）——$.Callbacks](https://www.w3ctech.com/topic/257)

+ 工程化
	+ 发展过程、目的
		+ glup、fis3到webpack
	+ webpack
		+ 原理
		+ 常用配置
		+ dev、production配置
		+ mock、proxy
		+ eslint
		+ 各种loader
		
+ react
	+ 为什么选择react
	+ 生命周期
	+ diff算法
		+ 复杂度o(n)怎么做到的
		+ key
	+ setState
		+ 为什么是异步的
		+ 在一个生命周期里面可能多次setState怎么做
	+ redux
	+ react-router
	+ 状态保存

+ node
	+ express和koa、koa2的区别
	+ 常用中间件
		+ proxy
		+ compression
		+ 静态资源处理
		+ session持久化
		+ react服务端渲染
		+ （node了解不多，还有一堆crud的东西直接说还没学到）

+ 其他
	+ 前端优化
	+ 多人协作开发
	+ 项目选型
	
------
暂时就回忆起这么多，每个问题基本都有细节可以扩展，后面再更新

### END
