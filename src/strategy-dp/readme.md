### 优缺点
#### 1.优点
+ 你可以在运行时切换对象内的算法。
+ 你可以将算法的实现和使用算法的代码隔离开来。
+ 你可以使用组合来代替继承。
+ 开闭原则: 你无需对上下文进行修改就能够引入新的策略。
#### 2.缺点
+ 如果你的算法极少发生改变， 那么没有任何理由引入新的类和接口。 使用该模式只会让程序过于复杂。
+ 客户端必须知晓策略间的不同——它需要选择合适的策略。

### 使用场景
+ 当你想使用对象中各种不同的算法变体，并希望能在运行时切换算法时，可使用策略模式。
+ 当你有许多仅在执行某些行为时略有不同的相似类时，可使用策略模式。
+ 如果算法在上下文的逻辑中不是特别重要，使用该模式能将类的业务逻辑与其算法实现细节隔离开来。
+ 当类中使用了复杂条件运算符以在同一算法的不同变体中切换时，可使用该模式。
  + 内存淘汰策略(fifo,lru,lfu等)
  + 距离度量策略(欧式距离,曼哈顿距离,切比雪夫距离,汉明距离,闵可夫斯基距离,余弦相似度和距离,半正矢距离等)
  + 货物运输策略(铁路,公路,空运,海运)