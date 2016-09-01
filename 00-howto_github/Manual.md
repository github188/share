Git 是当前最流行的版本控制程序之一，文本包含了 Git 的一些基本用法 

#创建 git 仓库 初始化 git 仓库

    mkdir project   # 创建项目目录 
    cd project      # 进入到项目目录 
    git init        # 初始化 git 仓库。此命令会在当前目录新建一个 .git 目录，用于存储 git 仓库的相关信息


#初始化提交

    touch README 
    git add .       # 将当前目录添加到 git 仓库中， 使用 git add -A 则是添加所有改动的文档 
    git commit  -m  "Initial commit" 
    git remote add origin  git@github.com:username/repo.git  # 设置仓库


#修补提交（修补最近一次的提交而不创建新的提交）
    git commit  --amend  -m  "commit message."

#提交冲突时可以合并后再推送
    git pull  # 获取远程版本库提交与本地提交进行合并 
    git push  # 提交

#使用别人的仓库
    git clone http://path/to/git.git  #clone 的内容会放在当前目录下的新目录

#将代码从本地回传到仓库
    git push  -u origin master

#使用 git status 查看文件状态
    git status

#查看提交日志
    git log  # 查看提交信息 
    git log  --pretty=oneline  # 以整洁的单行形式显示提交信息

#Git 分支
    git branch  # 查看分支 
    git branch  6.x- 1.x  # 添加分支 6.x-1.x 
    git branch checkout master  # 切换到主分支 
    git branch  -d  6.x- 1.x  # 删除分支 6.x-1.x 
    git push origin :branchname  # 删除远端分支

#Git 标签
    git tag  # 查看分支 
    git tag  6.x- 1.0  # 添加标签 6.x-1.0 
    git show  6.x- 1.0  # 查看标签 6.x-1.0 的信息 
    git tag  -a  6.x- 1.0 965e066  # 为之前提交的信息记录 965e066 加上标签 
    git push  --tags  # 提交时带上标签信息 
    git push origin : /refs /tags /tagname  # 删除远端标签

#从 git 仓库中导出项目

    git archive  --format  tar  --output  /path /to /file.tar master  # 将 master 以 tar 格式打包到指定文件


#git log 查看log

    git log -p                  #查看每个commit号改变了什么
    
    git log -p file             #查看file改变了什么
    
    git log --parents commit    #可以查看commit的父commit
    
    git branch                  #查看当前目录下有哪些分支
    
    git branch -a               #查看所有的分支
    
    git fetch origin a:a        #从origin那得到a这个分支
    
    git checkout a              #进入a这个分支
    
    git clean -xdf              #清空以前配置，编译的文件
    
    git reset --hard            #回到当前的commit,会清理文件
    
    git reset --hard commit-a   #回到commit-a

 
#当你修改文件后准备push上去

    git diff                #看看你改的地方是否正确 
    
    git status              #看看你当前是否提交了代码，或是否改动了代码
    
    git add file1 file2     #为下一个commit准备contents(即要push 上去的文件)
    
    git commit --author "Your name <email>"   #为你要提交的代码写log
    
    git log                 #查看你写的log是否正确
    
    git push                #push代码
    
    git status              #再检查一次


##使用 Git 的一些基本守则： 当要commit/提交patch时：

1. 使用 git diff --check 检查行尾有没有多余的空白
2. 每个 commit 只改一件事情。
3. 如果一个文档有多个变更，使用 git add --patch 只选择文档中的部分变更进入stage
4. 写清楚 commit message



