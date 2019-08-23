# Rxjava

## Rxjava开发中遇到的问题

### 数据类型的转换

```text
string int date 之间的转换
```

### jwt机制与head的运用

5W2H，是英文中最常见的七个问题：
Why（为什么），
What（是什么），
Where（在何处），
When（在何时），
Who（由谁做），
How（怎么做），
和How Much（要多少）的缩写。

## Why
代码简洁：异步操作有Handler、AsyncTask等，但是使用RxJava，就算再多的异步操作，代码逻辑越来越复杂，RxJava依然可以保持清晰的逻辑。
## What
https://github.com/ReactiveX/RxJava
RxJava – Reactive Extensions for the JVM – a library for composing asynchronous and event-based programs using observable sequences for the Java VM
RxJava is a Java VM implementation of Reactive Extensions: a library for composing asynchronous and event-based programs by using observable sequences.

It extends the observer pattern to support sequences of data/events and adds operators that allow you to compose sequences together declaratively while abstracting away concerns about things like low-level threading, synchronization, thread-safety and concurrent data structures.
## How

basic elements
```
1. 被观察者（Observable）
2. 观察者（Observer）
3. 订阅（subscribe)
```

``` java
Observable observable = Observable.create(new ObservableOnSubscribe<Integer>() {
    @Override
    public void subscribe(ObservableEmitter<Integer> e) throws Exception {
        Log.d(TAG, "=========================currentThread name: " + Thread.currentThread().getName());
        e.onNext(1);
        e.onNext(2);
        e.onNext(3);
        e.onComplete();
    }
});
```


Observer Pattern
http://reactivex.io/documentation/operators.html
### Operation 

#### create

#### just

#### from


interval
range
repeat


map
flatmap
cast
flatMapIterable
buffer
groupBy

白河第三方远程门诊、远程会诊通知接口，增加处方主表和处方明细表存储和显示逻辑：
1. 增加了处方表明细表的存储和显示
> a.增加处方表、明细表与业务表的关联关系。其中处方表、明细表不支持更新操作，只能跟随第三方业务主表数据新增或删除
> b.在pr/report附件Tab处提供处方表和明细表查看入口
2. 完善了第三方传值空值的处理
3. 完善了通知服务的相关日志


