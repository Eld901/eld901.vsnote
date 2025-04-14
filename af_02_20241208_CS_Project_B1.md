## F 笔记
### Project_B 本科毕业设计-毕设参考
#### 20241225 黑马10小时搞定毕业设计 https://www.bilibili.com/video/BV15BqAYNErA
##### (0)通义灵码
【AI】请阅读以下开题报告模板资料，然后生成《》的开题报告
【AI】通义灵码 @workspace本地工程问答
【AI】通义灵码 请使用Mermaid语法绘制出《》的关联图 ER图 业务流程图 时序图
【AI】我现在在写毕业设计的开题报告，我的题目是：基于富文本音视频集合的文化类博客系统，接下来请你帮我写一些东西
【AI】请你帮我写一下研究背景，我只要段落，不要分点，字数500字以上，写的内容就是为啥要选这个题目？
【AI】请你帮我写一下研究意义，我只要段落，不要分点，字数500字以上，写的内容就是选这个题目的作用是什么？可以从理论意义和现实意义这两个方向去写
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
初始配置：侧边栏Database 数据源设置(Host、Port、User、Password、Database)、下载驱动(Download missing driver files)、测试连接(Test Connection) 右键数据库(选择SQLScript RunSQLScript)
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
初始配置：侧边栏Database 数据源设置(Host、Port、User、Password、Database)、下载驱动(Download missing driver files)、测试连接(Test Connection)
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
文件介绍：nginx服务器有反向代理配置nginx.conf(监听80 反向代理8080)
#### 20241228 武哥毕设 https://www.javaxmsz.cn/
#### 20241227 武哥毕设 1.安装 vue+element
#### 20241229 武哥毕设 2.前端页面
#### 20241230 武哥毕设 3.后端 Springboot+Mybatis
#### 20241230 武哥毕设 4.增删改查
#### 20250103 武哥毕设 5.登录注册
#### 20250109 武哥毕设 6.登录鉴权 Jwt
#### 20250111 武哥毕设 7.文件上传下载
#### 20250131 武哥毕设 8.批量删除
#### 20250131 武哥毕设 9.批量导入导出
#### 20250201 武哥毕设 10.模块关联
#### 20250201 武哥毕设 11.权限控制
#### 20250202 武哥毕设 12.请假审核
#### 20250204 武哥毕设 13.预约预定
#### 20250208 武哥毕设 14.日志管理
#### 20250209 武哥毕设 15.系统公告
#### 20250209 武哥毕设 16.登录验证码
#### 20250211 武哥毕设 17.统计图表 echarts
#### 20250212 武哥毕设 18.富文本编辑 wangeditor
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
