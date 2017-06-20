
##### 目录  
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
[Youtube videos](#videos)  

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

## Tables

Tables aren't part of the core Markdown spec, but they are part of GFM and *Markdown Here* supports them. They are an easy way of adding tables to your email -- a task that would otherwise require copy-pasting from another application.

```no-highlight
Colons can be used to align columns.

| Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |

There must be at least 3 dashes separating each header cell.
The outer pipes (|) are optional, and you don't need to make the 
raw Markdown line up prettily. You can also use inline Markdown.

Markdown | Less | Pretty
--- | --- | ---
*Still* | `renders` | **nicely**
1 | 2 | 3
```

Colons can be used to align columns.

| Tables        | Are           | Cool |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |

There must be at least 3 dashes separating each header cell. The outer pipes (|) are optional, and you don't need to make the raw Markdown line up prettily. You can also use inline Markdown.

Markdown | Less | Pretty
--- | --- | ---
*Still* | `renders` | **nicely**
1 | 2 | 3

<a name="blockquotes"/>

## Blockquotes

```no-highlight
> Blockquotes are very handy in email to emulate reply text.
> This line is part of the same quote.

Quote break.

> This is a very long line that will still be quoted properly when it wraps. Oh boy let's keep writing to make sure this is long enough to actually wrap for everyone. Oh, you can *put* **Markdown** into a blockquote. 
```

> Blockquotes are very handy in email to emulate reply text.
> This line is part of the same quote.

Quote break.

> This is a very long line that will still be quoted properly when it wraps. Oh boy let's keep writing to make sure this is long enough to actually wrap for everyone. Oh, you can *put* **Markdown** into a blockquote. 

<a name="html"/>

## Inline HTML

You can also use raw HTML in your Markdown, and it'll mostly work pretty well. 

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

## Horizontal Rule

```
Three or more...

---

Hyphens

***

Asterisks

___

Underscores
```

Three or more...

---

Hyphens

***

Asterisks

___

Underscores

<a name="lines"/>

## Line Breaks

My basic recommendation for learning how line breaks work is to experiment and discover -- hit &lt;Enter&gt; once (i.e., insert one newline), then hit it twice (i.e., insert two newlines), see what happens. You'll soon learn to get what you want. "Markdown Toggle" is your friend. 

Here are some things to try out:

```
Here's a line for us to start with.

This line is separated from the one above by two newlines, so it will be a *separate paragraph*.

This line is also a separate paragraph, but...
This line is only separated by a single newline, so it's a separate line in the *same paragraph*.
```

Here's a line for us to start with.

This line is separated from the one above by two newlines, so it will be a *separate paragraph*.

This line is also begins a separate paragraph, but...  
This line is only separated by a single newline, so it's a separate line in the *same paragraph*.

(Technical note: *Markdown Here* uses GFM line breaks, so there's no need to use MD's two-space line breaks.)

<a name="videos"/>

## Youtube videos

They can't be added directly but you can add an image with a link to the video like this:

```no-highlight
<a href="http://www.youtube.com/watch?feature=player_embedded&v=YOUTUBE_VIDEO_ID_HERE
" target="_blank"><img src="http://img.youtube.com/vi/YOUTUBE_VIDEO_ID_HERE/0.jpg" 
alt="IMAGE ALT TEXT HERE" width="240" height="180" border="10" /></a>
```

Or, in pure Markdown, but losing the image sizing and border:

```no-highlight
[![IMAGE ALT TEXT HERE](http://img.youtube.com/vi/YOUTUBE_VIDEO_ID_HERE/0.jpg)](http://www.youtube.com/watch?v=YOUTUBE_VIDEO_ID_HERE)
```

Referencing a bug by #bugID in your git commit links it to the slip. For example #1. 

---

License: [CC-BY](https://creativecommons.org/licenses/by/3.0/)
