最近在写项目时，想给领域模型中的类添加注释，自己首先想到的是将它们标记为 `Java Bean` 或者 `POJO`，知道它们在概念上很接近，但不知道这两者的具体区别，所以搜索了相关资料来谈一谈 `Java Bean` 和 `POJO` 以及其他相关的概念。

### Java Bean
只要学过 Java，不管是在学校里教的还是自学的都会或多或少地提过 `Java Bean` 的概念，他们会告诉你 `Java Bean` 是一个类，类里面封装了 `getter` 和 `setter` 方法，但这仅仅是一部分，一个完整的 `Java Bean` 至少满足以下的条件：
  - 有一个默认的 `public` 构造方法
  - 类的属性通过 `get` 和 `set` 方法来访问，这意味着属性要设置为 `private`，同时 `get` 和 `set` 方法与属性名的大小也需要对应，例如 `public String getName() {}`
  - 类需要序列化，也就是需要继承 `Serializable` 接口

### POJO
`POJO` (Plain Old Java Object) 即简单 Java 对象，由 Martin Fowler 等人创造的，作为一种对普通 Java 对象的称呼。POJO 的包含的东西更加广泛，诸如 `PO` (`Persistant Object` 持久对象) `DTO` (`Data Transfer Object` 传输对象) `VO` (`View Object` 表现对象) 等都可以归为 POJO 的概念中。

### 总结
在实际的应用中两者的区别并不是太大，也没有必要特意强调两者的区别，同时一个 `Java` 对象既可以是 `Java Bean` 也可以是 `POJO`。