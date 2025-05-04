## F 笔记  
### Project_B 本科毕业设计-毕设参考  
#### 20241225 黑马10小时搞定毕业设计 https://www.bilibili.com/video/BV15BqAYNErA  
##### (0)通义灵码  
【AI】请阅读以下开题报告模板资料，然后生成《》的开题报告  
【AI】通义灵码 @workspace本地工程问答  
【AI】通义灵码 请使用Mermaid语法绘制出《》的关联图 ER图 业务流程图 时序图  
【AI】我现在在写毕业设计的开题报告，我的题目是：基于富文本音视频集合的文化类博客系统，接下来请你帮我写一些东西  
【AI】请你帮我写一下研究背景，我只要段落，不要分点，字数500字以上，写的内容就是为啥要选这个题目？  
【AI】请你帮我写一下研究意义，我只要段落，不要分点，字数500字以上，写的内容就是选这个题目的作用是什么？可以从理论意义和现实意义这两  个方向去写
【AI】请你帮我写一下研究目的，我只要段落，不要分点，字数500字以上，写的内容就是我准备做出来一个啥样的东西，对人群有什么帮助  
【AI】请你帮我生成以下研究现状，一段写中国的，一段写国外的，只要段落，不要分点，字数800字以上，要有数据支撑  
【AI】喵喵喵等人（2025）在其研究中指出，对我的设计提供了参考，特别是在方面有很大的研究意义  
【AI】喵喵喵等人（2025）在其研究中指出，对我系统设计，性能优化方面提供了良好的建议  
##### (1)文件管理  
文件管理：项目截图、业务流程图、项目源码、SQL脚本、前端环境、后端环境、数据库环境、README文档  
运行环境：前端Node、Nginx  
运行环境：后端JDK11、MySQL8.0、Redis5、Maven3.6.x  
开发软件：后端IDEA、前端VSCode  
##### (2)项目导入  
导入项目：导入pom.xml   
初始配置：application.yml(port spring mysql redis mybatis修改为自己的url、用户、密码)  
初始配置：检查Maven(Settings) 检查JDK(ProjectStructure SDK：选择JDK11)  
初始配置：侧边栏Maven LifeCycle(清理clean 安装install 跳过单元测试Toggle'SkipTests'Mode)  
初始配置：侧边栏Database 数据源设置(Host、Port、User、Password、Database)、下载驱动(Download missing driver files)、测试连  接(Test Connection) 右键数据库(选择SQLScript RunSQLScript)
环境启动：启动nginx.exe 默认端口80  
环境启动：启动redis 默认端口6379  
项目启动：Application.java 端口8080  
##### 安装：JDK11  
下载资源：Oracle官网：https://www.oracle.com/cn/  
选择文件：选择JDK.exe安装包  
安装向导：默认下一步  
环境变量：新建变量JAVA_HOME 在Path中添加%JAVA_HOME%\bin  
安装验证：cmd命令`java -version`  
##### 安装：IDEA  
下载资源：IDEA官网  
选择文件：选择IDEA.exe安装包  
安装向导：勾选添加“bin”文件夹到PATH 创建关联.java  
环境变量：已配置  
初始配置：通义灵码插件 @workspace本地工程问答  
初始配置：配置JDK(ProjectStructure SDK：选择JDK11)  
初始配置：配置Maven(MavenHomePath安装目录、UserSettingsFile配置文件、LocalRepository仓库目录默认即可)  
初始配置：配置Maven Runner(JRE：选择JDK11 Use JAVA_HOME)  
初始配置：配置JavaCompiler(Project bytecode version：选择JDK11)  
初始配置：配置Inspections(Security：取消勾选后两处dependency)  
初始配置：配置Configuration(package.json：在vue安装路径下找 `npm run serve`启动vue)  
初始配置：侧边栏Database 数据源设置(Host、Port、User、Password、Database)、下载驱动(Download missing driver files)、测试连  接(Test Connection)
##### 安装：MySQL8.0  
下载资源：MySQL官网：https://www.mysql.com/cn/  
选择文件：选择MySQL.msi安装包(图形化界面)  
安装向导：在安装向导中设置管理员密码  
环境变量：在Path中添加MySQL\bin目录  
安装验证：cmd命令`mysql -uroot -p`  
##### 安装：Redis5  
下载资源：Redis官网：https://www.redis.net.cn/  
选择文件：选择Redis.zip压缩包  
安装向导：文件解压  
环境变量：无需配置  
安装验证：启动redis.cmd`redis-server.exe redis.windows.conf` 验证连接`ping`返回`PONG`  
文件介绍：配置文件redis.windows.conf 启动服务器redis-server.exe 启动客户端redis-cli.exe   
##### 安装：Maven3.6.x 项目构建和管理工具  
下载资源：Maven官网：https://maven.apache.org/  
选择文件：选择Maven.zip压缩包  
安装向导：文件解压  
环境变量：新建变量MAVEN_HOME 在Path中添加%MAVEN_HOME%\bin  
安装验证：cmd命令`mvn -v`或`mvn --version`  
初始配置：编辑配置文件Maven\conf\setting.xml可配置本地仓库、镜像仓库等  
##### 安装：nginx  
下载资源：nginx官网：https://nginx.org/en/  
选择文件：选择nginx.zip压缩包  
安装向导：文件解压  
环境变量：无需配置  
安装验证：双击启动nginx.exe 默认端口80  
文件介绍：nginx服务器有反向代理配置nginx.conf(监听80 反向代理8080)  #### 20241228 武哥毕设 https://www.javaxmsz.cn/
1.项目使用的技术栈
后端：Java、Springboot、MyBatis
前端：Vue、Element-UI、HTML、CSS、Javascript
数据库：MySQL
2.电脑里需要准备的环境
后端运行环境：JDK 8
前端运行环境：nodejs
代码编写软件：IDEA
数据库：MySQL 5.7 或者 8
数据库可视化：navicat
文档编写软件：typora、word、WPS（非必要）
接口调试工具：postman（非必要）
3.该系列课程资料汇总
1、重磅推出！学完各种系统通吃！可用于Springboot+Vue的管理系统、论坛、博客、预定、预约等所有毕业设计项目场景
2、从0开始手把手带你做Vue框架的快速搭建以及项目工程的讲解
3、从0开始手把手教你使用Vue快速搭建一个管理系统页面框架和数据渲染
4、从0快速搭建Springboot项目框架以及Springboot整合MyBatis实战
5、手把手教Springboot+Vue实现增删改查、分页查询、模糊查询功能
6、手把手教Springboot+Vue实现登录注册
7、手把手教Springboot+Vue+JWT实现用户登录鉴权
8、手把手教Springboot+Vue实现文件上传和下载
9、Springboot+Vue快速实现批量删除功能
10、Springboot+Vue实现批量导入excel、批量导出excel
11、pringboot+Vue实现模块之间的关联功能
12、Springboot+Vue实现全网最简单实用的角色权限控制，全网最简单！
13、+Vue实现请假申请、请假审核功能
14、Springboot+Vue实现酒店预订、学生选课、教室预订、图书借阅、场地预约、房屋租赁等功能
15、Springboot+Vue+AOP实现登录、增删改查操作日志管理
16、Springboot+Vue实现系统公告（通知）增删改查、首页系统公告（通知）展示
17、Springboot+Vue实现登录注册图形验证码功能
18、Springboot+Vue集成echarts（饼图、柱状图、折线图）实现数据统计
19、Springboot+Vue集成富文本编辑器实现发帖、发博客等功能
#### 20241227 武哥毕设 1.安装 vue+element
01可用于Springboot+Vue的管理系统、论坛、博客、预定、预约等所有毕业设计项目场景
02使用Element-UI开发前台页面
##### (1)包层次
##### (2)预设模板
##### (3)清空页面
##### 前端：APP.vue：空模板
##### 前端：HomeView.vue：空模板
##### 前端：global.css
##### 前端：main.js：
##### 安装：【Vue】
下载资源：Vue官网：https://cn.vuejs.org/
环境验证：`node -v` `npm -v` （npm 是 Node.js 包管理工具）
安装向导：目标路径下打开cmd`cd <your-project-name>`
安装向导：淘宝镜像(过期)`npm config set registry https://registry.npm.taobao.org`
安装向导：修改镜像`npm config set registry https://registry.npmmirror.com`
安装向导：检查配置`npm config list`
安装向导：安装命令`npm install -g @vue/cli`
安装向导：安装验证`vue --version`
创建工程：`vue create vue`
创建工程：Vue CLI v5.0.8
创建工程：? Please pick a preset: Manually select features
创建工程：? Check the features needed for your project: Babel, Router
创建工程：? Choose a version of Vue.js that you want to start the project with 2.x
创建工程：? Use history mode for router? (Requires proper server setup for index fallback in production) Yes
创建工程：? Where do you prefer placing config for Babel, ESLint, etc.? In package.json
创建工程：? Save this as a preset for future projects? Yes
创建工程：? Save preset as: default
启动工程：`cd vue`(进入文件夹)
启动工程：`npm run serve`
##### 安装：【Element】
下载资源：Element：https://element.eleme.cn/
环境验证：`vue --version`
安装向导：安装命令`npm i element-ui -S`
#### 20241229 武哥毕设 2.[前端页面]
03使用Vue搭建管理系统页面框架和数据渲染
##### (1)前端页面
##### (2)前端页面
##### (3)配置文件
##### 前端：APP.vue：
##### 前端：AdminView.vue：
##### 前端：index.js：
##### 前端：main.js：
#### 20241230 武哥毕设 3.[后端Springboot+Mybatis]
04快速搭建Springboot项目框架以及Springboot整合MyBatis实战
##### (1)IDEA新建SpringBoot项目
##### (2)包结构
##### (3)项目结构
##### (4)数据库配置
##### 后端：UserController.java
##### 后端：UserService.java
##### 后端：UserDao.java(Interface)(Interface)
##### 后端：UserMapper.xml
##### 后端：User.java
##### 后端：pom.xml
##### 后端：appplication.yml
##### 数据库：user.sql
#### 20241230 武哥毕设 4.[增删改查]
05手把手教Springboot+Vue实现增删改查、分页查询、模糊查询功能
##### (1)统一封装
##### (2)全部查询
##### (3)条件查询
##### (4)分页查询
##### (5)增改
##### (6)删除
##### 前端：request.js
##### 前端：AdminView.vue script
##### 后端：Result.java
##### 后端：Params.java
##### 后端：AdminCtroller.java
##### 后端：AdminService.java
##### 后端：AdminDao.java(Interface)
##### 后端：AdminMapper.xml
##### 后端：Admin.java
##### 后端：GlobalExceptionHandler.java
##### 后端：CustomException.java
##### 后端：pom.xml
##### 后端：application.yml
#### 20250103 武哥毕设 5.[登录注册]
06手把手教Springboot+Vue实现登录注册
##### (1)登录
##### (2)注册
##### 前端：App.vue
##### 前端：LoginView.vue
##### 前端：RegisterView.vue
##### 前端：index.js 分级路由
##### 后端：AdminCtroller.java
##### 后端：AdminService.java
##### 后端：AdminDao.java(Interface)(Interface)
#### 20250109 武哥毕设 6.[登录鉴权Jwt]
07手把手教Springboot+Vue+JWT实现用户登录鉴权
##### (1)登录退出
##### (2)前端鉴权(不安全：前端数据可以人为篡改)
##### (3)后端鉴权(Jwt，token生成)
##### (4)后端鉴权(Jwt，token验证)
##### (5)后端鉴权(解决跨域问题)
##### 前端：LoginView.vue
##### 前端：LayoutView.vue
##### 前端：index.js
##### 前端：request.js
##### 后端：pom.xml
##### 后端：CorsConfig.java
##### 后端：WebConfig.java
##### 后端：AdminService.java
##### 后端：JwtTokenUtils.java
##### 后端：JwtInterceptor.java
#### 20250111 武哥毕设 7.*文件上传下载*
08手把手教Springboot+Vue实现文件上传和下载
##### (1)图书管理模块(后端框架)
##### (2)图书管理增删改查
##### (3)文件上传下载
##### (4)图片文件预览下载
##### 前端：Layout.vue
##### 前端：BookView.vue
##### 前端：index.js
##### 后端：BookController.java
##### 后端：FileController.java
##### 后端：BookService.java
##### 后端：BookDao.java(Interface)
##### 后端：BookMapper.xml
##### 后端：Params.java
##### 后端：Book.java
##### 后端：WebConfig.java
##### 数据库：book.sql
#### 20250131 武哥毕设 8.*批量删除*
09Springboot+Vue快速实现批量删除功能
##### (1)图书分类模块(后端框架)
##### (2)图书分类增删改查
##### 前端：TypeView.vue
##### 前端：index.js
##### 后端：TypeController.java
##### 后端：TypeService.java
##### 后端：TypeDao.java(Interface)
##### 后端：TypeMapper.xml
##### 后端：Type.java
##### 数据库：type.sql
#### 20250131 武哥毕设 9.*批量导入导出*
10Springboot+Vue实现批量导入excel、批量导出excel
##### (1)批量导出
##### (2)批量导入
##### 前端：TypeView.vue
##### 后端：pom.xml
##### 后端：TypeController.java
##### 后端：TypeService.java
##### 后端：Type.java
##### 后端：WebConfig.java
#### 20250201 武哥毕设 10.*模块关联*
11Springboot+Vue实现模块之间的关联功能
##### (1)模块关联(显示typeId)
##### (2)模块关联(显示typeName) 通过sql语句(left join查询)
##### (3)模块关联(显示typeName) 通过java逻辑(BookService查询)
##### 前端：BookView.vue
##### 后端：TypeController.java
##### 后端：BookService.java
##### 后端：BookMapper.xml
##### 后端：Book.java
##### 数据库：新建查询.sql
#### 20250201 武哥毕设 11.[权限控制]
12Springboot+Vue实现全网最简单实用的角色权限控制
##### (1)添加不同角色
##### (2)登录权限控制
##### (3)注册默认权限
##### 前端：Layout.vue
##### 前端：LoginView.vue
##### 前端：RegisterView.vue
##### 前端：AdminView.vue
##### 前端：index.js
##### 前端：TypeView.vue
##### 前端：BookView.vue
##### 后端：Admin.java
##### 后端：AdminMapper.xml
##### 数据库：admin.sql
#### 20250202 武哥毕设 12.*请假审核*
13Springboot+Vue实现请假申请、请假审核功能
##### (1)请假申请模块
##### (2)模块关联(显示请假用户姓名) 通过java逻辑(AuditService查询)
##### (3)模块关联(显示请假用户姓名) 通过sql语句(left join查询)
##### (4)审核功能
##### (5)用户区分
##### 前端：Layout.vue
##### 前端：index.js
##### 前端：AuditView.vue
##### 后端：AuditController.java
##### 后端：AuditService.java
##### 后端：AuditDao.java(Interface)
##### 后端：AuditMapper.xml
##### 后端：Audit.java
##### 后端：Params.java
##### 数据库：audit.sql
#### 20250204 武哥毕设 13.*预约预定*
14Springboot+Vue实现酒店预订、学生选课、教室预订、图书借阅、场地预约、房屋租赁等功能
##### (1)酒店信息模块
##### (2)预定信息模块
##### (3)预定完善
##### 前端：Layout.vue
##### 前端：index.js
##### 前端：HotelView.vue
##### 前端：ReserveView.vue
##### 后端：HotelController.java
##### 后端：HotelService.java
##### 后端：HotelDao.java(Interface)
##### 后端：HotelMapper.xml
##### 后端：Hotel.java
##### 后端：ReserveController.java
##### 后端：ReserveService.java
##### 后端：ReservelDao.java(Interface)
##### 后端：ReserveMapper.xml
##### 后端：Reserve.java
##### 数据库：hotel.sql
##### 数据库：reserve.sql
#### 20250208 武哥毕设 14.[日志管理]
15Springboot+Vue+AOP实现登录、增删改查操作日志管理
##### (1)日志管理模块
##### (2)日志管理实现(面向切面编程AOP)
##### (3)日志管理切面注解
##### 前端：Layout.vue
##### 前端：index.js
##### 前端：LogView.vue
##### 后端：AdminController.java
##### 后端：BookController.java
##### 后端：Params.java
##### 后端：LogController.java
##### 后端：LogService.java
##### 后端：LogDao.java(Interface)
##### 后端：LogMapper.xml
##### 后端：Log.java
##### 后端：AutoLog.java(Annotation)
##### 后端：LogAspect.java
##### 后端：pom.xml
##### 数据库：log.sql
#### 20250209 武哥毕设 15.*系统公告*
16Springboot+Vue实现系统公告（通知）增删改查、首页系统公告（通知）展示
##### (1)系统公告模块
##### 前端：Layout.vue
##### 前端：index.js
##### 前端：HomeView.vue
##### 前端：NoticeView.vue
##### 后端：NoticeController.java
##### 后端：NoticeService.java
##### 后端：NoticeMapper.xml
##### 后端：NoticeDao.java(Interface)
##### 后端：Notice.java
##### 数据库：notice.sql
#### 20250209 武哥毕设 16.[登录验证码]
17Springboot+Vue实现登录注册图形验证码功能
##### (1)图形验证码
##### (2)算数验证码
##### (2)登录背景图
##### 前端：LoginView.vue
##### 后端：AdminController.java
##### 后端：Admin.java
##### 后端：CaptureController.java
##### 后端：CaptureConfig.java
##### 后端：WebConfig.java
##### 后端：pom.xml
#### 20250211 武哥毕设 17.*统计图表echarts*
echarts官网：https://echarts.apache.org/examples/zh/index.html
18Springboot+Vue集成echarts实现数据统计
##### (1)饼图模块
##### (2)柱状、折线图模块
##### 前端：HomeView.vue
##### 后端：BookController.java
##### 后端：BookService.java
##### 后端：BookDao.java
##### 安装：【echarts】
#### 20250212 武哥毕设 18.*富文本编辑wangeditor*
wangeditor官网：https://www.wangeditor.com/v4
19Springboot+Vue集成富文本编辑器实现发帖、发博客等功能
##### (1)富文本编辑
##### 前端：BookView.vue
##### 后端：FileController.java
##### 后端：Book.java
##### 数据库：book.sql
##### 安装：【wangeditor】

#### 20241228 青戈毕设 (资料汇总)
Java项目网：https://javaxm.cn/
项目实战网：https://www.javaxmsz.cn/home
青哥：
https://www.javaxmsz.cn/webView/note?relId=60&type=COURSE_NOTE&contentType=ARTICLE&uuid=2c24fbce0fa349e09e902f6e865bac28
武哥：
https://www.javaxmsz.cn/webView/note?relId=61&type=COURSE_NOTE&contentType=ARTICLE&uuid=a8f929f8a3764775885a25db2de1b101
##### 【技术栈】
前端：Html、Css、JavaScript、Vue、Element-UI
后端：Java、SpringBoot、MyBatis、MyBatis-Plus
数据库：Mysql
服务器：腾讯云Linux（CentOS 7.9）
微信小程序：uniapp
##### 【课程所需软件】
（必需）Nodejs v16（Vue运行环境，包含npm包管理工具）
（必需）Jdk1.8（Java运行环境）
（必需）IDEA（编写Java和Vue项目通用软件）
（必需）Mysql5.7（数据库）
（必需）Navicat（数据库可视化工具）
（必需）Git（代码管理工具）https://gitee.com/
（必需）Redis（缓存数据库）
（必需）RDM（Redis可视化工具）
（非必需）natapp（内网穿透工具，学到支付宝沙箱的时候会需要）
（非必需）XShell & XFtp（服务器部署工具）
（非必需）Apache Maven软件（下载SpringBoot依赖包需要）
（非必需）Postman接口测试工具下载（接口测试的时候需要）
##### 【课程大纲】
1、网页布局技巧
2、JavaScript入门
3、Vue脚手架搭建
4、Git速成，推送代码到云端
5、网页布局神器ElementUI速成
6、Vue管理系统速成
7、SpringBoot速成
8、Http扫盲，让小白也能听懂
9、SpringBoot集成Mybatis实现增删改查
10、Vue封装前后端数据交互工具
11、Vue登录（含验证码）、注册页面开发
12、SpringBoot集成JWT token实现权限验证
13、SpringBoot+Vue实现单文件、多文件上传和下载
14、多角色登录（Vue-Router路由守卫）
15、Vue个人信息修改、修改密码、重置密码
16、SpringBoot+Vue管理系统实现增删改查
17、SpringBoot+Vue实现数据的批量导入和导出
18、SpringBoot+Vue项目部署上线
19、SpringBoot+Vue集成富文本编辑器
20、SpringBoot+Vue集成系统公告
21、SpringBoot+Vue集成AOP系统日志
22、SpringBoot+Vue实现Echarts数据报表（柱状图、饼图、折线图）
#### 20250216 青哥毕设 (vue+element安装教程)
