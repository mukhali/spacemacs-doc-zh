<a name="top"></a>
[![Gitter](https://badges.gitter.im/Join Chat.svg)](https://gitter.im/syl20bnr/spacemacs?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge) [![Build Status](https://travis-ci.org/syl20bnr/spacemacs.svg)](https://travis-ci.org/syl20bnr/spacemacs) [![Buy A Drink](https://img.shields.io/badge/Paypal-Buy%20a%20Drink-blue.svg)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=ESFVNPKP4Y742)[![Twitter][]](http://www.twitter.com/spacemacs)
***
<p align="center"><img src="/doc/img/title2.png" alt="Spacemacs"/></p>
<p align="center">
<b><a href="doc/DOCUMENTATION.org#core-pillars">编辑哲学</a></b>
|
<b><a href="doc/DOCUMENTATION.org#goals">目标</a></b>
|
<b><a href="doc/DOCUMENTATION.org#user-content-who-can-benefit-from-this">目标使用者</a></b>
|
<b><a href="doc/DOCUMENTATION.org#screenshots">截屏</a></b>
|
<b><a href="doc/DOCUMENTATION.org">文档</a></b>
|
<b><a href="doc/CONTRIBUTE.org">贡献者</a></b>
|
<b><a href="doc/DOCUMENTATION.org#achievements">成就</a></b>
|
<b><a href="#faq">FAQ</a></b>
</p>
***

**Quick Install:**

    git clone --recursive https://github.com/syl20bnr/spacemacs ~/.emacs.d

<!-- markdown-toc start - Don't edit this section. Run M-x markdown-toc/generate-toc again -->
**Table of Contents**

- [Introduction](#introduction)
- [Features](#features)
    - [Batteries Included](#batteries-included)
    - [Nice UI](#nice-ui)
    - [Excellent ergonomics](#excellent-ergonomics)
    - [Convenient and Mnemonic Key Bindings](#convenient-and-mnemonic-key-bindings)
        - [Great](#great-documentation) [Documentation][DOCUMENTATION.org]
- [Prerequisites](#prerequisites)
    - [Emacs](#emacs)
        - [Linux distros](#linux-distros)
        - [OS X](#os-x)
        - [Windows](#windows)
- [Install](#install)
    - [Spacemacs logo](#spacemacs-logo)
- [Update](#update)
    - [Update notification](#update-notification)
    - [Rollback](#rollback)
- [Configuration](#configuration)
    - [Configuration layers](#configuration-layers)
    - [Dotfile (.spacemacs)](#dotfile-spacemacs)
- [Learning Spacemacs](#learning-spacemacs)
    - [Editing Styles](#editing-styles)
    - [The leader keys](#the-leader-keys)
    - [Evil-tutor](#evil-tutor)
    - [Universal argument](#universal-argument)
    - [Configuration layers and Package discovery](#configuration-layers-and-package-discovery)
    - [Key bindings discovery](#key-bindings-discovery)
    - [Describe functions](#describe-functions)
- [How-To's](#how-tos)
- [Contributions](#contributions)
- [License](#license)
- [Special Credits](#special-credits)
- [Supporting Spacemacs](#supporting-spacemacs)
- [FAQ](#faq)
    - [Common](#common)
    - [Windows](#windows)
    - [OS X](#os-x)

<!-- markdown-toc end -->

# Introduction

_你是一个Vim使用者吗？

你不用为了使用Spacemacs而去学习Emacs！_

_你是一个Emacs用户吗？_

你不用为了使用Spacemacs而去学习Vim！

从0.101.0版本开始，Spacemacs将不再是能使用一种编辑风格了。用户将可以根据自己的爱好去选择不同的编辑风格，Emacs和Vim编辑风格都能享受Spacemacs带来的特性。

你不仅仅能够使用两种编辑风格，而且还能无缝，动态切换两种输入方法。这样就可以在结对编程时在同一编辑器上，依据个人不同的编辑爱好使用不同的编辑风格。

这两种编辑风格如此容易切换，以至于Spacemacs是学习两种编辑方法最好的配置。同时，你也可以将两种编辑风格融合，形成自己的混合编辑方式。

Spacemacs是集合了Emacs中许多优秀的包，同时对使用者友好，文档化的Emacs kit。Spacemacs通过使用[Evil Mode][]，从而将Vim的符合人体工学的编辑方式和Emacs这个强大的lisp引擎结合起来。

如果你已经是一个有经验的Emacs用户，你将会喜欢上这种优雅的可定制方法。

Spacemacs还是处于beta状态，欢迎各位的贡献

# Features

## Batteries Included

Spacemacs集合了上百个现有的包，在此感谢这种社区驱动的方法。

这些包是按[layers][]来组织，遵守这些通用的约得[CONVENTIONS.org][].

**[Visit the Documentation][DOCUMENTATION.org]**

## Nice UI

Spacemacs的UI很好看，这个UI附带一个高质量的主题和一个漂亮的mode-line。

![spacemacs_python](doc/img/spacemacs-python.png)

## Excellent ergonomics

Spacemacs是以[Evil Mode][]和a leader key为中心设计的，所有的包都被无缝的和Evil结合在一起。

Spacemacs通过micro-states组织相关命令，通过micro-states可以减少击键的次数，也可以减少对按键绑定的学习。

## Convenient and Mnemonic Key Bindings

`Spacemacs` 组织案件的方法是以易于记忆为主。比如，操作buffer的按键前缀是 `<SPC> b`，操作project的按键前缀是 `<SPC> p`。

### Great [Documentation][DOCUMENTATION.org]

绝大多数Spacemacs特性，按键绑定，配置选项都在文档里有记载。

如果你需要帮助，你可以在 [Gitter Chat][] 提问，会有社区成员给予你帮助。

如果你喜欢IRC，那么你可以通过[Gitter Chat IRC server][]参加`#syl20bnr/spacemacs`频道获取帮助。

# Prerequisites

## Emacs

`Spacemacs` is tested with Emacs 24.3 and 24.4 and therefore should boot
on all the major OSes where these versions are installable.

Some modes require third-party tools that you'll have to install via your
favorite package manager.

### Linux distros

Install Emacs from the package manager of your favorite Linux distribution.

### OS X

The recommended version for OS X is [emacs-mac-port][]. It can be installed
via [homebrew][] with the following commands:

```sh
$ brew tap railwaycat/emacsmacport
$ brew install emacs-mac --with-spacemacs-icon
```
(The `with-spacemacs-icon` option uses the official spacemacs logo for the app bundle.)

The default key handling is different from the official OS X port. To correct
this you can add the [osx layer][] to your [dotfile][] layer list:

```elisp
(setq-default dotspacemacs-configuration-layers '(osx))
```

Note that the `emacs-mac-port` server behaves differently than the regular
Emacs server.
Details can be found on the emacs-mac-port [README][emacs-mac-port-server].

### Windows

Good quality builds can be found [on this page][emacs-for-windows]. It is
recommended to install the most stable build.

Be sure to declare a environment variable named `HOME` and pointing to
your user directory `C:\Users\<username>`. Then you can clone Spacemacs
in this directory.

Sometimes you'll get the following error when you first start Emacs:

```
The directory ~/.emacs.d/server is unsafe
```

To fix it change the owner of the directory `~/.emacs.d/server`:
  - from Properties select the Tab “Security”,
  - select the button “Advanced”,
  - select the Tab “Owner”
  - change the owner to your account name

Source: [Stackoverflow][so-server-unsafe]

For efficient searches we recommend to install `pt` ([the platinum searcher][]).
`pt` version 1.7.7 or higher is required.

# Install

1. 如果你自己已经有Emacs配置文件，那么先备份一下:

   ```sh
   cd ~
   mv .emacs.d .emacs.bak
   ```

2. Clone this repository _with its submodules_:

   ```sh
   git clone --recursive https://github.com/syl20bnr/spacemacs ~/.emacs.d
   ```

   `master` is the stable branch and is regularly updated. Switch to the `develop`
   branch if you want to use the bleeding-edge version.

3. Launch Emacs. Spacemacs will automatically install the packages it requires.

4. Restart Emacs to complete the installation.

If the mode-line turns red then be sure to visit the [troubleshooting][troubleshoot]
guide and consult the [FAQ](#faq).

## Spacemacs logo

If you are using Ubuntu and Unity then you can add the Spacemacs logo by
following the instructions [here][cpaulik-unity-icon].

If you're on a mac and didn't install emacs with the spacemacs logo, you can apply
it to the app bundle after installation. An .icns version of the logo by [Nasser
Alshammari](http://www.nass3r.com) is [available from his github](https://github.com/nashamri/spacemacs-logo).
You can paste this into the app bundle to get the spacemacs logo on your emacs.
[More detailed instructions](http://www.idownloadblog.com/2014/07/16/how-to-change-app-icon-mac/)
if you've not done this before.

# Update

Spacemacs currently requires manual updates using the following procedure:

1. Update Emacs packages by clicking (press `RET`) on the `[Update]` link of
the starting page.

2. Close Emacs and update the git repository:

   ```sh
   git pull --rebase
   git submodule sync; git submodule update
   ```

3. Restart Emacs to complete the upgrade.

## Update notification

For convenience an indicator is displayed in the mode-line whenever a new
version of `Spacemacs` is available.

           Symbol                     | Description
:------------------------------------:|----------------------------------
![git-new](doc/img/update-green.png)  | < 3 releases behind
![git-del](doc/img/update-orange.png) | < 5 releases behind
![git-mod](doc/img/update-red.png)    | >= 5  releases behind

**Note:**
A feature allowing update by merely clicking on the indicator will be implemented _soon_!

## Rollback

Should anything go wrong during an update, you can rollback ELPA packages to a
previous version. Click (press `RET`) on the `[Rollback]` link of the startup
page, choose a rollback slot.

Rollback slot names are dates with the following format `YYYY-MM-DD_HH.MM.SS`.
The date corresponds to the date of an update. The most recent slots are
listed first.

# Configuration

`Spacemacs`将不同的配置通过[configuration layers][config]划分为不同的单元，所以的配置变量都在这些单元中。

`Spacemacs` 通过 `~/.spacemacs` 文件去控制哪些 layers 需要加载，同时，这个文件中还可以通过变量启用不同的特性。

## Configuration layers

没一个配置单元目录都包括以下几个问价：

- `packages.el`: 定义和配置需要下载的Emacs包需要使用 `package.el`文件
- `extensions.el`: Configures packages which cannot be downloaded with
  `package.el` such as built-in Emacs features and git submodules.

如果你已经有一份Emacs配置你可以将其移入你自己的配置单元（layer）中。

下面的命令将在 `private` 目录中新建一个layer：

    <SPC> : configuration-layer/create-layer RET

你创建的任何layers都必须在 `~/.spacemacs` 中声明。

**Note:** For your privacy, the contents of the `private` directory are not
under source control. See the documentation for a discussion on how to
[manage your private configuration][manage_config].

## Dotfile (.spacemacs)

在文件 `.spacemacs` 中配置需要加载的layers就是一种定制 `Spacemacs` 的方法。

The following command will create a `.spacemacs` file in your home directory:

    <SPC> : dotspacemacs/install RET

...在Emacs中打开该文件的方法：

    <SPC> f e d

...通过以下变量可以定制需要加载的layers
`dotspacemacs-configuration-layers`:

```elisp
;; List of configuration layers to load.
dotspacemacs-configuration-layers '(auto-completion smex)
```

有些layers支持不同的配置变量，通过这些变量可以定制这些layers的特性。比如，在layer [git layer]中，变量可以在 `dotspacemacs-configuration-layers` 做如下修改：

```elisp
;; List of configuration layers to load.
dotspacemacs-configuration-layers '(auto-completion
                                    (git :variables
                                         git-magit-status-fullscreen t)
                                    smex)
```

在任何时候你都可以通过 <kbd>SPC f e R</kbd> 应用你的修改，而不用重启 `Spacemacs` 。

在文件 `~/.spacemacs` 中有更详细的定制方法，你可以打开文件查看。

# Learning Spacemacs

## Editing Styles

Spacemacs 通过给文件 `~/.spacemacs`变量 `dotspacemacs-editing-style` 赋予 `'vim` 或 `'emacs` 的值来定义不同的编辑风格。

## The leader keys

`Spacemacs` key bindings use a leader key which is by default bound to
<kbd>SPC</kbd> (space bar) in `vim` editing style and <kbd>M-m</kbd> in
`emacs` style.

You can change it by setting the variable `dotspacemacs-leader-key` if
you use the `vim` style or `dotspacemacs-emacs-leader-key` if you use
the `emacs` style (these variables must be set in the file `~/.spacemacs`).

For simplicity the documentation always refers to the leader key as
<kbd>SPC</kbd>.

There is secondary leader key called the major-mode leader key which is
set to <kbd>,</kbd> by default. This key is a shortcut for <kbd>SPC m</kbd>
where all the major-mode specific commands are bound.

## Evil-tutor

If you are willing to learn the Vim key bindings (highly recommended since
you can benefit from them even in `emacs` style), press <kbd>SPC h T</kbd>
to begin an Evil-adapted Vimtutor.

## Universal argument

In `vim` editing style the universal argument defaults to `<SPC> u`
instead of `C-u` because the latter is used to scroll up as in Vim.

## Configuration layers and Package discovery

By using `helm-spacemacs` with <kbd>SPC f e h</kbd> you can quickly search
for a package and get the name of the layers using it.

You can also easily go to the `README.org` of a layer or go to the initialization
function of a package.

## Key bindings discovery

Thanks to [guide-key][], whenever a prefix command is pressed (like `SPC`)
a buffer appears after one second listing the possible keys for this prefix.

It is also possible to search for specific key bindings by pressing:

    SPC ?

To narrow the bindings list to those prefixed with `SPC`,
type a pattern like this regular expression:

    SPC\ b

which would list all `buffer` related bindings.

## Describe functions

`Describe functions` are powerful Emacs introspection commands to get information
about functions, variables, modes etc. These commands are bound thusly:

快捷键        |                 功能
--------------|------------------------------------------------------------------
`<SPC> h d f` | describe函数
`<SPC> h d k` | describe按键
`<SPC> h d m` | describe模式
`<SPC> h d v` | describe变量

# How-To's

Some quick `how-to's` are compiled in the [HOWTOs.org][] file.

# Contributions

`Spacemacs` needs _you_!

We especially need to create more configuration layers that, for instance, bring
support for new languages.

If you are ready to contribute please begin by consulting the
[contribution guidelines][CONTRIBUTE.org] and [conventions][CONVENTIONS.org],
thanks!

# License

The license is GPLv3 for all parts specific to `Spacemacs`, this includes:
- the initialization and core files
- all the layer files.
- the documentation

# Special Credits

[Spacemacs logo][] by [Nasser Alshammari][]
released under a Creative Commons license.

# Supporting Spacemacs

The best way to support Spacemacs is to contribute to it either by reporting
bugs, helping the community on the [Gitter Chat][] or sending pull requests.

If you want to show your support financially you can buy a drink to the
maintainer by clicking on the [Paypal badge](#top).

Thank you !

# FAQ

## Common

1. **Which version of Spacemacs am I running ?**
The version is displayed on the upper right corner of the loading screen.
You may also just type <kbd>SPC f e v</kbd>.

2. **What is the official pronunciation of Spacemacs ?**
As it is written, that is _space_ then _macs_.

3. **Why are packages installed with `package-install` automatically deleted by
Spacemacs when it boots ?**
To declare new packages you have to create a new configuration layer, see
the [quick start guide](#configuration).

4. **The Spacemacs banner is ugly, what should I do ?**
Install the default font supported by Spacemacs or choose a fixed width font.
More information in the [font section][] of the documentation.

5. **The powerline separators are ugly, how can I fix them ?**
Use the property `:powerline-scale` of the variable
`dotspacemacs-default-font`. See [font section][] documentation for more details.

6. **The powerline separators have no anti-aliasing, what can I do ?**
Emacs powerline uses XMP images to draw the separators in a graphical
environment. You can have anti-aliasing if you use the `utf8` separator.
Note that by default the `utf8` separator is used in a terminal.
See the powerline section in the [documentation][powerline-doc].

7. **Why is after-init-hook not executed ?**
Don't launch Spacemacs with `emacs -q -l init.el` command. This command will
run the hooked function in `after-init-hook` before the evaluation of the
passed `-l init.el` file.

## Windows

1. **Why do the fonts look crappy on Windows ?**
You can install [MacType][] on Windows to get very nice looking fonts. It is
also recommended to disable smooth scrolling on Windows.

2. **Why is there no Spacemacs logo in the startup buffer ?**
A GUI build of emacs supporting image display is required.
You can follow the instructions [here][Windows Image Support]. Alternatively you
can download binaries of emacs with image support
included such as [this one][emacs-for-windows].

## OS X

1. **Why are the powerline colors not correct on OS X ?**
This is a [known issue][powerline-srgb-issue] as of Emacs 24.4 due to
`ns-use-srgb-colorspace` defaulting to true. It is recommended to use
the [emacs-mac-port][] build. See the [install OSX section][] for more
details.

[Twitter]: http://i.imgur.com/tXSoThF.png
[CONTRIBUTE.org]: doc/CONTRIBUTE.org
[CONVENTIONS.org]: doc/CONVENTIONS.org
[DOCUMENTATION.org]: doc/DOCUMENTATION.org
[HOWTOs.org]: doc/HOWTOs.org
[VIMUSERS.org]: doc/VIMUSERS.org
[config]: doc/DOCUMENTATION.org#configuration-layers
[dotfile]: doc/DOCUMENTATION.org#dotfile-configuration
[manage_config]: doc/DOCUMENTATION.org#managing-private-configuration-layers
[using_package_buf]: doc/DOCUMENTATION.org#using-the-package-list-buffer
[troubleshoot]: doc/DOCUMENTATION.org#troubleshoot
[contrib layers]: doc/DOCUMENTATION.org#using-configuration-layers
[Git support]: contrib/git/README.org
[git layer]: contrib/git
[ace-jump]: doc/DOCUMENTATION.org#vim-motions-with-ace-jump-mode
[project management]: doc/DOCUMENTATION.org#project-management
[Evil Mode]: doc/DOCUMENTATION.org#evil
[private]: ./private
[layers]: ./contrib
[font section]: doc/DOCUMENTATION.org#font
[powerline-seps]: doc/DOCUMENTATION.org#powerline-separators
[FAQ]: https://github.com/syl20bnr/spacemacs#faq
[dotfile template]: ./core/templates/.spacemacs.template
[install OSX section]: https://github.com/syl20bnr/spacemacs#os-x
[osx layer]: contrib/osx/README.org
[guide-key]: https://github.com/kai2nenobu/guide-key
[guide-key-tip]: https://github.com/aki2o/guide-key-tip
[evil-nerd-commenter]: https://github.com/redguardtoo/evil-nerd-commenter
[Gitter Chat]: https://gitter.im/syl20bnr/spacemacs
[Gitter Chat IRC server]: https://irc.gitter.im/
[MacType]: https://code.google.com/p/mactype/
[emacs-mac-port]: https://github.com/railwaycat/homebrew-emacsmacport
[emacs-mac-port-server]: https://github.com/railwaycat/emacs-mac-port/blob/master/README-mac#L210-L213
[homebrew]: https://github.com/Homebrew/homebrew
[emacs-for-windows]: http://emacsbinw64.sourceforge.net/
[the platinum searcher]: https://github.com/monochromegane/the_platinum_searcher
[powerline-srgb-issue]: https://github.com/milkypostman/powerline/issues/54
[powerline-doc]: doc/DOCUMENTATION.org#powerline-separators
[so-server-unsafe]: http://stackoverflow.com/questions/885793/emacs-error-when-calling-server-start
[Spacemacs logo]: https://github.com/nashamri/spacemacs-logo
[Nasser Alshammari]: https://github.com/nashamri
[cpaulik-unity-icon]: http://splendidabacus.com/posts/2015/03/spacemacs-unity-icon/
[Windows Image Support]: http://stackoverflow.com/questions/2650041/emacs-under-windows-and-png-files
