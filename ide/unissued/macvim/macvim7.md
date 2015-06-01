#vim 配置html和javascript开发环境
前面我们学习了vim的相关配置，今天我们一起来看一看如果要搭建一个前段常用的开发环境需要哪些配置

## emmet

Emmet 是一款方便前段编辑HTML和CSS的插件，原名叫ZEN CODING，2012年改名字叫EMMET,安装非常简单
```
cd ~/.vim/bundle
git clone https://github.com/mattn/emmet-vim.git
```
于是神奇的事情发生了。重新打开vim以后在需要插入html模版的地方插入
```
html:5
```
然后键入ctrl＋y，（组合键c＋y再加上，），你会看到
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title></title>
</head>
<body>	
</body>
</html>
```
一段html5的标签，当然emmet还包括自动加入注释ctrl+y+/,以及快速排版的一系列有用的功能，具体的方式建议大家参考emmet的github地址的[帮助文档](https://github.com/mattn/emmet-vim/blob/master/doc/emmet.txt)

## neocomplete

neocomplet 是一个非常优秀的代码补全插件，同类还有youcompleteme，不过对于老得vimer来说，普遍反映neocomplet用起来更加顺手。她的安装基于pathogen,不过neocomplet需要相关的版本支持LUA脚本.
```
cd ~/.vim/bundle
git clone https://github.com/Shougo/neocomplete.vim.git
```
安装完成以后需要在.vimrc中加入
```
let g:neocomplete#enable_at_startup = 1
" Enable omni completion.
autocmd FileType css setlocal omnifunc=csscomplete#CompleteCSS
autocmd FileType html,markdown setlocal omnifunc=htmlcomplete#CompleteTags
autocmd FileType javascript setlocal omnifunc=javascriptcomplete#CompleteJS
autocmd FileType python setlocal omnifunc=pythoncomplete#Complete
autocmd FileType xml setlocal omnifunc=xmlcomplete#CompleteTags
```
这样代码补全就会被自动的开启。
## ctrlp
这是一个可以快速打开和定位文件的插件,是小猿用过的最爽的一个插件，它可以缓存你当前目录下的所有文件，然后提供快速定位和索引的目地，如果你对要查找的文件名比较清楚，又不希望一直切换vim和terminal，那这个插件几乎可以满足你所有的对文件系统快速查找的需求。
```
cd ~/.vimrc/bundle
git clone https://github.com/kien/ctrlp.vim.git
```
安装完以后直接按Ctrl+P 然后模糊输入需要打开的文件，就可以打开,也可以对需要打开的文件输ctrl+v/ctrl+x 来分屏打开,后者ctrl+t来分tab打开

## nerdcommenter
nerdcommenter 是一款可以快速注释的插件
```
cd ~/.vim/bundle
git clone https://github.com/scrooloose/nerdcommenter.git
```
同时确认在.vimrc里面开启
```
filetype plugin on
```
这样可以通过"\\cc" 来添加注释，也可以通过"\\cu" 来取消注释。

好了到这里我们的vim旅程就结束了，接下来要靠读者自己去体会vim编辑器的神奇之处了。有人形容vim像功夫片里的一句台词说的那样，“一支穿云箭，千军万马来相见”，可是小猿个人觉得她还是无法替代eclipse和IntelliJ等专业的IDE，不过就像术业有专供，她做为文本编辑器以及编写一些动态脚本语言还是非常爽的，比如ruby，比如JavaScript等。其实我觉得她更像一首歌里写的那样，“像一杯酒，像一首老歌”，希望大家在用的过程中慢慢品味这杯酒，也相信大家一定会有进一步的发现。


