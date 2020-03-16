# 框架通用知识

## Nav-List
- [**`路由原理`**](#路由原理)
- [**`mvvm`**](#MVVM)



## 路由原理
> 本质上就是监听url的变化，然后匹配路由规则显示相应页面，并且是无刷新。
> 目前有两种模式，history和hash模式。

> www.test.com/#/ 就是 Hash URL，当 # 后面的哈希值发生变化时，不会向服务器请求数据，可以通过 hashchange 事件来监听到 URL 的变化，从而进行跳转页面。

> History 模式是 HTML5 新推出的功能，比之 Hash URL 更加美观

## mvvm
> MVVM由下面3个部分组成

- 1.View：界面
- 2.Model：数据模型
- 3.ViewModel：作为桥梁负责沟通 View 和 Model

>在 MVVM 中，最核心的也就是数据双向绑定，例如 Angluar 的脏数据检测，Vue 中的数据劫持。

### 脏数据检测
> 当触发了指定事件后会进入脏数据检测，这时会调用 `$digest` 循环遍历所有的数据观察者，判断当前值是否和先前的值有区别，如果检测到变化的话，会调用 `$watch` 函数，然后再次调用 `$digest` 循环直到发现没有变化。循环至少为二次 ，至多为十次。脏数据检测虽然存在低效的问题，但是不关心数据是通过什么方式改变的，都可以完成任务，但是这在 Vue 中的双向绑定是存在问题的。并且脏数据检测可以实现批量检测出更新的值，再去统一更新 UI，大大减少了操作 DOM 的次数。所以低效也是相对的。

### 数据劫持
> Vue 内部使用了 `Object.defineProperty()` 来实现双向绑定，通过这个函数可以监听到 set 和 get 的事件。核心思路就是手动触发一次属性的 getter 来实现发布订阅的添加。

### Proxy 与 Object.defineProperty 对比
- 1.只能对属性进行数据劫持，所以需要深度遍历整个对象
- 2.对于数组不能监听到数据的变化