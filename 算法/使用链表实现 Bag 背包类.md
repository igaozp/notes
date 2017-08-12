## 使用链表实现 Bag 背包类

`Bag` 背包类可以用于元素的收集和遍历，类似于 `Set` 集合，但不可以删除其中的元素。在 `Bag` 内部使用节点类 `Node` 来作为链表的每一个节点元素，同时使用链表基本的头插法来实现元素的插入，属于链表最基本、最基础的应用。为了实现元素的迭代， `Bag` 通过自定义的内部类 `ListIterator` 来实现 `Iterable` 接口。

```java
package Base;

import java.util.Iterator;

/**
 * Bag 的链表实现
 * Bag 是一种不支持删除其中元素的集合数据类型，可以用来收集和遍历元素
 *
 * @author igaozp
 * @version 1.0
 * @since 2017-6-30
 * @param <Item> 泛型类型
 */
public class Bag<Item> implements Iterable<Item> {
    // 链表的首节点
    private Node first;

    /**
     * 内部的链表节点类
     */
    private class Node {
        Item item;
        Node next;
    }

    /**
     * 添加元素
     * @param item 向 {@code Bag} 中添加的元素
     */
    public void add(Item item) {
        // 使用头插法插入新的元素
        Node oldFirst = this.first;
        this.first = new Node();
        this.first.item = item;
        this.first.next = oldFirst;
    }

    /**
     * 实现 {@code Iterable} 接口的 {@code iterator} 函数
     * @return 迭代对象
     */
    public Iterator<Item> iterator() {
        return new ListIterator();
    }

    /**
     * {@code ListIterator} 用来实现 {@code Iterable} 接口
     */
    private class ListIterator implements Iterator<Item> {
        private Node current = first;

        /**
         * 检查是否有下一个元素
         * @return {@code true} 有下一个元素
         *         {@code false} 没有下一个元素
         */
        public boolean hasNext() {
            return current != null;
        }

        /**
         * 移除元素，{@code Bag} 中不需要实现
         */
        public void remove() { }

        /**
         * 获取下一个元素
         * @return {@code Item} 泛型类型的对象
         */
        public Item next() {
            Item item = current.item;
            current = current.next;
            return item;
        }
    }
}

```