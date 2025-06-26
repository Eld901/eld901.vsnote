# a4_04_PRJ_Project_FBD1  
`Created on 20241208 | Updated on 20250526`  
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
文件介绍：nginx服务器有反向代理配置nginx.conf(监听80 反向代理8080)  
#### 20241228 武哥毕设 https://www.javaxmsz.cn/
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
1. vue/vue.config.js：项目配置(可配置端口、跨域等)
2. vue/public/：静态文件(如图片、html)
3. vue/src/：项目源码目录
vue/src/App.vue 前端入口(页面)
vue/src/main.js 全局配置
(1)vue/src/views/视图文件(页面)
  HomeView.vue
  AboutView.vue
(2)vue/src/components/视图组件(页面)
  HelloWorld.vue
(3)vue/src/assets/静态文件(如图片、css)
(4)vue/src/router/路由配置
  index.js
(5)vue/src/utils/请求封装
  request.js
##### (2)预设模板
src.App.vue(页面)
src.views.AboutView.vue：(页面)
src.views.HomeView.vue：(页面)
src.components.HelloWorld.vue：(页面)
##### (3)清空页面
App.vue、HomeView.vue：清空预设模板
新建src.assets.global.css：清空预设样式
src.main.js：引入Css样式、ElementUI
##### 前端：APP.vue：空模板
```js
<template>
  <div id="app">
    <router-view/>
  </div>
</template>
```
##### 前端：HomeView.vue：空模板
```js
<template>
  <div>
  </div>
</template>
<script>
export default {
  name: 'HomeView',
}
</script>
```
##### 前端：global.css
```js
body {
    margin: 0;
    padding: 0;
    overflow: hidden;
}/*把所有的元素变成盒状模型*/
* {/*外边距不会额外占用1px的像素*/
    box-sizing: border-box;
}
```
##### 前端：main.js：
```js
import Vue from 'vue'
import App from './App.vue'
import router from './router'
import '@/assets/global.css'
import ElementUI from 'element-ui';
import 'element-ui/lib/theme-chalk/index.css';
Vue.config.productionTip = false
Vue.use(ElementUI);
new Vue({
  router,
  render: h => h(App)
}).$mount('#app')
```
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
##### (1)前端页面 <script>
`data(){return{定义变量}}`
`create(){页面初始化}`
`method(){监听方法}`
##### (2)前端页面 <template>
AdminView.vue：
重命名src.views.AboutView.vue为AdminView.vue
`<el-input>` 引入输入框组件
`<el-button>` 引入按钮组件
`<el-table>` 引入表格组件(表格假数据)
`<el-pagination>` 引入分页组件
App.vue：
`<el-container>` 引入布局组件
`<el-header>` 引入顶栏组件
`<el-aside>` 引入侧边栏组件
`<el-main>` 引入主区域组件
App.vue(header)：
`<img>` 引入图片组件
`<span>` 引入内联容器组件
App.vue(main)：
`<router-view/>` 渲染当前路由引用页面
App.vue(aside)：
`<el-menu>` 引入侧栏菜单组件
`<style>.el-menu{border-right: none !important;}</style>` 修改侧栏菜单预设样式小瑕疵
`<el-menu :default-active="$route.path" router>` 以动态路由方式作为菜单切换的index
`<el-menu-item index="/home">` index为路由path
##### (3)配置文件
index.js：
引入页面HomeView.vue(配置路由path、name、component)
引入页面AdminView.vue(配置路由path、name、component)
main.js：
`Vue.use(ElementUI, { size: "small" });` 全局配置UI大小
##### 前端：APP.vue：
```js
<template>
  <div id="app">
    <el-container>
      <el-header style="background-color: #4c535a">
        <img src="@/assets/logo.png" alt="" style="width: 40px; position: relative; top: 10px;">
        <span style="font-size: 20px; margin-left: 15px; color: white">手拉手带小白做毕设</span>
      </el-header>
    </el-container>
    <el-container>
      <el-aside style="overflow: hidden; min-height: 100vh; background-color: #545c64; width: 250px">
        <el-menu :default-active="$route.path" router background-color="#545c64" text-color="#fff" active-text-color="#ffd04b">
          <el-menu-item index="/">
            <i class="el-icon-s-home"></i>
            <span slot="title">系统首页</span>
          </el-menu-item>
          <el-submenu index="2">
            <template slot="title">
              <i class="el-icon-location"></i><span>用户管理</span>
            </template>
            <el-menu-item-group>
              <el-menu-item index="/admin">管理员信息</el-menu-item>
              <el-menu-item index="2-2">用户信息</el-menu-item>
            </el-menu-item-group>
          </el-submenu>
          <el-submenu index="3">
            <template slot="title">
              <i class="el-icon-location"></i><span>信息管理</span>
            </template>
            <el-menu-item-group>
              <el-menu-item index="3-1">xxx信息</el-menu-item>
              <el-menu-item index="3-2">yyy信息</el-menu-item>
            </el-menu-item-group>
          </el-submenu>
        </el-menu>
      </el-aside>
      <el-main>
        <router-view/>
      </el-main>
    </el-container>
  </div>
</template>
<style>
.el-menu{
  border-right: none !important;
}
</style>
<script lang="ts">
</script>
```
##### 前端：AdminView.vue：
```js
<template>
  <div>
    <div>
      <el-input style="width: 200px; margin-right: 10px" placeholder="请输入内容"></el-input>
      <el-button type="warning">搜索</el-button>
      <el-button type="primary">新增</el-button>
    </div>
    <div>
      <el-table :data="tableData" style="width: 100%; margin: 15px 0px">
        <el-table-column prop="date" label="日期" width="180"></el-table-column>
        <el-table-column prop="name" label="姓名" width="180"></el-table-column>
        <el-table-column prop="address" label="地址"></el-table-column>
        <el-table-column label="操作">
          <el-button type="primary">编辑</el-button>
          <el-button type="danger">删除</el-button>
        </el-table-column>
      </el-table>
    </div>
    <div class="block">
      <el-pagination
          @size-change="handleSizeChange"
          @current-change="handleCurrentChange"
          :current-page="currentPage4"
          :page-sizes="[10, 20, 30, 40]"
          :page-size="10"
          layout="total, sizes, prev, pager, next, jumper"
          :total="400">
      </el-pagination>
    </div>
  </div>
</template>
<script>
  export default {
    data() {
      return {
        tableData: [{
          date: '2016-05-02',
          name: '王小虎',
          address: '上海市普陀区金沙江路 1518 弄'
        }, {
          date: '2016-05-04',
          name: '王小虎',
          address: '上海市普陀区金沙江路 1517 弄'
        }]
      }
    }
  }
</script>
```
##### 前端：index.js：
```js
import Vue from 'vue'
import VueRouter from 'vue-router'
import HomeView from '../views/HomeView.vue'
Vue.use(VueRouter)
const routes = [
  {
    path: '/',
    name: 'home',
    component: HomeView
  },
  {
    path: '/admin',
    name: 'admin',
    component: () => import('../views/AdminView.vue')
  }]
const router = new VueRouter({
  mode: 'history',
  base: process.env.BASE_URL,
  routes
})
export default router
```
##### 前端：main.js：
```js
import Vue from 'vue'
import App from './App.vue'
import router from './router'
import '@/assets/global.css'
import ElementUI from 'element-ui';
import 'element-ui/lib/theme-chalk/index.css';
Vue.config.productionTip = false
Vue.use(ElementUI, { size: "small" });
new Vue({
  router,
  render: h => h(App)
}).$mount('#app')
```
#### 20241230 武哥毕设 3.[后端Springboot+Mybatis]
04快速搭建Springboot项目框架以及Springboot整合MyBatis实战
##### (1)IDEA新建SpringBoot项目
安装向导：Name：springboot
安装向导：Location：E:\eld901\Idea
安装向导：Language：Java
安装向导：Type：Maven
安装向导：Group：com.example
安装向导：Artifact：springboot(同Name)
安装向导：Packagename：com.example
安装向导：JDK：17
安装向导：Java：17
安装向导：Packaging：Jar
安装向导：Next=>
安装向导：SpringBoot：选择版本
安装向导：Dependencies：选择SpringWeb
安装向导：Create=>Fnish
##### (2)包结构
非必要文件：.mvn、.gitignore、HELP.md、mvnw、mvnw.cmd
初始配置：application.properties后缀改为.yml，配置端口等信息
初始配置：Maven、JDK、数据库、pom.xml等(MVNRepository：https://mvnrepository.com/)
业务逻辑：【controller】=>【service】=>【dao(mapper)】=>【entity】=>【数据库】
src.main.java.SpringbootApplication.java：启动类
src.main.java.com.example.controller：前后端接口，编写各种 xxxController，提供接口给前端调用。
src.main.java.com.example.service：后端业务层，编写一些后端业务逻辑。
src.main.java.com.example.dao(mapper)：后端持久层，继承映射类，操作实体类。
src.main.java.com.example.entity：(User.java)实体类对象，对应数据库表，实体类的属性对应表的字段信息。
src.main.java.com.example.entity：(Params.java)前端数据实体类，接收前端传递给后端的参数
src.main.java.com.example.common：(Result.java)统一封装类，封装后端返回给前端的数据
src.main.java.com.example.common：(JwtTokenUtils.java)Jwt工具类，生成token
src.main.java.com.example.common：(JwtInterceptor.java)自定义Jwt拦截器
src.main.java.com.example.common：(WebConfig.java)拦截器配置，统一前缀/api，统一controller接口前缀
src.main.resources.mapper.UserMapper.xml 映射类
src.main.resources.application.yml 配置项
pom.xml 依赖包
##### (3)项目结构
【Application】启动类(SpringbootApplication.java)：
`@SpringBootApplication`启动入口
`@MapperScan("com.example.dao")`扫描包
【Result】统一封装类(Result.java)
【Params】前端数据实体类(Params.java)
【controller】前后端接口(UserController.java)：
`@CrossOrigin`解决前后端联调时的跨域问题
`@RestController`controller层
`@RequestMapping("/user")`请求方法
`@Resource`引入service层(`private UserService userService;`)
`@GetMapping("/start")`GET请求方法(查询新增修改删除GET POST PUT DELETE) 
【service】后端业务层(UserService.java)：
`@Service`service层
`@Resource`引入dao层(`private UserDao userDao;`)
`return userDao.selectAll();`基于pom.xml依赖tk.mybatis查询数据库
【dao】后端持久层(UserDao.java(Interface)(Interface))：
`extends Mapper<User>`继承mapper，控制entity层
`@Repository`dao层
`@Param("params")`绑定参数
`@Select("select * from user")`基于注解查询数据库
【mapper】后端持久层(UserMapper.xml)：
`<select id="getUser" resultType="com.example.entity.User">`映射dao层，控制entity层
`select * from user`基于mapper.xml查询数据库
【entity】实体类对象(User.java)：
`@Table(name = "user")`对应数据库表名
`@Id`对应数据库主键
`@GeneratedValue(strategy = GenerationType.IDENTITY)`对应数据库自增
`@Column(name = "name")`对应数据库字段名
`@Transient`非数据库字段(DTO)
##### (4)数据库配置
Navicat连接MySQL：
新建连接：连接名：localhost_3306
新建连接：主机：localhost
新建连接：端口：3306
新建连接：用户名：root
新建连接：密码：1234
新建数据库：数据库名：与application.yml配置一致
新建数据库：字符集：utf8mb4
新建数据库：排序规则：utf8mb4_unicode_ci
新建表格：(手动建表)勾选不是null、主键、自增
新建表格：(自动建表)新建查询、运行SQL文件
导出sql：右键表格、转储SQL文件、结构和数据
##### 后端：UserController.java
```java
@RestController
@RequestMapping("/user")
public class UserController {
    @Resource
    private UserService userService;
    @GetMapping("/start")
    public String start() {
        return "！！！";
    }
    @GetMapping("/getUser")
    public List<User> getUser() {
        List<User> list = userService.getUser();
        return list;
    }
}
```
##### 后端：UserService.java
```java
@Service
public class UserService {
    @Resource
    private UserDao userDao;
    public List<User> getUser() {
        return userDao.getUser();
        //return userDao.selectAll(); //基于pom.xml依赖tk.mybatis查询数据库
        //return userDao.findBySearch(params); //传递参数
    }
}
```
##### 后端：UserDao.java(Interface)(Interface)
```java
@Repository
public interface UserDao extends Mapper<User> {//操作entity层：User
    //@Select("select * from user") //基于注解查询数据库
    List<User> getUser();
    //List<Admin> findBySearch(@Param("params")Params params); //绑定参数
}
```
##### 后端：UserMapper.xml
```xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE mapper PUBLIC "-//mybatis.org//DTD Mapper 3.0//EN" "http://mybatis.org/dtd/mybatis-3-mapper.dtd">
<mapper namespace="com.example.dao.UserDao"><!-- 映射dao层 -->
    <select id="getUser" resultType="com.example.entity.User">
        select * from user<!--基于xml映射查询数据库-->
    </select>
</mapper>
```
##### 后端：User.java
```java
@Table(name = "user")
public class User {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Integer id;
    @Column(name = "name")
    private String name;
    @Column(name = "password")
    private String password;
    @Column(name = "sex")
    private String sex;
    @Column(name = "age")
    private Integer age;
    @Column(name = "phone")
    private String phone;
    //getter setter constructor
}
```
##### 后端：pom.xml
```xml
<dependency>
			<groupId>org.mybatis.spring.boot</groupId>
			<artifactId>mybatis-spring-boot-starter</artifactId>
			<version>3.0.0</version>
</dependency>
<dependency>
    <groupId>mysql</groupId>
    <artifactId>mysql-connector-java</artifactId>
  	<version>8.0.13</version>
</dependency>
<dependency>
    <groupId>tk.mybatis</groupId>
    <artifactId>mapper</artifactId>
    <version>4.1.5</version>
</dependency>
```
##### 后端：appplication.yml
```yml
server:
  port:8080
# 数据库配置
spring:
  datasource:
    driver-class-name: com.mysql.cj.jdbc.Driver
    username: root   #你本地的数据库用户名
    password: 1234 #你本地的数据库密码
    url: jdbc:mysql://localhost:3306/springboot?useUnicode=true&characterEncoding=utf-8&allowMultiQueries=true&useSSL=false&serverTimezone=GMT%2b8&allowPublicKeyRetrieval=true
# 配置mybatis实体和xml映射
mybatis:
  mapper-locations: classpath:mapper/*.xml
  type-aliases-package: com.example.entity
```
##### 数据库：user.sql
```sql
DROP TABLE IF EXISTS `user`;
CREATE TABLE `user`  (
  `id` int(10) NOT NULL AUTO_INCREMENT COMMENT '主键ID',
  `name` varchar(255) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci NULL DEFAULT NULL COMMENT '姓名',
  `password` varchar(255) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci NULL DEFAULT NULL COMMENT '密码',
  `sex` varchar(255) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci NULL DEFAULT NULL COMMENT '性别',
  `age` int(10) NULL DEFAULT NULL COMMENT '年龄',
  `phone` varchar(255) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci NULL DEFAULT NULL COMMENT '电话',
  PRIMARY KEY (`id`) USING BTREE
) ENGINE = InnoDB CHARACTER SET = utf8mb4 COLLATE = utf8mb4_unicode_ci COMMENT = '用户信息表' ROW_FORMAT = Dynamic;
INSERT INTO `user` VALUES (1, '张三', '123456', '男', 25, '18888889999');
INSERT INTO `user` VALUES (2, '李四', '123456', '女', 25, '18899998888');
```
#### 20241230 武哥毕设 4.[增删改查]
05手把手教Springboot+Vue实现增删改查、分页查询、模糊查询功能
##### (1)统一封装
【前端】封装请求
安装axios：`npm i axios -S` package.json中出现axios
request.js：新建src.utils.request.js
【后端】统一返回类型
Result.java：新建com.example.common.Result.java
##### (2)全部查询
【数据库】
改表名：user变为admin
【前端】
AdminView.vue：
`import request from "@/utils/request";`
data：`tableData: []`清空假数据
create：`this.load();`初始化页面
method：`load(){}`加载(实现加载页面时查询全部数据并交给前端渲染)
发送请求`request.get("/admin")`
处理请求`.then(res => {处理请求})`
判断成功`if(res.code === '0'){}`
数据赋值`this.tableData = res.data;`
【后端】
AdminController.java：
`@RequestMapping("/admin")`
`@GetMapping`
`public Result findAll(){}`
`adminService.findAll()`
AdminService.java：
`public List<Admin> findAll(){}`
`adminDao.selectAll()` 基于tk.mybatis依赖查询数据库
AdminDao.java(Interface)：(extends Mapper<Admin>)
`List<Admin> findBySearch(@Param("params")Params params);`
Admin.java：
`@Table(name = "admin")`
定义变量，getter&setter
##### (3)条件查询
【前端】
AdminView.vue：
`<el-input v-model="params.name">` 绑定参数，用户输入
`<el-input v-model="params.phone">` 绑定参数，用户输入
`<elbutton @click="findBySearch()">` 绑定事件“搜索”
`<elbutton @click="reset()">` 绑定事件“清空”
data：`params: {name: '',phone: ''}`
method：`findBySearch(){}`“搜索”(条件查询，没有条件则查询全部)
发送请求`request.get("/admin/search",{params:this.params})` 传递参数
处理请求`.then(res => {处理请求})`
判断成功`if(res.code === '0'){}`
数据赋值`this.tableData = res.data;`
method：`reset(){}`“清空”
清空参数`this.params = {name: '',phone: ''}`
重载查询`this.findBySearch();`
【后端】
Params.java：
新建com.example.entity.Params.java 接收前端数据实体类
`private String name;`
`private String phone;`
AdminController.java：
`@RequestMapping("/admin")`
`@GetMapping("/search")`
`public Result findBySearch(Params params){}` 前端参数
`adminService.findBySearch(params)`
AdminService.java：
`public List<Admin> findBySearch(Params params){}`
`adminDao.findBySearch(params)()`
AdminDao.java(Interface)(Interface)：(extends Mapper<Admin>)
`List<Admin> findBySearch(@Param("params")Params params);`
AdminMapper.xml：
`<select id="findBySearch" resultType="com.example.entity.Admin">`
基于mapper.xml查询数据库
Admin.java：
`@Table(name = "admin")`
##### (4)分页查询
【前端】
AdminView.vue：
`<el-pagination>` 引入分页组件
`<el-pagination @size-change="handleSizeChange>"` 绑定事件
`<el-pagination @current-change="handleCurrentChange"` 绑定事件
`<el-pagination :current-page="params.pageNum">` 绑定参数，当前页数
`<el-pagination :page-size="params.pageSize">` 绑定参数，每页条数
`<el-pagination :page-sizes="[5, 10, 15, 20]">` 绑定参数，预设每页条数
`<el-pagination :total="total">` 绑定参数，总共条数
data：`params:{name: '',phone: '',pageNum: 1,pageSize: 5},tableData: [],total: 0`
method：`findBySearch(){}`“搜索”(条件查询，支持分页查询的条件查询)
发送请求`request.get("/admin/search",{params:this.params})` 传递参数
处理请求`.then(res => {处理请求})`
判断成功`if(res.code === '0'){}`
数据赋值`this.tableData = res.data.list;`返回类型List<Admin>变为PageInfo<Admin>
数据赋值 `this.total = res.data.total;`
method：`reset(){}`“清空”
清空参数`this.params = {pageNum: 1,pageSize: 5,name: '',phone: ''}`
重载查询`this.findBySearch();`
method：`handleSizeChange(pageSize){}`每页条数
传递参数：`this.params.pageSize = pageSize;`
重载查询：`this.findBySearch();`
method：`handleCurrentChange(pageNum){}`当前页数
传递参数：`this.params.pageNum = pageNum;`
重载查询：`this.findBySearch();`
【后端】
pom.xml：
`<groupId>com.github.pagehelper</groupId>`分页依赖
application.yml：
`pagehelper:`开启分页
`spring:`允许循环依赖
Params.java：
接收前端数据实体类 更新参数
`private String name;`
`private String phone;`
`private Integer PageNum;`
`private Integer PageSize;`
AdminController.java：
`@RequestMapping("/admin")`
`@GetMapping("/search")`
`public Result findBySearch(Params params){}` 前端参数
`adminService.findBySearch(params)`
AdminService.java：
`public PageInfo<Admin> findBySearch(Params params){}`
`PageHelper.startPage(params.getPageNum(), params.getPageSize());` 开启分页
`adminDao.findBySearch(params)()`
AdminDao.java(Interface)(Interface)：(extends Mapper<Admin>)
`List<Admin> findBySearch(@Param("params")Params params);`
AdminMapper.xml：
`<select id="findBySearch" resultType="com.example.entity.Admin">`
基于mapper.xml查询数据库
Admin.java：
`@Table(name = "admin")`
##### (5)增改
【前端】
AdminView.vue：
`<el-dialog>`引入对话框组件
`<el-radio>`引入单选框组件
`<elbutton @click="add()">` 绑定事件“新增”
`<elbutton @click="submit()">` 绑定事件“确认”
`<template slot-scope="scope">` 传递当前行数据“编辑”
`<el-button @click="edit(scope.row)">` 绑定事件“编辑”
data：`params:{name: '',phone: '',pageNum: 1,pageSize: 5},tableData: [],total: 0,dialogFormVisible: false,form:{}`
method：`add(){}`“新增”
清空表单`this.form = {};`清空原数据
显示表单`this.dialogFormVisible = true;`
method：`submit(){}`“确认”
发送请求`request.post("/admin",this.form)` 传递参数
处理请求`.then(res => {处理请求})`
判断成功`if(res.code === '0'){}else{判断失败}`
消息提示`this.$message({message: '操作成功',type: 'success'});`
消息提示`this.$message.success("操作成功");`
隐藏表单`this.dialogFormVisible = false;`
重载查询`this.findBySearch();`
消息提示`this.$message({message: res.msg,type: 'error'});`后端异常处理
消息提示`this.$message.error(res.msg);`后端异常处理
method：`edit(obj){}`“编辑”
数据赋值`this.form = obj;`编辑原数据
显示表单`this.dialogFormVisible = true;`
【后端】
AdminController.java：
`@RequestMapping("/admin")`
`@PostMapping`
`public Result save(@RequestBody Admin admin){}`前端参数，请求体
`if (admin.getId() == null){}`ID为空新增，非空编辑
`adminService.add(admin);`为空新增
`adminService.update(admin);`非空编辑
AdminService.java：
`public void add(Admin admin){}`“新增”
`if (admin.getName() == null || "".equals(admin.getName())){}`用户名为空【优化】
`throw new CustomException("用户名不能为空");`异常处理【优化】
`Admin user = adminDao.findByName(admin.getName());`查询数据【优化】
`if (user != null){}`用户名已存在【优化】
`throw new CustomException("用户名已存在");`异常处理【优化】
`if (admin.getPassword() == null){}`密码为空
`admin.setPassword("123456");`初始化密码
`adminDao.insertSelective(admin);`新增数据，基于tk.mybatis依赖新增
AdminService.java：
`public void update(Admin admin){}`“编辑”
`adminDao.updateByPrimaryKeySelective(admin);`编辑数据，基于tk.mybatis依赖更新
AdminDao.java(Interface)(Interface)：(extends Mapper<Admin>)
`Admin findByName(@Param("name")String name);`绑定参数
`@Select("select * from admin where name = #{name} limit 1")`基于注解查询
Admin.java：
`@Table(name = "admin")`
GlobalExceptionHandler.java：
新建com.example.exception.GlobalExceptionHandler.java 全局异常捕获器
`import jakarta.servlet.http.HttpServletRequest;`(SpringBoot3新特性：javax变更为jakarta)
`@ControllerAdvice(basePackages="com.example.controller")`基于指定包捕获异常
`@ExceptionHandler(Exception.class)` 监听系统异常(全局)
`return Result.error("系统异常");` 返回到前台
`@ExceptionHandler(CustomException.class)` 监听自定义异常
`return Result.error(e.getMsg());` 返回到前台
CustomException.java：
新建com.example.exception.CustomException.java 自定义异常
`extends RuntimeException`继承运行时异常类
`private String msg;`生成构造器、getter&setter 
提示：“新增”用户名非空判断并不完善，可以添加空格，初学供参考
##### (6)删除
【前端】
AdminView.vue：
`<el-popconfirm>` 引入气泡确认框组件
`<template slot-scope="scope">` 传递当前行数据“删除”
`<el-popconfirm @confirm="del(scope.row.id)">` 绑定事件“删除”
method：`del(id){}`
发送请求`request.post("/admin"+id)` 传递参数
处理请求`.then(res => {处理请求})`
判断成功`if(res.code === '0'){}else{判断失败}`
消息提示`this.$message({message: '删除成功',type: 'success'});`
重载查询`this.findBySearch();`
消息提示`this.$message({message: res.msg,type: 'error'});`后端异常处理
【后端】
AdminController.java：
`@RequestMapping("/admin")`
`@DeleteMapping("/{id}")`
`public Result delete(@PathVariable Integer id){}`前端参数，拼接路径
`adminService.delete(id);`
AdminService.java：
`public void delete(Integer id){}`“删除”
`adminDao.deleteByPrimaryKey(id);`删除数据，基于tk.mybatis依赖删除
AdminDao.java(Interface)(Interface)：(extends Mapper<Admin>)
Admin.java：
`@Table(name = "admin")`
##### 前端：request.js
```js
import axios from 'axios'
// 创建一个axios对象出来
const request = axios.create({
    baseURL: 'http://localhost:8080',
    timeout: 5000
})
// request 拦截器
// 可以自请求发送前对请求做一些处理
// 比如统一加token，对请求参数统一加密
request.interceptors.request.use(config => {
    config.headers['Content-Type'] = 'application/json;charset=utf-8';
    // config.headers['token'] = user.token;  // 设置请求头
    return config
}, error => {
    return Promise.reject(error)
});
// response 拦截器
// 可以在接口响应后统一处理结果
request.interceptors.response.use(
    response => {
        // response.data即为后端返回的Result
        let res = response.data;
        // 兼容服务端返回的字符串数据
        if (typeof res === 'string') {
            res = res ? JSON.parse(res) : res
        }
        return res;
    },
    error => {
        console.log('err' + error) // for debug
        return Promise.reject(error)
    }
)
export default request
```
##### 前端：AdminView.vue script
```js
<template>
  <div>
    <div>
      <el-input v-model="params.name" style="width: 200px; margin-right: 10px" placeholder="请输入姓名"></el-input>
      <el-input v-model="params.phone" style="width: 200px; margin-right: 10px" placeholder="请输入电话"></el-input>
      <el-button type="warning" @click="findBySearch()">搜索</el-button>
      <el-button type="primary" @click="reset()">清空</el-button>
      <el-button type="primary" @click="add()">新增</el-button>
    </div>
    <div>
      <el-table :data="tableData" style="width: 100%; margin: 15px 0px">
        <el-table-column prop="name" label="姓名" width="180"></el-table-column>
        <el-table-column prop="sex" label="性别" width="180"></el-table-column>
        <el-table-column prop="age" label="年龄" width="180"></el-table-column>
        <el-table-column prop="phone" label="电话" width="180"></el-table-column>
        <el-table-column label="操作">
          <template slot-scope="scope">
            <el-button type="primary" @click="edit(scope.row)">编辑</el-button>
            <el-popconfirm title="确定删除吗？" @confirm="del(scope.row.id)">
              <el-button slot="reference" type="danger" style="margin-left: 5px">删除</el-button>
            </el-popconfirm>
          </template>
        </el-table-column>
      </el-table>
    </div>
    <div class="block">
      <el-pagination
          @size-change="handleSizeChange"
          @current-change="handleCurrentChange"
          :current-page="params.pageNum"
          :page-sizes="[5, 10, 15, 20]"
          :page-size="params.pageSize"
          layout="total, sizes, prev, pager, next"
          :total="total">
      </el-pagination>
    </div>
    <div>
      <el-dialog title="请填写姓名" :visible.sync="dialogFormVisible" width="30%">
        <el-form :model="form">
          <el-form-item label="姓名" label-width="15%">
            <el-input v-model="form.name" autocomplete="off" style="width:90%"></el-input>
          </el-form-item>
          <el-form-item label="性别" label-width="15%">
            <el-radio v-model="form.sex" label="男">男</el-radio>
            <el-radio v-model="form.sex" label="女">女</el-radio>
          </el-form-item>
          <el-form-item label="年龄" label-width="15%">
            <el-input v-model="form.age" autocomplete="off" style="width:90%"></el-input>
          </el-form-item>
          <el-form-item label="电话" label-width="15%">
            <el-input v-model="form.phone" autocomplete="off" style="width:90%"></el-input>
          </el-form-item>
        </el-form>
        <div slot="footer" class="dialog-footer">
          <el-button @click="dialogFormVisible = false">取 消</el-button>
          <el-button type="primary" @click="submit()">确 定</el-button>
        </div>
      </el-dialog>
    </div>
  </div>
</template>
<script>
import request from "@/utils/request";
export default {
  name: "AdminView",
  data() {
    return {
      params:{
        name: '',
        phone: '',
        pageNum: 1,
        pageSize: 5
      },
      tableData: [],
      total: 0,
      dialogFormVisible: false,
      form: {}
    }
  },
  created() {
    //this.load();
    this.findBySearch();
  },
  methods: {
    // load() {
    //   request.get("/admin").then(res => {
    //     if (res.code === '0') {
    //       this.tableData = res.data;
    //     }
    //   })
    // },
    findBySearch(){
      request.get("/admin/search",{params:this.params}).then(res =>{
        if(res.code === '0'){
          this.tableData = res.data.list;
          this.total = res.data.total;
        }else{
          this.$message(error(res.msg));
        }
      })
    },
    reset(){
      this.params = {
        pageNum: 1,
        pageSize: 5,
        name: '',
        phone: ''
      }
      this.findBySearch();
    },
    handleSizeChange(pageSize) {
      this.params.pageSize = pageSize;
      this.findBySearch();
    },
    handleCurrentChange(pageNum) {
      this.params.pageNum = pageNum;
      this.findBySearch();
    },
    add(){
      this.form = {};
      this.dialogFormVisible = true;
    },
    edit(obj) {
      this.form = obj;
      this.dialogFormVisible = true;
    },
    submit(){
      request.post("/admin", this.form).then(res => {
        if (res.code === '0') {
          this.$message({
            message: '操作成功',
            type: 'success'
          });
          this.dialogFormVisible = false;
          this.findBySearch();
        } else {
          this.$message(error(res.msg));
        }
      })
    },
    del(id) {
      request.delete("/admin/" + id).then(res => {
        if (res.code === '0') {
          this.$message({
            message: '删除成功',
            type: 'success'
          });
          this.findBySearch();
        } else {
          this.$message(error(res.msg));
        }
      })
    }
  }
}
</script>
```
##### 后端：Result.java
```java
private static final String SUCCESS = "0";
private static final String ERROR = "-1";
private String code;
private String msg;
private Object data;
public static Result success() {
    Result result = new Result();
    result.setCode(SUCCESS);
    return result;
}
public static Result success(Object data) {
    Result result = new Result();
    result.setCode(SUCCESS);
    result.setData(data);
    return result;
}
public static Result error(String msg) {
    Result result = new Result();
    result.setCode(ERROR);
    result.setMsg(msg);
    return result;
}
```
##### 后端：Params.java
```java
public class Params {
    private String name;
    private String phone;
    private Integer PageNum;
    private Integer PageSize;
}
```
##### 后端：AdminCtroller.java
```java
@CrossOrigin
@RestController
@RequestMapping("/admin")
public class AdminController {
    @Resource
    private AdminService adminService;
    @GetMapping
    public Result findAll() {
        List<Admin> list = adminService.findAll();
        return Result.success(list);
    }
    @GetMapping("/search")
    public Result findBySearch(Params params) {
        //List<Admin> list = adminService.findBySearch(params);
        PageInfo<Admin> info = adminService.findBySearch(params);
        return Result.success(info);
    }
    @PostMapping
    public Result save(@RequestBody Admin admin) {
        if (admin.getId() == null) {
            adminService.add(admin);
        } else {
            adminService.update(admin);
        }
        return Result.success();
    }
    @DeleteMapping("/{id}")
    public Result delete(@PathVariable Integer id) {
        adminService.delete(id);
        return Result.success();
    }
}
```
##### 后端：AdminService.java
```java
@Service
public class AdminService {
    @Resource
    private AdminDao adminDao;
    public List<Admin> findAll() {
        return adminDao.selectAll();
    }
    public PageInfo<Admin> findBySearch(Params params) {
        // 开启分页查询
        PageHelper.startPage(params.getPageNum(), params.getPageSize());
        // 接下来的查询会自动按照当前开启的分页设置来查询
        //return adminDao.findBySearch(params);
        List<Admin> list = adminDao.findBySearch(params);
        return PageInfo.of(list);
    }
    public void add(Admin admin) {
        if (admin.getName() == null || "".equals(admin.getName())) {
            throw new CustomException("用户名不能为空");
        }
        Admin user = adminDao.findByName(admin.getName());
        if (user != null) {
            throw new CustomException("用户名已存在");
        }
        if (admin.getPassword() == null) {
            admin.setPassword("123456");
        }
        adminDao.insertSelective(admin);
    }
    public void update(Admin admin) {
        adminDao.updateByPrimaryKeySelective(admin);
    }
    public void delete(Integer id) {
        adminDao.deleteByPrimaryKey(id);
    }
}
```
##### 后端：AdminDao.java(Interface)
```java
@Repository
public interface AdminDao extends Mapper<Admin> {
    //@Select("select * from user")
    //List<Admin> getUser();
    List<Admin> findBySearch(@Param("params")Params params);
    @Select("select * from admin where name = #{name} limit 1")
    Admin findByName(@Param("name")String name);
}
```
##### 后端：AdminMapper.xml
```xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE mapper PUBLIC "-//mybatis.org//DTD Mapper 3.0//EN" "http://mybatis.org/dtd/mybatis-3-mapper.dtd">
<mapper namespace="com.example.dao.AdminDao">
<!--    <select id="getUser" resultType="com.example.entity.Admin">-->
<!--        select * from user-->
<!--    </select>-->
    <select id="findBySearch" resultType="com.example.entity.Admin">
        select * from admin
        <where>
            <if test="params != null and params.name != null and params.name != ''">
                and name like concat('%', #{ params.name }, '%')
            </if>
            <if test="params != null and params.phone != null and params.phone != ''">
                and phone like concat('%', #{ params.phone }, '%')
            </if>
        </where>
    </select>
</mapper>
```
##### 后端：Admin.java
```java
@Table(name = "admin")
public class Admin {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Integer id;
    @Column(name = "name")
    private String name;
    @Column(name = "password")
    private String password;
    @Column(name = "sex")
    private String sex;
    @Column(name = "age")
    private Integer age;
    @Column(name = "phone")
    private String phone;
}
```
##### 后端：GlobalExceptionHandler.java
```java
import com.example.common.Result;
import org.slf4j.Logger;
import org.slf4j.LoggerFactory;
import org.springframework.web.bind.annotation.ControllerAdvice;
import org.springframework.web.bind.annotation.ExceptionHandler;
import org.springframework.web.bind.annotation.ResponseBody;

import javax.servlet.http.HttpServletRequest;

@ControllerAdvice(basePackages="com.example.controller")
public class GlobalExceptionHandler {

    private static final Logger log = LoggerFactory.getLogger(GlobalExceptionHandler.class);

    //统一异常处理@ExceptionHandler,主要用于Exception
    @ExceptionHandler(Exception.class)
    @ResponseBody
    public Result error(HttpServletRequest request, Exception e){
        log.error("异常信息：",e);
        return Result.error("系统异常");
    }

    @ExceptionHandler(CustomException.class)
    @ResponseBody
    public Result customError(HttpServletRequest request, CustomException e){
        return Result.error(e.getMsg());
    }
}
```
##### 后端：CustomException.java
```java
package com.example.exception;
public class CustomException extends RuntimeException {
    private String msg;
    public CustomException(String msg) {
        this.msg = msg;
    }
    public String getMsg() {
        return msg;
    }
    public void setMsg(String msg) {
        this.msg = msg;
    }
}
```
##### 后端：pom.xml
```xml
		<dependency>
			<groupId>org.mybatis.spring.boot</groupId>
			<artifactId>mybatis-spring-boot-starter</artifactId>
			<version>3.0.0</version>
		</dependency>
		<dependency>
			<groupId>mysql</groupId>
			<artifactId>mysql-connector-java</artifactId>
			<version>8.0.13</version>
		</dependency>
		<dependency>
			<groupId>tk.mybatis</groupId>
			<artifactId>mapper</artifactId>
			<version>4.1.5</version>
		</dependency>
		<dependency>
			<groupId>com.github.pagehelper</groupId>
			<artifactId>pagehelper-spring-boot-starter</artifactId>
			<version>2.1.0</version>
		</dependency>
    <!-- <dependency>
			<groupId>javax.servlet</groupId>
			<artifactId>javax.servlet-api</artifactId>
			<version>3.1.0</version>
		</dependency> -->
```
##### 后端：application.yml
```yml
server:
  port:8080
# 数据库配置
spring:
  datasource:
    driver-class-name: com.mysql.cj.jdbc.Driver
    username: root   #你本地的数据库用户名
    password: 1234 #你本地的数据库密码
    url: jdbc:mysql://localhost:3306/springboot?useUnicode=true&characterEncoding=utf-8&allowMultiQueries=true&useSSL=false&serverTimezone=GMT%2b8&allowPublicKeyRetrieval=true
  main:
    allow-circular-references: true
# 配置mybatis实体和xml映射
mybatis:
  mapper-locations: classpath:mapper/*.xml
  type-aliases-package: com.example.entity
# 开启分页
pagehelper:
  helper-dialect: mysql
  reasonable: true
  support-methods-arguments: true
  params: count=countSql
```
#### 20250103 武哥毕设 5.[登录注册]
06手把手教Springboot+Vue实现登录注册
##### (1)登录
【前端】
LoginView.vue：
新建src.views.LoginView.vue
`<el-form>` 引入表单组件
`<el-input>` 引入输入框组件
`<el-button>` 引入按钮组件
Layout.vue：
新建src.views.Layout.vue
将App.vue剪切到Layout.vue
App.vue：
添加`<router-view/>` 渲染当前路由引用页面
index.js：
引入页面LoginView.vue(配置路由path、name、component)
引入页面Layout.vue(分级路由path、name、component、redirect、children)
将HomeView.vue、AdminView.vue调整为Layout.vue的子路由
LoginView.vue：
`<el-form :model="admin">`绑定参数
`<el-input v-model="admin.name">`绑定参数，用户输入
`<el-input v-model="admin.password"`绑定参数，用户输入
`<el-input v-model="admin.password" show-password`设置属性，显示隐藏密码
`<el-button @click="login()">` 绑定事件“登录”
`import request from "@/utils/request";`
data：`admin:{name: '',password: ''}`
method：`login(){}`“登录”
发送请求`request.post("/admin.login",this.admin)`
处理请求`.then(res => {处理请求})`
判断成功`if(res.code === '0'){}`
消息提示`this.$message({message: '登录成功',type: 'success'});`
跳转路由`this.$router.push("/");`
消息提示`this.$message({message: res.msg,type: 'error'});`后端异常处理
【后端】
AdminController.java：
`@RequestMapping("/admin")`
`@PostMapping("/login")`
`public Result login(@RequestBody Admin admin){}`前端参数，请求体
`Admin loginUser = adminService.login(admin);`
AdminService.java：
`public Admin login(Admin admin){}`“登录”
`if (admin.getName() == null || "".equals(admin.getName())){}`用户名为空
`throw new CustomException("用户名不能为空");`异常处理
`if (admin.getPassword() == null || "".equals(admin.getPassword())){}`密码为空
`throw new CustomException("密码不能为空");`异常处理
`Admin user = adminDao.findByNameAndPassword(admin.getName(), admin.getPassword());`查询账户
`if (user == null){}`查询失败
`throw new CustomException("用户名或密码输入错误");`异常处理
AdminDao.java(Interface)：(extends Mapper<Admin>)
`Admin findByNameAndPassword(@Param("name")String name, @Param("password")String password);`绑定参数
`@Select("select * from admin where name =#{name} and password =#{password}")`基于注解查询
Admin.java：
`@Table(name = "admin")`
##### (2)注册
【前端】
RegisterView.vue：
新建src.views.RegisterView.vue
`<el-form>` 引入表单组件
`<el-input>` 引入输入框组件
`<el-button>` 引入按钮组件
index.js：
引入页面RegisterView.vue(配置路由path、name、component)
【后端】
AdminController.java：
`@RequestMapping("/admin")`
`@PostMapping("/register")`
`public Result register(@RequestBody Admin admin){}`前端参数，请求体
`adminService.add(admin);`
AdminService.java：
`public void add(Admin admin){}`“注册”
`if (admin.getName() == null || "".equals(admin.getName())){}`用户名为空【优化】
`throw new CustomException("用户名不能为空");`异常处理【优化】
`Admin user = adminDao.findByName(admin.getName());`查询数据【优化】
`if (user != null){}`用户名已存在【优化】
`throw new CustomException("用户名已存在");`异常处理【优化】
`if (admin.getPassword() == null){}`密码为空
`admin.setPassword("123456");`初始化密码
`adminDao.insertSelective(admin);`新增数据，基于tk.mybatis依赖新增
AdminDao.java(Interface)(Interface)：(extends Mapper<Admin>)
`Admin findByName(@Param("name")String name);`绑定参数
`@Select("select * from admin where name = #{name} limit 1")`基于注解查询
Admin.java：
`@Table(name = "admin")`
##### 前端：App.vue
```js
<template>
  <div id="app">
    <router-view/>
  </div>
</template>
<style>
</style>
<script lang="ts">
</script>
```
##### 前端：LoginView.vue
```js
<template>
  <div>
    <div style="width: 400px; height: 350px; margin: 150px auto; background-color:rgba(107,149,224,0.5); border-radius: 10px">
      <div style="width: 100%; height: 100px; font-size: 30px; line-height: 100px; text-align: center; color: #4a5ed0">欢迎登录</div>
      <div style="margin-top: 25px; text-align: center; height: 320px;">
        <el-form :model="admin">
          <el-form-item>
            <el-input v-model="admin.name" prefix-icon="el-icon-user" style="width: 80%" placeholder="请输入用户名"></el-input>
          </el-form-item>
          <el-form-item>
            <el-input v-model="admin.password" show-password prefix-icon="el-icon-lock" style="width: 80%" placeholder="请输入密码"></el-input>
          </el-form-item>
          <el-form-item>
            <el-button style="width: 80%; margin-top: 10px" type="primary" @click="login()">登录</el-button>
          </el-form-item>
        </el-form>
      </div>
    </div>
  </div>
</template>
<script>
import request from "@/utils/request";
export default {
  name: "Login",
  data() {
    return {
      admin:{
        name: '',
        password: ''
      }

    }
  },
  methods: {
    login(){
      request.post("/admin/login", this.admin).then(res =>{
        if(res.code === '0'){
          this.$message({
            message: '登录成功',
            type: 'success'
          });
          this.$router.push("/");
        }else {
          this.$message({
            message: res.msg,
            type: 'error'
          });
        }
      })
    }

  }
}
</script>
```
##### 前端：RegisterView.vue
```js
<template>
  <div>
    <div style="width: 400px; height: 350px; margin: 150px auto; background-color:rgba(107,149,224,0.5); border-radius: 10px">
      <div style="width: 100%; height: 100px; font-size: 30px; line-height: 100px; text-align: center; color: #4a5ed0">欢迎注册</div>
      <div style="margin-top: 25px; text-align: center; height: 320px;">
        <el-form :model="admin">
          <el-form-item>
            <el-input v-model="admin.name" prefix-icon="el-icon-user" style="width: 80%" placeholder="请输入用户名"></el-input>
          </el-form-item>
          <el-form-item>
            <el-input v-model="admin.password" prefix-icon="el-icon-lock" style="width: 80%" placeholder="请输入密码"></el-input>
          </el-form-item>
          <el-form-item>
            <el-button style="width: 80%; margin-top: 10px" type="primary" @click="register()">注册</el-button>
          </el-form-item>
        </el-form>
      </div>
    </div>
  </div>
</template>
<script>
import request from "@/utils/request";

export default {
  name: "Register",
  data() {
    return {
      admin:{
        //name: '',
        //password: ''
      }
    }
  },
  // 页面加载的时候，做一些事情，在created里面
  created() {
  },
  methods: {
    register(){
      request.post("/admin/register", this.admin).then(res =>{
        if(res.code === '0'){
          this.$message({
            message: '注册成功',
            type: 'success'
          });
          this.$router.push("/login");
        }else {
          this.$message({
            message: res.msg,
            type: 'error'
          });
        }
      })
    }

  }
}
</script>
```
##### 前端：index.js 分级路由
```js
import Vue from 'vue'
import VueRouter from 'vue-router'
import HomeView from '../views/HomeView.vue'
import LoginView from "@/views/LoginView.vue";
import Layout from "@/views/Layout.vue";
import RegisterView from "@/views/RegisterView.vue";
import BookView from "@/views/BookView.vue";

Vue.use(VueRouter)
const routes = [
  {
    path: '/login',
    name: 'Login',
    component: LoginView
  },
  {
    path: '/',
    name: 'Layout',
    component: Layout,
    //redirect: '/home',
    children: [ // 子路由
      {
        path: '',
        name: 'home',
        component: HomeView
      },
      {
        path: 'admin',
        name: 'admin',
        component: () => import('../views/AdminView.vue')
      }
    ]
  },
]
const router = new VueRouter({
  mode: 'history',
  base: process.env.BASE_URL,
  routes
})
export default router
```
##### 后端：AdminCtroller.java
```java
@PostMapping("/login")
public Result login(@RequestBody Admin admin) {
    Admin loginUser = adminService.login(admin);
    return Result.success(loginUser);
}
@PostMapping("/register")
public Result register(@RequestBody Admin admin) {
    adminService.add(admin);
    return Result.success();
}
```
##### 后端：AdminService.java
```java
public Admin login(Admin admin) {
    // 1. 进行一些非空判断
    //return null;
    if (admin.getName() == null || "".equals(admin.getName())) {
        throw new CustomException("用户名不能为空");
    }
    if (admin.getPassword() == null || "".equals(admin.getPassword())) {
        throw new CustomException("密码不能为空");
    }
    // 2. 从数据库里面根据这个用户名和密码去查询对应的管理员信息，
    Admin user = adminDao.findByNameAndPassword(admin.getName(), admin.getPassword());
    if (user == null) {
        // 如果查出来没有，那说明输入的用户名或者密码有误，提示用户，不允许登录
        throw new CustomException("用户名或密码输入错误");
    }
    // 如果查出来了有，那说明确实有这个管理员，而且输入的用户名和密码都对；
    return user;
}
```
##### 后端：AdminDao.java(Interface)(Interface)
```java
@Select("select * from admin where name =#{name} and password =#{password}")
Admin findByNameAndPassword(@Param("name")String name, @Param("password")String password);
```
#### 20250109 武哥毕设 6.[登录鉴权Jwt]
07手把手教Springboot+Vue+JWT实现用户登录鉴权
##### (1)登录退出
【前端】
浏览器：
用户登录后，将用户信息缓存到前端，管理后台即可获取数据并展示到页面
打开F12开发者模式，点击“应用程序(Application)”，找到“存储(Storage)”，
提供本地存储(LocalStorage)、Cookies两种存储方式。以本地存储(LocalStorage)为例
LoginView.vue：
`localStorage.setItem("user", JSON.stringify(res.data));`缓存数据
LayoutView.vue：
`<el-dropdown>`引入下拉菜单组件
`<span>{{ user.name }}</span>` 绑定参数
`<div @click="logout">` 绑定事件“退出”
data：`user: localStorage.getItem("user") ? JSON.parse(localStorage.getItem("user")) : {}`获取数据
method：`logout(){}`“退出”
清除缓存`localStorage.removeItem("user");`
跳转路由`this.$router.push("/login");`
##### (2)前端鉴权(不安全：前端数据可以人为篡改)
【前端】
index.js：
`router.beforeEach((to ,from, next) =>{})`路由守卫
`if (to.path ==='/login'){}`前往登录页
`next();`允许跳转
`const user = localStorage.getItem("user");`获取数据
`if (!user && to.path !== '/login'){}`获取失败且前往非登录页(sql注入)
`return next("/login");`跳转登录
`next();`允许跳转
##### (3)后端鉴权(Jwt，token生成)
【前端】
request.js：
`baseURL: 'http://localhost:8080/api'`连接后端，统一前缀"/api"
`request.interceptors.request.use()` request拦截器，可在发送请求前做一些处理
`const user = localStorage.getItem("user");`获取数据
`if (user) {config.headers['token'] = JSON.parse(user).token;}`添加token到请求头
【后端】
pom.xml：
`<artifactId>java-jwt</artifactId>`jwt依赖
`<artifactId>hutool-all</artifactId>`hutool依赖
WebConfig.java：拦截器配置
新建src.main.java.com.example.common.WebConfig.java
`@Configuration`配置
`@Override`重写
`public void configurePathMatch(PathMatchConfigurer configurer){}`路由配置
`configurer.addPathPrefix("/api", clazz -> clazz.isAnnotationPresent(RestController.class));`统一前缀"/api"
JwtTokenUtils.java：Jwt工具类，生成token
新建src.main.java.com.example.common.JwtTokenUtils.java
SpringBoot3新特性：javax变更为jakarta
`@Component`组件
`private static AdminService staticAdminService;`创建对象
`@Resource`引入service层(`private AdminService adminService;`)
`@PostConstruct`项目启动时执行方法(Spring容器初始化时执行方法)
`public void setUserService(){}`引入Service层(`staticAdminService = adminService;`)
`public static String genToken(String adminId, String sign){}`生成token
创建`JWT.create()`JWT创建
载荷`.withAudience(adminId)`用户Id作为载荷
期限`.withExpiresAt(DateUtil.offsetHour(new Date(), 2))`过期时间2小时
签证`.sign(Algorithm.HMAC256(sign));`password作为签证，加密算法Algorithm.HMAC256
AdminService.java：
`public Admin login(Admin admin){}` 完善登录
`String token = JwtTokenUtils.genToken(user.getId().toString(), user.getPassword());`生成tokon
`user.setToken(token);`携带token返回前端
Admin.java：
`@Transient`非数据库字段
`private String token;`定义变量token
生成getter&setter
##### (4)后端鉴权(Jwt，token验证)
【后端】
JwtInterceptor.java：自定义Jwt拦截器(前端请求后端api时拦截验证token)
新建src.main.java.com.example.common.JwtInterceptor.java
SpringBoot3新特性：javax变更为jakarta
`@Component`组件
`@Override`重写方法
`public boolean preHandle(HttpServletRequest request, HttpServletResponse response, Object handler){}`token验证
`String token = request.getHeader("token");`从http请求头中获取token
`if (StrUtil.isBlank(token)){}`获取失败
`token = request.getParameter("token");`从参数获取数据(如"?"后的参数"/api/admin?token=xxxxx&yyyy&zzzz")
`if (StrUtil.isBlank(token)){}`获取失败
`throw new CustomException("无token，请重新登录");`异常处理
`try{}catch(Exception e){}`
`userId = JWT.decode(token).getAudience().get(0);`token解码
`admin = adminService.findById(Integer.parseInt(userId));`根据id查用户
`throw new CustomException(errMsg);`异常处理，返回前端
`if (admin == null){}`查询失败
`throw new CustomException("用户不存在，请重新登录");`异常处理
`try{}catch(JWTVerificationException e){}`
`JWTVerifier jwtVerifier = JWT.require(Algorithm.HMAC256(admin.getPassword())).build();`根据用户查密码并加签
`jwtVerifier.verify(token);`token验证
`throw new CustomException("token验证失败，请重新登录");`异常处理
AdminService.java：
`@Resource`引入dao层(`private UserDao userDao;`)
`public Admin findById(Integer id){}`根据id查用户方法
`return adminDao.selectByPrimaryKey(id);`基于pom.xml依赖tk.mybatis查询数据库
AdminDao.java(Interface)(Interface)：(extends Mapper<Admin>)
Admin.java：`@Table(name = "admin")`
WebConfig.java：
`@Resource`引入拦截器(`private JwtInterceptor jwtInterceptor;`)
`public void addInterceptors(InterceptorRegistry registry){}`新增拦截器
`registry.addInterceptor(jwtInterceptor)`新增拦截器
`.addPathPatterns("/api/**")`拦截规则(拦截所有"/api"开头的)
`.excludePathPatterns("/api/admin/login")`拦截规则(不包括"/api/admin/login")，放行登录页面
`.excludePathPatterns("/api/admin/register");`拦截规则(不包括"/api/admin/register")，放行注册页面
##### (5)后端鉴权(解决跨域问题)
CorsConfig.java
##### 前端：LoginView.vue
```js
<template>
  <div>
    <div style="width: 400px; height: 350px; margin: 150px auto; background-color:rgba(107,149,224,0.5); border-radius: 10px">
      <div style="width: 100%; height: 100px; font-size: 30px; line-height: 100px; text-align: center; color: #4a5ed0">欢迎登录</div>
      <div style="margin-top: 25px; text-align: center; height: 320px;">
        <el-form :model="admin">
          <el-form-item>
            <el-input v-model="admin.name" prefix-icon="el-icon-user" style="width: 80%" placeholder="请输入用户名"></el-input>
          </el-form-item>
          <el-form-item>
            <el-input v-model="admin.password" show-password prefix-icon="el-icon-lock" style="width: 80%" placeholder="请输入密码"></el-input>
          </el-form-item>
          <el-form-item>
            <el-button style="width: 80%; margin-top: 10px" type="primary" @click="login()">登录</el-button>
          </el-form-item>
        </el-form>
      </div>
    </div>
  </div>
</template>
<script>
import request from "@/utils/request";

export default {
  name: "Login",
  data() {
    return {
      admin:{
        //name: '',
        //password: ''
      }
    }
  },
  // 页面加载的时候，做一些事情，在created里面
  created() {
  },
  methods: {
    login(){
      request.post("/admin/login", this.admin).then(res =>{
        if(res.code === '0'){
          this.$message({
            message: '登录成功',
            type: 'success'
          });
          localStorage.setItem("user", JSON.stringify(res.data));
          this.$router.push("/");
        }else {
          this.$message({
            message: res.msg,
            type: 'error'
          });
        }
      })
    }
  }
}
</script>
```
##### 前端：LayoutView.vue
```java
<template>
  <div>
    <el-container>
      <el-header style="background-color: #4c535a">
        <img src="@/assets/logo.png" alt="" style="width: 40px; position: relative; top: 10px;">
        <span style="font-size: 20px; margin-left: 15px; color: white">手拉手带小白做毕设</span>
        <el-dropdown style="float: right; height: 60px; line-height: 60px">
          <span class="el-dropdown-link" style="color: white; font-size: 16px">{{ user.name }}<i class="el-icon-arrow-down el-icon--right"></i></span>
          <el-dropdown-menu slot="dropdown">
            <el-dropdown-item>
              <div @click="logout">退出</div>
            </el-dropdown-item>
          </el-dropdown-menu>
        </el-dropdown>
      </el-header>
    </el-container>
    <el-container>
      <el-aside style="overflow: hidden; min-height: 100vh; background-color: #545c64; width: 250px">
        <el-menu :default-active="$route.path" router background-color="#545c64" text-color="#fff" active-text-color="#ffd04b">
          <el-menu-item index="/">
            <i class="el-icon-s-home"></i>
            <span slot="title">系统首页</span>
          </el-menu-item>
          <el-submenu index="2">
            <template slot="title">
              <i class="el-icon-location"></i><span>用户管理</span>
            </template>
            <el-menu-item-group>
              <el-menu-item index="/admin">管理员信息</el-menu-item>
              <el-menu-item index="2-2">用户信息</el-menu-item>
            </el-menu-item-group>
          </el-submenu>
          <el-submenu index="3">
            <template slot="title">
              <i class="el-icon-location"></i><span>信息管理</span>
            </template>
            <el-menu-item-group>
              <el-menu-item index="3-1">xxx信息</el-menu-item>
              <el-menu-item index="3-2">yyy信息</el-menu-item>
            </el-menu-item-group>
          </el-submenu>
        </el-menu>
      </el-aside>
      <el-main>
        <router-view/>
      </el-main>
    </el-container>
  </div>
</template>
<style>
.el-menu{
  border-right: none !important;
}
</style>
<script>
export default {
  name: "Layout",
  data() {
    return {
      // user: {name: ''}
      user: localStorage.getItem("user") ? JSON.parse(localStorage.getItem("user")) : {}
    }
  },
  created() {
    this.user = JSON.parse(localStorage.getItem('user'))
  },
  methods: {
    logout() {
      localStorage.removeItem('user')
      this.$router.push('/login')
    }
  }
}
</script>
```
##### 前端：index.js
```js
// 路由守卫
router.beforeEach((to ,from, next) => {
  if (to.path ==='/login') {
    next();
  }
  const user = localStorage.getItem("user");
  if (!user && to.path !== '/login') {
    return next("/login");
  }
  next();
})
export default router
```
##### 前端：request.js
```js
import axios from 'axios'
// 创建一个axios对象出来
const request = axios.create({
    baseURL: 'http://localhost:8080/api',// /api
    timeout: 5000
})
// request 拦截器
// 可以自请求发送前对请求做一些处理
// 比如统一加token，对请求参数统一加密
request.interceptors.request.use(config => {
    config.headers['Content-Type'] = 'application/json;charset=utf-8';

    const user = localStorage.getItem("user");
    if (user) {
        config.headers['token'] = JSON.parse(user).token;
    }
    // config.headers['token'] = user.token;  // 设置请求头
    return config
}, error => {
    return Promise.reject(error)
});
// response 拦截器
// 可以在接口响应后统一处理结果
request.interceptors.response.use(
    response => {
        // response.data即为后端返回的Result
        let res = response.data;
        // 兼容服务端返回的字符串数据
        if (typeof res === 'string') {
            res = res ? JSON.parse(res) : res
        }
        return res;
    },
    error => {
        console.log('err' + error) // for debug
        return Promise.reject(error)
    }
)
export default request
```
##### 后端：pom.xml
```xml
<dependency>
	<groupId>com.auth0</groupId>
	<artifactId>java-jwt</artifactId>
	<version>3.10.3</version>
</dependency>
<dependency>
	<groupId>cn.hutool</groupId>
	<artifactId>hutool-all</artifactId>
	<version>5.3.7</version>
</dependency>
```
##### 后端：CorsConfig.java
```java
//解决跨域问题
import org.springframework.context.annotation.Bean;
import org.springframework.context.annotation.Configuration;
import org.springframework.web.cors.CorsConfiguration;
import org.springframework.web.cors.UrlBasedCorsConfigurationSource;
import org.springframework.web.filter.CorsFilter;

@Configuration
public class CorsConfig {

    @Bean
    public CorsFilter corsFilter() {
        UrlBasedCorsConfigurationSource source = new UrlBasedCorsConfigurationSource();
        CorsConfiguration corsConfiguration = new CorsConfiguration();
        corsConfiguration.addAllowedOrigin("*"); // 1 设置访问源地址
        corsConfiguration.addAllowedHeader("*"); // 2 设置访问源请求头
        corsConfiguration.addAllowedMethod("*"); // 3 设置访问源请求方法
        source.registerCorsConfiguration("/**", corsConfiguration); // 4 对接口配置跨域设置
        return new CorsFilter(source);
    }
}
```
##### 后端：WebConfig.java
```java
package com.example.common;
import jakarta.annotation.Resource;
import org.springframework.context.annotation.Configuration;
import org.springframework.web.bind.annotation.RestController;
import org.springframework.web.servlet.config.annotation.InterceptorRegistry;
import org.springframework.web.servlet.config.annotation.PathMatchConfigurer;
import org.springframework.web.servlet.config.annotation.WebMvcConfigurer;
@Configuration
public class WebConfig implements  WebMvcConfigurer {
    @Resource
    private JwtInterceptor jwtInterceptor;
    @Override
    public void configurePathMatch(PathMatchConfigurer configurer) {
        // 指定controller统一的接口前缀
        configurer.addPathPrefix("/api", clazz -> clazz.isAnnotationPresent(RestController.class));
    }
    // 加自定义拦截器JwtInterceptor，设置拦截规则
    @Override
    public void addInterceptors(InterceptorRegistry registry) {
        registry.addInterceptor(jwtInterceptor).addPathPatterns("/api/**")
                .excludePathPatterns("/api/admin/login")
                .excludePathPatterns("/api/admin/register");
    }
}
```
##### 后端：AdminService.java
```java
public Admin login(Admin admin) {
    // 1. 进行一些非空判断
    //return null;
    if (admin.getName() == null || "".equals(admin.getName())) {
        throw new CustomException("用户名不能为空");
    }
    if (admin.getPassword() == null || "".equals(admin.getPassword())) {
        throw new CustomException("密码不能为空");
    }
    // 2. 从数据库里面根据这个用户名和密码去查询对应的管理员信息，
    Admin user = adminDao.findByNameAndPassword(admin.getName(), admin.getPassword());
    if (user == null) {
        // 如果查出来没有，那说明输入的用户名或者密码有误，提示用户，不允许登录
        throw new CustomException("用户名或密码输入错误");
    }
    // 如果查出来了有，那说明确实有这个管理员，而且输入的用户名和密码都对；
    // 生成jwt token给前端
    String token = JwtTokenUtils.genToken(user.getId().toString(), user.getPassword());
    user.setToken(token);
    return user;
}
public Admin findById(Integer id) {
    return adminDao.selectByPrimaryKey(id);
}
```
##### 后端：JwtTokenUtils.java
```java
package com.example.common;
import cn.hutool.core.date.DateUtil;
import cn.hutool.core.util.StrUtil;
import com.auth0.jwt.JWT;
import com.auth0.jwt.algorithms.Algorithm;
import com.example.entity.Admin;
import com.example.service.AdminService;
import org.slf4j.Logger;
import org.slf4j.LoggerFactory;
import org.springframework.stereotype.Component;
import org.springframework.web.context.request.RequestContextHolder;
import org.springframework.web.context.request.ServletRequestAttributes;
//import javax.annotation.PostConstruct;
//import javax.annotation.Resource;
//import javax.servlet.http.HttpServletRequest;
import jakarta.annotation.PostConstruct;
import jakarta.annotation.Resource;
import jakarta.servlet.http.HttpServletRequest;
import java.util.Date;
@Component
public class JwtTokenUtils {
    private static AdminService staticAdminService;
    private static final Logger log = LoggerFactory.getLogger(JwtTokenUtils.class);
    @Resource
    private AdminService adminService;
    @PostConstruct
    public void setUserService() {
        staticAdminService = adminService;
    }
    /**
     * 生成token
     */
    public static String genToken(String adminId, String sign) {
        return JWT.create().withAudience(adminId) // 将 user id 保存到 token 里面,作为载荷
                .withExpiresAt(DateUtil.offsetHour(new Date(), 2)) // 2小时后token过期
                .sign(Algorithm.HMAC256(sign)); // 以 password 作为 token 的密钥
    }
    /**
     * 获取当前登录的用户信息
     */
    public static Admin getCurrentUser() {
        String token = null;
        try {
            HttpServletRequest request = ((ServletRequestAttributes) RequestContextHolder.getRequestAttributes()).getRequest();
            token = request.getHeader("token");
            if (StrUtil.isBlank(token)) {
                token = request.getParameter("token");
            }
            if (StrUtil.isBlank(token)) {
                log.error("获取当前登录的token失败， token: {}", token);
                return null;
            }
            // 解析token，获取用户的id
            String adminId = JWT.decode(token).getAudience().get(0);
            return staticAdminService.findById(Integer.valueOf(adminId));
        } catch (Exception e) {
            log.error("获取当前登录的管理员信息失败, token={}", token,  e);
            return null;
        }
    }
}
```
##### 后端：JwtInterceptor.java
```java
package com.example.common;
import cn.hutool.core.util.StrUtil;
import com.auth0.jwt.JWT;
import com.auth0.jwt.JWTVerifier;
import com.auth0.jwt.algorithms.Algorithm;
import com.auth0.jwt.exceptions.JWTVerificationException;
import com.example.entity.Admin;
import com.example.exception.CustomException;
import com.example.service.AdminService;
import org.slf4j.Logger;
import org.slf4j.LoggerFactory;
import org.springframework.stereotype.Component;
import org.springframework.web.servlet.HandlerInterceptor;
import jakarta.annotation.Resource;
import jakarta.servlet.http.HttpServletRequest;
import jakarta.servlet.http.HttpServletResponse;
import jakarta.annotation.Nonnull;//@Nonnull 
/**
 * jwt拦截器
 */
@Component
public class JwtInterceptor implements HandlerInterceptor {
    private static final Logger log = LoggerFactory.getLogger(JwtInterceptor.class);
    @Resource
    private AdminService adminService;
    @Override
    public boolean preHandle(HttpServletRequest request, HttpServletResponse response, Object handler) {
        // 1. 从http请求的header中获取token
        String token = request.getHeader("token");
        if (StrUtil.isBlank(token)) {
            // 如果没拿到，我再去参数里面拿一波试试  /api/admin?token=xxxxx
            token = request.getParameter("token");
        }
        // 2. 开始执行认证
        if (StrUtil.isBlank(token)) {
            throw new CustomException("无token，请重新登录");
        }
        // 获取 token 中的userId
        String userId;
        Admin admin;
        try {
            userId = JWT.decode(token).getAudience().get(0);
            // 根据token中的userid查询数据库
            admin = adminService.findById(Integer.parseInt(userId));
        } catch (Exception e) {
            String errMsg = "token验证失败，请重新登录";
            log.error(errMsg + ", token=" + token, e);
            throw new CustomException(errMsg);
        }
        if (admin == null) {
            throw new CustomException("用户不存在，请重新登录");
        }
        try {
            // 用户密码加签验证 token
            JWTVerifier jwtVerifier = JWT.require(Algorithm.HMAC256(admin.getPassword())).build();
            jwtVerifier.verify(token); // 验证token
        } catch (JWTVerificationException e) {
            throw new CustomException("token验证失败，请重新登录");
        }
        log.info("token认证通过，放行");
        return true;
    }
}
```
#### 20250111 武哥毕设 7.*文件上传下载*
08手把手教Springboot+Vue实现文件上传和下载
##### (1)图书管理模块(后端框架)
【前端】
Layout.vue：
`<el-menu-item index="/book">`编辑路由index(图书信息)
BookView.vue：
新建src.views.BookView.vue
index.js：
引入页面BookView.vue(配置路由path、name、component)
【后端】
book.sql(数据库Navicat)：
新建表，勾选主键自增
字符集：utf8mb4
排序规则：utf8mb4_unicode_ci
Params.java：
private String name;
private String phone;
private String author;
private Integer PageNum;
private Integer PageSize;
生成getter&setter
Book.java：
`@Table(name = "book")`数据库表名
生成getter&setter
private Integer id;
private String name;
private String price;
private String author;
private String press;
private String img;
BookDao.java(Interface)(Interface)：
`@Repository`dao层
`public interface BookDao extends Mapper<Book>{}`
BookMapper.xml：
`<mapper namespace="com.example.dao.BookDao">`
BookService.java：
`@Service`service层
`@Resource`引入dao层(`private BookDao bookDao;`)
BookController.java：
`@CrossOrigin`跨域问题
`@RestController`controller层
`@RequestMapping("/book")`
`@Resource`引入service层(`private BookService bookService;`)
##### (2)图书管理增删改查
【后端】
查找
BookController.java：
`public class BookController{}`
`@GetMapping("/search")`
`public Result findBySearch(Params params){}`
`PageInfo<Book> info = bookService.findBySearch(params);`
BookService.java：
`public PageInfo<Book> findBySearch(Params params){}`
`PageHelper.startPage(params.getPageNum(), params.getPageSize());`分页查询
`List<Book> list = bookDao.findBySearch(params);`
BookDao.java(Interface)：
`public interface BookDao extends Mapper<Book>{}`
`List<Book> findBySearch(@Param("params")Params params);`
BookMapper.xml：
`<select id="findBySearch" resultType="com.example.entity.Book">`
基于mapper.xml查询数据库
增改
BookController.java：
`public class BookController{}`
`@PostMapping`
`public Result save(@RequestBody Book book){}`
`bookService.add(book);`
`bookService.update(book);`
BookService.java：
`public void add(Book book){}`
`bookDao.insertSelective(book);`基于tk.mybatis依赖新增
`public void update(Book book){}`
`bookDao.updateByPrimaryKeySelective(book);`基于tk.mybatis依赖更新
删除
BookController.java：
`public class BookController{}`
`@DeleteMapping("/{id}")`
`public Result delete(@PathVariable Integer id){}`
`bookService.delete(id);`
BookService.java：
`public void delete(Integer id){}`
`bookDao.deleteByPrimaryKey(id);`基于tk.mybatis依赖删除
##### (3)文件上传下载
【后端】
FileController.java：
新建com.example.controller.FileController.java
WebConfig.java：
`.excludePathPatterns("/api/files/**")`放行文件上传下载接口
【前端】
BookView.vue：
`<el-upload>` 引入上传图片组件
`action="http://localhost:8080/api/files/upload"` 调用文件上传接口
`:on-success="successUpload"` 绑定事件(上传文件成功后调用钩子函数)
method：`successUpload(res){}`“上传成功”
数据赋值`this.form.img = res.data;`(图片信息)
##### (4)图片文件预览下载
【前端】
BookView.vue：
`<el-image>` 引入图片组件
`:src="'http://localhost:8080/api/files/' + scope.row.img"` 下载地址
`:preview-src-list="['http://localhost:8080/api/files/' + scope.row.img]"` 图片预览
`<el-button>` 引入按钮组件
`<el-button type="primary" @click="down(scope.row.img)">` 绑定事件(下载图片文件)
method：`down(flag){}`“下载”
下载地址`location.href = 'http://localhost:8080/api/files/' + flag`
##### 前端：Layout.vue
```js
<template>
  <div>
    <el-container>
      <el-header style="background-color: #4c535a">
        <img src="@/assets/logo.png" alt="" style="width: 40px; position: relative; top: 10px;">
        <span style="font-size: 20px; margin-left: 15px; color: white">手拉手带小白做毕设</span>
        <el-dropdown style="float: right; height: 60px; line-height: 60px">
          <span class="el-dropdown-link" style="color: white; font-size: 16px">{{ user.name }}<i class="el-icon-arrow-down el-icon--right"></i></span>
          <el-dropdown-menu slot="dropdown">
            <el-dropdown-item>
              <div @click="logout">退出</div>
            </el-dropdown-item>
          </el-dropdown-menu>
        </el-dropdown>
      </el-header>
    </el-container>
    <el-container>
      <el-aside style="overflow: hidden; min-height: 100vh; background-color: #545c64; width: 250px">
        <el-menu :default-active="$route.path" router background-color="#545c64" text-color="#fff" active-text-color="#ffd04b">
          <el-menu-item index="/">
            <i class="el-icon-s-home"></i>
            <span slot="title">系统首页</span>
          </el-menu-item>
          <el-submenu index="2">
            <template slot="title">
              <i class="el-icon-location"></i><span>用户管理</span>
            </template>
            <el-menu-item-group>
              <el-menu-item index="/admin">管理员信息</el-menu-item>
              <el-menu-item index="2-2">用户信息</el-menu-item>
            </el-menu-item-group>
          </el-submenu>
          <el-submenu index="3">
            <template slot="title">
              <i class="el-icon-location"></i><span>信息管理</span>
            </template>
            <el-menu-item-group>
              <el-menu-item index="/book">图书信息</el-menu-item>
              <el-menu-item index="3-2">yyy信息</el-menu-item>
            </el-menu-item-group>
          </el-submenu>
        </el-menu>
      </el-aside>
      <el-main>
        <router-view/>
      </el-main>
    </el-container>
  </div>
</template>

<style>
.el-menu{
  border-right: none !important;
}
</style>

<script>
export default {
  name: "Layout",

  data() {
    return {
      // user: {
      //   name: ''
      // }
      user: localStorage.getItem("user") ? JSON.parse(localStorage.getItem("user")) : {}
    }
  },
  // created() {
  //   this.user = JSON.parse(localStorage.getItem('user'))
  // },
  methods: {
    logout() {
      localStorage.removeItem('user')
      this.$router.push('/login')
    }
  }
}
</script>

<style>
.el-menu{
  border-right: none !important;
}
</style>
```
##### 前端：BookView.vue
```js
<template>
  <div>
    <div>
      <el-input v-model="params.name" style="width: 200px; margin-right: 10px" placeholder="请输入图书名称"></el-input>
      <el-input v-model="params.author" style="width: 200px; margin-right: 10px" placeholder="请输入图书作者"></el-input>
      <el-button type="warning" @click="findBySearch()">查询</el-button>
      <el-button type="primary" @click="reset()">清空</el-button>
      <el-button type="primary" @click="add()">新增</el-button>
    </div>
    <div>
      <el-table :data="tableData" style="width: 100%; margin: 15px 0px">
        <el-table-column label="图书封面" width="180">
          <template v-slot="scope">
            <el-image
                style="width: 70px; height: 70px; border-radius: 50%"
                :src="'http://localhost:8080/api/files/' + scope.row.img"
                :preview-src-list="['http://localhost:8080/api/files/' + scope.row.img]">
            </el-image>
          </template>
        </el-table-column>
        <el-table-column prop="name" label="图书姓名" width="180"></el-table-column>
        <el-table-column prop="author" label="图书作者" width="180"></el-table-column>
        <el-table-column prop="price" label="图书价格" width="180"></el-table-column>
        <el-table-column prop="press" label="图书出版社" width="180"></el-table-column>
        <el-table-column label="操作">
          <template slot-scope="scope">
            <el-button type="primary" @click="edit(scope.row)">编辑</el-button>
            <el-button type="primary" @click="down(scope.row.img)">下载</el-button>
            <el-popconfirm title="确定删除吗？" @confirm="del(scope.row.id)">
              <el-button slot="reference" type="danger" style="margin-left: 5px">删除</el-button>
            </el-popconfirm>
          </template>
        </el-table-column>
      </el-table>
    </div>
    <div class="block">
      <el-pagination
          @size-change="handleSizeChange"
          @current-change="handleCurrentChange"
          :current-page="params.pageNum"
          :page-sizes="[5, 10, 15, 20]"
          :page-size="params.pageSize"
          layout="total, sizes, prev, pager, next"
          :total="total">
      </el-pagination>
    </div>
    <div>
      <el-dialog title="请填写姓名" :visible.sync="dialogFormVisible" width="30%">
        <el-form :model="form">
          <el-form-item label="图书名称" label-width="25%">
            <el-input v-model="form.name" autocomplete="off" style="width:90%"></el-input>
          </el-form-item>
          <el-form-item label="图书封面" label-width="25%">
            <el-upload action="http://localhost:8080/api/files/upload" :on-success="successUpload">
              <el-button size="small" type="primary">点击上传</el-button>
            </el-upload>
          </el-form-item>
          <el-form-item label="图书作者" label-width="25%">
            <el-input v-model="form.author" autocomplete="off" style="width:90%"></el-input>
          </el-form-item>
          <el-form-item label="图书价格" label-width="25%">
            <el-input v-model="form.price" autocomplete="off" style="width:90%"></el-input>
          </el-form-item>
          <el-form-item label="图书出版社" label-width="25%">
            <el-input v-model="form.press" autocomplete="off" style="width:90%"></el-input>
          </el-form-item>
        </el-form>
        <div slot="footer" class="dialog-footer">
          <el-button @click="dialogFormVisible = false">取 消</el-button>
          <el-button type="primary" @click="submit()">确 定</el-button>
        </div>
      </el-dialog>
    </div>
  </div>
</template>
<script>
import request from "@/utils/request";
export default {
  //name: "BookView",
  data() {
    return {
      params:{
        name: '',
        author: '',
        //price: '',
        //press: '',
        //img: '',
        pageNum: 1,
        pageSize: 5
      },
      tableData: [],
      total: 0,
      dialogFormVisible: false,
      form: {}
    }
  },
  created() {
    this.findBySearch();
  },
  methods: {
    findBySearch(){
      request.get("/book/search",{
        params:this.params}
      ).then(res =>{
        if(res.code === '0'){
          this.tableData = res.data.list;
          this.total = res.data.total;
        }else{
          this.$message.error(res.msg);
        }
      })
    },
    reset(){
      this.params = {
        pageNum: 1,
        pageSize: 5,
        name: '',
        phone: ''
      }
      this.findBySearch();
    },
    handleSizeChange(pageSize) {
      this.params.pageSize = pageSize;
      this.findBySearch();
    },
    handleCurrentChange(pageNum) {
      this.params.pageNum = pageNum;
      this.findBySearch();
    },
    add(){
      this.form = {};
      this.dialogFormVisible = true;
    },
    edit(obj) {
      this.form = obj;
      this.dialogFormVisible = true;
    },
    submit(){
      request.post("/book", this.form).then(res => {
        if (res.code === '0') {
          this.$message.success("操作成功");
          this.dialogFormVisible = false;
          this.findBySearch();
        } else {
          this.$message.error(res.msg);
        }
      })
    },
    del(id) {
      request.delete("/book/" + id).then(res => {
        if (res.code === '0') {
          this.$message.success("删除成功");
          this.findBySearch();
        } else {
          this.$message.error(res.msg);
        }
      })
    },
    successUpload(res) {
      this.form.img = res.data;
    },
    down(flag) {
      location.href = 'http://localhost:8080/api/files/' + flag
    }
  }
}
</script>
```
##### 前端：index.js
```js
const routes = [
  {
    path: '/register',
    name: 'Register',
    component: RegisterView
  },
  {
    path: '/login',
    name: 'Login',
    component: LoginView
  },
  {
    path: '/',
    name: 'Layout',
    component: Layout,
    //redirect: '/home',
    children: [ // 子路由
      {
        path: '',
        name: 'home',
        component: HomeView
      },
      {
        path: 'admin',
        name: 'admin',
        component: () => import('../views/AdminView.vue')
      },
      {
        path: 'book',
        name: 'book',
        component: BookView
      }
    ]
  },
]
```
##### 后端：BookController.java
```java
package com.example.controller;
import com.example.common.Result;
import com.example.entity.Book;
import com.example.entity.Params;
import com.example.service.BookService;
import com.github.pagehelper.PageInfo;
import jakarta.annotation.Resource;
import org.springframework.web.bind.annotation.*;
@CrossOrigin
@RestController
@RequestMapping("/book")
public class BookController {
    @Resource
    private BookService bookService;
    @GetMapping("/search")
    public Result findBySearch(Params params) {
        PageInfo<Book> info = bookService.findBySearch(params);
        return Result.success(info);
    }
    @PostMapping
    public Result save(@RequestBody Book book) {
        //adminService.add(admin);
        if (book.getId() == null) {
            bookService.add(book);
        } else {
            bookService.update(book);
        }
        return Result.success();
    }
    @DeleteMapping("/{id}")
    public Result delete(@PathVariable Integer id) {
        bookService.delete(id);
        return Result.success();
    }
}
```
##### 后端：FileController.java
```java
package com.example.controller;
import cn.hutool.core.io.FileUtil;
import cn.hutool.core.util.StrUtil;
import com.example.common.Result;
import org.springframework.web.bind.annotation.*;
import org.springframework.web.multipart.MultipartFile;
import jakarta.servlet.http.HttpServletResponse;
import java.io.OutputStream;
import java.net.URLEncoder;
import java.util.List;

/**
 *  文件上传接口
 */
@RestController
@RequestMapping("/files")
public class FileController {
    // 文件上传存储路径
    private static final String filePath = System.getProperty("user.dir") + "/file/";
    /**
     * 文件上传
     */
    @PostMapping("/upload")
    public Result upload(MultipartFile file) {
        synchronized (FileController.class) {
            // 获取时间戳 时间戳作为文件名
            String flag = System.currentTimeMillis() + "";
            // 获取文件名
            String fileName = file.getOriginalFilename();
            try {
                // 判断文件路径是否存在，不存在则创建
                if (!FileUtil.isDirectory(filePath)) {
                    FileUtil.mkdir(filePath);
                }
                // 文件存储形式：时间戳-文件名
                FileUtil.writeBytes(file.getBytes(), filePath + flag + "-" + fileName);
                System.out.println(fileName + "--上传成功");
                Thread.sleep(1L);
            } catch (Exception e) {
                System.err.println(fileName + "--文件上传失败");
            }
            return Result.success(flag);
        }
    }
    /**
     * 获取文件
     */
    @GetMapping("/{flag}")
    public void avatarPath(@PathVariable String flag, HttpServletResponse response) {
        if (!FileUtil.isDirectory(filePath)) {
            FileUtil.mkdir(filePath);
        }
        OutputStream os;
        List<String> fileNames = FileUtil.listFileNames(filePath);
        String avatar = fileNames.stream().filter(name -> name.contains(flag)).findAny().orElse("");
        try {
            if (StrUtil.isNotEmpty(avatar)) {
                response.addHeader("Content-Disposition", "attachment;filename=" + URLEncoder.encode(avatar, "UTF-8"));
                response.setContentType("application/octet-stream");
                byte[] bytes = FileUtil.readBytes(filePath + avatar);
                os = response.getOutputStream();
                os.write(bytes);
                os.flush();
                os.close();
            }
        } catch (Exception e) {
            System.out.println("文件下载失败");
        }
    }
}
```
##### 后端：BookService.java
```java
package com.example.service;
import com.example.dao.BookDao;
import com.example.entity.Book;
import com.example.entity.Params;
import com.github.pagehelper.PageHelper;
import com.github.pagehelper.PageInfo;
import jakarta.annotation.Resource;
import org.springframework.stereotype.Service;
import java.util.List;
@Service
public class BookService {
    @Resource
    private BookDao bookDao;
    public void add(Book book) {
        bookDao.insertSelective(book);
    }
    public PageInfo<Book> findBySearch(Params params) {
        // 开启分页查询
        PageHelper.startPage(params.getPageNum(), params.getPageSize());
        // 接下来的查询会自动按照当前开启的分页设置来查询
        //return adminDao.findBySearch(params);
        List<Book> list = bookDao.findBySearch(params);
        return PageInfo.of(list);
    }
    public void update(Book book) {
        bookDao.updateByPrimaryKeySelective(book);
    }
    public void delete(Integer id) {
        bookDao.deleteByPrimaryKey(id);
    }
}
```
##### 后端：BookDao.java(Interface)
```java
package com.example.dao;
import com.example.entity.Book;
import com.example.entity.Params;
import org.apache.ibatis.annotations.Param;
import org.springframework.stereotype.Repository;
import tk.mybatis.mapper.common.Mapper;
import java.util.List;
@Repository
public interface BookDao extends Mapper<Book> {
    List<Book> findBySearch(@Param("params")Params params);
}
```
##### 后端：BookMapper.xml
```xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE mapper PUBLIC "-//mybatis.org//DTD Mapper 3.0//EN" "http://mybatis.org/dtd/mybatis-3-mapper.dtd">
<mapper namespace="com.example.dao.BookDao">
    <select id="findBySearch" resultType="com.example.entity.Book">
        select * from book
        <where>
            <if test="params != null and params.name != null and params.name != ''">
                and name like concat('%', #{ params.name }, '%')
            </if>
            <if test="params != null and params.author != null and params.author != ''">
                and author like concat('%', #{ params.author }, '%')
            </if>
        </where>
    </select>
</mapper>
```
##### 后端：Params.java
```java
public class Params {
    private String name;
    private String phone;
    private String author;
    private Integer PageNum;
    private Integer PageSize;
}
```
##### 后端：Book.java
```java
@Table(name = "book")
public class Book {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Integer id;
    @Column(name = "name")
    private String name;
    @Column(name = "price")
    private String price;
    @Column(name = "author")
    private String author;
    @Column(name = "press")
    private String press;
    @Column(name = "img")
    private String img;
}
```
##### 后端：WebConfig.java
```java
package com.example.common;

import org.springframework.context.annotation.Configuration;
import org.springframework.web.bind.annotation.RestController;
import org.springframework.web.servlet.config.annotation.InterceptorRegistry;
import org.springframework.web.servlet.config.annotation.PathMatchConfigurer;
import org.springframework.web.servlet.config.annotation.WebMvcConfigurer;

import jakarta.annotation.Resource;

@Configuration
public class WebConfig implements  WebMvcConfigurer {
    @Resource
    private JwtInterceptor jwtInterceptor;
    @Override
    public void configurePathMatch(PathMatchConfigurer configurer) {
        // 指定controller统一的接口前缀
        configurer.addPathPrefix("/api", clazz -> clazz.isAnnotationPresent(RestController.class));
    }
    // 加自定义拦截器JwtInterceptor，设置拦截规则
    @Override
    public void addInterceptors(InterceptorRegistry registry) {
        registry.addInterceptor(jwtInterceptor).addPathPatterns("/api/**")
                .excludePathPatterns("/api/files/**")
                .excludePathPatterns("/api/admin/login")
                .excludePathPatterns("/api/admin/register");
    }
}
```
##### 数据库：book.sql
```sql
CREATE TABLE `book` (
  `id` int(10) NOT NULL AUTO_INCREMENT COMMENT '主键ID',
  `name` varchar(255) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci DEFAULT NULL COMMENT '图书名称',
  `price` varchar(255) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci DEFAULT NULL COMMENT '图书价格',
  `author` varchar(255) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci DEFAULT NULL COMMENT '图书作者',
  `press` varchar(255) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci DEFAULT NULL COMMENT '图书出版社',
  `img` varchar(255) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci DEFAULT NULL COMMENT '图书封面',
  PRIMARY KEY (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_unicode_ci;
```
#### 20250131 武哥毕设 8.*批量删除*
09Springboot+Vue快速实现批量删除功能
##### (1)图书分类模块(后端框架)
【前端】
Layout.vue：
`<el-menu-item index="/type">`编辑路由index(图书分类)
TypeView.vue：
新建src.views.TypeView.vue
index.js：
引入页面TypeView.vue(配置路由path、name、component)
【后端】(type.sql->Type.java->TypeDao.java(Interface)->TypeMapper.xml->TypeService.java->TypeController.java)
type.sql(数据库Navicat)：
新建表，勾选主键自增
字符集：utf8mb4
排序规则：utf8mb4_unicode_ci
Type.java：
新建com.example.entity.Type.java
`@Table(name = "type")`数据库表名
生成getter&setter
private Integer id;
private String name;
private String description;
TypeDao.java(Interface)：
`public interface BookDao extends Mapper<Type>{}`
TypeMapper.xml：
`<mapper namespace="com.example.dao.TypeDao">`
TypeService.java：
`@Service`service层
`@Resource`引入dao层(`private TypeDao typeDao;`)
TypeController.java：
`@CrossOrigin`跨域问题
`@RestController`controller层
`@RequestMapping("/type")`
`@Resource`引入service层(`private TypeService typeService;`)
##### (2)图书分类增删改查
【前端】
TypeView.vue：
`<el-popconfirm>` 引入气泡确认框组件
`<el-popconfirm @confirm="delBatch()">` 绑定事件“批量删除”
`<el-table>` 引入表单组件
`<el-table-column>` 引入表单组件(Checkbox勾选框)
`<el-table @selection-change="handleSelectionChange">` 绑定事件(“选中表单行”)
`<el-table :row-key="getRowKeys">` 绑定事件(“跨页选中表单行”)
data：`multipleSelection: []` 多选框变量
method：`handleSelectionChange(val){}`
传递参数：`this.multipleSelection = val;`
method：`delBatch(id){}`
判断勾选`if (this.multipleSelection.length === 0){}`
消息提示`this.$message.warning("请勾选您要删除的项")`
发送请求`request.put("/type/delBatch", this.multipleSelection)` 传递参数
处理请求`.then(res => {处理请求})`
判断成功`if(res.code === '0'){}else{判断失败}`
消息提示`this.$message({message: '批量删除成功',type: 'success'});`
重载查询`this.findBySearch();`
消息提示`this.$message({message: res.msg,type: 'error'});`后端异常处理
method：`getRowKeys(row){}`
返回主键`return row.id;`
【后端】
增改
TypeController.java：
`public class TypeController{}`
`@PostMapping`
`public Result save(@RequestBody Type type){}`
`typeService.add(type);`
`typeService.update(type);`
TypeService.java：
`public void add(Type type){}`
`typeDao.insertSelective(type);`基于tk.mybatis依赖新增
`public void update(Type type){}`
`typeDao.updateByPrimaryKeySelective(type);`基于tk.mybatis依赖更新
查找
TypeController.java：
`public class TypeController{}`
`@GetMapping("/search")`
`public Result findBySearch(Params params){}`
`PageInfo<Type> info = typeService.findBySearch(params);`
TypeService.java：
`public PageInfo<Type> findBySearch(Params params){}`
`PageHelper.startPage(params.getPageNum(), params.getPageSize());`分页查询
`List<Type> list = typeDao.findBySearch(params);`
TypeDao.java(Interface)：
`public interface TypeDao extends Mapper<Type>{}`
`List<Type> findBySearch(@Param("params")Params params);`
TypeMapper.xml：
`<select id="findBySearch" resultType="com.example.entity.Type">`
基于mapper.xml查询数据库
删除
TypeController.java：
`public class TypeController{}`
`@DeleteMapping("/{id}")`
`public Result delete(@PathVariable Integer id){}`
`typeService.delete(id);`
TypeService.java：
`public void delete(Integer id){}`
`typeDao.deleteByPrimaryKey(id);`基于tk.mybatis依赖删除
批量删除
TypeController.java：
`public class TypeController{}`
`@PutMapping("/delBatch")`
`public Result delBatch(@RequestBody List<Type> list){}`
`for (Type type : list){}`遍历
`typeService.delete(type.getId());`删除
`return Result.success();`删除成功
##### 前端：TypeView.vue
```js
<template>
  <div>
    <div>
      <el-input v-model="params.name" style="width: 200px; margin-right: 10px" placeholder="请输入分类名称"></el-input>
      <el-button type="warning" @click="findBySearch()">搜索</el-button>
      <el-button type="primary" @click="reset()">清空</el-button>
      <el-button type="primary" @click="add()">新增</el-button>
      <el-popconfirm title="确定这些数据删除吗？" @confirm="delBatch()">
        <el-button slot="reference" type="danger" style="margin-left: 5px">批量删除</el-button>
      </el-popconfirm>
    </div>
    <div>
      <el-table :data="tableData" style="width: 100%" ref="table" @selection-change="handleSelectionChange":row-key="getRowKeys">
        <el-table-column type="selection" width="55" align="center" :reserve-selection="true"></el-table-column>
        <el-table-column prop="name" label="分类名称" width="180"></el-table-column>
        <el-table-column prop="description" label="分类描述" width="180"></el-table-column>
        <el-table-column label="操作">
          <template slot-scope="scope">
            <el-button type="primary" @click="edit(scope.row)">编辑</el-button>
            <el-popconfirm title="确定删除吗？" @confirm="del(scope.row.id)">
              <el-button slot="reference" type="danger" style="margin-left: 5px">删除</el-button>
            </el-popconfirm>
          </template>
        </el-table-column>
      </el-table>
    </div>
    <div class="block">
      <el-pagination
          @size-change="handleSizeChange"
          @current-change="handleCurrentChange"
          :current-page="params.pageNum"
          :page-sizes="[5, 10, 15, 20]"
          :page-size="params.pageSize"
          layout="total, sizes, prev, pager, next"
          :total="total">
      </el-pagination>
    </div>
    <div>
      <el-dialog title="请填写姓名" :visible.sync="dialogFormVisible" width="30%">
        <el-form :model="form">
          <el-form-item label="分类名称" label-width="15%">
            <el-input v-model="form.name" autocomplete="off" style="width:90%"></el-input>
          </el-form-item>
          <el-form-item label="分类描述" label-width="15%">
            <el-input v-model="form.description" autocomplete="off" style="width:90%"></el-input>
          </el-form-item>
        </el-form>
        <div slot="footer" class="dialog-footer">
          <el-button @click="dialogFormVisible = false">取 消</el-button>
          <el-button type="primary" @click="submit()">确 定</el-button>
        </div>
      </el-dialog>
    </div>
  </div>
</template>
<script>
import request from "@/utils/request";
export default {
  //name: "AdminView",
  data() {
    return {
      params:{
        name: '',
        pageNum: 1,
        pageSize: 5
      },
      tableData: [],
      total: 0,
      dialogFormVisible: false,
      form: {},
      multipleSelection: []
    }
  },
  created() {
    this.findBySearch();
  },
  methods: {
    findBySearch(){
      request.get("/type/search",{
        params:this.params
      }).then(res =>{
        if(res.code === '0'){
          this.tableData = res.data.list;
          this.total = res.data.total;
        }else{
          this.$message({
            message: res.msg,
            type: 'error'
          });
        }
      })
    },
    reset(){
      this.params = {
        pageNum: 1,
        pageSize: 5,
        name: '',
      }
      this.findBySearch();
    },
    handleSizeChange(pageSize) {
      this.params.pageSize = pageSize;
      this.findBySearch();
    },
    handleCurrentChange(pageNum) {
      this.params.pageNum = pageNum;
      this.findBySearch();
    },
    add(){
      this.form = {};
      this.dialogFormVisible = true;
    },
    edit(obj) {
      this.form = obj;
      this.dialogFormVisible = true;
    },
    submit(){
      request.post("/type", this.form).then(res => {
        if (res.code === '0') {
          this.$message({
            message: '操作成功',
            type: 'success'
          });
          this.dialogFormVisible = false;
          this.findBySearch();
        } else {
          this.$message({
            message: res.msg,
            type: 'error'
          });
        }
      })
    },
    del(id) {
      request.delete("/type/" + id).then(res => {
        if (res.code === '0') {
          this.$message({
            message: '删除成功',
            type: 'success'
          });
          this.findBySearch();
        } else {
          this.$message({
            message: res.msg,
            type: 'success'
          });
        }
      })
    },
    delBatch() {
      if (this.multipleSelection.length === 0) {
        this.$message.warning("请勾选您要删除的项")
        return
      }
      request.put("/type/delBatch", this.multipleSelection).then(res => {
        if (res.code === '0') {
          this.$message.success("批量删除成功")
          this.findBySearch()
        } else {
          this.$message.error(res.msg)
        }
      })
    },
    handleSelectionChange(val) {
      this.multipleSelection = val;
    },
    getRowKeys(row) {
      return row.id;
    }
  }
}
</script>
```
##### 前端：index.js
```js
const routes = [
  {
    path: '/register',
    name: 'Register',
    component: RegisterView
  },
  {
    path: '/login',
    name: 'Login',
    component: LoginView
  },
  {
    path: '/',
    name: 'Layout',
    component: Layout,
    //redirect: '/home',
    children: [ // 子路由
      {
        path: '',
        name: 'home',
        component: HomeView
      },
      {
        path: 'admin',
        name: 'admin',
        component: () => import('../views/AdminView.vue')
      },
      {
        path: 'book',
        name: 'book',
        component: BookView
      },
      {
        path: 'type',
        name: 'type',
        component: TypeView
      }
    ]
  },
]
```
##### 后端：TypeController.java
```java
package com.example.controller;
import com.example.common.Result;
import com.example.entity.Params;
import com.example.entity.Type;
import com.example.service.TypeService;
import com.github.pagehelper.PageInfo;
import jakarta.annotation.Resource;
import org.springframework.web.bind.annotation.*;
import java.util.List;
@CrossOrigin
@RestController
@RequestMapping("/type")
public class TypeController {
    @Resource
    private TypeService typeService;

    @PostMapping
    public Result save(@RequestBody Type type) {
        if (type.getId() == null) {
            typeService.add(type);
        } else {
            typeService.update(type);
        }
        return Result.success();
    }
    @GetMapping("/search")
    public Result findBySearch(Params params) {
        PageInfo<Type> info = typeService.findBySearch(params);
        return Result.success(info);
    }
    @DeleteMapping("/{id}")
    public Result delete(@PathVariable Integer id) {
        typeService.delete(id);
        return Result.success();
    }
    @PutMapping("/delBatch")
    public Result delBatch(@RequestBody List<Type> list) {
        for (Type type : list) {
            typeService.delete(type.getId());
        }
        return Result.success();
    }
}
```
##### 后端：TypeService.java
```java
package com.example.service;
import com.example.dao.TypeDao;
import com.example.entity.Params;
import com.example.entity.Type;
import com.github.pagehelper.PageHelper;
import com.github.pagehelper.PageInfo;
import jakarta.annotation.Resource;
import org.springframework.stereotype.Service;
import java.util.List;
@Service
public class TypeService {
    @Resource
    private TypeDao typeDao;

    public void add(Type type) {
        typeDao.insertSelective(type);
    }

    public void update(Type type) {
        typeDao.updateByPrimaryKeySelective(type);
    }

    public PageInfo<Type> findBySearch(Params params) {
        // 开启分页查询
        PageHelper.startPage(params.getPageNum(), params.getPageSize());
        // 接下来的查询会自动按照当前开启的分页设置来查询
        List<Type> list = typeDao.findBySearch(params);
        return PageInfo.of(list);
    }

    public void delete(Integer id) {
        typeDao.deleteByPrimaryKey(id);
    }
}
```
##### 后端：TypeDao.java(Interface)
```java
@Repository
public interface TypeDao extends Mapper<Type> {
    List<Type> findBySearch(@Param("params")Params params);
}
```
##### 后端：TypeMapper.xml
```xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE mapper PUBLIC "-//mybatis.org//DTD Mapper 3.0//EN" "http://mybatis.org/dtd/mybatis-3-mapper.dtd">
<mapper namespace="com.example.dao.TypeDao">
    <select id="findBySearch" resultType="com.example.entity.Type">
        select * from type
        <where>
            <if test="params != null and params.name != null and params.name != ''">
                and name like concat('%', #{ params.name }, '%')
            </if>
        </where>
    </select>
</mapper>
```
##### 后端：Type.java
```java
@Table(name = "type")
public class Type {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Integer id;
    @Column(name = "name")
    private String name;
    @Column(name = "description")
    private String description;
```
##### 数据库：type.sql
```sql
CREATE TABLE `type` (
  `id` int(10) NOT NULL AUTO_INCREMENT COMMENT '主键ID',
  `name` varchar(255) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci DEFAULT NULL COMMENT '分类名称',
  `description` varchar(255) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci DEFAULT NULL COMMENT '分类介绍',
  PRIMARY KEY (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=8 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_unicode_ci COMMENT='图书分类表';
```
#### 20250131 武哥毕设 9.*批量导入导出*
10Springboot+Vue实现批量导入excel、批量导出excel
##### (1)批量导出
【前端】
TypeView.vue：
`<el-button>` 引入按钮组件
`<el-button @click="exp()">` 绑定事件“导出报表”
method：`exp(){}`
`let user = localStorage.getItem("user");` 获取token
`location.href = 'http://localhost:8080/api/type/export?token=' + JSON.parse(user).token` 拼接token
【后端】
pom.xml：
`<artifactId>poi-ooxml</artifactId>`poi-ooxml依赖
TypeController.java：
`public class TypeController{}`
`@GetMapping("/export")`
`public Result export(HttpServletResponse response){}`
`public Result export(HttpServletResponse response) throws IOException{}`
`List<Type> all = typeService.findAll();` 1. 从数据库中查询出所有数据
`if (CollectionUtil.isEmpty(all)) {}`(hutool工具)
`throw new CustomException("未找到数据");`
`List<Map<String, Object>> list = new ArrayList<>(all.size());` 2. 定义一个 List，存储处理之后的数据，用于塞到 list 里
TypeService.java：
`public List<Type> findAll(){}`
`return typeDao.selectAll();`基于tk.mybatis查询所有
##### (2)批量导入
【前端】
TypeView.vue：
`<el-upload>`  引入批量上传组件
`<el-upload :on-success="successUpload">` 绑定事件“批量导入”
`<el-upload action="http://localhost:8080/api/type/upload">` 导入地址
`<el-upload :show-file-list="false">` 不显示已上传文件列表
method：`successUpload(res){}`
判断成功`if(res.code === '0'){}else{判断失败}`
消息提示`this.$message.success("批量导入成功")`
重载查询`this.findBySearch();`
消息提示`this.$message.error(res.msg)`后端异常处理
【后端】
TypeController.java：
`public class TypeController{}`
`@PostMapping("/upload")`
`public Result upload(MultipartFile file) throws IOException {}`
`List<Type> infoList = ExcelUtil.getReader(file.getInputStream()).readAll(Type.class);`
Type.java：
`@Alias("分类名称")` 映射表格字段
`@Alias("分类描述")` 映射表格字段
WebConfig.java：
`.excludePathPatterns("/api/type/upload")` 放行批量导入接口
##### 前端：TypeView.vue
```js
<template>
  <div>
    <div>
      <el-input v-model="params.name" style="width: 200px; margin-right: 10px" placeholder="请输入分类名称"></el-input>
      <el-button type="warning" @click="findBySearch()">搜索</el-button>
      <el-button type="primary" @click="reset()">清空</el-button>
      <el-button type="primary" @click="add()">新增</el-button>
      <el-popconfirm title="确定这些数据删除吗？" @confirm="delBatch()">
        <el-button slot="reference" type="danger" style="margin-left: 5px">批量删除</el-button>
      </el-popconfirm>
      <el-button type="success" style="margin-left: 10px" @click="exp()">导出报表</el-button>
      <el-upload action="http://localhost:8080/api/type/upload" style="display: inline-block; margin-left: 10px" :show-file-list="false" :on-success="successUpload">
        <el-button size="small" type="primary">批量导入</el-button>
      </el-upload>
    </div>
    <div>
      <el-table :data="tableData" style="width: 100%" ref="table" @selection-change="handleSelectionChange" :row-key="getRowKeys">
        <el-table-column type="selection" width="55" align="center" :reserve-selection="true"></el-table-column>
        <el-table-column prop="name" label="分类名称" width="180"></el-table-column>
        <el-table-column prop="description" label="分类描述" width="180"></el-table-column>
        <el-table-column label="操作">
          <template slot-scope="scope">
            <el-button type="primary" @click="edit(scope.row)">编辑</el-button>
            <el-popconfirm title="确定删除吗？" @confirm="del(scope.row.id)">
              <el-button slot="reference" type="danger" style="margin-left: 5px">删除</el-button>
            </el-popconfirm>
          </template>
        </el-table-column>
      </el-table>
    </div>
    <div class="block">
      <el-pagination
          @size-change="handleSizeChange"
          @current-change="handleCurrentChange"
          :current-page="params.pageNum"
          :page-sizes="[5, 10, 15, 20]"
          :page-size="params.pageSize"
          layout="total, sizes, prev, pager, next"
          :total="total">
      </el-pagination>
    </div>
    <div>
      <el-dialog title="请填写姓名" :visible.sync="dialogFormVisible" width="30%">
        <el-form :model="form">
          <el-form-item label="分类名称" label-width="15%">
            <el-input v-model="form.name" autocomplete="off" style="width:90%"></el-input>
          </el-form-item>
          <el-form-item label="分类描述" label-width="15%">
            <el-input v-model="form.description" autocomplete="off" style="width:90%"></el-input>
          </el-form-item>
        </el-form>
        <div slot="footer" class="dialog-footer">
          <el-button @click="dialogFormVisible = false">取 消</el-button>
          <el-button type="primary" @click="submit()">确 定</el-button>
        </div>
      </el-dialog>
    </div>
  </div>
</template>
<script>
import request from "@/utils/request";
export default {
  //name: "AdminView",
  data() {
    return {
      params:{
        name: '',
        pageNum: 1,
        pageSize: 5
      },
      tableData: [],
      total: 0,
      dialogFormVisible: false,
      form: {},
      multipleSelection: []
    }
  },
  created() {
    this.findBySearch();
  },
  methods: {
    findBySearch(){
      request.get("/type/search",{
        params:this.params
      }).then(res =>{
        if(res.code === '0'){
          this.tableData = res.data.list;
          this.total = res.data.total;
        }else{
          this.$message({
            message: res.msg,
            type: 'error'
          });
        }
      })
    },
    reset(){
      this.params = {
        pageNum: 1,
        pageSize: 5,
        name: '',
      }
      this.findBySearch();
    },
    handleSizeChange(pageSize) {
      this.params.pageSize = pageSize;
      this.findBySearch();
    },
    handleCurrentChange(pageNum) {
      this.params.pageNum = pageNum;
      this.findBySearch();
    },
    add(){
      this.form = {};
      this.dialogFormVisible = true;
    },
    edit(obj) {
      this.form = obj;
      this.dialogFormVisible = true;
    },
    submit(){
      request.post("/type", this.form).then(res => {
        if (res.code === '0') {
          this.$message({
            message: '操作成功',
            type: 'success'
          });
          this.dialogFormVisible = false;
          this.findBySearch();
        } else {
          this.$message({
            message: res.msg,
            type: 'error'
          });
        }
      })
    },
    del(id) {
      request.delete("/type/" + id).then(res => {
        if (res.code === '0') {
          this.$message({
            message: '删除成功',
            type: 'success'
          });
          this.findBySearch();
        } else {
          this.$message({
            message: res.msg,
            type: 'success'
          });
        }
      })
    },
    delBatch() {
      if (this.multipleSelection.length === 0) {
        this.$message.warning("请勾选您要删除的项")
        return
      }
      request.put("/type/delBatch", this.multipleSelection).then(res => {
        if (res.code === '0') {
          this.$message.success("批量删除成功")
          this.findBySearch()
        } else {
          this.$message.error(res.msg)
        }
      })
    },
    handleSelectionChange(val) {
      this.multipleSelection = val;
    },
    getRowKeys(row) {
      return row.id;
    },
    exp() {
      let user = localStorage.getItem("user");
      location.href = 'http://localhost:8080/api/type/export?token=' + JSON.parse(user).token
    },
    successUpload(res) {
      if (res.code === '0') {
        this.$message.success("批量导入成功")
        this.findBySearch()
      } else {
        this.$message.error(res.msg)
      }
    }
  }
}
</script>
```
##### 后端：pom.xml
```xml
<dependency>
	<groupId>org.apache.poi</groupId>
	<artifactId>poi-ooxml</artifactId>
	<version>4.1.2</version>
</dependency>
```
##### 后端：TypeController.java
```java
@PostMapping("/upload")
public Result upload(MultipartFile file) throws IOException {
    List<Type> infoList = ExcelUtil.getReader(file.getInputStream()).readAll(Type.class);
    if (!CollectionUtil.isEmpty(infoList)) {
        for (Type type : infoList) {
            try {
                typeService.add(type);
            } catch (Exception e) {
                e.printStackTrace();
            }
        }
    }
    return Result.success();
}
```
##### 后端：TypeService.java
```java
public List<Type> findAll() {
        return typeDao.selectAll();
    }
```
##### 后端：Type.java
```java
@Table(name = "type")
public class Type {
  @Id
  @GeneratedValue(strategy = GenerationType.IDENTITY)
  private Integer id;

  @Alias("分类名称")
  @Column(name = "name")
  private String name;

  @Alias("分类描述")
  @Column(name = "description")
  private String description;
}
```
##### 后端：WebConfig.java
```java
@Override
    public void addInterceptors(InterceptorRegistry registry) {
        registry.addInterceptor(jwtInterceptor).addPathPatterns("/api/**")
                .excludePathPatterns("/api/files/**")
                .excludePathPatterns("/api/type/upload")
                .excludePathPatterns("/api/admin/login")
                .excludePathPatterns("/api/admin/register");
    }
```
#### 20250201 武哥毕设 10.*模块关联*
11Springboot+Vue实现模块之间的关联功能
##### (1)模块关联(显示typeId)
【前端】
BookView.vue：
`<el-table>` 引入表单组件
`<el-table-column prop="typeId" label="图书分类">` 引入表单组件“图书分类”
`<el-dialog>` 引入对话框组件
`<el-form-item>` 引入对话框组件“图书分类”
`<el-select>` 引入选择器组件
`<el-select v-model="form.typeId">` 绑定参数(传给后台的ID)
`<el-option>` 引入选择器组件“下拉选项”
`<el-option v-for="item in typeObjs">` 选择器组件 遍历“下拉选项”
`<el-option :key="item.id">` 选择器组件“下拉选项” (属性ID)
`<el-option :label="item.name">` 选择器组件“下拉选项” (页面显示的文字内容)
`<el-option :value="item.id">` 选择器组件“下拉选项” (传给后台的ID)
data：`typeObjs: []` 分类信息变量
create：`this.findTypes();` 页面加载时调用
method：`findTypes(){}`“查询分类信息”
发送请求`request.get("/type")`
处理请求`.then(res => {处理请求})`
判断成功`if(res.code === '0'){}else{判断失败}`
数据赋值`this.typeObjs = res.data;`
消息提示`this.$message.error(res.msg)`后端异常处理
【后端】
book.sql：
在"图书信息表"中新建字段(typeId)，关联"图书分类表"
Book.java：
`@Column(name = "typeId")` 关联数据库表字段
`private Integer typeId;` 定义变量typeId
生成getter&setter
TypeController.java：
`public class TypeController{}`
`@GetMapping`
`public Result findAll(){}`
`return Result.success(typeService.findAll());` 查询所有
TypeService.java：
`public List<Type> findAll(){}`
`return typeDao.selectAll();`基于tk.mybatis查询所有
##### (2)模块关联(显示typeName) 通过sql语句(left join查询)
【前端】
BookView.vue：
`<el-table>` 引入表单组件
`<el-table-column prop="typeName" label="图书分类" width="180">` 引入表单组件“图书分类”
【后端】
Book.java：
`@Transient`非数据库字段
`private String typeName;`定义变量typeName
生成getter&setter
新建查询.sql：
`select book.*, type.name AS typeName from book left join type on book.typeId =type.id order by book.id acs`
BookMapper.xml：
`<select id="findBySearch" resultType="com.example.entity.Book">`
`select book.*, type.name AS typeName from book left join type on book.typeId =type.id` (typeName对应实体类字段)
`order by book.id acs`
##### (3)模块关联(显示typeName) 通过java逻辑(BookService查询)
【前端】
BookView.vue：
`<el-table>` 引入表单组件
`<el-table-column prop="typeName" label="图书分类" width="180">` 引入表单组件“图书分类”
【后端】
Book.java：
`@Transient`非数据库字段
`private String typeName;`定义变量typeName
生成getter&setter
BookMapper.xml：
`<select id="findBySearch" resultType="com.example.entity.Book">`
`select * from book`
`order by book.id acs`
BookService.java：
`@Resource`
`private TypeDao typeDao;`
`public PageInfo<Book> findBySearch(Params params){}`
`if (CollectionUtil.isEmpty(list)){}`判空
`return PageInfo.of(new ArrayList<>());`如果list空返回空list
`for (Book book : list){}` 遍历数组
`if (ObjectUtil.isNotEmpty(book.getTypeId())){}` 判断图书ID不为空
`Type type = typeDao.selectByPrimaryKey(book.getTypeId());` 根据图书ID查询分类信息
`if (ObjectUtil.isNotEmpty(type)){}` 判断分类信息不为空
`book.setTypeName(type.getName());`数据赋值
##### 前端：BookView.vue
```js
<template>
  <div>
    <div>
      <el-input v-model="params.name" style="width: 200px; margin-right: 10px" placeholder="请输入图书名称"></el-input>
      <el-input v-model="params.author" style="width: 200px; margin-right: 10px" placeholder="请输入图书作者"></el-input>
      <el-button type="warning" @click="findBySearch()">查询</el-button>
      <el-button type="primary" @click="reset()">清空</el-button>
      <el-button type="primary" @click="add()">新增</el-button>
    </div>
    <div>
      <el-table :data="tableData" style="width: 100%; margin: 15px 0px">
        <el-table-column label="图书封面" width="180">
          <template v-slot="scope">
            <el-image
                style="width: 70px; height: 70px; border-radius: 50%"
                :src="'http://localhost:8080/api/files/' + scope.row.img"
                :preview-src-list="['http://localhost:8080/api/files/' + scope.row.img]">
            </el-image>
          </template>
        </el-table-column>
        <el-table-column prop="name" label="图书姓名" width="180"></el-table-column>
        <el-table-column prop="author" label="图书作者" width="180"></el-table-column>
        <el-table-column prop="price" label="图书价格" width="180"></el-table-column>
        <el-table-column prop="press" label="图书出版社" width="180"></el-table-column>
        <el-table-column prop="typeName" label="图书分类" width="180"></el-table-column>
        <el-table-column label="操作">
          <template slot-scope="scope">
            <el-button type="primary" @click="edit(scope.row)">编辑</el-button>
            <el-button type="primary" @click="down(scope.row.img)">下载</el-button>
            <el-popconfirm title="确定删除吗？" @confirm="del(scope.row.id)">
              <el-button slot="reference" type="danger" style="margin-left: 5px">删除</el-button>
            </el-popconfirm>
          </template>
        </el-table-column>
      </el-table>
    </div>
    <div class="block">
      <el-pagination
          @size-change="handleSizeChange"
          @current-change="handleCurrentChange"
          :current-page="params.pageNum"
          :page-sizes="[5, 10, 15, 20]"
          :page-size="params.pageSize"
          layout="total, sizes, prev, pager, next"
          :total="total">
      </el-pagination>
    </div>
    <div>
      <el-dialog title="请填写姓名" :visible.sync="dialogFormVisible" width="30%">
        <el-form :model="form">
          <el-form-item label="图书名称" label-width="25%">
            <el-input v-model="form.name" autocomplete="off" style="width:90%"></el-input>
          </el-form-item>
          <el-form-item label="图书封面" label-width="25%">
            <el-upload action="http://localhost:8080/api/files/upload" :on-success="successUpload">
              <el-button size="small" type="primary">点击上传</el-button>
            </el-upload>
          </el-form-item>
          <el-form-item label="图书作者" label-width="25%">
            <el-input v-model="form.author" autocomplete="off" style="width:90%"></el-input>
          </el-form-item>
          <el-form-item label="图书价格" label-width="25%">
            <el-input v-model="form.price" autocomplete="off" style="width:90%"></el-input>
          </el-form-item>
          <el-form-item label="图书出版社" label-width="25%">
            <el-input v-model="form.press" autocomplete="off" style="width:90%"></el-input>
          </el-form-item>
          <el-form-item label="图书分类" label-width="25%">
            <el-select v-model="form.typeId" placeholder="请选择" style="width: 90%">
              <el-option v-for="item in typeObjs" :key="item.id" :label="item.name" :value="item.id"></el-option>
            </el-select>
          </el-form-item>
        </el-form>
        <div slot="footer" class="dialog-footer">
          <el-button @click="dialogFormVisible = false">取 消</el-button>
          <el-button type="primary" @click="submit()">确 定</el-button>
        </div>
      </el-dialog>
    </div>
  </div>
</template>
<script>
import request from "@/utils/request";
export default {
  //name: "BookView",
  data() {
    return {
      params:{
        name: '',
        author: '',
        //price: '',
        //press: '',
        //img: '',
        pageNum: 1,
        pageSize: 5
      },
      tableData: [],
      total: 0,
      dialogFormVisible: false,
      form: {},
      typeObjs: []
    }
  },
  created() {
    this.findBySearch();
    this.findTypes();
  },
  methods: {
    findTypes() {
      request.get("/type").then(res => {
        if (res.code === '0') {
          this.typeObjs = res.data;
        } else {
          this.$message.error(res.msg)
        }
      })
    },
    findBySearch(){
      request.get("/book/search",{
        params:this.params}
      ).then(res =>{
        if(res.code === '0'){
          this.tableData = res.data.list;
          this.total = res.data.total;
        }else{
          this.$message.error(res.msg);
        }
      })
    },
    reset(){
      this.params = {
        pageNum: 1,
        pageSize: 5,
        name: '',
        phone: ''
      }
      this.findBySearch();
    },
    handleSizeChange(pageSize) {
      this.params.pageSize = pageSize;
      this.findBySearch();
    },
    handleCurrentChange(pageNum) {
      this.params.pageNum = pageNum;
      this.findBySearch();
    },
    add(){
      this.form = {};
      this.dialogFormVisible = true;
    },
    edit(obj) {
      this.form = obj;
      this.dialogFormVisible = true;
    },
    submit(){
      request.post("/book", this.form).then(res => {
        if (res.code === '0') {
          this.$message.success("操作成功");
          this.dialogFormVisible = false;
          this.findBySearch();
        } else {
          this.$message.error(res.msg);
        }
      })
    },
    del(id) {
      request.delete("/book/" + id).then(res => {
        if (res.code === '0') {
          this.$message.success("删除成功");
          this.findBySearch();
        } else {
          this.$message.error(res.msg);
        }
      })
    },
    successUpload(res) {
      this.form.img = res.data;
    },
    down(flag) {
      location.href = 'http://localhost:8080/api/files/' + flag
    }
  }
}
</script>
```
##### 后端：TypeController.java
```java
@GetMapping
    public Result findAll() {
        return Result.success(typeService.findAll());
    }
```
##### 后端：BookService.java
```java
public PageInfo<Book> findBySearch(Params params) {
    // 开启分页查询
    PageHelper.startPage(params.getPageNum(), params.getPageSize());
    // 接下来的查询会自动按照当前开启的分页设置来查询
    //return adminDao.findBySearch(params);
    List<Book> list = bookDao.findBySearch(params);

    if (CollectionUtil.isEmpty(list)) {
        return PageInfo.of(new ArrayList<>());
    }
    for (Book book : list) {
        if (ObjectUtil.isNotEmpty(book.getTypeId())) {
            Type type = typeDao.selectByPrimaryKey(book.getTypeId());
            if (ObjectUtil.isNotEmpty(type)) {
                book.setTypeName(type.getName());
            }
        }
    }
    return PageInfo.of(list);
}
```
##### 后端：BookMapper.xml
##### 后端：Book.java
```java
@Table(name = "book")
public class Book {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Integer id;
    @Column(name = "name")
    private String name;
    @Column(name = "price")
    private String price;
    @Column(name = "author")
    private String author;
    @Column(name = "press")
    private String press;
    @Column(name = "img")
    private String img;
    @Column(name = "typeId")
    private Integer typeId;
    @Transient
    private String typeName;
}
```
##### 数据库：新建查询.sql
```sql
select book.*, type.name AS typeName from book 
left join type on book.typeId =type.id 
order by book.id asc
```
#### 20250201 武哥毕设 11.[权限控制]
12Springboot+Vue实现全网最简单实用的角色权限控制
##### (1)添加不同角色
【前端】
Layout.vue：
`<el-menu-item index="/admin">` “用户信息”
AdminView.vue：
`<el-table>` 引入表格组件
`<el-table-column prop="role" label="角色" width="180">` 表格组件“表格项”
`<el-dialog>` 引入对话框组件
`<el-form-item label="角色" label-width="15%">` 对话框组件“对话框条目”
`<el-select>` 引入选择器组件
`<el-option label="教师" value="ROLE_TEACHER">` 选择器组件“下拉选项”
`<el-option label="学生" value="ROLE_STUDENT">` 选择器组件“下拉选项”
【后端】
admin.sql：
在"用户信息表"中新建字段(role)
Admin.java：
`@Column(name = "role")` 关联数据库表字段
`private String role;` 定义变量typeId
生成getter&setter
AdminMapper.xml：
`<mapper namespace="com.example.dao.AdminDao">`
`<select id="findBySearch" resultType="com.example.entity.Admin">`
基于xml映射查询数据库
##### (2)登录权限控制
【前端】
Layout.vue：
`<el-submenu index="2" v-if="user.role === 'ROLE_ADMIN'">` “用户信息”设置“仅管理员可见”
data：`user: localStorage.getItem("user") ? JSON.parse(localStorage.getItem("user")) : {}`
TypeView.vue：
`<el-button  @click="add()" v-if="user.role === 'ROLE_ADMIN'">` “新增”设置“仅管理员可见”
`<el-button v-if="user.role === 'ROLE_ADMIN'">` “删除”设置“仅管理员可见”
`<el-button @click="exp()" v-if="user.role === 'ROLE_ADMIN'">` “导出报表”设置“仅管理员可见”
`<el-button v-if="user.role === 'ROLE_ADMIN'">` “批量导入”设置“仅管理员可见”
`<el-table-column type="selection" v-if="user.role === 'ROLE_ADMIN'">` 选择器组件设置“仅管理员可见”
data：`user: localStorage.getItem("user") ? JSON.parse(localStorage.getItem("user")) : {}`
BookView.vue：
`<el-button @click="add()"  v-if="user.role !== 'ROLE_STUDENT'">` “新增”设置“仅学生不可见”
`<el-button @click="edit(scope.row)" v-if="user.role === 'ROLE_ADMIN'">` “编辑”设置“仅管理员可见”
`<el-button v-if="user.role === 'ROLE_ADMIN'">` “删除”设置“仅管理员可见”
data：`user: localStorage.getItem("user") ? JSON.parse(localStorage.getItem("user")) : {}`
##### (3)注册默认权限
【前端】
LoginView.vue：
`<a @click="navRegister">` 跳转注册
method：`navRegister(){}` “跳转注册”
跳转路由`this.$router.push("/register")`
index.js：
`router.beforeEach((to ,from, next) =>{})`路由守卫
`const user = localStorage.getItem("user");`获取数据
`if (!user && to.path !== '/login' && to.path !== '/register'){}`获取失败且前往非登录页(sql注入)
`return next("/login");`跳转登录
`next();`允许跳转
RegisterView.vue：
`<el-form-item>` 引入下拉菜单组件
`<el-option label="教师" value="ROLE_TEACHER">` 下拉选项
`<el-option label="学生" value="ROLE_STUDENT">` 下拉选项
`<a @click="navLogin">` 跳转登录
method：`navLogin(){}` “跳转登录”
跳转路由`this.$router.push("/login")`
method：`register(){}` “登录”
默认权限`this.admin.role = 'ROLE_STUDENT'` “学生”角色
##### 前端：Layout.vue
```js
<template>
  <div>
    <el-container>
      <el-header style="background-color: #4c535a">
        <img src="@/assets/logo.png" alt="" style="width: 40px; position: relative; top: 10px;">
        <span style="font-size: 20px; margin-left: 15px; color: white">手拉手带小白做毕设</span>
        <el-dropdown style="float: right; height: 60px; line-height: 60px">
          <span class="el-dropdown-link" style="color: white; font-size: 16px">{{ user.name }}<i class="el-icon-arrow-down el-icon--right"></i></span>
          <el-dropdown-menu slot="dropdown">
            <el-dropdown-item>
              <div @click="logout">退出</div>
            </el-dropdown-item>
          </el-dropdown-menu>
        </el-dropdown>
      </el-header>
    </el-container>
    <el-container>
      <el-aside style="overflow: hidden; min-height: 100vh; background-color: #545c64; width: 250px">
        <el-menu :default-active="$route.path" router background-color="#545c64" text-color="#fff" active-text-color="#ffd04b">
          <el-menu-item index="/">
            <i class="el-icon-s-home"></i>
            <span slot="title">系统首页</span>
          </el-menu-item>
          <el-submenu index="2" v-if="user.role === 'ROLE_ADMIN'">
            <template slot="title">
              <i class="el-icon-location"></i><span>用户管理</span>
            </template>
            <el-menu-item-group>
              <el-menu-item index="/admin">用户信息</el-menu-item>
            </el-menu-item-group>
          </el-submenu>
          <el-submenu index="3">
            <template slot="title">
              <i class="el-icon-location"></i><span>信息管理</span>
            </template>
            <el-menu-item-group>
              <el-menu-item index="/type">图书分类</el-menu-item>
              <el-menu-item index="/book">图书信息</el-menu-item>
            </el-menu-item-group>
          </el-submenu>
        </el-menu>
      </el-aside>
      <el-main>
        <router-view/>
      </el-main>
    </el-container>
  </div>
</template>

<style>
.el-menu{
  border-right: none !important;
}
</style>

<script>
export default {
  name: "Layout",

  data() {
    return {
      // user: {
      //   name: ''
      // }
      user: localStorage.getItem("user") ? JSON.parse(localStorage.getItem("user")) : {}
    }
  },
  // created() {
  //   this.user = JSON.parse(localStorage.getItem('user'))
  // },
  methods: {
    logout() {
      localStorage.removeItem('user')
      this.$router.push('/login')
    }
  }
}
</script>

<style>
.el-menu{
  border-right: none !important;
}
</style>
```
##### 前端：LoginView.vue
```js
<div style="text-align: center">
  未有账号？<a href="javascript:void(0)" style="text-decoration: none" @click="navRegister">点击注册</a>
</div>

navRegister() {
  this.$router.push("/register")
}
```
##### 前端：RegisterView.vue
```js
<el-input v-model="admin.password" show-password prefix-icon="el-icon-lock" style="width: 80%" placeholder="请输入密码"></el-input>

<el-form-item>
  <el-select v-model="admin.role" placeholder="请选择" style="width: 80%">
    <el-option label="教师" value="ROLE_TEACHER"></el-option>
    <el-option label="学生" value="ROLE_STUDENT"></el-option>
  </el-select>
</el-form-item>

<div style="text-align: center">
  已有账号？<a href="javascript:void(0)" style="text-decoration: none" @click="navLogin">点击登录</a>
</div>

navLogin() {
  this.$router.push("/login")
}

this.admin.role = 'ROLE_STUDENT'
```
##### 前端：AdminView.vue
```js
<template>
  <div>
    <div>
      <el-input v-model="params.name" style="width: 200px; margin-right: 10px" placeholder="请输入姓名"></el-input>
      <el-input v-model="params.phone" style="width: 200px; margin-right: 10px" placeholder="请输入电话"></el-input>
      <el-button type="warning" @click="findBySearch()">搜索</el-button>
      <el-button type="primary" @click="reset()">清空</el-button>
      <el-button type="primary" @click="add()">新增</el-button>
    </div>
    <div>
      <el-table :data="tableData" style="width: 100%; margin: 15px 0px">
        <el-table-column prop="name" label="姓名" width="180"></el-table-column>
        <el-table-column prop="sex" label="性别" width="180"></el-table-column>
        <el-table-column prop="age" label="年龄" width="180"></el-table-column>
        <el-table-column prop="phone" label="电话" width="180"></el-table-column>
        <el-table-column prop="role" label="角色" width="180"></el-table-column>
        <el-table-column label="操作">
          <template slot-scope="scope">
            <el-button type="primary" @click="edit(scope.row)">编辑</el-button>
            <el-popconfirm title="确定删除吗？" @confirm="del(scope.row.id)">
              <el-button slot="reference" type="danger" style="margin-left: 5px">删除</el-button>
            </el-popconfirm>
          </template>
        </el-table-column>
      </el-table>
    </div>
    <div class="block">
      <el-pagination
          @size-change="handleSizeChange"
          @current-change="handleCurrentChange"
          :current-page="params.pageNum"
          :page-sizes="[5, 10, 15, 20]"
          :page-size="params.pageSize"
          layout="total, sizes, prev, pager, next"
          :total="total">
      </el-pagination>
    </div>
    <div>
      <el-dialog title="请填写姓名" :visible.sync="dialogFormVisible" width="30%">
        <el-form :model="form">
          <el-form-item label="姓名" label-width="15%">
            <el-input v-model="form.name" autocomplete="off" style="width:90%"></el-input>
          </el-form-item>
          <el-form-item label="性别" label-width="15%">
            <el-radio v-model="form.sex" label="男">男</el-radio>
            <el-radio v-model="form.sex" label="女">女</el-radio>
          </el-form-item>
          <el-form-item label="年龄" label-width="15%">
            <el-input v-model="form.age" autocomplete="off" style="width:90%"></el-input>
          </el-form-item>
          <el-form-item label="电话" label-width="15%">
            <el-input v-model="form.phone" autocomplete="off" style="width:90%"></el-input>
          </el-form-item>
          <el-form-item label="角色" label-width="15%">
            <el-select v-model="form.role" placeholder="请选择" style="width: 90%">
              <el-option label="教师" value="ROLE_TEACHER"></el-option>
              <el-option label="学生" value="ROLE_STUDENT"></el-option>
            </el-select>
          </el-form-item>
        </el-form>
        <div slot="footer" class="dialog-footer">
          <el-button @click="dialogFormVisible = false">取 消</el-button>
          <el-button type="primary" @click="submit()">确 定</el-button>
        </div>
      </el-dialog>
    </div>
  </div>
</template>
<script>
import request from "@/utils/request";
export default {
  //name: "AdminView",
  data() {
    return {
      params:{
        name: '',
        phone: '',
        pageNum: 1,
        pageSize: 5
      },
      tableData: [],
      total: 0,
      dialogFormVisible: false,
      form: {}
    }
  },
  created() {
    this.findBySearch();
  },
  methods: {
    findBySearch(){
      request.get("/admin/search",{
        params:this.params
      }).then(res =>{
        if(res.code === '0'){
          this.tableData = res.data.list;
          this.total = res.data.total;
        }else{
          this.$message({
            message: res.msg,
            type: 'error'
          });
        }
      })
    },
    reset(){
      this.params = {
        pageNum: 1,
        pageSize: 5,
        name: '',
        phone: ''
      }
      this.findBySearch();
    },
    handleSizeChange(pageSize) {
      this.params.pageSize = pageSize;
      this.findBySearch();
    },
    handleCurrentChange(pageNum) {
      this.params.pageNum = pageNum;
      this.findBySearch();
    },
    add(){
      this.form = {};
      this.dialogFormVisible = true;
    },
    edit(obj) {
      this.form = obj;
      this.dialogFormVisible = true;
    },
    submit(){
      request.post("/admin", this.form).then(res => {
        if (res.code === '0') {
          this.$message({
            message: '操作成功',
            type: 'success'
          });
          this.dialogFormVisible = false;
          this.findBySearch();
        } else {
          this.$message({
            message: res.msg,
            type: 'error'
          });
        }
      })
    },
    del(id) {
      request.delete("/admin/" + id).then(res => {
        if (res.code === '0') {
          this.$message({
            message: '删除成功',
            type: 'success'
          });
          this.findBySearch();
        } else {
          this.$message({
            message: res.msg,
            type: 'success'
          });
        }
      })
    }
  }
}
</script>
```
##### 前端：index.js
```js
// 路由守卫
router.beforeEach((to ,from, next) => {
  const user = localStorage.getItem("user");
  if (!user && to.path !== '/login' && to.path !== '/register') {
    return next("/login");
  }
  next();
})
```
##### 前端：TypeView.vue
```js
<template>
  <div>
    <div>
      <el-input v-model="params.name" style="width: 200px; margin-right: 10px" placeholder="请输入分类名称"></el-input>
      <el-button type="warning" @click="findBySearch()">查询</el-button>
      <el-button type="warning" @click="reset()">清空</el-button>
      <el-button type="primary" @click="add()" v-if="user.role === 'ROLE_ADMIN'">新增</el-button>
      <el-popconfirm title="确定这些数据删除吗？" @confirm="delBatch()">
        <el-button slot="reference" type="danger" style="margin-left: 5px" v-if="user.role === 'ROLE_ADMIN'">批量删除</el-button>
      </el-popconfirm>
      <el-button type="success" style="margin-left: 10px" @click="exp()" v-if="user.role === 'ROLE_ADMIN'">导出报表</el-button>
      <el-upload action="http://localhost:8080/api/type/upload" style="display: inline-block; margin-left: 10px" :show-file-list="false" :on-success="successUpload">
        <el-button size="small" type="primary" v-if="user.role === 'ROLE_ADMIN'">批量导入</el-button>
      </el-upload>
    </div>
    <div>
      <el-table :data="tableData" style="width: 100%" ref="table" @selection-change="handleSelectionChange" :row-key="getRowKeys">
        <el-table-column type="selection" width="55" align="center" :reserve-selection="true" v-if="user.role === 'ROLE_ADMIN'"></el-table-column>
        <el-table-column prop="name" label="分类名称" width="180"></el-table-column>
        <el-table-column prop="description" label="分类描述" width="180"></el-table-column>
        <el-table-column label="操作" v-if="user.role === 'ROLE_ADMIN'">
          <template slot-scope="scope">
            <el-button type="primary" @click="edit(scope.row)">编辑</el-button>
            <el-popconfirm title="确定删除吗？" @confirm="del(scope.row.id)">
              <el-button slot="reference" type="danger" style="margin-left: 5px">删除</el-button>
            </el-popconfirm>
          </template>
        </el-table-column>
      </el-table>
    </div>
    <div class="block">
      <el-pagination
          @size-change="handleSizeChange"
          @current-change="handleCurrentChange"
          :current-page="params.pageNum"
          :page-sizes="[5, 10, 15, 20]"
          :page-size="params.pageSize"
          layout="total, sizes, prev, pager, next"
          :total="total">
      </el-pagination>
    </div>
    <div>
      <el-dialog title="请填写姓名" :visible.sync="dialogFormVisible" width="30%">
        <el-form :model="form">
          <el-form-item label="分类名称" label-width="15%">
            <el-input v-model="form.name" autocomplete="off" style="width:90%"></el-input>
          </el-form-item>
          <el-form-item label="分类描述" label-width="15%">
            <el-input v-model="form.description" autocomplete="off" style="width:90%"></el-input>
          </el-form-item>
        </el-form>
        <div slot="footer" class="dialog-footer">
          <el-button @click="dialogFormVisible = false">取 消</el-button>
          <el-button type="primary" @click="submit()">确 定</el-button>
        </div>
      </el-dialog>
    </div>
  </div>
</template>
<script>
import request from "@/utils/request";
export default {
  //name: "AdminView",
  data() {
    return {

      params:{
        name: '',
        pageNum: 1,
        pageSize: 5
      },
      tableData: [],
      total: 0,
      dialogFormVisible: false,
      form: {},
      multipleSelection: [],
      user: localStorage.getItem("user") ? JSON.parse(localStorage.getItem("user")) : {}
    }
  },
  created() {
    this.findBySearch();
  },
  methods: {
    findBySearch(){
      request.get("/type/search",{
        params:this.params
      }).then(res =>{
        if(res.code === '0'){
          this.tableData = res.data.list;
          this.total = res.data.total;
        }else{
          this.$message({
            message: res.msg,
            type: 'error'
          });
        }
      })
    },
    reset(){
      this.params = {
        pageNum: 1,
        pageSize: 5,
        name: '',
      }
      this.findBySearch();
    },
    handleSizeChange(pageSize) {
      this.params.pageSize = pageSize;
      this.findBySearch();
    },
    handleCurrentChange(pageNum) {
      this.params.pageNum = pageNum;
      this.findBySearch();
    },
    add(){
      this.form = {};
      this.dialogFormVisible = true;
    },
    edit(obj) {
      this.form = obj;
      this.dialogFormVisible = true;
    },
    submit(){
      request.post("/type", this.form).then(res => {
        if (res.code === '0') {
          this.$message({
            message: '操作成功',
            type: 'success'
          });
          this.dialogFormVisible = false;
          this.findBySearch();
        } else {
          this.$message({
            message: res.msg,
            type: 'error'
          });
        }
      })
    },
    del(id) {
      request.delete("/type/" + id).then(res => {
        if (res.code === '0') {
          this.$message({
            message: '删除成功',
            type: 'success'
          });
          this.findBySearch();
        } else {
          this.$message({
            message: res.msg,
            type: 'success'
          });
        }
      })
    },
    delBatch() {
      if (this.multipleSelection.length === 0) {
        this.$message.warning("请勾选您要删除的项")
        return
      }
      request.put("/type/delBatch", this.multipleSelection).then(res => {
        if (res.code === '0') {
          this.$message.success("批量删除成功")
          this.findBySearch()
        } else {
          this.$message.error(res.msg)
        }
      })
    },
    handleSelectionChange(val) {
      this.multipleSelection = val;
    },
    getRowKeys(row) {
      return row.id;
    },
    exp() {
      let user = localStorage.getItem("user");
      location.href = 'http://localhost:8080/api/type/export?token=' + JSON.parse(user).token
    },
    successUpload(res) {
      if (res.code === '0') {
        this.$message.success("批量导入成功")
        this.findBySearch()
      } else {
        this.$message.error(res.msg)
      }
    }
  }
}
</script>
```
##### 前端：BookView.vue
```js
<template>
  <div>
    <div>
      <el-input v-model="params.name" style="width: 200px; margin-right: 10px" placeholder="请输入图书名称"></el-input>
      <el-input v-model="params.author" style="width: 200px; margin-right: 10px" placeholder="请输入图书作者"></el-input>
      <el-button type="warning" @click="findBySearch()">查询</el-button>
      <el-button type="primary" @click="reset()">清空</el-button>
      <el-button type="primary" @click="add()"  v-if="user.role !== 'ROLE_STUDENT'">新增</el-button>
    </div>
    <div>
      <el-table :data="tableData" style="width: 100%; margin: 15px 0px">
        <el-table-column label="图书封面" width="180">
          <template v-slot="scope">
            <el-image
                style="width: 70px; height: 70px; border-radius: 50%"
                :src="'http://localhost:8080/api/files/' + scope.row.img"
                :preview-src-list="['http://localhost:8080/api/files/' + scope.row.img]">
            </el-image>
          </template>
        </el-table-column>
        <el-table-column prop="name" label="图书姓名" width="180"></el-table-column>
        <el-table-column prop="author" label="图书作者" width="180"></el-table-column>
        <el-table-column prop="price" label="图书价格" width="180"></el-table-column>
        <el-table-column prop="press" label="图书出版社" width="180"></el-table-column>
        <el-table-column prop="typeName" label="图书分类" width="180"></el-table-column>
        <el-table-column label="操作">
          <template slot-scope="scope">
            <el-button type="primary" @click="edit(scope.row)" v-if="user.role === 'ROLE_ADMIN'">编辑</el-button>
            <el-button type="primary" @click="down(scope.row.img)">下载</el-button>
            <el-popconfirm title="确定删除吗？" @confirm="del(scope.row.id)">
              <el-button slot="reference" type="danger" style="margin-left: 5px" v-if="user.role === 'ROLE_ADMIN'">删除</el-button>
            </el-popconfirm>
          </template>
        </el-table-column>
      </el-table>
    </div>
    <div class="block">
      <el-pagination
          @size-change="handleSizeChange"
          @current-change="handleCurrentChange"
          :current-page="params.pageNum"
          :page-sizes="[5, 10, 15, 20]"
          :page-size="params.pageSize"
          layout="total, sizes, prev, pager, next"
          :total="total">
      </el-pagination>
    </div>
    <div>
      <el-dialog title="请填写姓名" :visible.sync="dialogFormVisible" width="30%">
        <el-form :model="form">
          <el-form-item label="图书名称" label-width="25%">
            <el-input v-model="form.name" autocomplete="off" style="width:90%"></el-input>
          </el-form-item>
          <el-form-item label="图书封面" label-width="25%">
            <el-upload action="http://localhost:8080/api/files/upload" :on-success="successUpload">
              <el-button size="small" type="primary">点击上传</el-button>
            </el-upload>
          </el-form-item>
          <el-form-item label="图书作者" label-width="25%">
            <el-input v-model="form.author" autocomplete="off" style="width:90%"></el-input>
          </el-form-item>
          <el-form-item label="图书价格" label-width="25%">
            <el-input v-model="form.price" autocomplete="off" style="width:90%"></el-input>
          </el-form-item>
          <el-form-item label="图书出版社" label-width="25%">
            <el-input v-model="form.press" autocomplete="off" style="width:90%"></el-input>
          </el-form-item>
          <el-form-item label="图书分类" label-width="25%">
            <el-select v-model="form.typeId" placeholder="请选择" style="width: 90%">
              <el-option v-for="item in typeObjs" :key="item.id" :label="item.name" :value="item.id"></el-option>
            </el-select>
          </el-form-item>
        </el-form>
        <div slot="footer" class="dialog-footer">
          <el-button @click="dialogFormVisible = false">取 消</el-button>
          <el-button type="primary" @click="submit()">确 定</el-button>
        </div>
      </el-dialog>
    </div>
  </div>
</template>
<script>
import request from "@/utils/request";
export default {
  //name: "BookView",
  data() {
    return {
      params:{
        name: '',
        author: '',
        //price: '',
        //press: '',
        //img: '',
        pageNum: 1,
        pageSize: 5
      },
      tableData: [],
      total: 0,
      dialogFormVisible: false,
      form: {},
      typeObjs: [],
      user: localStorage.getItem("user") ? JSON.parse(localStorage.getItem("user")) : {}
    }
  },
  created() {
    this.findBySearch();
    this.findTypes();
  },
  methods: {
    findTypes() {
      request.get("/type").then(res => {
        if (res.code === '0') {
          this.typeObjs = res.data;
        } else {
          this.$message.error(res.msg)
        }
      })
    },
    findBySearch(){
      request.get("/book/search",{
        params:this.params}
      ).then(res =>{
        if(res.code === '0'){
          this.tableData = res.data.list;
          this.total = res.data.total;
        }else{
          this.$message.error(res.msg);
        }
      })
    },
    reset(){
      this.params = {
        pageNum: 1,
        pageSize: 5,
        name: '',
        phone: ''
      }
      this.findBySearch();
    },
    handleSizeChange(pageSize) {
      this.params.pageSize = pageSize;
      this.findBySearch();
    },
    handleCurrentChange(pageNum) {
      this.params.pageNum = pageNum;
      this.findBySearch();
    },
    add(){
      this.form = {};
      this.dialogFormVisible = true;
    },
    edit(obj) {
      this.form = obj;
      this.dialogFormVisible = true;
    },
    submit(){
      request.post("/book", this.form).then(res => {
        if (res.code === '0') {
          this.$message.success("操作成功");
          this.dialogFormVisible = false;
          this.findBySearch();
        } else {
          this.$message.error(res.msg);
        }
      })
    },
    del(id) {
      request.delete("/book/" + id).then(res => {
        if (res.code === '0') {
          this.$message.success("删除成功");
          this.findBySearch();
        } else {
          this.$message.error(res.msg);
        }
      })
    },
    successUpload(res) {
      this.form.img = res.data;
    },
    down(flag) {
      location.href = 'http://localhost:8080/api/files/' + flag
    }
  }
}
</script>
```
##### 后端：Admin.java
```java
@Table(name = "admin")
public class Admin {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Integer id;
    @Column(name = "name")
    private String name;
    @Column(name = "password")
    private String password;
    @Column(name = "sex")
    private String sex;
    @Column(name = "age")
    private Integer age;
    @Column(name = "phone")
    private String phone;
    @Column(name = "role")
    private String role;

    @Transient
    private String token;
}
```
##### 后端：AdminMapper.xml
```xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE mapper PUBLIC "-//mybatis.org//DTD Mapper 3.0//EN" "http://mybatis.org/dtd/mybatis-3-mapper.dtd">
<mapper namespace="com.example.dao.AdminDao">
<!--    <select id="getUser" resultType="com.example.entity.User">-->
<!--        select * from user-->
<!--    </select>-->
    <select id="findBySearch" resultType="com.example.entity.Admin">
        select * from admin
        <where>
            role != 'ROLE_ADMIN'
            <if test="params != null and params.name != null and params.name != ''">
                and name like concat('%', #{ params.name }, '%')
            </if>
            <if test="params != null and params.phone != null and params.phone != ''">
                and phone like concat('%', #{ params.phone }, '%')
            </if>
        </where>
    </select>
</mapper>
```
##### 数据库：admin.sql
```sql
ALTER TABLE `springboot`.`admin` 
DROP COLUMN `role`,
ADD COLUMN `role` varchar(255) NULL COMMENT '角色' AFTER `phone`;
```
#### 20250202 武哥毕设 12.*请假审核*
13Springboot+Vue实现请假申请、请假审核功能
##### (1)请假申请模块
【前端】
Layout.vue：
`<el-menu>` 引入下拉框组件
`<el-menu-item index="/audit">` 下拉选项“请假审核”
index.js：
引入页面AuditView.vue(配置路由path、name、component)
AuditView.vue：
新建src.views.AuditView.vue
`<el-date-picker>` 引入日期选择器组件
`<el-date-picker value-format="yyyy-MM-dd">` 日期选择器“日期格式”
`<el-button @click="add()" v-if="user.role === 'ROLE_STUDENT'">` “新增”设置“仅学生可见”
data：`user: localStorage.getItem("user") ? JSON.parse(localStorage.getItem("user")) : {}`
method：`add(){}` “新增”
数据赋值`this.form.userId = this.user.id;`
【后端】
audit.sql：
新建表，勾选主键自增
字符集：utf8mb4
排序规则：utf8mb4_unicode_ci
在"请假审核表"中新建字段
Audit.java：
新建com.example.entity.Autit.java
`@Table(name = "audit")`数据库表名
生成getter&setter
private Integer id;
private String name;
private String time;
private String day;
private Integer userId;
private String status;
private String reason;
AuditDao.java(Interface)：
`public interface AuditDao extends Mapper<Audit>{}`
AuditMapper.xml：
`<mapper namespace="com.example.dao.AuditDao">`
`<select id="findBySearch" resultType="com.example.entity.Audit">`
AuditService.java：
`@Service`service层
`@Resource`引入dao层(`private AuditDao auditDao;`)
AuditController.java：
`@CrossOrigin`跨域问题
`@RestController`controller层
`@RequestMapping("/audit")`
`@Resource`引入service层(`private AuditService auditService;`)
##### (2)模块关联(显示请假用户姓名) 通过java逻辑(AuditService查询)
【前端】
AuditView.vue：
`<el-table>` 引入表单组件
`<el-table-column prop="userName" label="请假用户" width="180">` 引入表单组件“请假用户”
【后端】
Audit.java：
`@Transient` 非数据库字段
`private String userName;` 定义变量userName
生成getter&setter
AuditMapper.xml：
`<select id="findBySearch" resultType="com.example.entity.Audit">`
`select * from audit`
AuditService.java：
`@Resource`引入dao层(`private AdminDao adminDao;`)
`public PageInfo<Audit> findBySearch(Params params){}`
`for (Audit audit : list){}` 遍历数组
`if (ObjectUtil.isNotEmpty(audit.getUserId())) {}` 判断请假用户不为空
`Admin user = adminDao.selectByPrimaryKey(audit.getUserId());` 根据请假用户ID查询姓名
`if (ObjectUtil.isNotEmpty(user)){}` 判断用户不为空
`audit.setUserName(user.getName());` 数据赋值
##### (3)模块关联(显示请假用户姓名) 通过sql语句(left join查询)
【前端】
AuditView.vue：
`<el-table>` 引入表单组件
`<el-table-column prop="userName" label="请假用户" width="180">` 引入表单组件“请假用户”
【后端】
Audit.java：
`@Transient`非数据库字段
`private String typeName;`定义变量typeName
生成getter&setter
BookMapper.xml：
`<select id="findBySearch" resultType="com.example.entity.Audit">`
`select audit.*, admin.name as userName from audit left join admin on audit.userId = admin.id` (userName对应实体类字段)
`<if test="params != null and params.name != null and params.name != ''">` 条件查询
##### (4)审核功能
【前端】
AuditView.vue：
`<el-button @click="audit(scope.row)">` 引入按钮组件
`<el-button @click="audit(scope.row)" v-if="user.role !== 'ROLE_STUDENT'">` “审核”设置“仅学生不可见”
`<el-button  @click="edit(scope.row)" v-if="user.role === 'ROLE_STUDENT'">` “编辑”设置“仅学生可见”
`<el-dialog title="请审核" :visible.sync="auditVisible">` 引入对话框组件(审核)
`<el-radio v-model="form.status" label="审核通过">` 引入单选框组件
`<el-radio v-model="form.status" label="审核不通过">` 引入单选框组件
`<el-input v-model="form.reason" autocomplete="off" style="width: 90%">` “审核意见”
data：`dialogFormVisible: false`
method：`audit(obj){}` “审核”
数据赋值`this.form = obj;`编辑原数据
显示表单`this.auditVisible = true;`
method：`submit(){}` “确定”
隐藏表单`this.auditVisible = false;`
##### (5)用户区分
【后端】
Params.java：
`private Integer userId;` 定义变量userId
生成getter&setter
AuditService.java：
`Admin user = JwtTokenUtils.getCurrentUser();` 获取当前用户
`if (ObjectUtil.isNull(user)){}` 判断用户非空
`throw new CustomException("从token中未解析到用户信息，请重新登录");` 异常处理
`if ("ROLE_STUDENT".equals(user.getRole())){}` 判断为学生用户
`params.setUserId(user.getId());` 设置userId为学生
AuditMapper.xml：
`<if test="params != null and params.userId != null">` 条件查询
##### 前端：Layout.vue
```js
<el-menu-item index="/audit">请假审核</el-menu-item>
```
##### 前端：index.js
```js
import Vue from 'vue'
import VueRouter from 'vue-router'
import HomeView from '../views/HomeView.vue'
import LoginView from "@/views/LoginView.vue";
import Layout from "@/views/Layout.vue";
import RegisterView from "@/views/RegisterView.vue";
import BookView from "@/views/BookView.vue";
import TypeView from "@/views/TypeView.vue";
import AuditView from "@/views/AuditView.vue";

Vue.use(VueRouter)
const routes = [
  {
    path: '/login',
    name: 'Login',
    component: LoginView
  },
  {
    path: '/register',
    name: 'Register',
    component: RegisterView
  },
  {
    path: '/',
    name: 'Layout',
    component: Layout,
    //redirect: '/home',
    children: [ // 子路由
      {
        path: '',
        component: HomeView
      },
      {
        path: 'admin',
        component: () => import('../views/AdminView.vue')
      },
      {
        path: 'book',
        component: BookView
      },
      {
        path: 'type',
        component: TypeView
      },
      {
        path: 'audit',
        component: AuditView
      }
    ]
  },
]
const router = new VueRouter({
  mode: 'history',
  base: process.env.BASE_URL,
  routes
})
// 路由守卫
router.beforeEach((to ,from, next) => {
  const user = localStorage.getItem("user");
  if (!user && to.path !== '/login' && to.path !== '/register') {
    return next("/login");
  }
  next();
})
export default router
```
##### 前端：AuditView.vue
```js
<template>
  <div>
    <div>
      <el-input v-model="params.name" style="width: 200px; margin-right: 10px" placeholder="请输入请假原由"></el-input>
      <el-button type="warning" @click="findBySearch()">搜索</el-button>
      <el-button type="warning" @click="reset()">清空</el-button>
      <el-button type="primary" @click="add()" v-if="user.role === 'ROLE_STUDENT'">新增</el-button>
    </div>
    <div>
      <el-table :data="tableData" style="width: 100%">
        <el-table-column prop="name" label="请假原由" width="180"></el-table-column>
        <el-table-column prop="time" label="请假日期" width="180"></el-table-column>
        <el-table-column prop="day" label="请假天数" width="180"></el-table-column>
        <el-table-column prop="userName" label="请假用户" width="180"></el-table-column>
        <el-table-column prop="status" label="审核状态" width="180"></el-table-column>
        <el-table-column prop="reason" label="审核意见" width="180"></el-table-column>
        <el-table-column label="操作">
          <template slot-scope="scope">
            <el-button type="primary" @click="edit(scope.row)" v-if="user.role === 'ROLE_STUDENT'">编辑</el-button>
            <el-button type="success" @click="audit(scope.row)" v-if="user.role !== 'ROLE_STUDENT'">审核</el-button>
            <el-popconfirm title="确定删除吗？" @confirm="del(scope.row.id)">
              <el-button slot="reference" type="danger" style="margin-left: 5px">删除</el-button>
            </el-popconfirm>
          </template>
        </el-table-column>
      </el-table>
    </div>
    <div class="block">
      <el-pagination
          @size-change="handleSizeChange"
          @current-change="handleCurrentChange"
          :current-page="params.pageNum"
          :page-sizes="[5, 10, 15, 20]"
          :page-size="params.pageSize"
          layout="total, sizes, prev, pager, next"
          :total="total">
      </el-pagination>
    </div>
    <div>
      <el-dialog title="请填写信息" :visible.sync="dialogFormVisible" width="30%">
        <el-form :model="form">
          <el-form-item label="请假原由" label-width="20%">
            <el-input v-model="form.name" autocomplete="off" style="width:90%"></el-input>
          </el-form-item>
          <el-form-item label="请假日期" label-width="20%">
            <el-date-picker v-model="form.time" type="date" style="width: 90%" placeholder="选择日期" value-format="yyyy-MM-dd"></el-date-picker>
          </el-form-item>
          <el-form-item label="请假天数" label-width="20%">
            <el-input v-model="form.day" autocomplete="off" style="width:90%"></el-input>
          </el-form-item>
        </el-form>
        <div slot="footer" class="dialog-footer">
          <el-button @click="dialogFormVisible = false">取 消</el-button>
          <el-button type="primary" @click="submit()">确 定</el-button>
        </div>
      </el-dialog>
    </div>
    <div>
      <el-dialog title="请审核" :visible.sync="auditVisible" width="30%">
        <el-form :model="form">
          <el-form-item label="审核状态" label-width="15%">
            <el-radio v-model="form.status" label="审核通过"></el-radio>
            <el-radio v-model="form.status" label="审核不通过"></el-radio>
          </el-form-item>
          <el-form-item label="审核意见" label-width="15%">
            <el-input v-model="form.reason" autocomplete="off" style="width: 90%"></el-input>
          </el-form-item>
        </el-form>
        <div slot="footer" class="dialog-footer">
          <el-button @click="auditVisible = false">取 消</el-button>
          <el-button type="primary" @click="submit()">确 定</el-button>
        </div>
      </el-dialog>
    </div>
  </div>
</template>
<script>
import request from "@/utils/request";
export default {
  //name: "AdminView",
  data() {
    return {
      params:{
        name: '',
        phone: '',
        pageNum: 1,
        pageSize: 5
      },
      tableData: [],
      total: 0,
      dialogFormVisible: false,
      auditVisible: false,
      form: {},
      user: localStorage.getItem("user") ? JSON.parse(localStorage.getItem("user")) : {}
    }
  },
  created() {
    this.findBySearch();
  },
  methods: {
    findBySearch(){
      request.get("/audit/search",{
        params:this.params
      }).then(res =>{
        if(res.code === '0'){
          this.tableData = res.data.list;
          this.total = res.data.total;
        }else{
          this.$message.error(res.msg);
        }
      })
    },
    reset(){
      this.params = {
        pageNum: 1,
        pageSize: 5,
        name: '',
        phone: ''
      }
      this.findBySearch();
    },
    handleSizeChange(pageSize) {
      this.params.pageSize = pageSize;
      this.findBySearch();
    },
    handleCurrentChange(pageNum) {
      this.params.pageNum = pageNum;
      this.findBySearch();
    },
    add(){
      this.form = {};
      this.form.userId = this.user.id;
      this.dialogFormVisible = true;
    },
    edit(obj) {
      this.form = obj;
      this.dialogFormVisible = true;
    },
    audit(obj) {
      this.form = obj;
      this.auditVisible = true;
    },
    submit(){
      request.post("/audit", this.form).then(res => {
        if (res.code === '0') {
          this.$message.success("操作成功");
          this.dialogFormVisible = false;
          this.auditVisible = false;
          this.findBySearch();
        } else {
          this.$message.error(res.msg);
        }
      })
    },
    del(id) {
      request.delete("/audit/" + id).then(res => {
        if (res.code === '0') {
          this.$message.success("删除成功");
          this.findBySearch();
        } else {
          this.$message.error(res.msg);
        }
      })
    }
  }
}
</script>
```
##### 后端：AuditController.java
```java
@CrossOrigin
@RestController
@RequestMapping("/audit")
public class AuditController {
    @Resource
    private AuditService auditService;
    @PostMapping
    public Result save(@RequestBody Audit audit) {
        if (audit.getId() == null) {
            auditService.add(audit);
        } else {
            auditService.update(audit);
        }
        return Result.success();
    }
    @GetMapping("/search")
    public Result findBySearch(Params params) {
        PageInfo<Audit> info = auditService.findBySearch(params);
        return Result.success(info);
    }
    @DeleteMapping("/{id}")
    public Result delete(@PathVariable Integer id) {
        auditService.delete(id);
        return Result.success();
    }
}
```
##### 后端：AuditService.java
```java
@Service
public class AuditService {
    @Resource
    private AuditDao auditDao;
    public void add(Audit audit) {
        auditDao.insertSelective(audit);
    }
    public void update(Audit audit) {
        auditDao.updateByPrimaryKeySelective(audit);
    }
    public PageInfo<Audit> findBySearch(Params params) {
        Admin user = JwtTokenUtils.getCurrentUser();
        if (ObjectUtil.isNull(user)) {
            throw new CustomException("从token中未解析到用户信息，请重新登录");
        }
        if ("ROLE_STUDENT".equals(user.getRole())) {
            params.setUserId(user.getId());
        }

        // 开启分页查询
        PageHelper.startPage(params.getPageNum(), params.getPageSize());
        // 接下来的查询会自动按照当前开启的分页设置来查询
        List<Audit> list = auditDao.findBySearch(params);
//        for (Audit audit : list) {
//            if (ObjectUtil.isNotEmpty(audit.getUserId())) {
//                Admin user = adminDao.selectByPrimaryKey(audit.getUserId());
//                if (ObjectUtil.isNotEmpty(user)) {
//                    audit.setUserName(user.getName());
//                }
//            }
//        }
        return PageInfo.of(list);
    }
    public void delete(Integer id) {
        auditDao.deleteByPrimaryKey(id);
    }
}
```
##### 后端：AuditDao.java(Interface)
```java
@Repository
public interface AuditDao extends Mapper<Audit> {
    List<Audit> findBySearch(@Param("params") Params params);
}
```
##### 后端：AuditMapper.xml
```xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE mapper PUBLIC "-//mybatis.org//DTD Mapper 3.0//EN" "http://mybatis.org/dtd/mybatis-3-mapper.dtd">
<mapper namespace="com.example.dao.AuditDao">
    <select id="findBySearch" resultType="com.example.entity.Audit">
        select audit.*, admin.name as userName from audit
        left join admin on audit.userId = admin.id
        <where>
            <if test="params != null and params.name != null and params.name != ''">
                and audit.name like concat('%', #{ params.name }, '%')
            </if>
            <if test="params != null and params.userId != null">
                and audit.userId = #{ params.userId }
            </if>
        </where>
    </select>
</mapper>
```
##### 后端：Audit.java
```java
@Table(name = "audit")
public class Audit {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Integer id;
    @Column(name = "name")
    private String name;
    @Column(name = "time")
    private String time;
    @Column(name = "day")
    private String day;
    @Column(name = "userId")
    private Integer userId;
    @Column(name = "status")
    private String status;
    @Column(name = "reason")
    private String reason;
    @Transient
    private String userName;
    // get set 方法……
}
```
##### 后端：Params.java
```java
public class Params {
    private String name;
    private String phone;
    private String author;
    private Integer userId;
    private Integer PageNum;
    private Integer PageSize;
}
```
##### 数据库：audit.sql
```sql
CREATE TABLE `audit` (
  `id` int(11) NOT NULL AUTO_INCREMENT COMMENT '主键ID',
  `name` varchar(255) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci DEFAULT NULL COMMENT '请假原由',
  `time` varchar(255) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci DEFAULT NULL COMMENT '请假日期',
  `day` varchar(255) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci DEFAULT NULL COMMENT '请假天数',
  `userId` int(11) DEFAULT NULL COMMENT '请假用户ID',
  `status` varchar(255) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci DEFAULT NULL COMMENT '审核状态',
  `reason` varchar(255) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci DEFAULT NULL COMMENT '审核意见',
  PRIMARY KEY (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_unicode_ci COMMENT='请假审核表';
```
#### 20250204 武哥毕设 13.*预约预定*
14Springboot+Vue实现酒店预订、学生选课、教室预订、图书借阅、场地预约、房屋租赁等功能
##### (1)酒店信息模块
【前端】
Layout.vue：
`<el-menu>` 引入下拉框组件
`<el-menu-item index="/hotel">` 下拉选项“酒店信息”
index.js：
引入页面HotelView.vue(配置路由path、name、component)
HotelView.vue：
新建src.views.HotelView.vue
`<el-button @click="add()"  v-if="user.role === 'ROLE_ADMIN'">` “新增”设置“仅管理员可见”
`<el-button v-if="user.role !== 'ROLE_ADMIN'">` “预定”设置“仅管理员不可见”
`<el-button @click="edit(scope.row)" v-if="user.role === 'ROLE_ADMIN'">` “编辑”设置“仅管理员可见”
`<el-button v-if="user.role === 'ROLE_ADMIN'">` “删除”设置“仅管理员可见”
【后端】
hotel.sql：
拷贝表，新建表“酒店信息表”
Hotel.java：
新建com.example.entity.Hotel.java
`@Table(name = "hotel")`数据库表名
`private Integer id;`
`private String name;`
`private String price;`
`private String img;`
`private Integer num;`
生成getter&setter
HotelDao.java(Interface)：
`public interface AuditDao extends Mapper<Hotel>{}`
`List<Hotel> findBySearch(@Param("params")Params params);`
HotelMapper.xml：
`<mapper namespace="com.example.dao.HotelDao">`
`<select id="findBySearch" resultType="com.example.entity.Hotel">`
HotelService.java：
`@Service`service层
`@Resource`引入dao层(`private HotelDao hotelDao;`)
HotelController.java：
`@CrossOrigin`跨域问题
`@RestController`controller层
`@RequestMapping("/hotel")`
`@Resource`引入service层(`private HotelService hotelService;`)
##### (2)预定信息模块
【前端】
Layout.vue：
`<el-menu>` 引入下拉框组件
`<el-menu-item index="/reserve">` 下拉选项“预定信息”
index.js：
引入页面ReserveView.vue(配置路由path、name、component)
ReserveView.vue：
新建src.views.ReserveView.vue
`<el-table-column prop="hotelName" label="酒店名称">` 表格字段
`<el-table-column prop="userName" label="预订人">` 表格字段
`<el-table-column prop="time" label="预订时间">` 表格字段
【后端】
reserve.sql：
拷贝表，新建表“预定信息表”
Reserve.java：
新建com.example.entity.Reserve.java
`@Table(name = "reserve")`数据库表名
`private Integer id;`
`private Integer hotelId;`
`private Integer userId;`
`private String time;`
`@Transient` 非数据库字段
`private String hotelName;` 定义变量hotelName
`private String userName;` 定义变量userName
生成getter&setter
ReserveDao.java(Interface)：
`public interface AuditDao extends Mapper<Reserve>{}`
`List<Reserve> findBySearch(@Param("params")Params params);`
ReserveMapper.xml：
`<mapper namespace="com.example.dao.ReserveDao">`
`<select id="findBySearch" resultType="com.example.entity.Reserve">`
ReserveService.java：
`@Service`service层
`@Resource`引入dao层(`private ReserveDao reserveDao;`)
`@Resource`引入dao层(`private HotelDao hotelDao;`)
`@Resource`引入dao层(`private AdminDao adminDao;`)
ReserveController.java：
`@CrossOrigin`跨域问题
`@RestController`controller层
`@RequestMapping("/reserve")`
`@Resource`引入service层(`private ReserveService reserveService;`)
##### (3)预定完善
【前端】
HotelView.vue：
`<el-button @click="reserve(scope.row)" v-if="user.role !== 'ROLE_ADMIN'">` “预定”绑定事件
method：`reserve(row){}` “预定”
实体封装：`let param = {hotelId: row.id, userId: this.user.id}`
发送请求`request.post("/reserve", param)` 传递参数
处理请求`.then(res => {处理请求})`
判断成功`if(res.code === '0'){}else{判断失败}`
消息提示`this.$message.success("预订成功")`
重载查询`this.findBySearch();`
消息提示`this.$message.error(res.msg)`后端异常处理
【后端】
ReserveController.java：
`@PostMapping`
`public Result save(@RequestBody Reserve reserve){}`
`Hotel hotel = hotelDao.selectByPrimaryKey(reserve.getHotelId());`
`if (hotel.getNum() == 0){}`
`return Result.error("酒店该房间以预定完，请预定其他房间");`
`reserve.setTime(DateUtil.now());`
`reserveService.add(reserve);`
`hotel.setNum(hotel.getNum() - 1);`
`hotelDao.updateByPrimaryKeySelective(hotel);`
##### 前端：Layout.vue
```js
<el-menu-item index="/hotel">酒店信息</el-menu-item>
```
##### 前端：index.js
```js
{
  path: 'hotel',
  component: HotelView
},
{
  path: 'reserve',
  component: ReserveView
}
```
##### 前端：HotelView.vue
```js
<template>
  <div>
    <div>
      <el-input v-model="params.name" style="width: 200px; margin-right: 10px" placeholder="请输入图书名称"></el-input>
      <el-input v-model="params.author" style="width: 200px; margin-right: 10px" placeholder="请输入图书作者"></el-input>
      <el-button type="warning" @click="findBySearch()">查询</el-button>
      <el-button type="primary" @click="reset()">清空</el-button>
      <el-button type="primary" @click="add()"  v-if="user.role !== 'ROLE_STUDENT'">新增</el-button>
    </div>
    <div>
      <el-table :data="tableData" style="width: 100%; margin: 15px 0px">
        <el-table-column label="酒店图片" width="180">
          <template v-slot="scope">
            <el-image
                style="width: 70px; height: 70px; border-radius: 50%"
                :src="'http://localhost:8080/api/files/' + scope.row.img"
                :preview-src-list="['http://localhost:8080/api/files/' + scope.row.img]">
            </el-image>
          </template>
        </el-table-column>
        <el-table-column prop="name" label="酒店名称" width="180"></el-table-column>
        <el-table-column prop="price" label="酒店价格" width="180"></el-table-column>
        <el-table-column label="操作">
          <template slot-scope="scope">
            <el-button type="primary" @click="edit(scope.row)" v-if="user.role === 'ROLE_ADMIN'">编辑</el-button>
            <el-popconfirm title="确定删除吗？" @confirm="del(scope.row.id)">
              <el-button slot="reference" type="danger" style="margin-left: 5px" v-if="user.role === 'ROLE_ADMIN'">删除</el-button>
            </el-popconfirm>
          </template>
        </el-table-column>
      </el-table>
    </div>
    <div class="block">
      <el-pagination
          @size-change="handleSizeChange"
          @current-change="handleCurrentChange"
          :current-page="params.pageNum"
          :page-sizes="[5, 10, 15, 20]"
          :page-size="params.pageSize"
          layout="total, sizes, prev, pager, next"
          :total="total">
      </el-pagination>
    </div>
    <div>
      <el-dialog title="请填写姓名" :visible.sync="dialogFormVisible" width="30%">
        <el-form :model="form">
          <el-form-item label="酒店名称" label-width="25%">
            <el-input v-model="form.name" autocomplete="off" style="width:90%"></el-input>
          </el-form-item>
          <el-form-item label="酒店封面" label-width="25%">
            <el-upload action="http://localhost:8080/api/files/upload" :on-success="successUpload">
              <el-button size="small" type="primary">点击上传</el-button>
            </el-upload>
          </el-form-item>
          <el-form-item label="酒店价格" label-width="25%">
            <el-input v-model="form.price" autocomplete="off" style="width:90%"></el-input>
          </el-form-item>
        </el-form>
        <div slot="footer" class="dialog-footer">
          <el-button @click="dialogFormVisible = false">取 消</el-button>
          <el-button type="primary" @click="submit()">确 定</el-button>
        </div>
      </el-dialog>
    </div>
  </div>
</template>
<script>
import request from "@/utils/request";
export default {
  //name: "BookView",
  data() {
    return {
      params:{
        name: '',
        author: '',
        //price: '',
        //press: '',
        //img: '',
        pageNum: 1,
        pageSize: 5
      },
      tableData: [],
      total: 0,
      dialogFormVisible: false,
      form: {},
      typeObjs: [],
      user: localStorage.getItem("user") ? JSON.parse(localStorage.getItem("user")) : {}
    }
  },
  created() {
    this.findBySearch();
    this.findTypes();
  },
  methods: {
    findTypes() {
      request.get("/type").then(res => {
        if (res.code === '0') {
          this.typeObjs = res.data;
        } else {
          this.$message.error(res.msg)
        }
      })
    },
    findBySearch(){
      request.get("/hotel/search",{
        params:this.params}
      ).then(res =>{
        if(res.code === '0'){
          this.tableData = res.data.list;
          this.total = res.data.total;
        }else{
          this.$message.error(res.msg);
        }
      })
    },
    reset(){
      this.params = {
        pageNum: 1,
        pageSize: 5,
        name: '',
        phone: ''
      }
      this.findBySearch();
    },
    handleSizeChange(pageSize) {
      this.params.pageSize = pageSize;
      this.findBySearch();
    },
    handleCurrentChange(pageNum) {
      this.params.pageNum = pageNum;
      this.findBySearch();
    },
    add(){
      this.form = {};
      this.dialogFormVisible = true;
    },
    edit(obj) {
      this.form = obj;
      this.dialogFormVisible = true;
    },
    submit(){
      request.post("/hotel", this.form).then(res => {
        if (res.code === '0') {
          this.$message.success("操作成功");
          this.dialogFormVisible = false;
          this.findBySearch();
        } else {
          this.$message.error(res.msg);
        }
      })
    },
    del(id) {
      request.delete("/hotel/" + id).then(res => {
        if (res.code === '0') {
          this.$message.success("删除成功");
          this.findBySearch();
        } else {
          this.$message.error(res.msg);
        }
      })
    },
    successUpload(res) {
      this.form.img = res.data;
    },
    down(flag) {
      location.href = 'http://localhost:8080/api/files/' + flag
    }
  }
}
</script>
```
##### 前端：ReserveView.vue
```js
<template>
  <div>
    <div>
      <el-input v-model="params.name" style="width: 200px; margin-right: 10px" placeholder="请输入酒店名称"></el-input>
      <el-button type="warning" @click="findBySearch()">查询</el-button>
      <el-button type="warning" @click="reset()">清空</el-button>
      <el-button type="primary" @click="add()"  v-if="user.role === 'ROLE_ADMIN'">新增</el-button>
    </div>
    <div>
      <el-table :data="tableData" style="width: 100%; margin: 15px 0px">
        <el-table-column prop="hotelName" label="酒店名称" width="180"></el-table-column>
        <el-table-column prop="userName" label="预订人" width="180"></el-table-column>
        <el-table-column prop="time" label="预订时间" width="180"></el-table-column>
        <el-table-column label="操作">
          <template slot-scope="scope">
            <el-popconfirm title="确定删除吗？" @confirm="del(scope.row.id)">
              <el-button slot="reference" type="danger" style="margin-left: 5px" v-if="user.role === 'ROLE_ADMIN'">删除</el-button>
            </el-popconfirm>
          </template>
        </el-table-column>
      </el-table>
    </div>
    <div class="block">
      <el-pagination
          @size-change="handleSizeChange"
          @current-change="handleCurrentChange"
          :current-page="params.pageNum"
          :page-sizes="[5, 10, 15, 20]"
          :page-size="params.pageSize"
          layout="total, sizes, prev, pager, next"
          :total="total">
      </el-pagination>
    </div>
  </div>
</template>
<script>
import request from "@/utils/request";
export default {
  //name: "BookView",
  data() {
    return {
      params:{
        name: '',
        author: '',
        //price: '',
        //press: '',
        //img: '',
        pageNum: 1,
        pageSize: 5
      },
      tableData: [],
      total: 0,
      dialogFormVisible: false,
      form: {},
      user: localStorage.getItem("user") ? JSON.parse(localStorage.getItem("user")) : {}
    }
  },
  created() {
    this.findBySearch();
  },
  methods: {
    findBySearch(){
      request.get("/reserve/search",{
        params:this.params}
      ).then(res =>{
        if(res.code === '0'){
          this.tableData = res.data.list;
          this.total = res.data.total;
        }else{
          this.$message.error(res.msg);
        }
      })
    },
    reset(){
      this.params = {
        pageNum: 1,
        pageSize: 5,
        name: '',
        phone: ''
      }
      this.findBySearch();
    },
    handleSizeChange(pageSize) {
      this.params.pageSize = pageSize;
      this.findBySearch();
    },
    handleCurrentChange(pageNum) {
      this.params.pageNum = pageNum;
      this.findBySearch();
    },
    add(){
      this.form = {};
      this.dialogFormVisible = true;
    },
    edit(obj) {
      this.form = obj;
      this.dialogFormVisible = true;
    },
    del(id) {
      request.delete("/reserve/" + id).then(res => {
        if (res.code === '0') {
          this.$message.success("删除成功");
          this.findBySearch();
        } else {
          this.$message.error(res.msg);
        }
      })
    }
  }
}
</script>
```
##### 后端：HotelController.java
```java
@CrossOrigin
@RestController
@RequestMapping("/hotel")
public class HotelController {
    @Resource
    private HotelService hotelService;
    @GetMapping("/search")
    public Result findBySearch(Params params) {
        PageInfo<Hotel> info = hotelService.findBySearch(params);
        return Result.success(info);
    }
    @PostMapping
    public Result save(@RequestBody Hotel hotel) {
        //adminService.add(admin);
        if (hotel.getId() == null) {
            hotelService.add(hotel);
        } else {
            hotelService.update(hotel);
        }
        return Result.success();
    }
    @DeleteMapping("/{id}")
    public Result delete(@PathVariable Integer id) {
        hotelService.delete(id);
        return Result.success();
    }
}
```
##### 后端：HotelService.java
```java
@Service
public class HotelService {
    @Resource
    private HotelDao hotelDao;

    public void add(Hotel hotel) {
        hotelDao.insertSelective(hotel);
    }
    public PageInfo<Hotel> findBySearch(Params params) {
        // 开启分页查询
        PageHelper.startPage(params.getPageNum(), params.getPageSize());
        // 接下来的查询会自动按照当前开启的分页设置来查询
        //return adminDao.findBySearch(params);
        List<Hotel> list = hotelDao.findBySearch(params);

        if (CollectionUtil.isEmpty(list)) {
            return PageInfo.of(new ArrayList<>());
        }

        return PageInfo.of(list);
    }
    public void update(Hotel hotel) {
        hotelDao.updateByPrimaryKeySelective(hotel);
    }
    public void delete(Integer id) {
        hotelDao.deleteByPrimaryKey(id);
    }
}
```
##### 后端：HotelDao.java(Interface)
```java
@Repository
public interface HotelDao extends Mapper<Hotel> {
    List<Hotel> findBySearch(@Param("params")Params params);
}
```
##### 后端：HotelMapper.xml
```xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE mapper PUBLIC "-//mybatis.org//DTD Mapper 3.0//EN" "http://mybatis.org/dtd/mybatis-3-mapper.dtd">
<mapper namespace="com.example.dao.HotelDao">
    <select id="findBySearch" resultType="com.example.entity.Hotel">
        select * from hotel
        <where>
            <if test="params != null and params.name != null and params.name != ''">
                and hotel.name like concat('%', #{ params.name }, '%')
            </if>
        </where>
        order by hotel.id asc
    </select>
</mapper>
```
##### 后端：Hotel.java
```java
@Table(name = "hotel")
public class Hotel {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Integer id;
    @Column(name = "name")
    private String name;
    @Column(name = "price")
    private String price;
    @Column(name = "img")
    private String img;
    @Column(name = "num")
    private Integer num;
}
```
##### 后端：ReserveController.java
```java
@CrossOrigin
@RestController
@RequestMapping("/reserve")
public class ReserveController {
    @Resource
    private ReserveService reserveService;
    @Resource
    private HotelDao hotelDao;
    @GetMapping("/search")
    public Result findBySearch(Params params) {
        PageInfo<Reserve> info = reserveService.findBySearch(params);
        return Result.success(info);
    }
    @PostMapping
    public Result save(@RequestBody Reserve reserve) {
//        // 1. 酒店剩余房间是否为0，大于0的时候，才可以被预定
        Hotel hotel = hotelDao.selectByPrimaryKey(reserve.getHotelId());
        if (hotel.getNum() == 0) {
            return Result.error("酒店该房间以预定完，请预定其他房间");
        }
//        // 2. 往预定表里插入一条预定记录
        reserve.setTime(DateUtil.now());
        reserveService.add(reserve);
//        // 3. 对应的酒店房间剩余数量减一
        hotel.setNum(hotel.getNum() - 1);
        hotelDao.updateByPrimaryKeySelective(hotel);

        return Result.success();
    }
    @DeleteMapping("/{id}")
    public Result delete(@PathVariable Integer id) {
        reserveService.delete(id);
        return Result.success();
    }
}
```
##### 后端：ReserveService.java
```java
@Service
public class ReserveService {
    @Resource
    private ReserveDao reserveDao;

    @Resource
    private HotelDao hotelDao;
    @Resource
    private AdminDao adminDao;

    public void add(Reserve reserve) {
        reserveDao.insertSelective(reserve);
    }

    public PageInfo<Reserve> findBySearch(Params params) {
        // 开启分页查询
        PageHelper.startPage(params.getPageNum(), params.getPageSize());
        // 接下来的查询会自动按照当前开启的分页设置来查询
        //return adminDao.findBySearch(params);
        List<Reserve> list = reserveDao.findBySearch(params);

        if (CollectionUtil.isEmpty(list)) {
            return PageInfo.of(new ArrayList<>());
        }
        for (Reserve reserve : list) {
            if (ObjectUtil.isNotEmpty(reserve.getHotelId())) {
                Hotel hotel = hotelDao.selectByPrimaryKey(reserve.getHotelId());
                if (ObjectUtil.isNotEmpty(hotel)) {
                    reserve.setHotelName(hotel.getName());
                }
            }
            if (ObjectUtil.isNotEmpty(reserve.getUserId())) {
                Admin admin = adminDao.selectByPrimaryKey(reserve.getUserId());
                if (ObjectUtil.isNotEmpty(admin)) {
                    reserve.setUserName(admin.getName());
                }
            }
        }
        return PageInfo.of(list);
    }

    public void update(Reserve reserve) {
        reserveDao.updateByPrimaryKeySelective(reserve);
    }

    public void delete(Integer id) {
        reserveDao.deleteByPrimaryKey(id);
    }
}
```
##### 后端：ReservelDao.java(Interface)
```java
@Repository
public interface ReserveDao extends Mapper<Reserve> {
    List<Reserve> findBySearch(@Param("params")Params params);
}
```
##### 后端：ReserveMapper.xml
```xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE mapper PUBLIC "-//mybatis.org//DTD Mapper 3.0//EN" "http://mybatis.org/dtd/mybatis-3-mapper.dtd">
<mapper namespace="com.example.dao.ReserveDao">
    <select id="findBySearch" resultType="com.example.entity.Reserve">
        select * from reserve
        order by reserve.id asc
    </select>
</mapper>
```
##### 后端：Reserve.java
```java
@Table(name = "reserve")
public class Reserve {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Integer id;
    @Column(name = "hotelId")
    private Integer hotelId;
    @Column(name = "userId")
    private Integer userId;
    @Column(name = "time")
    private String time;
    @Transient
    private String hotelName;
    @Transient
    private String userName;
}
```
##### 数据库：hotel.sql
```sql
CREATE TABLE `hotel` (
  `id` int(10) NOT NULL AUTO_INCREMENT COMMENT '主键ID',
  `name` varchar(255) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci DEFAULT NULL COMMENT '酒店名称',
  `price` varchar(255) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci DEFAULT NULL COMMENT '入住价格',
  `img` varchar(255) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci DEFAULT NULL COMMENT '酒店图片',
  `num` int(10) DEFAULT NULL COMMENT '剩余间数',
  PRIMARY KEY (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=9 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_unicode_ci COMMENT='酒店信息表';
```
##### 数据库：reserve.sql
```sql
CREATE TABLE `reserve` (
  `id` int(10) NOT NULL AUTO_INCREMENT COMMENT '主键ID',
  `hotelId` int(10) DEFAULT NULL COMMENT '酒店ID',
  `userId` int(10) DEFAULT NULL COMMENT '用户ID',
  `time` varchar(255) COLLATE utf8mb4_unicode_ci DEFAULT NULL COMMENT '预订时间',
  PRIMARY KEY (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=9 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_unicode_ci COMMENT='预订信息表';
```
#### 20250208 武哥毕设 14.[日志管理]
15Springboot+Vue+AOP实现登录、增删改查操作日志管理
##### (1)日志管理模块
【前端】
Layout.vue：
`<el-menu>` 引入下拉框组件
`<el-menu-item index="/log">` 下拉选项“日志管理”
index.js：
引入页面LogView.vue(配置路由path、name、component)
LogView.vue：
新建src.views.LogView.vue
`<el-input v-model="params.name" placeholder="请输入操作内容">` 输入框
`<el-input v-model="params.username"  placeholder="请输入操作人">` 输入框
`<el-table-column prop="name" label="操作内容">` 表格字段
`<el-table-column prop="time" label="操作时间">` 表格字段
`<el-table-column prop="username" label="操作人">` 表格字段
`<el-table-column prop="ip" label="ip">` 表格字段
data：`params:{name: '',username: '',pageNum: 1,pageSize: 5},tableData: [],total: 0,dialogFormVisible: false,form:{}`
method：`reset(){}` “清空”
`this.params = {pageNum: 1,pageSize: 5,name: '',username: ''}`
`<el-button @click="add()"  v-if="user.role === 'ROLE_ADMIN'">` “新增”设置“仅管理员可见”
`<el-button v-if="user.role !== 'ROLE_ADMIN'">` “预定”设置“仅管理员不可见”
`<el-button @click="edit(scope.row)" v-if="user.role === 'ROLE_ADMIN'">` “编辑”设置“仅管理员可见”
`<el-button v-if="user.role === 'ROLE_ADMIN'">` “删除”设置“仅管理员可见”
【后端】
log.sql：
拷贝表，新建表“操作日志表”
Params.java：
`private Integer username;` 定义变量username(与数据库保持一致)
Log.java：
新建com.example.entity.Log.java
`@Table(name = "log")`数据库表名
`private Integer id;`
`private String name;`
`private String time;`
`private String username;`
`private String ip;`
生成getter&setter、constructer
LogDao.java(Interface)：
`public interface AuditDao extends Mapper<Log>{}`
`List<Log> findBySearch(@Param("params")Params params);`
LogMapper.xml：
`<mapper namespace="com.example.dao.LogDao">`
`<select id="findBySearch" resultType="com.example.entity.Log">`
LogService.java：
`@Service`service层
`@Resource`引入dao层(`private LogDao logDao;`)
LogController.java：
`@CrossOrigin`跨域问题
`@RestController`controller层
`@RequestMapping("/log")`
`@Resource`引入service层(`private LogService logService;`)
##### (2)日志管理实现(面向切面编程AOP)
【后端】
pom.xml：
`<artifactId>spring-boot-starter-aop</artifactId>` AOP依赖
AutoLog.java(Annotation)：
新建com.example.common.AutoLog.java(Annotation) 自定义切面注解
`@Target(ElementType.METHOD)` 作用于方法
`@Retention(RetentionPolicy.RUNTIME)` 作用于运行时
`@Documented` 支持文档
`public @interface AutoLog {}`
`String value() default "";` 定义注解内容
LogAspect.java：
新建com.example.common.LogAspect.java
`@Component` 组件(交给SpringBoot管理)
`@Aspect` AOP处理器
`public class LogAspect(){}`
`@Around("@annotation(autoLog)")` 调用切面处理器
`joinPoint.proceed();` 调用切面注解
`String name = autoLog.value();` 操作内容，获取注解内容
`String time = DateUtil.now();` 操作时间，获取当前时间
`String username = "";` 操作人，定义操作人
`Admin user = JwtTokenUtils.getCurrentUser();` 操作人，获取当前用户(JWT登录放行无法获取token或用户信息)
`if (ObjectUtil.isNotNull(user)) {}` 操作人，如果不为空
`username = user.getName();` 操作人，赋值
`HttpServletRequest request = ((ServletRequestAttributes) RequestContextHolder.getRequestAttributes()).getRequest();` 操作人IP
`String ip = request.getRemoteAddr();` 操作人IP
`Result result = (Result) joinPoint.proceed();` 调用切面注解(返回Result)
`Object data = result.getData();` 操作人，获取Result对象(Object类型)
`if (data instanceof Admin) {}` 操作人，如果是Admin对象
`Admin admin = (Admin) data;` 操作人，类型强转
`username = admin.getName();` 操作人，赋值
`Log log = new Log(null, name, time, username, ip);` 封装数据(记录日志)
`@Resource()`引入service层(`private LogService logService;`)
`logService.add(log);` 添加到数据库
##### (3)日志管理切面注解
【后端】
BookController.java：
`@CrossOrigin`
`@RestController`
`@RequestMapping("/book")`
`public class BookController {}`
`@DeleteMapping("/{id}")`
`@AutoLog("删除图书信息")` 调用切面处理器
`public Result delete(@PathVariable Integer id){}`
`@PostMapping`
`@AutoLog("修改图书信息")` 调用切面处理器
`public Result save(@RequestBody Book book) {}`
AdminController.java：
`@CrossOrigin`
`@RestController`
`@RequestMapping("/admin")`
`public class AdminController {}`
`@PostMapping("/login")`
`@AutoLog("登录该系统")` 调用切面处理器
`public Result login(@RequestBody Admin admin) {}`
##### 前端：Layout.vue
```js
<el-menu-item index="/log">日志管理</el-menu-item>
```
##### 前端：index.js
```js
{
  path: 'log',
  component: LogView
}
```
##### 前端：LogView.vue
```js
<template>
  <div>
    <div>
      <el-input v-model="params.name" style="width: 200px; margin-right: 10px" placeholder="请输入操作内容"></el-input>
      <el-input v-model="params.username" style="width: 200px; margin-right: 10px" placeholder="请输入操作人"></el-input>
      <el-button type="warning" @click="findBySearch()">查询</el-button>
      <el-button type="warning" @click="reset()">清空</el-button>
    </div>
    <div>
      <el-table :data="tableData" style="width: 100%; margin: 15px 0px">
        <el-table-column prop="name" label="操作内容" width="180"></el-table-column>
        <el-table-column prop="time" label="操作时间" width="180"></el-table-column>
        <el-table-column prop="username" label="操作人" width="180"></el-table-column>
        <el-table-column prop="ip" label="ip" width="180"></el-table-column>
        <el-table-column label="操作">
          <template slot-scope="scope">
            <el-popconfirm title="确定删除吗？" @confirm="del(scope.row.id)">
              <el-button slot="reference" type="danger" style="margin-left: 5px">删除</el-button>
            </el-popconfirm>
          </template>
        </el-table-column>
      </el-table>
    </div>
    <div class="block">
      <el-pagination
          @size-change="handleSizeChange"
          @current-change="handleCurrentChange"
          :current-page="params.pageNum"
          :page-sizes="[5, 10, 15, 20]"
          :page-size="params.pageSize"
          layout="total, sizes, prev, pager, next"
          :total="total">
      </el-pagination>
    </div>
  </div>
</template>
<script>
import request from "@/utils/request";
export default {
  //name: "AdminView",
  data() {
    return {
      params:{
        name: '',
        username: '',
        pageNum: 1,
        pageSize: 5
      },
      tableData: [],
      total: 0,
      dialogFormVisible: false,
      form: {}
    }
  },
  created() {
    this.findBySearch();
  },
  methods: {
    findBySearch(){
      request.get("/log/search",{
        params:this.params
      }).then(res =>{
        if(res.code === '0'){
          this.tableData = res.data.list;
          this.total = res.data.total;
        }else{
          this.$message({
            message: res.msg,
            type: 'error'
          });
        }
      })
    },
    reset(){
      this.params = {
        pageNum: 1,
        pageSize: 5,
        name: '',
        username: ''
      }
      this.findBySearch();
    },
    handleSizeChange(pageSize) {
      this.params.pageSize = pageSize;
      this.findBySearch();
    },
    handleCurrentChange(pageNum) {
      this.params.pageNum = pageNum;
      this.findBySearch();
    },
    submit(){
      request.post("/log", this.form).then(res => {
        if (res.code === '0') {
          this.$message({
            message: '操作成功',
            type: 'success'
          });
          this.dialogFormVisible = false;
          this.findBySearch();
        } else {
          this.$message({
            message: res.msg,
            type: 'error'
          });
        }
      })
    },
    del(id) {
      request.delete("/log/" + id).then(res => {
        if (res.code === '0') {
          this.$message({
            message: '删除成功',
            type: 'success'
          });
          this.findBySearch();
        } else {
          this.$message({
            message: res.msg,
            type: 'success'
          });
        }
      })
    }
  }
}
</script>
```
##### 后端：AdminController.java
```java
@PostMapping("/login")
@AutoLog("登录该系统")
public Result login(@RequestBody Admin admin) {
    Admin loginUser = adminService.login(admin);
    return Result.success(loginUser);
}
```
##### 后端：BookController.java
```java
@PostMapping
@AutoLog("修改图书信息")
public Result save(@RequestBody Book book) {
    //adminService.add(admin);
    if (book.getId() == null) {
        bookService.add(book);
    } else {
        bookService.update(book);
    }
    return Result.success();
}
@DeleteMapping("/{id}")
@AutoLog("删除图书信息")
public Result delete(@PathVariable Integer id) {
    bookService.delete(id);
    return Result.success();
}
```
##### 后端：Params.java
```java
public class Params {
    private String name;
    private String username;
    private String phone;
    private String author;
    private Integer userId;
    private Integer PageNum;
    private Integer PageSize;
}
```
##### 后端：LogController.java
```java
@CrossOrigin
@RestController
@RequestMapping("/log")
public class LogController {
    @Resource
    private LogService logService;
    @PostMapping
    public Result save(@RequestBody Log log) {
       logService.add(log);
        return Result.success();
    }
    @GetMapping("/search")
    public Result findBySearch(Params params) {
        PageInfo<Log> info = logService.findBySearch(params);
        return Result.success(info);
    }
    @DeleteMapping("/{id}")
    public Result delete(@PathVariable Integer id) {
        logService.delete(id);
        return Result.success();
    }
}
```
##### 后端：LogService.java
```java
@Service
public class LogService {
    @Resource
    private LogDao logDao;
    public void add(Log type) {
        logDao.insertSelective(type);
    }
    public PageInfo<Log> findBySearch(Params params) {
        // 开启分页查询
        PageHelper.startPage(params.getPageNum(), params.getPageSize());
        // 接下来的查询会自动按照当前开启的分页设置来查询
        List<Log> list = logDao.findBySearch(params);
        return PageInfo.of(list);
    }
    public void delete(Integer id) {
        logDao.deleteByPrimaryKey(id);
    }
}
```
##### 后端：LogDao.java(Interface)
```java
@Repository
public interface LogDao extends Mapper<Log> {
    List<Log> findBySearch(@Param("params") Params params);
}
```
##### 后端：LogMapper.xml
```xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE mapper PUBLIC "-//mybatis.org//DTD Mapper 3.0//EN" "http://mybatis.org/dtd/mybatis-3-mapper.dtd">
<mapper namespace="com.example.dao.LogDao">
    <select id="findBySearch" resultType="com.example.entity.Log">
        select * from log
        <where>
            <if test="params != null and params.name != null and params.name != ''">
                and name like concat('%', #{ params.name }, '%')
            </if>
            <if test="params != null and params.username != null and params.username != ''">
                and username like concat('%', #{ params.username }, '%')
            </if>
        </where>
        order by time desc
    </select>
</mapper>
```
##### 后端：Log.java
```java
@Table(name = "type")
public class Log {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Integer id;

    @Column(name = "name")
    private String name;
    @Column(name = "time")
    private String time;
    @Column(name = "username")
    private String username;
    @Column(name = "ip")
    private String ip;
}
```
##### 后端：AutoLog.java(Annotation)
```java
import java.lang.annotation.*;

@Target(ElementType.METHOD)
@Retention(RetentionPolicy.RUNTIME)
@Documented
public @interface AutoLog {
    String value() default "";
}
```
##### 后端：LogAspect.java
```java
@Component
@Aspect
public class LogAspect {
    @Resource
    private LogService logService;
    @Around("@annotation(autoLog)")
    public Object doAround(ProceedingJoinPoint joinPoint, AutoLog autoLog) throws Throwable {
        // 操作内容，我们在注解里已经定义了value()，然后再需要切入的接口上面去写上对应的操作内容即可
        String name = autoLog.value();
        // 操作时间（当前时间）
        String time = DateUtil.now();
        // 操作人
        String username = "";
        Admin user = JwtTokenUtils.getCurrentUser();
        if (ObjectUtil.isNotNull(user)) {
            username = user.getName();
        }
        // 操作人IP
        HttpServletRequest request = ((ServletRequestAttributes) RequestContextHolder.getRequestAttributes()).getRequest();
        String ip = request.getRemoteAddr();
        // 执行具体的接口
        Result result = (Result) joinPoint.proceed();
        Object data = result.getData();
        if (data instanceof Admin) {
            Admin admin = (Admin) data;
            username = admin.getName();
        }
        // 再去往日志表里写一条日志记录
        Log log = new Log(null, name, time, username, ip);
        logService.add(log);
        // 你可以走了，去返回前台报到吧~
        return result;
    }
}
```
##### 后端：pom.xml
```xml
<dependency>
  <groupId>org.springframework.boot</groupId>
  <artifactId>spring-boot-starter-aop</artifactId>
</dependency>
```
##### 数据库：log.sql
```sql
CREATE TABLE `log` (
  `id` int(10) NOT NULL AUTO_INCREMENT COMMENT '主键ID',
  `name` varchar(255) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci DEFAULT NULL COMMENT '操作内容',
  `time` varchar(255) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci DEFAULT NULL COMMENT '操作时间',
  `username` varchar(255) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci DEFAULT NULL COMMENT '操作人',
  `ip` varchar(255) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci DEFAULT NULL COMMENT '操作人IP',
  PRIMARY KEY (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=42 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_unicode_ci COMMENT='操作日志表';
```
#### 20250209 武哥毕设 15.*系统公告*
16Springboot+Vue实现系统公告（通知）增删改查、首页系统公告（通知）展示
##### (1)系统公告模块
【前端】
Layout.vue：
`<el-menu>` 引入下拉框组件
`<el-menu-item index="/notice">` 下拉选项“系统公告”
`<el-menu-item index="/notice" v-if="user.role === 'ROLE_ADMIN'">` “系统公告”设置“仅管理员可见”
index.js：
引入页面NoticeView.vue(配置路由path、name、component)
NoticeView.vue：
新建src.views.NoticeView.vue
`<el-input v-model="params.name" placeholder="请输入公告标题">` 输入框
`<el-table-column prop="name" label="公告标题">` 表格字段
`<el-table-column prop="content" label="公告内容">` 表格字段
`<el-table-column prop="time" label="更新时间">` 表格字段
`<el-input v-model="form.name">` 输入框“公告标题”
`<el-input v-model="form.content" type="textarea">` 输入框(多行)“公告内容”
HomeView.vue：
`<el-collapse v-model="activeName" accordion>`引入折叠面板组件(手风琴效果) 
`<el-collapse-item v-for="item in data">` 遍历数据
`<el-collapse-item v-for="item in data" :title="item.name">` 绑定参数(对应数据库字段)
`<el-collapse-item v-for="item in data" :title="item.name"> :name="item.id">` 绑定参数(对应数据库字段)
`<div>{{item.content}}</div>` 绑定参数(对应数据库字段)
data：`activeNames: '1',data: []`
mounted：`this.findNotice();` 页面加载时调用
method：`findNotice(){}` “清空”
`import request from "@/utils/request";`
发送请求`request.get("/notice")`
处理请求`.then(res => {处理请求})`
判断成功`if(res.code === '0'){}else{判断失败}`
数据赋值`this.data = res.data;`
数据赋值`this.activeName = res.data[0].id;` 默认展开第一条
消息提示`this.$message.error(res.msg)`后端异常处理
【后端】
notice.sql：
拷贝表，新建表“系统公告表”
Notice.java：
新建com.example.entity.Notice.java
`@Table(name = "notice")`数据库表名
`private Integer id;`
`private String name;`
`private String content;`
`private String time;`
生成getter&setter
NoticeDao.java(Interface)：
`public interface AuditDao extends Mapper<Notice>{}`
NoticeMapper.xml：
`<mapper namespace="com.example.dao.NoticeDao">`
`<select id="findBySearch" resultType="com.example.entity.Notice">`
NoticeService.java：
`@Service`service层
`@Resource`引入dao层(`private NoticeDao noticeDao;`)
NoticeController.java：
`@CrossOrigin`跨域问题
`@RestController`controller层
`@RequestMapping("/notice")`
`@Resource`引入service层(`private NoticeService noticeService;`)
##### 前端：Layout.vue
```js
<el-menu-item index="/notice">系统公告</el-menu-item>
```
##### 前端：index.js
```js
{
  path: 'notice',
  component: NoticeView
}
```
##### 前端：HomeView.vue
```js
<div style="width: 50%">
  <div style="margin-bottom: 15px; font-weight: bold; font-size: 18px">系统公告</div>
  <el-collapse v-model="activeName" accordion>
    <el-collapse-item v-for="item in data" :title="item.name" :name="item.id">
      <div>{{item.content}}</div>
    </el-collapse-item>
  </el-collapse>
</div>
```
##### 前端：NoticeView.vue
```js
<template>
  <div>
    <div>
      <el-input v-model="params.name" style="width: 200px; margin-right: 10px" placeholder="请输入公告标题"></el-input>
      <el-button type="warning" @click="findBySearch()">查询</el-button>
      <el-button type="warning" @click="reset()">清空</el-button>
      <el-button type="primary" @click="add()">新增</el-button>
    </div>
    <div>
      <el-table :data="tableData" style="width: 100%; margin: 15px 0px">
        <el-table-column prop="name" label="公告标题" width="180"></el-table-column>
        <el-table-column prop="content" label="公告内容" width="180"></el-table-column>
        <el-table-column prop="time" label="发布时间" width="180"></el-table-column>
        <el-table-column label="操作">
          <template slot-scope="scope">
            <el-button type="primary" @click="edit(scope.row)">编辑</el-button>
            <el-popconfirm title="确定删除吗？" @confirm="del(scope.row.id)">
              <el-button slot="reference" type="danger" style="margin-left: 5px">删除</el-button>
            </el-popconfirm>
          </template>
        </el-table-column>
      </el-table>
    </div>
    <div class="block">
      <el-pagination
          @size-change="handleSizeChange"
          @current-change="handleCurrentChange"
          :current-page="params.pageNum"
          :page-sizes="[5, 10, 15, 20]"
          :page-size="params.pageSize"
          layout="total, sizes, prev, pager, next"
          :total="total">
      </el-pagination>
    </div>
    <div>
      <el-dialog title="请填写姓名" :visible.sync="dialogFormVisible" width="35%">
        <el-form :model="form">
          <el-form-item label="公告标题" label-width="15%">
            <el-input v-model="form.name" autocomplete="off" style="width:90%"></el-input>
          </el-form-item>
          <el-form-item label="公告内容" label-width="15%">
            <el-input type="textarea" v-model="form.content" autocomplete="off" style="width:90%"></el-input>
          </el-form-item>
        </el-form>
        <div slot="footer" class="dialog-footer">
          <el-button @click="dialogFormVisible = false">取 消</el-button>
          <el-button type="primary" @click="submit()">确 定</el-button>
        </div>
      </el-dialog>
    </div>
  </div>
</template>
<script>
import request from "@/utils/request";
export default {
  //name: "AdminView",
  data() {
    return {
      params:{
        name: '',
        pageNum: 1,
        pageSize: 5
      },
      tableData: [],
      total: 0,
      dialogFormVisible: false,
      form: {}
    }
  },
  created() {
    this.findBySearch();
  },
  methods: {
    findBySearch(){
      request.get("/notice/search",{
        params:this.params
      }).then(res =>{
        if(res.code === '0'){
          this.tableData = res.data.list;
          this.total = res.data.total;
        }else{
          this.$message({
            message: res.msg,
            type: 'error'
          });
        }
      })
    },
    reset(){
      this.params = {
        pageNum: 1,
        pageSize: 5,
        name: '',
        phone: ''
      }
      this.findBySearch();
    },
    handleSizeChange(pageSize) {
      this.params.pageSize = pageSize;
      this.findBySearch();
    },
    handleCurrentChange(pageNum) {
      this.params.pageNum = pageNum;
      this.findBySearch();
    },
    add(){
      this.form = {};
      this.dialogFormVisible = true;
    },
    edit(obj) {
      this.form = obj;
      this.dialogFormVisible = true;
    },
    submit(){
      request.post("/notice", this.form).then(res => {
        if (res.code === '0') {
          this.$message({
            message: '操作成功',
            type: 'success'
          });
          this.dialogFormVisible = false;
          this.findBySearch();
        } else {
          this.$message({
            message: res.msg,
            type: 'error'
          });
        }
      })
    },
    del(id) {
      request.delete("/notice/" + id).then(res => {
        if (res.code === '0') {
          this.$message({
            message: '删除成功',
            type: 'success'
          });
          this.findBySearch();
        } else {
          this.$message({
            message: res.msg,
            type: 'success'
          });
        }
      })
    }
  }
}
</script>
```
##### 后端：NoticeController.java
```java
@CrossOrigin
@RestController
@RequestMapping("/notice")
public class NoticeController {
    @Resource
    private NoticeService noticeService;
    @AutoLog("更新日志操作")
    @PostMapping
    public Result update(@RequestBody Notice notice) {
        if (ObjectUtil.isEmpty(notice.getId())) {
            noticeService.add(notice);
        } else {
            noticeService.update(notice);
        }
        return Result.success();
    }
    @GetMapping
    public Result findTop() {
        List<Notice> list = noticeService.findTop();
        return Result.success(list);
    }
    @GetMapping("/search")
    public Result findBySearch(Params params) {
        PageInfo<Notice> info = noticeService.findBySearch(params);
        return Result.success(info);
    }
    @DeleteMapping("/{id}")
    public Result delete(@PathVariable Integer id) {
        noticeService.delete(id);
        return Result.success();
    }
}
```
##### 后端：NoticeService.java
```java
@Service
public class NoticeService {
    @Resource
    private NoticeDao noticeDao;
    public void add(Notice notice) {
        notice.setTime(DateUtil.now());
        noticeDao.insertSelective(notice);
    }
    public PageInfo<Notice> findBySearch(Params params) {
        // 开启分页查询
        PageHelper.startPage(params.getPageNum(), params.getPageSize());
        // 接下来的查询会自动按照当前开启的分页设置来查询
        List<Notice> list = noticeDao.findBySearch(params);
        return PageInfo.of(list);
    }
    public void update(Notice notice) {
        notice.setTime(DateUtil.now());
        noticeDao.updateByPrimaryKeySelective(notice);
    }
    public void delete(Integer id) {
        noticeDao.deleteByPrimaryKey(id);
    }
    public List<Notice> findTop() {
        return noticeDao.findTop3();
    }
}
```
##### 后端：NoticeMapper.xml
```xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE mapper PUBLIC "-//mybatis.org//DTD Mapper 3.0//EN" "http://mybatis.org/dtd/mybatis-3-mapper.dtd">
<mapper namespace="com.example.dao.NoticeDao">
    <select id="findBySearch" resultType="com.example.entity.Notice">
        select * from notice
        <where>
            <if test="params != null and params.name != null and params.name != ''">
                and name like concat('%', #{ params.name }, '%')
            </if>
        </where>
        order by time desc
    </select>
</mapper>
```
##### 后端：NoticeDao.java(Interface)
```java
@Repository
public interface NoticeDao extends Mapper<Notice> {
    List<Notice> findBySearch(@Param("params") Params params);
    @Select("select * from notice order by time desc limit 3")
    List<Notice> findTop3();
}
```
##### 后端：Notice.java
```java
@Table(name = "notice")
public class Notice {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Integer id;
    @Column(name = "name")
    private String name;
    @Column(name = "content")
    private String content;
    @Column(name = "time")
    private String time;
}
```
##### 数据库：notice.sql
```sql
CREATE TABLE `notice` (
  `id` int(10) NOT NULL AUTO_INCREMENT COMMENT '主键ID',
  `name` varchar(255) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci DEFAULT NULL COMMENT '公告标题',
  `content` text CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci COMMENT '公告内容',
  `time` varchar(255) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci DEFAULT NULL COMMENT '公告时间',
  PRIMARY KEY (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=47 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_unicode_ci COMMENT='系统公告表';
```
#### 20250209 武哥毕设 16.[登录验证码]
17Springboot+Vue实现登录注册图形验证码功能
##### (1)图形验证码
【前端】
Login.View.vue：
`<el-input>` 引入输入框组件
`<el-input v-model="admin.verCode">` 绑定用户输入“验证码”
`<img/>` 引入图片组件
`<img :src="captchaUrl"/>` 绑定图片地址
`<img :src="captchaUrl" @click="clickImg()" />` 绑定事件
data：`admin:{},key: '',captchaUrl: ''`
data：`admin:{},captchaUrl: 'http://localhost:8080/captcha'` 前后端不分离时用
data：`admin:{},captchaUrl: 'http://localhost:8080/captcha?key='` 前后端分离时用
mounted：(页面初始化时)
`this.key = Math.random();` key值生成随机数
`this.captchaUrl = 'http://localhost:8080/api/captcha?key=' + this.key;` 前后端分离时用
method：`login(){}` “登录”
`request.post("/admin/login?key=", this.key)` 传递参数key
`this.key = Math.random();` key重新生成随机数
`this.captchaUrl = 'http://localhost:8080/api/captcha?key=' + this.key;` 刷新验证码
`this.admin.verCode = ''` 清空输入框
method：`clickImg(){}` “刷新验证码”
`this.key = Math.random();` key重新生成随机数
`this.captchaUrl = 'http://localhost:8080/api/captcha?key=' + this.key;` 刷新验证码
【后端】
pom.xml：
`<artifactId>easy-captcha</artifactId>` easy-captcha依赖
CaptureController.java：
新建com.example.controller.CaptureController.java
`@CrossOrigin`跨域问题
`@RestController`controller层
`@RequestMapping`
`public class CaptureController{}`
`@RequestMapping("/captcha")`

`public void captcha(HttpServletRequest request, HttpServletResponse response) throws Exception{}`
`SpecCaptcha captcha = new SpecCaptcha(135, 33, 5);` 指定验证码的长宽以及字符的个数
`captcha.setCharType(Captcha.TYPE_NUM_AND_UPPER);` 指定验证码类型
`CaptchaUtil.out(captcha, request, response);` 返回验证码到前端(JarEditor插件修改jar内配置文件)

注意：前后端不分离时候可以使用session原理，前后端分离时要在后台另存一份(存到redis或Map里)
`public void captcha(@RequestParam String key, HttpServletRequest request, HttpServletResponse response) throws Exception{}`
`SpecCaptcha captcha = new SpecCaptcha(135, 33, 5);` 指定验证码的长宽以及字符的个数
`captcha.setCharType(Captcha.TYPE_NUM_AND_UPPER);` 指定验证码类型
`CaptureConfig.CAPTURE_MAP.put(key, captcha.text().toLowerCase());` Map(键值对)另存验证码
`CaptchaUtil.out(captcha, request, response);` 返回验证码到前端(JarEditor修改jar内配置文件)
CaptureConfig.java：
新建com.example.common.CaptureConfig.java(Map另存验证码值)
`@Component` 组件(交给SpringBoot管理)
`public static Map<String, String> CAPTURE_MAP = new HashMap<>();`
AdminController.java：
`@CrossOrigin`
`@RestController`
`@RequestMapping("/admin")`
`public class AdminController {}`
`@PostMapping("/login")`
`@AutoLog("登录该系统")`
`public Result login(@RequestBody Admin admin,@RequestParam String key){}` 传递参数key
`public Result login(@RequestBody Admin admin, @RequestParam String key, HttpServletRequest request){}`
`if (!admin.getVerCode().toLowerCase().equals(CaptureConfig.CAPTURE_MAP.get(key))) {}` 判断验证码是否输入正确
`CaptchaUtil.clear(request);` 清空验证码(session前后端不分离)
`return Result.error("验证码不正确");`
`CaptureConfig.CAPTURE_MAP.remove(key);` 清空验证码(Map前后端分离)
Admin.java：
`@Transient` 非数据库字段
`private String verCode;` 定义变量verCode
生成getter&setter
##### (2)算数验证码
【后端】
CaptureController.java：
`ArithmeticCaptcha captcha = new ArithmeticCaptcha(135, 33);` 指定验证码的长宽以及字符的个数
`captcha.setLen(4);` 几位数运算，默认是两位
`captcha.getArithmeticString();` 获取运算的公式：3+2=?
`captcha.text();` 获取运算的结果：5
`CaptureConfig.CAPTURE_MAP.put(key, captcha.text().toLowerCase());` Map另存验证码值(键值对) 
`CaptchaUtil.out(captcha, request, response);` 返回验证码到前端(JarEditor修改jar内配置文件)
pom.xml：
`<artifactId>nashorn-core</artifactId>` nashorn-core依赖
注意：【报错】关于Cannot invoke “javax.script.ScriptEngine.eval(String)“ because “engine“ is null的俩种解决方案https://blog.csdn.net/m0_69519887/article/details/140420512
##### (2)登录背景图
【前端】
LoginView.vue：
`<div class="login-container">`
`<style scoped>`
##### 前端：LoginView.vue
```js
<template>
  <div class="login-container">
    <div style="width: 400px; height: 400px; margin: 150px auto; background-color:rgba(107,149,224,0.5); border-radius: 10px">
      <div style="width: 100%; height: 100px; font-size: 30px; line-height: 100px; text-align: center; color: #4a5ed0">欢迎登录</div>
      <div style="margin-top: 25px; text-align: center; height: 320px;">
        <el-form :model="admin">
          <el-form-item>
            <el-input v-model="admin.name" prefix-icon="el-icon-user" style="width: 80%" placeholder="请输入用户名"></el-input>
          </el-form-item>
          <el-form-item>
            <el-input v-model="admin.password" show-password prefix-icon="el-icon-lock" style="width: 80%" placeholder="请输入密码"></el-input>
          </el-form-item>
          <el-form-item>
            <div style="display: flex; justify-content: center">
              <el-input v-model="admin.verCode" prefix-icon="el-icon-user" style="width: 42%; margin-right: 10px" placeholder="请输入验证码"></el-input>
              <img :src="captchaUrl" @click="clickImg()" width="140px" height="33px" />
            </div>
          </el-form-item>
          <el-form-item>
            <el-button style="width: 80%; margin-top: 10px" type="primary" @click="login()">登录</el-button>
          </el-form-item>
          <div style="text-align: center">
            未有账号？<a href="javascript:void(0)" style="text-decoration: none" @click="navRegister">点击注册</a>
          </div>
        </el-form>
      </div>
    </div>
  </div>
</template>
<script>
import request from "@/utils/request";

export default {
  name: "Login",
  data() {
    return {
      admin:{
        //name: '',
        //password: ''
      },
      key:'',
      captchaUrl: ''
      // key:Math.random(),
      // captchaUrl: 'http://localhost:8080/api/captcha'
      // captchaUrl: 'http://localhost:8080/api/captcha?key=' + this.key
    }
  },
  // 页面加载的时候，做一些事情，在created里面
  mounted() {
    this.key = Math.random();
    this.captchaUrl = 'http://localhost:8080/api/captcha?key=' + this.key;
  },
  methods: {
    navRegister() {
      this.$router.push("/register")
    },
    login() {
      request.post("/admin/login?key=" + this.key, this.admin).then(res => {
        if (res.code === '0') {
          this.$message.success("登录成功");
          localStorage.setItem("user", JSON.stringify(res.data));
          this.$router.push("/");
        } else {
          this.$message.error(res.msg);
          this.key = Math.random();
          this.captchaUrl = 'http://localhost:8080/api/captcha?key=' + this.key;
          this.admin.verCode = ''
        }
      })
    },
    clickImg() {
      this.key = Math.random();
      this.captchaUrl = 'http://localhost:8080/api/captcha?key=' + this.key;
    }
  }
}
</script>
<style scoped>
.login-container {
  height: 100vh;
  overflow: hidden;
  background-image: url("@/assets/login_bg.jpg");
  background-size: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>
```
##### 后端：AdminController.java
```java
@PostMapping("/login")
@AutoLog("登录该系统")
public Result login(@RequestBody Admin admin, @RequestParam String key, HttpServletRequest request) {
      // 判断验证码对不对
    if (!admin.getVerCode().toLowerCase().equals(CaptureConfig.CAPTURE_MAP.get(key))) {
        // 如果不相等，说明验证不通过
        CaptchaUtil.clear(request);
        return Result.error("验证码不正确");
    }
    Admin loginUser = adminService.login(admin);
    CaptureConfig.CAPTURE_MAP.remove(key);
    return Result.success(loginUser);
}
```
##### 后端：Admin.java
```java
@Table(name = "admin")
public class Admin {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Integer id;
    @Column(name = "name")
    private String name;
    @Column(name = "password")
    private String password;
    @Column(name = "sex")
    private String sex;
    @Column(name = "age")
    private Integer age;
    @Column(name = "phone")
    private String phone;
    @Column(name = "role")
    private String role;

    @Transient
    private String token;
    @Transient
    private String verCode;
}
```
##### 后端：CaptureController.java
```java
@CrossOrigin
@RestController
@RequestMapping
public class CaptureController {
    @RequestMapping("/captcha")
    public void captcha(@RequestParam String key, HttpServletRequest request, HttpServletResponse response) throws Exception {

//        // 指定验证码的长宽以及字符的个数
//        SpecCaptcha captcha = new SpecCaptcha(135, 33, 5);
//        captcha.setCharType(Captcha.TYPE_NUM_AND_UPPER);
//        // 首先把验证码在后台保存一份，但是不能保存在session，可以存在redis，也可以存在后台的某个Map里面
//        CaptureConfig.CAPTURE_MAP.put(key, captcha.text().toLowerCase());
//        CaptchaUtil.out(captcha, request, response);//报错解决(JarEditor插件)
        // 算术类型
        ArithmeticCaptcha captcha = new ArithmeticCaptcha(135, 33);
        captcha.setLen(4);  // 几位数运算，默认是两位
        captcha.getArithmeticString();  // 获取运算的公式：3+2=?
        captcha.text();  // 获取运算的结果：5
        CaptureConfig.CAPTURE_MAP.put(key, captcha.text().toLowerCase());
        CaptchaUtil.out(captcha, request, response);
    }
}
```
##### 后端：CaptureConfig.java
```java
@Component
public class CaptureConfig {
    public static Map<String, String> CAPTURE_MAP = new HashMap<>();
}
```
##### 后端：WebConfig.java
```java
@click="clickImg()"
.excludePathPatterns("/api/captcha")
```
##### 后端：pom.xml
```xml
<dependency>
    <groupId>com.github.whvcse</groupId>
    <artifactId>easy-captcha</artifactId>
    <version>1.6.2</version>
</dependency>
<dependency>
	<groupId>org.openjdk.nashorn</groupId>
	<artifactId>nashorn-core</artifactId>
	<version>15.4</version>
</dependency>
```
#### 20250211 武哥毕设 17.*统计图表echarts*
echarts官网：https://echarts.apache.org/examples/zh/index.html
18Springboot+Vue集成echarts实现数据统计
##### (1)饼图模块
【前端】
HomeView.vue：
`import * as echarts from "echarts";` 引入echarts
`<div style="width: 50%; margin-top: 50px">` 作图区域
`<div id="bie" style="width: 100%; height: 400px">` 作图区域
mounted：`this.initBie(data);`
method：`initBie(data){}`
mounted：`this.initEcharts();`
method：`initEcharts(){}`
发送请求`request.get("/book/echarts/bie")`
处理请求`.then(res => {处理请求})`
判断成功`if(res.code === '0'){}else{判断失败}`
数据赋值`this.initBie(res.data)` 调用方法赋值数据
消息提示`this.$message.error(res.msg)`后端异常处理
【后端】
BookController.java：
`@CrossOrigin`
`@RestController`
`@RequestMapping("/book")`
`public class BookController{}`
`@GetMapping("/echarts/bie")`
`public Result bie(){}`
`List<Book> list = bookService.findAll();`
`Map<String, Long> collect = list.stream()` List转流、返回Map
`.filter(x -> ObjectUtil.isNotEmpty(x.getTypeName()))` 过滤条件TypeName不为空
`.collect(Collectors.groupingBy(Book::getTypeName, Collectors.counting()));` 根据类型、数量分组
`List<Map<String, Object>> mapList = new ArrayList<>();` 定义返回给前端的数据结构
`if (CollectionUtil.isNotEmpty(collect)){}` 返回Map数据不为空
`for (String key : collect.keySet()){}` 遍历向数据结构塞数据
`Map<String, Object> map = new HashMap<>();` 定义HashMap
`map.put("name", key);` 塞数据“key”
`map.put("value", collect.get(key));` 塞数据“value”
`mapList.add(map);` 添加Map到List
`return Result.success(mapList);` List返回给前端
BookService.java：
`@Service`
`public class BookService{}`
`public List<Book> findAll(){}`
`return bookDao.findAll();`
BookDao.java：
`@Repository`
`public interface BookDao extends Mapper<Book>{}`
`@Select("select book.*,type.name as typeName from book left join type on book.typeId = type.id")`
`List<Book> findAll();`
##### (2)柱状、折线图模块
【前端】
HomeView.vue：
`<div style="width: 50%; margin-top: 50px">` 作图区域
`<div id="bar" style="width: 100%; height: 400px">` 作图区域
`<div id="line" style="width: 100%; height: 400px">` 作图区域
mounted：`this.initBar(xAxis,yAxis);`
mounted：`this.initLine(xAxis,yAxis);`
method：`initEcharts(){}`
发送请求`request.get("/book/echarts/bar")`
处理请求`.then(res => {处理请求})`
判断成功`if(res.code === '0'){}else{判断失败}`
数据赋值`let map = res.data;`
数据赋值`this.initBar(map.xAxis, map.yAxis)` 调用方法赋值数据
数据赋值`this.initLine(map.xAxis, map.yAxis)` 调用方法赋值数据
消息提示`this.$message.error(res.msg)`后端异常处理
【后端】
BookController.java：
`@CrossOrigin`
`@RestController`
`@RequestMapping("/book")`
`public class BookController{}`
`@GetMapping("/echarts/bar")`
`public Result bie(){}`
`List<Book> list = bookService.findAll();`
`Map<String, Long> collect = list.stream()` List转流、返回Map
`.filter(x -> ObjectUtil.isNotEmpty(x.getTypeName()))` 过滤条件TypeName不为空
`.collect(Collectors.groupingBy(Book::getTypeName, Collectors.counting()));` 根据类型、数量分组
`List<String> xAxis = new ArrayList<>();` 定义返回给前端的数据结构(X轴)
`List<Long> yAxis = new ArrayList<>();` 定义返回给前端的数据结构(Y轴)
`if (CollectionUtil.isNotEmpty(collect)){}` 返回Map数据不为空
`for (String key : collect.keySet()){}` 遍历向数据结构塞数据
`xAxis.add(key);` 塞数据“key”
`yAxis.add(collect.get(key));` 塞数据“value”
`Map<String, Object> map = new HashMap<>();` 定义HashMap
`map.put("xAxis", xAxis);` 塞数据“x轴”
`map.put("yAxis", yAxis);` 塞数据“y轴”
`return Result.success(map);` Map返回给前端
##### 前端：HomeView.vue
```java
<template>
  <div>
    <div style="display: flex">
      <div style="flex: 1;">
        <div style="margin-bottom: 15px; font-weight: bold; font-size: 18px">系统公告</div>
        <el-collapse v-model="activeName" accordion>
          <el-collapse-item v-for="item in data" :title="item.name" :name="item.id">
            <div style="padding: 0 20px">{{ item.content }}</div>
          </el-collapse-item>
        </el-collapse>
      </div>
      <div style="width: 50px"></div>
      <div style="flex: 1; margin-top: 50px;">
        <div id="bie" style="width: 100%; height: 400px"></div>
      </div>
    </div>
    <div style="display: flex">
      <div style="flex: 1; margin-top: 50px">
        <div id="bar" style="width: 100%; height: 400px"></div>
      </div>
      <div style="flex: 1; margin-top: 50px">
        <div id="line" style="width: 100%; height: 400px"></div>
      </div>
    </div>
  </div>
</template>
<script>

import request from "@/utils/request";
import * as echarts from "echarts";

export default {
  name: 'HomeView',
  data() {
    return {
      activeName: '1',
      data: []
    };
  },
  mounted() {
    this.findNotice();
    this.initEcharts();
    //this.initBar();
  },
  methods: {
    findNotice(){
      request.get("/notice").then(res =>{
        if(res.code === '0'){
          this.data = res.data;
          this.activeName = res.data[0].id;
        }else{
          this.$message.error(res.msg);
        }
      })
    },
    initEcharts() {
      request.get("/book/echarts/bie").then(res => {
        if (res.code === '0') {
          // 开始去渲染饼图数据啦
          this.initBie(res.data)
        } else {
          this.$message.error(res.msg)
        }
      })
      request.get("/book/echarts/bar").then(res => {
        if (res.code === '0') {
          // 开始去渲染柱状图数据啦
          let map = res.data;
          this.initBar(map.xAxis, map.yAxis)
          // 开始去渲染折线图数据啦
          this.initLine(map.xAxis, map.yAxis)
        } else {
          this.$message.error(res.msg)
        }
      })
    },
    initBie(data) {
      let chartDom = document.getElementById('bie');
      let myChart = echarts.init(chartDom);
      let option;

      option = {
        title: {
          text: '图书统计(饼图)',
          subtext: '统计维度：图书分类',
          left: 'center'
        },
        tooltip: {
          trigger: 'item'
        },
        legend: {
          orient: 'vertical',
          left: 'left'
        },
        series: [
          {
            name: '图书分类',
            type: 'pie',
            radius: '50%',
            data: data,
            //     [
            //   { value: 1048, name: '情感类图书' },
            //   { value: 735, name: '技术类图书' },
            //   { value: 580, name: '生活类图书' },
            //   { value: 484, name: '悬疑类图书' }
            // ],
            emphasis: {
              itemStyle: {
                shadowBlur: 10,
                shadowOffsetX: 0,
                shadowColor: 'rgba(0, 0, 0, 0.5)'
              }
            }
          }
        ]
      };

      option && myChart.setOption(option);

    },
    initBar(xAxis,yAxis) {
      let chartDom = document.getElementById('bar');
      let myChart = echarts.init(chartDom);
      let option;

      option = {
        title: {
          text: '图书统计（柱状图）',
          subtext: '统计维度：图书分类',
          left: 'center'
        },
        xAxis: {
          type: 'category',
          data: xAxis
          //['情感类图书', '技术类图书', '生活类图书', '悬疑类图书']
        },
        yAxis: {
          type: 'value'
        },
        series: [
          {
            data: yAxis,
            //[1048, 735, 580, 484],
            type: 'bar',
            showBackground: true,
            backgroundStyle: {
              color: 'rgba(180, 180, 180, 0.2)'
            }
          }
        ]
      };

      option && myChart.setOption(option);
    },
    initLine(xAxis, yAxis) {
      let chartDom = document.getElementById('line');
      let myChart = echarts.init(chartDom);
      let option;

      option = {
        title: {
          text: '图书统计（折线图）',
          subtext: '统计维度：图书分类',
          left: 'center'
        },
        xAxis: {
          type: 'category',
          data: xAxis
        },
        yAxis: {
          type: 'value'
        },
        series: [
          {
            data: yAxis,
            type: 'line'
          }
        ]
      };

      option && myChart.setOption(option);
    }
  }
}
</script>
```
##### 后端：BookController.java
```java
@GetMapping("/echarts/bie")
public Result bie() {
    // 查询出所有图书
    List<Book> list = bookService.findAll();
    Map<String, Long> collect = list.stream()
            .filter(x -> ObjectUtil.isNotEmpty(x.getTypeName()))
            .collect(Collectors.groupingBy(Book::getTypeName, Collectors.counting()));
    // 最后返回给前端的数据结构
    List<Map<String, Object>> mapList = new ArrayList<>();
    if (CollectionUtil.isNotEmpty(collect)) {
        for (String key : collect.keySet()) {
            Map<String, Object> map = new HashMap<>();
            map.put("name", key);
            map.put("value", collect.get(key));
            mapList.add(map);
        }
    }
    return Result.success(mapList);
}

@GetMapping("/echarts/bar")
public Result bar() {
    // 查询出所有图书
    List<Book> list = bookService.findAll();
    Map<String, Long> collect = list.stream()
            .filter(x -> ObjectUtil.isNotEmpty(x.getTypeName()))
            .collect(Collectors.groupingBy(Book::getTypeName, Collectors.counting()));

    List<String> xAxis = new ArrayList<>();
    List<Long> yAxis = new ArrayList<>();
    if (CollectionUtil.isNotEmpty(collect)) {
        for (String key : collect.keySet()) {
            xAxis.add(key);
            yAxis.add(collect.get(key));
        }
    }

    Map<String, Object> map = new HashMap<>();
    map.put("xAxis", xAxis);
    map.put("yAxis", yAxis);

    return Result.success(map);
}
```
##### 后端：BookService.java
```java
public List<Book> findAll() {
    return bookDao.findAll();
}
```
##### 后端：BookDao.java
```java
@Repository
public interface BookDao extends Mapper<Book> {
    List<Book> findBySearch(@Param("params")Params params);

    @Select("select book.*,type.name as typeName from book left join type on book.typeId = type.id")
    List<Book> findAll();
}
```
##### 安装：【echarts】
安装路径：`E:\eld901\Idea\vue` (Vue工程)
安装命令：`npm install echarts --save`
#### 20250212 武哥毕设 18.*富文本编辑wangeditor*
wangeditor官网：https://www.wangeditor.com/v4
19Springboot+Vue集成富文本编辑器实现发帖、发博客等功能
##### (1)富文本编辑
【前端】
BookView.vue：
`import E from 'wangeditor'` 引入wangeditor
`<el-form-item label="图书介绍" label-width="25%">` 富文本区域
`<div id="editor">` 富文本区域
`const editor = new E('#editor')` 初始化富文本编辑器
`editor = new E('#editor')` 初始化富文本编辑器
`editor.config.placeholder = '请输入内容'` 默认提示
`editor.config.uploadFileName = 'file'` 上传文件变量名
`editor.config.uploadImgServer = 'http://localhost:8080/files/wang/upload'` 上传文件接口
`editor.create()` 初始化富文本编辑器
`editor.txt.html(content)` “编辑”时传递富文本内容
`<el-dialog title="图书介绍" :visible.sync="editorVisible" width="50%">` 引入对话框组件
`<div v-html="viewData" class="w-e-text"></div>` 渲染html页面内容//this.form.content
`<el-button type="success" @Click="viewEditor(scope.row.content)">` “点击查看”
data：`editorVisible: false`
data：`viewData:''` 
method：`add(){}` “新增”
`initWangEditor("");` 初始化，富文本编辑器为空
method：`edit(obj){}` “编辑”
`initWangEditor(obj.content ? this.form.content : "");` “编辑”时传递富文本内容
method：`submit(){}` “提交”
`this.form.content = editor.txt.html();` “提交”时传递内容到后台
method：`viewEditor(data){}` “点击查看”
`this.viewData = data;` 
`this.editorVisible = true;` 开启对话框
【后端】
book.sql：
在"图书信息表"中新建字段(content)，“图书介绍”
Book.java：
`@Column(name = "content")` 关联数据库表字段
`private String content;` 定义变量content
生成getter&setter
FileController.java：
`@PostMapping("/wang/upload")` 文件上传接口
##### 前端：BookView.vue
```js
<template>
  <div>
    <div>
      <el-input v-model="params.name" style="width: 200px; margin-right: 10px" placeholder="请输入图书名称"></el-input>
      <el-input v-model="params.author" style="width: 200px; margin-right: 10px" placeholder="请输入图书作者"></el-input>
      <el-button type="warning" @click="findBySearch()">查询</el-button>
      <el-button type="warning" @click="reset()">清空</el-button>
      <el-button type="primary" @click="add()"  v-if="user.role !== 'ROLE_STUDENT'">新增</el-button>
    </div>
    <div>
      <el-table :data="tableData" style="width: 100%; margin: 15px 0px">
        <el-table-column label="图书封面" width="180">
          <template v-slot="scope">
            <el-image
                style="width: 70px; height: 70px; border-radius: 50%"
                :src="'http://localhost:8080/api/files/' + scope.row.img"
                :preview-src-list="['http://localhost:8080/api/files/' + scope.row.img]">
            </el-image>
          </template>
        </el-table-column>
        <el-table-column prop="name" label="图书姓名" width="180"></el-table-column>
        <el-table-column label="图书介绍" width="180">
          <template slot-scope="scope">
            <el-button type="success" @click="viewEditor(scope.row.content)">点击查看</el-button>
          </template>
        </el-table-column>
        <el-table-column prop="author" label="图书作者" width="180"></el-table-column>
        <el-table-column prop="price" label="图书价格" width="180"></el-table-column>
        <el-table-column prop="press" label="图书出版社" width="180"></el-table-column>
        <el-table-column prop="typeName" label="图书分类" width="180"></el-table-column>
        <el-table-column label="操作" width="250px">
          <template slot-scope="scope">
            <el-button type="primary" @click="edit(scope.row)" v-if="user.role === 'ROLE_ADMIN'">编辑</el-button>
            <el-button type="primary" @click="down(scope.row.img)">下载</el-button>
            <el-popconfirm title="确定删除吗？" @confirm="del(scope.row.id)">
              <el-button slot="reference" type="danger" style="margin-left: 5px" v-if="user.role === 'ROLE_ADMIN'">删除</el-button>
            </el-popconfirm>
          </template>
        </el-table-column>
      </el-table>
    </div>
    <div class="block">
      <el-pagination
          @size-change="handleSizeChange"
          @current-change="handleCurrentChange"
          :current-page="params.pageNum"
          :page-sizes="[5, 10, 15, 20]"
          :page-size="params.pageSize"
          layout="total, sizes, prev, pager, next"
          :total="total">
      </el-pagination>
    </div>
    <div>
      <el-dialog title="请填写姓名" :visible.sync="dialogFormVisible" width="50%">
        <el-form :model="form">
          <el-form-item label="图书名称" label-width="15%">
            <el-input v-model="form.name" autocomplete="off" style="width:90%"></el-input>
          </el-form-item>
          <el-form-item label="图书封面" label-width="15%">
            <el-upload action="http://localhost:8080/api/files/upload" :on-success="successUpload">
              <el-button size="small" type="primary">点击上传</el-button>
            </el-upload>
          </el-form-item>
          <el-form-item label="图书作者" label-width="15%">
            <el-input v-model="form.author" autocomplete="off" style="width:90%"></el-input>
          </el-form-item>
          <el-form-item label="图书价格" label-width="15%">
            <el-input v-model="form.price" autocomplete="off" style="width:90%"></el-input>
          </el-form-item>
          <el-form-item label="图书出版社" label-width="15%">
            <el-input v-model="form.press" autocomplete="off" style="width:90%"></el-input>
          </el-form-item>
          <el-form-item label="图书分类" label-width="15%">
            <el-select v-model="form.typeId" placeholder="请选择" style="width: 90%">
              <el-option v-for="item in typeObjs" :key="item.id" :label="item.name" :value="item.id"></el-option>
            </el-select>
          </el-form-item>
          <el-form-item label="图书介绍" label-width="15%">
            <div id="editor" style="width:90%"></div>
          </el-form-item>
        </el-form>
        <div slot="footer" class="dialog-footer">
          <el-button @click="dialogFormVisible = false">取 消</el-button>
          <el-button type="primary" @click="submit()">确 定</el-button>
        </div>
      </el-dialog>
    </div>
    <el-dialog title="图书介绍" :visible.sync="editorVisible" width="50%">
      <div v-html="viewData" class="w-e-text"></div>
    </el-dialog>
  </div>
</template>
<script>
import request from "@/utils/request";
import E from 'wangeditor'
let editor
function initWangEditor(content) {	setTimeout(() => {
  if (!editor) {
    editor = new E('#editor')
    editor.config.placeholder = '请输入内容'
    editor.config.uploadFileName = 'file'
    editor.config.uploadImgServer = 'http://localhost:8080/api/files/wang/upload'
    editor.create()
  }
  editor.txt.html(content)
}, 0)
}
export default {
  //name: "BookView",
  data() {
    return {
      params:{
        name: '',
        author: '',
        //price: '',
        //press: '',
        //img: '',
        pageNum: 1,
        pageSize: 5
      },
      tableData: [],
      total: 0,
      dialogFormVisible: false,
      editorVisible: false,
      form: {},
      typeObjs: [],
      viewData:'',
      user: localStorage.getItem("user") ? JSON.parse(localStorage.getItem("user")) : {}
    }
  },
  created() {
    this.findBySearch();
    this.findTypes();
  },
  methods: {
    findTypes() {
      request.get("/type").then(res => {
        if (res.code === '0') {
          this.typeObjs = res.data;
        } else {
          this.$message.error(res.msg)
        }
      })
    },
    findBySearch(){
      request.get("/book/search",{
        params:this.params}
      ).then(res =>{
        if(res.code === '0'){
          this.tableData = res.data.list;
          this.total = res.data.total;
        }else{
          this.$message.error(res.msg);
        }
      })
    },
    reset(){
      this.params = {
        pageNum: 1,
        pageSize: 5,
        name: '',
        phone: ''
      }
      this.findBySearch();
    },
    handleSizeChange(pageSize) {
      this.params.pageSize = pageSize;
      this.findBySearch();
    },
    handleCurrentChange(pageNum) {
      this.params.pageNum = pageNum;
      this.findBySearch();
    },
    add(){
      this.form = {};
      initWangEditor("");
      this.dialogFormVisible = true;
    },
    edit(obj) {
      this.form = obj;
      //this.form = JSON.parse(JSON.stringify(obj));
      //initWangEditor(this.form.content);
      initWangEditor(obj.content ? this.form.content : "");
      this.dialogFormVisible = true;
    },
    viewEditor(data){
      //this.form.content = data;
      this.viewData = data;
      this.editorVisible = true;

    },
    submit(){
      this.form.content = editor.txt.html();
      request.post("/book", this.form).then(res => {
        if (res.code === '0') {
          this.$message.success("操作成功");
          this.dialogFormVisible = false;
          this.findBySearch();
        } else {
          this.$message.error(res.msg);
        }
      })
    },
    del(id) {
      request.delete("/book/" + id).then(res => {
        if (res.code === '0') {
          this.$message.success("删除成功");
          this.findBySearch();
        } else {
          this.$message.error(res.msg);
        }
      })
    },
    successUpload(res) {
      this.form.img = res.data;
    },
    down(flag) {
      location.href = 'http://localhost:8080/api/files/' + flag
    }
  }
}
</script>
```
##### 后端：FileController.java
```java
/**
 * wang-editor编辑器文件上传接口
 */
@PostMapping("/wang/upload")
public Map<String, Object> wangEditorUpload(MultipartFile file) {
    String flag = System.currentTimeMillis() + "";
    String fileName = file.getOriginalFilename();
    try {
        // 文件存储形式：时间戳-文件名
        FileUtil.writeBytes(file.getBytes(), filePath + flag + "-" + fileName);
        System.out.println(fileName + "--上传成功");
        Thread.sleep(1L);
    } catch (Exception e) {
        System.err.println(fileName + "--文件上传失败");
    }
    Map<String, Object> resMap = new HashMap<>();
    // wangEditor上传图片成功后， 需要返回的参数
    resMap.put("errno", 0);
    resMap.put("data", CollUtil.newArrayList(Dict.create().set("url", "http://localhost:8080/api/files/" + flag)));
    return resMap;
}
```
##### 后端：Book.java
```java
@Table(name = "book")
public class Book {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Integer id;
    @Column(name = "name")
    private String name;
    @Column(name = "price")
    private String price;
    @Column(name = "author")
    private String author;
    @Column(name = "press")
    private String press;
    @Column(name = "img")
    private String img;
    @Column(name = "content")
    private String content;
    @Column(name = "typeId")
    private Integer typeId;

    @Transient
    private String typeName;
}
```
##### 数据库：book.sql
```sql
CREATE TABLE `book` (
  `id` int NOT NULL AUTO_INCREMENT COMMENT '主键ID',
  `name` varchar(255) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci DEFAULT NULL COMMENT '图书名称',
  `price` varchar(255) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci DEFAULT NULL COMMENT '图书价格',
  `author` varchar(255) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci DEFAULT NULL COMMENT '图书作者',
  `press` varchar(255) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci DEFAULT NULL COMMENT '图书出版社',
  `img` varchar(255) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci DEFAULT NULL COMMENT '图书封面',
  `typeId` int DEFAULT NULL COMMENT '图书分类ID',
  `content` longtext CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci COMMENT '图书介绍',
  PRIMARY KEY (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=9 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_unicode_ci COMMENT='图书信息表';
```
##### 安装：【wangeditor】
安装路径：`E:\eld901\Idea\vue` (Vue工程)
安装命令：`npm i wangeditor --save`

#### 20241228 武哥毕设 https://www.javaxmsz.cn/
1. 项目使用的技术栈  
后端：Java、Springboot、MyBatis  
前端：Vue、Element-UI、HTML、CSS、Javascript  
数据库：MySQL  
2. 电脑里需要准备的环境  
后端运行环境：JDK 8  
前端运行环境：nodejs  
代码编写软件：IDEA  
数据库：MySQL 5.7 或者 8  
数据库可视化：navicat  
文档编写软件：typora、word、WPS（非必要）  
接口调试工具：postman（非必要）  
3. 该系列课程资料汇总  
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
##### 安装：【Element】
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
