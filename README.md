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

### [NgModule](#ngmodule-1)

- [我应该把哪些类添加到declarations中？](#我应该把哪些类添加到declarations中)
- [我不应该把哪些类添加到declarations中？](#我不应该把哪些类添加到declarations中)
- [为什么要把同一个组件声明在不同的NgModule属性中？](#为什么要把同一个组件声明在不同的ngmodule属性中)
- [我应该导入什么？](#我应该导入什么)
- [我应该导入 BrowserModule 还是 CommonModule？](#我应该导入-browsermodule-还是-commonmodule)
- [如果我两次导入同一个模块会怎么样？](#如果我两次导入同一个模块会怎么样)
- [我应该导出什么？](#我应该导出什么)
- [我不应该导出什么？](#我不应该导出什么)
- [我可以重新导出类和模块么？](#我可以重新导出类和模块么)
- [forRoot() 方法是什么？](#forroot-方法是什么)
- [为什么服务提供商在特性模块中的任何地方都是可见的？](#为什么服务提供商在特性模块中的任何地方都是可见的)
- [为什么在惰性加载模块中声明的服务提供商只对该模块自身可见？](#为什么在惰性加载模块中声明的服务提供商只对该模块自身可见)
- [如果两个模块提供了同一个服务会怎么样？](#如果两个模块提供了同一个服务会怎么样)
- [我们应该如何把服务的范围限制到模块中？](#我们应该如何把服务的范围限制到模块中)
- [我应该把全应用级提供商添加到根模块(AppModule)还是根组件(AppComponent)中](#我应该把全应用级提供商添加到根模块appmodule还是根组件appcomponent中)
- [我应该把其它提供商注册到模块中还是组件中？](#我应该把其它提供商注册到模块中还是组件中)
- [为什么 SharedModule 为惰性加载模块提供服务是个馊主意？](#为什么-sharedmodule-为惰性加载模块提供服务是个馊主意)
- [为什么惰性加载模块会创建一个子注入器？](#为什么惰性加载模块会创建一个子注入器)
- [我要如何知道一个模块或服务是否已经加载过了？](#我要如何知道一个模块或服务是否已经加载过了)
- [什么是入口组件？](#什么是入口组件)
- [引导组件和入口组件有什么不同？](#引导组件和入口组件有什么不同)
- [什么时候我应该把组件添加到 entryComponents 中？](#什么时候我应该把组件添加到-entrycomponents-中)
- [为什么 Angular 需要入口组件？](#为什么-angular-需要入口组件)
- [SharedModule 有什么用？](#sharedmodule-有什么用)
- [CoreModule 有什么用？](#coremodule-有什么用)

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

### 什么是接口

在面向对象语言中，接口（Interfaces）是一个很重要的概念，它是对行为的抽象，而具体如何行动需要由类（classes）去实现（implements）。

TypeScript 中的接口是一个非常灵活的概念，除了可用于[对类的一部分行为进行抽象](https://ts.xcatliu.com/advanced/class-and-interfaces.html#类实现接口)以外，也常用于对「对象的形状（Shape）」进行描述。

#### 对象的形状

```typescript
interface Person {
  name: string;
  age: number;
}

let semlinker: Person = {
  name: 'semlinker',
  age: **
};
```

#### 可选|只读属性

```typescript
interface Person {
  readonly name: string;
  age?: number;
}
```

#### 函数类型

接口能够描述 JavaScript 中对象拥有的各种各样的外形。 除了描述带有属性的普通对象外，接口也可以描述函数类型。

```typescript
interface SearchFunc {
  (source: string, subString: string): boolean;
}

let mySearch: SearchFunc;
mySearch = function(source: string, subString: string) {
  let result = source.search(subString);
  return result > -1;
}
```

详细的内容可以参考 - [typescript-handbook-interface](https://zhongsp.gitbooks.io/typescript-handbook/content/doc/handbook/Interfaces.html)

### 什么是泛型？

泛型（Generics）是允许同一个函数接受不同类型参数的一种模板。相比于使用 any 类型，使用泛型来创建可复用的组件要更好，因为泛型会保留参数类型。

#### 泛型接口

```typescript
interface GenericIdentityFn<T> {
    (arg: T): T;
}
```

#### 泛型类

```typescript
class GenericNumber<T> {
    zeroValue: T;
    add: (x: T, y: T) => T;
}

let myGenericNumber = new GenericNumber<number>();
myGenericNumber.zeroValue = 0;
myGenericNumber.add = function(x, y) { return x + y; };
```

#### 实际应用

```typescript
// Hero接口定义
interface Hero {
    id: number;
    name: string;
}

getHeroes(): Observable<Hero[]> {
  return Observable.of([
     { id: 1, name: 'Windstorm' },
     { id: 13, name: 'Bombasto' },
     { id: 15, name: 'Magneta' },
     { id: 20, name: 'Tornado' }
  ]);
}
```

上面 `getHeroes(): Observable<Hero[]>` 表示调用 `getHeroes()` 方法后返回的是一个 Observable 对象，`<Hero[]>` 用于表示该 Observable 对象的观察者，将会收到的数据类型。示例中表示将会返回 `<Hero[]>` 英雄列表。

### 什么是枚举？

枚举用来定义一些有名字的数字常量。枚举通过 `enum` 关键字来定义。

```typescript
// angular2/packages/http/src/enums.ts 片段
export enum RequestMethod {
  Get, // 0
  Post, // 1
  Put, // 2
  Delete, // 3
  Options, // 4
  Head, // 5
  Patch // 6
}
```

编译后的 ES 5 代码

```typescript
var RequestMethod;
(function (RequestMethod) {
        RequestMethod[RequestMethod["Get"] = 0] = "Get";
        RequestMethod[RequestMethod["Post"] = 1] = "Post";
        RequestMethod[RequestMethod["Put"] = 2] = "Put";
        RequestMethod[RequestMethod["Delete"] = 3] = "Delete";
        RequestMethod[RequestMethod["Options"] = 4] = "Options";
        RequestMethod[RequestMethod["Head"] = 5] = "Head";
        RequestMethod[RequestMethod["Patch"] = 6] = "Patch";
})(RequestMethod = exports.RequestMethod || (exports.RequestMethod = {}));
```

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

## NgModule

### 我应该把哪些类添加到declarations中？

可以把可声明的类添加到模块 `declarations` 列表中。可声明的类是指：组件、指令和管道。

这些类只能在应用程序的一个并且只有一个模块中声明。只有当它们从属某个模块时，才能在此模块中声明它们。

### 我不应该把哪些类添加到declarations中？

只有可声明的类才能添加到模块的 `declarations` 列表中。以下类不能添加到 `declarations` 列表中：

- 已经在其它模块中声明过的类。无论它来自应用内模块还是第三方模块
- 从其它模块中导入的指令
- 模块类
- 服务类
- 非 Angular 的类和对象，比如：字符串、数字、函数、实体模型、配置、业务逻辑和辅助类

### 为什么要把同一个组件声明在不同的NgModule属性中？

我们经常看到 `AppComponent` 同时出现在 `declarations` 和 `bootstrap` 中。我们还可以看到 `HeroComponent` 也同时出现在 `declarations`、`exports` 和 `entryComponent` 中。

这看起来是多余的，但因为不同的列表有不同的意义，如果仅在一个列表中声明，我们无法推断它是否出现在其它列表中。

### 我应该导入什么？

一句话：导入你需要在当前模块的组件模板中使用的那些公开的 (被导出的) 可声明类。

这意味着要从 `@angular/common` 中导入 `CommonModule` 才能访问 Angular 的内置指令，如 `*ngIf` 和 `*ngFor`。如果你的组件中需要使用 `[(ngModel)]` 双向绑定的功能，就需要从 `@angular/forms` 中导入 `FormsModule`。

需要注意的是，只能在根模块 (AppModule) 中导入 `BrowserModule`。

### 我应该导入 BrowserModule 还是 CommonModule？

几乎所有要在浏览器中使用的应用的根模块 (AppModule ) 都应该从`@angular/platform-browser` 模块中导入`BrowserModule`。

BrowserModule 提供了浏览器平台下运行的基础指令和服务，该模块内部重新导出了 CommonModule，这意味着 AppModule 中组件也可以访问 Angular 的内置指令。

在其它任何模块中都不要导入 `BrowserModule` 。在特性模块和惰性加载模块中应该导入 `CommonModule`。因为它们只需要 Angular 中提供的内置指令，而不需要重新初始化应用级的服务。

特性模块中导入 `CommonModule` 可以让它能用在任何目标平台上，不仅是浏览器平台。

### 如果我两次导入同一个模块会怎么样？

不会有问题。当三个模块全都导入模块 'A' 时，Angular 只会首次遇到时加载一次模块 'A'，之后就不会这么做了。

无论`A`出现在所导入模块的哪个层级，都会如此。 如果模块 'B' 导入模块 'A'、模块 'C' 导入模块 'B'，模块 'D' 导入`[C, B, A]`，那么 'D' 会触发模块 'C' 的加载，'C' 会触发 'B' 的加载，而 'B' 会加载 'A'。 当Angular在 'D' 中想要获取 'B' 和 'A' 时，这两个模块已经被缓存过了，可以立即使用。

Angular 不允许模块之间出现循环依赖，所以不要让模块 'A' 导入模块 'B'，而模块 'B' 又导入模块 'A'。

### 我应该导出什么？

导出其它模块需要引用的可声明类，如果你不导出某个类，它就是私有的，只对当前模块中声明的其它组件可见。

你可以导出任何可声明类 (组件、指令和管道)，而不用管它是声明在当前模块中还是某个导入的模块中。

你也可以重新导出整个已导入的模块，这将导致重新导出模块中导出的所有类。模块甚至还可以导出它未曾导入过的模块。

### 我不应该导出什么？

不要导出的：

- 那些你只想在当前模块中使用的私有组件、指令和管道。如果你不希望在任何模块看到它，就不要导出。
- 不可声明的对象，比如服务、函数、配置、实体模型等
- 纯服务的模块没有公开导出的声明。例如，没有必要重新导出 `HttpModule` ，因为它不导出任何东西。它唯一的用途就是把 Http 相关的服务注册到应用中

### 我可以重新导出类和模块么？

模块是从其它模块中选取类并把它们重新导出成统一、便利的新模块的最佳方式。

模块可以重新导出其它模块，这会导致重新导出它们导出的所有类。Angular 的 BrowserModule 就重新导出了一组模块，例如：

```typescript
exports: [CommonModule, ApplicationModule]
```

> 不要费心去导出纯服务类。纯服务类的模块不会导出任何可供其它模块使用的可声明类。例如，不用重新导出 `HttpModule`，因为它没有导出任何东西。它唯一的用途就是把 Http 相关的服务注册到应用中。

### forRoot() 方法是什么？

静态方法 `forRoot()` 是一个约定，它可以让开发人员更轻松的配置模块的服务提供商。

`RouterModule.forRoot()` 就是一个很好的例子。我们把一个 `Routes` 对象作为参数传给 `RouterModule.forRoot()` 方法，就是为了配置应用级的路由。`RouterModule.forRoot()` 方法返回一个 `ModuleWithProviders` 对象，我们把返回的对象添加到根模块的 `imports` 列表中。

> 只能在应用的根模块中调用并导入 `forRoot()` 方法返回的对象。在其它模块中导入它，特别是惰性加载模块中，是违反设计目标并会导致一个运行时异常。

`RootModule` 也提供了一个静态方法 `forChild`，用于配置惰性加载模块的路由。

**forRoot**和**forChild**都是方法的约定名称，它们分别用于在根模块和特性模块中配置服务。

### 为什么服务提供商在特性模块中的任何地方都是可见的？

列在引导模块的 `@NgModule.providers` 中的服务提供商具有全应用级作用域。往 `@NgModule.providers` 中添加服务提供商将导致该服务被发布到整个应用中。

当我们导入一个模块时，Angular 就会把该模块的服务提供商 (也就是 providers 列表中的内容) 加入该应用的根注入器中，这会让该服务提供商对应用中的所有模块都是可见的。

Angular 就是如此设计的。 通过模块导入来实现可扩展性是 Angular 模块系统的主要设计目标。 把模块的提供商并入应用程序的注入器可以让库模块使用新的服务来强化应用程序变得更容易。 只要添加一次 `HttpModule`，那么应用中的每个组件就都可以发起 Http请求了。

不过，如果你期望模块的服务只对那个特性模块内部声明的组件可见，那么这可能会带来一些问题。 如果 `HeroModule` 提供了一个 `HeroService`，并且根模块 `AppModule` 导入了`HeroModule`，那么任何知道 `HeroService` *类型*的类都可能注入该服务，而不仅是在 `HeroModule `中声明的那些类。

### 为什么在惰性加载模块中声明的服务提供商只对该模块自身可见？

和启动时就加载的模块中的提供商不同，惰性加载模块中的提供商是局限于模块自身。

当 Angular 路由器惰性加载一个模块时，它创建了一个新的运行环境。这个环境拥有自己的注入器，它是应用注入器的直属子级。

路由器把惰性加载模块的提供商和它导入模块的提供商添加到这个子注入器中。

这些提供商不会被拥有相同令牌的应用级别提供商的变化所影响。当路由器在惰性加载环境中创建组件时，Angular 会优先使用惰性加载模块中的服务实例，而不是来自应用的根注入器。

### 如果两个模块提供了同一个服务会怎么样？

当同时加载了两个导入的模块，它们都列出了使用同一个令牌的提供商时，后导入的模块会 "获胜"，这是因为这两个提供商都被添加到了同一个注入器中。

当 Angular 尝试根据令牌注入服务时，它使用第二个提供商来创建并交付服务实例。

每个注入了该服务的类获得的都是由第二个提供商创建的实例。 即使是声明在第一个模块中的类，它取得的实例也是来自第二个提供商的。

### 我们应该如何把服务的范围限制到模块中？

如果一个模块在应用程序启动时就加载，它的`@NgModule.providers`具有**全应用级作用域**。 它们也可用于整个应用的注入中。

导入的提供商很容易被由其它导入模块中的提供商替换掉。 虽然设计如此，但是也可能引起意料之外的结果。

> 作为一个通用的规则，应该*只导入一次*带提供商的模块，最好在应用的*根模块*中。 那里也是配置、包装和改写这些服务的最佳位置。

假设模块需要一个定制过的 `HttpBackend`，它为所有的 Http 请求添加一个特别的请求头。 如果应用中其它地方的另一个模块也定制了`HttpBackend` 或仅仅导入了`HttpModule`，它就会改写当前模块的`HttpBackend`提供商，丢掉了这个特别的请求头。 这样服务器就会拒绝来自该模块的请求。

要消除这个问题，就只能在应用的根模块 `AppModule` 中导入 `HttpModule`。

只要有可能，就让模块惰性加载。Angular 为惰性加载模块提供了独立的子注入器。该模块中的提供商只对由该注入器创建的组件树可见。

继续看了例子，假设某个模块的组件真的需要一个私有的、自定义的 `HttpBackend`。

那就创建一个 "顶级组件" 来扮演该模块中所有组件的根。把这个自定义的 `HttpBackend` 提供商添加到这个顶级组件的 `providers` 列表中，而不是该模块的 `providers` 中。回忆一下，Angular 会为每个组件实例创建一个子注入器，并使用组件自己的 `providers` 来配置这个注入器。

当该组件的子组件需要一个 `HttpBackend` 服务时，Angular 会提供一个局部的 `HttpBackend` 服务，而不是应用根注入器创建的那个服务。此时，子组件将正确发起 http 请求，而不管其它模块对 `HttpBackend` 做了什么？同时需要确保模块中的组件都创建成这个顶级组件的子组件。

### 我应该把全应用级提供商添加到根模块(AppModule)还是根组件(AppComponent)中？

在根模块 (AppModule) 中注册全应用级提供商，而不是 `AppComponent` 中。

惰性加载的模块及其组件可以注入 `AppModule` 中的服务，却不能注入 `AppComponent` 中注册的服务。

只有当该服务必须对 `AppComponent` 组件树之外的组件不可见时，才应该把服务注册进 `AppComponent` 的 `providers` 中。但这是一个不常见的用法，正常情况下，我们是优先把服务提供商注册进模块中，而不是组件中。

Angular 把所有启动期模块的提供商都注册进了应用的根注入器中。这些服务是由根注入器中的提供商创建的，并且在整个应用中都可用。它们具有应用级作用域。

某些服务 (比如 Router) 只有当注册进应用的根注入器时才能正常工作。

相反，Angular 使用 `AppComponent` 自己的注入器注册了 `AppComponent` 的提供商。`AppComponent `服务只在该组件及其子组件树中才能使用。 它们具有组件级作用域。

`AppComponent  `的注入器是根注入器的子级，注入器层次中的下一级。 这对于没有路由器的应用来说几乎是整个应用了。 但这个 "几乎" 对于带路有的应用仍然是不够的。

### 我应该把其它提供商注册到模块中还是组件中？

通常，优先把模块中具体特性的提供商注册到模块中 (`@NgModule.providers`)，而不是组件中 (`@Component.providers`)。

当你必须把服务实例的范围限制到某个组件及其子组件树时，就把提供商注册到该组件中。 指令的提供商也同样照此处理。

需要注意的是，总在根模块中注册全应用级服务，而不要在根组件中。

### 为什么 SharedModule 为惰性加载模块提供服务是个馊主意？

假设把 `UserService` 列在了模块的 `providers` 中。 假设每个模块都导入了这个`SharedModule` 模块。导入 `SharedModule` 的每个模块都会设置 `UserService` 提供商。Angular 把它们中的一个注册到根注入器中。当应用中的某些组件要求注入 `UserService` ，Angular 就会在应用的根注入器中查找它，并交付一个全应用级的 `UserService` 单例对象。

现在，该考虑惰性加载模块了。当路由器惰性加载模块时，它会创建一个子注入器，并且把 `UserService` 的提供商注册到那个子注入器中。子注入器和根注入器是不同的。

当 Angular 创建一个惰性加载的组件时，它必须注入 `UserService` 服务。这时，它会从惰性加载模块的子注入器查找 `UserService` 的提供商，并用它创建一个 `UserService` 的新实例。这个 `UserService` 实例与 Angular 在主动加载的组件中注入的那个全应用级单例对象截然不同。

### 为什么惰性加载模块会创建一个子注入器？

Angular会把 `@NgModule.providers` 中的提供商添加到应用的根注入器中。除非该模块是惰性加载的，这种情况下，它会创建 一 子注入器，并且把该模块的提供商添加到这个子注入器中。

为什么 Angular 不能像主动加载模块那样把惰性加载模块的提供商也添加到应用程序的根注入器中呢？为什么会出现这种不一致？

归根结底，这来自于 Angular 依赖注入系统的一个基本特征： 在注入器还没有被第一次使用之前，可以不断为其添加提供商。 一旦注入器已经创建和开始交付服务，它的提供商列表就被冻结了，不再接受新的提供商。

当应用启动时，Angular 会首先使用所有主动加载模块中的提供商来配置根注入器，这发生在它创建第一个组件以及注入任何服务之前。 一旦应用开始工作，应用的根注入器就不再接受新的提供商了。

之后，应用逻辑开始惰性加载某个模块。 Angular 必须把这个惰性加载模块中的提供商添加到某个注入器中。 但是它无法将它们添加到应用的根注入器中，因为根注入器已经不再接受新的提供商了。 于是，Angular 在惰性加载模块的上下文中创建了一个新的子注入器。

### 我要如何知道一个模块或服务是否已经加载过了？

某些模块及其服务只能被根模块 `AppModule` 加载一次。 在惰性加载模块中再次导入这个模块会[导致错误的行为](https://angular.cn/docs/ts/latest/cookbook/ngmodule-faq.html#q-why-bad)，这个错误可能非常难于检测和诊断。

为了防范这种风险，我们可以写一个构造函数，它会尝试从应用的根注入器中注入该模块或服务。如果这种注入成功了，那就说明这个类是被第二次加载的，我们就可以抛出一个错误，或者采取其它挽救措施。

某些 Angular 模块 (例如 `BrowserModule`) 就实现了构造函数守卫功能。

```typescript
constructor (@Optional() @SkipSelf() parentModule: CoreModule) {
  if (parentModule) {
    throw new Error(
      'CoreModule is already loaded. Import it in the AppModule only');
  }
}
```

### 什么是入口组件？

Angular 中通过组件选择器加载的组件不是入口组件。大多数应用组件都是声明式加载的，Angular 使用该组件的选择器在模板中定位元素，然后创建表现该组件的 HTML，并把它插入 DOM 中所选元素的内部。它们不是入口组件。

用于引导的根 `AppComponent` 就是一个入口组件。虽然它的选择器匹配了 `index.html` 中的一个元素，但是 `index.html` 并不是组件模板，而且 `AppComponent` 选择器也不会在任何组件模板中出现。

Angular 总是会动态加载 `AppComponent` —— 无论把它的类型列在了 `@NgModule.bootstrap`函数中，还是命令式的调用该模块的`ngDoBootstrap`方法来引导它。

在路由定义中用到的组件也同样是入口组件。 路由定义根据类型来引用组件。 路由器会忽略路由组件的选择器 (即使它有选择器)，并且把该组件动态加载到 `RouterOutlet` 元素中。

编译器无法通过在其它组件的模板中查找来发现这些入口组件。 我们必须通过把它们加入 `entryComponents` 列表中来让编译器知道它们的存在。

Angular 会自动把下列类型的组件添加到模块的 `entryComponents` 中：

- 那些出现在 `@NgModule.bootstrap` 列表中的组件。
- 那些被路由定义引用的组件。

### 引导组件和入口组件有什么不同？

引导组件是入口组件的一种。它是被 Angular 的引导 (应用启动) 过程加载到 DOM 中的入口组件。 其它入口组件则是被其它方式动态加载的，比如被路由器加载。

`@NgModule.bootstrap ` 属性告诉编译器这是一个入口组件，同时它应该生成一些代码来用该组件引导此应用。

不需要把组件同时列在 `bootstrap` 和 `entryComponent ` 列表中 —— 虽然这样做也没坏处。

### 什么时候我应该把组件添加到 entryComponents 中？

大多数应用开发者都不需要把组件添加到 `entryComponents` 中。

Angular会自动把恰当的组件添加到*入口组件*中。 列在 `@NgModule.bootstrap` 中的组件会自动加入。 由路由配置引用到的组件会被自动加入。 用这两种机制添加的组件在入口组件中占了绝大多数。

如果你的应用要用其它手段来根据类型引导或动态加载组件，那就得把它显式添加到 `entryComponents` 中。

### 为什么 Angular 需要入口组件？

入口组件也是被声明的。为什么 Angular 编译器不为 `@NgModule.declarations` 中的每个组件都生成一份代码呢？那样就不需要入口组件了。

原因在于 `tree shaking` 。对于产品化的应用，我们希望加载尽可能小的代码。 代码中应该仅仅包括那些实际用到的类。 它应该排除那些我们从未用过的组件，无论该组件是否被声明过。

事实上，大多数库中声明和导出的组件我们都用不到。如果我们从未引用它们，那么`tree shaking` 就会从最终的代码包中把这些组件砍掉。

如果 Angular 编译器为每个声明的组件都生成了代码，那么 `tree shaking` 的优化作用就没了。所以，编译器转而采用一种递归策略，它只为我们用到的那些组件生成代码。

### SharedModule 有什么用？

在实际项目中，我们通常会有一些通用的组件、指令或管道。为了便于统一的维护，我们会定义一个 `SharedModule` 模块，这种模块应该只包含 `declarations` 声明，并且应该导出几乎所有的 `declarations` 声明类。

SharedModule 也可以重新导出其它模块，比如 `CommonModule`、`FormsModule` 和通用的模块 (包含通用 UI组件)。

SharedModule 不应该带有 providers，它导入或重新导出的模块中，也不应该有 `providers` 。如果你要违背这条原则，请务必想清楚你在做什么，并要有充分的理由。

在任何特性模块中 (无论是你在应用启动时主动加载的模块还是之后惰性加载的模块)，你都可以随意导入这个`SharedModule`。

### CoreModule 有什么用？

为了便于统一的管理系统中通用的服务，我们可以创建一个 `CoreModule` 模块。我们可以把 `CoreModule` 当做一个没有 `declarations` 的纯服务模块。

需要注意的是，只能在根模块 (AppModule) 中导入 `CoreModule`。永远不要在除了根模块之外的任何模块导入 `CoreModule`。

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
