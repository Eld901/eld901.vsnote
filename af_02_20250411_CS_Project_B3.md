## F 笔记  
### Project_B 本科毕业设计-毕设小结  
#### Vue+SpringBoot前后端分离项目 （一）流程小结  
#### 20250315 (1-1)准备工作  
1. 前端环境  
Node.js  
2. 后端环境  
JDK11  
Maven3.6.x  
3. 数据库环境  
MySQL8.0  
4. 开发软件安装  
IntelliJ IDEA 2024.2.0.1  
Navicat Premium 16  
5. 笔记软件安装  
Visual Studio Code  
Typora  
6. 文件夹归类  
(1)项目源码：PRJ_code文件夹  
(2)项目截图：PRJ_img文件夹  
(3)项目SQL：PRJ_sql文件夹  
(4)项目介绍：README.md  
(5)项目笔记：.md文件  
#### 20250315 (1-1)新建工程  
##### [1]数据库连接(Navicat)  
1. 新建连接(MySQL)  
(1)连接名：localhost_3306  
(2)主机：localhost  
(3)端口：3306  
(4)用户名：root  
(5)密码：(1234)  
2. 新建数据库  
(1)数据库名：(springboot)  
(2)字符集：utf8mb4  
(3)排序规则：utf8mb4_unicode_ci  
3. 新建数据库表  
(1)运行SQL文件  
  1新建查询  
  2运行  
(2)手动建表  
  1添加注释(如"用户信息表")  
  2添加字段  
  3保存并命名  
  4填充表数据  
4. 数据库表  
(1)建表属性：注释 字段 SQL预览 选项 索引 外键 检查 触发器  
(2)字段属性：名、类型、长度、小数点、不是null、虚拟、键、注释  
  对应数据库表的每一列属性  
  对应前端data(){return {}}  
  对应后端Entity层  
5. 建表规则  
(1)字段是主键ID  
  名(id)、类型(int)、长度、小数点、不是null(勾选)、虚拟、键(勾选)、注释(主键ID)  
  默认、自动递增(勾选)、无符号、填充零  
(2)字段是字符类型  
  名(name)、类型(varchar)、长度(255)、小数点、不是null、虚拟、键、注释(姓名)  
  默认(NULL)、字符集(utf8mb4)、排序规则(utf8mb4_unicode_ci)、键长度、二进制  
6. 导出文件(.sql)  
右键表->转储SQL文件->结构和数据->(选择保存位置)  
##### [2]前端工程  
1. 安装Node.js  
2. 安装Vue.js  
  Vue官网：https://cn.vuejs.org/  
  VueCLI官网：https://cli.vuejs.org/zh/  
(1)项目路径下打开cmd：`cd <your-project-name>`  
(2)验证前端环境Node.js：`node -v`  
(2)验证Node.js包管理工具npm：`npm -v`  
(3)使用npm可查看当前库：`npm config get registry`  
(3)使用npm可设置官方库：`npm config set registry https://registry.npmjs.org`  
(3)使用npm设置淘宝镜像：`npm config set registry https://registry.npm.taobao.org`(过期)  
(3)使用npm设置有效镜像：`npm config set registry https://registry.npmmirror.com`(有效)  
(4)安装VueCLI工具：`npm install -g @vue/cli`  
(4)查看VueCLI版本：`vue --version` (`@vue/cli 5.0.8`)  
(5)使用VueCLI创建Vue.js项目：`vue create <vue-project-name>` (`vue create vue`)  
  Vue CLI v5.0.8  
  ? Please pick a preset: `Manually select features(手动选择特性)`  
  ? Check the features needed for your project: `选Babel(编译工具)、Router(Vue路由)，取消Linter/Fomatter`  
  ? Choose a version of Vue.js that you want to start the project with `2.x(Vue.js版本)`  
  ? Use history mode for router? (Requires proper server setup for index fallback in production) `Yes(用历史模板)`  
  ? Where do you prefer placing config for Babel, ESLint, etc.? `In package.json(选择配置文件)`  
  ? Save this as a preset for future projects? `Yes(保存为预设)`  
  ? Save preset as: `default(为预设命名)`  
(6)进入Vue.js项目文件夹：`cd <vue-project-name>`(`cd vue`)  
(6)使用命令行启动Vue.js项目：`npm run serve`  
(7)使用IDEA启动Vue.js项目：配置Add Configuration  
3. 安装Element  
  Element官网：https://element.eleme.cn/  
(1)vue项目路径下打开终端` E:\eld901\Idea\vue> `  
(2)验证Vue.js项目环境：`vue --version`  
(3)使用npm安装：`npm i element-ui -S`  
4. 安装axios(前端封装)  
(1)vue项目路径下打开终端` E:\eld901\Idea\vue> `  
(2)安装命令：`npm i axios -S`  
(3)安装验证：vue/package.json中出现"axios"  
##### [3]后端工程  
1. 修改项目配置  
JDK、Maven、数据库、pom.xml  
2. 编写业务逻辑  
Controller=>Service=>Dao(Mapper)=>Entity=>数据库  
#### 20250425 (1-2)项目导入  
1. 导入pom.xml  
2. 配置文件  
(1)修改application.yml  
  修改port、username、password、url、mybatis等信息(端口号、数据库名、数据库密码)  
(2)修改pom.xml  
  选择正确的依赖(MVNRepository：https://mvnrepository.com/)  
3. 配置项目  
(1)配置JDK(项目结构)  
  选择正确的JDK  
(2)配置Maven(设置入口)  
  选择正确Maven  
(3)配置Maven(侧栏入口)  
  生命周期(LifeCycle)  
  依次点击"清理(clean)"、"安装(install)"  
  如遇爆红点击"跳过单元测试(Toggle'SkipTests'Mode)"  
(4)配置Database(侧栏入口)  
  数据源设置(Host、Port、User、Password、Database)  
  下载驱动(Download missing driver files)  
  测试连接(Test Connection)  
  运行脚本(选择SQLScript RunSQLScript)  
(5)配置前端项目启动入口Add Configuration(顶栏入口)  
  添加npm配置  
  package.json:(`E:\eld901\Idea\vue\package.json`)  
  Command:run  
  Scripts:serve  
  Arguments:(空)  
  Node interpreter:Project node(`D:\appdownload\appd_node\node.exe`)  
  Node options:(空)  
  Package manager:Project(`D:\appdownload\appd_node\npm.cmd`)  
  Environment:(空)  
#### 20250425 (1-2)项目打包  
1. 拷贝前端项目  
(1)方法一：cv拷贝  
  cv拷贝，重命名，不修改其他文件  
  cv拷贝，删除node_modules文件夹，再命令行运行项目`npm install``npm run dev`  
(2)方法二：命令行  
  修改配置文件*vue.config.js*`publicPath: './',`  
  修改路由配置*index.js*`mode: 'hash',`  
  打包项目到dist文件夹`npm run build`  
2. 拷贝后端项目  
(1)方法一：maven按钮  
  双击`clean`清除缓存文件  
  双击`package`打成jar包到target文件夹下  
(2)方法二：命令行  
  清理项目并安装到本地仓库同时跳过测试阶段`mvn clean install -Dmaven.test.skip`  
  运行jar包`java -jar xxx.jar`  

#### Vue+SpringBoot前后端分离项目 （二）项目小结  
#### 20250408 (2-1)1.前端源码  
##### [1]前端 vue.config.js  
vue/vue.config.js
```js
const { defineConfig } = require('@vue/cli-service')
module.exports = defineConfig({
  // publicPath: './',
  transpileDependencies: true
})
```
1. const { defineConfig } = require('@vue/cli-service')  
从 `@vue/cli-service` 包中导入 `defineConfig` 函数。  
`@vue/cli-service` 是 Vue CLI 提供的工具包。  
`defineConfig` 是一个辅助函数，用于定义项目的配置。  
2. module.exports = defineConfig({...})  
作用：将配置对象导出为模块，供 Vue CLI 使用。  
`module.exports` 是 Node.js 中用于导出模块的语法。  
`defineConfig({...})` 包装了一个配置对象，确保其结构符合 Vue CLI 的要求。  
3. transpileDependencies: true  
配置是否对依赖项进行转译（transpile）。  
默认情况下，Vue CLI 会忽略 `node_modules` 中的依赖项，不会对它们进行 Babel 转译。  
设置 `transpileDependencies: true` 会强制对所有依赖项进行转译。  
##### [2]前端 main.js  
vue/src/main.js  
```js
import Vue from 'vue'
import App from './App.vue'
import router from './router'
Vue.config.productionTip = false
new Vue({
  router,
  render: h => h(App)
}).$mount('#app')
```
```js
import Vue from 'vue'
import App from './App.vue'
import router from './router'
import '@/assets/global.css'//(new)
import ElementUI from 'element-ui';//(new)
import 'element-ui/lib/theme-chalk/index.css';//(new)
Vue.use(ElementUI, { size: "small" });//(new)
Vue.config.productionTip = false
new Vue({
  router,
  render: h => h(App)
}).$mount('#app')
```
##### [3]前端 request.js  
vue/src/utils/request.js  
```js
import axios from 'axios'
const request = axios.create({
    baseURL: 'http://localhost:8080',
    timeout: 5000
})
request.interceptors.request.use(config => {
    config.headers['Content-Type']= 'application/json;charset=utf-8';
    return config
}, error => {
    return Promise.reject(error)
});
request.interceptors.response.use(
    response => {
        let res = response.data;
        if (typeof res === 'string') {
            res = res ? JSON.parse(res) : res
        }
        return res;
    },
    error => {
        console.log('err' + error)
        return Promise.reject(error)
    }
)
export default request
```
##### [4]前端 global.css  
vue/src/assets/global.css  
```css
body {
    margin: 0;
    padding: 0;
    overflow: hidden;
}
* {
    box-sizing: border-box;
}
```
##### [5]前端 index.js  
vue/src/router/index.js  
```js
import Vue from 'vue'
import VueRouter from 'vue-router'
import HomeView from '../views/HomeView.vue'
Vue.use(VueRouter)
const routes = [
  {path: '/',name: 'home',component: HomeView},// redirect: '/home',
  {path: '/about',name: 'about',component: () => import('../views/AboutView.vue')
  }]
const router = new VueRouter({
  mode: 'history',
  base: process.env.BASE_URL,
  routes
})
export default router
```
```js
import Vue from 'vue'
import VueRouter from 'vue-router'
import LoginView from "@/views/LoginView.vue";
import RegisterView from "@/views/RegisterView.vue";
import Layout from "@/views/Layout.vue";
import HomeView from '../views/HomeView.vue'
import AdminView from '../views/AdminView.vue'
Vue.use(VueRouter)
const routes = [
  {path: '/login',name: 'Login',component: LoginView},
  {path: '/register',name: 'Register',component: RegisterView},
  {path: '/',name: 'Layout',component: Layout,//redirect: '/home',
    children: [
      {path: '',component: HomeView},
      {path: 'admin',component: AdminView}
    ]},
]
const router = new VueRouter({
  mode: 'history',
  // mode: 'hash',
  base: process.env.BASE_URL,
  routes
})
// 路由守卫
router.beforeEach((to ,from, next) => {
  const user = localStorage.getItem("user");
  if (!user && to.path !== '/login' && to.path !== '/register') {
    return next("/login");
  }else {next();}
})
export default router
```
##### [6]前端 [App.vue]  
vue/src/App.vue  
```js
<template>
  <nav>
    <router-link to="/">Home页面</router-link>
    <router-link to="/about">About页面</router-link>
  </nav>
  <div id="app">
    <router-view/>
  </div>
</template>
```
```js
<template>
  <div id="app">
    <nav>
      <router-link to="/">Home</router-link> |
      <router-link to="/login">Login</router-link> |
      <router-link to="/register">Register</router-link>
    </nav>
    <router-view/> 
  </div>
</template>
<style>
</style>
<script lang="ts">
 export default {
   name: 'App'
 };
</script>
```
1. template 部分  
`<nav>`：一个语义化的 HTML 元素，表示导航栏。  
`<router-link>` 创建导航链接  
`<div id="app">`：一个容器，用于包裹路由视图。  
`<router-view>` 渲染当前路由匹配的组件。  
2. script 部分  
`lang="ts"` 指定脚本语言为 TypeScript  
`export default` 导出一个默认对象，定义了组件的基本信息  
`name: 'App'` 组件的名称，通常用于调试和递归组件调用  
3. 执行流程  
App.vue 是 Vue 应用的根组件，负责渲染导航栏和路由视图。  
当 Vue 应用启动时，App.vue 作为根组件被加载到页面的 #app 元素中。  
`<nav>` 标签中的两个 `<router-link>` 会被渲染为导航链接，分别指向 / 和 /about 路径。  
`<router-view>` 会根据当前的路由路径，渲染对应的组件。例如：  
当路径为 / 时，`<router-view>` 会渲染 HomeView 组件。  
当路径为 /about 时，`<router-view>` 会渲染 AboutView 组件。  
##### [7]前端 [HomeView.vue]  
vue/src/views/HomeView.vue  
```js
<template>
  <div class="home">
  <HelloWorld msg="Welcome to Your Vue.js APP"/>
  </div>
</template>
<script>
import HelloWorld from '@/components/HelloWorld.vue'
export default {
  name: 'HomeView',
  components:{Helloworld}
}
</script>
```
1. template 部分  
`<div class="home">` 一个容器，用于包裹 HelloWorld 组件。  
`<HelloWorld msg="Welcome to Your Vue.js APP"/>`HelloWorld 是一个自定义组件  
msg 是一个属性，将字符串 "Welcome to Your Vue.js APP" 传递给 HelloWorld 组件。  
2. script 部分  
`import HelloWorld from '@/components/HelloWorld.vue'`  
  从 @/components/HelloWorld.vue 导入 HelloWorld 组件。  
  @ 是 Vue CLI 配置的别名，通常指向 src 目录。  
`export default`  
  导出一个默认对象，定义了组件的基本信息。  
  name: 'HomeView'：组件的名称，通常用于调试和递归组件调用。  
  components: { HelloWorld }：注册 HelloWorld 组件，使其可以在模板中使用。  
3. 执行流程  
HomeView.vue 是 Vue.js 项目的首页组件，它通过 `<router-view>` 被加载，并渲染了一个 HelloWorld 组件。
当路由路径为 / 时，HomeView 组件会被加载到 `<router-view>` 中。  
`<div class="home">` 会被渲染到页面中。  
`<HelloWorld msg="Welcome to Your Vue.js APP"/>` 会被渲染为 HelloWorld 组件，并将 msg 属性传递给它。  
在 `<script>` 部分，HelloWorld 组件被导入并注册到 HomeView 组件中，使其可以在模板中使用。  
##### [8]前端 [HelloWorld.vue] 
vue/src/components/HelloWorld.vue  
```js
<template>
  <div class="hello">
    <h1>{{msg}}</h1>
  </div>
</template>
<script>
export default {
  name: 'HelloWorld',
  props: {msg: String}
}
</script>
```
1. template 部分  
`<div class="hello">`：一个容器，用于包裹组件的内容，添加了 hello 类名，方便后续添加样式。  
`<h1>{{ msg }}</h1>`：一个标题，显示传入的 msg 属性值。{{ msg }} 是 Vue.js 的插值语法，用于动态绑定数据。  
2. script 部分  
`name: 'HelloWorld'` 组件的名称，通常用于调试和递归组件调用。  
`props: { msg: String }` 定义了一个名为 msg 的属性（prop），类型为 String。  
`props` 是 Vue.js 中用于父子组件通信的机制  
子组件可以通过 `props` 接收父组件传递的数据  
在父组件中，可以通过 `:msg="someValue"` 或 `msg="someValue"` 的方式将数据传递给 HelloWorld 组件。  
3. 执行流程  
HelloWorld.vue 是 Vue.js 项目中的一个简单组件，用于显示传入的消息。  
它通过 props 接收父组件传递的数据，并在模板中动态显示。  
当 HelloWorld 组件被父组件（如 HomeView）使用时，它会被加载到页面中。  
`<div class="hello">` 会被渲染到页面中。  
`<h1>{{ msg }}</h1>` 会动态显示父组件传递的 msg 属性值。  
确保在父组件中正确传递 msg 属性。例如：`<HelloWorld msg="Welcome to Your Vue.js APP"/>`  
如果 msg 属性未传递，HelloWorld 组件中的 `{{ msg }}` 将显示为 `undefined`。  
##### [9]前端 [AboutView.vue] 
vue/src/views/AboutView.vue  
```js
<template>
  <div class="about">
    <h1>This is an about page<h1/>
  </div>
</template>
<script>
export default {
  name: 'AboutView'
}
</script>
```
1. template 部分  
`<div class="about">`：一个容器，用于包裹页面内容，添加了 about 类名，方便后续添加样式。  
`<h1>This is an about page</h1>`：一个标题，显示“关于”页面的内容。  
2. script 部分  
`name: 'AboutView'`：组件的名称，通常用于调试和递归组件调用。  
3. 执行流程  
AboutView.vue 是 Vue.js 项目的“关于”页面组件，它通过 `<router-view>` 被加载，并显示简单的页面内容。  
当路由路径为 /about 时，AboutView 组件会被加载到 `<router-view> `中。  
`<div class="about">` 会被渲染到页面中。  
`<h1>This is an about page</h1>` 会被渲染为标题。  
##### [10]前端 index.html  
vue/public/index.html  
```html
<!DOCTYPE html>
<html lang="">
  <head>
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width,initial-scale=1.0">
    <link rel="icon" href="<%= BASE_URL %>favicon.ico">
    <title><%= htmlWebpackPlugin.options.title %></title>
  </head>
  <body>
    <noscript>
      <strong>We're sorry but <%= htmlWebpackPlugin.options.title %> doesn't work properly without JavaScript enabled. Please enable it to continue.</strong>
    </noscript>
    <div id="app"></div>
    <!-- built files will be auto injected -->
  </body>
</html>
```
1. head 部分 这部分定义了页面的元数据和链接。  
`<meta charset="utf-8">`：设置字符编码为 UTF-8，确保页面支持多种语言。  
`<meta http-equiv="X-UA-Compatible" content="IE=edge">`：确保 Internet Explorer 使用最新的渲染引擎。  
`<meta name="viewport" content="width=device-width,initial-scale=1.0">`：设置视口（viewport），确保页面在移动设备上正确显示。  
`<link rel="icon" href="<%= BASE_URL %>favicon.ico">`：设置页面的图标文件。  
`<title><%= htmlWebpackPlugin.options.title %></title>`：设置页面的标题。  
2. body 部分 这部分定义了页面的主体内容。  
`<noscript>`：如果用户的浏览器禁用了 JavaScript，这段内容会被显示。
`<div id="app"></div>`：Vue 应用的挂载点。在 main.js 中，Vue 实例会被挂载到这个 div 元素上。  
`<!-- built files will be auto injected -->`：这是一个注释，表示构建文件（如 bundle.js 和 bundle.css）将由 html-webpack-plugin 自动注入到页面中。  
3. 模板变量  
`<%= BASE_URL %>` 是一个模板变量，由 html-webpack-plugin 替换为实际的基路径（通常是 / 或其他配置的路径）。  
`<%= htmlWebpackPlugin.options.title %>` 是一个模板变量，由 html-webpack-plugin 替换为实际的标题内容。  
4. 执行流程  
index.html 是 Vue.js 项目的 HTML 模板文件，用于定义页面的基本结构。  
它在项目构建时被 html-webpack-plugin 处理，模板变量会被替换为实际的值，构建文件会被自动注入到页面中。  
通过这个文件，你可以自定义页面的元数据、图标和标题等内容。  
项目构建  
当运行 npm run build 时，Vue CLI 会使用 html-webpack-plugin 处理 index.html 文件。  
模板变量（如 <%= BASE_URL %> 和 <%= htmlWebpackPlugin.options.title %>）会被替换为实际的值。  
构建文件（如 bundle.js 和 bundle.css）会被自动注入到 `<body>` 中。  
页面加载  
当用户访问页面时，浏览器会加载处理后的 index.html 文件。  
如果用户的浏览器禁用了 JavaScript，会显示 `<noscript>` 中的内容。  
Vue 应用会通过 main.js 被挂载到 `<div id="app"></div>` 中。  
#### 20250408 (2-1)1.后端源码  
##### [1]后端 pom.xml  
springboot/pom.xml  
```xml
<?xml version="1.0" encoding="UTF-8"?>
<project 
  xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
	xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 https://maven.apache.org/xsd/maven-4.0.0.xsd"
>
	<modelVersion>4.0.0</modelVersion>
	<parent>
		<groupId>org.springframework.boot</groupId>
		<artifactId>spring-boot-starter-parent</artifactId>
		<version>3.3.7</version>
		<relativePath/> <!-- lookup parent from repository -->
	</parent>
	<groupId>com.example</groupId>
	<artifactId>springboot1</artifactId>
	<version>0.0.1-SNAPSHOT</version>
	<name>springboot</name>
	<description>springboot</description>
	<url/>
	<licenses>
		<license/>
	</licenses>
	<developers>
		<developer/>
	</developers>
	<scm>
		<connection/>
		<developerConnection/>
		<tag/>
		<url/>
	</scm>
	<properties>
		<java.version>17</java.version>
	</properties>
	<dependencies>
		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-web</artifactId>
		</dependency>
		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-test</artifactId>
			<scope>test</scope>
		</dependency>
  </dependencies>
	<build>
		<plugins>
			<plugin>
				<groupId>org.springframework.boot</groupId>
				<artifactId>spring-boot-maven-plugin</artifactId>
			</plugin>
		</plugins>
	</build>
</project>
```
1. 项目声明  
`<?xml version="1.0" encoding="UTF-8"?>`声明XML文件版本为1.0，编码格式为UTF-8。  
`<project></project>`  
  `xmlns`：命名空间声明，确保 XML 文件遵循 Maven POM 的规范。  
  `xsi:schemaLocation`：指定 XML Schema 的位置，用于验证 POM 文件的结构。  
`<modelVersion></modelVersion>`：指定 POM 文件的模型版本，通常是 4.0.0  
`<parent></parent>`：定义父项目依赖，这里使用了 Spring Boot 的父项目 spring-boot-starter-parent，版本为 3.3.7。  
`<relativePath/>`：指定父项目的相对路径，这里为空，表示从 Maven 仓库中查找。  
4. 项目基本信息  
`<name></name>`：项目的名称，这里是 springboot。  
`<description></description>`：项目的描述，这里是 springboot。  
`<groupId></groupId>`：项目的组 ID，通常是公司的域名反转，这里为 com.example。  
`<artifactId></artifactId>`：项目的 artifact ID，这里是 springboot1。  
`<version></version>`：项目的版本号，这里是 0.0.1-SNAPSHOT，表示这是一个开发中的快照版本。  
5. 项目配置  
`<properties></properties>`：定义项目的属性，这里指定了 Java 版本为 17。  
6. 依赖管理  
`<dependencies></dependencies>`：定义项目的依赖项。  
`spring-boot-starter-web`：包含 Spring MVC 和 Tomcat 的依赖，用于构建 Web 应用。  
`spring-boot-starter-test`：包含测试相关的依赖，如 JUnit 和 Mockito，作用域为 test，仅在测试编译和执行阶段使用。  
7. 构建配置  
`<build></build>`：定义项目的构建配置。  
`<plugins></plugins>`：定义使用的插件，这里使用了 spring-boot-maven-plugin，用于支持 Spring Boot 的构建和运行。  
8. 总结  
这个 pom.xml 文件是一个典型的 Spring Boot 项目的 Maven 配置文件，它定义了项目的依赖、属性和构建配置。  
通过这个文件，Maven 可以管理项目的依赖项、编译代码、运行测试和打包项目。  
##### [2]后端 application.yml  
springboot/src/main/resources/application.yml  
```yml
# 服务器配置
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
# mybatis配置
mybatis:
  mapper-locations: classpath:mapper/*.xml
  type-aliases-package: com.example.entity
# 分页配置
pagehelper:
  helper-dialect: mysql
  reasonable: true
  support-methods-arguments: true
  params: count=countSql
```
1. 服务器配置  
`server.port`：指定 Spring Boot 应用的服务器端口，默认为 8080 。  
2. Spring 配置  
数据源配置  
`spring.datasource.driver-class-name`：指定数据库驱动类名，这里是 MySQL 的驱动类 com.mysql.cj.jdbc.Driver。  
`spring.datasource.username`：数据库用户名，这里是 root。  
`spring.datasource.password`：数据库密码，这里是 1234。  
`spring.datasource.url`：数据库连接 URL，这里是连接到本地 MySQL 数据库的 URL，包含了一些连接参数：  
  `useUnicode=true` 和 `characterEncoding=utf-8`：确保支持 Unicode 和 UTF-8 编码。  
  `allowMultiQueries=true`：允许执行多条 SQL 语句。  
  `useSSL=false`：禁用 SSL 连接。  
  `serverTimezone=GMT%2b8`：设置服务器时区为 GMT+8。  
  `allowPublicKeyRetrieval=true`：允许公钥检索。  
Spring 主配置  
`spring.main.allow-circular-references`：允许循环引用，这在某些情况下可能会导致问题，但有时在复杂的项目中可能需要(分页查询)。  
3. MyBatis 配置  
`mybatis.mapper-locations`：指定 MyBatis 的映射文件位置  
  这里是 classpath:mapper/*.xml，表示在 src/main/resources/mapper 目录下查找所有 .xml 文件。  
`mybatis.type-aliases-package`：指定 MyBatis 的类型别名包  
  这里是 com.example.entity，表示在 com.example.entity 包下查找实体类并为其生成别名。  
4. PageHelper 配置  
`pagehelper.helper-dialect`：指定 PageHelper 的方言，这里是 mysql，表示使用 MySQL 的分页方言。  
`pagehelper.reasonable`：启用合理化分页，当分页参数不合理时，自动调整为合理值。  
`pagehelper.support-methods-arguments`：支持通过方法参数传递分页参数。  
`pagehelper.params`：自定义分页参数，这里是 count=countSql，表示分页参数的名称为 countSql。  
##### [3]后端 [SpringbootApplication.java] 
springboot/src/main/java/com/example/SpringbootApplication.java  
```java
@SpringBootApplication
@MapperScan("com.example.dao")
public class SpringbootApplication {
	public static void main(String[]args) {
		SpringApplication.run(SpringbootApplication.class, args);
	}
}
```
1. @SpringBootApplication 注解  
2. @MapperScan 注解  
3. SpringbootApplication 类  
`public static void main(String[]args)`：应用的入口方法。  
`SpringApplication.run(SpringbootApplication.class, args)`：启动 Spring Boot 应用。  
  `SpringbootApplication.class`：指定当前类作为 Spring Boot 应用的主配置类。  
  `args`：传递给应用的命令行参数。  
4. 执行流程  
当运行 main 方法时，SpringApplication.run(SpringbootApplication.class, args) 会启动 Spring Boot 应用。  
Spring Boot 会加载 SpringbootApplication 类，并解析其上的注解。  
@SpringBootApplication：启用自动配置和组件扫描。  
@MapperScan("com.example.dao")：扫描 com.example.dao 包及其子包中的所有接口，并将它们注册为 MyBatis 的 Mapper Bean。  
扫描 com.example 包及其子包，找到 HomeController、HomeService 和 HomeDao。  
应用启动完成，Spring Boot 的嵌入式服务器（如 Tomcat）开始监听指定的端口（默认为 8080），准备接收请求。  
访问 http://localhost:8080/home 时，HomeController 会调用 HomeService，HomeService 会调用 HomeDao，最终返回数据库中的消息。  
##### [4]后端 [Controller.java] 
springboot/src/main/java/com/example/controller/AdminController.java  
```java
@CrossOrigin
@RestController
@RequestMapping("/admin")
public class AdminController {
    private static final Logger log = LoggerFactory.getLogger(AdminController.class);
    @Resource
    private AdminService adminService;
    @PostMapping("/login")
    @AutoLog("登录该系统")
    public Result login(@RequestBody Admin admin, @RequestParam String key, HttpServletRequest request) {
        if (!admin.getVerCode().toLowerCase().equals(CaptureConfig.CAPTURE_MAP.get(key))) {
            CaptchaUtil.clear(request);
            return Result.error("验证码不正确");
        }
        Admin loginUser = adminService.login(admin);
        CaptureConfig.CAPTURE_MAP.remove(key);
        return Result.success(loginUser);
    }
    @PostMapping("/register")
    public Result register(@RequestBody Admin admin) {
        adminService.add(admin);
        return Result.success();
    }
    @GetMapping
    public Result findAll() {
        List<Admin> list = adminService.findAll();
        return Result.success(list);
    }
    @GetMapping("/search")
    public Result findBySearch(Params params) {
        log.info("拦截器已放行，正式调用接口内部，查询管理员信息");
        //List<Admin> list = adminService.findBySearch(params);
        PageInfo<Admin> info = adminService.findBySearch(params);
        return Result.success(info);
    }
    @PostMapping
    public Result save(@RequestBody Admin admin) {
        //adminService.add(admin);
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
##### [5]后端 [Service.java] 
springboot/src/main/java/com/example/service/AdminService.java  
```java
@Service
public class AdminService {
    @Resource
    private AdminDao adminDao;
    public List<Admin> findAll() {
        //return userDao.getUser();
        return adminDao.selectAll();
    }
    public PageInfo<Admin> findBySearch(Params params) {
        PageHelper.startPage(params.getPageNum(), params.getPageSize());
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
    public Admin login(Admin admin) {
        //return null;
        if (admin.getName() == null || "".equals(admin.getName())) {
            throw new CustomException("用户名不能为空");
        }
        if (admin.getPassword() == null || "".equals(admin.getPassword())) {
            throw new CustomException("密码不能为空");
        }
        Admin user = adminDao.findByNameAndPassword(admin.getName(), admin.getPassword());
        if (user == null) {
            throw new CustomException("用户名或密码输入错误");
        }
        String token = JwtTokenUtils.genToken(user.getId().toString(), user.getPassword());
        user.setToken(token);
        return user;
    }
    public Admin findById(Integer id) {
        return adminDao.selectByPrimaryKey(id);
    }
}
```
##### [6]后端 [Dao.java(Interface)] 
springboot/src/main/java/com/example/dao/AdminDao.java(Interface)  
```java
@Repository
public interface AdminDao extends Mapper<Admin> {
    @Select("select * from admin")
    List<Admin> getAll();
    List<Admin> findBySearch(@Param("params")Params params);
    @Select("select * from admin where name = #{name} limit 1")
    Admin findByName(@Param("name")String name);
    @Select("select * from admin where name =#{name} and password =#{password}")
    Admin findByNameAndPassword(@Param("name")String name, @Param("password")String password);
}

```
1. extends Mapper<Admin>  
继承了MyBatis的Mapper接口，这使得AdminDao可以使用MyBatis提供的通用CRUD方法（如selectById、insert等）。  
2. findBySearch方法  
定义了一个方法，用于根据传入的Params参数进行条件查询。  
使用@Param注解为params参数命名，以便在SQL语句中引用。  
具体的SQL实现通常在MyBatis的Mapper XML文件中定义。  
##### [7]后端 [Mapper.xml] 
springboot/src/main/resources/mapper/AdminMapper.xml  
```xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE mapper PUBLIC "-//mybatis.org//DTD Mapper 3.0//EN" "http://mybatis.org/dtd/mybatis-3-mapper.dtd">
<mapper namespace="com.example.dao.AdminDao">
    <select id="getAll" resultType="com.example.entity.Admin">
        select * from admin
    </select>
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
1. XML声明  
`<?xml version="1.0" encoding="UTF-8"?>`  
这是XML文件的标准声明，指定了XML文件的版本和编码格式。这里声明了版本为1.0，编码格式为UTF-8。  
2. DOCTYPE声明  
`<!DOCTYPE>`这是文档类型声明（DOCTYPE），用于指定XML文件的文档类型定义（DTD）。  
  `mapper`是根元素的名称，表示这是一个MyBatis的Mapper文件。  
  `PUBLIC "-//mybatis.org//DTD Mapper 3.0//EN"`是公共标识符，用于标识MyBatis的Mapper DTD。  
  `http://mybatis.org/dtd/mybatis-3-mapper.dtd`是系统标识符，指向MyBatis的DTD文件。这个文件定义了Mapper XML文件的结构和约束。  
3. Mapper根元素  
`<mapper></mapper>`是根元素，表示这是一个MyBatis的Mapper文件。  
  `namespace="com.example.dao.AdminDao"`属性指定了Mapper的命名空间。  
  这个命名空间通常与接口的全限定名一致，用于唯一标识这个Mapper文件。  
  在`<mapper>`标签内部，可以定义多个SQL映射语句（如`<select>`、`<insert>`、`<update>`、`<delete>`等）。  
##### [8]后端 [Entity.java] 
springboot/src/main/java/com/example/entity/Admin.java  
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
    //getter、setter
}
```
##### [9]后端 [Result.java] 
springboot/src/main/java/com/example/common/Result.java  
```java
private static final String SUCCESS = "0";
private static final String ERROR = "-1";
private String code;
private String msg;
private Object data;
public static Result success() {
    Result result = new Result();
    result.setCode(SUCCESS);
    return result;//result.getCode() == SUCCESS;
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
//getter、setter
```
##### [10]后端 [Params.java] 
springboot/src/main/java/com/example/entity/Params.java
```java
public class Params {
    private String content;
    private String username;
    private String name;
    private String phone;
    private String author;
    private Integer userId;
    private Integer PageNum;
    private Integer PageSize;
    //getter、setter
}
```
##### [11]后端 GlobalExceptionHandler.java  
springboot/src/main/java/com/example/exception/GlobalExceptionHandler.java  
```java
@ControllerAdvice(basePackages="com.example.controller")
public class GlobalExceptionHandler {
    private static final Logger log = LoggerFactory.getLogger(GlobalExceptionHandler.class);
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
##### [11]后端 CustomException.java  
springboot/src/main/java/com/example/exception/CustomException.java  
```java
public class CustomException extends RuntimeException {
    private String msg;
    public CustomException(String msg) { this.msg = msg; }
    public String getMsg() { return msg; }
    public void setMsg(String msg) { this.msg = msg; }
}
```
##### [12]后端 CorsConfig.java  
springboot/src/main/java/com/example/common/CorsConfig.java  
```java
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
##### [12]后端 CaptureConfig.java  
springboot/src/main/java/com/example/common/CaptureConfig.java  
```java
@Component
public class CaptureConfig {
    public static Map<String, String> CAPTURE_MAP = new HashMap<>();
}
```
##### [13]后端 WebConfig.java  
springboot/src/main/java/com/example/common/WebConfig.java  
```java
@Configuration
public class WebConfig implements  WebMvcConfigurer {
    @Resource
    private JwtInterceptor jwtInterceptor;
    @Override
    public void configurePathMatch(PathMatchConfigurer configurer) {
        configurer.addPathPrefix("/api", clazz -> clazz.isAnnotationPresent(RestController.class));
    }
    @Override
    public void addInterceptors(InterceptorRegistry registry) {
        registry.addInterceptor(jwtInterceptor).addPathPatterns("/api/**")
                .excludePathPatterns("/api/files/**")
                .excludePathPatterns("/api/captcha")
                .excludePathPatterns("/api/type/upload")
                .excludePathPatterns("/api/admin/login")
                .excludePathPatterns("/api/admin/register");
    }
}
```
##### [13]后端 CaptureController.java  
springboot/src/main/java/com/example/controller/CaptureController.java  
```java
@CrossOrigin
@RestController
@RequestMapping
public class CaptureController {
    @RequestMapping("/captcha")
    public void captcha(@RequestParam String key, HttpServletRequest request, HttpServletResponse response) throws Exception {
        SpecCaptcha captcha = new SpecCaptcha(135, 33, 5);
        captcha.setCharType(Captcha.TYPE_NUM_AND_UPPER);
        CaptureConfig.CAPTURE_MAP.put(key, captcha.text().toLowerCase());
        CaptchaUtil.out(captcha, request, response);//报错解决(JarEditor插件)
        // 算术类型
//        ArithmeticCaptcha captcha = new ArithmeticCaptcha(135, 33);
//        captcha.setLen(4);  // 几位数运算，默认是两位
//        captcha.getArithmeticString();  // 获取运算的公式：3+2=?
//        captcha.text();  // 获取运算的结果：5
//        CaptureConfig.CAPTURE_MAP.put(key, captcha.text().toLowerCase());
//        CaptchaUtil.out(captcha, request, response);
    }
}
```
##### [14]后端 JwtTokenUtils.java  
springboot/src/main/java/com/example/common/JwtTokenUtils.java  
```java
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
    public static String genToken(String adminId, String sign) {
        return JWT.create().withAudience(adminId) // 将 user id 保存到 token 里面,作为载荷
                .withExpiresAt(DateUtil.offsetHour(new Date(), 2)) // 2小时后token过期
                .sign(Algorithm.HMAC256(sign)); // 以 password 作为 token 的密钥
    }
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
            String adminId = JWT.decode(token).getAudience().get(0);
            return staticAdminService.findById(Integer.valueOf(adminId));
        } catch (Exception e) {
            log.error("获取当前登录的管理员信息失败, token={}", token,  e);
            return null;
        }
    }
}
```
##### [14]后端 JwtInterceptor.java  
springboot/src/main/java/com/example/common/JwtInterceptor.java  
```java
@Component
public class JwtInterceptor implements HandlerInterceptor {
    private static final Logger log = LoggerFactory.getLogger(JwtInterceptor.class);
    @Resource
    private AdminService adminService;
    @Override
    public boolean preHandle(HttpServletRequest request,HttpServletResponse response,Object handler) {
        String token = request.getHeader("token");
        if (StrUtil.isBlank(token)) {
            token = request.getParameter("token");
        }
        if (StrUtil.isBlank(token)) {
            throw new CustomException("无token，请重新登录");
        }
        String userId;
        Admin admin;
        try {
            userId = JWT.decode(token).getAudience().get(0);
            // 根据token中的userid查询数据库
//            if (userId == null || userId.isEmpty()) {
//                throw new CustomException("无效的token，请重新登录");
//            }
            admin = adminService.findById(Integer.parseInt(userId));
//            if (admin == null) {
//                throw new CustomException("用户不存在，请重新登录");
//            }
        } catch (Exception e) {
            String errMsg = "token验证失败，请重新登录";
            log.error(errMsg + ", token=" + token, e);
            throw new CustomException(errMsg);
        }
        if (admin == null) {
            throw new CustomException("用户不存在，请重新登录");
        }
        try {
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
##### [15]后端 AutoLog.java(Interface)  
springboot/src/main/java/com/example/common/AutoLog.java(Interface)  
```java
@Target(ElementType.METHOD)
@Retention(RetentionPolicy.RUNTIME)
@Documented
public @interface AutoLog {
    String value() default "";
}
```
##### [15]后端 LogAspect.java  
springboot/src/main/java/com/example/common/LogAspect.java  
```java
@Component
@Aspect
public class LogAspect {
    @Resource
    private LogService logService;
    @Around("@annotation(autoLog)")
    public Object doAround(ProceedingJoinPoint joinPoint, AutoLog autoLog) throws Throwable {
        String content = autoLog.value();
        String time = DateUtil.now();
        String username = "";
        Admin user = JwtTokenUtils.getCurrentUser();
        if (ObjectUtil.isNotNull(user)) {
            username = user.getName();
        }
        HttpServletRequest request = ((ServletRequestAttributes) RequestContextHolder.getRequestAttributes()).getRequest();
        String ip = request.getRemoteAddr();
        Result result = (Result) joinPoint.proceed();
        Object data = result.getData();
        if (data instanceof Admin) {
            Admin admin = (Admin) data;
            username = admin.getName();
        }
        Log log = new Log(null, content, time, username, ip);
        logService.add(log);
        return result;
    }
}
```
##### [16]后端 SpringBootApplicationTests.java  
springboot/src/test/com/example/SpringBootApplicationTests.java  
```java
package com.example;
import org.junit.jupiter.api.Test;
import org.springframework.boot.test.context.SpringBootTest;
@SpringBootTest
class SpringbootApplicationTests {
	@Test
	void contextLoads() {
	}
}
```
#### 20250424 (2-1)2.前端结构  
vue/  
├── public/ -----------------------静态文件目录  
│   ├── favicon.ico--------------------图标文件  
│   └── index.html---------------------入口模板  
├── src/ --------------------------项目源码目录  
│   ├── *main.js*----------------------*入口文件*  
│   ├── [App.vue]----------------------[入口组件] 
│   ├── views/ --------------------[视图文件目录] 
│   │   ├── [HomeView.vue] 
│   │   ├── [AboutView.vue] 
│   ├── components/ ---------------[视图组件目录] 
│   │   ├── [HelloWorld.vue] 
│   ├── router/  
│   │   └── *index.js*-----------------*路由配置*  
│   ├── utils/  
│   │   └── *request.js*---------------*封装鉴权*  
│   └── assets/ -------------------静态文件目录  
│       ├── global.css-----------------*全局样式*  
│       └── bg.jpg---------------------图片资源  
└── *vue.config.js*--------------------配置文件  
#### 20250424 (2-1)2.后端结构  
业务逻辑：Controller=>Service=>Dao(Mapper)=>Entity=>数据库  
springboot/  
├── src/test/com/example/  
│   │            └── [SpringBootApplicationTests.java]----测试类  
│   └── main/  
│       ├── resources/  
│       │   ├── *application.yml(.properties)* -----------*配置类*  
│       │   └── mapper/  
│       │       └── *XxxMapper.xml* -----------------------[持久层映射] 
│       └── java/com/example/  
│                    ├── [SpringbootApplication.java]-----[启动类] 
│                    ├── common/  
│                    │   └── [Result.java]----------------[统一返回类型] 
│                    │   └── [WebConfig.java]-------------(后端鉴权配置统一前缀、拦截器配置)  
│                    │   └── [CorsConfig.java]------------(后端鉴权全局配置跨域资源共享)  
│                    │   └── [JwtTokenUtils.java]---------(后端鉴权Jwt拦截器，生成token、获取用户)  
│                    │   └── [JwtInterceptor.java]--------(后端鉴权Jwt拦截器，验证token、抛出异常)  
│                    │   └── [CaptureConfig.java]---------(图形验证码工具类)  
│                    │   └── [AutoLog.java(Interface)]----(日志记录自定义注解接口)  
│                    │   └── [LogAspect.java]-------------(日志记录面向切面编程类)  
│                    ├── exception/ -----------------------[异常处理] 
│                    │   └── [GlobalExceptionHandler.java]-(后端异常处理全局异常捕获器)  
│                    │   └── [CustomException.java]--------(后端异常处理自定义异常)  
│                    ├── controller/ ----------------------[前后端接口] 
│                    │   └── [XxxController.java] 
│                    ├── service/ -------------------------[后端业务层] 
│                    │   └── [XxxService.java] 
│                    ├── dao/ -----------------------------[后端持久层] 
│                    │   └── [XxxDao.java(Interface)] 
│                    └── entity/ --------------------------[实体类对象] 
│                        └── [XxxEntity.java] 
│                        └── [Params.java]----------------[接收前端参数实体类] 
└── *pom.xml* ---------------------------------------------*依赖包*  
#### 20250315 (2-2)1.常用依赖(MVNREPOSITORY)  
0. 复制依赖 MVNREPOSITORY：https://mvnrepository.com/  
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
		<dependency>
			<groupId>com.github.whvcse</groupId>
			<artifactId>easy-captcha</artifactId>
			<version>1.6.2</version>
		</dependency>
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
		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-aop</artifactId>
		</dependency>
		<dependency>
			<groupId>org.apache.poi</groupId>
			<artifactId>poi-ooxml</artifactId>
			<version>4.1.2</version>
		</dependency>
		<dependency>
			<groupId>org.openjdk.nashorn</groupId>
			<artifactId>nashorn-core</artifactId>
			<version>15.4</version>
		</dependency>
```
1. mybatis-spring-boot-starter  
作用：整合 MyBatis 和 Spring Boot，提供自动配置功能。  
功能：自动配置 MyBatis 的 SqlSessionFactory 和 SqlSessionTemplate，支持 XML 映射文件和注解方式，简化 MyBatis 的配置。  
2. mysql-connector-java  
作用：MySQL 的 JDBC 驱动，用于连接 MySQL 数据库。  
功能：提供与 MySQL 数据库的连接功能，支持 SQL 查询和更新操作，适用于 Spring Boot 的数据访问层。  
3. mapper  
作用：MyBatis 的增强工具，提供通用 Mapper 功能。  
功能：提供通用的 CRUD 操作，减少重复代码，支持自定义 SQL 和动态 SQL，提高开发效率。  
4. pagehelper-spring-boot-starter  
作用：分页插件，用于实现分页功能。  
功能：自动拦截 SQL 查询，实现分页逻辑，提供分页信息，简化分页代码。  
5. easy-captcha  
作用：用于生成验证码。  
功能：提供生成验证码的功能，支持多种验证码类型，常用于登录验证、注册验证等场景。  
6. java-jwt  
作用：用于生成和解析 JSON Web Tokens (JWT)。  
功能：提供 JWT 的生成和解析功能，支持多种加密算法，常用于实现基于 JWT 的身份验证和授权机制。  
7. hutool-all  
作用：一个 Java 工具类库，提供丰富的工具类。  
功能：提供字符串处理、日期时间处理、文件操作、网络请求等工具类，简化常见的 Java 开发任务。  
8. spring-boot-starter-aop  
作用：提供 Spring AOP（面向切面编程）的支持。  
功能：支持切面编程，用于实现日志记录、事务管理、权限校验等横切关注点，简化 AOP 的配置。  
9. poi-ooxml  
作用：用于读写 Excel 文件（支持 .xls 和 .xlsx 格式）。  
功能：提供读取和写入 Excel 文件的功能，支持复杂的 Excel 操作，常用于数据导入导出功能。  
10. nashorn-core  
作用：提供 Nashorn JavaScript 引擎的支持。  
功能：提供 JavaScript 的解析和执行功能，支持在 Java 应用程序中运行 JavaScript 代码，适用于脚本执行、动态代码生成等场景。  
#### 20250315 (2-2)1.常用注解  
##### [-]Others  
1. @Component  
是一个类级别的注解，用于标记一个类为 Spring 容器管理的 Bean  
2. @Override  
当前方法的是重写父类中的方法  
3. @Resource  
将 Spring 容器中的 Bean 注入到字段或方法中  
`private AdminService adminService;`  
##### [1]Exception  
1. @ControllerAdvice(basePackages="com.example.controller")  
标记全局异常捕获器，指定包中的控制器会被当前的 `@ControllerAdvice` 类影响  
2. @ExceptionHandler(Exception.class)  
定义异常处理方法(所有异常类型)  
3. @ExceptionHandler(CustomException.class)  
定义异常处理方法(自定义异常)  
4. @ResponseBody  
将方法的返回值直接作为 HTTP 响应体返回给客户端  
##### [2]Config  
1. @Configuration  
定义 Spring 的配置类，替代传统的 XML 配置文件  
2. @Bean  
是一个方法级别的注解，用于在配置类中显式地声明一个 Bean  
##### [3]Jwt  
1. @Component  
2. @PostConstruct  
通常用于在 Spring 容器初始化一个 Bean 之后，执行一些初始化逻辑  
##### [4]Log  
1. @Component  
2. @Aspect  
注解标记切面类  
3. @Around("@annotation(autoLog)")  
注解用于定义环绕通知  
  `@Around`环绕通知可以在目标方法执行之前和之后执行自定义逻辑  
  `@annotation`表示匹配带有某个注解的方法  
  `@annotation(autoLog)`表示匹配所有带有@AutoLog注解的方法  
4. @Target(ElementType.METHOD)  
自定义注解，注解只能应用于方法上  
5. @Retention(RetentionPolicy.RUNTIME)  
自定义注解，注解在运行时仍然可用  
6. @Documented  
自定义注解，注解应该被包含在JavaDoc中  
使用了@AutoLog方法会显示相关信息  
7. @AutoLog("登录该系统")  
自定义注解，使用方法  
##### [-]SpringBoot  
1. @SpringBootApplication  
启动类  
是`@SpringBootConfiguration``@EnableAutoConfiguration``@ComponentScan`的组合注解  
  `@SpringBootConfiguration`表示当前类是一个 Spring Boot 配置类  
  `@EnableAutoConfiguration`自动启用 Spring Boot 的自动配置功能  
  `@ComponentScan`启用组件扫描功能  
2. @MapperScan("com.example.dao")  
MyBatis 提供的注解，用于指定 MyBatis Mapper 接口的扫描路径  
你可以在 com.example.dao 包下定义所有的 Mapper 接口，而不需要在每个接口上手动添加 @Mapper 注解  
3. @SpringBootTest  
测试类  
4. @Test  
测试方法  
##### [1]Controller  
1. @CrossOrigin  
允许跨域请求访问当前控制器或方法  
解决跨域资源共享（CORS，Cross-Origin Resource Sharing）问题  
它允许后端服务在处理 HTTP 请求时，动态地添加响应头，以支持跨域请求  
1. @RestController  
Controller层  
是`@Controller``@ResponseBody`的组合注解  
1. @RequestMapping("/admin")  
定义控制器的根路径为 /admin  
2. @GetMapping("/search")  
对应前端GET请求  
2. @PostMapping("/login")  
对应前端POST请求  
2. @DeleteMapping("/{id}")  
对应前端DELETE请求  
等同于 `@RequestMapping(method = RequestMethod.DELETE)`  
3. @RequestBody  
用于接收 请求体 `request.post("/admin", this.form)`  
3. @RequestParam  
用于接收 URL 查询参数 `request.post("/admin/login?key=" + this.key, this.admin)`  
3. @PathVariable  
用于接收 URL 路径参数 `request.delete("/admin/" + id)`  
##### [2]Service  
1. @Service  
Service层  
##### [3]Dao  
1. @Repository  
Dao层  
2. @Select("select * from admin where name = #{name} limit 1")  
SQL语句  
3. @Param("name")  
@Param注解通常用于在Repository接口中为方法参数命名，方便在SQL语句中引用这些参数
##### [4]Entity  
1. @Table(name = "admin")  
对应数据库表  
2. @Id  
主键  
3. @GeneratedValue(strategy = GenerationType.IDENTITY)  
自增  
指定主键生成策略为数据库自增（适用于MySQL、PostgreSQL等支持自增主键的数据库）  
4. @Column(name = "column-name")  
对应数据库字段  
指定该字段映射到数据库表中的name列  
5. @Transient  
对应非数据库字段  
#### 20250315 (2-2)2.常用组件(ElementUI)  
##### [-]Element官网  
1. Icon 图标：https://element.eleme.cn/#/zh-CN/component/icon  
1. Container 布局容器：https://element.eleme.cn/#/zh-CN/component/container  
2. Button 按钮：https://element.eleme.cn/#/zh-CN/component/button  
3. Radio 单选框：https://element.eleme.cn/#/zh-CN/component/radio  
3. Checkbox 多选框：https://element.eleme.cn/#/zh-CN/component/checkbox  
3. Input 输入框：https://element.eleme.cn/#/zh-CN/component/input  
3. Select 选择器：https://element.eleme.cn/#/zh-CN/component/select  
3. Switch 开关：https://element.eleme.cn/#/zh-CN/component/switch  
3. TimePicker 时间选择器：https://element.eleme.cn/#/zh-CN/component/time-picker  
3. DatePicker 日期选择器：https://element.eleme.cn/#/zh-CN/component/date-picker  
3. DateTimePicker 日期时间选择器：https://element.eleme.cn/#/zh-CN/component/datetime-picker  
4. Form 表单：https://element.eleme.cn/#/zh-CN/component/form  
5. Table 表格：https://element.eleme.cn/#/zh-CN/component/table  
6. Pagination 分页：https://element.eleme.cn/#/zh-CN/component/pagination  
7. Dialog 对话框：https://element.eleme.cn/#/zh-CN/component/dialog  
8. NavMenu 导航菜单：https://element.eleme.cn/#/zh-CN/component/menu  
9. Dropdown 下拉菜单：https://element.eleme.cn/#/zh-CN/component/dropdown  
10. Popconfirm 气泡确认框：https://element.eleme.cn/#/zh-CN/component/popconfirm  
##### [1]Container 布局容器  
```js
<el-container>
  <el-header>Header</el-header>
  <el-container>
    <el-aside width="200px">Aside</el-aside>
    <el-container>
      <el-main>Main</el-main>
      <el-footer>Footer</el-footer>
    </el-container>
  </el-container>
</el-container>
```
```js
<style>
  .el-header, .el-footer {//用途：通常用于页面的头部（导航栏）和底部（页脚）。
    background-color: #B3C0D1;//背景颜色：#B3C0D1，一种浅蓝色。
    color: #333;//文字颜色：#333，深灰色。
    text-align: center;//文本对齐方式：居中对齐。
    line-height: 60px;//行高：60px，用于控制内容的垂直居中显示。
  }
  
  .el-aside {//用途：通常用于侧边栏，放置菜单、工具栏等。
    background-color: #D3DCE6;//背景颜色
    color: #333;//文字颜色
    text-align: center;//对齐方式
    line-height: 200px;//行高
  }
  
  .el-main {//用途：通常用于主内容区域。
    background-color: #E9EEF3;
    color: #333;
    text-align: center;
    line-height: 160px;
  }
  
  body > .el-container {//为 .el-container 添加底部外边距，用于控制布局之间的间距
    margin-bottom: 40px;
  }
  
  .el-container:nth-child(5) .el-aside,
  .el-container:nth-child(6) .el-aside {
    //用途：通过 :nth-child 选择器，可以针对特定的 .el-container 元素调整样式，而不会影响其他元素
    line-height: 260px;//用于调整特定 .el-container 中的 .el-aside 的行高。
  }
  
  .el-container:nth-child(7) .el-aside {
    line-height: 320px;//用于调整特定 .el-container 中的 .el-aside 的行高。
  }
</style>
```
1. `<el-container>`：外层容器。  
(1)当子元素中包含 `<el-header>` 或 `<el-footer>` 时，全部子元素会垂直上下排列，否则会水平左右排列。  
(2)此外，`<el-container>` 的子元素只能是后四者，后四者的父元素也只能是 `<el-container>`。  
2. `<el-header>`：顶栏容器。  
3. `<el-aside>`：侧边栏容器。  
4. `<el-main>`：主要区域容器。  
5. `<el-footer>`：底栏容器。  
6. `body > .el-container{}`选择 body 的直接子元素  
(1)`body`：HTML 文档的主体部分，包含页面的所有可见内容。  
(2)`>`：子代选择器，表示选择 body 的直接子元素（即 body 的一级子元素）。  
(3)`.el-container`：一个类名为 el-container 的元素。  
(4)这个选择器的作用是选择 body 元素的直接子元素 .el-container。  
(5)它不会影响嵌套在其他元素内部的 .el-container。  
7. `:nth-child(n)`伪类选择器  
(1)用于选择父元素的第 n 个子元素。  
(2)它不考虑子元素的类型，只按顺序选择。  
8. `.el-container:nth-child(5) .el-aside`选择 .el-container 元素中的第 5 个子元素内的 .el-aside 元素  
(1)`.el-container`：选择页面中所有类名为 .el-container 的元素。  
(2)`:nth-child(5)`：伪类选择器，表示选择父元素的第 5 个子元素。如果 .el-container 是其父元素的第 5 个子元素，则会被选中。  
(3)`.el-aside`：在被选中的 .el-container 内部，选择类名为 .el-aside 的元素。  
(4)这个选择器的作用是选择 .el-container 元素中的第 5 个子元素内的 .el-aside 元素  
##### [2]Button 按钮  
```js
<el-row>
  <el-button>默认按钮</el-button>
  <el-button plain>朴素按钮</el-button>
  <el-button round>圆角按钮</el-button>
  <el-button icon="el-icon-search" circle></el-button>
  <el-button type="primary" plain>主要按钮</el-button>
  <el-button type="success" plain>成功按钮</el-button>
  <el-button type="info" plain>信息按钮</el-button>
  <el-button type="warning" plain>警告按钮</el-button>
  <el-button type="danger" plain>危险按钮</el-button>
</el-row>
```
1. 按钮的样式包括颜色属性和风格属性  
(1)两种属性可以组合使用，也可以都不使用  
(2)当风格为图标按钮时，使用图标取代文字释义  
2. 按钮颜色，对应"type"属性  
(1)默认按钮：不添加type属性 效果：白色  
(2)主要按钮：type="primary" 效果：蓝色  
(3)成功按钮：type="success" 效果：绿色  
(4)信息按钮：type="info" 效果：灰色  
(5)警告按钮：type="warning" 效果：橙色  
(6)危险按钮：type="danger" 效果：红色  
3. 按钮风格，对应"plain"、"round"、"circle"属性  
(1)默认按钮：不添加形状属性 效果：按钮为直角矩形  
(2)朴素按钮："plain" 效果：按钮颜色方案更改  
(3)圆角按钮："round" 效果：按钮为圆角矩形  
(4)图标按钮："circle" 效果：按钮使用图标取代文字释义  
4. 按钮图标，对应"icon"属性  
(1)搜索图标：icon="el-icon-search"  
(2)编辑图标：icon="el-icon-edit"  
(3)对号图标：icon="el-icon-check"  
(4)消息图标：icon="el-icon-message"  
(5)收藏图标：icon="el-icon-star-off"  
(6)删除图标：icon="el-icon-delete"  
##### [3]Radio 单选框  
```js
<p>当前选中的值是：{{ radio }}</p>
<el-radio border v-model="radio" label="1">备选项1</el-radio>
<el-radio border v-model="radio" label="2">备选项2</el-radio>
<el-radio disabled v-model="radio" label="3">备选项3</el-radio>
<el-radio-group v-model="radio" size="medium">
  <el-radio-button :label="3">备选项</el-radio>
  <el-radio-button :label="6">备选项</el-radio>
  <el-radio-button :label="9">备选项</el-radio>
</el-radio-group>
```
```js
<script>
  export default {
    data () {
      return {
        radio: ''
      };
    }
  }
</script>
```
1. "label"选中状态  
(1)指定单选按钮的值：当单选按钮被选中时，v-model 绑定的变量会被设置为 label 的值。  
(2)控制单选按钮的选中状态：如果 v-model 的值与某个 `<el-radio>` 的 label 值相同，那么这个单选按钮会被选中。  
1. 单选禁用，对应"disabled"属性  
(1)disabled接收布尔值，默认为true。  
(2)效果：单选项变为灰色不可更改选择状态。  
(3)可以禁用选中选项和未选中选项。  
1. 单选组，对应`<el-radio-group>`标签  
(1)在el-radio-group中绑定v-model  
(2)无需再给每一个el-radio绑定变量  
1. 单选按钮，对应`<el-radio-button>`标签  
(1)由"size"属性控制单选按钮的大小。  
(2)"size"属性可为"medium"、"small"、"mini"。  
1. 单选边框，对应"border"属性
设置 border 属性可以渲染为带有边框的单选框。  
##### [5]Input 输入框  
```js
<el-input v-model="input" type="textarea" autocomplete="off" placeholder="请输入内容"></el-input>
```
```js
<script>
export default {
  data() {
    return {
      input: ''//绑定动态数据
    }
  }
}
</script>
```
1. "v-model"绑定动态数据  
2. "placeholder"指定输入框的提示信息  
3. `type="textarea"`文本域  
4. "autocomplete"自动填充  
(1)`on`：浏览器会自动填充输入框的内容，通常基于用户之前输入的历史数据。  
(2)`off`：浏览器不会自动填充输入框的内容。  
##### [6]Select 选择器  
```js
<el-select v-model="value" placeholder="请选择">
  <el-option v-for="item in options" :key="item.value"
    :label="item.label"
    :value="item.value"
  >
  </el-option>
</el-select>
```
```js
<script>
  export default {
    data() {
      return {
        options: [{
          label: '黄金糕',value: '选项1'}, 
        {label: '双皮奶',value: '选项2'}, 
        {label: '蚵仔煎',value: '选项3'}, 
        {label: '龙须面',value: '选项4'}, 
        {label: '北京烤鸭',value: '选项5'}
        ],
      }
    }
  }
</script>
```
1. "placeholder"提示信息  
2. "label"显示文本  
3. "value"指定选项的值  
##### [7]Form 表单  
```js
<el-form ref="form" :model="form" :inline="true" label-width="80px">
  <el-form-item label="Radio 单选框">
    <el-radio-group v-model="form.radio_options">
      <el-radio label="单选框选项1"></el-radio>
      <el-radio label="单选框选项2"></el-radio>
    </el-radio-group>
  </el-form-item>
  <el-form-item label="Checkbox 多选框">
    <el-checkbox-group v-model="form.check_options">
      <el-checkbox label="多选框选项1" name="check_options"></el-checkbox>
      <el-checkbox label="多选框选项2" name="check_options"></el-checkbox>
      <el-checkbox label="多选框选项3" name="check_options"></el-checkbox>
      <el-checkbox label="多选框选项4" name="check_options"></el-checkbox>
    </el-checkbox-group>
  </el-form-item>
  <el-form-item label="Input 输入框">
    <el-input v-model="form.input_content"></el-input>
  </el-form-item>
  <el-form-item label="Input 输入框 (文本域)">
    <el-input type="textarea" v-model="form.input_desc"></el-input>
  </el-form-item>
  <el-form-item label="Select 选择器">
    <el-select v-model="form.select_region" placeholder="请选择下拉选项">
      <el-option label="下拉选项1" value="shanghai"></el-option>
      <el-option label="下拉选项2" value="beijing"></el-option>
    </el-select>
  </el-form-item>
  <el-form-item label="Switch 开关">
    <el-switch v-model="form.switch_delivery"></el-switch>
  </el-form-item>
  <el-form-item label="日期、时间选择器">
    <el-col :span="11">
      <el-date-picker type="date" placeholder="选择日期" v-model="form.date" style="width: 100%;"></el-date-picker>
    </el-col>
    <el-col class="line" :span="2">-</el-col>
    <el-col :span="11">
      <el-time-picker placeholder="选择时间" v-model="form.time" style="width: 100%;"></el-time-picker>
    </el-col>
  </el-form-item>
  <el-form-item>
    <el-button type="primary" @click="onSubmit">立即创建</el-button>
    <el-button>取消</el-button>
  </el-form-item>
</el-form>
```
```js
<script>
  export default {
    data() {
      return {
        form: {
          radio_options: '',
          check_options: [],
          input_content: '',
          input_desc: ''
          select_region: '',
          date: '',
          time: '',
          switch_delivery: false,
        }
      }
    },
    methods: {
      onSubmit() {
        console.log('submit!');
      }
    }
  }
</script>
```
1. 在 Form 组件中  
(1)每一个表单域由一个 Form-Item 组件构成，表单域中可以放置各种类型的表单控件  
(2)包括 Radio、Checkbox、Input、Select、Switch、DatePicker、TimePicker  
(3)`:model="form"`  
##### [8]Table 表格  
```js
<el-table :data="tableData" style="width: 100%; margin: 15px 0px">
  <el-table-column prop="column1" label="第1列" width="180"></el-table-column>
  <el-table-column prop="column2" label="第2列" width="180"></el-table-column>
  <!-- 第3列... -->
</el-table>
```
```js
<script>
  export default {
    data() {
      return {
        tableData: [
          {column1: '第1行 第1列',column2: '第1行 第2列'},//第1行 
          {column1: '第2行 第1列',column2: '第2行 第2列'},//第2行 
          {column1: '第3行 第1列',column2: '第3行 第2列'}]//第3行 ...
      }
    }
  }
</script>
```
1. "prop"对应数据库字段名  
2. "label"对应列名  
3. "width"对应列宽  
##### [9]Pagination 分页  
```js
<el-pagination
  @size-change="handleSizeChange"
  @current-change="handleCurrentChange"
  :current-page="currentPage1"
  :page-sizes="[100, 200, 300, 400]"
  :page-size="100"
  :pager-count="11"
  :total="400"
  layout="total, sizes, prev, pager, next, jumper"
  background
  small
  :hide-on-single-page="value"
>
</el-pagination>
```
```js
<script>
  export default {
    data() {
      return {
        value: false,
        currentPage1: 1,
        currentPage2: 2,
        currentPage3: 3,
        currentPage4: 4
      };
    },
    methods: {
      handleSizeChange(val) {
        console.log(`${val}条/页`);
      },
      handleCurrentChange(val) {
        console.log(`当前页: ${val}`);
      }
    }
  }
</script>
```
1. 分页模块，对应"layout"属性  
(1)切换上页模块："prev" 效果：`<`  
(2)切换下页模块："next" 效果：`>`  
(3)页码列表模块："pager" 效果：每页对应按钮，如 `1 2 3 ...`  
折叠页码 `:pager-count="11"` 效果：从第11页(包括11)开始隐藏页码列表(默认从第8页)  
(4)总共几条模块："total" 效果：共几条，如 `共0条`  
(5)每页几条模块："sizes" 效果：几条/页，如 `0条/页`  
(6)前往几页模块："jumper" 效果：前往几页，如 `前往0页`  
(7)向右对齐语法："->"  效果：此符号之后的元素会靠右显示  
2. 分页样式，对应"background"、"small"属性  
(1)添加背景："background" 效果：分页按钮带上浅灰的背景色  
(2)小型分页："small" 效果：分页按钮整体比例缩小  
3. 绑定事件，对应"size-change"、"current-change"属性  
(1)切换每页几条：`@size-change="handleSizeChange"`  
(2)切换当前页码：`@current-change="handleCurrentChange"`  
4. 绑定数据，对应"current-page"、"page-sizes"、"total"、"hide-on-single-page"属性  
(1)当前页码：`:current-page="5"` 效果：当前页码5显示高亮  
(2)每页条数：`:page-sizes="[100, 200, 300, 400]"` 效果：`100条/页`下拉列表  
(3)每页条数：`:page-size="100"` 效果：`100条/页`  
(4)总条目数：`:total="50"` 效果：`共50条`  
(5)隐藏分页：`:hide-on-single-page="true"` 效果：当只有一页时，设置true可以隐藏分页  
##### [10]Dialog 对话框  
```js
<el-dialog
  title="提示" width="30%"
  :visible.sync="dialogVisible"
  :before-close="handleClose"
>
  <span>这是一段信息</span>
  <span slot="footer" class="dialog-footer">
    <el-button @click="dialogVisible = false">取 消</el-button>
    <el-button type="primary" @click="dialogVisible = false">确 定</el-button>
  </span>
</el-dialog>
```
```js
<script>
  export default {
    data() {
      return {
        dialogVisible: false
      };
    },
    methods: {
      handleClose(done) {
        this.$confirm('确认关闭？')
          .then(_ => {
            done();
          })
          .catch(_ => {});
      }
    }
  };
</script>
```
1. 对话框分为 body 和 footer  
(1)body 包括 标题信息、内容信息  
(2)footer 包括 取消按钮、确定按钮  
2. body 部分  
(1)标题信息，对应"title"属性  
(2)内容信息，对应`<span>`标签  
(3)弹框宽度，对应"width"属性  
3. footer 部分  
(1)footer 需要具名为 footer 的 slot  
(2)`slot="footer" class="dialog-footer"`  
4. "visible"绑定数据控制对话框显隐  
为true时弹出对话框  
5. "before-close"绑定事件对话框确认关闭操作  
(1)before-close 仅当用户通过点击关闭图标或遮罩关闭 Dialog 时起效。  
(2)如果你在 footer 具名 slot 里添加了用于关闭 Dialog 的按钮，  
  那么可以在按钮的点击回调函数里加入 before-close 的相关逻辑。  
6. `handleClose(done) {}`函数  
(1)当调用 handleClose(done) 方法时，会弹出一个确认对话框，提示用户是否确认关闭。  
(2)如果用户点击“确认”，则执行 done()，这通常会触发关闭操作。  
(3)如果用户点击“取消”，则什么都不做（catch 中为空）。  
7. `done` 参数：  
(1)done 是一个回调函数，通常由调用方传入。它的作用是通知调用方可以安全地关闭当前组件。  
(2)在 Vue.js 的某些场景中（如 el-dialog 的 before-close 回调），done 是一个必须调用的函数，用于完成关闭操作。  
8. `this.$confirm`：  
(1)这是 Vue.js 中 Element UI 提供的一个全局方法，用于显示确认对话框。  
(2)它返回一个 Promise：  
(3)如果用户点击“确认”，Promise 解析（then）。  
(4)如果用户点击“取消”，Promise 拒绝（catch）。  
##### [11]NavMenu 导航菜单  
```js
<el-menu
  default-active="2" class="el-menu-vertical-demo"
  @open="handleOpen" @close="handleClose"
  background-color="#545c64" text-color="#fff" active-text-color="#ffd04b"
>
  <el-submenu index="1">
    <template slot="title">
      <i class="el-icon-location"></i><span>导航一</span>
    </template>
    <el-menu-item-group>
      <template slot="title">分组一</template>
      <el-menu-item index="1-1">选项1</el-menu-item>
      <el-menu-item index="1-2">选项2</el-menu-item>
    </el-menu-item-group>
    <el-menu-item-group title="分组二">
      <el-menu-item index="1-3">选项3</el-menu-item>
    </el-menu-item-group>
    <el-submenu index="1-4">
      <template slot="title">选项4</template>
      <el-menu-item index="1-4-1">选项1</el-menu-item>
    </el-submenu>
  </el-submenu>

  <el-menu-item index="2"><i class="el-icon-menu"></i><span slot="title">导航二</span></el-menu-item>
  <el-menu-item index="3" disabled><i class="el-icon-document"></i><span slot="title">导航三</span></el-menu-item>
  <el-menu-item index="4"><i class="el-icon-setting"></i><span slot="title">导航四</span></el-menu-item>
</el-menu>
```
```js
<style>
.el-menu-vertical-demo{
  border-right: none !important;
}
</style>
<script>
  export default {
    methods: {
      handleOpen(key, keyPath) {
        console.log(key, keyPath);
      },
      handleClose(key, keyPath) {
        console.log(key, keyPath);
      }
    }
  }
</script>
```
1. `<el-menu>`导航菜单  
2. `<el-submenu>`下拉菜单集  
3. `<el-menu-item-group>`菜单项分组  
4. `<el-menu-item>`子菜单项、独立菜单项  
(1)在`<el-submenu>`后使用，表示子菜单项  
(2)在`<el-menu-item-group>`后使用，表示子菜单项  
(2)单独使用，表示独立菜单项  
5. `slot="title"`首菜单项、分组名  
(1)在`<el-submenu>`后使用，表示首菜单项 `<template slot="title">`  
(2)在`<template>`中使用，表示首菜单项 `<template slot="title">`  
(3)在`<span>`中使用，表示独立菜单项 `<span slot="title">`  
(4)在`<el-menu-item-group>`中使用，表示分组名`<el-menu-item-group slot="title">`  
6. "index"属性  
(1)菜单集的索引`<el-submenu index="1">`  
(2)菜单项的索引`<el-menu-item index="2">`  
(3)可用于表示路由路径url  
7. "default-active"属性  
(1)默认激活菜单项  
(2)对应"index"属性  
8. "disabled"属性  
禁用菜单项`<el-menu-item disabled>`  
9. "class"属性
更改样式，纠正边距小瑕疵  
10. 自定义颜色，对应"background-color"、"text-color"、"active-text-color"属性  
(1)背景颜色：background-color  
(2)文字颜色：text-color  
(3)激活文字：active-text-color  
##### [12]Dropdown 下拉菜单
```js
<el-dropdown @command="handleCommand">
  <span class="el-dropdown-link">
    下拉菜单<i class="el-icon-arrow-down el-icon--right"></i>
  </span>
  <el-button type="primary">
    更多菜单<i class="el-icon-arrow-down el-icon--right"></i>
  </el-button>
  <el-dropdown-menu slot="dropdown">
    <el-dropdown-item command="a">黄金糕</el-dropdown-item>
    <el-dropdown-item command="b">狮子头</el-dropdown-item>
    <el-dropdown-item command="c">螺蛳粉</el-dropdown-item>
    <el-dropdown-item command="d" disabled>双皮奶</el-dropdown-item>
    <el-dropdown-item command="e" divided>蚵仔煎</el-dropdown-item>
  </el-dropdown-menu>
</el-dropdown>

<el-dropdown split-button size="medium" type="primary" @click="handleClick">
  更多菜单
  <el-dropdown-menu slot="dropdown">
    <el-dropdown-item>黄金糕</el-dropdown-item>
    <el-dropdown-item>狮子头</el-dropdown-item>
    <el-dropdown-item>螺蛳粉</el-dropdown-item>
    <el-dropdown-item>双皮奶</el-dropdown-item>
    <el-dropdown-item>蚵仔煎</el-dropdown-item>
  </el-dropdown-menu>
</el-dropdown>
```
```js
<style>
  .el-dropdown-link {
    cursor: pointer;
    color: #409EFF;
  }
  .el-icon-arrow-down {
    font-size: 12px;
  }
</style>
```
```js
<script>
  export default {
    methods: {
      handleCommand(command) {
        this.$message('click on item ' + command);
      },
      handleClick() {
        alert('button click');
      }
    }
  }
</script>
```
1. `class="el-dropdown-link"`设置手型图标  
(1)"class"属性不是必须的  
(2)定义CSS样式`.el-dropdown-link {}`  
  cursor 效果：鼠标悬停时变为手型图标  
  color 效果：设置文本颜色  
2. `<i class="el-icon-arrow-down el-icon--right"></i>` 标签  
(1)不使用class，用于表示斜体文本  
(2)使用class，用于插入图标  
  el-icon-arrow-down 效果：下拉选项图标  
  el-icon--right 效果：将图标对齐到其父元素的右侧  
(3)定义CSS样式`.el-icon-arrow-down {}`  
  font-size 效果：设置文本大小  
3. `slot="dropdown"`设置下拉菜单  
"slot"属性不是必须的  
4. "disabled"禁用下拉选项  
5. "divided"选项分割线  
6. "command"绑定选项  
  `@command="handleCommand"`绑定点击事件  
  `command="a"`传递选项参数  
7. "split-button"下拉按钮组  
(1)左边是功能按钮，右边是下拉菜单  
(2)绑定事件`@click="handleClick"`  
8. "size"下拉按钮组尺寸  
(1)默认尺寸，不设置此属性  
(1)中等尺寸，size="medium"  
(1)小型尺寸，size="small"  
(1)超小尺寸，size="mini"  
##### [13]Popconfirm 气泡确认框
```js
<el-popconfirm
  cancel-button-text='不用了'
  confirm-button-text='好的'
  icon="el-icon-info"
  icon-color="red"
  title="这是一段内容确定删除吗？"
>
  <el-button slot="reference">删除</el-button>
</el-popconfirm>
```
1. `slot="reference"` 用于指定触发弹出确认框的元素。  
2. "title"自定义气泡框内容  
3. "cancel-button-text"自定义气泡框取消按钮  
4. "confirm-button-text"自定义气泡框确认按钮  
5. "icon"自定义气泡框图标  
6. "icon-color"自定义气泡框图标颜色  
##### [14]Drawer 抽屉  
#### 20250315 (2-2)2.常用样式  
##### [1]页面导航
```js
<nav style="font-size: 13px;color: #00c1ed">
  <router-link to="/" style="color: #00c1ed;text-decoration: none">Home</router-link> |
  <router-link to="/login" style="color: #00c1ed;text-decoration: none">Login</router-link> |
  <router-link to="/register" style="color: #00c1ed;text-decoration: none">Register</router-link>
</nav>
```
##### [2]背景模块
1. div：`<div class="login-container"></div>`背景容器  
2. style：`<style scoped>.login-container {}</style>`背景容器  
  height: 100vh;  
  background-image: url("@/assets/login_bg1.png");  
  background-size: 50%;  
  overflow: hidden;  
  display: flex;  
  align-items: center;  
  justify-content: center;  
(1)scoped：该样式只会应用于当前组件或当前 HTML 文件中的元素，而不会影响其他组件或页面的样式。  
(2)@ 是一个路径别名，通常在 Vue.js 项目中用于表示 src 目录  
(3)height：定义视口高度，高度占据整个屏幕  
(4)background-image：设置容器的背景图片  
(5)background-size：将背景图片的宽度设置为容器宽度的 50%  
(6)overflow：隐藏超出容器的内容  
(7)display：使用弹性布局，方便地对子元素进行水平和垂直对齐  
(8)align-items：在弹性布局中，这个属性会将子元素垂直居中对齐  
(9)justify-content：在弹性布局中，这个属性会将子元素水平居中对齐  
##### [3]布局模块
1. el-container：`<el-container style=""></el-container>`布局容器  
  style="overflow: auto;height: 100vh"  
(1)超出页面的内容，设置滚动条  
2. el-header：`<el-header style=""></el-header>`顶栏  
3. el-aside：`<el-aside style=""></el-aside>`侧栏  
4. el-main：`<el-main></el-main>`主内容区  
##### [4]顶栏模块
1. el-header：`<el-header style=""></el-header>`顶栏  
  background-color: rgba(0,215,236,0.17);  
  height: 50px;  
  text-align: center;  
  line-height: 50px;  
(1)背景填充颜色  
(2)顶栏占据高度  
(3)文本水平对齐方式 居中  
(4)元素垂直方向距离 与高度保持一致即为垂直居中效果  
2. span：`<span style=""></span>`顶栏标题  
  color: #00c1ed  
  font-size: 20px;  
(1)文本颜色  
(2)文本大小  
3. img：`<img src="" style="" alt="">`顶栏标志  
  src="@/assets/login_bg3.png"  
  style="  
    height: 40px;  
    float: left;  
    position: relative;  
    top: 5px;  
  "  
(1)@ 是一个路径别名，通常在 Vue.js 项目中用于表示 src 目录  
(2)图片大小 高40像素  
(3)脱离文档流浮动 左对齐  
(4)定位方式 相对定位：图片的位置可以相对于其正常位置进行调整，但不会脱离文档流  
(5)图片下移  
  将图片在垂直方向上向下移动 5 像素  
  由于使用了相对定位，图片仍然在文档流中，只是视觉上向下移动了 5 像素  
4. el-dropdown：`<el-dropdown style=""></el-dropdown>`顶栏用户下拉选项  
  style="float: right"  
(1)脱离文档流浮动 右对齐  
5. span：`<span class="" style=""></span>`顶栏用户下拉选项文本  
  class="el-dropdown-link"  
  style="color: #00c1ed; font-size: 15px"  
(1)定义CSS样式`.el-dropdown-link {cursor: pointer;}` 鼠标悬停时变为手型图标  
(2)文本颜色、文本大小  
6. i：`<i class=""></i>`顶栏用户下拉选项图标  
  class="el-icon-arrow-down el-icon--right"  
(1)下拉图标、图标位置  
##### [5]侧栏模块
1. el-aside：`<el-aside style=""></el-aside>`侧栏  
  width: 150px;  
  height: 100vh;  
  min-height: 100vh;  
  background-color: #b3cad6 ;  
  overflow: hidden;  
(1)侧栏宽度  
(2)侧栏高度 为视口高度的 100%  
(3)侧栏最小高度 为视口高度的 100%  
(4)背景颜色  
(5)隐藏超界内容 当内容超出侧边栏的边界时，超出部分将被隐藏，不会显示滚动条  
2. el-menu：`<el-menu router class="" background-color="" text-color="" active-text-color=""></el-menu>`侧栏导航菜单  
  class="el-menu-vertical-demo"  
  background-color="#c7deea"  
  text-color="#fff"  
  active-text-color="#006fff"  
  router 
  :default-active="$route.path"  
(1)定义CSS样式`el-menu-vertical-demo {border-right: none !important;}` 处理边界小瑕疵  
(2)背景颜色  
(3)文本颜色  
(4)文本激活颜色  
(5)router：启用路由模式，使菜单项与 Vue Router 的路由路径绑定  
(6)default-active：设置默认激活的菜单项，绑定为当前路由路径  
3. el-submenu：`<el-submenu></el-submenu>`导航选项集  
4. el-menu-item-group：`<el-menu-item-group></el-menu-item-group>`导航选项组  
5. el-menu-item：`<el-menu-item></el-menu-item>`导航选项  
6. i：`<i class=""></i>`侧栏导航菜单选项图标  
  class="el-icon-s-home"  
  class="el-icon-location"  
(1)首页  
(2)定位  
##### [6]主内容区
1. el-main：`<el-main><router-view/></el-main>`主内容区  
##### [7]登录模块
1. div：`<div style=""></div>`登录框  
  width: 400px;  
  height: 400px;  
  background-color:rgba(0,215,236,0.17);  
  border-radius: 10px  
  margin: 150px auto;  
(1)元素宽度  
(2)元素高度  
(3)背景颜色  
(4)元素圆角半径  
(5)元素外边距  
  150px 是上下外边距的值，元素的顶部和底部与父容器之间距离 150 像素  
  auto 是上下外边距的值，使元素在其父容器中水平居中  
2. div：`<div style=""></div>`登录标题文本  
  width: 100%;  
  height: 100px;  
  color: #00c1ed;  
  font-size: 30px;  
  text-align: center;  
  line-height: 100px;  
(1)元素宽度 宽度为父容器宽度的 100%  
(2)元素高度  
(3)元素颜色  
(4)文本字体大小  
(5)文本水平对齐方式 居中  
(6)行高  
3. div：`<div style=""></div>`登录元素布局  
  height: 320px;  
  margin-top: 25px;  
  text-align: center;  
(1)元素高度  
(2)元素上边距  
(3)文本水平对齐方式 居中  
4. div：`<div style=""></div>`登录验证码布局  
  display: flex;  
  justify-content: center  
(1)设置为一个弹性容器，使用弹性布局  
(2)控制子元素在主轴（默认是水平方向）上的对齐方式 水平居中  
5. div：`<div style=""></div>`登录跳转文本布局  
  style="text-align: center"  
(1)文本水平对齐方式 居中  
6. img：`<img width="" height="" />`登录验证码  
  width="140px"
  height="33px"
(1)宽度  
(2)高度  
7. el-input：`<el-input style="" prefix-icon="" placeholder="" show-password></el-input>`登录输入框  
  style="width: 42%; margin-right: 10px"  
  style="width: 80%"  
  prefix-icon="el-icon-user"  
  prefix-icon="el-icon-lock"  
  placeholder="请输入验证码"  
  placeholder="请输入用户名"  
  placeholder="请输入密码"  
  show-password  
(1)宽度、右外边距  
(2)图标  
(3)提示  
(4)显示密码按键  
8. el-button：`<el-button style=""></el-button>`登录按钮  
  width: 80%;  
  margin-top: 10px  
(1)宽度  
(2)上外边距  
9. a：`<a href="javascript:void(0)" style="text-decoration: none"></a>`登录跳转文本  
  href="javascript:void(0)"  
  style="color: #006fff;text-decoration: none"  
  style="color: #015c8c;"  
  text-align: center  
(1)用于创建一个“空链接”。  
  它表示点击链接时不会导航到任何页面，而是执行 JavaScript 表达式 void(0)，  
  该表达式返回 undefined，从而不会有任何页面跳转。  
(2)使得链接看起来更像是普通文本或按钮，而不是传统的超链接。  
  text-decoration 是 CSS 属性，用于控制文本的装饰效果。  
  none 表示移除文本的下划线（默认情况下，链接会显示下划线）。  
#### 20250428 (2-2)3.相关答疑  
##### [1]SpringBoot3新特性  
javax变更为jakarta`import jakarta.servlet.http.HttpServletRequest;`  
##### [2]=== 和 == 的区别  
```js
5 === 5; // true，值和类型都相同
5 == 5; // true，值和类型都相同
5 === 5.0; // true，值和类型都相同（都是数字类型）
5 == 5.0; // true，值和类型都相同
5 === "5"; // false，类型不同（一个是数字，一个是字符串）
5 == "5"; // true，类型不同，但会将 "5" 转换为数字 5 再比较
null === undefined; // false，类型不同
null == undefined; // true，特殊规则：null 和 undefined 相等
//== 转换规则
NaN == NaN; // false，特殊规则
true == 1; // true，true 转换为 1
false == 0; // true，false 转换为 0
[1]== 1; // true，对象转为字符串，字符串转为数字
[1]== "1"; // true，对象转为字符串
5 == "5"; // true，字符串转为数字
5 == "05"; // false，字符串转为数字，但 5 != 05
```
1. === == 比较值和类型  
(1)严格等于`===` 类型不同直接返回 false，不进行类型转换。  
(2)宽松等于`==` 类型不同，先进行类型转换再比较值。  
(3)建议优先使用 `===`，以避免意外的类型转换行为。  
2. == 转换规则  
特殊：null、undefined 返回 true  
特殊：NaN、任何值（包括自身）返回 false。  
布尔：布尔值转换为数字，true 转为 1false 转为 0。  
对象、字符串/数字：对象转换为字符串或数字。  
数字、字符串：字符串转换为数字。  
##### [3]登录鉴权Token验证  
1. 登录验证的原理  
(1)验证用户输入正误  
(2)验证token有效性  
(3)解释  
  登录验证包括两步，验证用户输入正误、验证token有效性  
  token验证不是为了检测用户输入正误，而是验证签名、用户ID、过期时间和其他字段等信息  
2. 验证token有效性的办法  
(1)工具类生成token  
  创建jwt生成工具`JWT.create()`
  以id作为token载荷`.withAudience(adminId)`  
  token过期时间为2小时`.withExpiresAt(DateUtil.offsetHour(new Date(), 2))`  
  用户密码加签作为token密钥`.sign(Algorithm.HMAC256(sign));`  
(2)工具类验证token  
  创建jwt验证器`JWT.require(Algorithm.HMAC256(admin.getPassword())).build()`  
  用户密码加签作为jwt验证器密钥`Algorithm.HMAC256(admin.getPassword())`  
  通过jwt验证器验证token有效性`jwtVerifier.verify(token);`  
(3)解释  
  token验证和生成token不同，只是都以用户密码加签作为密钥  
  token验证不是重新生成token，而是创建jwt验证器来验证token有效性  
##### [4]比较前端三种传递参数方式  
在 HTTP 请求中，传递参数的方式主要有三种：  
1. 请求体（Request Body）  
(1)请求体是 HTTP 请求的正文部分，通常用于 POST 和 PUT 请求  
  参数存储在 HTTP 请求的正文中  
  没有长度限制，适合传递大量数据，适合传递复杂的数据结构，如对象、数组等  
  比查询参数更安全，因为数据不会暴露在 URL 中  
(2)格式 请求体的内容类型可以是 JSON、表单数据（application/x-www-form-urlencoded）或文件等  
  `request.post("/admin", this.form)`  
  `request.post("/admin", { username: "admin", password: "password", role: "admin" });`  
2. URL 查询参数（Query Parameters）  
(1)URL 查询参数是附加在 URL 末尾的键值对，通常用于 GET 请求，但也可以用于其他类型的请求  
  参数附加在 URL 中，通过 ? 分隔  
  参数长度有限制（通常取决于浏览器和服务器的限制），不适合传递大量数据  
  不适合传递敏感信息（如密码），因为这些信息会暴露在 URL 中  
(2)格式 `URL?key1=value1&key2=value2`  
  `request.post("/admin/login?key=" + this.key, this.admin)`  
  `request.post("/admin/login?key=abc123", { username: "admin", password: "password" });`  
3. URL 路径参数（Path Parameters）  
(1)路径参数是嵌入在 URL 路径中的变量部分，通常用于 RESTful API 中  
  参数嵌入在 URL 的路径中  
  常用于指定资源的唯一标识符（如 ID、用户名等）  
  参数数量较少，通常用于单个资源的标识，不适合传递复杂数据  
(2)格式 `/resource/{id}`，其中 `{id}` 是路径参数  
  `request.delete("/admin/" + id)`  
  `request.delete("/admin/123");`  
##### [5]当一个页面加载时，如何在另一个页面显示相关信息
##### [6]overflow: auto;不起作用的原因（主内容区）  
1. 确保父容器的高度是固定的  
overflow: auto; 只有在容器的高度被明确限制时才会生效。  
如果父容器的高度是动态的或未被明确设置，.main-content 的高度可能无法正确计算，从而导致滚动条不显示。  
##### [7]window.scrollY始终为0的原因（悬浮按钮）  
1. 检查滚动是否被限制在某个元素内  
如果页面的滚动行为被限制在某个特定的元素内（例如，一个具有 overflow: auto 的容器），而不是整个 window，那么 window.scrollY 将始终为 0，因为 window 本身并没有滚动。  
##### [8]flex 属性的过渡问题  


#### Vue+SpringBoot前后端分离项目 （三）代码小结  
#### 20250416 (3-1)1.页面  
1. 实现内容  
(1)全局配置Vue核心库、router路由对象、.css样式文件、UI组件库  
(1)配置并渲染页面入口App.vue  
(1)增加跳转链接  
2. 前端配置 main.js  
vue/src/main.js  
(1)引入对象  
  导入 Vue.js 核心库`import Vue from 'vue'`  
  导入根组件 App.vue`import App from './App.vue'`  
  导入路由配置模块`import router from './router'`  
  导入全局样式文件`import '@/assets/global.css'`//(new)  
  导入 Element UI 组件库`import ElementUI from 'element-ui';`//(new)  
  导入 Element UI 的默认主题样式文件`import 'element-ui/lib/theme-chalk/index.css';`//(new)  
(2)全局配置  
  全局注册 Element UI 组件库，设置默认的组件大小`Vue.use(ElementUI, { size: "small" });`//(new)  
  关闭 Vue 的生产环境提示`Vue.config.productionTip = false`  
(3)创建实例  
  创建 Vue 实例`new Vue({})`  
  将路由配置传递给 Vue 实例`router`  
  将根组件 App 渲染到页面上`render: h => h(App)`  
  挂载到页面 #app 元素上`.$mount('#app')`  
3. 前端创建 App.vue  
vue/src/views/App.vue  
4. 前端组件 App.vue  
vue/src/views/App.vue  
(1)引入 导航语义标签`<nav></nav>`  
(2)引入 单页导航标签`<router-link></router-link>`  
(3)引入 `<router-view/>`  
5. 前端数据 App.vue  
vue/src/views/App.vue  
(1)绑定数据  
  `id="app"`  
  `to="/"`，单页导航路径-到首页  
  `to="/login"`，单页导航路径-到登录页  
  `to="/register"`，单页导航路径-到注册页  
#### 20250408 (3-1)2.封装  
1. 实现内容  
(1)前端封装请求消息、后端封装返回结果  
(2)前端request拦截器在请求发送之前，配置请求对象，如在请求头中设置token  
(3)前端response拦截器在响应成功之后，处理响应结果，把字符串类型数据转换为 JSON 对象  
(4)前端export导出封装的请求对象，供前端引用，向后端发送请求、处理响应结果  
(5)后端Params.java实体类接收前端请求传递数据=>  
(6)后端Controller=>Service=>Dao(Mapper)=>Entity=>数据库=>  
(7)后端Result.java封装响应结果、返回到前端，封装结果包含含状态、数据、消息字段  
2. 前端配置 request.js (前端封装)  
vue/src/utils/request.js  
(1)导入axios库`import axios from 'axios'`  
(2)创建axios实例`const request = axios.create({})`  
  1设置后台访问端口`baseURL: 'http://localhost:8080/api',`  
  2设置请求超时为 5000 毫秒（5 秒）`timeout: 5000`  
(3)request请求拦截器，配置请求对象`request.interceptors.request.use();`  
  1`config => {}` 在请求发送之前被调用  
    设置请求头中的 Content-Type 字段`config.headers['Content-Type']= 'application/json;charset=utf-8';`  
    返回配置对象`return config`  
  2`error => {}` 在请求发送过程中发生错误时被调用  
    捕获错误并返回一个拒绝的 Promise`return Promise.reject(error)`  
(4)response响应拦截器，res即为后端返回的Result结果`request.interceptors.response.use()`  
  1`response => {}` 对响应数据进行统一处理  
    获取后端返回数据`let res = response.data;`  
    判断变量是否为字符串类型`if (typeof res === 'string'){}`  
    如果为非空字符串，解析为 JSON 对象`res = res ? JSON.parse(res) : res`  
    返回结果`return res;`  
  2`error => {}` 响应失败时被调用  
    控制台打印错误信息`console.log('err' + error)`  
    捕获错误并返回一个拒绝的 Promise`return Promise.reject(error)`  
(5)导出封装的请求对象，供前端引用，向后端发送请求`export default request`  
3. 后端创建 Params.java (接收前端参数实体类)  
springboot/src/main/java/com/example/entity/Params.java  
(1)定义接收参数(参数名"params"对应前端data() {return {}}绑定数据)  
    private String content;
    private String username;
    private String name;
    private String phone;
    private String author;
    private Integer userId;
    private Integer PageNum;
    private Integer PageSize;  
(2)生成getter、setter方法  
4. 后端配置 Result.java (后端封装)  
springboot/src/main/java/com/example/common/Result.java  
(1)定义成员变量，生成getter、setter  
  返回状态`private String code;`  
  返回消息`private String msg;`  
  返回数据`private Object data;`  
(2)定义常量  
  响应成功状态码`private static final String SUCCESS = "0";`  
  响应失败状态码`private static final String ERROR = "-1";`  
(3)定义成功的静态方法(响应成功，返回状态)`public static Result success(){}`  
  创建封装对象`Result result = new Result();`  
  设置响应状态`result.setCode(SUCCESS);`  
  返回封装结果`return result;`  
(4)定义成功的静态方法(响应成功，返回状态和数据)`public static Result success(Object data){}`  
  创建封装对象`Result result = new Result();`  
  设置响应状态`result.setCode(SUCCESS);`  
  设置响应数据`result.setData(data);`  
  返回封装结果`return result;`  
(5)定义失败的静态方法(响应失败，返回状态和提示)`public static Result error(String msg){}`  
  创建封装对象`Result result = new Result();`  
  设置响应状态`result.setCode(ERROR);`  
  设置响应消息`result.setMsg(msg);`  
  返回封装结果`return result;`  
5. 后端创建 Entity.java (操作数据库实体类)  
springboot/src/main/java/com/example/entity/Admin.java  
(1)注解对应数据库表`@Table(name = "admin")`  
(2)注解对应数据库主键字段`@Id`自增`@GeneratedValue(strategy = GenerationType.IDENTITY)`  
    private Integer id;  
(3)注解对应数据库非主键字段`@Column(name = "column-name")`  
    private String name;
    private String password;
    private String sex;
    private Integer age;
    private String phone;
    private String role;  
(4)注解对应非数据库字段`@Transient`  
    private String token;
    private String verCode;  
(5)定义实体类参数，生成getter、setter方法  
5. 后端创建 Entity.java (操作数据库实体类)  
springboot/src/main/java/com/example/entity/Log.java  
(1)注解对应数据库表`@Table(name = "log")`  
(2)注解对应数据库主键字段`@Id`自增`@GeneratedValue(strategy = GenerationType.IDENTITY)`  
    private Integer id;  
(3)注解对应数据库非主键字段`@Column(name = "column-name")`  
    private String content;
    private String time;
    private String username;
    private String ip;  
(4)定义实体类参数，生成getter、setter方法  
#### 20250420 (3-1)3.登录(登录鉴权)  
1. 实现内容  
(1)登录步骤  
  输入登录用户名、密码，输入验证码  
  输入密码可控制显隐，验证码可点击刷新  
  点击登录按钮，输入错误则返回提示，输入正确则跳转到首页  
  点击注册链接，跳转到注册页面  
(1)鉴权规则  
  登录前、退出后，不允许访问指定页面  
  登录后，允许访问指定页面、指定模块  
(2)前端鉴权  
  未登录时，未存储登录信息；登录时存储用户信息、token；退出清空登录信息  
  路由守卫拦截页面跳转，从 localStorage 获取登录信息  
  获取失败，阻止访问目标路由；获取成功，允许访问目标路由  
(3)后端鉴权  
  通过用户名密码联合查询数据库，判断用户输入正误。  
  通过从请求头或请求参数中获取token，验证有效登录。  
(4)验证Token  
  获取Token，解析Token的载荷部分提取用户ID。  
  根据ID查询用户信息，使用用户密码作为密钥。  
  验证Token的签名、过期时间和其他字段。  
  如果Token验证通过，允许请求继续处理。  
(5)后端拦截  
  配置统一前缀，防止用户通过地址栏输入直接访问  
  配置拦截器，拦截仅登录可见页面  
  配置全局跨域资源共享  
2. 前端配置 index.js (前端鉴权)(不安全，还需后端鉴权)  
vue/src/router/index.js  
(1)路由守卫 (前端页面鉴权)  
  路由跳转前拦截处理`router.beforeEach((to ,from, next) =>{})`  
  从本地存储获取用户信息`const user = localStorage.getItem("user");`  
  获取失败且进入目标路由对象`if (!user && to.path !== '/login' && to.path !== '/register'){}`  
  判断未登录，重定向到登录页面`return next("/login");`  
  判断已登录，允许访问目标路由`else {next();}`  
(2)导出 VueRouter 实例`export default router`  
3. 前端配置 request.js (后端鉴权)(解析用户信息并设置token令牌)  
在vue/src/utils/request.js中写  
(1)导入axios库`import axios from 'axios'`  
(2)创建axios实例`const request = axios.create({})`  
  1设置后台访问端口`baseURL: 'http://localhost:8080/api',`  
  2设置请求超时为 5000 毫秒（5 秒）`timeout: 5000`  
(3)request请求拦截器，配置请求对象`request.interceptors.request.use();`  
  1`config => {}` 在请求发送之前被调用(后端页面鉴权)  
    设置请求头中的 Content-Type 字段`config.headers['Content-Type']= 'application/json;charset=utf-8';`  
    从浏览器的 localStorage 中获取用户信息`const user = localStorage.getItem("user");`  
    获取成功，解析用户信息并添加token到请求头`if (user) {config.headers['token']= JSON.parse(user).token;}`  
    返回配置对象`return config`  
  2`error => {}` 在请求发送过程中发生错误时被调用  
    捕获错误并返回一个拒绝的 Promise`return Promise.reject(error)`  
(4)response响应拦截器，res即为后端返回的Result结果`request.interceptors.response.use()`  
  1`response => {}` 对响应数据进行统一处理  
    获取后端返回数据`let res = response.data;`  
    判断变量是否为字符串类型`if (typeof res === 'string'){}`  
    如果为非空字符串，解析为 JSON 对象`res = res ? JSON.parse(res) : res`  
    返回结果`return res;`  
  2`error => {}` 响应失败时被调用  
    控制台打印错误信息`console.log('err' + error)`  
    捕获错误并返回一个拒绝的 Promise`return Promise.reject(error)`  
(5)导出封装的请求对象，供前端引用，向后端发送请求`export default request`  
4. 前端创建 LoginView.vue  
vue/src/views/LoginView.vue  
4. 前端创建 Layout.vue  
vue/src/views/Layout.vue  
5. 前端路由 index.js  
vue/src/router/index.js  
(1)import  
  `import LoginView from "@/views/LoginView.vue";`  
  `import Layout from '../views/Layout.vue'`  
(2)`const routes = []`  
  `{path: '/login',name: 'Login',component: LoginView},`  
  `{path: '/',name: 'Layout',component: Layout,children: []}`  
  `{path: '/',name: 'Layout',redirect: '/home',component: Layout,children: []}` 页面路径使用重定向  
(3)`children: []`  
  `{path: '',component: HomeView},`  
  `{path: 'admin',component: AdminView}`  
6. 前端组件 LoginView.vue  
vue/src/views/LoginView.vue  
(1)引入 Form 表单`<el-form></el-form>`  
(2)引入 Input 输入框`<el-input></el-input>`  
(3)引入 Button 按钮`<el-button></el-button>`  
(4)引入 img 图片标签`<img/>`  
(5)引入 a 超链接标签`<a></a>`  
6. 前端组件 Layout.vue  
vue/src/views/Layout.vue  
(1)引入 Container 布局容器`<el-container></el-container>`  
(2)引入 Container 顶栏容器`<el-header></el-header>`  
(3)引入 Container 侧栏容器`<el-aside></el-aside>`  
(4)引入 Container 主内容区`<el-main></el-main>`  
(5)引入 NavMenu 导航菜单`<el-menu></el-menu>`  
(6)引入 `<router-view/>`  
7. 前端数据 LoginView.vue  
vue/src/views/LoginView.vue  
(1)绑定样式`class="login-container"`，定义登录背景样式  
(2)绑定数据  
  `:model="admin"`，动态绑定表单输入信息  
  `v-model="admin.name"`，动态绑定输入的用户名  
  `v-model="admin.password"`动态绑定输入的用户密码  
  `show-password`控制密码显示  
  `v-model="admin.verCode"`动态绑定输入的验证码  
  `:src="captchaUrl"`，动态绑定图片地址  
  `href="javascript:void(0)"`，空链接  
(3)绑定事件  
  `@click="navRegister"`，超链接跳转注册页面方法  
  `@click="login()"`，登录方法  
  `@click="clickImg()"`，切换验证码方法  
7. 前端数据 Layout.vue  
vue/src/views/Layout.vue  
(1)绑定样式  
  `class="el-menu-vertical-demo"`，侧栏定义导航菜单样式，处理边界小瑕疵  
  `style="overflow: auto;height: 100vh"`，主内容区容器样式，设置为下拉滚动  
(2)绑定数据  
  `:default-active="$route.path"`，侧栏设置默认激活的菜单项，绑定为当前路由路径  
  `index="/"`，侧栏绑定页面路由-首页  
  `index="/admin"`，侧栏绑定路由-用户信息页面(管理员可见)  
  `{{ user.name }}`，顶栏绑定登录用户信息  
  `v-if="user.role === 'ROLE_ADMIN'"`，判断用户访问权限(仅管理员可见)  
(4)绑定事件`@click="logout"`，顶栏退出登录方法  
8. 前端逻辑 LoginView.vue  
vue/src/views/LoginView.vue  
(1)导入封装对象`import request from "@/utils/request";`  
(2)编写响应式数据`data() {return {}}`  
  1动态绑定表单输入信息`admin:{},`  
  2随机数`key:'',`  
  3动态绑定图片地址`captchaUrl: ''`  
(3)编写钩子函数`created() {}`  
  ` `  
(4)编写组件挂载后调用的钩子函数`mounted() {}`  
  1初始化随机数`this.key = Math.random();`  
  2初始化验证码(请求captcha接口并传参)`this.captchaUrl = 'http://localhost:8080/api/captcha?key=' + this.key;`  
(5)编写事件方法`methods: {navRegister() {}}`  
  跳转到注册页面`this.$router.push("/register")`  
(5)编写事件方法`methods: {clickImg() {}}`  
  刷新随机数`this.key = Math.random();`  
  刷新验证码`this.captchaUrl = 'http://localhost:8080/api/captcha?key=' + this.key;`  
(5)编写事件方法`methods: {login() {}}`  
  1发送POST请求、传递参数`request.post("/admin/login?key=" + this.key, this.admin)`  
  2响应成功，处理响应`.then(res => {if (res.code === '0') {}})`  
    登录操作成功提示`this.$message({message: '操作成功',type: 'success'});`  
    在本地存储登录用户信息`localStorage.setItem("user", JSON.stringify(res.data));`  
    跳转到首页`this.$router.push("/");`  
  3响应失败，返回消息`else{}`  
    后端异常处理`this.$message.error(res.msg);`  
    刷新随机数`this.key = Math.random();`  
    刷新验证码`this.captchaUrl = 'http://localhost:8080/api/captcha?key=' + this.key;`  
    刷新输入框`this.admin.verCode = ''`  
8. 前端逻辑 Layout.vue (退出清空登录信息)  
vue/src/views/Layout.vue  
(1)导入封装对象`import request from "@/utils/request";`  
(2)编写响应式数据`data() {return {}}`  
  从本地存储获取用户数据`user: localStorage.getItem("user") ? JSON.parse(localStorage.getItem("user")) : {}`  
  (三元运算符：获取成功，转换Json数据格式为JavaScript对象，展示已登录用户；获取失败，清空信息)  
  (v-if="user.role === 'ROLE_ADMIN'"条件渲染：若用户权限为管理员，则允许访问指定内容)  
(3)编写钩子函数`created() {}`  
  渲染登陆用户具体名字`this.user = JSON.parse(localStorage.getItem('user'))`  
(4)编写事件方法`methods: {logout() {}}`  
  清空本地存储用户数据`localStorage.removeItem('user')`  
  跳转到登录页面`this.$router.push('/login')`  
9. 后端配置 pom.xml  
springboot/pom.xml  
(1)添加依赖  
  (验证码)easy-captcha  
  (jwt)java-jwt  
  (hutool)hutool-all  
(2)点击Maven按钮刷新加载依赖  
10. 后端创建 CaptureConfig.java (验证码-存储配置)  
springboot/src/main/java/com/example/common/CaptureConfig.java  
(1)注解标记Spring 管理的 Bean`@Component`  
(2)验证码存储配置类`public class CaptureConfig {}`  
  存储验证码(静态Map存储键值对)`public static Map<String, String> CAPTURE_MAP = new HashMap<>();`  
10. 后端创建 CaptureController.java (验证码-生成方式)  
springboot/src/main/java/com/example/controller/CaptureController.java  
(1)注解对应前端REQUEST请求`@RequestMapping("/captcha")`  
(2)生成验证码方法`public void captcha(@RequestParam String key, HttpServletRequest request, HttpServletResponse response) {}`  
  (@RequestParam用于将请求参数绑定到方法的参数上)  
  抛出异常`public void captcha(@RequestParam String key, HttpServletRequest request, HttpServletResponse response) throws Exception{}`  
(3)方式一：图形验证码  
  1验证码长宽、字符个数`SpecCaptcha captcha = new SpecCaptcha(135, 33, 5);`  
  2设置类型为数字、大写字母`captcha.setCharType(Captcha.TYPE_NUM_AND_UPPER);`  
  3转化为小写并存储`CaptureConfig.CAPTURE_MAP.put(key, captcha.text().toLowerCase());`  
  4将验证码图片输出到响应中`CaptchaUtil.out(captcha, request, response);`  
  (报错解决：使用JarEditor插件修改jar内配置文件)  
(4)方式二：算数验证码  
  1验证码长宽`ArithmeticCaptcha captcha = new ArithmeticCaptcha(135, 33);`  
  2设置运算的位数(默认是两位)`captcha.setLen(4);`  
  3返回生成的数学运算公式(字符串如 3+2=?)`captcha.getArithmeticString();`  
  4返回运算的结果`captcha.text();`  
  5转化为小写并存储`CaptureConfig.CAPTURE_MAP.put(key, captcha.text().toLowerCase());`  
  6将验证码图片输出到响应中`CaptchaUtil.out(captcha, request, response);`  
  (报错解决：使用JarEditor插件修改jar内配置文件)  
11. 后端创建 JwtTokenUtils.java (后端鉴权-Jwt拦截器，生成token、获取用户)  
springboot/src/main/java/com/example/common/JwtTokenUtils.java  
(1)注解标记Spring 管理的 Bean`@Component`  
(2)后端鉴权-Jwt拦截器，生成token、获取用户`public class JwtTokenUtils{}`  
(3)初始操作  
  1创建控制台打印对象`private static final Logger log = LoggerFactory.getLogger(JwtTokenUtils.class);`  
  2注解引入Service层，初始化为静态对象  
    创建静态Service对象`private static AdminService staticAdminService;`  
    注解引入Service层`@Resource` `private AdminService adminService;`  
    注解用于初始化操作`@PostConstruct`  
    初始化静态对象`public void setUserService() {staticAdminService = adminService;}`  
(4)以用户ID和密码生成token方法`public static String genToken(String adminId, String sign){}`  
  生成token并作为结果返回`return JWT.create()`  
  用户Id作为载荷`.withAudience(adminId)`  
  token过期时间设为2小时`.withExpiresAt(DateUtil.offsetHour(new Date(), 2))`  
  以 password 作为 token 的密钥`.sign(Algorithm.HMAC256(sign));`  
  (使用Algorithm.HMAC256算法加密password作为签证)  
(5)以解析token获取当前登录用户方法`public static Admin getCurrentUser(){}`  
  1创建空token`String token = null;`  
  2`try {}`包含可能会抛出异常的代码  
  步骤一：获取token  
    1创建request`HttpServletRequest request = ((ServletRequestAttributes) RequestContextHolder.getRequestAttributes()).getRequest();`  
    2从请求头获取token`token = request.getHeader("token");`  
    3用hutool工具判断请求头token是否为空或空白`if (StrUtil.isBlank(token)) {}`  
      请求头为空，从参数获取token`token = request.getParameter("token");`  
    4用hutool工具判断参数token是否为空或空白`if (StrUtil.isBlank(token)){}`  
      请求头和参数均为空，控制台打印提示`log.error("获取当前登录的token失败， token: {}", token);`  
      返回空(防报错)`return null;`  
  步骤二：解析token，以ID查询用户  
    5获取成功，解析token以获取用户ID`String adminId = JWT.decode(token).getAudience().get(0);`  
    6调用Service层以ID查询用户方法`staticAdminService.findById(Integer.valueOf(adminId));`  
    7作为结果返回`return staticAdminService.findById(Integer.valueOf(adminId));`  
    8快捷键生成Service层以ID查询用户方法`public Admin findById(Integer id){}`  
  3`catch (Exception e) {}`捕获并处理 try 块中抛出的异常  
    9控制台打印提示、报错日志`log.error("获取当前登录的管理员信息失败, token={}", token,  e);`  
    10返回空(防报错)`return null;`  
11. 后端创建 JwtInterceptor.java (后端鉴权-Jwt拦截器，验证token、抛出异常)  
springboot/src/main/java/com/example/common/JwtInterceptor.java  
(1)注解标记Spring 管理的 Bean`@Component`  
(2)创建控制台打印对象`private static final Logger log = LoggerFactory.getLogger(JwtTokenUtils.class);`  
(3)注解引入Service层`@Resource` `private AdminService adminService;`  
(4)注解标记重写方法`@Override`  
  重写接口方法`public boolean preHandle(HttpServletRequest request,HttpServletResponse response,Object handler) {}`  
(5)重写接口方法(步骤一：获取token)  
  1从请求头获取token`token = request.getHeader("token");`  
  2用hutool工具判断请求头token是否为空或空白`if (StrUtil.isBlank(token)) {}`  
    请求头为空，从参数获取token`token = request.getParameter("token");`  
  3用hutool工具判断参数token是否为空或空白`if (StrUtil.isBlank(token)){}`  
    请求头和参数均为空，抛出自定义异常`throw new CustomException("无token，请重新登录");`  
(5)重写接口方法(步骤二：解析token，以ID查询用户)  
  1创建对象`String userId;``Admin admin;`  
  2`try {}`包含可能会抛出异常的代码  
    解析token以获取用户ID`userId = JWT.decode(token).getAudience().get(0);`  
    调用Service层以ID查询用户方法`admin = adminService.findById(Integer.parseInt(userId));`  
  3`catch (Exception e) {}`捕获并处理 try 块中抛出的异常  
    创建字符串对象`String errMsg = "token验证失败，请重新登录";`  
    控制台打印提示、错误日志`log.error(errMsg + ", token=" + token, e);`  
    抛出自定义异常`throw new CustomException(errMsg);`  
  4以ID查询失败，抛出自定义异常  
    `if (admin == null) {}`  
    `throw new CustomException("用户不存在，请重新登录");`  
(5)重写接口方法(步骤三：获取用户输入密码，验证token)  
  1`try {}`包含可能会抛出异常的代码  
    以用户输入密码加密作为token密钥`JWTVerifier jwtVerifier = JWT.require(Algorithm.HMAC256(admin.getPassword())).build();`  
    验证token`jwtVerifier.verify(token);`  
  2`catch (JWTVerificationException e) {}`捕获并处理 try 块中抛出的异常  
    `throw new CustomException("token验证失败，请重新登录");`  
12. 后端创建 WebConfig.java (后端鉴权-统一前缀、拦截器配置)  
springboot/src/main/java/com/example/common/WebConfig.java  
(1)注解标记配置类`@Configuration`  
(2)实现父接口`implements WebMvcConfigurer`  
(3)注解标记重写方法`@Override`  
(4)重写接口方法`public void configurePathMatch(PathMatchConfigurer configurer){}`  
  配置统一前缀`configurer.addPathPrefix("/api", clazz -> clazz.isAnnotationPresent(RestController.class));`  
(5)重写接口方法`public void addInterceptors(InterceptorRegistry registry){}`  
  注解引入拦截器`@Resource` `private JwtInterceptor jwtInterceptor;`  
  新增拦截器`registry.addInterceptor(jwtInterceptor)`  
  拦截规则，拦截所有"/api"开头的`.addPathPatterns("/api/**")`  
  拦截规则，放行文件上传下载接口`.excludePathPatterns("/api/files/**")`  
  拦截规则，放行文件分类页的上传接口`.excludePathPatterns("/api/type/upload")`
  拦截规则，放行图形验证码`.excludePathPatterns("/api/captcha")`  
  拦截规则，放行登录页面`.excludePathPatterns("/api/admin/login")`  
  拦截规则，放行注册页面`.excludePathPatterns("/api/admin/register");`  
12. 后端创建 CorsConfig.java (后端鉴权-全局跨域配置)  
springboot/src/main/java/com/example/common/CorsConfig.java  
(1)注解标记配置类`@Configuration`  
(2)注解用于定义一个 Bean`@Bean`  
(3)处理跨域请求过滤器`public CorsFilter corsFilter() {}`  
  定义基于 URL 的 CORS 配置`UrlBasedCorsConfigurationSource source = new UrlBasedCorsConfigurationSource();`  
  定义具体的 CORS 配置`CorsConfiguration corsConfiguration = new CorsConfiguration();`  
  允许所有来源访问`corsConfiguration.addAllowedOrigin("*");`  
  允许所有请求头`corsConfiguration.addAllowedHeader("*");`  
  允许所有 HTTP 方法(GET、POST、PUT、DELETE 等)`corsConfiguration.addAllowedMethod("*");`  
  将 CORS 配置注册到指定的路径(对所有路径生效)`source.registerCorsConfiguration("/**", corsConfiguration);`  
  返回处理跨域请求 CorsFilter 实例`return new CorsFilter(source);`  
13. 后端创建 GlobalExceptionHandler.java (后端异常-全局异常捕获器)  
springboot/src/main/java/com/example/exception/GlobalExceptionHandler.java  
(1)注解标记全局异常捕获器`@ControllerAdvice(basePackages="com.example.controller")`  
(2)创建控制台打印对象`private static final Logger log = LoggerFactory.getLogger(JwtTokenUtils.class);`  
(2)注解用于定义异常处理方法(所有异常类型)`@ExceptionHandler(Exception.class)`  
  注解用于将返回值直接作为响应体返回`@ResponseBody`  
  异常处理方法(所有)`public Result error(HttpServletRequest request, Exception e){}`  
  控制台打印异常信息`log.error("异常信息：",e);`  
  发生系统异常，返回提示到前端`return Result.error("系统异常");`  
(3)注解用于定义异常处理方法(自定义异常)`@ExceptionHandler(CustomException.class)`  
  注解用于将返回值直接作为响应体返回`@ResponseBody`  
  异常处理法(自定义)`public Result customError(HttpServletRequest request, CustomException e){}`  
  发生自定义异常，返回提示到前端`return Result.error(e.getMsg());`  
13. 后端创建 CustomException.java (后端异常-自定义异常)  
springboot/src/main/java/com/example/exception/CustomException.java  
(1)继承自运行时异常类`extends RuntimeException`  
(2)定义成员变量，生成getter、setter方法  
  用于存储异常消息`private String msg;`
(3)定义构造方法`public CustomException(String msg){}`  
  接收参数并传递给成员变量`this.msg = msg;`  
14. 后端创建 Entity.java  
springboot/src/main/java/com/example/entity/Admin.java  
(1)注解对应数据库表`@Table(name = "admin")`  
(2)注解对应数据库主键字段`@Id`自增`@GeneratedValue(strategy = GenerationType.IDENTITY)`  
    private Integer id;  
(3)注解对应数据库非主键字段`@Column(name = "column-name")`  
    private String name;
    private String password;
    private String sex;
    private Integer age;
    private String phone;
    private String role;  
(4)注解对应非数据库字段`@Transient`  
    private String token;
    private String verCode;  
(5)定义实体类参数，生成getter、setter方法  
15. 后端创建 Controller.java  
springboot/src/main/java/com/example/controller/AdminController.java  
(1)注解对应前端POST请求`@PostMapping("/login")`  
(2)Controller层登录方法`public Result login(@RequestBody Admin admin, @RequestParam String key, HttpServletRequest request){}`  
  (@RequestBody对应前端data() {return {}}绑定数据，admin输入框请求体数据)  
  (@RequestParam用于将请求参数绑定到方法的参数上)  
(3)比较用户输入与Map存储的验证码  
  1如果输入错误`if (!admin.getVerCode().toLowerCase().equals(CaptureConfig.CAPTURE_MAP.get(key))){}`  
  2拒绝登录请求`CaptchaUtil.clear(request);`  
  3返回错误提示`return Result.error("验证码不正确");`  
(4)输入正确，调用Service层登录方法`Admin loginUser = adminService.login(admin);`  
(5)返回封装结果`return Result.success(loginUser);`  
(6)清除Map存储的验证码`CaptureConfig.CAPTURE_MAP.remove(key);`  
(7)快捷键生成Service层登录方法`public Admin login(Admin admin){}`  
16. 后端创建 Service.java  
springboot/src/main/java/com/example/service/AdminService.java  
(1)Service层登录方法`public Admin login(Admin admin){}`  
  1进行非空判断  
    用户名为空，异常处理  
    `if (admin.getName() == null || "".equals(admin.getName())){}`  
    `throw new CustomException("用户名不能为空");`  
    密码为空，异常处理  
    `if (admin.getPassword() == null || "".equals(admin.getPassword())){}`  
    `throw new CustomException("密码不能为空");`  
  2调用Dao层查询账户方法`Admin user = adminDao.findByNameAndPassword(admin.getName(), admin.getPassword());`  
    查询失败，异常处理  
    `if (user == null){}`  
    `throw new CustomException("用户名或密码输入错误");`  
    查询成功，生成token  
    `String token = JwtTokenUtils.genToken(user.getId().toString(), user.getPassword());`  
    `user.setToken(token);`  
  3返回查询结果`return user;`  
  4快捷键生成Dao层查询账户方法`Admin findByNameAndPassword(String name, String password);`  
(2)Service层以ID查询用户方法`public Admin findById(Integer id){}`  
  调用Dao层以ID查询用户方法`adminDao.selectByPrimaryKey(id);`  
  作为结果返回`return adminDao.selectByPrimaryKey(id);`  
  Dao层基于tk.mybatis依赖完成以ID查询用户操作  
17. 后端创建 Dao.java(Interface)  
springboot/src/main/java/com/example/dao/AdminDao.java(Interface)  
(1)继承Mapper泛型接口，并指定泛型参数为Admin实体类`extends Mapper<Admin>{}`  
(2)Dao层SQL注解`@Select("select * from admin where name =#{name} and password =#{password}")`  
(3)Dao层查询账户方法`Admin findByNameAndPassword(String name, String password);`  
(4)注解标记方法参数`Admin findByNameAndPassword(@Param("name")String name, @Param("password")String password);`  
  @Param("params")为方法的参数params指定了名称params。  
(5)Dao层基于注解查询数据库  
(6)Dao层基于tk.mybatis依赖完成以ID查询用户操作  
18. 业务逻辑  
(1)前端发送请求=>  
(2)后端接收前端参数Params.java=>  
(3)后端业务逻辑Controller=>Service=>Dao(Mapper)=>Entity=>数据库=>  
(4)后端封装返回结果Result.java=>  
(5)前端处理后端响应结果并渲染视图  
#### 20250420 (3-1)4.注册(默认身份)  
1. 实现内容  
(1)输入登录用户名、密码，选择用户身份  
(2)输入密码可控制显隐，注册身份不选择则默认为学生  
(3)点击注册按钮，输入错误则返回提示，输入正确则新增数据库用户信息并跳转到登录页  
(4)点击登录链接，跳转到登录页面  
2. 前端创建 RegisterView.vue  
vue/src/views/RegisterView.vue  
3. 前端路由 index.js  
vue/src/router/index.js  
(1)import  
  `import RegisterView from "@/views/RegisterView.vue";`  
(2)`const routes = []`  
  `{path: '/register',name: 'Register',component: RegisterView},`  
4. 前端组件 RegisterView.vue  
vue/src/views/RegisterView.vue  
(1)引入 Form 表单`<el-form></el-form>`  
(2)引入 Input 输入框`<el-input></el-input>`  
(3)引入 Button 按钮`<el-button></el-button>`  
(4)引入 Select 选择器`<el-select></el-select>`  
(5)引入 a 超链接标签`<a></a>`  
5. 前端数据 RegisterView.vue  
vue/src/views/RegisterView.vue  
(1)绑定样式`class="register-container"`，定义注册背景样式  
(2)绑定数据  
  `:model="admin"`，动态绑定表单输入信息  
  `v-model="admin.name"`，动态绑定输入的用户名  
  `v-model="admin.password"`动态绑定输入的用户密码  
  `show-password`控制密码显示  
  `v-model="admin.role"`动态绑定选择的用户类型(角色权限)  
  `value="ROLE_TEACHER"`，下拉选项关联数据库字段，教师角色  
  `value="ROLE_STUDENT"`，下拉选项关联数据库字段，学生角色  
  `href="javascript:void(0)"`，空链接  
(3)绑定事件  
  `@click="navLogin"`，超链接跳转登录页面方法  
  `@click="register()"`，注册方法  
6. 前端逻辑 RegisterView.vue  
vue/src/views/RegisterView.vue  
(1)导入封装对象`import request from "@/utils/request";`  
(2)编写响应式数据`data() {return {}}`  
  绑定表单输入信息`admin:{}`  
(3)编写钩子函数`created() {}`  
  ` `  
(4)编写事件方法`methods: {navLogin() {}}`  
  跳转到登录页面`this.$router.push("/login")`  
(5)编写事件方法`methods: {register() {}}`  
  1默认注册角色设为学生  
    如果手动选择教师角色，则注册权限为教师  
      `if(this.admin.role === 'ROLE_TEACHER'){}`
      `this.admin.role = 'ROLE_TEACHER'`
    如果未选择或手动选择非教师角色，则注册权限为学生  
      `else {this.admin.role = 'ROLE_STUDENT'}`
  1发送POST请求、传递参数`request.post("/admin/register", this.admin)`  
  2响应成功，处理响应`.then(res => {if (res.code === '0') {}})`  
    注册成功提示`this.$message({message: '注册成功',type: 'success'});`  
    跳转到登录页`this.$router.push("/login");`  
  3响应失败，返回消息`else{}`  
    后端异常处理`this.$message.error(res.msg);`  
7. 后端创建 Entity.java  
springboot/src/main/java/com/example/entity/Admin.java  
(1)注解对应数据库表`@Table(name = "admin")`  
(2)注解对应数据库主键字段`@Id`自增`@GeneratedValue(strategy = GenerationType.IDENTITY)`  
    private Integer id;  
(3)注解对应数据库非主键字段`@Column(name = "column-name")`  
    private String name;
    private String password;
    private String sex;
    private Integer age;
    private String phone;
    private String role;  
(4)注解对应非数据库字段`@Transient`  
    private String token;
    private String verCode;  
(5)定义实体类参数，生成getter、setter方法  
8. 后端创建 Controller.java  
springboot/src/main/java/com/example/controller/AdminController.java  
(1)注解对应前端POST请求`@PostMapping("/register")`  
(2)Controller层登录方法`public Result register(@RequestBody Admin admin){}`  
  (@RequestBody对应前端data() {return {}}绑定数据，admin输入框请求体数据)  
(3)调用Service层注册方法`adminService.add(admin);`  
(4)返回成功提示(防报错)`return Result.success();`  
(5)快捷键生成Service层注册方法`public void add(Admin admin){}`  
9. 后端创建 Service.java  
springboot/src/main/java/com/example/service/AdminService.java  
(1)Service层注册方法`public void add(Admin admin){}`  
(2)进行非空判断  
  1用户名为空，异常处理  
    `if (admin.getName() == null || "".equals(admin.getName())){}`  
    `throw new CustomException("用户名不能为空");`  
(3)调用Dao层以用户名查询用户方法`Admin user = adminDao.findByName(admin.getName());`  
  1查询成功，异常处理  
    `if (user != null){}`  
    `throw new CustomException("用户名已存在");`  
  2密码为空，初始化用户密码  
    `if (admin.getPassword() == null){}`  
    `admin.setPassword("123456");`  
  3快捷键生成Dao层以用户名查询用户方法`Admin findByName(String name);`  
  4Dao层基于注解以用户名查询数据库  
(4)调用Dao层注册(新增)方法`adminDao.insertSelective(admin);`  
(5)Dao层基于tk.mybatis依赖完成数据库注册(新增)操作  
10. 后端创建 Dao.java(Interface)  
springboot/src/main/java/com/example/dao/AdminDao.java(Interface)  
(1)继承Mapper泛型接口，并指定泛型参数为Admin实体类`extends Mapper<Admin>{}`  
(2)Dao层SQL注解`@Select("select * from admin where name = #{name} limit 1")`  
(3)Dao层以用户名查询用户方法`Admin findByName(String name);`  
  注解标记方法参数`Admin findByName(@Param("name")String name);`  
  @Param("params")为方法的参数params指定了名称params。  
(4)Dao层基于注解以用户名查询数据库  
(5)Dao层基于tk.mybatis依赖完成数据库的注册(新增)操作  
11. 业务逻辑  
(1)前端发送请求=>  
(2)后端接收前端参数Params.java=>  
(3)后端业务逻辑Controller=>Service=>Dao(Mapper)=>Entity=>数据库=>  
(4)后端封装返回结果Result.java=>  
(5)前端处理后端响应结果并渲染视图  
#### 20250424 (3-1)5.日志(面向切面)  
0. 数据库表 log.sql (操作日志表)  
主键ID：`id` int、不是null、键、自动递增  
操作内容：`content` varchar、255、utf8mb4、utf8mb4_unicode_ci  
操作时间：`time` varchar、255、utf8mb4、utf8mb4_unicode_ci  
操作人：`username` varchar、255、utf8mb4、utf8mb4_unicode_ci  
操作人IP：`ip` varchar、255、utf8mb4、utf8mb4_unicode_ci  
1. 实现内容  
(1)记录操作日志  
  自定义日志记录注解，使用环绕通知匹配带自定义注解的方法  
  从自定义注解信息中获取操作内容  
  使用hutool工具获取操作时间  
  使用jwt工具获取登录对象作为初始操作人  
  通过环绕通知拦截带自定义注解的方法获取返回的数据，进而获取当前日志的操作人  
  将操作内容、操作时间、操作人、ip封装为一条日志记录，保存到数据库  
(2)管理日志记录，增删查操作  
  输入操作内容、操作人  
  点击按钮进行条件查询、分页查询  
  点击按钮进行清空查询  
  点击按钮进行删除一条日志记录  
2. 前端创建 LogView.vue  
vue/src/views/LogView.vue  
3. 前端路由 index.js  
vue/src/router/index.js  
(1)import  
  `import Layout from '../views/Layout.vue'`  
  `import LogView from "@/views/LogView.vue";`  
(2)`const routes = []`  
  `{path: '/',name: 'Layout',component: Layout,children: []}`  
(3)`children: []`  
  `{path: '',component: HomeView},`  
  `{path: '/log',name: 'Log',component: LogView},`  
4. 前端组件 LogView.vue  
vue/src/views/LogView.vue  
(1)引入 Table 表格`<el-table></el-table>` 根据数据库表字段添加表格列  
(2)引入 Input 输入框`<el-input></el-input>`  
(3)引入 Button 按钮`<el-button></el-button>`  
(1)引入 Pagination 分页`<el-pagination></el-pagination>`  
(2)引入 Popconfirm 气泡确认框`<el-popconfirm></el-popconfirm>`  
5. 前端数据 LogView.vue  
vue/src/views/LogView.vue  
(1)绑定数据  
  `v-model="params.content"`，后端接收参数(操作内容)随输入内容动态更新  
  `v-model="params.username"`，后端接收参数(操作人)随输入内容动态更新  
(2)绑定数据  
  `:data="tableData"`，绑定表格数组数据，表格内容随后端查询动态更新  
  表格的"prop"属性对应数据库字段名，多个字段属性构成表格数组数据  
  `prop="content" label="操作内容"`  
  `prop="time" label="操作时间"`  
  `prop="username" label="操作人"`  
  `prop="ip" label="ip"`  
  `label="操作"`  
(3)绑定数据  
  `:current-page="params.pageNum"`，当前页码，随后端查询动态更新  
  `:page-sizes="[5, 10, 15, 20]"`，每页几条-下拉列表  
  `:page-size="params.pageSize"`，每页几条-默认选择  
  `:total="total"`，总共几条，根据条件查询结果动态更新  
  `layout=" total, sizes, prev, pager, next"` 为分页组件添加模块  
  表示 总共几条、每页几条、切换上页、页码列表、切换下页(共0条|0条/页|<|1 2 3 ...|>)  
(4)绑定数据  
  `slot-scope="scope"`，传递参数，指定表格一行的自定义信息  
  `slot="reference"`，指定触发弹出确认框的按钮(删除)  
(2)绑定事件  
  `@click="findBySearch()"`，点击按钮进行条件查询  
  `@click="reset()"`，点击按钮进行清空条件查询  
  `@size-change="handleSizeChange"`，点击切换每页几条-下拉列表  
  `@current-change="handleCurrentChange"`，点击切换当前页码  
  `@confirm="del(scope.row.id)"`，点击按钮进行删除一行信息  
6. 前端逻辑 LogView.vue  
vue/src/views/RegisterView.vue  
(1)导入封装对象`import request from "@/utils/request";`  
(2)编写响应式数据`data() {return {}}`  
  绑定表格内容`tableData: [],`  
  绑定表单输入、分页信息`params:{},`  
  绑定分页条目总数`total: 0,`  
(3)编写钩子函数`created() {}`  
  页面初始化查询`this.findBySearch();`  
(4)编写事件方法`methods: {findBySearch() {}}`  
  1发送GET请求、传递参数`request.get("/log/search",{params:this.params})`  
  2响应成功，处理响应`.then(res => {if (res.code === '0') {}})`  
    更新表格数据`this.tableData = res.data.list;`  
    更新分页条目总数`this.total = res.data.total;`  
  (由于进行了分页封装，前端接收后端查询数据有所变化)  
  3响应失败，返回消息`else{}`  
    后端异常处理`this.$message.error(res.msg);`  
(5)编写事件方法`methods: {reset() {}}`  
  1清空输入框的绑定数据`this.params = {content: '',username: ''}`  
  2重置分页数据`this.params = {pageNum: 1,pageSize: 5}`  
  3重新加载条件查询`this.findBySearch();`  
(6)编写事件方法`methods: {handleSizeChange(pageSize) {}}`  
  1更新每条页数`this.params.pageSize = pageSize;`  
  2重新加载条件查询`this.findBySearch();`  
(7)编写事件方法`methods: {handleCurrentChange(pageNum) {}}`  
  1更新当前页数`this.params.pageNum = pageNum;`  
  2重新加载条件查询`this.findBySearch();`  
(8)编写事件方法`methods: {del(id) {}}`  
  1发送DELETE请求、传递参数`request.delete("/log/" + id)`  
  2响应成功，处理响应`.then(res => {if (res.code === '0') {}})`  
    删除操作成功提示`this.$message({message: '操作成功',type: 'success'});`  
    重新加载查询`this.findBySearch();`  
  3响应失败，返回消息`else{}`  
    后端异常处理`this.$message.error(res.msg);`  
7. 后端配置 pom.xml  
springboot/pom.xml  
(1)添加依赖(aop)spring-boot-starter-aop  
(2)点击Maven按钮刷新加载依赖  
7. 后端创建 Params.java (接收前端参数实体类)  
springboot/src/main/java/com/example/entity/Params.java  
(1)定义接收参数(参数名"params"对应前端data() {return {}}绑定数据)  
  操作内容`private String content;`  
  操作用户`private String username;`  
(2)生成getter、setter方法  
8. 后端创建 AutoLog.java(Interface) (日志记录-自定义注解接口)  
(1)注解只能应用于方法上`@Target(ElementType.METHOD)`  
(2)注解在运行时仍然可用`@Retention(RetentionPolicy.RUNTIME)`  
(3)注解应该被包含在JavaDoc中`@Documented`  
  使用了@AutoLog方法会显示相关信息  
(4)自定义注解接口`public @interface AutoLog{}`  
  自定义注解value属性`String value() default "";`  
(5)使用方法`@AutoLog(value = "用户登录操作")`  
8. 后端创建 LogAspect.java (日志记录-面向切面编程类)  
(1)注解标记Spring 管理的 Bean`@Component`  
(2)注解标记切面类`@Aspect`  
  `public class LogAspect{}`  
(3)注解引入Service层`private LogService logService;`  
(4)注解用于定义环绕通知`@Around("@annotation(autoLog)")`  
  `@Around`环绕通知可以在目标方法执行之前和之后执行自定义逻辑  
  `@annotation`表示匹配带有某个注解的方法  
  `@annotation(autoLog)`表示匹配所有带有@AutoLog注解的方法  
(5)环绕通知方法  
  `public Object doAround(ProceedingJoinPoint joinPoint, AutoLog autoLog) throws Throwable{}`  
  `ProceedingJoinPoint joinPoint`：表示当前被拦截的方法的执行点，用于环绕通知。  
  `AutoLog autoLog`：表示匹配到的 @AutoLog 注解实例。通过这个参数可以访问注解的属性值，例如 autoLog.value()。  
  `throws Throwable`：表示该方法可能会抛出异常，需要对异常进行处理。  
(5)环绕通知方法(步骤一：初始化操作内容、操作时间、操作人)  
  1从@AutoLog注解中获取操作内容`String content = autoLog.value();`  
  2获取操作时间`String time = DateUtil.now();`  
  3定义操作人参数`String username = "";`  
    获取当前登录的用户对象`Admin user = JwtTokenUtils.getCurrentUser();`  
    如果用户不为空获取用户名，作为当前日志记录操作人  
      `if (ObjectUtil.isNotNull(user)) {}`  
      `username = user.getName();`  
(5)环绕通知方法(步骤二：获取ip、操作人)  
  1获取请求对象(强转)，通过请求对象获取ip地址  
    `HttpServletRequest request = ((ServletRequestAttributes) RequestContextHolder.getRequestAttributes()).getRequest();`  
    `String ip = request.getRemoteAddr();`  
  2继续执行环绕通知中被拦截的方法(强转)，获取返回数据  
    `Result result = (Result) joinPoint.proceed();`  
    `Object data = result.getData();`  
  3判断是否为Admin类型的实例，更新操作人(强转)  
    `if (data instanceof Admin){}`  
    `username = ((Admin) data).getName();`  
(5)环绕通知方法(步骤三：创建日志对象，保存日志记录到数据库)  
  1创建日志对象`Log log = new Log(null, content, time, username, ip);`  
  2调用Service层保存日志记录`logService.add(log);`  
7. 后端创建 Entity.java  
springboot/src/main/java/com/example/entity/Log.java  
(1)注解对应数据库表`@Table(name = "log")`  
(2)注解对应数据库主键字段`@Id`自增`@GeneratedValue(strategy = GenerationType.IDENTITY)`  
    private Integer id;  
(3)注解对应数据库非主键字段`@Column(name = "column-name")`  
    private String content;
    private String time;
    private String username;
    private String ip;  
(4)定义实体类参数，生成getter、setter方法  
8. 后端创建 Controller.java  
springboot/src/main/java/com/example/controller/LogController.java  
(1)注解对应前端GET请求`@GetMapping("/search")`  
  Controller层分页查询方法`public Result findBySearch(Params params){}`  
  (参数名"params"对应前端data() {return {}}绑定数据)  
  调用Service层分页查询方法`PageInfo<Log> info = logService.findBySearch(params);`  
  返回封装结果`return Result.success(info);`  
  快捷键生成Service层分页查询方法`public PageInfo<Log> findBySearch(Params params){}`  
(2)注解对应前端DELETE请求`@DeleteMapping("/{id}")`  
  Controller层删除方法`public Result delete(@PathVariable Integer id){}`  
  (@PathVariable用于将 URL 中的路径变量绑定到方法参数上)  
  调用Service层删除方法`logService.delete(id);`  
  返回成功提示(防报错)`return Result.success();`  
  快捷键生成Service层删除方法`public void delete(Integer id){}`  
9. 后端创建 Service.java  
springboot/src/main/java/com/example/service/LogService.java  
(1)Service层分页查询方法`public PageInfo<Log> findBySearch(Params params){}`  
  传递参数(当前页码、每页几条)开启分页查询`PageHelper.startPage(params.getPageNum(), params.getPageSize());`  
  调用Dao层条件查询方法`logDao.findBySearch(params);`  
  快捷键生成Dao层查询结果`List<Log> list = logDao.findBySearch(params);`  
  将查询结果进行分页封装，作为结果返回`return PageInfo.of(list);`  
  快捷键生成Dao层条件查询方法`List<Log> findBySearch(Params params);`  
  Dao层基于映射查询数据库  
(2)Service层删除方法`public void delete(Integer id){}`  
  调用Dao层删除方法`logDao.deleteByPrimaryKey(id);`  
  Dao层基于tk.mybatis依赖完成数据库删除操作  
(3)Service层新增方法`public void add(Log log){}`  
  调用Dao层新增方法`logDao.insertSelective(log);`  
  Dao层基于tk.mybatis依赖完成数据库新增操作  
10. 后端创建 Dao.java(Interface)  
springboot/src/main/java/com/example/service/LogDao.java(Interface)  
(1)继承Mapper泛型接口，并指定泛型参数为Admin实体类`extends Mapper<Log>{}`  
  Dao层条件查询方法`List<Log> findBySearch(Params params);`  
  注解标记方法参数`List<Log> findBySearch(@Param("params")Params params);`  
  @Param("params")为findBySearch方法的参数params指定了名称params。  
  Dao层基于映射查询数据库  
(2)Dao层基于tk.mybatis依赖完成数据库删除操作  
(3)Dao层基于tk.mybatis依赖完成数据库的新增操作  
12. 后端创建 Mapper.xml (Dao层映射)  
springboot/src/main/resources/mapper/LogMapper.xml  
(1)`<mapper></mapper>`标签。定义映射的命名空间  
  对应Dao层全限定名`namespace="com.example.dao.LogDao"`  
(2)`<select></select>`标签。定义查询结果映射实体类  
  查询方法唯一标识对应Dao层方法名`id="findBySearch"`  
  对应实体类全限定名`resultType="com.example.entity.Log`  
  编写SQL语句`select * from log`  
(3)`<where></where>`标签。根据条件动态生成 WHERE 子句  
  编写SQL语句`role != 'ROLE_ADMIN'`  
(4)`<if></if>`标签。根据条件动态生成 SQL 片段  
  条件表达式  
  test 属性是一个布尔表达式，如果表达式的结果为 true，则会将 `<if>` 标签内的 SQL 片段添加到最终的 SQL 语句中  
  确保传入的参数对象不为 null、字段不为 null、字段不为空字符串  
  `test="params != null and params.content != null and params.content != ''"`  
  `test="params != null and params.username != null and params.username != ''"`  
  SQL片段  
  模糊查询(%通配符：查询包含字段的所有记录)  
  `and content like concat('%', #{params.content}, '%')`  
  `and username like concat('%', #{params.username}, '%')`  
(5)Dao层基于映射查询数据库  
13. 业务逻辑  
(1)前端发送请求=>  
(2)后端接收前端参数Params.java=>  
(3)后端业务逻辑Controller=>Service=>Dao(Mapper)=>Entity=>数据库=>  
(4)后端封装返回结果Result.java=>  
(5)前端处理后端响应结果并渲染视图  
#### 20250424 (3-1)6.公告  
#### 20250424 (3-1)6.图表echarts  
#### 20250424 (3-1)6.批量删除  
#### 20250424 (3-1)6.模块关联  
#### 20250424 (3-1)6.预约  
#### 20250424 (3-1)6.审核  
#### 20250424 (3-1)6.编辑wangeditor  
#### 20250424 (3-1)6.文件上传下载  
#### 20250424 (3-1)6.协同文档  
#### 20250424 (3-1)6.导出excel  
#### 20250315 (3-2)1.查(查询全部)  
0. 数据库表 admin.sql (用户信息表)  
主键ID：`id` int、不是null、键、自动递增  
姓名：`name` varchar、255、utf8mb4、utf8mb4_unicode_ci  
密码：`password` varchar、255、utf8mb4、utf8mb4_unicode_ci  
性别：`sex` varchar、255、utf8mb4、utf8mb4_unicode_ci  
年龄：`age` int  
电话：`phone` varchar、255、utf8mb4、utf8mb4_unicode_ci  
角色：`role` Varchar、255、utf8mb4、utf8mb4_unicode_ci  
1. 实现内容  
(1)通过浏览器地址访问对应页面时  
(2)后端查询全部数据库返回给前端  
(3)前端在页面上展示全部用户信息  
2. 前端创建 AdminView.vue  
vue/src/views/AdminView.vue  
3. 前端路由 index.js  
vue/src/router/index.js  
(1)import  
  `import Layout from '../views/Layout.vue'`  
  `import AdminView from "@/views/AdminView.vue";`  
(2)`const routes = []`  
  `{path: '/',name: 'Layout',component: Layout,children: []}`  
(3)`children: []`  
  `{path: '',component: HomeView},`  
  `{path: '/admin',name: 'admin',component: AdminView},`  
4. 前端组件 AdminView.vue  
vue/src/views/AdminView.vue  
(1)引入 Table 表格`<el-table></el-table>` 根据数据库表字段添加表格列  
5. 前端数据 AdminView.vue  
vue/src/views/AdminView.vue  
(1)绑定数据  
  `:data="tableData"`，绑定表格数组数据，表格内容随后端查询动态更新  
  表格的"prop"属性对应数据库字段名，多个字段属性构成表格数组数据  
  `prop="name" label="姓名"`  
  `prop="sex" label="性别"`  
  `prop="age" label="年龄"`  
  `prop="phone" label="电话"`  
  `prop="role" label="角色"`  
  ` label="操作"`  
6. 前端逻辑 AdminView.vue  
vue/src/views/AdminView.vue  
(1)导入封装对象`import request from "@/utils/request";`  
(2)编写响应式数据`data() {return {}}`  
  绑定表格数组数据`tableData: []`  
(3)编写钩子函数`created() {}`  
  页面初始化查询`this.load();`  
(4)编写事件方法`methods: {load() {}}`  
  1发送GET请求`request.get("/admin")`  
  2响应成功，处理响应`.then(res => {if (res.code === '0') {}})`  
    传递赋值表格数据`this.tableData = res.data;`  
  3响应失败，返回消息`else{}`  
    后端异常处理-完整写法`this.$message({message: res.msg,type: 'error'});`  
    后端异常处理-简化写法`this.$message.error(res.msg);`  
7. 后端创建 Entity.java  
springboot/src/main/java/com/example/entity/Admin.java  
(1)注解对应数据库表`@Table(name = "admin")`  
(2)注解对应数据库主键字段`@Id`自增`@GeneratedValue(strategy = GenerationType.IDENTITY)`  
    private Integer id;  
(3)注解对应数据库非主键字段`@Column(name = "column-name")`  
    private String name;
    private String password;
    private String sex;
    private Integer age;
    private String phone;
    private String role;  
(4)注解对应非数据库字段`@Transient`  
    private String token;
    private String verCode;  
(5)定义实体类参数，生成getter、setter方法  
8. 后端创建 Controller.java  
springboot/src/main/java/com/example/controller/AdminController.java  
(1)注解对应前端GET请求`@GetMapping`  
(2)Controller层查询全部方法`public Result findAll(){}`  
(3)调用Service层查询全部方法`List<Admin> list = adminService.findAll();`  
(4)返回封装结果`return Result.success(list);`  
(5)快捷键生成Service层查询全部方法`public List<Admin> findAll(){}`  
9. 后端创建 Service.java [1]Dao层基于tk.mybatis依赖查询数据库  
springboot/src/main/java/com/example/service/AdminService.java  
(1)Service层查询全部方法`public List<Admin> findAll(){}`  
(2)调用Dao层查询全部方法`adminDao.selectAll();`  
(3)作为结果返回`return adminDao.selectAll();`  
(4)Dao层基于tk.mybatis依赖查询数据库  
9. 后端创建 Dao.java(Interface) [1]Dao层基于tk.mybatis依赖查询数据库  
springboot/src/main/java/com/example/dao/AdminDao.java(Interface)  
(1)继承Mapper泛型接口，并指定泛型参数为Admin实体类`extends Mapper<Admin>{}`  
(2)Dao层基于tk.mybatis依赖查询数据库  
10. 后端创建 Service.java [2]Dao层基于注解查询数据库  
springboot/src/main/java/com/example/service/AdminService.java
(1)Service层查询全部方法`public List<Admin> findAll(){}`  
(2)调用Dao层查询全部方法`adminDao.getAll();`  
(3)作为结果返回`return adminDao.getAll();`  
(4)快捷键生成Dao层查询全部方法`List<Admin> getAll();`  
(5)Dao层基于注解查询数据库  
10. 后端创建 Dao.java(Interface) [2]Dao层基于注解查询数据库  
springboot/src/main/java/com/example/dao/AdminDao.java(Interface)  
(1)继承Mapper泛型接口，并指定泛型参数为Admin实体类`extends Mapper<Admin>{}`  
(2)Dao层SQL注解`@Select("select * from admin")`  
(3)Dao层查询全部方法`List<Admin> getAll();`  
(4)Dao层基于注解查询数据库  
11. 后端创建 Dao.java(Interface) [3]Dao层基于映射查询数据库  
springboot/src/main/java/com/example/dao/AdminDao.java(Interface)  
(1)继承Mapper泛型接口，并指定泛型参数为Admin实体类`extends Mapper<Admin>{}`  
(2)Dao层查询全部方法`List<Admin> getAll();`  
(3)Dao层基于映射查询数据库  
11. 后端创建 Mapper.xml (Dao层映射) [3]Dao层基于映射查询数据库  
springboot/src/main/resources/mapper/AdminMapper.xml  
(1)`<mapper></mapper>`标签。定义映射的命名空间  
  对应Dao层全限定名`namespace="com.example.dao.AdminDao"`  
(2)`<select></select>`标签。定义查询结果映射实体类  
  查询方法唯一标识对应Dao层方法名`id="getAll"`  
  对应实体类全限定名`resultType="com.example.entity.Admin`  
  编写SQL语句`select * from admin`  
(3)Dao层基于映射查询数据库  
12. 业务逻辑  
(1)前端发送请求=>  
(2)后端接收前端参数Params.java=>  
(3)后端业务逻辑Controller=>Service=>Dao(Mapper)=>Entity=>数据库=>  
(4)后端封装返回结果Result.java=>  
(5)前端处理后端响应结果并渲染视图  
#### 20250404 (3-2)2.查(条件查询)  
1. 实现内容  
(1)在查询全部基础上完成条件查询  
(2)在页面输入框内输入查询条件(姓名、电话)  
(3)点击查询按钮，后端根据前端输入内容查询数据库  
(4)点击清空按钮，前端在页面上重新加载全部用户信息  
(5)前端在页面上展示条件查询结果  
2. 前端创建 AdminView.vue  
vue/src/views/AdminView.vue  
3. 前端组件 AdminView.vue  
vue/src/views/AdminView.vue  
(1)引入 Input 输入框`<el-input></el-input>`  
(2)引入 Button 按钮`<el-button></el-button>`  
4. 前端数据 AdminView.vue  
vue/src/views/AdminView.vue  
(1)绑定数据  
  `v-model="params.name"`，后端接收参数(姓名)随输入内容动态更新  
  `v-model="params.phone"`，后端接收参数(电话)随输入内容动态更新  
(2)绑定事件  
  `@click="findBySearch()"`，点击按钮进行条件查询  
  `@click="reset()"`，点击按钮清空条件查询  
5. 前端逻辑 AdminView.vue  
vue/src/views/AdminView.vue  
(1)导入封装对象`import request from "@/utils/request";`  
(2)编写响应式数据`data() {return {}}`  
  绑定输入框数据`params: {name: '',phone: ''}`  
(3)编写钩子函数`created() {}`  
  页面初始化查询`this.findBySearch();`  
(4)编写事件方法`methods: {findBySearch() {}}`  
  1发送GET请求、传递参数`request.get("/admin/search",{params:this.params})`  
  2响应成功，处理响应`.then(res => {if (res.code === '0') {}})`  
    传递赋值表格数据`this.tableData = res.data;`  
  3响应失败，返回消息`else{}`  
    后端异常处理`this.$message.error(res.msg);`  
(5)编写事件方法`methods: {reset() {}}`  
  1清空输入框绑定数据`this.params = {name: '',phone: ''}`  
  2重新加载条件查询`this.findBySearch();`  
6. 后端创建 Params.java (接收前端参数实体类)  
springboot/src/main/java/com/example/entity/Params.java  
(1)定义接收参数(参数名"params"对应前端data() {return {}}绑定数据)  
    private String name;
    private String phone;  
(2)生成getter、setter方法  
7. 后端创建 Entity.java  
springboot/src/main/java/com/example/entity/Admin.java  
(1)注解对应数据库表`@Table(name = "admin")`  
(2)注解对应数据库主键字段`@Id`自增`@GeneratedValue(strategy = GenerationType.IDENTITY)`  
    private Integer id;  
(3)注解对应数据库非主键字段`@Column(name = "column-name")`  
    private String name;
    private String password;
    private String sex;
    private Integer age;
    private String phone;
    private String role;  
(4)注解对应非数据库字段`@Transient`  
    private String token;
    private String verCode;  
(5)定义实体类参数，生成getter、setter方法  
8. 后端创建 Controller.java  
springboot/src/main/java/com/example/controller/AdminController.java  
(1)注解对应前端GET请求`@GetMapping("/search")`  
(2)Controller层条件查询方法`public Result findBySearch(Params params){}`  
  (参数名"params"对应前端data() {return {}}绑定数据)  
(3)调用Service层条件查询方法`List<Admin> list = adminService.findBySearch(params);`  
(4)返回封装结果`return Result.success(list);`  
(5)快捷键生成Service层条件查询方法`public List<Admin> findBySearch(Params params){}`  
9. 后端创建 Service.java  
springboot/src/main/java/com/example/service/AdminService.java  
(1)Service层条件查询方法`public List<Admin> findBySearch(Params params){}`  
(2)调用Dao层条件查询方法`adminDao.findBySearch(params);`  
(4)作为结果返回`return adminDao.findBySearch(params);`  
(3)快捷键生成Dao层条件查询方法`List<Admin> findBySearch(Params params);`  
(4)Dao层基于映射查询数据库  
10. 后端创建 Dao.java(Interface)  
springboot/src/main/java/com/example/dao/AdminDao.java(Interface)  
(1)继承Mapper泛型接口，并指定泛型参数为Admin实体类`extends Mapper<Admin>{}`  
(2)Dao层条件查询方法`List<Admin> findBySearch(Params params);`  
  注解标记方法参数`List<Admin> findBySearch(@Param("params")Params params);`  
  @Param("params")为findBySearch方法的参数params指定了名称params。  
(3)Dao层基于映射查询数据库  
11. 后端创建 Mapper.xml (Dao层映射)  
springboot/src/main/resources/mapper/AdminMapper.xml  
(1)`<mapper></mapper>`标签。定义映射的命名空间  
  对应Dao层全限定名`namespace="com.example.dao.AdminDao"`  
(2)`<select></select>`标签。定义查询结果映射实体类  
  查询方法唯一标识对应Dao层方法名`id="findBySearch"`  
  对应实体类全限定名`resultType="com.example.entity.Admin`  
  编写SQL语句`select * from admin`  
(3)`<where></where>`标签。根据条件动态生成 WHERE 子句  
  编写SQL语句`role != 'ROLE_ADMIN'`  
(4)`<if></if>`标签。根据条件动态生成 SQL 片段  
  条件表达式  
  test 属性是一个布尔表达式，如果表达式的结果为 true，则会将 `<if>` 标签内的 SQL 片段添加到最终的 SQL 语句中  
  确保传入的参数对象不为 null、字段不为 null、字段不为空字符串  
  `test="params != null and params.name != null and params.name != ''"`  
  `test="params != null and params.phone != null and params.phone != ''"`  
  SQL片段  
  模糊查询(%通配符：查询包含字段的所有记录)  
  `and name like concat('%', #{params.name}, '%')`  
  `and phone like concat('%', #{params.phone}, '%')`  
(5)Dao层基于映射查询数据库  
12. 业务逻辑  
(1)前端发送请求=>  
(2)后端接收前端参数Params.java=>  
(3)后端业务逻辑Controller=>Service=>Dao(Mapper)=>Entity=>数据库=>  
(4)后端封装返回结果Result.java=>  
(5)前端处理后端响应结果并渲染视图  
#### 20250413 (3-2)3.查(分页查询)  
1. 实现内容  
(1)在条件查询基础上完成分页查询  
(2)在页面输入框内输入查询条件(姓名、电话)  
(3)点击查询按钮，后端根据前端输入内容查询数据库  
(4)点击清空按钮，前端在页面上重新加载全部用户信息  
(5)点击分页相关按键，切换每页几条、当前页码、上页、下页  
(6)前端在页面上按照分页要求展示条件查询结果  
2. 前端创建 AdminView.vue  
vue/src/views/AdminView.vue  
3. 前端组件 AdminView.vue  
vue/src/views/AdminView.vue  
(1)引入 Pagination 分页`<el-pagination></el-pagination>`  
4. 前端数据 AdminView.vue  
vue/src/views/AdminView.vue  
(1)绑定数据  
  `:current-page="params.pageNum"`，当前页码，随后端查询动态更新  
  `:page-sizes="[5, 10, 15, 20]"`，每页几条-下拉列表  
  `:page-size="params.pageSize"`，每页几条-默认选择  
  `:total="total"`，总共几条，根据条件查询结果动态更新  
  `layout=" total, sizes, prev, pager, next"` 为分页组件添加模块  
  表示 总共几条、每页几条、切换上页、页码列表、切换下页(共0条|0条/页|<|1 2 3 ...|>)  
(2)绑定事件  
  `@size-change="handleSizeChange"`，点击切换每页几条-下拉列表  
  `@current-change="handleCurrentChange"`，点击切换当前页码  
5. 前端逻辑 AdminView.vue  
vue/src/views/AdminView.vue  
(1)导入封装对象`import request from "@/utils/request";`  
(2)编写响应式数据`data() {return {}}`  
  `params: {pageNum: 1, pageSize: 5}`  
(3)编写钩子函数`created() {}`  
  页面初始化查询`this.findBySearch();`  
(4)编写事件方法`methods: {findBySearch() {}}`  
  1发送GET请求、传递参数`request.get("/admin/search",{params:this.params})`  
  2响应成功，处理响应`.then(res => {if (res.code === '0') {}})`  
    更新表格数据`this.tableData = res.data.list;`  
    更新分页条目总数`this.total = res.data.total;`  
  (由于进行了分页封装，前端接收后端查询数据有所变化)  
  3响应失败，返回消息`else{}`  
    后端异常处理`this.$message.error(res.msg);`  
(5)编写事件方法`methods: {handleSizeChange(pageSize) {}}`  
  1更新每条页数`this.params.pageSize = pageSize;`  
  2重新加载条件查询`this.findBySearch();`  
(6)编写事件方法`methods: {handleCurrentChange(pageNum) {}}`  
  1更新当前页数`this.params.pageNum = pageNum;`  
  2重新加载条件查询`this.findBySearch();`  
(7)编写事件方法`methods: {reset() {}}`  
  1清空输入框的绑定数据`this.params = {name: '',phone: ''}`  
  2重置分页数据`this.params = {pageNum: 1,pageSize: 5}`  
  3重新加载条件查询`this.findBySearch();`  
6. 后端配置 pom.xml  
springboot/pom.xml  
(1)添加依赖(分页)pagehelper-spring-boot-starter  
(2)点击Maven按钮刷新加载依赖  
7. 后端配置 application.yml  
springboot/src/main/resources/application.yml  
(1)添加分页配置`pagehelper:`  
(2)解决分页查询可能出现的循环依赖问题`spring: main: allow-circular-references: true`  
8. 后端创建 Params.java (接收前端参数实体类)  
springboot/src/main/java/com/example/entity/Params.java  
springboot/src/main/java/com/example/entity/Params.java  
(1)定义接收参数(参数名"params"对应前端data() {return {}}绑定数据)  
    private Integer PageNum;
    private Integer PageSize;  
(2)生成getter、setter方法  
9. 后端创建 Entity.java  
springboot/src/main/java/com/example/entity/Admin.java  
(1)注解对应数据库表`@Table(name = "admin")`  
(2)注解对应数据库主键字段`@Id`自增`@GeneratedValue(strategy = GenerationType.IDENTITY)`  
    private Integer id;  
(3)注解对应数据库非主键字段`@Column(name = "column-name")`  
    private String name;
    private String password;
    private String sex;
    private Integer age;
    private String phone;
    private String role;  
(4)注解对应非数据库字段`@Transient`  
    private String token;
    private String verCode;  
(5)定义实体类参数，生成getter、setter方法  
10. 后端创建 Controller.java  
springboot/src/main/java/com/example/controller/AdminController.java  
(1)注解对应前端GET请求`@GetMapping("/search")`  
(2)Controller层分页查询方法`public Result findBySearch(Params params){}`  
  (参数名"params"对应前端data() {return {}}绑定数据)  
(3)调用Service层分页查询方法`PageInfo<Admin> info = adminService.findBySearch(params);`  
(4)返回封装结果`return Result.success(info);`  
(5)快捷键生成Service层分页查询方法`public PageInfo<Admin> findBySearch(Params params){}`  
11. 后端创建 Service.java  
springboot/src/main/java/com/example/service/AdminService.java  
(1)Service层分页查询方法`public PageInfo<Admin> findBySearch(Params params){}`  
(2)传递参数(当前页码、每页几条)开启分页查询`PageHelper.startPage(params.getPageNum(), params.getPageSize());`  
(3)调用Dao层条件查询方法`adminDao.findBySearch(params);`  
(4)快捷键生成Dao层查询结果`List<Admin> list = adminDao.findBySearch(params);`  
(5)对查询结果进行分页封装，作为结果返回`return PageInfo.of(list);`  
(6)快捷键生成Dao层条件查询方法`List<Admin> findBySearch(Params params);`  
(7)Dao层基于映射查询数据库  
12. 后端创建 Dao.java(Interface) 内容同条件查询  
springboot/src/main/java/com/example/dao/AdminDao.java(Interface)  
(1)继承Mapper泛型接口，并指定泛型参数为Admin实体类`extends Mapper<Admin>{}`  
(2)Dao层条件查询方法`List<Admin> findBySearch(Params params);`  
  注解标记方法参数`List<Admin> findBySearch(@Param("params")Params params);`  
  @Param("params")为findBySearch方法的参数params指定了名称params。  
(3)Dao层基于映射查询数据库  
13. 后端创建 Mapper.xml(Dao层映射) 内容同条件查询  
springboot/src/main/resources/mapper/AdminMapper.xml  
(1)`<mapper></mapper>`标签。定义映射的命名空间  
  对应Dao层全限定名`namespace="com.example.dao.AdminDao"`  
(2)`<select></select>`标签。定义查询结果映射实体类  
  查询方法唯一标识对应Dao层方法名`id="findBySearch"`  
  对应实体类全限定名`resultType="com.example.entity.Admin`  
  编写SQL语句`select * from admin`  
(3)`<where></where>`标签。根据条件动态生成 WHERE 子句  
  编写SQL语句`role != 'ROLE_ADMIN'`  
(4)`<if></if>`标签。根据条件动态生成 SQL 片段  
  条件表达式  
  test 属性是一个布尔表达式，如果表达式的结果为 true，则会将 `<if>` 标签内的 SQL 片段添加到最终的 SQL 语句中  
  确保传入的参数对象不为 null、字段不为 null、字段不为空字符串  
  `test="params != null and params.name != null and params.name != ''"`  
  `test="params != null and params.phone != null and params.phone != ''"`  
  SQL片段  
  模糊查询(%通配符：查询包含字段的所有记录)  
  `and name like concat('%', #{params.name}, '%')`  
  `and phone like concat('%', #{params.phone}, '%')`  
(5)Dao层基于映射查询数据库  
14. 业务逻辑  
(1)前端发送请求=>  
(2)后端接收前端参数Params.java=>  
(3)后端业务逻辑Controller=>Service=>Dao(Mapper)=>Entity=>数据库=>  
(4)后端封装返回结果Result.java=>  
(5)前端处理后端响应结果并渲染视图  
#### 20250414 (3-2)4.增  
1. 实现内容  
(1)在条件查询基础上完成新增操作  
(2)点击新增按钮，弹出新增表单  
(3)点击取消按钮，隐藏新增表单  
(4)点击确定按钮，提交新增表单  
(5)后端根据前端请求，操作数据库表新增一条记录  
(6)前端在页面上重新加载新增后的用户信息  
2. 前端创建 AdminView.vue  
vue/src/views/AdminView.vue  
3. 前端组件 AdminView.vue  
vue/src/views/AdminView.vue  
(1)引入 Button 按钮`<el-button></el-button>`  
(2)引入 Dialog 对话框`<el-dialog></el-dialog>`  
(3)引入 Form 表单`<el-form></el-form>`  
(4)引入 Input 输入框`<el-input></el-input>`  
(5)引入 Radio 单选框`<el-radio></el-radio>`  
(6)引入 Select 选择器`<el-select></el-select>`  
4. 前端数据 AdminView.vue  
vue/src/views/AdminView.vue  
(1)绑定数据  
  `:visible.sync="dialogFormVisible"`，双向绑定控制对话框显隐  
(2)绑定数据  
  `:model="form"`，绑定表单数据，表单信息随后端查询动态更新  
  `v-model="form.name"`，双向绑定输入框内容，输入用户姓名  
  `v-model="form.sex`，双向绑定单选框内容，选择用户性别  
  `v-model="form.age"`，双向绑定输入框内容，输入用户年龄  
  `v-model="form.phone"`，双向绑定输入框内容，属于用户电话  
  `v-model="form.role"`，双向绑定下拉选项内容，选择用户角色  
(3)绑定数据  
  `value="ROLE_TEACHER"`，下拉选项关联数据库字段，教师角色  
  `value="ROLE_STUDENT"`，下拉选项关联数据库字段，学生角色  
(4)绑定事件  
  `@click="add()"`，点击按钮进行新增  
  `@click="dialogFormVisible = false"`，点击按钮取消新增  
  `@click="submit()"`，点击按钮确认提交新增  
5. 前端逻辑 AdminView.vue  
vue/src/views/AdminView.vue  
(1)导入封装对象`import request from "@/utils/request";`  
(2)编写响应式数据`data() {return {}}`  
  绑定对话框显隐、表单数据`params: {dialogFormVisible: false, form: {}}`  
(3)编写钩子函数`created() {}`  
  页面初始化查询`this.findBySearch();`  
(4)编写事件方法`methods: {add() {}}`  
  1清空表单数据`this.form = {};`  
  2打开新增对话框`this.dialogFormVisible = true;`  
(5)编写事件方法`methods: {submit() {}}`  
  1发送POST请求、传递参数`request.post("/admin", this.form)`  
  2响应成功，处理响应`.then(res => {if (res.code === '0') {}})`  
    新增操作成功提示`this.$message({message: '操作成功',type: 'success'});`  
    关闭对话框`this.dialogFormVisible = false;`  
    重新加载查询`this.findBySearch();`  
  3响应失败，返回消息`else{}`  
    后端异常处理`this.$message.error(res.msg);`  
6. 后端创建 Params.java (接收前端参数实体类)  
springboot/src/main/java/com/example/entity/Params.java  
springboot/src/main/java/com/example/entity/Params.java  
(1)定义接收参数(参数名"params"对应前端data() {return {}}绑定数据)  
    private Integer PageNum;
    private Integer PageSize;  
(2)生成getter、setter方法  
7. 后端创建 后端创建 Entity.java  
springboot/src/main/java/com/example/entity/Admin.java  
(1)注解对应数据库表`@Table(name = "admin")`  
(2)注解对应数据库主键字段`@Id`自增`@GeneratedValue(strategy = GenerationType.IDENTITY)`  
    private Integer id;  
(3)注解对应数据库非主键字段`@Column(name = "column-name")`  
    private String name;
    private String password;
    private String sex;
    private Integer age;
    private String phone;
    private String role;  
(4)注解对应非数据库字段`@Transient`  
    private String token;
    private String verCode;  
(5)定义实体类参数，生成getter、setter方法  
8. 后端创建 Controller.java  
springboot/src/main/java/com/example/controller/AdminController.java  
(1)注解定义控制器的根路径`@RequestMapping("/admin")`  
  `public class AdminController{}`  
(2)注解对应前端POST请求`@PostMapping`  
(3)Controller层新增方法`public Result save(@RequestBody Admin admin){}`  
  (@RequestBody对应前端data() {return {}}绑定数据，form表单请求体数据)  
(4)调用Service层新增方法`adminService.add(admin);`  
(5)返回成功提示(防报错)`return Result.success();`  
(6)快捷键生成Service层新增方法`public void add(Admin admin){}`  
9. 后端创建 Service.java  
springboot/src/main/java/com/example/service/AdminService.java  
(1)Service层新增方法`public void add(Admin admin){}`  
  判断有无密码，表单新增无密码则初始化密码  
  `if (admin.getPassword() == null){}`  
  `admin.setPassword("123456");`  
(2)调用Dao层新增方法`adminDao.insertSelective(admin);`  
(3)Dao层基于tk.mybatis依赖完成数据库新增操作  
10. 后端创建 Dao.java(Interface)  
springboot/src/main/java/com/example/dao/AdminDao.java(Interface)  
(1)继承Mapper泛型接口，并指定泛型参数为Admin实体类`extends Mapper<Admin>{}`  
(2)Dao层基于tk.mybatis依赖完成数据库的新增操作  
11. 业务逻辑  
(1)前端发送请求=>  
(2)后端接收前端参数Params.java=>  
(3)后端业务逻辑Controller=>Service=>Dao(Mapper)=>Entity=>数据库=>  
(4)后端封装返回结果Result.java=>  
(5)前端处理后端响应结果并渲染视图  
#### 20250415 (3-2)5.改  
1. 实现内容  
(1)在条件查询基础上完成编辑操作  
(2)点击编辑按钮，弹出表单  
(3)点击取消按钮，隐藏表单  
(4)点击确定按钮，提交编辑后的表单  
(5)后端根据前端请求，操作数据库表编辑一条记录  
(6)前端在页面上重新加载编辑后的用户信息  
2. 前端创建 AdminView.vue  
vue/src/views/AdminView.vue  
3. 前端组件 AdminView.vue  
vue/src/views/AdminView.vue  
(1)引入 Button 按钮`<el-button></el-button>`  
4. 前端数据 AdminView.vue  
vue/src/views/AdminView.vue  
(1)绑定数据  
  `:visible.sync="dialogFormVisible"`，双向绑定控制对话框显隐  
(1)绑定数据  
  `:model="form"`，绑定表单数据，表单信息随后端查询动态更新  
  `v-model="form.name"`，双向绑定输入框内容，输入用户姓名  
  `v-model="form.sex`，双向绑定单选框内容，选择用户性别  
  `v-model="form.age"`，双向绑定输入框内容，输入用户年龄  
  `v-model="form.phone"`，双向绑定输入框内容，属于用户电话  
  `v-model="form.role"`，双向绑定下拉选项内容，选择用户角色  
(1)绑定数据  
  `value="ROLE_TEACHER"`，下拉选项关联数据库字段，教师角色  
  `value="ROLE_STUDENT"`，下拉选项关联数据库字段，学生角色  
(1)绑定数据  
  `slot-scope="scope"`，传递参数，指定表格一行的自定义信息  
  `slot="reference"`，指定触发弹出确认框的按钮(编辑)  
(2)绑定事件  
  `@click="edit(scope.row)"`，点击按钮进行编辑一行信息  
  `@click="dialogFormVisible = false"`，点击按钮取消编辑  
  `@click="submit()"`，点击按钮进行确认提交  
5. 前端逻辑 AdminView.vue  
vue/src/views/AdminView.vue  
(1)导入封装对象`import request from "@/utils/request";`  
(2)编写响应式数据`data() {return {}}`  
  绑定对话框显隐、表单数据`params: {dialogFormVisible: false, form: {}}`  
(3)编写钩子函数`created() {}`  
  页面初始化查询`this.findBySearch();`  
(4)编写事件方法`methods: {edit(obj) {}}`  
  1传递表单数据`this.form = obj;`  
  2打开编辑对话框`this.dialogFormVisible = true;`  
(5)编写事件方法`methods: {submit() {}}`  
  1发送POST请求、传递参数`request.post("/admin", this.form)`  
  2响应成功，处理响应`.then(res => {if (res.code === '0') {}})`  
    新增操作成功提示`this.$message({message: '操作成功',type: 'success'});`  
    关闭对话框`this.dialogFormVisible = false;`  
    重新加载查询`this.findBySearch();`  
  3响应失败，返回消息`else{}`  
    后端异常处理`this.$message.error(res.msg);`  
6. 后端创建 Params.java (接收前端参数实体类)  
springboot/src/main/java/com/example/entity/Params.java  
springboot/src/main/java/com/example/entity/Params.java  
(1)定义接收参数(参数名"params"对应前端data() {return {}}绑定数据)  
    private Integer PageNum;
    private Integer PageSize;  
(2)生成getter、setter方法  
7. 后端创建 后端创建 Entity.java  
springboot/src/main/java/com/example/entity/Admin.java  
(1)注解对应数据库表`@Table(name = "admin")`  
(2)注解对应数据库主键字段`@Id`自增`@GeneratedValue(strategy = GenerationType.IDENTITY)`  
    private Integer id;  
(3)注解对应数据库非主键字段`@Column(name = "column-name")`  
    private String name;
    private String password;
    private String sex;
    private Integer age;
    private String phone;
    private String role;  
(4)注解对应非数据库字段`@Transient`  
    private String token;
    private String verCode;  
(5)定义实体类参数，生成getter、setter方法  
8. 后端创建 Controller.java  
springboot/src/main/java/com/example/controller/AdminController.java  
(1)注解定义控制器的根路径`@RequestMapping("/admin")`  
  `public class AdminController{}`  
(2)注解对应前端POST请求`@PostMapping`  
(3)Controller层编辑方法`public Result save(@RequestBody Admin admin){}`  
  (@RequestBody对应前端data() {return {}}绑定数据，form表单请求体数据)  
(4)通过获取ID判断编辑提交的信息是否已存在`if (admin.getId() == null){}`  
  未存在，调用Service层新增方法`adminService.add(admin);`  
  已存在，调用Service层更改方法`adminService.update(admin);`  
(5)返回成功提示(防报错)`return Result.success();`  
(6)快捷键生成Service层更改方法`public void update(Admin admin){}`  
9. 后端创建 Service.java  
springboot/src/main/java/com/example/service/AdminService.java  
(1)Service层更改方法`public void update(Admin admin){}`  
(2)调用Dao层更改方法`adminDao.updateByPrimaryKeySelective(admin);`  
(3)Dao层基于tk.mybatis依赖完成数据库更改操作  
10. 后端创建 Dao.java(Interface)  
springboot/src/main/java/com/example/dao/AdminDao.java(Interface)  
(1)继承Mapper泛型接口，并指定泛型参数为Admin实体类`extends Mapper<Admin>{}`  
(2)Dao层基于tk.mybatis依赖完成数据库更改操作  
11. 业务逻辑  
(1)前端发送请求=>  
(2)后端接收前端参数Params.java=>  
(3)后端业务逻辑Controller=>Service=>Dao(Mapper)=>Entity=>数据库=>  
(4)后端封装返回结果Result.java=>  
(5)前端处理后端响应结果并渲染视图  
#### 20250415 (3-2)6.删  
1. 实现内容  
(1)在条件查询基础上完成删除操作  
(2)点击删除按钮，弹出气泡确认框  
(3)点击取消按钮，隐藏气泡确认框  
(4)点击确定按钮，删除一条记录  
(5)后端根据前端请求操作数据库表，删除一条记录  
(6)前端在页面上重新加载删除后的用户信息  
2. 前端创建 AdminView.vue  
vue/src/views/AdminView.vue  
3. 前端组件 AdminView.vue  
vue/src/views/AdminView.vue  
(1)引入 Button 按钮`<el-button></el-button>`  
(2)引入 Popconfirm 气泡确认框`<el-popconfirm></el-popconfirm>`  
4. 前端数据 AdminView.vue  
vue/src/views/AdminView.vue  
(1)绑定数据  
  `slot-scope="scope"`，传递参数，指定表格一行的自定义信息  
  `slot="reference"`，指定触发弹出确认框的按钮(删除)  
(2)绑定事件`@confirm="del(scope.row.id)"`，点击按钮进行删除一行信息  
5. 前端逻辑 AdminView.vue  
vue/src/views/AdminView.vue  
(1)导入封装对象`import request from "@/utils/request";`  
(2)编写响应式数据`data() {return {}}`  
  ` `  
(3)编写钩子函数`created() {}`  
  页面初始化查询`this.findBySearch();`  
(4)编写事件方法`methods: {del(id) {}}`  
  1发送DELETE请求、传递参数`request.delete("/admin/" + id)`  
  2响应成功，处理响应`.then(res => {if (res.code === '0') {}})`  
    删除操作成功提示`this.$message({message: '操作成功',type: 'success'});`  
    重新加载查询`this.findBySearch();`  
  3响应失败，返回消息`else{}`  
    后端异常处理`this.$message.error(res.msg);`  
6. 后端创建 Params.java (接收前端参数实体类)  
springboot/src/main/java/com/example/entity/Params.java  
springboot/src/main/java/com/example/entity/Params.java  
(1)定义接收参数(参数名"params"对应前端data() {return {}}绑定数据)  
    private Integer PageNum;
    private Integer PageSize;  
(2)生成getter、setter方法  
7. 后端创建 后端创建 Entity.java  
springboot/src/main/java/com/example/entity/Admin.java  
(1)注解对应数据库表`@Table(name = "admin")`  
(2)注解对应数据库主键字段`@Id`自增`@GeneratedValue(strategy = GenerationType.IDENTITY)`  
    private Integer id;  
(3)注解对应数据库非主键字段`@Column(name = "column-name")`  
    private String name;
    private String password;
    private String sex;
    private Integer age;
    private String phone;
    private String role;  
(4)注解对应非数据库字段`@Transient`  
    private String token;
    private String verCode;  
(5)定义实体类参数，生成getter、setter方法  
8. 后端创建 Controller.java  
springboot/src/main/java/com/example/controller/AdminController.java  
(1)注解定义控制器的根路径`@RequestMapping("/admin")`  
  `public class AdminController{}`  
(2)注解对应前端DELETE请求`@DeleteMapping("/{id}")`  
(3)Controller层删除方法`public Result delete(@PathVariable Integer id){}`  
  (@PathVariable用于将 URL 中的路径变量绑定到方法参数上)  
(4)调用Service层删除方法`adminService.delete(id);`  
(5)返回成功提示(防报错)`return Result.success();`  
(6)快捷键生成Service层删除方法`public void delete(Integer id){}`  
9. 后端创建 Service.java  
springboot/src/main/java/com/example/service/AdminService.java  
(1)Service层删除方法`public void delete(Integer id){}`  
(2)调用Dao层删除方法`adminDao.deleteByPrimaryKey(id);`  
(3)Dao层基于tk.mybatis依赖完成数据库删除操作  
10. 后端创建 Dao.java(Interface)  
springboot/src/main/java/com/example/dao/AdminDao.java(Interface)  
(1)继承Mapper泛型接口，并指定泛型参数为Admin实体类`extends Mapper<Admin>{}`  
(2)Dao层基于tk.mybatis依赖完成数据库删除操作  
11. 业务逻辑  
(1)前端发送请求=>  
(2)后端接收前端参数Params.java=>  
(3)后端业务逻辑Controller=>Service=>Dao(Mapper)=>Entity=>数据库=>  
(4)后端封装返回结果Result.java=>  
(5)前端处理后端响应结果并渲染视图  


#### 20241208 毕设参考  
https://1x.antdv.com/components/upload-cn/  
vue-simple-uploaders视频上传  
视频播放插件：https://github.com/xdlumia/vue3-video-play  

kkFileView 万能预览  
OnlyOffice 文档在线协同  
使用集成的富文本编辑器如TinyMCE或Quill  
上传音视频TinyMCE、 Quill  

协同文档  
WebSocket与OT算法  
Yjs + Quill  
SpreadJS  
vue-quill-editor  
#### 20250315 毕设参考  
微博：https://weibo.com/  
csdn：https://www.csdn.net/  
知乎：https://www.zhihu.com/  
思否：https://segmentfault.com/  
掘金：https://juejin.cn/  
Discuz!社区动力：https://bbs.ishare1.cn/  
中研网：https://www.chinairn.com/yjbg/  
Boss：https://www.zhipin.com/chengshi/c101270500/?seoRefer=index  
腾讯文档：https://docs.qq.com/home  
飞书文档：https://jcnafceunr3k.feishu.cn/drive/home/  
语雀：https://www.yuque.com/dashboard  
Element在线讨论：https://app.gitter.im/  
永硕：http://eld901.ysepan.com/  
考试酷：https://www.examcoo.com/  
#### 20250315 毕设项目  
题目	融创富文本音视频集合的文档社区平台的设计与实现    
##### 一、登录注册  
登录入口  
注册入口  
##### 二、个人管理  
1.账户管理（对个人账户）  
账号设置 昵称、头像、说明  
权限设置 公开隐藏 主页、访客、关注、内容  
2.管理发布（对个人内容）  
内容类别 我的发布、我的收藏、我的关注  
内容板块 行业、兴趣、生活、地区、学校  
文件类型 文本、图片、音频、视频、其他文件  
查找方式 标题、内容、时间、文件类型  
自定义类 新增类别、修改类别、删除类别  
主要功能 新增、保存、预览、发布、修改、删除、上传、下载  
协同文档  
3.内容浏览  
内容板块 行业、兴趣、生活、地区、学校  
文件类型 文本、图片、音频、视频、其他文件  
查找方式 标题、内容、时间、文件类型  
用户互动 关注、收藏、点赞、评论、转发  
##### 三、后台管理  
1.账户管理（对所有账户）  
账号设置 昵称、头像、说明  
权限设置 公开隐藏 主页、访客、关注、内容  
2.管理发布（对所有内容）  
内容类别 我的发布、我的收藏、我的关注  
文件类型 文本、图片、音频、视频、其他文件  
查找方式 标题、内容、时间、文件类型  
自定义类 新增类别、修改类别、删除类别  
主要功能 新增、保存、预览、发布、修改、删除、上传、下载  
协同文档  
3.发布审核  
4.操作日志  
5.通知公告  
##### 四、协同文档  
##### 五、内容浏览  
内容板块 行业、兴趣、生活、地区、学校  
文件类型 文本、图片、音频、视频、其他文件  
查找方式 标题、内容、时间、文件类型  
用户互动 关注、收藏、点赞、评论、转发  
#### 20250315 毕设项目  
1、实现一个功能全面、用户友好的文档社区平台。  
2、提供前后端分离的架构，确保系统的高扩展性和维护性。  
3、支持富文本编辑、音视频播放等高级功能，满足用户对文档处理的多样化需求。  
4、实现本地文件的上传下载预览功能，方便用户管理个人文档。  
5、提供互动功能，增强用户间的交流与合作。  

设计并实现一个功能完备、界面友好的文档社区平台。  
系统支持用户登录注册、个人信息管理、文章创作与发布等功能。  
能够集成富文本编辑器，允许用户在创作文章时灵活插入图片、音频、视频等多媒体元素，并实现这些元素的在线预览与播放。  
实现文档的分类管理以及搜索功能，方便用户快速查找特定内容，提高信息检索效率。  
拥有合理的用户互动模块，如评论、点赞、分享等，增强用户之间的交流与互动，营造良好的社区氛围。  

