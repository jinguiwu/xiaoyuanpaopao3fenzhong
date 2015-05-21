#macvim的缓存器
vim的缓存器又叫寄存器,vim 的寄存器可以分为内置的和具名的，用
```
:reg
""   gasdg
"0   gasdg
"1   #macvim 的常用快捷键^Jvim里面有很多令人赏心悦目的命令，这次3分钟的小跑，将给大家介绍10条有趣的vim命令^J- 在editor模式下使用点号键'.' 可以重复上一次的命令，
"2   ^J
"3   ^J
"4   sdgsadg^Jxxxasgxxxs^Jadsgasgxxx^Jxxxdsag^Jmacvim 的常用快捷键^Jsdgsadg^Jxxxasgxxxs^Jadsgasgxxx^Jxxxdsag^Jmacvim 的常用快捷键^Jsdgsad^Jxxxasgxxxs^Jadsgasgxx
"5   map <F5> :wall!<CR>:!sbcl --load foo.cl<CR><CR>^J
"6   # macvim 编辑模式下的常用指令^J这里将给大家介绍一下最常用的编辑命令，虽然vim的命令有很多，这里就不一一列出了，需要详细了解的同学们可以在EX模下通过如下命令
"7   ^J
"8   ^J
"9   ppsdg^Jpp^Jpp^Jppppaaaaaaaasdgasdg^Jadsgasdgasdgsadgdsagdsa^J^Jasdgasdgasdgasdg^J^Jsdagasdgsdgasdg^Jadsgasdgasdgsadgdsagdsa^J^Jasdgasdgasdgasdg^J^Jsdagasdg
"-   #macvim 的常用快捷键^Jvim里面有很多令人赏心悦目的命令，这次3分钟的小跑，将给大家介绍10条有趣的vim命令^J- 在editor模式下使用点号键'.' 可以重复上一次的命令，
"*
".   e
":   reg
"%   macvim5.md
"/   xxx

```
可能粗看起来有点混乱的感觉，那就对了：），接下来我们一起来熟悉一下每一个寄存器的作用
- 寄存器 “” :每一个寄存器都是以为"作为前缀，这个寄存器主要用来保存最近一次复制的内容

