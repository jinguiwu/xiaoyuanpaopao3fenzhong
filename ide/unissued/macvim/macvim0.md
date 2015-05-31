# macvim 的安装和环境变量的修改

macvim的安装非常的简单，可以官方网站下载安装包，也可以第三方包管理工具去安装，macvim是macos上是vim的一种类型，不过前者提供了一套完整的GUI而普通的vim是没有UI的。
```
$ brew install macvim --with-cscope --with-lua --HEAD
```
只要这一行命令我们就能完成macvim的安装，HOMEBREW 是mac上面的包管理工具，她可以方便的帮你下载，安装，查询和删除工具，作用和UBUNTU里面的apt-get和 OpenSuse里面的Zypper 是一样的。macvim安装成功以后，会在$VIM路径下面安装macvim的启动脚本.同时将启动脚本安装到/usr/local/bin.mvim是启动命令，mvimdiff是文件比较，mvimex是以命令行的方式运行，这个比较古老，比如打开一个文件是 mvimex filename ，这样vim就会加载文件到buffer，但不会现实，如果需要看内容可以运行 1p（表示显示第一行），一般现在很少会用，大家只要了解就够了.这里最后的LUA代表支持vim支持LUA脚本。

```
$ ls /usr/local/bin |grep mvim
$ ls -l | grep mvim
lrwxr-xr-x  1 jicui  admin        32 May 11 16:19 mvim -> ../Cellar/macvim/7.4-76/bin/mvim
lrwxr-xr-x  1 jicui  admin        36 May 11 16:19 mvimdiff -> ../Cellar/macvim/7.4-76/bin/mvimdiff
lrwxr-xr-x  1 jicui  admin        34 May 11 16:19 mvimex -> ../Cellar/macvim/7.4-76/bin/mvimex
```
安装完mvim后 可以
```
$mvim --version
VIM - Vi IMproved 7.4 (2013 Aug 10, compiled May 11 2015 16:19:12)
MacOS X (unix) version
Included patches: 1-712
```
mvim会输出相关的版本号，这样就代表安装成功了。启动的话直接在terminal输入
```
$mvim filename
```
就可以直接打开macvim。

# macvim 环境变量的修改
我们先开始熟悉以下macvim的配置文件，如下：

- $VIM/vimrc :系统级的vim配置,在macvim的安装目录下面。
- $HOME/.vimrc:用户级的vim配置，一般需要手动新建。
- ~/.vim/vimrc:用户级的第二级配置，会被$HOME/.vimrc覆盖。
- $HOME/.exrc: 为了兼容mvimex模式，一般不会动这个文件。
- $VIM/gvimrc:系统级的gvim配置,gvim是在vim的核心之上新增了图形前段，macvim是gvim的一种。
- $HOME/.gvimrc:用户级的gvim配置
- ~/.vim/gvimrc:用户级的二级配置，会被$HOME/.gvimrc覆盖。

我们可以尝试在$HOME下面建立 .vimrc 然后加入
```
color desert
```
再打开macvim的时候你就会发现，desert主题已经生效。简单吧：）
