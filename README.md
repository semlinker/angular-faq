# Angular FAQ

> 后期会对问题进行分类(初级、中级、高级)，给您带来不便深表歉意。欢迎有兴趣的朋友，一起维护哈！

## 目录

### [TypeScript](#typescript)

- [面向对象编程中类的概念是什么？](#面向对象编程中类的概念是什么)
- [面向对象编程中继承的概念是什么？](#面向对象编程中继承的概念是什么)
- [什么是接口？](#什么是接口)
- [什么是泛型？](#什么是泛型)
- [什么是枚举？](#什么是枚举)
- [为什么 ES6 或 TypeScript 中的 Class 不会自动提升？](#为什么-es6-或-typescript-中的-class-不会自动提升)
- [TypeScrip 中类静态属性和成员属性有什么区别？](#typescrip-中类静态属性和成员属性有什么区别)

### [RxJS](#rxjs-1)

- [Pull 模式 与 Push 模式有什么区别？](#pull-模式-与-push-模式有什么区别)
- [Observable 与 Promise 有什么区别？](#observable-与-promise-有什么区别)
- [RxJS 中 Subject 有什么特点？](#rxjs-中-subject-有什么特点)
- [RxJS 中 BehaviorSubject、ReplaySubject、AsyncSubject 各有什么作用？](#rxjs-中-behaviorsubjectreplaysubjectasyncsubject-各有什么作用)

### [Common](#common-1)

- [Angular 1.x 与 Angular 4.x 区别大么？](#angular-1x-与-angular-4x-区别大么)
- [Angular 2.x 与 Angular 4.x 区别大么？](#angular-2x-与-angular-4x-区别大么)
- [AngularJS 1.x DI 系统有什么问题？](#angularjs-1x-di-系统有什么问题)
- [constructor 与 ngOnInit 的应用场景是什么？](#constructor-与-ngoninit-的应用场景是什么)
- [ElementRef 有什么作用？](#elementref-有什么作用)
- [Angular 开发 AppService 时，@Injectable() 是必须的么？](#angular-开发-appservice-时injectable-是必须的么)
- [Angular 中使用 [innerHtml] 时内容被转义了要怎么办？](#angular-中使用-innerhtml-时内容被转义了要怎么办)

### [Provider](#provider-1)

- [Angular 中 forwardRef 有什么作用？](#angular-中-forwardref-有什么作用)
- [使用字符串作为 Token 会有什么问题？](#使用字符串作为-token-会有什么问题)
- [Angular 中 Provider 的作用是什么？](#angular-中-provider-的作用是什么)
- [Angular 中配置 Provider 有哪几种方式？](#angular-中配置-provider-有哪几种方式)
- [为什么 useClass 可以使用简洁的语法？](#为什么-useclass-可以使用简洁的语法)
- [Angular 中 multi Provider 有什么作用？](#angular-中-multi-provider-有什么作用)

### [Component](#component-1)

- [Angular 中 ViewEncapsulation 模式分为哪几种？](#angular-中-viewencapsulation-模式分为哪几种)
- [Angular 中宿主元素是什么？](#angular-中宿主元素是什么)
- [Angular 中组件如何实现继承？](#angular-中组件如何实现继承)
- [Angular 中如何传递异步数据？](#angular-中如何传递异步数据)
- [Angular 组件通信有哪些方式？](#angular-组件通信有哪些方式)

### [Directive](#directive-1)

- [Angular 指令分为哪几种？](#angular-指令分为哪几种)
- [Angular 中指令与组件之间有什么联系？](#angular-中指令与组件之间有什么联系)
- [使用 `[hidden]` 属性控制元素可见性有什么问题？](#使用-hidden-属性控制元素可见性有什么问题)
- [自定义属性指令中的 `ElementRef` 与 `Renderer` 有什么作用？](#自定义属性指令中的-elementref-与-renderer-有什么作用)
- [自定义结构指令中的 `TemplateRef` 与 `ViewContainerRef` 有什么作用？](#自定义结构指令中的-templateref-与-viewcontainerref-有什么作用)
- [注册指令生命周期钩子时，一定要实现对应的接口么?](#注册指令生命周期钩子时一定要实现对应的接口么)
- [为什么在构造函数中是获取不到输入属性的值？](#为什么在构造函数中是获取不到输入属性的值)

### [Decorator](#decorator-1)

- [装饰器是什么？](#装饰器是什么)
- [装饰器有几种分类？](#装饰器有几种分类)
- [@Component 中 `@` 的有什么作用？](#component-中--的有什么作用)
- [为什么在构造函数中，非 Type 类型的参数只能用 @Inject(Something) 的方式注入？](#为什么在构造函数中非-type-类型的参数只能用-injectsomething-的方式注入-)
- [@Input 装饰器的作用是什么？](#input-装饰器的作用是什么)
- [@Output 装饰器的作用是什么?](#output-装饰器的作用是什么)
- [@Input 与 inputs 有什么区别？](#input-与-inputs-有什么区别)
- [使用@Input 与 @Output 有什么注意事项？](#使用input-与-output-有什么注意事项)
- [@ViewChild 与 @ViewChildren 装饰器的作用是什么？](#viewchild-与-viewchildren-装饰器的作用是什么)
- [@ContentChild 与 @ContentChildren 装饰器的作用是什么？](#contentchild-与-contentchildren-装饰器的作用是什么)
- [@ViewChild 与 @ContentChild 有什么区别？](#viewchild-与-contentchild-有什么区别)
- [@HostListener 与 @HostBinding 有什么用？](#hostlistener-与-hostbinding-有什么用)
- [为什么在 Root Component 中无法使用 `ng-content`？](#为什么在-root-component-中无法使用-ng-content)

### [Form](#form-1)

- [模板驱动与模型驱动表单各有什么特点？](#模板驱动与模型驱动表单各有什么特点)
- [Angular 中如何使用模板驱动表单？](#angular-中如何使用模板驱动表单)
- [Angular 中如何使用模型驱动表单？](#angular-中如何使用模型驱动表单)
- [form 表单上的 `novalidate` 属性作用是什么？](#form-表单上的-novalidate-属性作用是什么)
- [表单控件的状态除了 `touched` 外，还包含其它几种状态？](#表单控件的状态除了-touched-外还包含其它几种状态)
- [表单控件上 `#userName` 和 `#userName="ngModel"` 这两种方式有什么区别？](#表单控件上-username-和-usernamengmodel-这两种方式有什么区别)
- [ngModelGroup 有什么作用？](#ngmodelgroup-有什么作用)
- [Angular 表单中 patchValue 与 setValue 方法有什么区别？](#angular-表单中-patchvalue-与-setvalue-方法有什么区别)
- [Angular 中内置验证器有哪一些？](#angular-中内置验证器有哪一些)
- [Angular 中如何自定义验证指令？](#angular-中如何自定义验证指令)
- [Angular 中如何自定义表单控件？](#angular-中如何自定义表单控件)

### [ChangeDetection](#changedetection-1)

- [ChangeDetectionStrategy 变化检测策略总共有几种？](#changedetectionstrategy-变化检测策略总共有几种)
- [变化检测器的状态有哪几种？](#变化检测器的状态有哪几种)

### [Pipe](#pipe-1)

- [Angular 内置管道有哪一些？](#angular-内置管道有哪一些)
- [Angular 中管道分为哪几类？](#angular-中管道分为哪几类)
- [Angular 中怎么定义一个管道？](#angular-中怎么定义一个管道)

### Resources

- [Frameworks](#frameworks)
- [Blogs](#blogs)
- [Tools](#tools)
- [Platforms](#platforms)


## TypeScript

### 面向对象编程中类的概念是什么？

虽然 JavaScript 中有类的概念，但是可能大多数 JavaScript 程序员并不是非常熟悉类，这里对类相关的概念做一个简单的介绍。

- 类 (Class)：一种面向对象计算机编程语言的构造，是创建对象的蓝图，描述了所创建的对象共同的属性和方法。
- 对象 (Object)：类的实例，通过 `new` 创建
- 面向对象 (OOP) 的三大特性：封装、继承、多态
- 封装 (Encapsulation)：将对数据的操作细节隐藏起来，只暴露对外的接口。外界调用端不需要知道细节，就能通过对外提供的接口来访问该对象，同时也保证了外界无法任意更改对象内部的数据
- 继承 (Inheritance)：子类继承父类，子类除了拥有父类的所有特性外，还可以扩展自有的功能特性
- 多态 (Polymorphism)：由继承而产生了相关的不同的类，对同一个方法可以有不同的响应。比如 `Cat` 和 `Dog` 都继承自 `Animal`，但是分别实现了自己的 `eat()` 方法。此时针对某一个实例，我们无需了解它是 `Cat` 还是 `Dog`，就可以直接调用 `eat()` 方法，程序会自动判断出来应该如何执行 `eat()`
- 存取器（getter & setter）：用于属性的读取和赋值
- 修饰符（Modifiers）：修饰符是一些关键字，用于限定成员或类型的性质。比如 `public` 表示公有属性或方法
- 抽象类（Abstract Class）：抽象类是供其他类继承的基类，抽象类不允许被实例化。抽象类中的抽象方法必须在子类中被实现
- 接口（Interfaces）：不同类之间公有的属性或方法，可以抽象成一个接口。接口可以被类实现（implements）。一个类只能继承自另一个类，但是可以实现多个接口。

### 面向对象编程中继承的概念是什么？

> **继承**（英语：inheritance）是[面向对象](https://zh.wikipedia.org/wiki/%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1)软件技术当中的一个概念。如果一个类别A “继承自” 另一个类别B，就把这个A称为 “B的子类别”，而把B称为“A的父类别”也可以称 “B是A的超类”。**继承可以使得子类别具有父类别的各种属性和方法，而不需要再次编写相同的代码。在令子类别继承父类别的同时，可以重新定义某些属性，并重写某些方法，即覆盖父类别的原有属性和方法，使其获得与父类别不同的功能。**另外，为子类别追加新的属性和方法也是常见的做法。 一般静态的面向对象编程语言，继承属于静态的，意即在子类别的行为在编译期就已经决定，无法在执行期扩充。 —— 维基百科

继承 (Inheritance) 是一种联结类与类的层次模型。指的是一个类 (称为子类、子接口) 继承另外的一个类 (称为父类、父接口) 的功能，并可以增加它自己的新功能的能力，继承是类与类或者接口与接口之间最常见的关系；继承是一种 [is-a ](https://zh.wikipedia.org/wiki/Is-a)关系。

![](https://segmentfault.com//img/bVLPun?w=293&h=204)

### 为什么 ES6 或 TypeScript 中的 Class 不会自动提升？

因为当 class 使用 extends 关键字实现继承的时候，我们不能确保所继承父类是有效的，那么就可能导致一些无法预知的行为。详细的内容可以参考 - [Angular 2 Forward Reference](https://segmentfault.com/a/1190000008626276) 这篇文章。

### TypeScrip 中类静态属性和成员属性有什么区别？

AppComponent.ts

```typescript
class AppComponent {
  static type: string = 'component';
  name: string;

  constructor() {
    this.name = 'AppComponent';
  }
}
```

TS 编译成 ES5 的代码：

```typescript
var AppComponent = (function () {
    function AppComponent() {
        this.name = 'AppComponent';
    }
    return AppComponent;
}());
AppComponent.type = 'component';
```

通过转换后的代码，我们可以知道类中的静态属性是作为 AppComponent 构造函数的一个属性，而成员属性是属于 AppComponent 实例。

## RxJS

### Pull 模式 与 Push 模式有什么区别？

Pull 和 Push 是数据生产者和数据的消费者两种不同的交流方式。

#### 什么是 Pull？

在 "拉" 体系中，数据的消费者决定何时从数据生产者那里获取数据，而生产者自身并不会意识到什么时候数据将会被发送给消费者。

每一个 JavaScript 函数都是一个 "拉" 体系，函数是数据的生产者，调用函数的代码通过 ''拉出" 一个单一的返回值来消费该数据。

```
const add = (a, b) => a + b;
let sum = add(3, 4);
```

ES6介绍了 [iterator迭代器](http://es6.ruanyifeng.com/#docs/iterator) 和 [Generator生成器](http://es6.ruanyifeng.com/#docs/generator) — 另一种 "拉" 体系，调用 `iterator.next()` 的代码是消费者，可从中拉取*多个值*。

#### 什么是 Push？

在 "推" 体系中，数据的生产者决定何时发送数据给消费者，消费者不会在接收数据之前意识到它将要接收这个数据。

[Promise(承诺)](http://es6.ruanyifeng.com/#docs/promise) 是当今 JS 中最常见的 "推" 体系，一个Promise (数据的生产者)发送一个 resolved value (成功状态的值)来执行一个回调(数据消费者)，但是不同于函数的地方的是：Promise 决定着何时数据才被推送至这个回调函数。

RxJS 引入了 Observables (可观察对象)，一个全新的 "推" 体系。一个可观察对象是一个产生多值的生产者，当产生新数据的时候，会主动 "推送给" Observer (观察者)。

|       | 生产者        | 消费者        |
| ----- | ---------- | ---------- |
| pull拉 | 被请求的时候产生数据 | 决定何时请求数据   |
| push推 | 按自己的节奏生产数据 | 对接收的数据进行处理 |

### Observable 与 Promise 有什么区别？

Observable（**可观察对象**）是基于推送（**Push**）运行时执行（**lazy**）的多值集合。

| MagicQ       | 单值                                       | 多值                                       |
| ------------ | ---------------------------------------- | ---------------------------------------- |
| **拉取(Pull)** | [函数](https://developer.mozilla.org/en-US/docs/Glossary/Function) | [遍历器](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Iteration_protocols) |
| **推送(Push)** | [Promise](https://developer.mozilla.org/en-US/docs/Mozilla/JavaScript_code_modules/Promise.jsm/Promise) | [Observable](http://reactivex.io/rxjs/class/es6/Observable.js~Observable.html) |

- Promise
  - 返回单个值
  - 不可取消的
- Observable
  - 随着时间的推移发出多个值
  - 可以取消的
  - 支持 map、filter、reduce 等操作符
  - 延迟执行，当订阅的时候才会开始执行

### RxJS 中 Subject 有什么特点？

Subject 其实是观察者模式的实现，所以当观察者订阅 Subject 对象时，Subject 对象会把订阅者添加到观察者列表中，每当有 subject 对象接收到新值时，它就会遍历观察者列表，依次调用观察者内部的 `next()` 方法，把值一一送出。

Subject 既是 Observable 对象，又是 Observer 对象，当有新消息时，Subject 会对内部的 observers 列表进行组播 (multicast)。Subject 之所以具有 Observable 中的所有方法，是因为 Subject 类继承了 Observable 类，在 Subject 类中有五个重要的方法：

- next - 每当 Subject 对象接收到新值的时候，next 方法会被调用
- error - 运行中出现异常，error 方法会被调用
- complete - Subject 订阅的 Observable 对象结束后，complete 方法会被调用
- subscribe - 添加观察者
- unsubscribe - 取消订阅 (设置终止标识符、清空观察者列表)

详细的内容可以参考 - [RxJS - Subject](https://segmentfault.com/a/1190000008886598)

### RxJS 中 BehaviorSubject、ReplaySubject、AsyncSubject 各有什么作用？

#### BehaviorSubject 的作用

有些时候我们会希望 Subject 能保存当前的最新状态，而不是单纯的进行事件发送，也就是说每当新增一个观察者的时候，我们希望 Subject 能够立即发出当前最新的值，而不是没有任何响应。

#### ReplaySubject 的作用

有些时候我们希望在 Subject 新增订阅者后，能向新增的订阅者重新发送最后几个值，这时我们就可以使用 ReplaySubject 。

#### AsyncSubject 的作用

AsyncSubject 类似于 `last` 操作符，它会在 Subject 结束后发出最后一个值。

详细的内容可以参考 - [RxJS - Subject](https://segmentfault.com/a/1190000008886598)

## Common

### Angular 1.x 与 Angular 4.x 区别大么？

令人抓狂的是，这变化是 "惊天地泣鬼神"。

#### 主要变化的内容

- 数据绑定机制
- 去除 $scope
- 变化检测 - 使用 Zone.js，检测变化(主要是 Event、Timer、XHR 这些事件源，引起的变化)，不需要再使用 $scope.$watch()、$scope.$apply()、$timeout() 等方法。
- 重新设计的 DI 系统，解决 AngularJS 1.x DI 系统中存在的问题
- 组件通信方面，移除了 $broadcast() 、$emit() 等方法
- 重新设计了指令系统，让开发自定义指令变得更简单
- 引入了全新的组件和模块化方案，且 2.3 版本以后还支持组件继承
- 引入了 Render 渲染层，能够更好地实现跨平台
- 引入了视图封装机制，可以灵活地控制视图渲染方式
- 路由支持模块懒加载、预加载等功能
- 编译器支持 AOT 模式，大大减少了包的大小和提高了应用的性能

### Angular 2.x 与 Angular 4.x 区别大么？

令人欣慰的是，Angular 4.x  向后兼容 Angular 2.x 版本。

#### Angular 4.x 主要更新的内容

- 体积更小，速度更快 - Angular应用程序变得更小更快，并且在未来几个月将进一步改进框架。
- 向后兼容 - 该版本向后兼容 2.x 系列
- 更好的模板引擎 - 改进了AoT，将生成的代码的大小减少约60％。如果模板越复杂，那么优化的代码也会越多。
- 动画模块改进 - 将动画部分从@angular/core拆分出来，单独打包。将核心模块精简后，在不使用动画时产品中将不包含冗余的动画代码。如果需要动画，可使用相关功能自行导入。

#### Angular 4.x 新的特性

- 优化了内置指令nglf和ngFor
- 服务端渲染（Angular Universal）
- TypeScript 2.1 和 2.2 的兼容
- 模板的Source Maps

建议新人可以直接学习 Angular 4.x 的内容。

详细的内容可以参考 - [Angular4.0.0正式发布，附新特性及升级指南](https://mp.weixin.qq.com/s?__biz=MzIwNjQwMzUwMQ==&mid=2247485103&idx=1&sn=21dc4fc255fc7ec7d0450c2b123987f6&chksm=9723646da054ed7b893f70501be713864a25f268710990cd64d517013815297811e394587d59&mpshare=1&scene=1&srcid=0326hPdNEf02VmhCiSSpms97&key=dd10c42bc26371bdbd21897ee53ff29cd2517008e5e84dca11d5b40e9803df17f4bec849b580b0e56c6a1b7bdd9d70be0f0875f9d4c5a60687ebe9c75023bc7a272a78b5a769870c790252a9cdeb96ce&ascene=0&uin=NjY5Njk1MDU=&version=12020010&nettype=WIFI&fontScale=100&pass_ticket=o6T399OazPWhRSHEuVQroeEuYrWnbx7co58INRbEi10=)

### AngularJS 1.x DI 系统有什么问题？

- 内部缓存： angular1 应用程序中所有的依赖项都是单例，我们不能控制是否使用新的实例
- 命名空间冲突： 在系统中我们使用字符串来标识 service 的名称，假设我们在项目中已有一个 CarService，然而第三方库中也引入了同样的服务，这样的话就容易出现混淆
- DI 耦合度太高： angular1 中 DI 功能已经被框架集成了，我们不能单独使用它的 DI 特性
- 未能和模块加载器结合： 在浏览器环境中，很多场景都是异步的过程，我们需要的依赖模块并不是一开始就加载好的，或许我们在创建的时候才会去加载依赖模块，再进行依赖创建，而 angualr 的 IoC 容器没法做到这点。

### constructor 与 ngOnInit 的应用场景是什么？

在 Angular 中 constructor 一般用于依赖注入或执行简单的数据初始化操作，ngOnInit 钩子主要用于执行组件的其它初始化操作或获取组件输入的属性值。

```typescript
export class AppComponent {
  name: string = '';

  constructor(public elementRef: ElementRef) { // 使用构造注入的方式注入依赖对象
    this.name = 'Semlinker'; // 执行初始化操作
  }
}
```

详细的内容可以参考 - [Angular 2 constructor & ngOnInit](https://segmentfault.com/a/1190000008685752)

### ElementRef 有什么作用？

在应用层直接操作 DOM，就会造成应用层与渲染层之间强耦合，导致我们的应用无法运行在不同环境，如 `web worker` 中，因为在 web worker 环境中，是不能直接操作 DOM。有兴趣的读者，可以阅读一下 [Web Workers 中支持的类和方法](https://developer.mozilla.org/en-US/docs/Web/API/Web_Workers_API/Functions_and_classes_available_to_workers) 这篇文章。通过 ElementRef 我们就可以封装不同平台下视图层中的 native 元素 (在浏览器环境中，native 元素通常是指 DOM 元素)，最后借助于 Angular 2 提供的强大的依赖注入特性，我们就可以轻松地访问到 native 元素。

详细的内容可以参考 - [Angular 2 ElementRef](https://segmentfault.com/a/1190000008653690)

### Angular 开发 AppService 时，@Injectable() 是必须的么？

如果 AppService 不依赖于其他对象，是可以不用使用 Injectable 类装饰器。当 AppService 需要在构造函数中注入依赖对象，就需要使用 Injectable 类装饰器。比较推荐的做法不管是否有依赖对象，service 中都使用 Injectable 类装饰器。

### Angular 中使用 [innerHtml] 时内容被转义了要怎么办？

Angular 中默认将所有输入值视为不受信任。当我们通过 property，attribute，样式，类绑定或插值等方式，将一个值从模板中插入到DOM中时，Angular 会自帮我们清除和转义不受信任的值。此时，我们 `DomSanitizer` 对象中，提供的 `sanitize()` 方法来解决上述问题。

详细的内容可以参考 - [Angular 2 DomSanitizer](https://segmentfault.com/a/1190000008809095)

## Provider

### Angular 中 forwardRef 有什么作用？

Angular 通过引入 forwardRef 让我们可以在使用构造注入时，使用尚未定义的依赖对象类型。下面我们先看一下如果没有使用 forwardRef ，在开发中可能会遇到的问题：

```typescript
@Injectable()
class Socket {
  constructor(private buffer: Buffer) { }
}

console.log(Buffer); // undefined

@Injectable()
class Buffer {
  constructor(@Inject(BUFFER_SIZE) private size: Number) { }
}

console.log(Buffer); // [Function: Buffer]
```

若运行上面的例子，将会抛出以下异常:

```typescript
Error: Cannot resolve all parameters for Socket(undefined).
Make sure they all have valid type or annotations
```

那么要解决上面的问题，最简单的处理方式是交换类定义的顺序。除此之外，我们还可以使用 Angular  提供的 forward reference 特性来解决问题，具体如下：

```typescript
import { forwardRef } from'@angular2/core';

@Injectable()
class Socket {
  constructor(@Inject(forwardRef(() => Buffer)) 
      private buffer) { }
}

class Buffer {
  constructor(@Inject(BUFFER_SIZE) private size: Number) { }
}
```

详细的内容可以参考 - [Angular 2 Forward Reference](https://segmentfault.com/a/1190000008626276)

### 使用字符串作为 Token 会有什么问题？

Token 的作用是用来标识依赖对象，Token值可能是 Type、InjectionToken、OpaqueToken 类的实例或字符串。通常不推荐使用字符串，因为如果使用字符串存在命名冲突的可能性比较高。在 Angular 4.x 以前的版本我们一般使用 OpaqueToken 来创建 Token，而在 Angular 4.x 以上的版本版本，推荐使用 InjectionToken 来创建 Token 。

详细的内容可以参考 - [如何解决 Angular 2 中 Provider 命名冲突](https://github.com/semlinker/angular2-ionic2/issues/3)。

### Angular 中 Provider 的作用是什么？

Provider 是用来描述与 Token 关联的依赖对象的创建方式。当我们使用 Token 向 DI 系统获取与之相关连的依赖对象时，DI 会根据已设置的创建方式，自动的创建依赖对象并返回给使用者。

#### Provider 接口

```typescript
export interface ClassProvider {
  // 用于设置与依赖对象关联的Token值，Token值可能是Type、InjectionToken、OpaqueToken的实例或字符串
  provide: any; 
  useClass: Type<any>;
  // 用于标识是否multiple providers，若是multiple类型，则返回与Token关联的依赖对象列表
  multi?: boolean; 
}
  
export interface ValueProvider {
  provide: any;
  useValue: any;
  multi?: boolean;
}
  
export interface ExistingProvider {
  provide: any;
  useExisting: any;
  multi?: boolean;
}
  
export interface FactoryProvider {
  provide: any;
  useFactory: Function;
  deps?: any[]; // 用于设置工厂函数的依赖对象
  multi?: boolean;
}
```

### Angular 中配置 Provider 有哪几种方式？

Angular 中配置 Provider 有四种方式，它们分别为：

- useClass


- useValue
- useExisting
- useFactory

#### useClass

```typescript
{ provide: ApiService, useClass: ApiService } // 可使用简洁的语法，即直接使用ApiService
```

#### useValue

```typescript
{ provide: 'API_URL', useValue: 'http://my.api.com/v1' }
```

#### useExisting

```typescript
{ provide: 'ApiServiceAlias', useExisting: ApiService }
```

#### useFactory

```typescript
export function configFactory(config: AppConfig) {
  return () => config.load();
}

{ provide: APP_INITIALIZER, useFactory: configFactory, deps: [AppConfig], multi: true }
```

### 为什么 useClass 可以使用简洁的语法？

当 DI 解析 Providers 时，都会对提供的每个 provider 进行规范化处理，即转换成标准的形式。具体如下：

```typescript
function _normalizeProviders(providers: Provider[], res: Provider[]): Provider[] {
  providers.forEach(b => {
    if (b instanceof Type) { // 支持简洁的语法，转换为标准格式
      res.push({provide: b, useClass: b});
    }
    ...
  });
  return res;
}
```

### Angular 中 multi Provider 有什么作用？

首先我们先来分析一下，若没有设置 multi: true 属性时，使用同一个 token 注册 provider 时，会出现什么问题？

```typescript
class Engine { }
class TurboEngine { }

var injector = ReflectiveInjector.resolveAndCreate([
  provide(Engine, {useClass: Engine}),
  provide(Engine, {useClass: TurboEngine})
]);

var engine = injector.get(Engine); // engine instanceof TurboEngine == true
```

这说明如果使用同一个 token 注册 provider，后面注册的 provider 将会覆盖前面已注册的 provider。此外，Angular 2 使用 multi provider 的这种机制，为我们提供可插拔的钩子(pluggable hooks) 。另外需要注意的是，multi provider是不能和普通的 provider 混用。

详细的内容可以参考 - [Angular 2 Multi Providers](https://segmentfault.com/a/1190000008626215)

## Component

### Angular 中 ViewEncapsulation 模式分为哪几种？

ViewEncapsulation 允许设置三个可选的值：

- ViewEncapsulation.Emulated - 无 Shadow DOM，但是通过 Angular 提供的样式包装机制来封装组件，使得组件的样式不受外部影响。这是 Angular 的默认设置。
- ViewEncapsulation.Native - 使用原生的 Shadow DOM 特性
- ViewEncapsulation.None - 无 Shadow DOM，并且也无样式包装

详细的内容可以参考 - [Angular 2 ViewEncapsulation](https://segmentfault.com/a/1190000008677532)

### Angular 中宿主元素是什么？

宿主元素的概念同时适用于指令和组件。对于指令来说，这个概念是相当简单的。应用指令的元素，就是宿主元素。假设我们已声明了一个 HighlightDirective 指令 (selector: '[exeHighlight]')：

```html
<p exeHighlight>
   <span>高亮的文本</span>
</p>
```

上面 html 代码中，`p` 元素就是宿主元素。如果该指令应用于自定义组件中如：

```html
<exe-counter exeHighlight>
    <span>高亮的文本</span>
</exe-counter>
```

此时 `exe-counter` 自定义元素，就是宿主元素。

详细的内容可以参考 - [Angular 2 HostListener & HostBinding](https://segmentfault.com/a/1190000008878888)

### Angular 中组件如何实现继承？

组件继承涉及以下的内容：

- Metadata：如 `@Input()`、`@Output()`、`@ContentChild/Children`、`@ViewChild/Children` 等。在派生类中定义的元数据将覆盖继承链中的任何先前的元数据，否则将使用基类元数据。
- Constructor：如果派生类未声明构造函数，它将使用基类的构造函数。这意味着在基类构造函数注入的所有服务，子组件都能访问到。
- Lifecycle hooks：如果基类中包含生命周期钩子，如 ngOnInit、ngOnChanges 等。尽管在派生类没有定义相应的生命周期钩子，基类的生命周期钩子会被自动调用。

**需要注意的是，模板是不能被继承的** ，因此共享的 DOM 结构或行为需要单独处理。

详细的内容可以参考 - [Angular 2 Component Inheritance](https://segmentfault.com/a/1190000008976996)

### Angular 中如何传递异步数据？

在父子组件通信时，如果输入属性绑定的数据是异步的，那我们可以使用 *ngIf、ngOnChanges、Observable 等方案解决上述问题。

详细的内容可以参考 - [Angular 2 Pass Async Data](https://segmentfault.com/a/1190000008986205)

### Angular 组件通信有哪些方式？

组件通信的常用方式：@Input、@Output、@ViewChild、模板变量、MessageService、Broadcaster (Angular 1.x $rootScope 中 $on、$broadcast ) 等。

详细的内容可以参考 - [Angular 2 Components Communicate](https://segmentfault.com/a/1190000008959575)

## Directive

### Angular 指令分为哪几种？

- 组件(Component directive)：用于构建UI组件，继承于 Directive 类 
- 属性指令(Attribute directive):  用于改变组件的外观或行为
- 结构指令(Structural directive):  用于动态添加或删除DOM元素来改变DOM布局

详细的内容可以参考 - [Angular 2 Directive](https://segmentfault.com/a/1190000008626070)

### Angular 中指令与组件之间有什么联系？

组件继承于指令，并扩展了与 UI 视图相关的属性，如 template、styles、animations、encapsulation 等。

详细的内容可以参考 -  [Angular 2 Directive Lifecycle](https://segmentfault.com/a/1190000008716308)

![](https://segmentfault.com/img/bVKJFs?w=300&h=280)

### 使用 `[hidden]` 属性控制元素可见性有什么问题？

```html
<div [hidden]="!showGreeting">
  Hello, there!
</div>
```

当在对应的 DOM 元素上设置 `display: flex` 属性时，尽管`[hidden]` 对应的表达式为 `true`，但元素却能正常显示。对于这种特殊情况，则推荐使用 `*ngIf`。

### 自定义属性指令中的 `ElementRef` 与 `Renderer` 有什么作用？

为了能够支持跨平台，Angular 2 通过抽象层封装了不同平台的差异，统一了 API 接口。如定义了抽象类 Renderer 、抽象类 RootRenderer 等。此外还定义了以下引用类型：ElementRef、TemplateRef、ViewRef 、ComponentRef 和 ViewContainerRef 等。

详细内容请参考 - [Angular 2 ElementRef](https://segmentfault.com/a/1190000008653690)

### 自定义结构指令中的 `TemplateRef` 与 `ViewContainerRef` 有什么作用？

#### TemplateRef

用于表示内嵌的 template 模板元素，通过 TemplateRef 实例，我们可以方便创建内嵌视图(Embedded Views)，且可以轻松地访问到通过 ElementRef 封装后的 nativeElement。需要注意的是组件视图中的 template 模板元素，经过渲染后会被替换成 comment 元素。

#### ViewContainerRef

用于表示一个视图容器，可添加一个或多个视图。通ViewContainerRef 实例，我们可以基于 TemplateRef 实例创建内嵌视图，并能指定内嵌视图的插入位置，也可以方便对视图容器中已有的视图进行管理。简而言之，ViewContainerRef 的主要作用是创建和管理内嵌视图或组件视图。

详细的内容可以参考 - [Angular 2 TemplateRef & ViewContainerRef](https://segmentfault.com/a/1190000008672478)

### 注册指令生命周期钩子时，一定要实现对应的接口么?

注册指令生命周期钩子时，实现对应的接口不是必须的，接口可以帮助我们在开发阶段尽早地发现错误，因为我们有可能在注册生命周期钩子的时候，写错了某个钩子的名称，在运行时可能不会抛出任何异常，但页面显示却不是预期的效果，因此建议读者还是遵守该开发规范。另外还要注意的一点是，TypeScript 中定义的接口，是不会编译生成 ES5 相关代码，它只用于编译阶段做校验。

### 为什么在构造函数中是获取不到输入属性的值？

在子组件的构造函数中，是无法获取输入属性的值，只能在 ngOnChanges 或 ngOnInit 钩子中获取到。因为子组件的构造函数会优先执行，当子组件输入属性变化时会自动调用 ngOnChanges 钩子，然后在调用 ngOnInit 钩子，所以在 ngOnInit 钩子内能获取到输入的属性。

详细的内容可以参考 - [Angular 2 constructor & ngOnInit](https://segmentfault.com/a/1190000008685752)

## Decorator

### 装饰器是什么？

- 它是一个表达式
- 该表达式被执行后，返回一个函数
- 函数的入参分别为 targe、name 和 descriptor
- 执行该函数后，可能返回 descriptor 对象，用于配置 target 对象

### 装饰器有几种分类？

- 类装饰器 (Class decorators)
- 属性装饰器 (Property decorators)
- 方法装饰器 (Method decorators)
- 参数装饰器 (Parameter decorators)

详细的内容可以参考 - [Angular 2 Decorators - 1](https://segmentfault.com/a/1190000008626417)

### @Component 中 `@` 的有什么作用？

@Component 中 `@` 是语法糖，用于表示装饰器。

```typescript
import { Component } from '@angular/core';
@Component({
  selector: 'exe-app',
  template: `
   <h1>Hello Angular</h1>
  `,
})
export class AppComponent {
  constructor() { }
}
```

编译后 ES 5 代码：

```typescript
var __decorate = (this && this.__decorate) || function (decorators, target, key, desc) {};
define(["require", "exports", "@angular/core"], function (require, exports, core_1) {
    "use strict";
    var AppComponent = (function () {
        function AppComponent() {
        }
        return AppComponent;
    }());
    AppComponent = __decorate([
        core_1.Component({
            selector: 'exe-app',
            template: "\n   <h1>Hello Angular</h1>\n  ",
        })
    ], AppComponent);
    exports.AppComponent = AppComponent;
});
```

@Component 中 @ 符号的作用是为了告诉 TypeScript 编译器，@ 后面的是装饰器函数或装饰器工厂，需要特殊处理。假设在 @Component({...}) 中去掉 @ 符号，那么变成了普通的函数调用，这样马上就会报错，因为我们并没有定义 Component 函数。通过观察转换后的代码，我们发现 @Component({...}) 被转换成 core_1.Component ，它就是从 `@angular/core` 导入的装饰器函数。

### 为什么在构造函数中，非 Type 类型的参数只能用 @Inject(Something) 的方式注入 ？

因为只有是 Type 类型的对象，才会被 TypeScript 编译器编译。

详细的内容可以参考 - [Angular 2 Inject](https://segmentfault.com/a/1190000008634359)

### @Input 装饰器的作用是什么？

@Input 是属性装饰器，用来定义组件内的输入属性。在实际应用场合，我们主要用来实现父组件向子组件传递数据。Angular 应用是由各式各样的组件组成，当应用启动时，Angular 会从根组件开始启动，并解析整棵组件树，数据由上而下流下下一级子组件。

![](https://segmentfault.com/img/bVK0py?w=330&h=240)

详细的内容可以参考 - [Angular 2 Input](https://segmentfault.com/a/1190000008780672)

### @Output 装饰器的作用是什么?

Output 是属性装饰器，用来定义组件内的输出属性。在 [Angular 2 Input](https://segmentfault.com/a/1190000008780672) 文章中，我们介绍了 Input 装饰器的作用，也了解了当应用启动时，Angular 会从根组件开始启动，并解析整棵组件树，数据由上而下流下下一级子组件。而我们今天介绍的 Output 装饰器，是用来实现子组件将信息通过事件的形式通知到父级组件。具体如下图所示：

![](https://segmentfault.com/img/bVK3VM?w=417&h=250)

详细的内容可以参考 - [Angular 2 Output](https://segmentfault.com/a/1190000008794323)

### @Input 与 inputs 有什么区别？

相同点：

- 它们都是用来定义输入属性

不同点：

- inputs 定义在指令的 metadata 信息中，开发者对指令的输入属性一目了然。此外对于未选用 TypeScript 作为开发语言的开发者，也只能在 metadata 中定义指令的输入属性。
- @Input 属于属性装饰器，通过它我们可以一起定义属性的访问描述符 (public、private、protected)：

```typescript
@Input() public attr: string;
```

### 使用@Input 与 @Output 有什么注意事项？

坚持使用 @Input 和 @Output ，而非 @Directive 和 @Component 装饰器的 inputs 和 outputs 属性：

- 易于在类里面识别哪些属性是输入属性或输出属性。

坚持把 @Input 或者 @Output 放到所装饰的属性的同一行：

- 如果需要重命名与`@Input`或者`@Output`关联的属性或事件名，你可以在一个位置修改。

避免为输入和输出属性指定别名

- 同一个属性有两个名字（一个对内一个对外）很容易导致混淆。

详细的内容可以参考 - [Angular 2 风格指南 - STYLE 05-12](https://angular.cn/docs/ts/latest/guide/style-guide.html) 

### @ViewChild 与 @ViewChildren 装饰器的作用是什么？

- @ViewChild 属性装饰器，用来从模板视图中获取匹配的元素。它支持 Type 类型或 string 类型的选择器，同时支持设置 read 查询条件，以获取不同类型的实例。


- @ViewChildren 属性装饰器是用来从模板视图中获取匹配的多个元素，返回的结果是一个 QueryList 集合。

详细的内容可以参考 - [Angular 2 ViewChild & ViewChildren](https://segmentfault.com/a/1190000008695459)

### @ContentChild 与 @ContentChildren 装饰器的作用是什么？

- @ContentChild 属性装饰器，用来从通过 Content Projection 方式 (ng-content) 设置的视图中获取匹配的元素。
- @ContentChild 属性装饰器，从通过 Content Projection 方式设置的视图中获取匹配的多个元素，返回的结果是一个 QueryList 集合。

详细的内容可以参考 - [Angular 2 ContentChild & ContentChildren](https://segmentfault.com/a/1190000008707828)

### @ViewChild 与 @ContentChild 有什么区别？

相同点

- 都是属性装饰器
- 都有对应的复数形式装饰器：ContentChildren、ViewChildren
- 都支持 `Type<any>`|Function|string 类型的选择器

不同点

- ContentChild 用来从通过 Content Projection 方式 (ng-content) 设置的视图中获取匹配的元素
- ViewChild 用来从模板视图中获取匹配的元素
- 在父组件的 ngAfterContentInit 生命周期钩子中才能成功获取通过 ContentChild 查询的元素
- 在父组件的 ngAfterViewInit 生命周期钩子中才能成功获取通过 ViewChild 查询的元素

### @HostListener 与 @HostBinding 有什么用？

@HostListener 是属性装饰器，用来为宿主元素添加事件监听。而 @HostBinding 也是属性装饰器，用来动态设置宿主元素的属性值。

详细的内容可以参考 - [Angular 2 HostListener & HostBinding](https://segmentfault.com/a/1190000008878888)

### 为什么在 Root Component 中无法使用 `ng-content`？

原因主要有以下几点：

- `<my-app></my-app>` 标签之间的信息是用来表明 Angular 的应用程序正在启动中
- Angular 2 编译器不会处理 `index.html` 文件中设置的绑定信息，另外出于安全因素考虑，为了避免 `index.html` 中的 `{{}}` 插值，被服务端使用的模板引擎处理。

## Form

### 模板驱动与模型驱动表单各有什么特点？

#### **模板驱动(Template-Driven)表单的特点**

- 使用方便
- 适用于简单的场景
- 通过 [(ngModel)] 实现数据双向绑定
- 最小化组件类的代码
- 不易于单元测试

#### **模型驱动(Model-Driven|Reactive)表单的特点**

- 比较灵活
- 适用于复杂的场景
- 简化了HTML模板的代码，把验证逻辑抽离到组件类中
- 方便的跟踪表单控件值的变化
- 易于单元测试

### Angular 中如何使用模板驱动表单？

#### 1.导入 FormsModule 模块

```typescript
import { NgModule } from '@angular/core';
import { BrowserModule } from '@angular/platform-browser';
import { FormsModule } from '@angular/forms';

@NgModule({
  imports: [BrowserModule, FormsModule], // we add FormsModule here
  declarations: [AppComponent],
  bootstrap: [AppComponent]
})
export class AppModule {}
```

#### 2.实际应用

```typescript
<form novalidate>
  <input type="text" name="name" ngModel required>
  <input type="text" name="street" ngModel minlength="3">
  <input type="text" name="city" ngModel maxlength="10">
  <input type="text" name="zip" ngModel pattern="[A-Za-z]{5}">
</form>
```

详细的内容可以参考 - [Angular 4.x Template-Driven Forms](https://segmentfault.com/a/1190000009037539)

### Angular 中如何使用模型驱动表单？

#### 1.导入 ReactiveFormsModule 模块

```typescript
import { ReactiveFormsModule } from '@angular/forms';

@NgModule({
  imports: [BrowserModule, ReactiveFormsModule],
  ...
})
export class AppModule {}
```

#### 2.实际应用

```typescript
@Component({
  selector: 'exe-app',
  template: `
	<form novalidate [formGroup]="form">
  		...
	</form>
  `
})
class AppComponent {
  constructor(private fb: FormBuilder) {}
  ngOnInit() {
    this.form = this.fb.group({
      name: ['', Validators.required],
      street: ['', Validators.minLength(3)],
      city: ['', Validators.maxLength(10)],
      zip: ['', Validators.pattern('[A-Za-z]{5}')]
    });
  }
}
```

详细的内容可以参考 - [Angular 4.x Reactive Forms](https://segmentfault.com/a/1190000009041192)

### form 表单上的 `novalidate` 属性作用是什么？

通常情况下，我们需要为每个 `form` 都添加 `novalidate` 属性，该属性用于禁用浏览器 `native` 表单验证。如果想要开启 `native` 表单验证，只需添加 `ngNativeValidate` 属性。

novalidate

```html
<form novalidate></form>
```

ngNativeValidate

```html
<form ngNativeValidate></form>
```

### 表单控件的状态除了 `touched` 外，还包含其它几种状态？

表单控件有以下 6 种状态，我们可以通过 `#userName="ngModel"` 方式获取对应的状态值。具体状态如下：

- valid - 表单控件有效
- invalid - 表单控件无效
- pristine - 表单控件值未改变
- dirty - 表单控件值已改变
- touched - 表单控件已被访问过
- untouched - 表单控件未被访问过

### 表单控件上 `#userName` 和 `#userName="ngModel"` 这两种方式有什么区别？

- `#userName` - 指向 input 表单控件
- `#userName="ngModel"` - 指向 NgModel 实例

### ngModelGroup 有什么作用？

ngModelGroup 指令是 Angular 提供的另一特殊指令，可以对表单输入内容进行分组，方便我们在语义上区分不同性质的输入。例如联系人的信息包括姓名及住址，现在需对姓名和住址进行精细化信息收集，姓名可精细化成姓和名字，地址可精细化成城市、区、街等。此时就可以将姓名及住址进行分组收集，具体如下:

```html
<form #concatForm = "ngForm">
	<fieldset ngModelGroup="nameGroup" #nameGroup="ngModelGroup">
		<label>姓:</label>
		<input type="text" name="firstname" [(ngModel)]="curContact.firstname" 
               required> 
      	<label>名字:</label>
		<input type="text" name="lastname" [(ngModel)]="curContact.lastname" 	
               required>
	</fieldset>
	<fieldset ngModelGroup="addressGroup" #addressGroup ="ngModelGroup">
		<label>街:</label>
		<input type="text" name="street" [(ngModel)]="curContact.street" required> 			<label>区:</label>
		<input type="text" name="zip" [(ngModel)]="curContact.zip" required> 
        <label>城市:</label>
		<input type="text" name="city" [(ngModel)]="curContact.city" required>
    </fieldset>
</form>
```

上述例子分别对联系人的姓名和住址进行分组， ngModelGroup 将姓和名字的表单内容进行包裹组成姓名分组，将城市、区和街道的表单内容进行包裹组成住址分组。此时concatForm.value值为:

```typescript
{
  nameGroup: {
	firstname: ''，
	lastname: ''，
  }，
  addressGroup: { 
    street: ''， 
    zip: ''， 
    city: ''
  } 
}
```

### Angular 表单中 patchValue 与 setValue 方法有什么区别？

在 Angular 4.x 中有多种方式可以更新表单的值，对于使用响应式表单的场景，我们可以通过框架内部提供的 API ，(如 patchValue 和 setValue )方便地更新表单的值。

#### FormControl

对于 FormControl 对象来说，patchValue() 和 setValue() 这两个方法是等价的。此外 setValue() 方法中做了三件事：

- 更新控件当前值
- 判断是否注册 `onChange` 事件，若有则循环调用已注册的 `changeFn` 函数。
- 重新计算控件的值和验证状态

#### FormGroup

对于 FormGroup 对象来说， setValue() 方法相比 patchValue() 会更严格，会执行多个判断：

- 判断的是否为所有控件都设置更新值
- 判断控件是否存在

而 patchValue() 方法，会先使用 `this.controls[name]` 进行过滤，只更新参数 `value` 中设定控件的值。

详细的内容可以参考 - [Angular 4.x Forms patchValue and setValue](https://segmentfault.com/a/1190000009090037)

### Angular 中内置验证器有哪一些？

目前 Angular 支持的内建 validators 如下：

- required - 设置表单控件值是非空的
- email - 设置表单控件值的格式是 email
- minlength - 设置表单控件值的最小长度
- maxlength - 设置表单控件值的最大长度
- pattern - 设置表单控件的值需匹配 pattern 对应的模式

### Angular 中如何自定义验证指令？

表单是几乎每个 Web 应用程序的一部分。虽然 Angular 为我们提供了几个内置 validators (验证器)，但在实际工作中为了满足项目需求，我们经常需要为应用添加一些自定义验证功能。

详细的内容可以参考 - [Angular 4.x 自定义验证指令](https://segmentfault.com/a/1190000009053752)

### Angular 中如何自定义表单控件？

在 Angular 创建自定义控件，需要考虑以下问题：

- 如何实现 model -> view 的数据绑定?
- 如何实现 view -> model 的数据同步?
- 若需要自定义验证，应该如何实现?
- 如何向DOM元素添加有效性状态，便于设置不同样式?
- 如何让控件可以访问 (accessible)?
- 该控件能应用于 template-driven 表单?
- 该控件能应用于 model-driven 表单?

详细的内容可以参考 - [Angular 4.x 自定义表单控件](https://segmentfault.com/a/1190000009070500)

## ChangeDetection

### ChangeDetectionStrategy 变化检测策略总共有几种？

```typescript
export declare enum ChangeDetectionStrategy {
    OnPush = 0, // 变化检测器的状态值是 CheckOnce
    Default = 1, // 组件默认值 - 变化检测器的状态值是 CheckAlways，即始终执行变化检测
}
```

### 变化检测器的状态有哪几种？

```typescript
export declare enum ChangeDetectorStatus {
    CheckOnce = 0, // 表示在执行detectChanges之后，变化检测器的状态将会变成Checked
    Checked = 1, // 表示变化检测将被跳过，直到变化检测器的状态恢复成CheckOnce
    CheckAlways = 2, // 表示在执行detectChanges之后，变化检测器的状态始终为CheckAlways
    Detached = 3, // 表示该变化检测器树已从根变化检测器树中移除，变化检测将会被跳过
    Errored = 4, // 表示在执行变化检测时出现异常
    Destroyed = 5, // 表示变化检测器已被销毁
}
```

## Pipe

### Angular 内置管道有哪一些？

- String -> String
  - UpperCasePipe
  - LowerCasePipe
  - TitleCasePipe
- Number -> String
  - DecimalPipe
  - PercentPipe
  - CurrencyPipe
- Object -> String
  - JsonPipe
  - DatePipe
- Tools
  - SlicePipe
  - AsyncPipe
  - I18nPluralPipe
  - I18nSelectPipe

详细的内容可以参考 - [Angular 2 Pipe](https://segmentfault.com/a/1190000008646187)

### Angular 中管道分为哪几类？

- pure 管道：仅当管道输入值变化的时候，才执行转换操作，默认的类型是 pure 类型。(备注：输入值变化是指原始数据类型如：string、number、boolean 等的数值或对象的引用值发生变化)。
- impure 管道：在每次变化检测期间都会执行，如鼠标点击或移动都会执行 impure 管道。

### Angular 中怎么定义一个管道？

自定义管道的步骤：

- 使用 @Pipe 装饰器定义 Pipe 的 metadata 信息，如 Pipe 的名称 - 即 name 属性
- 实现 PipeTransform 接口中定义的 transform 方法

RepeatPipe 定义

```typescript
import {Pipe, PipeTransform} from '@angular/core';

@Pipe({name: 'repeat'})
export class RepeatPipe implements PipeTransform {
    transform(value: any, times: number) {
        return value.repeat(times);
    }
}
```

RepeatPipe 使用

```html
<div>
   <p ngNonBindable>{{ 'lo' | repeat:3 }}</p>
   <p>{{ 'lo' | repeat:3 }}</p> <!-- Output: lololo -->
</div>
```

详细的内容可以参考 - [Angular 2 Pipe](https://segmentfault.com/a/1190000008646187)

## Resources

### Frameworks

- [Angular Material 2](https://github.com/angular/material2)
- [Kendo-UI](http://www.telerik.com/kendo-angular-ui/components/)
- [ng2-bootstrap](http://valor-software.com/ng2-bootstrap/#/)
- [primeng](https://github.com/primefaces/primeng)
- [ngSemantic](https://ng-semantic.herokuapp.com/#/)
- [ng-lightning](http://ng-lightning.github.io/ng-lightning/#/components)
- [Onsen UI](https://onsen.io/v2/docs/guide/angular2/)

### Blogs

- [thoughtram](https://blog.thoughtram.io/all/)
- [toddmotto](https://toddmotto.com/)
- [nrwl](https://blog.nrwl.io/)
- [angular-university](http://blog.angular-university.io/)
- [scotch](https://scotch.io/tag/angular-js)
- [medium](https://medium.com/tag/angular2)

### Tools

- [Augury(调试工具)](https://augury.angular.io/)
- [Codelyzer(代码分析)](https://github.com/mgechev/codelyzer)
- [Lite-Server(轻量Node服务器)](https://github.com/johnpapa/lite-server)

### Platforms

- [angular-electron(桌面版)](https://github.com/angular/angular-electron)
- [ionic(mobile app)](http://ionicframework.com/)
- [nativescript-angular](https://github.com/NativeScript/nativescript-angular)
- [angular 2 and react native](http://angular.github.io/react-native-renderer/)
- [universal-windows-app](https://github.com/preboot/angular2-universal-windows-app)
