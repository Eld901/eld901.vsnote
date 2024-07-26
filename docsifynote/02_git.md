##### git笔记
###### 00
###### 01 初始化命令
`git confit --global user.name "your name"`  
`git config --global user.email "your email"`  

###### 02 常用命令
清屏：`clear`  
拷贝文件：`cp -rf filename1.suffix filename2.suffix`  

初始化仓库：`git init filename`  

创建文件夹：`mkdir filename`  
创建文件：`touch filename.suffix`  
创建文件：`echo "hhh" > filename.suffix`  

修改文件内容：`vim filename.suffix`  
查看文件内容：`cat filename.suffix`  
对比前后内容：`git diff filename.suffix`  

删除文件夹：`\rm -rf filename`  
删除文件：`rm filename.suffix`  
硬删除-提示：`git rm filename.suffix`  
软删除-只保留本地，不保留暂存区：`git rm --cached filename.suffix`  

丢弃工作区，丢弃暂存区：`git reset --hard filename.suffix`  
保留工作区，保留暂存区：`git reset --soft filename.suffix`  
保留工作区，丢弃暂存区：`git reset --mixed filename.suffix`  

添加到暂存区：`git add filename.suffix`  
提交到仓库：`git commit filename.suffix -m "message"`  
添加暂存并提交：`git commit -am "message"`  

查看git状态：`git status -s`  
查看提交记录：`git log --oneline`  
查看工作区内容：`ls`  
查看暂存区内容：`git ls-files`  
查看回退操作：`git reflog`  

创建分支：`git branch dev`  
查看当前仓库所有分支：`git branch`  
切换不同分支：`git switch branchname`  

分支和文件同名冲突，默认切换分支  
`git checkout xxx` 切换当前分支  
`git checkout xxx` 恢复文件状态  

合并分支到当前分支：`git merge branchname`  
查看分支图：`git log --graph --oneline --decorate --all `   
定义别命：`alias = "cmd"`  
删除已合并分支：`git branch -d branchname`  
删除未合并分支：`git branch -D branchname`  
恢复删除的分支：`git checkout -b xxx`  

主分支和从分支修改同一文件，  
合并产生冲突，  
重新修改，重新提交，  
中断合并 `git merge --abort`

变基rebase = 将当前合并到目标  
在分支上执行变rebase = 分支合并到主干  
```git
$ git switch dev
$ git rebase master
```
在主干上执行master = 主干合并到分支
```git
$ git switch master
$ git rebase dev
```

标记版本号：`git tag v0.0.0`  
主版本、次版本、修订版本


###### 03 返回消息
Untracked files：新文件，未添加到暂存区  
Changes to be committed：新文件，添加到暂存区，未提交到仓库  
modified：已在暂存区，修改文件内容，未提交到仓库  
deleted：已在暂存区，删除文件，未提交到仓库  
nothing to commit, working tree clean：已在仓库  

撤销添加到暂存区操作：`git restore --staged filename.suffix`  
撤销在仓库的删除操作：`git restore --staged filename.suffix`  
撤销在暂存区删除操作：`git restore filename.suffix`  

###### 04 .gitignore
.gitignore  
已提交到仓库的文件会被纳入版本控制  
空文件夹默认不会被纳入版本控制  

忽略单文件：`filename.suffix`  
忽略多文件：`*.suffix`  
忽略文件夹：`filename/`  

注释：`#`  
任意：`*`  
单个：`?`  
任选：`[]`  
取反：`!`  
范围：`[0-9]` `a-z` `A-Z`  


`*.suffix`  忽略所有`.suffix`文件  
`!filename.suffix`  忽略所有`.suffix`文件除了`filename.suffix`文件  
`filename/*.suffix`  忽略`filename`文件夹下的`.suffix`文件，不忽略子目录下的  
`filename/**/*.suffix`  忽略`filename`文件夹及其子目录下的`.suffix`文件  
`filename/`  忽略任何目录下的`filename`文件夹  
`/filename`  忽略当前目录下的`filename`文件夹，不忽略子目录下的  

###### 05 小结 rm
**小结 rm**  
**提交到仓库后，分别执行以下删除命令，git status的结果**  
rm 仓库删除，暂存区删除，本地删除，无提示
```git 
$ git status
Changes not staged for commit:
  (use "git add/rm <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        deleted:    1.txt
```
git rm 仓库删除，暂存区删除，本地删除，有提示
```git
$ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        deleted:    1.txt
```
git rm --cached 仓库删除，暂存区删除，本地保留
```git
$ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        deleted:    1.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        1.txt
```

###### 06 小结 reset
**小结 reset**  
工作区、暂存区、本地仓库  
git reset --soft 保留工作区，保留暂存区  
git reset --hard 丢弃工作区，丢弃暂存区  
git reset --mixed 保留工作区，丢弃暂存区  
**新建三个commit操作**  
```git
$ cd gitest
$ touch 1.txt 2.txt 3.txt
```
```
$ git add .
$ git commit 1.txt -m "1.txt"
$ git commit 2.txt -m "2.txt"
$ git commit 3.txt -m "3.txt"
```
```
$ cd ..
$ cp -rf gitest t1
$ cp -rf gitest t2
$ cp -rf gitest t3
```
**git reset --soft 保留工作区，保留暂存区**  
```git
$ cd t1
$ git reset --soft HEAD^
```
```
$ ls
1.txt  2.txt  3.txt
```
```
$ git ls-files
1.txt
2.txt
3.txt
```
```
$ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   3.txt
```
**git reset --hard 丢弃工作区，丢弃暂存区**  
```git
$ cd t2
$ git reset --hard HEAD^
```
```
$ ls
1.txt  2.txt  
```
```
$ git ls-files
1.txt
2.txt
```
```
On branch master
nothing to commit, working tree clean
```
**git reset --mixed 保留工作区，丢弃暂存区**  
```git
$ cd t3
$ git reset --mixed HEAD^
```
```
$ ls
1.txt  2.txt  3.txt  
```
```
$ git ls-files
1.txt
2.txt
```
```
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        3.txt
```
##### gitlab 私有化部署
gtihub、gitee、gitlab  
私有化部署：在自己的服务器上部署gitlab代码托管服务，  
使用docker部署在电脑本地，启动后输入localhost访问

克隆github远程仓库到本地：`git clone <github repository path>`    
添加新的远程仓库gitlab：`git remote add <repository alias> <gitlab repository path>`  
移除关联的远程仓库：`git remote remove <repository alias>`  
查看关联的远程仓库地址：`git remote -v`  
提交本地仓库到github默认仓库：`git push`  
提交本地仓库到新的远程仓库：`git push <repository alias> main`  

###### VScode 使用 git
预设置：手动配置VScode的bin目录  
用VScode打开仓库：`code .`  
打开命令面板：【Ctrl】+【Shift】+【P】  

VScode图形化界面
`??` untracked 未跟踪  
`M` modeied 已修改  
`A` added 已添加暂存  
`D` deleted 已删除  
`R` renamed 重命名  
`U` updated 已更新未合并  

Git 图形化界面 GitKraken  
