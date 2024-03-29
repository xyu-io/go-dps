### 简介
* 享元模式只是一种优化。在应用该模式之前，你要确定程序中存在与大量类似对象同时占用内存相关的内存消耗问题，并且确保该问题无法使用其他更好的方式来解决。
* 享元（Flyweight）类包含原始对象中部分能在多个对象中共享的状态。同一享元对象可在许多不同情景中使用。 
* 享元中存储的状态被称为“内在状态”。传递给享元方法的状态被称为“外在状态”。
* 情景（Context）类包含原始对象中各不相同的外在状态。情景与享元对象组合在一起就能表示原始对象的全部状态。
* 客户端（Client）负责计算或存储享元的外在状态。
  * 在客户端看来，享元是一种可在运行时进行配置的模板对象，具体的配置方式为向其方法中传入一些情景数据参数。
* 享元工厂（Flyweight Factory）会对已有享元的缓存池进行管理。
  * 有了工厂后，客户端就无需直接创建享元，它们只需调用工厂并向其传递目标享元的一些内在状态即可。
  * 工厂会根据参数在之前已创建的享元中进行查找，如果找到满足条件的享元就将其返回；
  * 如果没有找到就根据参数新建享元。
### 优缺点
#### 1.优点
* 如果程序中有很多相似对象，拥有相同的属性，那么使用享元模式可以节省大量内存。
#### 2.缺点
* 时间换空间，每次调用享元方法时都需要重新计算部分情景数据。
* 代码会变得更加复杂。
#### 使用场景
* 仅在程序必须支持大量对象且没有足够的内存容量时使用享元模式。
  * 角色资源分配（衣服，饭菜配套）
  * 内外资源属性值的差异
  * 人员的种类权限（部门差异，上下级差异）