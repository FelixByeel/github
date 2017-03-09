# 常用Git命令清单  
## Git 名词解释  
* workspace: 工作区  
* stage：暂存区  
* repository：仓库  
* remote：远程仓库  

## 配置  

\# 配置全局用户信息，用来标识commit的用户  

>$ git config --global user.name "your user name"  

>$ git config --global user.email "youremail@XXX.XXX"  

\# 获取Git配置信息  

>$ git config --list  

## 创建版本库  

\# 在当前目录初始化Git库  

>$ git init  

\# 新建一个目录，将其初始化为Git代码库  

>$ git init [project-name]  

\# 下载一个项目和它的所有历史版本  

>$ git clone [url]  

### 添加文件到版本库  

\# filename为需要添加的文件名，包括文件后缀   

>$ git add \<filename\>  

\# 一次可以add多个文件  

>$ git add \<filename\> \<filename\> \<filename\>  

### 提交文件到仓库  

\# 提交更改，“some words”为本次commit 的说明,一般为有意义性说明，方便从历史记录找到改动记录  

>$ git commit -m "some words"  

## 查看仓库状态  

>$ git status  

### 查看文件具体修改内容  

>$ git diff \<filename\>  

## 版本回退  

### 查看commit历史记录  
>$ git log  
 
