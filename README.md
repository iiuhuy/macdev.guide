# 我的 MacOS 环境搭建

> YuHui’s macOS setup guide. 持续更新。

作为开发人员，搭建自己的熟悉的开发环境。(总结笔记) Mac 下一些基础软件，使用 brew 与 brew cask 统一管理。

## 0x01 软件

1.下载软件。

- [WeChat](https://weixin.qq.com/)
- [JetBrains](https://www.jetbrains.com/toolbox/app/?fromMenu)

## 0x02 通用开发

1.安装 XCode，在 App Store 里面免费下载。

2.安装 [HomeBrew](https://brew.sh/index_zh-cn)

brew 是 Mac 下的包管理，常用的命令提示符都可以用它来安装。与 [HomeBrew-Cask](https://github.com/Homebrew/homebrew-cask)

```bash
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

3.Install brew Casks
基于 brew 的 Mac 程序封装机制。

安装 Google-Chrome、Iterm2、Sourcetree、Alfred

```bash
brew cask install google-chrome
brew cask install iterm2 sourcetree alfred
```

4.虚拟机

```
brew cask install virtualbox
brew cask install vagrant
```

## 一键装机

很多常用的软件都可以一起一键安装。

使用 brew 与 brew cask，就不用去慢慢找软件包下载安装等等一个个慢慢的安装了。



## 参考

- Phodal's 前端程序员的 macOS 搭建指南：https://phodal.github.io/setup.guide/
- Mac 入门笔记：https://www.yangzhiping.com/tech/mac1.html
