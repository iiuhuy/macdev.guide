# 我的 MacOS 环境搭建

> YuHui’s macOS setup guide. 持续更新。

作为开发人员，搭建自己的熟悉的开发环境。(总结笔记) Mac 下一些基础软件，使用 brew 与 brew cask 统一管理。

## 科学上网

- https://github.com/qinyuhang/ShadowsocksX-NG-R/releases
- [Shadowsocks for OSX](https://github.com/shadowsocks/shadowsocks-iOS/wiki/Shadowsocks-for-OSX-%E5%B8%AE%E5%8A%A9), [下载 dmg 解压](https://github.com/shadowsocks/shadowsocks-iOS/releases)，拖到应用程序，设置自己的服务器节点即可。

## 通用开发

1.安装 XCode，在 App Store 里面免费下载。

2.安装 [HomeBrew](https://brew.sh/index_zh-cn)

brew 是 Mac 下的包管理，brew 主要用来下载一些不带界面的命令行下的工具和第三方库来进行二次开发。

```bash
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

安装通用软件:

```bash
brew install wget
brew install curl
brew install openssl
brew install imagemagick gs #未来Rails图片处理需要
# brew install gfortran #未来R语言等编译需要
brew install node #未来安装Ruby web服务器pow需要
brew install zsh
brew install python3
# some tools
brew install wget nvm gradle git-extras scrcpy coreutils gnu-sed  —with-default-names
# docker
brew install kitematic
# search
brew install elasticsearch
# ffmpeg
brew install ffmpeg --with-faac --with-libssh --with-libvorbis --with-libvpx --with-openssl --with-opus --with-theora --with-webp --with-x265
# postman
brew install postman
# 矢量
brew install potrace
# Phodal 常用
brew cask install xquartz inkscape gimp blender
```

>Terminal 用 iTerm2 + zsh + oh-my-zsh 的组合，配置 oh-my-zsh，只需要[执行一行命令](https://ohmyz.sh/)。

3.[Install Brew-Casks](https://github.com/Homebrew/homebrew-cask/blob/master/USAGE.md)

再也不用拖动图标的安装软件，「“To install, drag this icon…” no more!」，保证 HomeBrew 不低于 0.9.5 。

```bash
brew tap phinze/homebrew-cask
brew install brew-cask
```

基于 brew 的 Mac 程序封装机制, Brew-Casks 主要用来下载一些带界面的应用软件，下载好后会自动安装，并能在 mac 中直接运行使用。

```bash
brew cask install google-chrome
brew cask install iterm2 sourcetree alfred
# Daily
brew cask install neteasemusic sketch thunder firefox baiducloud
brew cask install virtualbox shadowsocksx charles
brew cask install vlc                #视频软件
# 虚拟机
brew cask install virtualbox
brew cask install vagrant
# vscode
brew cask install visual-studio-code
```

## 一键装机

很多常用的软件都可以一起一键安装。

使用 brew 与 brew cask，就不用去慢慢找软件包下载安装等等一个个慢慢的安装了。你自己也可以总结自己常用的软件，一次性安装。

更新已安装的程序：

在终端中输入：`brew update && brew upgrade` 即可。

// TODO 一键安装

# 开发相关配置

## vscode

安装 Settings Sync 插件，[同步自己的  VSCode 插件](https://gist.github.com/AlvinMi/289dd0d76ca746fc9dedb9f530569ffd)。

## JDK

```bash
brew tap caskroom/versions
brew cask install java8
```

## Git Config

```bash
git config --global user.email "alvin.mi0620@gmail.com"
git config --global user.name "AlvinMi"
ssh-keygen -o 
cat ~/.ssh/id_rsa.pub
# 复制到 GitHub 设置 -> SSH
```

Get Token: [Personal access tokens](https://github.com/settings/tokens).

## 其他软件推荐

- Mac 用户可以使用 Multipass 搞一套 Ubuntu 系统，除了图形界面，基本上都能用。这个几年使用 Ubuntu 下来，体验还是不错的。 
- 社交软件：[WeChat](https://weixin.qq.com/)、QQ、钉钉(工作)、[Telegram](https://macos.telegram.org/)、
- [Cyberduck](https://cyberduck.io/)
- [JetBrains](https://www.jetbrains.com/toolbox/app/?fromMenu)

## Python 

> 这里有配置：https://www.yangzhiping.com/tech/mac-dev.html

## 参考

- Installing Development environment on macOS: http://sourabhbajaj.com/mac-setup/
- Phodal's 前端程序员的 macOS 搭建指南：https://phodal.github.io/setup.guide/
- Mac 入门笔记：https://www.yangzhiping.com/tech/mac1.html
- Mac 开发者 2013 年新机设置参考：https://www.yangzhiping.com/tech/mac-dev.html
- 装了啥：https://github.com/sorrycc/blog/issues/16

欢迎加入 [Telegram Channel](https://t.me/joinchat/AAAAAFN6x9m8LhwqkkHG4w) 记录个人学习的笔记。(需要科学上网)
<a href="https://t.me/joinchat/AAAAAFN6x9m8LhwqkkHG4w"><img src="https://raw.githubusercontent.com/AlvinMi/2019-Pic/master/20190223094415.png" width="190px" height="190px"/></a>
