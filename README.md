# javascript-this（JavaScript函数this指向）
![GitHub commit activity (branch)](https://img.shields.io/github/commit-activity/m/Hlxuan/javascript-this) ![GitHub issues](https://img.shields.io/github/issues/Hlxuan/javascript-this) ![GitHub Stars](https://img.shields.io/github/stars/Hlxuan/javascript-this)

## 项目描述

### [步骤0：验证函数调用时`this`指向的不同情况](00_this指向的实验.html)

本步骤将理解`this`在`JavaScript`执行上下文中的指向规则。

#### 预期结果
- 直接调用`foo()`函数，`this`指向全局对象`window`；
- 通过对象调用`obj.showThis`函数，`this`指向调用函数的对象。


### [步骤1：验证不同场景下`this`的默认绑定规则](01_this绑定规则实验.html)

本步骤将通过研究不同的场景来观察`this`指向的变化，包括普通函数调用、对象属性方法独立调用、高阶函数内部调用，以及严格模式下的函数调用。

#### 预期结果
- 普通函数独立调用，在非严格模式下，`this`指向全局对象`window`；在严格模式下，`this`为`undefined`；
- 在对象内定义的方法独立调用`baz()`，`this`指向全局对象`window`；
- 在高阶函数内部调用`obj.bar`，`this`指向全局对象`window`；
- 在严格模式下，`this`为`undefined`；


### [步骤2：验证`this`的隐式绑定规则](02_this隐式绑定实验.html)

本步骤将探索`this`的隐式绑定规则。

#### 预期结果
- 在`obj.bar()`调用中，`this`指向调用函数的对象。


### [步骤3：验证`this`在`new`调用下的绑定规则](03_this_new绑定实验.html)

本步骤将探索`this`在`new`调用下的绑定规则。

#### 预期结果
- 使用`new`关键词调用`foo()`，`this`指向新创建的对象。


### [步骤4：验证`this`的显式绑定规则](04_this显式绑定实验.html)

本步骤将探索`this`的显式绑定规则。

#### 预期结果
- 调用`foo.call(obj)`，`this`被显式绑定指向对象`obj`；
- 调用`foo.apply(123)`，数字会被自动封装成对应的Number对象。
- 调用`foo.call("abc")`，字符串会自动封装成对应的String对象。


### [步骤5：验证`apply`和`call`的使用方法](05_apply_call实验.html)

本步骤将在不同调用方式下改变`this`指向以参数传递的方式。

#### 预期结果
- 直接调用`foo("gkd", 18, 1.88)`函数，`this`指向全局对象`window`，在严格模式下为`undefined`；
- 使用`apply`调用`foo.apply("apply", ["kobe", 30, 1.98])`，`this`指向字符串`apply`；
- 使用`call`调用`foo.call("call", "james", 30, 1.98)`，`this`指向字符串`call`；


### [步骤6：验证`bind`方法的使用](06_bind方法实验.html)

本步骤将学习`bind`方法的作用和使用方法。

#### 预期结果
- 使用`bind`方法绑定`this`指向，`this`指向绑定对象。


### [步骤7：验证特殊场景中的`this`绑定](07_特殊场景this绑定实验.html)

本步骤将研究定时器、事件监听器以及数组的`forEach`方法如何处理`this`指向`this`指向。

#### 预期结果
- 使用`setTimeout`绑定`this`指向，`this`指向全局对象`window`（在非严格模式下）；
- 使用`addEventListener`和`onclick`绑定`this`指向，`this`指向绑定对象；
- 使用`forEach`绑定`this`指向，`this`指向绑定对象。



## 问题反馈

有任何问题，建议通过 [Github issues](https://github.com/Hlxuan/javascript-this/issues) 反馈或扫码进入「反馈系统」发起反馈。

| 反馈系统网页端                                             | 反馈系统小程序端                                                   |
| ---------------------------------------------------------- | ------------------------------------------------------------------ |
| ![](https://res.hlxuan.top/opendoc/feedback/web/other.png) | ![](https://res.hlxuan.top/opendoc/feedback/miniprogram/other.png) |

反馈系统网页端：[https://www.hlxuan.top/feedback](https://www.hlxuan.top/feedback/add?section_id=1000)


## 我的网站
[hlxuan的树屋](https://www.hlxuan.top)

[Hlxuan的开放文档](https://docs.hlxuan.top)


## 支持作者

如果你觉得本项目对你有帮助，欢迎给我打赏一杯咖啡哈~

If you think this project will help you, you can buy the author a cup of coffee~


| 支付宝<br>Alipay                                              | 微信<br>WeChat                                                |
| ------------------------------------------------------------- | ------------------------------------------------------------- |
| ![](https://res.hlxuan.top/opendoc/support-author/alipay.png) | ![](https://res.hlxuan.top/opendoc/support-author/weixin.png) |


## 公众号
微信搜索「**黄朗轩**」关注我的公众号，我们一起探索～
![](https://res.hlxuan.top/opendoc/gzh-banner.png)