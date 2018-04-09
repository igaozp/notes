Java 10 引入了 `var` 保留类型来实现局部变量推断。为了兼容旧版本，`var` 不是关键字，而是一个保留类型，仍然可以使用 `var` 作为为变量和函数名。

与 JavaScript 不同，使用 var 修饰的变量仍然是静态类型，并不是与 JavaScript 类似的动态类型，变量的类型在编译期已经确定，不能像动态类型语言一样在运行时随意改变变量的类型，所以 `var` 的引入使代码更加简洁易读。

我们可以写出这样的代码：
``` java
var i = 0;
var s = "123";
var list = new ArrayList<Integer>();
var map = Map.of(1, "a", 2, "b");
for (var entry: map.entrySet()) {
    System.out.println(entry);
}
for (var j = 0; j < 10; j++) {
    System.out.println(j);
}
```

使用 `var` 声明的变量时必须要在声明的同时初始化：
``` java
var a; // error: 'var' on variable without initializer
a = 0;
```

同时 `var` 不能用于局部变量声明以外的地方，例如：
``` java
public class LocalVariableTypeInference {
    var num = 0; // error: 'var' is not allowed here

    public LocalVariableTypeInference(var i) { // error: 'var' is not allowed here
        try {

        } catch (var e) { // error: 'var' is not allowed here

        }
    }

    var toString() { // error: 'var' is not allowed here
        
    }
}
```

也不能使用 `var` 将变量初始化为 `null`
