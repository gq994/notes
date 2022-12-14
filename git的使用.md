# git的使用

### 1. 克隆文件

git clone 仓库地址 （采用静默的方式下载，不需要另存为和解压等相关操作）

### 2. 初始化文件

git init  创建（初始化）空仓库，由git接管，文件的改动（修改、删除）都能监测到

### 3. git的常用命令

​         创建一个hello文件夹 ，里面创建文本 welcome.txt，输入文本保存修改 ，打开git bash here 然后输入

![git](C:\Users\g1843\Desktop\sc\课堂笔记\image\git.jpg)

**git的常见命令**

#### 1. git init

 初始化文件夹，监听到文件中的改动

#### 2. git status 

查看文件状态，例如：修改，添加或删除了那些文件

#### 3. git add ./

 (git add . 或者 git add -A) 将修改文件添加到暂存区

#### 4. git commit -m '版本' 

将修改暂存区中的文件提交一个版本 

#### 5. git log 

 命令可以显示当前分支所有提交过的版本信息，不包括已经被删除的 commit 记录和reset的操作。

#### 6. git log --pretty=oneline

直接使用git log显示的信息太繁琐，可以加上参数 **--pretty=oneline** 只会显示版本号和提交时的备注信息，这样阅读起来更友好得多。

#### 7. git reflog  

命令可以查看所有分支的所有操作记录信息（包括已经被删除的 commit 记录和 reset 的操作）。

参考：https://blog.csdn.net/Seky_fei/article/details/114729213

<!--**git log 和 git reflog的最大区别是能不能查询到被删除的 commit 记录和 reset 的操作记录，log不能，而reflog可以；所以以后要买后悔药就去找reflog。**-->

#### 8. git reset --hard HEAD^  

回到上一个版本

git reset --hard 版本号   回到指定版本

<!--版本号可以通过git reflog来查-->

#### 9. git diff 文件名

显示暂存区和工作区的差异

#### 10. git diff --staged 文件名 

或者是使用 git diff --cached 文件名     显示暂存区和上次提交（commit）的差异

### 4. git的撤销命令

#### 1. git checkout -- 文件名

在工作区编辑文件后保存并关闭，使用该命令可以撤销工作区的操作，从来没有被添加到版本库就被删除的文件，是无法恢复的！

#### 2. git reset HEAD 文件名

可以将文件从暂存区撤销到工作区

#### 

