### ArrayList 初始化操作
`ArrayList` 提供了3个构造方法：
 - 当提供列表初始化的大小时，构造方法会构建相应大小的列表
 - 当提供集合类型参数时会将集合类型转换成相应的列表
 - 当没有提供参数时构造方法会 构建一个默认的空列表
``` java 
    public ArrayList(int initialCapacity) {
        if (initialCapacity > 0) {
            // 初始化相应的大小的列表
            this.elementData = new Object[initialCapacity];
        } else if (initialCapacity == 0) {
            // 初始化一个空的列表
            this.elementData = EMPTY_ELEMENTDATA;
        } else {
            // 参数错误抛出异常
            throw new IllegalArgumentException("Illegal Capacity: "+
                                               initialCapacity);
        }
    }

    public ArrayList() {
        // 初始化一个空的列表
        this.elementData = DEFAULTCAPACITY_EMPTY_ELEMENTDATA;
    }

    public ArrayList(Collection<? extends E> c) {
        // 将集合类型转换成相应的数组列表
        elementData = c.toArray();
        if ((size = elementData.length) != 0) {
            // 转换列表元素的类型
            if (elementData.getClass() != Object[].class)
                elementData = Arrays.copyOf(elementData, size, Object[].class);
        } else {
            // 当集合大小为 0 时，初始化一个空的列表
            this.elementData = EMPTY_ELEMENTDATA;
        }
    }
```