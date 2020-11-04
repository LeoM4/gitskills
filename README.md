# gitskills
git clone git@github.com:LeoM4/gitskills.git

1. 下载git ： https://git-scm.com/downloads
2. 安装，并配置用户信息
linux: 先检查是否安装git
$ git
The program 'git' is currently not installed. You can install it by typing:
sudo apt-get install git

sudo apt-get install git //Debian 或 Ubuntu

windows 下载后 一直下一步

3. 配置：打开gitbash
$ git config --global user.name "Your Name"
$ git config --global user.email "email@example.com"


4. 创建并初始化
$ mkdir learngit
$ cd learngit
$ pwd
/Users/michael/learngit


初始化本地库：
git init


git 常用命令
git add filename.file <---> git rm <file>
git commit -m" log context"
git status
git diff name.file
git log // 查看提交历史
git reset--hard HEAD^ //HEAD表示当前版本，指向当前版本的HEAD指针，
回退版本只是改变指针指向
git reset --hard 1094a... 根据commint id 来回退
git reflog  //查看历史命令
git checkout -- name.file //就是让这个文件回到最近一次git commit或git add时的状态。
git reset HEAD <file> //把暂存区的修改撤销，unstage，回到工作区
git checkout -b dev
git checkout 1094a
git checkout dev
git checkout master
git merge dev   把dev分支接到当前分支，并移动HEAD 【只有一个参数】
git rebase dev  把当前分支并到dev上               【】
git rebase dev feature  把feature 并到dev上。。。 【后面的并到前面】
git branch -f master HEAD~3
git reset HEAD^
git revert HEAD


工作区   working Directory  
版本库 Repository
暂存区Stage

【注】
git checkout其实是用版本库里的版本替换工作区的版本，无论工作区是修改还是删除，都可以“一键还原”。



远程仓库：
1. 先获取本地ssh key
$ ssh-keygen -t rsa -C "youremail@example.com"

2. 远程设置，添加ssh key
github account setting - SSH Keys

关联远程仓库
git remote add origin git@server-name:path/repo-name.git

git push -u origin master

git push origin master

$ git clone git@github.com:githubusername/repo-name.git


远程仓库命令：
git checkout origin/master //切换到远程仓库分支
git commin            
git fetch      //从远程仓库下载更新同步，并未修改本地master分支
git fetch origin remote:place
git merge origin/master 把目标分支接到当前分支

git pull = git fetch+ fit merge
git push
git push <remote> <place>
git push origin <source>:<destination>

git pull --rebase; git push
git reset --hard origin/master //根据远程master来回退。
git push origin feature

git rebase master feature




分支管理
git checkout -b totallyNotMaster o/master  
//创建一个名为 totallyNotMaster 的分支，它跟踪远程分支 o/master。

git branch -u o/master foo  //已有foo 分支,跟踪origin/master





标签管理


