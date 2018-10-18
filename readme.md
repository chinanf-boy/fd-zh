# fd [![translate-svg]][translate-list]

[translate-svg]: http://llever.com/translate.svg
[translate-list]: https://github.com/chinanf-boy/chinese-translate-list

「 *fd*是一种简单ㄡ快速和用户友好的[*find*](https://www.gnu.org/software/findutils/)替代方案.」

[中文](./readme.md) | [english](https://github.com/sharkdp/fd)


---

## 校对 ✅

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


- [fd](#fd)
  - [特征](#%E7%89%B9%E5%BE%81)
  - [演示](#%E6%BC%94%E7%A4%BA)
  - [基准](#%E5%9F%BA%E5%87%86)
  - [彩色输出](#%E5%BD%A9%E8%89%B2%E8%BE%93%E5%87%BA)
  - [并行命令执行](#%E5%B9%B6%E8%A1%8C%E5%91%BD%E4%BB%A4%E6%89%A7%E8%A1%8C)
  - [安装](#%E5%AE%89%E8%A3%85)
    - [Ubuntu](#ubuntu)
    - [Fedora](#fedora)
    - [Arch Linux](#arch-linux)
    - [Gentoo Linux](#gentoo-linux)
    - [openSUSE Linux](#opensuse-linux)
    - [Void Linux](#void-linux)
    - [macOS](#macos)
    - [Windows](#windows)
    - [NixOS / via Nix](#nixos--via-nix)
    - [FreeBSD](#freebsd)
    - [源码文件](#%E6%BA%90%E7%A0%81%E6%96%87%E4%BB%B6)
    - [二进制文件](#%E4%BA%8C%E8%BF%9B%E5%88%B6%E6%96%87%E4%BB%B6)
  - [开发](#%E5%BC%80%E5%8F%91)
  - [命令行选项](#%E5%91%BD%E4%BB%A4%E8%A1%8C%E9%80%89%E9%A1%B9)
  - [教程](#%E6%95%99%E7%A8%8B)
    - [简单搜索](#%E7%AE%80%E5%8D%95%E6%90%9C%E7%B4%A2)
    - [正则表达式搜索](#%E6%AD%A3%E5%88%99%E8%A1%A8%E8%BE%BE%E5%BC%8F%E6%90%9C%E7%B4%A2)
    - [指定根目录](#%E6%8C%87%E5%AE%9A%E6%A0%B9%E7%9B%AE%E5%BD%95)
    - [仅运行*fd*](#%E4%BB%85%E8%BF%90%E8%A1%8Cfd)
    - [搜索特定的文件扩展名](#%E6%90%9C%E7%B4%A2%E7%89%B9%E5%AE%9A%E7%9A%84%E6%96%87%E4%BB%B6%E6%89%A9%E5%B1%95%E5%90%8D)
    - [隐藏和忽略的文件](#%E9%9A%90%E8%97%8F%E5%92%8C%E5%BF%BD%E7%95%A5%E7%9A%84%E6%96%87%E4%BB%B6)
    - [排除特定文件或目录](#%E6%8E%92%E9%99%A4%E7%89%B9%E5%AE%9A%E6%96%87%E4%BB%B6%E6%88%96%E7%9B%AE%E5%BD%95)
    - [使用fd  带`xargs`或`parallel`](#%E4%BD%BF%E7%94%A8fd--%E5%B8%A6xargs%E6%88%96parallel)
    - [与其他程序的集成](#%E4%B8%8E%E5%85%B6%E4%BB%96%E7%A8%8B%E5%BA%8F%E7%9A%84%E9%9B%86%E6%88%90)
      - [使用fd与`fzf`](#%E4%BD%BF%E7%94%A8fd%E4%B8%8Efzf)
      - [使用fd与`emacs`](#%E4%BD%BF%E7%94%A8fd%E4%B8%8Eemacs)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->


# fd

[![Build Status](https://travis-ci.org/sharkdp/fd.svg?branch=master)](https://travis-ci.org/sharkdp/fd)
[![Build status](https://ci.appveyor.com/api/projects/status/21c4p5fwggc5gy3j?svg=true)](https://ci.appveyor.com/project/sharkdp/fd)
[![Version info](https://img.shields.io/crates/v/fd-find.svg)](https://crates.io/crates/fd-find)

*fd*是一种简单ㄡ快速和用户友好的[*fd*](https://www.gnu.org/software/findutils/)替代方案. 

虽然它不寻求复刻*find*所有强大的功能,但它提供了明智的 (自定的) [80%](https://en.wikipedia.org/wiki/Pareto_principle)的用例. 

## 特征

-   方便语法: `fd PATTERN`而不是`find -iname '*PATTERN*'`.
-   彩色终端输出 (类似于*ls*) 
-   它是*快速的* (见[基准](#%E5%9F%BA%E5%87%86)下面) . 
-   聪明案例: 默认情况下,搜索不区分大小写. 如果模式包含大写字符[\*](http://vimdoc.sourceforge.net/htmldoc/options.html#'smartcase'), 则切换为区分大小写字符. .
-   默认情况下,忽略隐藏的目录和文件. 
-   忽略匹配你`.gitignore`文件中的模式,默认情况. 
-   正则表达式. 
-   Unicode感知. 
-   命令输入量*50%*优于[\*](https://github.com/ggreer/the_silver_searcher)`find`: -) 
-   用类似于GNU穿行的语法，执行并行命令. 

## 演示

![Demo](doc/screencast.svg)

## 基准

让我们搜索我的主文件夹的以`[0-9].jpg`为结束的文件. 它包含190个子目录和大约一百万个文件. 我使用[hyperfine](https://github.com/sharkdp/hyperfine)进行平均和统计分析. 下面的基准是用"warm"/预填充的磁盘缓存执行的 (对于"冷"磁盘缓存的结果显示出相同的趋势) . 

让我们从`find`: 


    Benchmark #1: find ~ -iregex '.*[0-9]\.jpg$'

      Time (mean ± σ):      7.236 s ±  0.090 s

      Range (min … max):    7.133 s …  7.385 s

`find`如果不需要执行正则表达式搜索,则会更快得多: 

    Benchmark #2: find ~ -iname '*[0-9].jpg'

      Time (mean ± σ):      3.914 s ±  0.027 s

      Range (min … max):    3.876 s …  3.964 s

现在让我们尝试同样的`fd`. 注意`fd` *总是*执行正则表达式搜索. 选项`--hidden`和`--no-ignore`需要自行决策, 下面的`fd`需要遍历隐藏文件夹和忽略的路径 (见下文) : 

    Benchmark #3: fd -HI '.*[0-9]\.jpg$' ~

      Time (mean ± σ):     811.6 ms ±  26.9 ms

      Range (min … max):   786.0 ms … 870.7 ms

对于这个特殊的例子,`fd`大约比`find -iregex`快九倍,和大约比`find -iname`快五倍. 顺便说一下,两个工具都找到了完全相同的20880个文件: :smile: . 

最后,让我们运行`fd`没有`--hidden`和`--no-ignore`选项 (当然,这会导致不同的搜索结果) . 如果*fd*不必遍历隐藏的和Git忽略的文件夹,它的数量级快了一个数量级: 

    Benchmark #4: fd '[0-9]\.jpg$' ~

      Time (mean ± σ):     123.7 ms ±   6.0 ms

      Range (min … max):   118.8 ms … 140.0 ms

**注释**这是在*一个特定的*机器上的*一个特定的*基准. 虽然我已经做了很多不同的测试 (并且发现了一致的结果) ,但是事情可能对你来说不同. 我鼓励每个人自己尝试测试. 在[这个仓库](https://github.com/sharkdp/fd-benchmarks)是所有用于对比的脚本. 

关于*fd*的速度,主要的耗时在`regex`和`ignore`,还有[ripgrep](https://github.com/BurntSushi/ripgrep)箱子 (检查一下!) .

## 彩色输出

`fd`可以通过扩展来帮输出着色,就像`ls`. 为了使这工作,环境变量[`LS_COLORS`](https://linux.die.net/man/5/dir_colors)必须设置. 通常,此变量的值由`dircolors`命令控制,它提供了一种方便的配置格式,来定义不同文件格式的颜色. 在大多数分配情况,`LS_COLORS`应该已经设置好了. 如果您正在寻找替代的，且更完整的 (以及更丰富多彩的) 变体,请参见[在这里](https://github.com/seebi/dircolors-solarized)或[在这里](https://github.com/trapd00r/LS_COLORS).

## 并行命令执行

如果`-x`/`--exec`选项与命令模板一起指定,将创建一个作业池,用于并行执行命令，每个发现的路径则作为输入. 生成命令的语法类似于GNU穿行的语法: 

-   `{}`: 将被替换为搜索结果路径的占位符令牌 (`documents/images/party.jpg`) 
-   `{.}`: 像`{}`,但没有文件扩展名 (`documents/images/party`) 
-   `{/}`:占位符,将被搜索结果的基名替换 (占位符) . `party.jpg`) 
-   `{//}`:使用已发现路径的父节点 (`documents/images`) 
-   `{/.}`:使用BaseNeNe,将扩展名移除 (`party`) 

```bash
# 转换 所有 jpg 到  png :
fd -e jpg -x convert {} {.}.png

# Unpack all zip files (if no placeholder is given, the path is appended):
fd -e zip -x unzip

# Convert all flac files into opus files:
fd -e flac -x ffmpeg -i {} -c:a libopus {.}.opus

# Count the number of lines in Rust files (the command template can be terminated with ';'):
fd -x wc -l \; -e rs
```

## 安装

### Ubuntu

*以及其他基于Debian的Linux发行版.*

下载最新`.deb`包装从[releases页面](https://github.com/sharkdp/fd/releases)并通过以下方式安装: 

```bash
sudo dpkg -i fd_7.0.0_amd64.deb  # adapt version number and architecture
```

### Fedora

从 FEDORA 28 开始,您可以从官方包装来源安装`fd`: 

```bash
dnf install fd-find
```

对于旧版本,您可以使用[Fedora copr](https://copr.fedorainfracloud.org/coprs/keefle/fd/)安装`fd`: 

```bash
dnf copr enable keefle/fd
dnf install fd
```

### Arch Linux

你可以从官方回购安装[fd 软件包](https://www.archlinux.org/packages/community/x86_64/fd/): 

    pacman -S fd

### Gentoo Linux

你可以从官方回购使用[fd 软件包](https://packages.gentoo.org/packages/sys-apps/fd): 

    emerge -av fd

### openSUSE Linux

你可以从官方回购安装[fd 软件包](https://software.opensuse.org/package/fd): 

    zypper in fd

### Void Linux

你可以安装`fd`通过xbps安装: 

    xbps-install -S fd

### macOS

你可以安装`fd`具有[brew](http://braumeister.org/formula/fd): 

    brew install fd

或与Mac port: 

    sudo port install fd

### Windows

您可以从中 [releases页面](https://github.com/sharkdp/fd/releases)，下载预构建的二进制文件.

或者,您可以安装`fd`通过[Scoop](http://scoop.sh): 

    scoop install fd

或通过[Chocolatey](https://chocolatey.org): 

    choco install fd

### NixOS / via Nix

你可以使用[NixOS 包管理](https://nixos.org/nix/)安装`fd`: 

    nix-env -i fd

### FreeBSD

你可以安装`sysutils/fd`通过patmaster: 

    portmaster sysutils/fd

### 源码文件

你可以通过rust的包管理[cargo](https://github.com/rust-lang/cargo)安装*fd*:

    cargo install fd-find

注意rust版本要*1.20.0*或以上. 

### 二进制文件

这个[releases页面](https://github.com/sharkdp/fd/releases)包括Linux,MaOS和Windows的预编译二进制文件. 

## 开发

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
        -H, --hidden            搜索隐藏的文件和目录
        -I, --no-ignore         不要忽略 .(git | fd)ignore 文件匹配
            --no-ignore-vcs     不要忽略.gitignore文件的匹配
        -s, --case-sensitive    区分大小写的搜索（默认值：智能案例）
        -i, --ignore-case       不区分大小写的搜索（默认值：智能案例）
        -F, --fixed-strings     将模式视为文字字符串
        -a, --absolute-path     显示绝对路径而不是相对路径
        -L, --follow            遵循符号链接
        -p, --full-path         搜索完整路径（默认值：仅限 file-/dirname）
        -0, --print0            用null字符分隔结果
        -h, --help              打印帮助信息
        -V, --version           打印版本信息

    OPTIONS:
        -d, --max-depth <depth>        设置最大搜索深度（默认值：无）
        -t, --type <filetype>...       按类型过滤：文件（f），目录（d），符号链接（l），
                                       可执行（x），空（e）
        -e, --extension <ext>...       按文件扩展名过滤
        -x, --exec <cmd>               为每个搜索结果执行命令
        -E, --exclude <pattern>...     排除与给定glob模式匹配的条目
            --ignore-file <path>...    以.gitignore格式添加自定义忽略文件
        -c, --color <when>             何时使用颜色：never，*auto*, always
        -j, --threads <num>            设置用于搜索和执行的线程数
        -S, --size <size>...           根据文件大小限制结果。

    ARGS:
        <pattern>    the search pattern, a regular expression (optional)
        <path>...    the root directory for the filesystem search (optional)

## 教程

首先,为了获得所有可用的命令行选项的概述,您可以运行`fd -h`的简明帮助消息 (见上文) 或`fd --help`更详细的版本. 

### 简单搜索

*fd*设计用于查找文件系统中的条目. 你可以执行的最基本的搜索就是运行一个参数:搜索模式的*fd*. 例如,假设您想查找您的旧脚本 (包括`netflix`) : 

```bash
> fd netfl
Software/python/imdb-ratings/netflix-details.py
```

如果只调用一个这样的参数,*fd*递归检索当前目录中, *包含*模式`netfl`的任何条目.

### 正则表达式搜索

搜索模式被视为正则表达式. 这里,我们搜索开始`x`并以`rc`结束的条目. : 

```bash
> cd /etc
> fd '^x.*rc$'
X11/xinit/xinitrc
X11/xinit/xserverrc
```

### 指定根目录

如果我们想搜索一个特定的目录,它可以作为第二个参数*fd*: 

```bash
> fd passwd /etc
/etc/default/passwd
/etc/pam.d/passwd
/etc/passwd
```

### 仅运行*fd*

*fd*可以不带参数调用. 这是非常有用的,以便快速地查看当前目录中的所有条目,递归地 (类似于`ls -R`) : 

```bash
> cd fd/tests
> fd
testenv
testenv/mod.rs
tests.rs
```

### 搜索特定的文件扩展名

通常,我们对特定类型的所有文件感兴趣. 这可以用`-e` (或) `--extension`选择权. 在这里,我们搜索FD仓库中的所有md文件: 

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

默认情况下,*fd*不搜索隐藏目录,不在搜索结果中显示隐藏文件. 若要禁用此行为,我们可以使用`-H` (或) `--hidden`选项: 

```bash
> fd pre-commit
> fd -H pre-commit
.git/hooks/pre-commit.sample
```

如果我们在一个Git存储库 (或者包括Git存储库) 中工作,*fd*不搜索`.gitignore`文件中匹配模式 (并且不显示文件) . 若要禁用此行为,我们可以使用`-I` (或) `--no-ignore`选项: 

```bash
> fd num_cpu
> fd -I num_cpu
target/debug/deps/libnum_cpus-f5ce7ef99006aa05.rlib
```

真正搜索*全部的*文件和目录,简单地组合隐藏和忽略的特性来显示一切 (`-HI`) 

### 排除特定文件或目录

有时我们希望忽略来自特定子目录的搜索结果. 例如,我们可能要搜索所有隐藏的文件和目录 (`-H`,但仍会排除所有`.git`目录. 我们可以使用`-E` (或) `--exclude`选择此选项. 它以任意的模式作为一个参数: 

```bash
> fd -H -E .git …
```

我们也可以用这个来跳过安装的目录: 

```bash
> fd -E /mnt/external-drive …
```

或跳过某些文件类型: 

```bash
> fd -E '*.bak' …
```

为了让这些模式永久不变,你可以创建一个`.fdignore`文件. 他们工作得很像`.gitignore`文件. 例如: 

```bash
> cat ~/.fdignore
/mnt/external-drive
*.bak
```

### 使用fd  带`xargs`或`parallel`

如果我们想在所有搜索结果上运行命令,我们可以将输出管`xargs`: 

```bash
> fd -0 -e rs | xargs -0 wc -l
```

这里,`-0`选项告诉*fd*用空字符 (而不是换行符) 分隔搜索结果. 以同样的方式,`xargs`的`-0`选项同样告诉它以这种方式读取输入. 

### 与其他程序的集成

#### 使用fd与`fzf`

你可以使用*fd*生成[fzf](https://github.com/junegunn/fzf)命令行模糊查找器的输入: 

```bash
export FZF_DEFAULT_COMMAND='fd --type file'
export FZF_CTRL_T_COMMAND="$FZF_DEFAULT_COMMAND"
```

然后,您可以键入`vim <Ctrl-T>`在你的终端打开FZF，也即是fd的搜索结果. 

或者,您可能喜欢遵循符号链接并包含隐藏文件 (但不包括`.git`文件夹) : 

```bash
export FZF_DEFAULT_COMMAND='fd --type file --follow --hidden --exclude .git'
```

你甚至可以通过设置fzf内的fd的颜色输出: 

```bash
export FZF_DEFAULT_COMMAND="fd --type file --color=always"
export FZF_DEFAULT_OPTS="--ansi"
```

有关详细信息,请参见 *fzf* reamde文件的[提示部分](https://github.com/junegunn/fzf#tips). 

#### 使用fd与`emacs`

Emacs封装了[find-file-in-project](https://github.com/technomancy/find-file-in-project)包, 这可以使用*fd*查找文件. 

安装`find-file-in-project`后，添加行`(setq ffip-use-rust-fd t)`在你的`~/.emacs`或`~/.emacs.d/init.el`文件中. 

在Emacs中,运行`M-x find-file-in-project-by-selected`查找匹配文件. 或者,运行`M-x find-file-in-project`列出项目中所有可用的文件. 
