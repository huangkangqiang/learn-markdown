#Markdown入门#

声明：仅作为个人学习笔记，以下为原作链接：  
[LearnShare：Learning-Markdown (Markdown 入门参考)](https://github.com/LearnShare/Learning-Markdown/tree/v2)

##1. 关于Markdown##

###1.1 介绍 

[Wiki:Markdown](https://zh.wikipedia.org/wiki/Markdown)

>Markdown是一种轻量级标记语言，创始人为约翰.格鲁伯。它允许人们“使用易读易写的纯文本格式编写文档，然后转换为有效的XHTML（或者HTML）文档”。这种语言吸收了很多在电子邮件中已有的纯文本标记的特性。

###1.2 为什么选择Markdown

* 它基于纯文本，方便修改和共享
* 几乎可以在所有的文本编辑器中编写
* 在github等网站中有很好的应用
* 很容易转换为HTML文档或其他格式
* 适合用来编写文档、记录笔记、撰写文章等

###1.3 兼容HTML

Markdown完全兼容HTML语法，可以直接在Markdown文档中插入HTML内容

<html>

    <html>
        <table>
            <tr>
                <td>1</td>
                <td>2</td>
            </tr>
            <tr>
                <td>3</td>
                <td>4</td>
            </tr>
        </table>
    </html>

</html>

<html>
    <table>
        <tr>
            <td>1</td>
            <td>2</td>
        </tr>
        <tr>
            <td>3</td>
            <td>4</td>
        </tr>
    </table>
</html>

###1.4 第一个Markdown文档

打开熟悉的文本编辑器（如Sublime Text），新建一个hello.md文件，写入下面的内容，并保存：

>.md和.markdown都是被普遍支持的扩展名，不过.md更加简单和方便。

<html>
    
    Hello
    ====

    [Google](https:www.google.com/)

</html>

Hello
====

[Google](https:www.google.com/)

##2. 语法
###2.1 段落与换行

段落的前后必须是空行  
空行指的是行内什么都没有，或者只有空白符（空格或制表符）
相邻两行文本，如果中间没有空行会显示在一行中（换行符被转换为空格） 

如果需要在段落内加入换行（<br\>)  
可以在前一行的末尾加入至少两个空格  
然后换行写其他的文字  

Markdown中的多数区块都需要在两个空行之间

###2.2 标题
####2.2.1 Setext形式
<html>
    
    H1
    ====

    H2
    ----

</html>

#H1
##H2

=和-的数量是没有限制的。通常的做法是使其和标题文本的长度相同，这样看起来比较舒服。或者可以像我一样，用四个-或=。  
>Setext形式只支持h1和h2两种标题。

####2.2.2 atx形式

 可以用对称的#包括文本

 <html>
    
    ####H4####

    #####H5#####

 </html>

####H4####
#####H5#####

也可以只在左边使用#

<html>
    
    ####H4

    #####H5

</html>

####H4
#####H5

成对的#左侧和只在左边使用的#左侧都不可以有任何空白，但其内侧可以使用空白。

<html>
    
     ###左侧使用了空格###

    #### 内侧使用了空格

</html>

 ###左侧使用了空格###
#### 内侧使用了空格

>在这一点上，可能各种Markdown的实现会有不同的结果，不过仍然需要我们遵守语法规则

###2.3 引用
####2.3.1 引用内容

在段落或其他内容前使用>符号，就可以将这段内容标记为引用的内容（<blockquote\>）

<html>
    
    >引用内容

</html>

>引用内容

####2.3.2 多行引用

<html>
    
    >多行引用
    >可以在每行前加'>'    

</html>

>多行引用
>可以在每行前加>

<html>
    
    >如果仅在第一行使用>  
    后面相邻的行即使省略>，也会变成引用内容

</html>

>如果仅在第一行使用>  
后面相邻的行即使省略>，也会变成引用内容

<html>

    >如果引用内容小换行  
    >可以在行尾添加两个空格  
    >
    >或者在引用内容中加一个空行

</html>

>如果引用内容小换行  
>可以在行尾添加两个空格  
>
>或者在引用内容中加一个空行

####2.3.3 嵌套引用

<html>

    >也可以在引用中
    >>使用嵌套的引用

</html>

>也可以在引用中
>>使用嵌套的引用

####2.4.4 其他Markdown

<html>

    >在引用中可以使用其他任何Markdown语法

</html>
>在引用中可以使用其他任何Markdown语法

###2.4 列表

####2.4.1 无序列表

<html>
    
    * 可以使用*作为标记
    + 可以使用+作为标记
    - 可以使用-作为标记

</html>

* 可以使用*作为标记
+ 可以使用+作为标记
- 可以使用-作为标记

####2.4.2 有序列表

<html>
    
    1. 有序列表以数字和.开始
    3. 数字的序列并不会影响生成的列表序列
    4. 但仍然推荐按照自然顺序（1,2,3...）编写

</html>

1. 有序列表以数字和.开始
3. 数字的序列并不会影响生成的列表序列
4. 但仍然推荐按照自然顺序（1,2,3...）编写

####2.4.3 嵌套的列表

<html>
    
    1. 第一层
        + 1-1
        + 1-2
    2. 无序列表和有序列表可以随意相互嵌套
        1. 2-1
        2. 2-2

</html>

1. 第一层
    + 1-1
    + 1-2
2. 无序列表和有序列表可以随意相互嵌套
    1. 2-1
    2. 2-2
####2.4.4 语法和用法

1. 无序列表项的开始是：符号 空格
2. 有序列表项的开始是：数字 . 空格
3. 空格至少为一个，多个空格将被解析为一个
4. 如果仅需要在行前显示数字和.：

<html>
    
    可以使用\.来取消显示为列表

</html>

可以使用\.来取消显示为列表

>\*的语法专门用来显示Markdown语法中使用的特殊字符*

###2.5 代码

####2.5.1 代码块

可以使用缩进来插入代码块

<html>
    
    <title>Markdown</title>

</html>

代码块前后需要有至少一个空行，且每行代码前需要有至少一个Tab或四个空格。

####2.5.2 行内代码

也可以通过``插入行内代码

例如`<title>Markdown</title>` 

####2.5.3 转换规则

代码块中的文本（包括Markdown语法）都会显示为原始内容，而特殊字符会被转换为HTML字符实体。

###2.6 分割线
###2.7 超链接
###2.8 图像
###2.9 强调
###2.10 字符转义



