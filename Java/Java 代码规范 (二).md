Java 中的集合处理是日常开发中比较常用的技术，手册中关于的集合部分也是开发中经常遇到的问题，因此这部分还是非常值得开发人员参考和学习的。

### 集合处理

1. 关于 `hashCode` 和 `equals` 的处理，遵顼以下规则：
  - 只要重写 `equals`，就必须重写 `hashCode`
  - 因为 `Set` 存储的是不重复的对象，依据 `hashCode` 和 `equals` 进行判断，所以 `Set` 存储的 对象必须重写这两个方法
  - 如果自定义对象做为 `Map` 的键，那么必须重写 `hashCode` 和 `equals`

2. 泛型通配符 `<? extends T>` 来接收返回的数据，此写法的泛型集合不能使用 `add` 方法。例如，苹果装箱后返回一个 `<? extends Fruits>` 对象，此对象就不能往里加任何水果包括苹果

3. 不要在 `foreach` 循环里进行元素的 `remove / add` 操作。`remove` 元素请使用 `Iterator` 方式，如果并发操作，需要对 `Iterator` 对象加锁
  ``` java
  // 反例： 
  List<String> a = new ArrayList<String>(); 
  a.add("1"); 
  a.add("2"); 
  for (String temp : a) { 
      if ("1".equals(temp)) { 
          a.remove(temp);
      } 
  }
  
  // 正例：
  Iterator<String> it = a.iterator(); 
  while(it.hasNext()) { 
      String temp =
      it.next();
      if (删除元素的条件) { 
          it.remove();
      }
  }
  ```

4. 在 JDK7 版本以上，`Comparator` 要满足自反性，传递性，对称性，不然 `Arrays.sort， Collections.sort` 会报 `IllegalArgumentException` 异常

5. 集合初始化时，尽量指定集合初始值大小

6. 使用 `entrySet` 遍历 `Map` 类集合 KV，而不是 `keySet` 方式进行遍历。`keySet` 其实是遍历了 2 次，一次是转为 `Iterator` 对象，另一次是从 `hashMap` 中取出 `key` 所对应的 `value`。而 `entrySet` 只是遍历了一次就把 `key` 和 `value` 都放到了 `entry`中，效率更高，如果是 JDK8，使用 `Map.foreach` 方法。

7. 高度注意 `Map` 类集合 `K/V` 能不能存储 `null` 值的情况

| 集合类             | Key          | Value        | Super       | 说明       |
| ----------------- | ------------ | ------------ | ----------- | ---------- |
| Hashtable         | 不允许为 null | 不允许为 null | Dictionary  | 线程安全   |
| ConcurrentHashMap | 不允许为 null | 不允许为 null | AbstractMap | 分段锁技术 |
| TreeMap           | 不允许为 null | 允许为 null   | AbstractMap | 线程不安全 |
| HashMap           | 允许为 null   | 允许为 null   | AbstractMap | 线程不安全 | 
