# summary essay

[内容导航](#nav)

[这是什么](#what)

[为什么创建这个项目](#why)

[需要做什么](#any)

[与博客有什么区别](#diff)

[如何运行项目](#run)

[如何创建第一个模块(demo)?](#demo)

[帮助](#help)


##### <span id="nav">内容导航</span>

- [如何参与开源项目](open/menu.md)

##### <span id="what">这是什么</span>

- 团队技术交流的轻量级结点

##### <span id="why">为什么创建这个项目</span>

- 工作中聚集团队成员做技术分享的成本太高了，为了充分利用团队成员的闲暇时间沉淀工作中的技能， 经验， 互相学习，增进交流，与凡哥商量后共同创建这个项目 
- 团队review，可以鼓励成员沉淀现有技术栈知识，把新技术运用到项目中并分享， 加速成员成长速度
- 前人栽树， 后人乘凉，通过积累、沉淀、 归类和迭代升级，形成对新人友好的技术文档库

##### <span id="any">需要做什么</span>

- 工作中用到了一个非常巧妙的方法，模式， 算法等， 总结一下
- 对工作框架的理解某一天忽然加深了一些， 分享一下你的收获
- 最近学了一项新技术， 想在此推广一下, 请开始吧~
- 我对这位同学对某个知识点的理解有不同的看法， 我可以帮他完善一下
- 尽管这个项目并不强制我们输出内容，但一定频率的输出对团队成员以及自身的成长都是有好处的， 所以建议能保持一定的连续性
- 对他人的付出给予肯定

##### <span id="diff">与博客有什么区别</span>

- 受众：主要是面向具体的团队成员而非抽象的阅读者，作者和受众的距离很近
- 传播方式： 传统博客信息传递为单向， 这里的信息交互是多向的 

##### <span id="run">如何运行项目</span>

- fork 并 clone 本项目

- 安装gitbook插件

```
npm install -g gitbook-cli
```
- 切换到summary-essay目录然后运行项目

``` 
gitbook serve
```

##### <span id="demo">如何创建第一个模块（demo）</span>

- 在根目录的SUMMARY.md添加文档目录

```
# Summary

* [Introduction](README.md)
* [DemoEmnu](demo/demomenu.md) // 一级目录(链接md文档)
 * [Demo](demo/demo.md) // 二级目录空一格(链接md文档)
```

- 创建对应的目录以及文档


##### <span id="help">帮助</span>

- [gitbook使用方法](http://www.chengweiyang.cn/gitbook/introduction/README.html)

