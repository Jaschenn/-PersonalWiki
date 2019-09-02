# HomeBrew 

HomeBrew 是Mac上十分好用的包管理工具。
```
如果使用过 Linux，那么一定不会对 yum 或者 apt 感到陌生。homebrew 就是 Mac 上的这样的一个包管理工具。
```
> 如果没有使用过，下面是一个简单地介绍：
假设你需要下载一个应用，那么可能需要经历打开网站-下载 .DMG 映像-挂载，打开，拖入Application 文件夹....。但是使用包管理工具就可以一个命令完成上述操作。


## 安装

Mac 中已经包含了 ruby，所以我们可以使用 ruby 方便的完成 homebrew 的安装。
```BASH
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```
> 来自于 HomeBrew [官网](https://brew.sh/index_zh-cn.html)

## QuickStart

* 搜索
```
brew search 
```
* 安装
```
brew install
```
* 卸载
```
brew uninstall
```

好了，现在这些已经足够日常使用了。

*Tips：*
HomeBrew还可以安装应用程序(GUI)，只需要使用```brew cask search```即可，同样安装使用```brew cask install ```

## brew做了什么？

brew会将软件安装到独立的目录。
位于：```/usr/local/Cellar/```,cask位于```/usr/local/cask/```中。安装到此的文件会被软链接到```/usr/local```

> Notice:HomeBrew 除了自己的目录，HomeBrew不会安装到其他目录，所以实际上你可以把HomeBrew安装到任何位置。

## 下载太慢？

### 替换索引内容为清华源
```
cd "$(brew --repo)"
git remote set-url origin https://mirrors.tuna.tsinghua.edu.cn/git/homebrew/brew.git
cd "$(brew --repo)/Library/Taps/homebrew/homebrew-core"
git remote set-url origin https://mirrors.tuna.tsinghua.edu.cn/git/homebrew/homebrew-core.git
brew update
```

### 替换二进制预编译镜像
**对于zsh用户**
```
echo 'export HOMEBREW_BOTTLE_DOMAIN=https://mirrors.tuna.tsinghua.edu.cn/homebrew-bottles' >> ~/.zshrc
source ~/.zshrc
```
**对于bash用户**
```
echo 'export HOMEBREW_BOTTLE_DOMAIN=https://mirrors.tuna.tsinghua.edu.cn/homebrew-bottles' >> ~/.bash_profile
source ~/.bash_profile

```
That's all ✅