## 指令 ##
### 基本指令 ###
*  git config --global user.name "Your Name"
*  git config --global user.email "email@example.com"
    --global：所有的Git仓库都会使用这个配置
*  git init：初始化Git库
* 添加文件到Git仓库，分两步：
  git add <file>  把文件修改添加到暂存区
  git commit -m <message>  把暂存区的所有内容提交到当前分支
* git status :查看git状态
*  git diff : 查看修改内容
*  git log ：查看提交历史
*  git reset --hard HEAD^ :回退到上一版本
  HEAD ：当前版本，HEAD^ ：上一版本，HEAD^^ ：上上版本 HEAD~n：历史版本 
*  git reflog：查看命令历史
*  git diff HEAD -- file 查看工作区和版本库里面最新版本的区别
*  git checkout -- file 丢弃工作区修改，让文件回到最近一次git commit或git add时的状态
*  git reset HEAD <file> 把暂存区的修改撤销掉（unstage），重新放回工作区
*  删除文件
  git rm file git commit -m <message>
  
 ### 远程仓库 ###
* 创建SSH key: ssh-keygen -t rsa -C "youremail@example.com"
* git remote add origin git@server-name:path/repo-name.git 关联远程仓库
* git push origin master 把本地master分支的最新修改推送至GitHub 第一次推送：git push -u origin master
* git clone git@github.com:your name/repo name.git ：克隆远程库
### 分支 ###
* git branch 查看分支
* git branch <name> 创建分支
* git checkout <name> 切换分支
* git checkout -b <name> 创建并切换分支
* git merge <name> 合并某分支到当前分支
  git merge --no-ff -m "description" dev
    --no-ff ：普通模式合并
    fast forward ：删除分支后，会丢掉分支信息
* git branch -d <name> 删除分支
* git log --graph 查看分支合并图
