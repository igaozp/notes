## 目录  
[标题](#headers)  
[加粗强调](#emphasis)  
[列表](#lists)  
[链接](#links)  
[图片](#images)  
[代码高亮](#code)  
[表格](#tables)  
[引用](#blockquotes)  
[内联 HTML](#html)  
[水平线](#hr)  
[换行](#lines)  


<a name="headers"/>

## 标题

```no-highlight
# H1
## H2
### H3
#### H4
##### H5
###### H6

H1 H2 有额外的下划线样式:

Alt-H1
======

Alt-H2
------
```

# H1
## H2
### H3
#### H4
##### H5
###### H6

H1 H2 有额外的下划线样式:

Alt-H1
======

Alt-H2
------


<a name="emphasis"/>

## 强调

```no-highlight

使用 *星号* 或者 _下划线_ 进行斜体强调

使用 **两个星号** 或者 __两条下划线__ 进行加粗强调

使用 **星号 或者 _下划线_** 进行混合强调

使用 ~~两条波浪线~~ 添加删除线效果
```

使用 *星号* 或者 _下划线_ 进行斜体强调

使用 **两个星号** 或者 __两条下划线__ 进行加粗强调

使用 **星号 或者 _下划线_** 进行混合强调

使用 ~~两条波浪线~~ 添加删除线效果


<a name="lists"/>

## 列表

(在示例中，使用 . 来表示前导和尾随的空格)

```no-highlight
1. 有序列表的第一个项目
2. 另一个项目
⋅⋅* 无序列表. 
1. 前面的数字无关紧要
⋅⋅1. 有序的子列表
4. 另一个项目.

⋅⋅⋅在列表中你可以适当的缩进段落。 注意上面的空白行和前导空格.

⋅⋅⋅想要在新段落里另起一行，要在尾部加两个空格⋅⋅
⋅⋅⋅在同一段落里新的一行⋅⋅

* 无序列表使用星号
- 也可以使用减号
+ 也可以使用加号
```

1. 有序列表的第一个项目
2. 另一个项目
  * 无序列表. 
1. 前面的数字无关紧要
  1. 有序的子列表
4. 另一个项目.

   在列表中你可以适当的缩进段落。 注意上面的空白行和前导空格.

   想要在新段落里另起一行，要在尾部加两个空格  
   在同一段落里新的一行  

* 无序列表使用星号
- 也可以使用减号
+ 也可以使用加号


<a name="links"/>

## 链接

有两种方式可以创建链接

```no-highlight
[这是一个内联样式的链接](https://www.google.com)

[这是一个有标题的内联样式的链接](https://www.google.com "Google's Homepage")

[这是一个引用样式的链接][Arbitrary case-insensitive reference text]

[引用仓库相对地址的链接](../blob/master/LICENSE)

[通过数字引用相关链接][1]

或者留空自动引用相关链接[link text itself].

URL或者尖括号中的URL将自动转换成相应的链接 https://github.com 或者 <https://github.com>

引用链接的相关文本

[arbitrary case-insensitive reference text]: https://www.mozilla.org
[1]: http://github.com
[link text itself]: http://www.youtube.com
```

[这是一个内联样式的链接](https://www.google.com)

[这是一个有标题的内联样式的链接](https://www.google.com "Google's Homepage")

[这是一个引用样式的链接][Arbitrary case-insensitive reference text]

[引用仓库相对地址的链接](../blob/master/LICENSE)

[通过数字引用相关链接][1]

或者留空自动引用相关链接[link text itself].

URL或者尖括号中的URL将自动转换成相应的链接 https://github.com 或者 <https://github.com>

引用链接的相关文本

[arbitrary case-insensitive reference text]: https://www.mozilla.org
[1]: http://github.com
[link text itself]: http://www.youtube.com


<a name="images"/>

## 图片

```no-highlight

内联样式: 
![alt text](https://www.google.com/images/branding/googlelogo/2x/googlelogo_color_120x44dp.png "图片文字")

引用样式: 
![alt text][logo]

[logo]: https://www.google.com/images/branding/googlelogo/2x/googlelogo_color_120x44dp.png "图片文字"
```

内联样式: 
![alt text](https://www.google.com/images/branding/googlelogo/2x/googlelogo_color_120x44dp.png "图片文字")

引用样式: 
![alt text][logo]

[logo]: https://www.google.com/images/branding/googlelogo/2x/googlelogo_color_120x44dp.png "图片文字"


<a name="code"/>

## 代码语法及高亮

```no-highlight
使用 `单反引号` 来显示 `代码` 
```

使用 `单反引号` 来显示 `代码` 

代码块可以在开头使用三个单反引号 <code>```</code>, 或者使用四个空格.

<pre lang="no-highlight"><code>```javascript
var s = "JavaScript 语法高亮";
alert(s);
```
 
```python
s = "Python 语法高亮"
print s
```

</code></pre>



```javascript
var s = "JavaScript 语法高亮";
alert(s);
```

```python
s = "Python 语法高亮"
print s
```


<a name="tables"/>

## 表格

```no-highlight
冒号决定表格内容的对齐方向

| Table 1 | Table 2  | Table 3 |
| ------- |:--------:| -------:|
| left    |  center  | right   |

每个表头单元格至少三个破折号，表格中可以内联其他的样式

Markdown | Less | Pretty
--- | --- | ---
*Still* | `renders` | **nicely**
1 | 2 | 3
```

冒号决定表格内容的对齐方向

| Table 1 | Table 2  | Table 3 |
| ------- |:--------:| -------:|
| left    |  center  | right   |

每个表头单元格至少三个破折号，表格中可以内联其他的样式

Markdown | Less | Pretty
--- | --- | ---
*Still* | `renders` | **nicely**
1 | 2 | 3


<a name="blockquotes"/>

## 引用

```no-highlight
> 这是一个单行引用

多行引用

> 这是一句非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常长的句子，自动转化为多行引用。
```

> 这是一个单行引用

多行引用

> 这是一句非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常非常长的句子，自动转化为多行引用。


<a name="html"/>

## 内联 HTML

在 Markdown 也可以书写原生的 HTML 页面

```no-highlight
<dl>
  <dt>Definition list</dt>
  <dd>Is something people use sometimes.</dd>

  <dt>Markdown in HTML</dt>
  <dd>Does *not* work **very** well. Use HTML <em>tags</em>.</dd>
</dl>
```

<dl>
  <dt>Definition list</dt>
  <dd>Is something people use sometimes.</dd>

  <dt>Markdown in HTML</dt>
  <dd>Does *not* work **very** well. Use HTML <em>tags</em>.</dd>
</dl>


<a name="hr"/>

## 水平线

```
至少需要三个相应的字符

---

使用连字符

***

使用星号

___

使用下划线
```

至少需要三个相应的字符

---

使用连字符

***

使用星号

___

使用下划线


<a name="lines"/>

## 换行

单次点击回车会完成换行操作，两次点击回车会完成更换段落的操作。

```
这是一句话

这也是一句话，点击两次回车后这句话属于新的一行

这是一句话
这是也是一句话，点击一次回车后这句话还是在同一行中
```

这是一句话

这也是一句话，点击两次回车后这句话属于新的一行

这是一句话
这是也是一句话，点击一次回车后这句话还是在同一行中
