##### docsify笔记
###### 00 预信息
docsify官网：[docsify官网](https://docsify.js.org/#/zh-cn/)  
bilibili教程：[docsify博客](https://www.bilibili.com/video/BV1kT4y1T7wY/?spm_id_from=333.337.search-card.all.click&)  
docsify演示： [docsify演示](https://thinkaboutai.github.io)  
node官网：[node官网](https://nodejs.org/en/download/)

###### 01 安装和初始化
安装nodejs，npm  
安装docsify：`npm i docsify-cli -g`  
初始化docsify：`docsify init`  
创建文件：`docsify init ./docs`  
本地预览：`docsify serve docs`  
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