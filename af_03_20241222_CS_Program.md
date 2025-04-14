## F 笔记
### Program 编程
#### 2024---- 前端路线 https://www.bilibili.com/read/cv10431130/
01 从0到1学前端HTML5+CSS3：https://www.bilibili.com/video/BV1kM4y127Li
01 前端基础进阶：https://www.bilibili.com/video/BV1xq4y1q7jZ/
02 JavaScript核心前端 前端必学：https://www.bilibili.com/video/BV1Y84y1L7Nn/
03 前端框架前置课：https://www.bilibili.com/video/BV1MN411y7pw/
04 Node.js：https://www.bilibili.com/video/BV1a34y167AZ/
05 Vue2+3：https://www.bilibili.com/video/BV1HV4y1a7n4/
06 iHRM人资项目：https://www.bilibili.com/video/BV1Te411X7Wz/
07 Vue3小兔鲜：https://www.bilibili.com/video/BV1Ac411K7EQ/
08 微信小程序Vue3+TS实战开发：https://www.bilibili.com/video/BV1Bp4y1379L/
09 微信小程序从搭建到项目上线：https://www.bilibili.com/video/BV1834y1676P/
10 TypeScript入门到实战：https://www.bilibili.com/video/BV14Z4y1u7pi/
11 React18：https://www.bilibili.com/video/BV1ZB4y1Z7o8/
11 React从入门到项目开发：https://www.bilibili.com/video/BV1gh411U7JD/
12 前端面试必考：https://www.bilibili.com/video/BV1mH4y1Q7Z7/
#### 2024---- Java路线 https://www.bilibili.com/read/cv9965357/
01 20天精通Java：https://www.bilibili.com/video/BV1Cv411372m/
01 Java入门到起飞上：https://www.bilibili.com/video/BV17F411T7Ao/
01 Java入门到起飞下：https://www.bilibili.com/video/BV1yW4y1Y7Ms/
01 一套超哇塞的Java教程：https://www.bilibili.com/video/BV1Fv4y1q7ZH/
01 从0到1学Java：https://www.bilibili.com/video/BV18J411W7cE/
02 JavaWeb全链路开发：https://www.bilibili.com/video/BV1yGydYEE3H/
02 JavaWeb企业开发流程：https://www.bilibili.com/video/BV1m84y1w7Tb/
03 苍穹外卖：https://www.bilibili.com/video/BV1TP411v7v6/
04 AI+若依：https://www.bilibili.com/video/BV1pf421B71v/
05 SpringCloud微服务开发与实战：https://www.bilibili.com/video/BV1S142197x7/
05 学成在线：https://www.bilibili.com/video/BV1j8411N7Bm/
06 黑马头条：https://www.bilibili.com/video/BV1Qs4y1v7x4/
07 Java大厂面试题：https://www.bilibili.com/video/BV1yT411H7YK/
08 Java面试宝典：https://www.bilibili.com/video/BV15b4y117RJ/

#### 20241224 鱼皮编程工具 https://www.bilibili.com/video/BV1Ab4y1r7bo
【在线编辑器】小闪电：https://jsrun.net/
【在线编辑器】菜鸟工具：https://tool.cainiaoplus.com/
【在线编辑器】菜鸟工具：https://www.jyshare.com/compile/10/
【在线编辑器】BEJson：https://www.bejson.com/
【在线编辑器】码曰：https://www.dotcpp.com/run/
【在线编辑器】编程中国：https://www.bccn.net/run/
【在线编辑器】在线工具：https://tool.lu/coderunner/
【在线编辑器】Jupyter：https://jupyter.org/
【在线IDE】腾讯云CODING：https://e.coding.net/
【在线IDE】前端新技术Svelte：https://www.svelte.cn/
【在线IDE】codesandbox：https://codesandbox.io/
【在线IDE】codepen：https://codepen.io/
【在线IDE】coder：https://coder.com/
【在线IDE】gitpod：https://www.gitpod.io/
【在线IDE】REMIX：https://remix-project.org/
【本地编辑器】Typora version 0.9.97
【本地编辑器】Notepad++(64-bit x64)
【本地编辑器】VSCode-win32-x64-1.96.0
【本地编辑器】SublimeText3
【本地编辑器】Atom
【本地编辑器】Vim
【本地IDE】JetBrains WebStorm(前端)
【本地IDE】JetBrains InteliJ IDEA 2024.2.0.1
【本地IDE】VisulStudio
【本地IDE】Eclipse
【本地IDE】devcpp(C++)
【本地IDE】HbuilderX(前端小程序app)
【本地IDE】QtCreater(C++桌面应用)
【本地IDE】CodeBlocks(简单C++项目)
【本地IDE】AndroidStudio(安卓)
【本地IDE】SpringToolSuite(Spring)
【本地IDE】Xcode(mac应用)

#### 20240725 Docsify：https://www.bilibili.com/video/BV1kT4y1T7wY/
###### 01 安装和初始化
安装nodejs，npm
安装docsify：`npm i docsify-cli -g`
初始化docsify：`docsify init`
启动docsify：`docsify serve`
创建文件：`docsify init docsname`
本地预览：`docsify serve docsname`
本地浏览：http://localhost:3000

注意事项：在markdown中修改以后【Ctrl】+【S】保存
###### 02 层级页面的路径引用
```
* [首页](/)
* [指南](guide.md)

* 目录
  * [js](01/js/js.md)
  * [ec](01/ec/ec.md)
```
路径解释：01文件夹下，js文件夹下的，js.md文件
注意事项：如果文件夹下只有一个README.md文件，则可以省略js.md文件,直接写js文件夹即可
###### 03 预制页和属性
```html
<script>
    window.$docsify = {
      name: '',
      repo: '',
      loadSidebar:true,
      loadNavbar:true,
      subMaxLevel: 3
    }
</script>
```
属性文件index.html
侧边栏：`loadSidebar:true`
导航栏：`loadNavbar:true`
封面页：`coverpage: true`
独立封面：`onlyCover:false`
目录层级：`subMaxLevel: 3`

页面类型
普通页面：`name.md`
侧边栏：`_sidebar.md`
导航栏：`_navbar.md`
封面页：`coverpage.md`
###### 04 发布远端
生成密钥：`ssh-keygen -t rsa -C "<email>"`
查看密钥：`cat id_rsa.pub`
验证链接：`ssh -T git@github.com`
克隆仓库：`git clone <path>`

流程解释：
在本地生成一对密钥，公钥和私钥；
公钥配置到github，私钥本地存储在.ssh文件夹；
验证链接，本地仓库和github仓库建立连接后，
clone和push操作就不用每次登录验证密码；
在github中创建仓库`name.github.io`，部署网页；
克隆github仓库到本地，复制docsify文件到仓库根目录；
打开VScode，进行`git add` 和 `git commit` 提交到github

把仓库克隆到本地，仓库不能为空，
把docsify转移到仓库，再从本地提交到github。

直接在本地创建docsify，提交到仓库，
命名新仓库为`name.github.io`，部署网页。
#### 20240726 Git：https://www.bilibili.com/video/BV1HM411377j/
###### 01 初始化命令
`git confit --global user.name "your name"`
`git config --global user.email "your email"`
###### 02 常用命令
清屏：`clear`
拷贝文件：`cp -rf filename1.suffix filename2.suffix`

创建文件夹：`mkdir filename`
初始化仓库：`git init filename`
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

查看当前仓库所有分支：`git branch`
查看分支图：`git log --graph --oneline --decorate --all ` 
定义别命：`alias = "cmd"`
创建分支：`git branch dev`
切换不同分支：`git switch branchname`

分支和文件同名冲突，默认切换分支
`git checkout xxx` 切换当前分支
`git checkout xxx` 恢复文件状态

合并分支到当前分支：`git merge branchname`
产生冲突中断合并 `git merge --abort`
删除已合并分支：`git branch -d branchname`
删除未合并分支：`git branch -D branchname`
恢复删除的分支：`git checkout -b xxx`

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
空文件夹默认不会被纳入版本控制
已提交到仓库的文件会被纳入版本控制

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
###### 07 VScode 使用 git
预设置：环境变量，手动配置VScode的bin目录
VScode命令面板：【Ctrl】+【Shift】+【P】
用VScode打开仓库：`code .`
Git 图形化界面：GitKraken

VScode图形化界面
`??` untracked 未跟踪
`M` modeied 已修改
`A` added 已添加暂存
`D` deleted 已删除
`R` renamed 重命名
`U` updated 已更新未合并
###### 08 gtihub、gitee、gitlab私有化部署
github、gitee、gitlab
`git add` `git commit` `git push`
私有化部署：在自己的服务器上部署gitlab代码托管服务，
使用docker部署在电脑本地，启动后输入localhost访问

克隆github远程仓库到本地：`git clone <github repository path>`
添加新的远程仓库gitlab：`git remote add <repository alias> <gitlab repository path>`
移除关联的远程仓库：`git remote remove <repository alias>`
查看关联的远程仓库地址：`git remote -v`
提交本地仓库到github默认仓库：`git push`
提交本地仓库到新的远程仓库：`git push <repository alias> main`
#### 20240727 Linux：https://www.bilibili.com/video/BV1n84y1i7td/
###### 01 Linux简介
安装虚拟机、操作系统、远程连接
`ncpa.cpl` 打开网络连接

windows：`\` `D:\data\work\hello.txt`
Linux：`/` `/user/local/hello.txt`
根目录、家目录、当前工作目录
###### 02 权限
`ifconfig` 查看本机ip地址 `inet 192.168.118.128`
`hostname` 查看主机名 `localhost.localdomain`
`hostnamectl set-hostname <hostname>`  修改主机名

`getent passwd` 查看所有用户 `用户名：密码x：用户ID：组ID：描述信息：home目录：终端`
`getent group` 查看所有组 `组名称：组认证x：组ID：`
`id` `id <username>`  查看用户信息

`ls -l`  查看当前 列表
**`drwxr-xr-x.`** `2` `root` `root` `4096 Aug 18 17:53` `data`
**`d` `rwx` `r-x` `r-x`** 权限细节    `文件` `所属user权限` `所属group权限` `other用户权限`
`-|d|l` `r|w|x` `r|w|x` `r|w|x` 
**`-`** 文件 **`d`** 文件夹 **`l`** 软链接
**`r`** 读 4  **`w`** 写 2  **`x`** 执行 1
0：`---` 000
1：`--x` 001
2：`-w-` 020
3：`-wx` 021
4：`r--` 400
5：`r-x` 401
6：`rw-` 420
7：`rwx` 421

---
`chown -R <username>:<groupname> <file path>`  修改文件及其子文件所属用户和组
`chmod -R u=rwx,g=rx,o=x <file path>`  修改文件及其子文件权限
`chmod -R 751 <file path>`  修改文件及其子文件权限

`useradd <username> -g <groupname> -d <homepath>`  创建用户 设组与home目录
`usermod -aG <groupname> <username>`  为用户添加组
`userdel -r <username>`  删除用户和home目录
`groupadd <groupname>`  创建用户组
`groupdel <groupname>`  删除用户组

---
切换超级管理员root用户：`su - root` `<password>`
退回普通用户：`exit`  `【Ctrl】+【D】`
切换指定用户：`su - <username>`

使用临时root权限执行命令:`sudo <cmd>`
临时root：为普通用户配置sudo认证:
```shell
su - root <password>
visudo (vi /etc/sudoers)
<username> ALL=(ALL)【Tab】NOPASSWD:ALL
:wq
```
###### 03 Linux cmd 
**`command` `-option` `parameter`**
查看历史命令：`history`
倒序匹配命令：`!<keyword>`
关键词匹配命令：`【Ctrl】+【R】<keyword>`
移动光标：行首尾`【Ctrl】+【A|E】`  词首尾`【Ctrl】+【←|→】`
清空：`【Ctrl】+【L】` `clear`

打印工作目录：`pwd`
当前目录：`cd .`
切换上级目录：`cd ..`
切换上上级目录：`cd ../..`
切换home目录：`cd ~`  `cd`
切换指定目录：`cd <directory path>`

复制文件夹：`cp -r <cp path> <dir path>`
复制文件：`cp <cp path> <dir path>`
移动文件或文件夹：`mv <cp path> <dir path>`
删除文件夹：`rm -r`
强制删除文件夹：`rm -rf` 管理员root使用

创建多级：`mkdir -p <directory1 path>/<directory2 path>/...`
创建文件夹：`mkdir <file path>` mkdir不能创建文件
创建文件： `touch <file path>` touch不能创建文件夹
输出指定内容：`echo`
执行指定命令：```echo `cmd` ```
将内容覆盖到文件中：`>`
将内容追加到文件中：`>>`

列出隐藏选项 平铺：`ls -a <file path>`
列出当前目录 列表：`ls -l <file path>`
列出文件大小：`ls -h <file path>`  `kb、mb、gb`
列出home目录：`ls`
以列表展示根目录的全部内容：`ls -la /`
以列表展示根目录的文件大小：`ls -lh /`

按名准确查找文件：`find <start path> -name "filename"`
按大小查找文件：`find <start path> -size [+|-]<number>[k|M|G]`
查找小于 10KB 的文件：`find / -size -10k`
查找大于 100MB 的文件：`find / -size +100M`
查找大于 1GB 的文件：`find / -size +1G`
查找命令程序：`which <cmd>`

管道符| 将左命令输出作为右命令输入：`cmd1 | cmd2`  `可嵌套`
过滤文件内容并显示行号：`grep -n "keyword" <file path>`
统计文件行数：`wc -l <file path>`
统计文件单词数：`wc -w <file path>`
统计文件bytes数：`wc -c <file path>`
统计文件字符数：`wc -m <file path>`
查看文件内容 单页：`cat <file path>`
查看文件内容 多页：`more <file path>`  `【space】翻页，【Q】退出`
查看文件尾部10行内容：`tail <file path>`
持续查看文件尾部内容：`tail -f <file path>`
查看文件几行尾部内容：`tail -n <number> <file path>`
###### 04 vim
1开头：`1*`
1结尾：`*1`
包含1：`*1*`

设置行号：`:set nu`  粘贴模式`:set paste`
移动光标：行首`0`  行尾`$`  首行`gg`  尾行`G`
复制行：`<number>yy`  粘贴`p`
删除行：`<number>dd`  至行首`d0`  至行尾`d$`  至首行`dgg`  至尾行`dG`
撤销：`u`  反撤销`【Ctrl】+【R】`
输入：当前`i`  当后：`a`  行首`I`  行尾`A`  上行`O`  下行`o`
搜索：`/`  下个`n`
保存退出：`:wq`  保存`:w`  退出`:q`  强制退`:q!`
###### 05 yum apt 
安装包
windows：`.exe`
macOS：`.pkg`
CentOS：`.rpm`  `yum`
Ubuntu：`.deb`  `apt`

CentOS安装yum
搜索程序：`yum -y serch <program>`  `yum serch wget`
安装程序：`yum -y install wget`
卸载程序：`yum -y remove wget`

Ubuntu安装apt
搜索程序：`apt -y serch <program>`
安装程序：`apt -y install wget`
卸载程序：`apt -y remove wget`
###### 06 systemctl 
`systemctl status <service>`  查看状态
`systemctl start <service>`  启动服务
`systemctl stop <service>`  关闭服务
`systemctl enable <service>`  开机自启
`systemctl disable <service>`  手动启动

内置服务：
`NetworkManeger`  主网络服务
`network`  副网络服务
`firewalld`  防火墙服务
`sshd`  ssh服务

第三方服务：
时间同步软件：`yum install ntp`  `httpd`
查看软件状态：`systemctl status ntpd`
安装的软件一般自动集成到systemctl中，否则需要手动配置
###### 07 日期和时区 
**`date -d "+|-<time>" "+<string>"`**
`date` `2024年 7月 28日 星期日 12:27:45 UTC`
`date -d "-3 month" "+%Y-%m-%d %H:%M:%S"`  `前三月 2024-4-28 12:27:45`

time
`year`  年
`month`  月
`day`  日
`hour`  时
`minute`  分
`second`  秒

string
`%Y`  年 `%y` 后两位`00~99`
`%M`  月 `01~12`
`%d`  日 `01~31`
`%H`  时 `00~23`
`%M`  分 `00~59`
`%S`  秒 `00~60` `%s` 时间戳`form 1970/1/1 00：00：00 UTC to now`

**修改时区**
系统默认时区：`UTC`  `2024年 7月 28日 星期日 12:27:45 UTC`
中国东八区：`CTS` `Fri Oct 21 15:49:02 CST`
```shell
su - root <password>
rm -rf /etc/localtime
ln -s /user/share/zoneinfo/Asia/Shanghai /etc/localtime
date
```
`ln -s <origin path> <dir path>`  创建软连接
**ntp时间校准程序**
```shell
yum install ntp
systemctl start ntpd
systemctl status ntpd
systemctl enable ntpd
```
手动校准
`ntpdate -u ntp.aliyun.com`
###### 08 域名解析 
访问域名：www.baidu.com
Windows检查本机：`C:\Windows\System32\drivers\etc\hosts`
Linux检查本机：`/etc/hosts`
检查公开的DNS服务器：`114.114.114.114` `8.8.8.8`

在Windows中配置Linux的IP与主机名映射：
```
以管理员身份运行 记事本
打开文件 `C:\Windows\System32\drivers\etc\hosts`
编辑记事本 `IP地址 主机名`
保存退出
可用主机名访问到Linux的IP地址
```
###### 09 配置固定IP地址 
虚拟机的Linux操作系统通过DHCP服务获取IP地址，
DHCP动态获取IP地址，每重启一次就获取一次，IP地址频繁变更。

Windows 在VMware中配置固定IP
```
【编辑】【虚拟网络编辑器】【VMnet8】
【子网IP：192.168.88.0】【子网掩码：255.255.255.0】
【NAT设置】【网关：192.168.88.2】
```

```
vim /etc/sysconfig/network-scripts/ifcfg-ens33 打开网卡配置文件
BOOTPROTO=dhcp → static 修改
IPADDR="192.168.88.130" IP地址
NETMASK="255.255.255.0" 子网掩码固定
GAMEWAY="192.168.88.2" 网关和VMware虚拟网络编辑器中设置一致
DNS1="192.168.88.2" DNS1设置为网关
:wq 保存退出

systemctl restart network  重启网卡
ipconfig  查看固定后的IP地址 192.168.88.130
```
###### 10 网络传输 
检查网络是否连通 ping
`ping -c <num> <ip|hostname>`
`ping baidu.com`
`ping -c 110.242.68.66`   检查3次此IP地址

文件下载 wget
`wget -b <url>` 后台下载保存日志到wget-log文件中

发送http请求 curl
`curl -O <url>` -O存在为下载文件，不存在为发起请求
`curl cip.cc` 向cip.cc发起请求，公开网站，获取主机公网IP
`curl python.itheima.com` 向官网发起请求，获取网页
###### 11 端口 
物理端口：接口，USB接口，RJ45网口，HDM端口
虚拟端口：IP地址用于唯一标识计算机，虚拟端口用于不同计算机之间通信

Linux支持6万多个端口65535个，分3类
公认端口：1~1023 系统内置，知名程序，SSH用22端口，HTTPS用443端口
注册端口：1024~49151 任意使用，绑定程序、服务
动态端口：49152~65535 临时使用，程序访问外网链接

查看端口占用情况 `nmap <IP>`
```shell
yum -y istall namp  安装nmap
nmap 127.0.0.1  查看本机可以公开访问的端口
```

查看指定端口/进程占用情况 `netstat -anp|grep <端口号>`
```shell
yum -y istall net-tools 安装netstat
netstat -anp 查看所有
netstat -anp|grep 6000 管道符过滤
netstat -anp|grep 12345
```
###### 12 进程 
显示进程：`ps -ef`  `ps -ef | grep <keyword>`
关闭进程：`kill -9 <PID>`  强制
```shell
UID 用户ID
PID 进程ID
PPID 父进程ID
C CPU占用率 %
STIME 启动时间
TTY 终端启动序号/??系统内置启动
TIME 累计使用CPU时间
CMD 启动命令/路径
```

查看磁盘占用：`df -h`
查看磁盘信息：`iostat -x <refresh duration> <refresh frequency>`
```shell
rrqm/s 每秒这个设备的写入请求有多少被merge了
wrqm/s 每秒读取的扇区数 sectors
rsec/s 每秒写入的扇区数
wsec/ 每秒发送到设备的读取请求数 
rKB/s 读取
wKB/s 写入
avgrq-sz 平均请求队列的长度 长度越短越好
avgqu-sz 每一个IO请求处理的平均时间
await 每个IO请求的处理的平均时间
svctm 表示平均每次设备IO操作的服务时间
%util 磁盘利用率
```
网络统计信息：`sar -n DEV <refresh duration> <refresh frequency>`
```shell
IFACE 本地网卡接口的名称
rxpck/s 每秒钟接收的数据包
txpck/s 每秒钟发送的数据包
rxKB/s 每秒钟接受的数据包大小 KB
rxcmp/s 每秒钟发送的数据包大小 KB
txcmp/s 每秒钟发送的压缩包
rxmcst/s 每秒钟接收的多播数据包
```

**查看系统资源占用：`top` `【Q】退出`** 
```shell
top - 14:39:58 up 6 min, 2users,load average: 0.06,0.07,0.13
Task: 175 total, 1 running, 174 sleeping, 0stopped, 0 zombie
%Cpu(s): 0.3 us, 1.4 sy, 0.0 ni, 98.3 id, 0.0 wa, 0.0 hi, 0.0 si, 0.0 st
KiB Mem : 995892 total, 187672 free, 394912 used, 413308 buff/cache
KiB Swap : 2098172 total, 2098172 free, 0 used. 391852 avail Mem
```
```shell
top - 14:39:58 up 6 min, 2users,load average: 0.06,0.07,0.13
```
`top` 命令名称
`14:39:58` 当前系统时间
`up 6 min` 启动了6分钟
`2users` 2个用户登录
`load average` 1、1、15分钟平均负载

```shell
Task: 175 total, 1 running, 174 sleeping, 0stopped, 0 zombie
```
`Task: 175 total` 175个进程
`1 running` 1个进程在运行
`174 sleeping` 174个睡眠进程
`0stopped` 0个停止进程
`0 zombie` 0个僵尸进程

```shell
%Cpu(s): 0.3 us, 1.4 sy, 0.0 ni, 98.3 id, 0.0 wa, 0.0 hi, 0.0 si,0.0 st
```
`%Cpu(s):` CPU使用率
`0.3 us` 用户CPU使用率
`1.4 sy` 系统CPU使用率
`0.0 ni` 高优先级进程占用CPU时间百分比
`98.3 id` 空闲CPU率
`0.0 wa` IO等待CPU占用率
`0.0 hi` CPU硬件中断率
`0.0 si` 软件中断率
` 0.0 st` 强制等待占用CPU率

```shell
KiB Mem : 995892 total, 187672 free, 394912 used, 413308 buff/cache
```
`KiB Mem :` 物理内存
`995892 total` 总量
`187672 free` 空闲
`394912 used` 使用
`413308 buff/cache` buff和cache占用
```shell
KiB Swap : 2098172 total, 2098172 free, 0 used. 391852 avail Mem
```
`KiB Swap :` 虚拟内存
`2098172 total` 总量
`2098172 free,` 空闲
`0 used.` 使用
`391852 avail Mem` 可用

```shell
PID 进程id
USER 进程所属用户
PR 进程优先级，越小越高
NI 负值表示高优先级，正表示降低优先级
VIRT 进程使用虚拟内存 KB
RES 进程使用物理内存 KB
SHR 进程使用共享内存 KB
S 进程状态 （S休眠 R运行 Z僵尸 N负数优先级 I空闲）
%CPU 进程CPU占用率
%MEM 进程内存占用率
TIME+ 进程使用CPU时间总计 单位10ms
COMMAND 进程命令或程序文件路径
```
```shell
top命令
-p 显示某ID进程信息 `top -p <PID>`
-d 刷新间隔默认5s `top -d <refresh duration>`
-c 详细进程命令或程序文件路径 `top -c <cmd>`
-n 指定刷新次数 `top -n <refresh frequency>`
-b 保存历史刷新记录 `top -b -n 3 > /tmp/top.tmp`
-i 隐藏闲置idel、无用zombie进程
-u 查找特定用户启动的进程
```

```shell
top命令
h 帮助
C 详略进程命令或程序文件路径
f 选择展示新列信息
q 退出
M 按照%MEM排序
P 按照CPU排序
T 按照TIME+排序
E 切换单位
e 切换单位
l 显示隐藏top
i 显示隐藏无用进程
t 切换%CPU信息
m 切换MiB信息
```
###### 13 环境变量 
查看当前系统中的环境变量：`env` `env | grep PATH`
取出环境变量的值：`echo $PATH` `echo $PWD` `echo ${PWD}<string>`
设置临时环境变量：`export MYNAME=<string>`
设置永久环境变量：
```shell
当前用户
vi ~/.bashrc 
export MYNAME=<string> 添加
:wq 保存退出
source .bashrc 生效

所有用户
vi /etc/profile 
export MYNAME=<string> 添加
:wq 保存退出
source /etc/profile 生效
```
自定义环境变量：
```shell
mkdir myenv 创建文件夹，我的环境变量
cd myenv
vim mkhhh 创建并编辑文件mkhhh
echo "hhh"
:wq 
ls -l 查看详细权限信息
chmod 755 mkhhh 编辑权限信息
ls -l 查看详细权限信息 有x权限 可执行
./mkhhh 执行文件，输出hhh

vim /etc/profile 设置永久环境变量
export PATH=$PATH:/root/myenv 创建环境变量，在原有的PATH上追加了“:/root/myenv”
:wq
source /etc/profile 生效

echo $PATH 查看编辑后的环境变量
mkhhh 执行，任意目录、用户均可
```
###### 14 finalshell上传下载 
安装程序：`yum -y install lrzsz`
从finallshell下载到Windows：`sz <file>`
从Windows上传到finallshell：`rz`  建议拖拽上传

Linux压缩格式：`.tar` `.gz`
```shell
tar
-z gzip模式，否则tarball模式
-c 创建压缩文件
-v 查看压缩进度
-f 目标文件
-x 解压
-C 解压目的地

压缩文件
`tar -cvf <filename.tar> <file1><file2>...`  tar格式
`tar -zcvf <filename.tar.gz> <file1><file2>...`  gzip格式

解压文件
`tar -xvf <filename.tar> -C <dir path>` tar格式
`tar -zxvf <filename.tar.gz> -C <dir path>` gzip格式
```

```shell
zip
压缩文件
`zip -r <filename.zip> <file1><file2>... `
解压文件
`unzip <file.zip> -d <dir path>`
```
#### 20240728 康文昌 编程入门：https://www.bilibili.com/video/BV1eF411x7g5/
###### 02 VScode
插件
`live preview` `live server` 内置预览
`wisen translator` 悬浮翻译
`Search/Translate Hero` 在线搜索

首选项
`AutoSave`onFocusChange，自动保存
`Format On Save` 勾选，保存后自动格式化
`Format On Paste` 勾选，粘贴时自动格式化
`Linked Editing` 勾选，自动补全html双标签

快捷键
`【Ctrl】+【D】` 多选单词
`【Alt】+【左击】` 添加光标
`【Ctrl】+【K】+【V】`侧边预览
`【Ctrl】+【A】，【Ctrl】+【K】+【F】`自动对齐
`【Alt】+【Shift】+【↑|↓】`快速复制
`【Ctrl】+【Enter】`在下方输入
`【Ctrl】+【Shift】+【Enter】`在上方输入
###### 03 html
`<!DOCTYPE html>`  文档类型
`<html lang="zh-CN">`  中文
`<meta charset="UTF-8">` 元数据，解析文字
`<meta name="viewport" content="width=device-width, initial-scale=1.0">` 适配手机屏
`<title>Document</title>` 网站标题
`<meta name='description' content='Put your content here.'>` 网页简介

布局小技巧：
```html
*{
    border: 1px solid black;
}
```


