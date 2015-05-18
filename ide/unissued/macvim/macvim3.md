# macvim 编辑模式下的常用指令
这里将给大家介绍一下最常用的编辑命令，虽然vim的命令有很多，这里就不一一列出了，需要详细了解的同学们可以在EX模下通过如下命令来查看
```
help mvim
```
下面列举的vim命令，小猿给大家的建议就是一个词背，当你熟练掌握的时候，你会发现效率会非常的高。
- 移动：
'h'(左移一位)'j'(下移一行)'k'(上移一行)'l'(右移一位)'G'(移动到文件最后一行)'L'(移动到当前屏幕最后一行)'M'(移动到当前屏幕中间一行)'H'(移动到当前屏幕第一行)'w'(向前移动一个单词)'b'(向后移动一个单词) '('(移动句子的开头)')'(移动到句子的结尾)'{'(移动到段落的开头)'}'(移动到段落的结尾) '0'(移动到行首) '$'(移动到行尾)
- 选中：
'v'(进入可视化模式，通过上下左右，或者hjkl来选择需要高亮的内容)
- 复制/粘贴：
'y'(复制内容进入buffer) 'yy'(复制整行内容进入buffer) 'p'(在当前光标后插入buffer内容) 'P'(在当前光标前插入buffer内容)，这里注意如果buffer内容是以行或者段落位单位的话，那么当用户输入p或者P时候，是以当前光标所在的行或者段落为一个整体，在前或者后插入buffer内容。
- 删除：
'dw(删除一个word) 'dd'(删除一行),或者可以先进入可视化模式来选择内容在按'd'来删除,'x'(删除当前光标位置的一个字符)，这里要注意vim的删除，会把删除的字符存入buffer，其实就是剪切。
－回撤：
'u'(最近一次撤销) 'U'(撤销当前行的所有操作)
－查找替换：
'/'(向前查找) '?'(向后查找) 'n'(重复查找) 'N'(相反方向查找)
- 保存退出：
'w'(保存文件) 'q'(退出文件)

当然以上只是列出了最基本和常用的命令，小猿建议大家就死记硬背就可以了，下次给大家介绍一些其他的常用的命令
