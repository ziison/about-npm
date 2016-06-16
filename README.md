# npm详解

NPM（node package manager），通常称为node包管理器。顾名思义，它的主要功能就是管理node包，包括：安装、卸载、更新、查看、搜索、发布等。
能解决NodeJS代码部署上的很多问题，常见的使用场景有以下几种：

* 允许用户从NPM服务器下载别人编写的三方包到本地使用。

* 允许用户从NPM服务器下载并安装别人编写的命令行程序到本地使用。

* 允许用户将自己编写的包或命令行程序上传到NPM服务器供别人使用。

可以看到，NPM建立了一个NodeJS生态圈，NodeJS开发者和用户可以在里边互通有无。
> JS模块的基本单位是单个JS文件，但复杂些的模块往往由多个子模块组成。为了便于管理和使用，我们把由多个子模块组成的大模块称做`包`(package)，并把所有子模块放在同一个目录里。

在安装node的时候，会连带一起安装npm。如果node附带的npm不是最新版可用下面的命令更新。

``` 
$ npm install npm@latest -g
```

## 使用npm管理包

### 安装依赖包

node包的安装分两种：本地安装、全局安装。两者的区别如下：

* 本地安装：package会被下载到当前所在目录，也只能在当前目录下使用。

* 全局安装：package会被下载到到特定的系统目录下，安装的package能够在所有目录下使用。

#### 1.本地安装

``` 
$ npm install packageName
```
安装完毕后会产生一个node_modules目录，其目录下就是安装的各个node模块。

#### 2.全局安装

``` 
$ npm install packageName -g
```
在全局模式下，Node包会被安装到Node的安装目录下的node_modules下。

#### 3.示例

``` 
npm install express 
```

默认会安装express的最新版本，也可以通过在后面加版本号的方式安装指定版本，如： 
``` 
npm install express@3.0.6 
```
