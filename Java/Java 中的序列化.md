在日常的项目开发过程中可能会遇到序列化的问题，而且多半与数据的存储相关，同时的序列化的过程并不会在代码中的有过多的体现，很容易忽视它的存在，接下来将介绍序列化的概念以及序列化的用途。

### 什么是序列化？
维基百科中的定义：`序列化（serialization）在计算机科学的资料处理中，是指将数据结构或物件状态转换成可取用格式（例如存成档案，存于缓冲，或经由网络中传送），以留待后续在相同或另一台计算机环境中，能恢复原先状态的过程。依照序列化格式重新获取字节的结果时，可以利用它来产生与原始物件相同语义的副本。` 简单的来讲就是将某种数据结构或者对象转换成一种数据格式，数据格式可以通过网络传送或者存入数据库中，同时可以根据数据格式还原出原来的数据结构（反序列化）。在 Java 中，对象只有在 JVM 运行时才会存在，如果想要把对象存储到本地或者发送到远程的服务器，则必须通过序列化将对象转换成相应的子节然后进行存储或者传送，之后再将子节组装成对象。


### 为什么需要序列化？
在以下场景中都会遇到序列化：
  - 将对象状态保存到文件或者数据库中
  - 通过 socket 在网络中传送对象
  - 通过 RMI (远程方法调用) 传输对象

通过序列化将可以将一个复杂的对象转化成相应的子节，这为数据的持久化提供了方便，或者说是为持久化提供了前提条件。如果想要在网络中直接传送对象，服务器是无法判断传递对象的，无法通过 Java 的字节码识别出对象，所以必须将对象序列化，传送完成后在服务器端反序列化，服务器才可能正常地使用传递过来的对象。

### 如何序列化？
在 Java 中如果想要序列化，类必须实现 `Serializable` 接口，下面是一个简单的序列化和反序列化的例子：

需要序列化的类
``` java
public class User implements java.io.Serializable {
   public String userName;
   public String email;
   public String password;
}
```

序列化的过程
``` java
import java.io.*;
public class SerializeDemo {
   public static void main(String [] args) {
      User user = new User();
      user.userName = "username";
      user.eamil = "email";
      user.password = "password";

      try {
         FileOutputStream fileOut = new FileOutputStream("temp");
         ObjectOutputStream nout = new ObjectOutputStream(fileOut);
         out.writeObject(user);
         out.close();
         fileOut.close();
      } catch (IOException e) {
         e.printStackTrace();
      }
   }
}
```

反序列化过程
``` java
import java.io.*;
public class DeserializeDemo {

   public static void main(String [] args) {
      User user = null;

      try {
         FileInputStream fileIn = new FileInputStream("temp");
         ObjectInputStream in = new ObjectInputStream(fileIn);
         user = (User) in.readObject();
         in.close();
         fileIn.close();
      } catch (IOException e) {
         e.printStackTrace();
         return;
      } catch (ClassNotFoundException c) {
         c.printStackTrace();
         return;
      }
  }
}
```