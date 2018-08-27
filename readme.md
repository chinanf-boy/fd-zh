# fd [![translate-svg]][translate-list]

[translate-svg]: http://llever.com/translate.svg
[translate-list]: https://github.com/chinanf-boy/chinese-translate-list
    


「 *fd*是一种简单ㄡ快速和用户友好的[*find*](https://www.gnu.org/software/findutils/)替代方案.」

[中文](./readme.md) | [english](https://github.com/sharkdp/fd)


---

## 校对 🀄️
<!-- doc-templite START generated -->
<!-- time = '2018 8.20' -->
<!-- repo = 'sharkdp/fd' -->
<!-- commit = '2465cd139962c2f3a1d674846b6adc687daa72fa' -->
翻译的原文 | 与日期 | 最新更新 | 更多
---|---|---|---
[commit] | ⏰ 2018 8.20 | ![last] | [中文翻译][translate-list]

[last]: https://img.shields.io/github/last-commit/sharkdp/fd.svg
[commit]: https://github.com/sharkdp/fd/tree/2465cd139962c2f3a1d674846b6adc687daa72fa

<!-- doc-templite END generated -->

### 贡献

欢迎 👏 勘误/校对/更新贡献 😊 [具体贡献请看](https://github.com/chinanf-boy/chinese-translate-list#贡献)

## 生活

[help me live , live need money 💰](https://github.com/chinanf-boy/live-need-money)

---

### 目录

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->


- [峡湾](#%E5%B3%A1%E6%B9%BE)
  - [特征](#%E7%89%B9%E5%BE%81)
  - [演示](#%E6%BC%94%E7%A4%BA)
  - [基准](#%E5%9F%BA%E5%87%86)
  - [彩色输出](#%E5%BD%A9%E8%89%B2%E8%BE%93%E5%87%BA)
  - [并行命令执行](#%E5%B9%B6%E8%A1%8C%E5%91%BD%E4%BB%A4%E6%89%A7%E8%A1%8C)
  - [安装](#%E5%AE%89%E8%A3%85)
    - [关于Ubuntu](#%E5%85%B3%E4%BA%8Eubuntu)
    - [论费多拉](#%E8%AE%BA%E8%B4%B9%E5%A4%9A%E6%8B%89)
    - [ARCLinux的研究](#arclinux%E7%9A%84%E7%A0%94%E7%A9%B6)
    - [基于GUToOLinux的研究](#%E5%9F%BA%E4%BA%8Egutoolinux%E7%9A%84%E7%A0%94%E7%A9%B6)
    - [浅谈OpenSSuLinux](#%E6%B5%85%E8%B0%88openssulinux)
    - [论无效Linux](#%E8%AE%BA%E6%97%A0%E6%95%88linux)
    - [论马科斯](#%E8%AE%BA%E9%A9%AC%E7%A7%91%E6%96%AF)
    - [在Windows上](#%E5%9C%A8windows%E4%B8%8A)
    - [关于NIXOS/VIX NIX](#%E5%85%B3%E4%BA%8Enixosvix-nix)
    - [关于FreeBSD](#%E5%85%B3%E4%BA%8Efreebsd)
    - [从源头](#%E4%BB%8E%E6%BA%90%E5%A4%B4)
    - [从二进制文件](#%E4%BB%8E%E4%BA%8C%E8%BF%9B%E5%88%B6%E6%96%87%E4%BB%B6)
  - [发展](#%E5%8F%91%E5%B1%95)
  - [命令行选项](#%E5%91%BD%E4%BB%A4%E8%A1%8C%E9%80%89%E9%A1%B9)
  - [辅导的](#%E8%BE%85%E5%AF%BC%E7%9A%84)
    - [简单搜索](#%E7%AE%80%E5%8D%95%E6%90%9C%E7%B4%A2)
    - [正则表达式搜索](#%E6%AD%A3%E5%88%99%E8%A1%A8%E8%BE%BE%E5%BC%8F%E6%90%9C%E7%B4%A2)
    - [指定根目录](#%E6%8C%87%E5%AE%9A%E6%A0%B9%E7%9B%AE%E5%BD%95)
    - [运行*峡湾*没有任何争论](#%E8%BF%90%E8%A1%8C%E5%B3%A1%E6%B9%BE%E6%B2%A1%E6%9C%89%E4%BB%BB%E4%BD%95%E4%BA%89%E8%AE%BA)
    - [搜索特定的文件扩展名](#%E6%90%9C%E7%B4%A2%E7%89%B9%E5%AE%9A%E7%9A%84%E6%96%87%E4%BB%B6%E6%89%A9%E5%B1%95%E5%90%8D)
    - [隐藏和忽略的文件](#%E9%9A%90%E8%97%8F%E5%92%8C%E5%BF%BD%E7%95%A5%E7%9A%84%E6%96%87%E4%BB%B6)
    - [排除特定文件或目录](#%E6%8E%92%E9%99%A4%E7%89%B9%E5%AE%9A%E6%96%87%E4%BB%B6%E6%88%96%E7%9B%AE%E5%BD%95)
    - [使用FD与`xargs`或`parallel`](#%E4%BD%BF%E7%94%A8fd%E4%B8%8Exargs%E6%88%96parallel)
    - [与其他程序的集成](#%E4%B8%8E%E5%85%B6%E4%BB%96%E7%A8%8B%E5%BA%8F%E7%9A%84%E9%9B%86%E6%88%90)
      - [使用FD与`fzf`](#%E4%BD%BF%E7%94%A8fd%E4%B8%8Efzf)
      - [使用FD与`emacs`](#%E4%BD%BF%E7%94%A8fd%E4%B8%8Eemacs)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->


# 峡湾

[![Build Status](https://travis-ci.org/sharkdp/fd.svg?branch=master)](https://travis-ci.org/sharkdp/fd)
[![Build status](https://ci.appveyor.com/api/projects/status/21c4p5fwggc5gy3j?svg=true)](https://ci.appveyor.com/project/sharkdp/fd)
[![Version info](https://img.shields.io/crates/v/fd-find.svg)](https://crates.io/crates/fd-find)

*峡湾*是一种简单ㄡ快速和用户友好的替代方案. [*找到*](https://www.gnu.org/software/findutils/).

当它不寻求镜像所有*找到*强大的功能,它提供了明智的 (自定的) 默认值. [80%](https://en.wikipedia.org/wiki/Pareto_principle)的用例. 

## 特征

-   方便语法: `fd PATTERN`而不是`find -iname '*PATTERN*'`.
-   彩色终端输出 (类似于*ls*) 
-   它是*快速的* (见[基准点](#benchmark)下面) . 
-   Smart案例: 默认情况下,搜索不区分大小写. 如果模式包含大写字符,则切换为区分大小写字符. [\*](http://vimdoc.sourceforge.net/htmldoc/options.html#'smartcase').
-   默认情况下,忽略隐藏的目录和文件. 
-   忽略你的模式`.gitignore`默认情况下. 
-   正则表达式. 
-   Unicode感知. 
-   命令名为*50%*更短的[\*](https://github.com/ggreer/the_silver_searcher)比`find`: -) 
-   用类似于GNU并行的语法执行并行命令. 

## 演示

![Demo](doc/screencast.svg)

## 基准

让我们搜索我的主文件夹的文件结束`[0-9].jpg`. 它包含190个子目录和大约一百万个文件. 对于平均和统计分析,我在使用[超精细](https://github.com/sharkdp/hyperfine). 下面的基准是用"热"/预填充的磁盘缓存执行的 (对于"冷"磁盘缓存的结果显示出相同的趋势) . 

让我们从`find`: 

    Benchmark #1: find ~ -iregex '.*[0-9]\.jpg$'

      Time (mean ± σ):      7.236 s ±  0.090 s

      Range (min … max):    7.133 s …  7.385 s

`find`如果不需要执行正则表达式搜索,则会更快得多: 

    Benchmark #2: find ~ -iname '*[0-9].jpg'

      Time (mean ± σ):      3.914 s ±  0.027 s

      Range (min … max):    3.876 s …  3.964 s

现在让我们尝试同样的`fd`. 注意`fd` *总是*执行正则表达式搜索. 选项`--hidden`和`--no-ignore`需要公平的比较,否则`fd`不必遍历隐藏文件夹和忽略路径 (见下文) : 

    Benchmark #3: fd -HI '.*[0-9]\.jpg$' ~

      Time (mean ± σ):     811.6 ms ±  26.9 ms

      Range (min … max):   786.0 ms … 870.7 ms

对于这个特殊的例子,`fd`大约快九倍`find -iregex`大约快五倍`find -iname`. 顺便说一下,两个工具都找到了完全相同的20880个文件: 微笑. 

最后,让我们运行`fd`没有`--hidden`和`--no-ignore` (当然,这会导致不同的搜索结果) . 如果*峡湾*不必遍历隐藏的和Git忽略的文件夹,它的数量级快了一个数量级: 

    Benchmark #4: fd '[0-9]\.jpg$' ~

      Time (mean ± σ):     123.7 ms ±   6.0 ms

      Range (min … max):   118.8 ms … 140.0 ms

**注释**这是*一个特别*基准*一个特别*机器. 虽然我已经做了很多不同的测试 (并且发现了一致的结果) ,但是事情可能对你来说不同. 我鼓励每个人自己尝试. 见[这个仓库](https://github.com/sharkdp/fd-benchmarks)用于所有必需的脚本. 

关于*峡湾*的速度,主要的信贷转到`regex`和`ignore`也适用于板条箱[里普格雷普](https://github.com/BurntSushi/ripgrep) (检查一下!) .

## 彩色输出

`fd`可以通过扩展着色文件,就像`ls`. 为了使这工作,环境变量[`LS_COLORS`](https://linux.die.net/man/5/dir_colors)必须设置. 通常,此变量的值由`dircolors`命令,它提供了一种方便的配置格式来定义不同文件格式的颜色. 在大多数分布上,`LS_COLORS`应该已经设置好了. 如果您正在寻找替代的ㄡ更完整的 (以及更丰富多彩的) 变体,请参见[在这里](https://github.com/seebi/dircolors-solarized)或[在这里](https://github.com/trapd00r/LS_COLORS).

## 并行命令执行

如果`-x`/`--exec`选项与命令模板一起指定,将创建一个作业池,用于为每个发现的路径并行执行命令作为输入. 生成命令的语法类似于GNU并行的语法: 

-   `{}`将被替换为搜索结果路径的占位符令牌 (`documents/images/party.jpg`) 
-   `{.}`喜欢`{}`,但没有文件扩展名 (`documents/images/party`) 
-   `{/}`占位符,将被搜索结果的基名替换 (占位符) . `party.jpg`) 
-   `{//}`使用已发现路径的父节点 (`documents/images`) 
-   `{/.}`使用BaseNeNe,将扩展名移除 (`party`) 

```bash
# Convert all jpg files to png files:
fd -e jpg -x convert {} {.}.png

# Unpack all zip files (if no placeholder is given, the path is appended):
fd -e zip -x unzip

# Convert all flac files into opus files:
fd -e flac -x ffmpeg -i {} -c:a libopus {.}.opus

# Count the number of lines in Rust files (the command template can be terminated with ';'):
fd -x wc -l \; -e rs
```

## 安装

### 关于Ubuntu

*ⅆ以及其他基于Debian的Linux发行版. *

下载最新`.deb`包装从[发布页面](https://github.com/sharkdp/fd/releases)并通过以下方式安装: 

```bash
sudo dpkg -i fd_7.0.0_amd64.deb  # adapt version number and architecture
```

### 论费多拉

从FEDORA 28开始,您可以安装`fd`从官方包装来源: 

```bash
dnf install fd-find
```

对于旧版本,您可以使用[费多拉公司](https://copr.fedorainfracloud.org/coprs/keefle/fd/)安装`fd`: 

```bash
dnf copr enable keefle/fd
dnf install fd
```

### ARCLinux的研究

你可以安装[FD软件包](https://www.archlinux.org/packages/community/x86_64/fd/)从官方回购: 

    pacman -S fd

### 基于GUToOLinux的研究

你可以使用[FD eBug](https://packages.gentoo.org/packages/sys-apps/fd)从官方回购: 

    emerge -av fd

### 浅谈OpenSSuLinux

你可以安装[FD软件包](https://software.opensuse.org/package/fd)从官方回购: 

    zypper in fd

### 论无效Linux

你可以安装`fd`通过XBPS安装: 

    xbps-install -S fd

### 论马科斯

你可以安装`fd`具有[自酿啤酒](http://braumeister.org/formula/fd): 

    brew install fd

ⅆ或与Mac端口: 

    sudo port install fd

### 在Windows上

您可以从中下载预构建的二进制文件. [发布页面](https://github.com/sharkdp/fd/releases).

或者,您可以安装`fd`通过[勺](http://scoop.sh): 

    scoop install fd

或通过[巧克力味](https://chocolatey.org): 

    choco install fd

### 关于NIXOS/VIX NIX

你可以使用[封装管理器](https://nixos.org/nix/)安装`fd`: 

    nix-env -i fd

### 关于FreeBSD

你可以安装`sysutils/fd`通过PATMASTER: 

    portmaster sysutils/fd

### 从源头

带锈的包装经理[货物](https://github.com/rust-lang/cargo)你可以安装*峡湾*通过: 

    cargo install fd-find

注意锈版*1.20.0*或以后需要. 

### 从二进制文件

这个[发布页面](https://github.com/sharkdp/fd/releases)包括LinuxㄡMaOS和Windows的预编译二进制文件. 

## 发展

```bash
git clone https://github.com/sharkdp/fd

# Build
cd fd
cargo build

# Run unit tests and integration tests
cargo test

# Install
cargo install
```

## 命令行选项

    USAGE:
        fd [FLAGS/OPTIONS] [<pattern>] [<path>...]

    FLAGS:
        -H, --hidden            Search hidden files and directories
        -I, --no-ignore         Do not respect .(git|fd)ignore files
            --no-ignore-vcs     Do not respect .gitignore files
        -s, --case-sensitive    Case-sensitive search (default: smart case)
        -i, --ignore-case       Case-insensitive search (default: smart case)
        -F, --fixed-strings     Treat the pattern as a literal string
        -a, --absolute-path     Show absolute instead of relative paths
        -L, --follow            Follow symbolic links
        -p, --full-path         Search full path (default: file-/dirname only)
        -0, --print0            Separate results by the null character
        -h, --help              Prints help information
        -V, --version           Prints version information

    OPTIONS:
        -d, --max-depth <depth>        Set maximum search depth (default: none)
        -t, --type <filetype>...       Filter by type: file (f), directory (d), symlink (l),
                                       executable (x), empty (e)
        -e, --extension <ext>...       Filter by file extension
        -x, --exec <cmd>               Execute a command for each search result
        -E, --exclude <pattern>...     Exclude entries that match the given glob pattern
            --ignore-file <path>...    Add a custom ignore-file in .gitignore format
        -c, --color <when>             When to use colors: never, *auto*, always
        -j, --threads <num>            Set number of threads to use for searching & executing
        -S, --size <size>...           Limit results based on the size of files.

    ARGS:
        <pattern>    the search pattern, a regular expression (optional)
        <path>...    the root directory for the filesystem search (optional)

## 辅导的

首先,为了获得所有可用的命令行选项的概述,您可以运行`fd -h`有关简明帮助消息 (见上文) 或`fd --help`更详细的版本. 

### 简单搜索

*峡湾*设计用于查找文件系统中的条目. 你可以执行的最基本的搜索就是运行. *峡湾*有一个参数: 搜索模式. 例如,假设您想查找您的旧脚本 (包括`netflix`) : 

```bash
> fd netfl
Software/python/imdb-ratings/netflix-details.py
```

如果只调用一个这样的参数,*峡湾*递归检索当前目录中的任何条目*包含*模式`netfl`.

### 正则表达式搜索

搜索模式被视为正则表达式. 这里,我们搜索开始的条目. `x`并结束`rc`: 

```bash
> cd /etc
> fd '^x.*rc$'
X11/xinit/xinitrc
X11/xinit/xserverrc
```

### 指定根目录

如果我们想搜索一个特定的目录,它可以作为第二个参数*峡湾*: 

```bash
> fd passwd /etc
/etc/default/passwd
/etc/pam.d/passwd
/etc/passwd
```

### 运行*峡湾*没有任何争论

*峡湾*可以不带参数调用. 这是非常有用的,以便快速地查看当前目录中的所有条目,递归地 (类似于`ls -R`) : 

```bash
> cd fd/tests
> fd
testenv
testenv/mod.rs
tests.rs
```

### 搜索特定的文件扩展名

通常,我们对特定类型的所有文件感兴趣. 这可以用`-e` (或) `--extension`选择权. 在这里,我们搜索FD仓库中的所有降价文件: 

```bash
> cd fd
> fd -e md
CONTRIBUTING.md
README.md
```

这个`-e`选项可以与搜索模式结合使用: 

```bash
> fd -e rs mod
src/fshelper/mod.rs
src/lscolors/mod.rs
tests/testenv/mod.rs
```

### 隐藏和忽略的文件

默认情况下,*峡湾*不搜索隐藏目录,不在搜索结果中显示隐藏文件. 若要禁用此行为,我们可以使用`-H` (或) `--hidden`选项: 

```bash
> fd pre-commit
> fd -H pre-commit
.git/hooks/pre-commit.sample
```

如果我们在一个Git存储库 (或者包括Git存储库) 中工作,*峡湾*不搜索与其中一个匹配的文件夹 (并且不显示文件) `.gitignore`模式. 若要禁用此行为,我们可以使用`-I` (或) `--no-ignore`选项: 

```bash
> fd num_cpu
> fd -I num_cpu
target/debug/deps/libnum_cpus-f5ce7ef99006aa05.rlib
```

真正搜索*全部的*文件和目录,简单地组合隐藏和忽略的特性来显示一切 (`-HI`) 

### 排除特定文件或目录

有时我们希望忽略来自特定子目录的搜索结果. 例如,我们可能要搜索所有隐藏的文件和目录 (`-H`但排除所有比赛`.git`目录. 我们可以使用`-E` (或) `--exclude`选择此选项. 它以任意的球形模式作为一个论点: 

```bash
> fd -H -E .git …
```

我们也可以用这个来跳过安装的目录: 

```bash
> fd -E /mnt/external-drive …
```

ⅆ或跳过某些文件类型: 

```bash
> fd -E '*.bak' …
```

为了让这些模式永久不变,你可以创建一个`.fdignore`文件. 他们工作得很像`.gitignore`文件,但具体到`fd`. 例如: 

```bash
> cat ~/.fdignore
/mnt/external-drive
*.bak
```

### 使用FD与`xargs`或`parallel`

如果我们想在所有搜索结果上运行命令,我们可以将输出管`xargs`: 

```bash
> fd -0 -e rs | xargs -0 wc -l
```

这里,`-0`选项告诉*峡湾*用空字符 (而不是换行符) 分隔搜索结果. 以同样的方式,`-0`选择权`xargs`告诉它以这种方式读取输入. 

### 与其他程序的集成

#### 使用FD与`fzf`

你可以使用*峡湾*生成命令行模糊查找器的输入[fzf](https://github.com/junegunn/fzf): 

```bash
export FZF_DEFAULT_COMMAND='fd --type file'
export FZF_CTRL_T_COMMAND="$FZF_DEFAULT_COMMAND"
```

然后,您可以键入`vim <Ctrl-T>`在你的终端打开FZF并通过FD搜索结果. 

或者,您可能喜欢遵循符号链接并包含隐藏文件 (但不包括`.git`文件夹) : 

```bash
export FZF_DEFAULT_COMMAND='fd --type file --follow --hidden --exclude .git'
```

你甚至可以通过设置FZF内的FD颜色输出: 

```bash
export FZF_DEFAULT_COMMAND="fd --type file --color=always"
export FZF_DEFAULT_OPTS="--ansi"
```

有关详细信息,请参见[提示部分](https://github.com/junegunn/fzf#tips)FZF自述文件. 

#### 使用FD与`emacs`

Emacs封装[在项目中查找文件](https://github.com/technomancy/find-file-in-project)可以使用*峡湾*查找文件. 

安装后`find-file-in-project`添加行`(setq ffip-use-rust-fd t)`对你`~/.emacs`或`~/.emacs.d/init.el`文件. 

在Emacs中,运行`M-x find-file-in-project-by-selected`查找匹配文件. 或者,运行`M-x find-file-in-project`列出项目中所有可用的文件. 
