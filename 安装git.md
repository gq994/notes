# git的使用

1. ### 安装git

官网https://git-scm.com/downloads

淘宝镜像https://npm.taobao.org/mirrors/git-for-windows/

2. ### 打开桌面的git bush here 

输入 git -v 查看git版本 

3. ### 配置git用户名，邮箱，设置默认记事本编辑器

   git config --global user.name "Your Name"  ---配置用户名

   git config --global user.email "email@example.com" ---配置邮箱

   git config --global core.editor "编辑器的目标路径"   ---配置默认记事本编辑器编辑文本 

   （git config --global core.editor "C:/Windows/notepad.exe"设置编辑器为记事本，写好回车键执行）

 4. ### 查看git 配置

    git config --list 查看git的配置项

 5. ### 克隆文件

    git clone 仓库地址 （采用静默的方式下载，不需要另存为和解压等相关操作）

 6. ### 初始化文件

    git init  创建（初始化）空仓库，由git接管，文件的改动（修改、删除）都能监测到

 7. ### 创建一个hello文件夹 ，里面创建文本 welcome.txt，输入文本保存修改 ，打开git bash here 然后输入

    1. git status 查看文件中修改了那些文件
    2. git add ./ (git add . 或者 git add -A) 将修改文件添加到暂存区
    3. git commit -m 'name' 将修改暂存区中的文件提交一个版本 

