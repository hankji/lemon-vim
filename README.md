# lemon-vim

## 目录

- [简介](#简介)
- [安装步骤](#安装步骤)
- [自定义快捷键](#自定义快捷键)
- [插件](#插件)
    - [插件管理](##插件管理)
    - [插件列表](##插件列表)
- [vim主题](#vim主题)
- [参考内容](#参考内容)
- [vim资料](#vim资料)

## 简介

这里我自己平时工作环境的vim，参考了k-vim，spf13，space-vim等一些优秀的vim配置，常用的功能和插件都都包含在内。个人感觉vim还是用自己配置的最舒服，熟悉自己vimrc中所有的配置，熟悉安装的插件的功能和快捷键设置。简单学习了vimscript语法，但还无法编写自己的vim插件，欢迎喜欢vim的人共同交流。

## 安装步骤

### 1. clone lemon-vim到本地

```
git clone git@github.com:lemon0910/lemon-vim.git
```

### 2. 安装

进入目录, 执行安装脚本，操作步骤如下：

```
cd lemon-vim/
sh -x install.sh
```

安装时需要注意：

1. 安装是从github clone的，完全取决于网速
2. 如果发现有插件安装失败 可以进入vim, 执行`:PlugInstall`

### 2.3 卸载安装

执行下面的命令：
```
cd ~ && rm -rf .vim .vimrc .vimrc.bundles .config/nvim && cd -
```

## 自定义快捷键

记录自己在vimrc文件中设置的快捷键，快捷键的好处是大大提高了vim的使用效率，配置都是基于自己的喜好。

```
注意, 以下 ',' 代表<leader>
ctrl + j/k/h/l                进行上下左右窗口跳转,不需要ctrl+w+jkhl

" ctags的设置
gd                            跳转到定义
gb                            返回上一次跳转点

" 命令行模式加强
H                        跳到行首
L                        跳到行尾

,q                            退出
,wq                           保存退出
,ww                           保存文件

,+数字                        切换到对应数字的buffer
tab                      进行buffer的切换
Alt+c                        清空所有的tab
ctrl+t                       新建tab

ctrl+r                       执行程序，目前支持c，c++，sh，python和go
,y                           复制选中区到系统剪切板中
ctrl+n                       相对/绝对行号切换
```

## 插件

### 插件管理

使用 [vim-plug](https://github.com/junegunn/vim-plug) 管理插件。
`vim-plug` 常见问题: [vim-plug faq](https://github.com/junegunn/vim-plug/wiki/faq)，关于YouCompleteMe安装问题[YCM timeout](https://github.com/junegunn/vim-plug/wiki/faq#youcompleteme-timeout)。
管理插件的命令：

```
:PlugInstall     install                      安装插件
:PlugUpdate      install or update            更新插件
:PlugClean       remove plugin not in list    删除本地无用插件
:PlugUpgrade     Upgrade vim-plug itself      升级本身
:PlugStatus      Check the status of plugins  查看插件状态
```

### 插件列表

### gmarik/vundle

[项目地址](https://github.com/VundleVim/Vundle.vim)

用于管理所有插件，和plug类似。

### scrooloose/nerdtree

[项目地址](https://github.com/scrooloose/nerdtree)

在VIM的编辑窗口树状显示文件目录。效果如下:

![nerdtree](/images/1.png)

演示如下：

![nerdtreegif](/images/2.gif)

通过配置快捷键，使用`<leader>n`可以展示目录。

### majutsushi/tagbar

[项目地址](https://github.com/majutsushi/tagbar)

标签导航，显示文件中的函数和变量。效果如下：

![tag](/images/3.png)

演示如下：

![tagbargif](/images/4.gif)

配置`<leader>t`用于展示tagbar。

### kien/ctrlp.vim

[项目地址](https://github.com/kien/ctrlp.vim)

非常强大，可以根据关键词查找相应的文件。
演示如下：

![ctrlp](/images/5.gif)

配置`<leader>p`来唤醒该插件。

### vim-airline/vim-airline和vim-airline/vim-airline-themes

[airline项目地址](https://github.com/vim-airline/vim-airline)

[airline-themes项目地址](https://github.com/vim-airline/vim-airline-themes)

用于美观状态栏，演示如下：

![airline](/images/6.gif)

### kien/rainbow_parentheses.vim

[项目地址](https://github.com/kien/rainbow_parentheses.vim)

括号高亮，演示如下：

![rainbow_parentheses](/images/7.png)

### Lokaltog/vim-easymotion

[项目地址](https://github.com/easymotion/vim-easymotion)

快速转到指定位置，提高效率神器。演示如下：

![easy-motion](/images/8.gif)

### Valloric/YouCompleteMe

[项目地址](https://github.com/Valloric/YouCompleteMe)

YCM是目前最好的自动补全插件，用起来非常的爽，大大提高了写代码的效率。安装的时候要求vim的版本在7.3.584 以上。演示如下：

![YCM](/images/9.gif)

对于每个项目，YCM可以定制配置文件，参考项目[YCM-Generator](https://github.com/rdnetto/YCM-Generator)进行快速设置。

### lfv89/vim-interestingwords

[项目地址](https://github.com/lfv89/vim-interestingwords)

高亮光标下的word，可以同时高亮多个，用不同的颜色显示。演示如下：

![interestingwords](/images/10.png)

### Raimondi/delimitMate

[项目地址](https://github.com/Raimondi/delimitMate)

自动补全引号，括号等。

### scrooloose/nerdcommenter

[项目地址](https://github.com/scrooloose/nerdcommenter)

快速的添加和去除注释，快捷键`<leader>cc`添加注释，`<leader>c<space>`取消注释。

### matze/vim-move

[项目地址](https://github.com/matze/vim-move)

快速移动选中的行。演示如下：

![vim-move](/images/11.gif)

### a.vim

[项目地址](https://github.com/vim-scripts/a.vim)

快速的进行.h和.c文件进行切换，在编写c和c++程序时比较实用，文件切换非常快速。

### sirver/ultisnips

[项目地址](https://github.com/SirVer/ultisnips)

别名定义，可以更高效的编写代码，需要将别名牢记在心。演示如下：

![ultisnips](/images/12.gif)

### honza/vim-snippets

[项目地址](https://github.com/honza/vim-snippets)

和ultisnips一起配合使用，规定了一些别名的定义，比较齐全。

### mbbill/undotree

[项目地址](https://github.com/mbbill/undotree)

将撤销的操作按照日志的形式展示出来，并可以切换到每一个撤销点。演示如下：

![undotree](/images/13.png)

使用`<leader>u`可以查看撤销操作日志。

### rking/ag.vim

[项目地址](https://github.com/rking/ag.vim)

使用ag命令搜索代替grep搜索，搜索更加的快速高效。

### brookhong/cscope.vim

[项目地址](https://github.com/brookhong/cscope.vim)

帮助创建和更新cscope的database的插件，无需自己配置cscope，非常方便。

### conradirwin/vim-bracketed-paste

[项目地址](https://github.com/ConradIrwin/vim-bracketed-paste)

在vim中粘贴往往会导致格式错误，vim-bracketed-paste会处理相关问题，无需每次粘贴都输入`:paste`。

### skywind3000/asyncrun.vim

[项目地址](https://github.com/skywind3000/asyncrun.vim)

在后台异步的执行任务，如编译连接等。使用`<leader>ar`唤醒，使用`<leader>co`查看执行结果。

### Shougo/neocomplete.vim

[项目地址](https://github.com/Shougo/neocomplete.vim)

另一款比较流行的代码自动补全插件，需要vim支持lua。因为YCM安装要求太多，所以使用neocomplete作为备选方案。

### tpope/vim-fugitive

[项目地址](https://github.com/tpope/vim-fugitive)

在vim中使用git的相关功能，主要配置了下面几项:

- <leader>gs :Gstatus
- <leader>gd :Gdiff
- <leader>gc :Gcommit
- <leader>gb :Gblame
- <leader>gl :Glog
- <leader>gp :Git push

最常用的是Gblame查看修改。

### christoomey/vim-tmux-navigator

[项目地址](https://github.com/christoomey/vim-tmux-navigator)

非常好用的插件，用来在tmux和vim之间的导航，不再需要先按tmux中的<prefix>键，使用<C-h>，<C-l>，<C-j>和<C-k>在vim和tmux之间跳转。

## vim主题

vim下面比较流行的两个主题是molokai和solarized。
molokai主题：

![molokai](/images/30.png)

solarized主题：

![solarized](/images/31.png)

## 参考内容

1. vimrc文件布局`vimrc+vimrc.bundles`配置方式参考 [maximum-awesome](https://github.com/square/maximum-awesome)
2. install.sh 参考`spf13-vim` 的`bootstrap.sh` [spf13-vim](https://github.com/spf13/spf13-vim)
3. 插件管理使用[Vundle](https://github.com/gmarik/Vundle.vim)
4. 自动补全 [YCM](https://github.com/Valloric/YouCompleteMe)

## vim资料

1. [space-vim](https://github.com/liuchengxu/space-vim)
2. [spacevim](https://github.com/SpaceVim/SpaceVim)
3. 配色主题 [vimcolor](http://vimcolors.com/)
4. 插件挑选 [VimAwesome](http://vimawesome.com/)
5. vim介绍[vim-galore-zh_cn](https://github.com/wsdjeg/vim-galore-zh_cn#%E5%AE%8F)
6. [vim官网](http://www.vim.org/)
