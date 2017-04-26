# Adapter Class/Object（适配器）

在平常开发当中，适配器 ( Adapter ) 是十分常用的模式，比如常用的 RecyclerView 的 Adapter，ListView 的 Adapter 等。但是在经常使用，但是并不知道适配器模式的具体实现原理是什么？那么下面就将结合具体案例分析一下这个适配器模式。

首先先理解什么是适配器？平常在手机充电或者给笔记本电脑充电时，都会使用到充电器。因为我们知道插板上的电压是 220 V ，如果直接连接上设备，则会将给烧坏，那么适配器的作用就是这样 ———— **将原本因接口不匹配而无法在一起工作的两样东西能够在一起工作**

## Adapter Class/Object（适配器）的 UML 类图

这里要说明的是，适配器按类型来分有两种：
 + 类适配器
 + 对象适配器

下面是对应的 UML 类图

> 类适配器

![](https://github.com/InnoFang/DesignPatterns/blob/master/uml/class_adapter.png)

 + Target : 适配器接口
 + Adaptee : 需要适配的角色
 + Adapter : 适配器，将需要适配的角色的对应操作进行适配

![](https://github.com/InnoFang/DesignPatterns/blob/master/uml/object_adapter.png)

 这里的三个角色同上，但是这里使用了组合的方式

那么这里这两种实现方式有什么不同的呢？
 + 相同点：都是将被适配的类的 API 转换成目标类的 API
 + 不同点：
   - 类适配器使用**继承**的方式连接到 Adaptee 类
   - 对象适配器使用**组合**的方式连接到 Adaptee 类

使用组合的方式实现接口兼容的效果更为灵活，好处就是被适配对象中的方法不会暴露出来，而类适配器由于继承了被适配对象，因此也能使用被适配对象中的方法

相比之下，**使用对象适配器模式更加灵活、使用**

## 适配器模式的简单实现