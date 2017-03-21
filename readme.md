# 常用Git命令清单  
## Git 名词解释  
* workspace: 工作区  
* stage：暂存区  
* repository：仓库  
* remote：远程仓库  

## 配置  

配置全局用户信息，用来标识commit的用户  
>$ git config --global user.name "your user name"  
>$ git config --global user.email "youremail@XXX.XXX"  

获取Git配置信息  
>$ git config --list  

## 创建版本库  

在当前目录初始化Git库  
>$ git init  

新建一个目录，将其初始化为Git代码库  
>$ git init [project-name]  

下载一个项目和它的所有历史版本  
>$ git clone [url]  

## 添加文件到版本库  

filename为需要添加的文件名，包括文件后缀   
>$ git add \<filename\>  

一次可以add多个文件  
>$ git add \<filename\> \<filename\> \<filename\>  

## 提交文件到仓库  

提交更改，“some words”为本次commit 的说明,一般为有意义性说明，方便从历史记录找到改动记录  
>$ git commit -m "some words"  

## 查看仓库状态  

>$ git status  

## 查看文件具体修改内容  

>$ git diff \<filename\>  

## 版本回退  

### 查看commit历史记录

git log 无法查看已经删除的commit记录。
>$ git log  

### 执行回退命令

首先，Git必须知道当前版本是哪个版本，在Git中，用HEAD表示当前版本，
上一个版本就是HEAD^，上上一个版本就是HEAD^^，当然往上100个版本写100个^比较容易数不过来，所以写成HEAD~100。
>$ git reset --hard HEAD^

可以通过git reflog 来查看所有版本记录，包括已经删除的commit记录。
>$git reflog

## 添加远程仓库

origin为自定义标识远程仓库名称，后跟远程仓库地址。
>$ git remote add origin xxxxxx

## 远程仓库文件复制到本地

git pull命令的作用是，取回远程主机某个分支的更新，再与本地的指定分支合并。如果远程分支是与当前分支合并，则冒号后面的部分可以省略。
>$ git pull <远程仓库名> <远程分支名>:<本地分支名>