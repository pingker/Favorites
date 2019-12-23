# 目录
- [常用 VIM 命令](#常用VIM命令)
  * [复制粘贴](#复制粘贴)
    + [Gvim 如何复制和粘贴系统粘贴板的内容](#Gvim如何复制和粘贴系统粘贴板的内容)
  * [列操作命令](#列操作命令)
  * [删除行首行尾空格和tab](#删除行首行尾空格和tab)
    + [删除行首空白字符](#删除行首空白字符)
    + [删除行尾空白字符](#删除行尾空白字符)
  * [多窗口、多文件切换](#多窗口、多文件切换)
    + [切分窗口](#切分窗口)
    + [文件之间切换](#文件之间切换)
    + [窗口之间切换](#窗口之间切换)
  * [References](#references)


# 常用VIM命令

## 复制粘贴

在正常模式下（按esc键进入）按v键进入可视化模式，然后你就可以使用hjkl四个光标键进行区域的选择；（shift+v键是一行一行的选取），选中了你想要的文本后，你就可以使用ctrl+c复制，ctrl+v进行粘贴了

### Gvim如何复制和粘贴系统粘贴板的内容

复制Gvim里面的内容至系统粘贴板："+y
粘贴系统粘贴板里面的内容至Gvim："+p

## 列操作命令

1. 进入列模式下： 移动光标到要注释区块的第一行，Unix下按Ctrl+v，Windows版本的VIM则按Ctrl+Q
1. 选择所需要的列：光标移动到要注释区块的最后一行（若干个j，或者直接输入行号再按G，或者按G到最后一行） 或 上下左右方向键
1. 针对列的操作： 例如
 删除 输入d ；
 替换 输入c ；
 需要输入则 按Shift+i，然后输入内容
1. 然后退出保存 ：按两次ESC


## 删除行首行尾空格和tab

### 删除行首空白字符

在非编辑状态下输入
:%s/^\s\+//

其中,
%s表示全局搜索
/为分隔符如例：s/a/b/g ；a 被查找的字符串（正则匹配）；b 要替换成的文字；g 表示全局搜索替换（否则只处理找到的第一个结果）
^代表行首
\s代表空格和tab
\+代表匹配一个或多个
$匹配行尾

更多信息参考[博客](https://blog.csdn.net/shenhuxi_yu/article/details/53413499)

### 删除行尾空白字符

在非编辑状态下输入
:%s/\s\+$//

## 多窗口、多文件切换

:e file
  在当前VIM中再打开一个文件，并显示内容

### 切分窗口

:sp
  水平切分窗口

:vsplit
  垂直切分窗口

### 文件之间切换

Ctrl+6
  两文件间的切换

:bn
  下一个文件

:bp
  上一个文件

:ls
  列出打开的文件，带编号

:b1~n
  切换至第n个文件

### 窗口之间切换

Ctrl+w+方向键
  切换到前／下／上／后一个窗格

Ctrl+w+h/j/k/l
  切换到前／下／上／后一个窗格

Ctrl+ww
  依次向后切换到下一个窗格中


## References

[Vim: Tips and tricks](https://www.cs.umd.edu/~yhchan/vim.pdf)

[Vi Pages - Substitution Guide](www.guckes.net/vi/substitute.html)

[Vi / VIM: Find And Replace All Text Substitute Command](https://www.cyberciti.biz/faq/vim-text-editor-find-and-replace-all-text/)

[vim删除以#，空格开头的行](https://www.cnblogs.com/doseoer/p/6241306.html)
