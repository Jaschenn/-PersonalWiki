# 在Mac上使用Latex输入数学公式以及撰写论文
## 前言
> Mac上使用是MacTex，顾名思义就是Mac上的Latex。

## 安装

[MacTex](http://www.tug.org/mactex/)有两个版本，其中给一个是附带了工具包的MacTex，这个版本较大（4GB左右），另外一个是最小的安装版本，仅仅包含核心部分不带有gui，好在文件很小（70MB左右），为了节省时间我们使用这个最小安装版。

### 使用HomeBrew

如果你有homebrew的话，那就在简单不过了
只需要使用
```
brew cask install basictex
```
就可以进行安装，过程中需要输入密码一次。

### 没有Homebrew 

如果英文不是很好或者网速太慢，还可以在清华大学开源软件站上下载。请自行搜索下载。

### 说明

⚠️注意安装完成之后，有关的命令工具都在
```
/Library/TeX/texbin
```

由于下载的最小版本，为了完成工具链，我们还需要使用Tex的包管理工具来补充缺失的包。
> tlmgr是Tex的包管理工具，我们就是使用它来管理Tex的各种包。

使用如下命令安装：

```
sudo tlmgr install chktex
```
```
sudo tlmgr install latexmk
```

至此我们已经全部安装完成。✅

## 配置编辑器

关于编辑器的选择，每个人有每个人的偏好，在这里我选择的是VS code。

### 安装Latex拓展

打开拓展面板，搜索`Latex`
安装`Latex Workshop`

done✅

 至此，就已经安装和配置好了环境。以下是一些有用的网站：

[如何使用latex输入公式？](https://www.jianshu.com/p/a0aa94ef8ab2)

[常用的数学符号对应表](https://www.jianshu.com/p/c534c18b931a)

[在Windows环境配置Latex环境](https://blog.stackoverflow.club/install-latex-on-win10/)