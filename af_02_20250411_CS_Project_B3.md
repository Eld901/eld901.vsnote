## F 笔记
### Project_B 本科毕业设计-毕设小结
#### 20250315 小结 ElementUI常用组件
##### Element官网
1. Container 布局容器：https://element.eleme.cn/#/zh-CN/component/container
2. Table 表格：https://element.eleme.cn/#/zh-CN/component/table
3. Input 输入框：https://element.eleme.cn/#/zh-CN/component/input
4. Button 按钮：https://element.eleme.cn/#/zh-CN/component/button
5. Pagination 分页：https://element.eleme.cn/#/zh-CN/component/pagination
##### [1]. Container 布局容器
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
##### [2]. Table 表格
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
##### [3]. Input 输入框
```js
<el-input v-model="input" placeholder="请输入内容"></el-input>
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
##### [4]. Button 按钮
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
##### [5]. Pagination 分页
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
##### [5]. Pagination 分页
#### 20250315 小结 MVNREPOSITORY常用依赖
0. MVNREPOSITORY：https://mvnrepository.com/
0. 复制依赖
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
			<groupId>org.apache.poi</groupId>
			<artifactId>poi-ooxml</artifactId>
			<version>4.1.2</version>
		</dependency>
		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-aop</artifactId>
		</dependency>
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
5. java-jwt
作用：用于生成和解析 JSON Web Tokens (JWT)。
功能：提供 JWT 的生成和解析功能，支持多种加密算法，常用于实现基于 JWT 的身份验证和授权机制。
6. hutool-all
作用：一个 Java 工具类库，提供丰富的工具类。
功能：提供字符串处理、日期时间处理、文件操作、网络请求等工具类，简化常见的 Java 开发任务。
7. poi-ooxml
作用：用于读写 Excel 文件（支持 .xls 和 .xlsx 格式）。
功能：提供读取和写入 Excel 文件的功能，支持复杂的 Excel 操作，常用于数据导入导出功能。
8. spring-boot-starter-aop
作用：提供 Spring AOP（面向切面编程）的支持。
功能：支持切面编程，用于实现日志记录、事务管理、权限校验等横切关注点，简化 AOP 的配置。
9. easy-captcha
作用：用于生成验证码。
功能：提供生成验证码的功能，支持多种验证码类型，常用于登录验证、注册验证等场景。
10. nashorn-core
作用：提供 Nashorn JavaScript 引擎的支持。
功能：提供 JavaScript 的解析和执行功能，支持在 Java 应用程序中运行 JavaScript 代码，适用于脚本执行、动态代码生成等场景。
#### 20250315 小结 Vue+SpringBoot前后端分离项目
#### 20250315 小结 （一）准备工作
##### [1].准备工作
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
#### 20250315 小结 （二）新建项目
##### [1].新建前端工程
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
##### [2].新建后端工程
1. 修改项目配置
JDK、Maven、数据库、pom.xml
2. 编写业务逻辑
Controller=>Service=>Dao(Mapper)=>Entity=>数据库
##### [3].新建数据库连接(Navicat)
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
3. 新建表
(1)运行SQL文件
(2)手动建表(名、类型、长度、小数点、不是null、虚拟、键、注释)
4. 导出.sql文件
右键表->转储SQL文件->结构和数据->(选择保存位置)
##### [4].新项目导入
1. 导入pom.xml
2. 修改配置文件
(1)修改application.yml
  修改port、username、password、url、mybatis等信息(端口号、数据库名、数据库密码)
(2)修改pom.xml
  选择正确的依赖(MVNRepository：https://mvnrepository.com/)
3. 修改项目配置
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
(5)配置Vue.js项目启动入口Add Configuration(顶栏入口)
  添加npm配置
  package.json:(`E:\eld901\Idea\vue\package.json`)
  Command:run
  Scripts:serve
  Arguments:(空)
  Node interpreter:Project node(`D:\appdownload\appd_node\node.exe`)
  Node options:(空)
  Package manager:Project(`D:\appdownload\appd_node\npm.cmd`)
  Environment:(空)
#### 20250408 小结 （三）项目文件
##### [1].前端项目 vue.config.js
vue/vue.config.js
```js
const { defineConfig } = require('@vue/cli-service')
module.exports = defineConfig({
  transpileDependencies: true
})
```
1. const { defineConfig } = require('@vue/cli-service')
作用：从 `@vue/cli-service` 包中导入 `defineConfig` 函数。
解释：
`@vue/cli-service` 是 Vue CLI 提供的工具包，用于支持 Vue CLI 项目的构建和开发。
`defineConfig` 是一个辅助函数，用于定义项目的配置。它可以帮助确保配置文件的结构符合 Vue CLI 的要求，并提供一些额外的功能（如类型检查）。
2. module.exports = defineConfig({...})
作用：将配置对象导出为模块，供 Vue CLI 使用。
解释：
`module.exports` 是 Node.js 中用于导出模块的语法。
`defineConfig({...})` 包装了一个配置对象，确保其结构符合 Vue CLI 的要求。
3. transpileDependencies: true
作用：配置是否对依赖项进行转译（transpile）。
解释：
默认情况下，Vue CLI 会忽略 `node_modules` 中的依赖项，不会对它们进行 Babel 转译。
设置 `transpileDependencies: true` 会强制对所有依赖项进行转译。这在某些情况下很有用，例如：
  依赖项中使用了较新的 JavaScript 特性，而目标环境不支持这些特性。
  依赖项需要在构建过程中进行特殊处理。
4. 总结
这段代码的作用是配置 Vue CLI 项目，确保所有依赖项在构建过程中被转译。这在某些情况下很有用，尤其是当依赖项使用了较新的 JavaScript 特性时。如果你的项目依赖项较多，建议只转译必要的依赖项，以避免不必要的构建开销。
##### [2].前端项目 main.js
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
1. import Vue from 'vue'
作用：从 vue 包中导入 Vue 构造函数。
解释：这是 Vue.js 的核心库，提供了 Vue 实例的构造函数和其他必要的功能。
2. import App from './App.vue'
作用：导入根组件 App.vue。
解释：App.vue 是 Vue 应用的根组件，定义了整个应用的布局和结构。
3. import router from './router'
作用：导入路由配置模块。
解释：./router 是路由配置文件（通常是 router/index.js），定义了应用的路由规则。
4. import '@/assets/global.css'
作用：导入全局样式文件 global.css。
解释：@ 是 Vue CLI 配置的别名，通常指向 src 目录。global.css 是全局样式文件，包含应用的通用样式。
5. import ElementUI from 'element-ui'
作用：导入 Element UI 组件库。
解释：Element UI 是一个基于 Vue.js 的 UI 组件库，提供了丰富的组件和样式。
6. import 'element-ui/lib/theme-chalk/index.css'
作用：导入 Element UI 的默认主题样式文件。
解释：theme-chalk 是 Element UI 的默认主题样式，确保 Element UI 的组件在页面上有正确的样式。
7. Vue.use(ElementUI, { size: "small" })
作用：全局注册 Element UI 组件库，并设置默认的组件大小为 small。
解释：
Vue.use 是 Vue.js 提供的插件安装方法，用于全局注册插件。
{ size: "small" } 是传递给 Element UI 的配置选项，设置组件的默认大小为 small。
8. Vue.config.productionTip = false
作用：关闭 Vue 的生产环境提示。
解释：在生产环境中，Vue 会显示一些提示信息，可以通过设置 productionTip 为 false 来关闭这些提示。
9. new Vue({...}).$mount('#app')
作用：创建一个新的 Vue 实例，并将其挂载到页面的 #app 元素上。
解释：
new Vue({...}) 创建一个新的 Vue 实例。
router：将路由配置传递给 Vue 实例。
render: h => h(App)：定义了 Vue 实例的渲染函数，将根组件 App 渲染到页面上。
.$mount('#app')：将 Vue 实例挂载到页面的 #app 元素上。
10. 执行流程
导入必要的模块和文件
  导入 Vue 构造函数。
  导入根组件 App.vue。
  导入路由配置模块。
  导入全局样式文件 global.css。
  导入 Element UI 组件库及其默认主题样式。
全局注册 Element UI
  使用 Vue.use 方法全局注册 Element UI 组件库，并设置默认的组件大小为 small。
关闭生产环境提示
  设置 Vue.config.productionTip 为 false，关闭 Vue 的生产环境提示。
创建并挂载 Vue 实例
  创建一个新的 Vue 实例。
  将路由配置传递给 Vue 实例。
  定义渲染函数，将根组件 App 渲染到页面上。
  将 Vue 实例挂载到页面的 #app 元素上。
11. 总结
这段代码是 Vue.js 项目的入口文件，负责初始化 Vue 应用并挂载到页面上。它导入了必要的模块和文件，全局注册了 Element UI 组件库，关闭了生产环境提示，并创建了一个 Vue 实例，将根组件 App 渲染到页面的 #app 元素上。
##### [3].前端项目 request.js
vue/src/utils/request.js
```js
import axios from 'axios'
const request = axios.create({
    baseURL: 'http://localhost:8080',
    timeout: 5000
})
request.interceptors.request.use(config => {
    config.headers['Content-Type'] = 'application/json;charset=utf-8';
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
1. import axios from 'axios'
作用：从 axios 包中导入 axios。
解释：axios 是一个基于 Promise 的 HTTP 客户端，用于浏览器和 node.js。
2. const request = axios.create({...})
作用：创建一个自定义的 axios 实例。
参数：
baseURL：所有请求的基准 URL，这里设置为 http://localhost:8080。
timeout：请求超时时间，这里设置为 5000 毫秒（5 秒）。
解释：通过 axios.create 创建的实例可以复用配置，方便统一管理请求的默认行为。
3. request.interceptors.request.use(...)
作用：添加请求拦截器。
解释：
请求拦截器在请求发送之前被调用，可以对请求配置进行修改或添加额外的逻辑。
这里设置请求头 Content-Type 为 application/json;charset=utf-8，确保发送的请求体是 JSON 格式。
如果请求配置对象 config 没有问题，返回 config 继续执行请求；如果有错误，返回一个拒绝的 Promise。
4. request.interceptors.response.use(...)
作用：添加响应拦截器。
解释：
响应拦截器在请求成功返回响应后被调用，可以对响应数据进行处理。
这里对响应数据 response.data 进行处理：
如果响应数据是字符串，尝试将其解析为 JSON 对象。
如果解析失败或数据为空，保持原样返回。
如果响应没有问题，返回处理后的响应数据；如果有错误，打印错误信息并返回一个拒绝的 Promise。
5. export default request
作用：将自定义的 axios 实例导出，供其他模块使用。
解释：通过 export default 将 request 实例导出，其他模块可以通过 import request from './utils/request' 来使用这个自定义的请求实例。
6. 总结
这段代码封装了一个基于 axios 的自定义请求实例，通过配置请求和响应拦截器，统一处理请求头和响应数据。这样可以简化代码，提高可维护性，并且方便统一管理请求的默认行为。
##### [4].前端项目 global.css
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
1. body 样式
margin: 0;
作用：移除 body 元素的默认外边距。
解释：默认情况下，浏览器会给 body 元素添加一定的外边距，这可能导致页面内容与浏览器窗口边缘有空隙。设置 margin: 0; 可以移除这个默认外边距，确保页面内容紧贴浏览器窗口边缘。
padding: 0;
作用：移除 body 元素的默认内边距。
解释：类似地，浏览器也可能给 body 元素添加默认的内边距。设置 padding: 0; 可以移除这个默认内边距，确保页面内容不会因为内边距而产生额外的空白区域。
overflow: hidden;
作用：隐藏 body 元素的滚动条，并防止内容溢出。
解释：设置 overflow: hidden; 会隐藏 body 元素的滚动条，确保页面内容不会超出浏览器窗口的可视区域。这在某些情况下很有用，例如在全屏应用或需要固定布局的页面中。
2. * 通用样式
box-sizing: border-box;
作用：设置所有元素的盒模型为 border-box。
解释：
默认情况下，HTML 元素的盒模型是 content-box，即宽度和高度只包括内容区域，不包括内边距（padding）和边框（border）。
设置 box-sizing: border-box; 后，宽度和高度会包括内容区域、内边距和边框，但不包括外边距（margin）。这使得布局更加直观和容易管理，因为你可以直接设置元素的宽度和高度，而不用担心内边距和边框会增加额外的空间。
3. 作用总结
这段代码的作用是：
移除 body 的默认外边距和内边距，确保页面内容紧贴浏览器窗口边缘。
隐藏 body 的滚动条，防止内容溢出，适用于全屏应用或固定布局的页面。
统一设置所有元素的盒模型为 border-box，使布局更加直观和容易管理。
4. 总结
这段代码是 Vue.js 项目中常见的全局样式文件，用于统一设置页面的基本样式，确保布局的一致性和可维护性。
##### [5].前端项目 App.vue
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
1. template 部分 这部分定义了组件的 HTML 结构。
`<nav>`：一个语义化的 HTML 元素，表示导航栏。
`<router-link>`：Vue Router 提供的组件，用于创建导航链接。它会被渲染为 `<a>` 标签，并且点击时会触发路由跳转，而不是传统的页面刷新。
to="/"：链接到根路径（通常是首页）。
to="/about"：链接到 /about 路径（通常是关于页面）。
`<div id="app">`：一个容器，用于包裹路由视图。
`<router-view>`：Vue Router 提供的组件，用于显示当前路由匹配的组件。根据当前的路由路径，`<router-view>` 会渲染对应的组件（如 HomeView 或 AboutView）。
2. style 部分 这部分定义了组件的样式。
在你的代码中，`<style>` 部分是空的，但你可以在这里添加全局样式或组件特定的样式。
3. script 部分 这部分定义了组件的逻辑。
lang="ts"：指定脚本语言为 TypeScript。
export default：导出一个默认对象，定义了组件的基本信息。
name: 'App'：组件的名称，通常用于调试和递归组件调用。
4. 执行流程
加载组件
当 Vue 应用启动时，App.vue 作为根组件被加载到页面的 #app 元素中。
渲染导航栏
`<nav>` 标签中的两个 `<router-link>` 会被渲染为导航链接，分别指向 / 和 /about 路径。
渲染路由视图
`<router-view>` 会根据当前的路由路径，渲染对应的组件。例如：
当路径为 / 时，`<router-view>` 会渲染 HomeView 组件。
当路径为 /about 时，`<router-view>` 会渲染 AboutView 组件。
样式应用
`<style>` 部分可以添加全局样式或组件特定的样式，但目前是空的。
5. 总结
App.vue 是 Vue 应用的根组件，负责渲染导航栏和路由视图。通过 <router-link> 创建导航链接，通过 <router-view> 渲染当前路由匹配的组件。你可以通过 <style> 部分添加样式来美化界面。
##### [6].前端项目 index.js
vue/src/router/index.js
```js
import Vue from 'vue'
import VueRouter from 'vue-router'
import HomeView from '../views/HomeView.vue'
Vue.use(VueRouter)
const routes = [
  {path: '/',name: 'home',component: HomeView},
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
  {path: '/',name: 'Layout',component: Layout,
    children: [
      {path: '',component: HomeView},
      {path: 'admin',component: AdminView}
    ]},
]
const router = new VueRouter({
  mode: 'history',
  base: process.env.BASE_URL,
  routes
})
export default router
```
1. import Vue from 'vue'
作用：从 vue 包中导入 Vue 构造函数。
解释：这是 Vue.js 的核心库，提供了 Vue 实例的构造函数和其他必要的功能。
2. import VueRouter from 'vue-router'
作用：从 vue-router 包中导入 VueRouter。
解释：vue-router 是 Vue.js 的官方路由管理器，用于管理页面的导航和组件的切换。
3. import HomeView from '../views/HomeView.vue'
作用：导入 HomeView 组件。
解释：HomeView.vue 是首页组件，定义了首页的布局和逻辑。
4. Vue.use(VueRouter)
作用：全局注册 vue-router 插件。
解释：通过 Vue.use 方法，将 vue-router 注册为 Vue 的全局插件，使其可以在整个应用中使用。
5. const routes = [...]
作用：定义路由规则。
解释：
routes 是一个数组，每个元素定义了一个路由规则。
每个路由规则是一个对象，包含以下属性：
path：路由路径。
name：路由名称，用于编程式导航。
component：路由对应的组件。
具体路由规则
  首页路由
  路径为 /，名称为 home，对应的组件是 HomeView。
  关于页面路由
  路径为 /about，名称为 about，对应的组件是 AboutView。
  使用了懒加载（import），只有在访问 /about 路径时才会加载 AboutView 组件，这可以提高应用的性能。
6. const router = new VueRouter({...})
作用：创建一个 VueRouter 实例。
参数：
mode：路由模式，这里设置为 history，表示使用历史模式。
base：应用的基路径，从环境变量 process.env.BASE_URL 获取。
routes：路由规则数组。
7. export default router
作用：将 VueRouter 实例导出，供其他模块使用。
解释：通过 export default，将 router 实例导出，其他模块可以通过 import router from './router' 来使用这个路由实例。
8. 总结
这段代码定义了 Vue.js 项目的路由规则，使用 vue-router 管理页面的导航和组件的切换。它包括：
全局注册 vue-router 插件。
定义路由规则，包括首页和关于页面。
使用懒加载优化性能。
创建并导出路由实例。
##### [7].前端项目 HomeView.vue
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
1. template 部分 这部分定义了组件的 HTML 结构。
`<div class="home">`：一个容器，用于包裹 HelloWorld 组件。
`<HelloWorld msg="Welcome to Your Vue.js APP"/>`：
HelloWorld 是一个自定义组件，通常用于显示欢迎信息。
msg 是一个属性（prop），将字符串 "Welcome to Your Vue.js APP" 传递给 HelloWorld 组件。
2. script 部分 这部分定义了组件的逻辑。
import HelloWorld from '@/components/HelloWorld.vue'：
  从 @/components/HelloWorld.vue 导入 HelloWorld 组件。
  @ 是 Vue CLI 配置的别名，通常指向 src 目录。
export default：
  导出一个默认对象，定义了组件的基本信息。
  name: 'HomeView'：组件的名称，通常用于调试和递归组件调用。
  components: { HelloWorld }：注册 HelloWorld 组件，使其可以在模板中使用。
3. 执行流程
加载组件
当路由路径为 / 时，HomeView 组件会被加载到 `<router-view>` 中。
渲染模板
`<div class="home">` 会被渲染到页面中。
`<HelloWorld msg="Welcome to Your Vue.js APP"/>` 会被渲染为 HelloWorld 组件，并将 msg 属性传递给它。
注册组件
在 `<script>` 部分，HelloWorld 组件被导入并注册到 HomeView 组件中，使其可以在模板中使用。
4. 注意事项
组件名称大小写
在 `<script>` 部分，组件名称是大小写敏感的。确保在 components 中注册的组件名称与导入的组件名称一致。
例如，components: { HelloWorld } 中的 HelloWorld 必须与 import HelloWorld 中的 HelloWorld 一致。
属性传递
在模板中，msg 属性被传递给 HelloWorld 组件。确保 HelloWorld 组件定义了对应的 props，否则属性不会生效。
5. 总结
HomeView.vue 是 Vue.js 项目的首页组件，它通过 `<router-view>` 被加载，并渲染了一个 HelloWorld 组件。你可以通过 `<style>` 部分添加样式来美化界面。
##### [8].前端项目 AboutView.vue
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
1. template 部分 这部分定义了组件的 HTML 结构。
`<div class="about">`：一个容器，用于包裹页面内容，添加了 about 类名，方便后续添加样式。
`<h1>This is an about page</h1>`：一个标题，显示“关于”页面的内容。
2. script 部分 这部分定义了组件的逻辑。
`name: 'AboutView'`：组件的名称，通常用于调试和递归组件调用。
3. 执行流程
加载组件
当路由路径为 /about 时，AboutView 组件会被加载到 `<router-view> `中。
渲染模板
`<div class="about">` 会被渲染到页面中。
`<h1>This is an about page</h1>` 会被渲染为标题。
应用样式
如果定义了 `<style>` 部分，页面内容会根据定义的样式进行渲染。
4. 注意事项
组件名称
确保在 `<script>` 部分定义了组件的名称，例如 name: 'AboutView'，这有助于调试和递归组件调用。
样式定义
如果需要美化页面，可以在 `<style>` 部分添加 CSS 样式。
路由配置
确保在路由配置文件中正确注册了 AboutView 组件，以便可以通过路由路径访问它。
5. 总结
AboutView.vue 是 Vue.js 项目的“关于”页面组件，它通过 `<router-view>` 被加载，并显示简单的页面内容。你可以通过 `<style>` 部分添加样式来美化界面。
##### [9].前端项目 HelloWorld.vue
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
1. template 部分 这部分定义了组件的 HTML 结构。
`<div class="hello">`：一个容器，用于包裹组件的内容，添加了 hello 类名，方便后续添加样式。
`<h1>{{ msg }}</h1>`：一个标题，显示传入的 msg 属性值。{{ msg }} 是 Vue.js 的插值语法，用于动态绑定数据。
2. script 部分 这部分定义了组件的逻辑。
name: 'HelloWorld'：
组件的名称，通常用于调试和递归组件调用。
在 Vue Devtools 中，组件名称会显示为 HelloWorld，便于开发者识别。
props: { msg: String }：
定义了一个名为 msg 的属性（prop），类型为 String。
props 是 Vue.js 中用于父子组件通信的机制，子组件可以通过 props 接收父组件传递的数据。
在父组件中，可以通过 :msg="someValue" 或 msg="someValue" 的方式将数据传递给 HelloWorld 组件。
3. 执行流程
加载组件
当 HelloWorld 组件被父组件（如 HomeView）使用时，它会被加载到页面中。
渲染模板
`<div class="hello">` 会被渲染到页面中。
`<h1>{{ msg }}</h1>` 会动态显示父组件传递的 msg 属性值。
应用样式
如果定义了 `<style>` 部分，页面内容会根据定义的样式进行渲染。
4. 注意事项
属性传递
确保在父组件中正确传递 msg 属性。例如：`<HelloWorld msg="Welcome to Your Vue.js APP"/>`
如果 msg 属性未传递，HelloWorld 组件中的 {{ msg }} 将显示为 undefined。
类型检查
在 props 中定义了 msg 的类型为 String，这有助于在开发过程中进行类型检查，避免传递错误类型的数据。
样式定义
如果需要美化页面，可以在 `<style>` 部分添加 CSS 样式。
5. 总结
HelloWorld.vue 是 Vue.js 项目中的一个简单组件，用于显示传入的消息。它通过 props 接收父组件传递的数据，并在模板中动态显示。你可以通过 `<style>` 部分添加样式来美化界面。
##### [10].前端项目 index.html
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
`<link rel="icon" href="<%= BASE_URL %>favicon.ico">`：设置页面的图标文件。<%= BASE_URL %> 是一个模板变量，由 html-webpack-plugin 替换为实际的基路径（通常是 / 或其他配置的路径）。
`<title><%= htmlWebpackPlugin.options.title %></title>`：设置页面的标题。<%= htmlWebpackPlugin.options.title %> 是一个模板变量，由 html-webpack-plugin 替换为实际的标题内容。
2. body 部分 这部分定义了页面的主体内容。
`<noscript>`：如果用户的浏览器禁用了 JavaScript，这段内容会被显示。<%= htmlWebpackPlugin.options.title %> 是一个模板变量，由 html-webpack-plugin 替换为实际的标题内容。
`<div id="app"></div>`：Vue 应用的挂载点。在 main.js 中，Vue 实例会被挂载到这个 div 元素上。
`<!-- built files will be auto injected -->`：这是一个注释，表示构建文件（如 bundle.js 和 bundle.css）将由 html-webpack-plugin 自动注入到页面中。
3. 模板变量
`<%= BASE_URL %>`：由 html-webpack-plugin 替换为实际的基路径。
`<%= htmlWebpackPlugin.options.title %>`：由 html-webpack-plugin 替换为实际的标题内容。
4. 执行流程
项目构建
当运行 npm run build 时，Vue CLI 会使用 html-webpack-plugin 处理 index.html 文件。
模板变量（如 <%= BASE_URL %> 和 <%= htmlWebpackPlugin.options.title %>）会被替换为实际的值。
构建文件（如 bundle.js 和 bundle.css）会被自动注入到 <body> 中。
页面加载
当用户访问页面时，浏览器会加载处理后的 index.html 文件。
如果用户的浏览器禁用了 JavaScript，会显示 <noscript> 中的内容。
Vue 应用会通过 main.js 被挂载到 <div id="app"></div> 中。
5. 总结
index.html 是 Vue.js 项目的 HTML 模板文件，用于定义页面的基本结构。它在项目构建时被 html-webpack-plugin 处理，模板变量会被替换为实际的值，构建文件会被自动注入到页面中。通过这个文件，你可以自定义页面的元数据、图标和标题等内容。
##### [11].后端项目 pom.xml
springboot/pom.xml
```xml
<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
	xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 https://maven.apache.org/xsd/maven-4.0.0.xsd">
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
xmlns：命名空间声明，确保 XML 文件遵循 Maven POM 的规范。
xsi:schemaLocation：指定 XML Schema 的位置，用于验证 POM 文件的结构。
2. 模型版本
modelVersion：指定 POM 文件的模型版本，通常是 4.0.0
3. 父项目依赖
parent：定义父项目依赖，这里使用了 Spring Boot 的父项目 spring-boot-starter-parent，版本为 3.3.7。
relativePath：指定父项目的相对路径，这里为空，表示从 Maven 仓库中查找。
4. 项目基本信息
groupId：项目的组 ID，通常是公司的域名反转，这里为 com.example。
artifactId：项目的 artifact ID，这里是 springboot1。
version：项目的版本号，这里是 0.0.1-SNAPSHOT，表示这是一个开发中的快照版本。
name：项目的名称，这里是 springboot。
description：项目的描述，这里是 springboot。
5. 项目配置
properties：定义项目的属性，这里指定了 Java 版本为 17。
6. 依赖管理
dependencies：定义项目的依赖项。
spring-boot-starter-web：包含 Spring MVC 和 Tomcat 的依赖，用于构建 Web 应用。
spring-boot-starter-test：包含测试相关的依赖，如 JUnit 和 Mockito，作用域为 test，仅在测试编译和执行阶段使用。
7. 构建配置
build：定义项目的构建配置。
plugins：定义使用的插件，这里使用了 spring-boot-maven-plugin，用于支持 Spring Boot 的构建和运行。
8. 总结
这个 pom.xml 文件是一个典型的 Spring Boot 项目的 Maven 配置文件，它定义了项目的依赖、属性和构建配置。通过这个文件，Maven 可以管理项目的依赖项、编译代码、运行测试和打包项目。
##### [12].后端项目 application.yml
springboot/src/main/resources/application.yml
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
1. 服务器配置
server.port：指定 Spring Boot 应用的服务器端口，默认为 8080 。
2. Spring 配置
数据源配置
spring.datasource.driver-class-name：指定数据库驱动类名，这里是 MySQL 的驱动类 com.mysql.cj.jdbc.Driver。
spring.datasource.username：数据库用户名，这里是 root。
spring.datasource.password：数据库密码，这里是 1234。
spring.datasource.url：数据库连接 URL，这里是连接到本地 MySQL 数据库的 URL，包含了一些连接参数：
useUnicode=true 和 characterEncoding=utf-8：确保支持 Unicode 和 UTF-8 编码。
allowMultiQueries=true：允许执行多条 SQL 语句。
useSSL=false：禁用 SSL 连接。
serverTimezone=GMT%2b8：设置服务器时区为 GMT+8。
allowPublicKeyRetrieval=true：允许公钥检索。
Spring 主配置
spring.main.allow-circular-references：允许循环引用，这在某些情况下可能会导致问题，但有时在复杂的项目中可能需要(分页查询)。
3. MyBatis 配置
mybatis.mapper-locations：指定 MyBatis 的映射文件位置，这里是 classpath:mapper/*.xml，表示在 src/main/resources/mapper 目录下查找所有 .xml 文件。
mybatis.type-aliases-package：指定 MyBatis 的类型别名包，这里是 com.example.entity，表示在 com.example.entity 包下查找实体类并为其生成别名。
4. PageHelper 配置
pagehelper.helper-dialect：指定 PageHelper 的方言，这里是 mysql，表示使用 MySQL 的分页方言。
pagehelper.reasonable：启用合理化分页，当分页参数不合理时，自动调整为合理值。
pagehelper.support-methods-arguments：支持通过方法参数传递分页参数。
pagehelper.params：自定义分页参数，这里是 count=countSql，表示分页参数的名称为 countSql。
5. 总结
这个 application.yml 文件定义了 Spring Boot 应用的服务器端口、数据源配置、MyBatis 配置和 PageHelper 配置。通过这些配置，你可以：
设置应用的服务器端口。
配置数据库连接信息。
指定 MyBatis 的映射文件位置和类型别名包。
配置 PageHelper 的分页功能。
##### [13].后端项目 SpringbootApplication.java
springboot/src/main/java/com/example/SpringbootApplication.java
```java
@SpringBootApplication
@MapperScan("com.example.dao")
public class SpringbootApplication {
	public static void main(String[] args) {
		SpringApplication.run(SpringbootApplication.class, args);
	}
}
```
1. @SpringBootApplication 注解
作用：这是一个组合注解，包含了以下三个注解：
@SpringBootConfiguration：标识当前类是一个 Spring Boot 的配置类。
@EnableAutoConfiguration：启用 Spring Boot 的自动配置机制，Spring Boot 会根据添加的依赖自动配置 Spring 和 Spring Boot。
@ComponentScan：启用组件扫描，扫描当前包及其子包中的注解（如 @Controller、@Service、@Repository、@Component 等），并将它们注册为 Spring 的 Bean。
2. @MapperScan 注解
作用：指定 MyBatis 的 Mapper 接口所在的包路径。
com.example.dao：表示 Spring Boot 会扫描 com.example.dao 包及其子包中的所有接口，并将它们注册为 MyBatis 的 Mapper Bean。
这样，你可以在 com.example.dao 包下定义所有的 Mapper 接口，而不需要在每个接口上手动添加 @Mapper 注解。
3. SpringbootApplication 类
public static void main(String[] args)：应用的入口方法。
SpringApplication.run(SpringbootApplication.class, args)：启动 Spring Boot 应用。
SpringbootApplication.class：指定当前类作为 Spring Boot 应用的主配置类。
args：传递给应用的命令行参数。
4. 执行流程
启动应用
当运行 main 方法时，SpringApplication.run(SpringbootApplication.class, args) 会启动 Spring Boot 应用。
Spring Boot 会加载 SpringbootApplication 类，并解析其上的注解。
自动配置
@SpringBootApplication：启用自动配置和组件扫描。
@EnableAutoConfiguration：根据添加的依赖自动配置 Spring 和 Spring Boot。
@ComponentScan：扫描当前包及其子包中的注解，并将它们注册为 Spring 的 Bean。
扫描 Mapper 接口
@MapperScan("com.example.dao")：扫描 com.example.dao 包及其子包中的所有接口，并将它们注册为 MyBatis 的 Mapper Bean。
5. 启动完成
应用启动完成，Spring Boot 的嵌入式服务器（如 Tomcat）开始监听指定的端口（默认为 8080），准备接收请求。
示例用法
当启动 SpringbootApplication 时，Spring Boot 会：
扫描 com.example 包及其子包，找到 HomeController、HomeService 和 HomeDao。
自动配置 Spring 和 Spring Boot。
启动嵌入式服务器，监听 8080 端口。
访问 http://localhost:8080/home 时，HomeController 会调用 HomeService，HomeService 会调用 HomeDao，最终返回数据库中的消息。
6. 总结
SpringbootApplication.java 是 Spring Boot 项目的主类文件，它定义了应用的入口点，并通过注解配置了自动配置和组件扫描。通过 @MapperScan 注解，它还指定了 MyBatis 的 Mapper 接口所在的包路径。
##### [14].后端项目 Controller.java
springboot/src/main/java/com/example/controller/AdminController.java
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
```
1. @RestController
表示这是一个控制器类，返回的数据通常是JSON或XML格式，而不是HTML页面。
2. @RequestMapping("/admin")
为该控制器类的所有方法定义了基础路径/admin，所有请求都会以/admin开头。
3. @Resource
使用`@Resource`注解注入了AdminService服务类，用于调用业务逻辑层的方法。
4. @GetMapping
表示该方法处理GET请求，路径为/admin（继承自类级别的@RequestMapping）。
5. findAll方法
(1)`adminService.findAll()`：调用AdminService中的findAll方法，获取所有管理员信息。
(2)`Result.success(list)`：将查询结果封装到Result对象中并返回。Result通常是一个自定义的通用返回类，用于统一返回格式。
##### [15].后端项目 Service.java
springboot/src/main/java/com/example/service/AdminService.java
```java
@Service
public class AdminService {
    @Resource
    private AdminDao adminDao;
    public List<Admin> findAll() {
        return adminDao.selectAll();
    }
    public PageInfo<Admin> findBySearch(Params params) {
        return adminDao.findBySearch(params);
    }
```
1. @Service
标注这是一个服务层组件，Spring会自动扫描并注册为一个Bean，便于在其他地方通过依赖注入使用。
2. @Resource
使用@Resource注解注入了AdminDao数据访问对象，用于与数据库交互。
3. findAll方法
调用AdminDao的selectAll方法，获取所有管理员信息。
返回一个`List<Admin>`集合，包含所有管理员对象。
4. findBySearch方法
调用AdminDao的findBySearch方法，根据传入的Params参数进行条件查询。
返回一个`PageInfo<Admin>`对象，包含分页信息和查询结果。
PageInfo是分页插件（如PageHelper）提供的类，用于封装分页数据。
##### [16].后端项目 Dao.java
springboot/src/main/java/com/example/dao/AdminDao.java(Interface)
```java
@Repository//[标记层]
public interface AdminDao extends Mapper<Admin> {
    @Select("select * from admin")
    List<Admin> getAll();
    List<Admin> findBySearch(@Param("params")Params params);
}
```
1. @Repository
标注这是一个数据访问层组件，Spring会自动扫描并注册为一个Bean，便于在其他地方通过依赖注入使用。
2. extends Mapper<Admin>
继承了MyBatis的Mapper接口，这使得AdminDao可以使用MyBatis提供的通用CRUD方法（如selectById、insert等）。
3. getAll方法
使用@Select注解定义了一个SQL查询，直接查询admin表的所有记录。
返回一个List<Admin>集合，包含所有管理员对象。
4. findBySearch方法
定义了一个方法，用于根据传入的Params参数进行条件查询。
使用@Param注解为params参数命名，以便在SQL语句中引用。
具体的SQL实现通常在MyBatis的Mapper XML文件中定义。
##### [17].后端项目 Mapper.xml
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
1. 这段代码是一个MyBatis的Mapper XML文件，用于定义与数据库交互的SQL语句。
2. XML声明
`<?xml version="1.0" encoding="UTF-8"?>`
这是XML文件的标准声明，指定了XML文件的版本和编码格式。这里声明了版本为1.0，编码格式为UTF-8。
3. DOCTYPE声明
这是文档类型声明（DOCTYPE），用于指定XML文件的文档类型定义（DTD）。
mapper是根元素的名称，表示这是一个MyBatis的Mapper文件。
PUBLIC "-//mybatis.org//DTD Mapper 3.0//EN"是公共标识符，用于标识MyBatis的Mapper DTD。
http://mybatis.org/dtd/mybatis-3-mapper.dtd是系统标识符，指向MyBatis的DTD文件。这个文件定义了Mapper XML文件的结构和约束。
4. Mapper根元素
`<mapper>`是根元素，表示这是一个MyBatis的Mapper文件。
namespace="com.example.dao.AdminDao"属性指定了Mapper的命名空间。这个命名空间通常与接口的全限定名一致，用于唯一标识这个Mapper文件。
在`<mapper>`标签内部，可以定义多个SQL映射语句（如`<select>`、`<insert>`、`<update>`、`<delete>`等）。
5. getAll 查询
这是一个简单的查询，返回admin表中的所有记录。
返回类型为com.example.entity.Admin，表示查询结果会被映射到Admin实体类。
6. findBySearch 查询
这是一个条件查询，根据params对象中的name和phone字段进行模糊匹配。
使用了MyBatis的动态SQL功能，<where>标签会自动处理条件的拼接，避免SQL语句中多余的AND或OR。
#{params.name}和#{params.phone}是参数占位符，MyBatis会自动将params对象中的对应字段值替换进去。
##### [18].后端项目 Entity.java
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
    //getter、setter
}
```
1. 这段代码是一个典型的Spring Boot实体类，映射到数据库中的admin表。
2. @Table(name = "admin")
指定该实体类映射到数据库中的admin表。
3. public class Admin：定义了一个名为Admin的Java类，表示管理员实体。
4. @Id
标识该字段为实体的主键
5. @GeneratedValue(strategy = GenerationType.IDENTITY)
指定主键生成策略为数据库自增（适用于MySQL、PostgreSQL等支持自增主键的数据库）
6. @Column(name = "name")
指定该字段映射到数据库表中的name列
7. 为每个字段生成getter和setter方法
##### [19].后端项目 Result.java
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
1. 这段代码是一个典型的Result类，用于封装API的返回结果。
2. 定义了两个常量SUCCESS和ERROR，分别表示成功和错误的状态码。这里使用字符串"0"表示成功，"-1"表示错误。
3. 字段定义
code：表示返回的状态码。
msg：表示返回的消息，通常用于描述成功或失败的原因。
data：表示返回的数据，可以是任意类型，例如列表、对象等。
4. success()：创建一个表示成功的Result对象，状态码为SUCCESS，不包含数据。
5. success(Object data)：创建一个表示成功的Result对象，状态码为SUCCESS，并包含指定的数据。
6. error(String msg)：创建一个表示失败的Result对象，状态码为ERROR，并包含错误消息。
7. 为每个字段生成getter和setter方法
##### [20].后端项目 Params.java
springboot/src/main/java/com/example/entity/Params.java
```java
public class Params {
    private String name;
    private String phone;
    //getter、setter
}
```
1. 这段代码是一个简单的Params类，用于封装前端查询参数。
2. 定义接收参数(参数名"params"对应前端data() {return {}}绑定数据)
姓名`private String name;`
电话`private String phone;`
3. 生成getter、setter方法
##### [21].后端项目 SpringBootApplicationTests.java
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
1. 这段代码是一个基本的Spring Boot测试类，用于验证Spring应用程序上下文是否能够正确加载。
2. 包声明
指定了该测试类所在的包路径为com.example。
3. 导入依赖
org.junit.jupiter.api.Test：JUnit 5的注解，用于标记测试方法。
org.springframework.boot.test.context.SpringBootTest：Spring Boot提供的注解，用于加载Spring Boot应用程序的上下文。
4. 测试类定义
@SpringBootTest：这个注解会启动Spring Boot的测试上下文，加载SpringBootApplication类中的配置，确保整个Spring应用程序上下文被加载。
class SpringbootApplicationTests：定义了一个名为SpringbootApplicationTests的测试类。
5. 测试方法
@Test：标记这是一个测试方法。
contextLoads：这是测试方法的名称，通常用于测试Spring上下文是否能够正确加载。目前这个方法是空的，但它会通过Spring Boot的测试上下文来验证Spring应用程序上下文是否能够正常启动。
#### 20250315 小结 （四）执行顺序
##### [0].项目文件清单
1. 前端树形结构表示
vue/
├── public/ ---------------------------(静态文件)
│   ├── *favicon.ico*
│   └── *index.html*
├── src/ ------------------------------(项目源码目录)
│   ├── *main.js*
│   ├── [App.vue]
│   ├── views/ ------------------------(视图文件)
│   │   ├── [HomeView.vue]
│   │   ├── [AboutView.vue]
│   ├── components/ -------------------(视图组件)
│   │   ├── [HelloWorld.vue]
│   ├── router/ -----------------------(路由配置)
│   │   └── *index.js*
│   ├── utils/ ------------------------(封装请求)
│   │   └── *request.js*(自创建)
│   └── assets/ -----------------------(静态文件)
│       ├── css/ *global.css*(自创建)
│       └── images/
└── *vue.config.js*
2. 后端树形结构表示
业务逻辑：Controller=>Service=>Dao(Mapper)=>Entity=>数据库
springboot/
├── src/
│   ├── test/
│   │   └── com/
│   │       └── example/
│   │           └── [SpringBootApplicationTests.java] --- 测试类
│   └── main/
│       ├── resources/
│       │   ├── *application.yml*(.properties) ----------**
│       │   └── mapper/
│       │       └── *XxxMapper.xml* (自创建) ------------(后端持久层映射)
│       └── java/
│           └── com/
│               └── example/
│                   ├── [SpringbootApplication.java] ----(启动类)
│                   ├── common/
│                   │   └── [Result.java] ---------------(统一返回类型)
│                   ├── exception/ ----------------------**
│                   ├── controller/ ---------------------(前后端接口)
│                   │   └── [XxxController.java]
│                   ├── service/ ------------------------(后端业务层)
│                   │   └── [XxxService.java]
│                   ├── dao/ ----------------------------(后端持久层)
│                   │   └── [XxxDao.java]
│                   └── entity/ -------------------------(实体类对象)
│                       └── [XxxEntity.java]
│                       └── [Params.java] ---------------(接收前端参数实体类)
└── *pom.xml* ------------------------------------------- 依赖包
3. 前端项目文件清单
vue/*vue.config.js*
vue/src/*main.js*
vue/src/utils/*request.js*
vue/src/assets/*global.css*
vue/src/[App.vue]
vue/src/router/*index.js*
vue/src/views/[HomeView.vue]
vue/src/views/[AboutView.vue]
vue/src/components/[HelloWorld.vue]
vue/public/*favicon.ico*
vue/public/*index.html*
4. 后端项目文件清单
springboot/*pom.xml*
springboot/src/main/resources/*application.yml*
springboot/src/main/java/com/example/[SpringbootApplication.java]
springboot/src/main/java/com/example/controller/[Controller.java]
springboot/src/main/java/com/example/service/[Service.java]
springboot/src/main/java/com/example/dao/[Dao.java]
springboot/src/main/resources/mapper/*Mapper.xml*
springboot/src/main/java/com/example/entity/[Entity.java]
springboot/src/main/java/com/example/common/[Result.java]
springboot/src/main/java/com/example/entity/[Params.java]
springboot/src/test/com/example/[SpringBootApplicationTests.java]
##### [1].前端项目执行顺序
1. vue.config.js：配置文件，初始化时加载。
(1)作用：这是 Vue CLI 项目的配置文件，用于自定义项目的构建配置、插件配置等。
(2)执行顺序：在项目启动时（如运行 npm run serve 或 npm run build）首先读取并应用配置。
2. vue/src/main.js：入口文件，初始化 Vue 实例。
(1)作用：这是 Vue 应用的入口文件，负责初始化 Vue 实例并挂载到 DOM 上。
(2)执行顺序：在项目启动后，main.js 会被加载并执行，它是整个应用的入口点。
3. vue/src/utils/request.js：工具文件，按需加载。
(1)作用：通常用于封装 HTTP 请求，如使用 Axios 进行 API 调用。
(2)执行顺序：在 main.js 中导入并使用 request.js 时，request.js 会被加载并执行。
4. vue/src/assets/global.css：全局样式文件，按需加载。
(1)作用：全局样式文件，用于定义全局的 CSS 样式。
(2)执行顺序：在 main.js 中导入 global.css 时，样式会被加载并应用到整个应用中。
5. vue/src/App.vue：根组件，挂载到页面。
(1)作用：这是 Vue 应用的根组件，包含整个应用的布局和结构。
(2)执行顺序：在 main.js 中创建 Vue 实例时，App.vue 会被加载并挂载到页面上。
6. vue/src/router/index.js：路由配置，初始化路由。
(1)作用：定义路由配置，管理页面跳转和组件的显示。
(2)执行顺序：在 main.js 中导入并使用 router/index.js 时，路由配置会被加载并初始化。
7. vue/src/views/HomeView.vue：首页组件，按路由加载。
(1)作用：首页组件，通常在路由配置中被定义为默认路由。
(2)执行顺序：在路由初始化后，当访问默认路由时，HomeView.vue 会被加载并显示。
8. vue/src/views/AboutView.vue：关于页面组件，按路由加载。
(1)作用：关于页面组件，通常在路由配置中被定义为一个子路由。
(2)执行顺序：在路由初始化后，当访问对应的路由时，AboutView.vue 会被加载并显示。
9. vue/src/components/HelloWorld.vue：自定义组件，按需加载。
(1)作用：自定义组件，通常在其他组件中被引用。
(2)执行顺序：在其他组件（如 HomeView.vue 或 App.vue）中导入并使用 HelloWorld.vue 时，该组件会被加载并渲染。
10. vue/public/favicon.ico 网站图标，构建时复制并加载。
作用：网站的图标文件，显示在浏览器标签页上。
执行顺序：在项目构建时，favicon.ico 会被复制到构建目录中，并在页面加载时被浏览器加载。
11. vue/public/index.html HTML 模板文件，构建时复制并加载。
作用：项目的 HTML 模板文件，定义了页面的基本结构。
执行顺序：在项目构建时，index.html 会被复制到构建目录中，并在页面加载时被浏览器加载。
##### [2].后端项目执行顺序
1. pom.xml：解析依赖和插件。（在接收到 HTTP 请求之前已经完成）
(1)作用：Maven 项目的配置文件，定义了项目的依赖、插件、构建配置等。
(2)执行顺序：在项目启动时，Maven 会首先解析 pom.xml 文件，加载项目所需的依赖和插件。
2. application.yml：加载配置。（在接收到 HTTP 请求之前已经完成）
(1)作用：Spring Boot 的配置文件，用于定义项目的各种配置，如数据库连接、服务器端口等。
(2)执行顺序：在 Spring Boot 应用启动时，Spring Boot 的 Environment 会加载 application.yml 文件中的配置。
3. SpringbootApplication.java：启动 Spring Boot 应用。（在接收到 HTTP 请求之前已经完成）
(1)作用：Spring Boot 应用的入口类，通常包含 @SpringBootApplication 注解，用于启动 Spring Boot 应用。
(2)执行顺序：在运行 SpringbootApplication 类的 main 方法时，Spring Boot 应用开始启动。
4. Controller.java：控制器类，匹配并处理 HTTP 请求。
(1)作用：控制器类，用于处理 HTTP 请求。
(2)执行顺序：当接收到 HTTP 请求时，Spring MVC 的 DispatcherServlet 会根据请求的 URL 和方法，匹配到对应的控制器方法。Controller 类中的相应方法会被调用。
5. Service.java：服务层类，调用业务逻辑。
(1)作用：服务层类，用于定义业务逻辑。
(2)执行顺序：在控制器方法中调用服务层方法时，Service 类中的相应方法会被调用。
6. Dao.java：数据访问对象，执行数据库操作。
(1)作用：数据访问对象（DAO），用于定义与数据库交互的方法。
(2)执行顺序：在服务层方法中调用 DAO 方法时，Dao 类中的相应方法会被调用。
7. Mapper.xml：MyBatis 映射文件，解析 SQL 映射。（在应用启动时加载）
(1)作用：MyBatis 的映射文件，用于定义 SQL 映射。
(2)执行顺序：如果使用 MyBatis，Mapper.xml 文件会在应用启动时被加载并解析。在 DAO 方法中调用数据库操作时，MyBatis 会根据 Mapper.xml 中的 SQL 映射执行相应的数据库操作。
8. Entity.java：实体类，映射数据库表。
(1)作用：实体类，通常用于映射数据库表。
(2)执行顺序：在 DAO 方法中操作数据库时，Entity 类会被使用。例如，查询结果会被映射到 Entity 类的实例中。
9. Result.java：通用响应结果类，封装响应数据。
(1)作用：通用的响应结果类，通常用于封装 API 的响应数据。
(2)执行顺序：在服务层方法中返回响应数据时，Result 类会被使用。
10. Params.java：请求参数类，接收请求参数。
(1)作用：实体类，用于定义请求参数的结构。
(2)执行顺序：在控制器方法中接收请求参数时，Params 类会被使用。
11. SpringBootApplicationTests.java：测试类，用于开发阶段的测试。（与 HTTP 请求处理无关）
(1)作用：测试类，用于编写单元测试或集成测试。
(2)执行顺序：测试类通常在开发阶段使用，用于验证应用的功能是否正常。
#### 20250408 小结 （五）统一步骤
##### [0].统一配置
1. 前端项目统一配置
(1)main.js
(2)global.css
(3)index.js
2. 后端项目统一配置
(1)pom.xml
(2)application.yml
(3)SpringbootApplication.java
##### [0].统一封装
1. vue封装请求消息
vue/src/utils/request.js
(1)导入axios库
(2)创建axios实例，设置后台访问端口`baseURL: 'http://localhost:8080'`
(3)request拦截器，配置请求对象
(4)response 拦截器，res即为后端返回的Result结果
(5)导出封装的请求对象，供前端引用，向后端发送请求
2. springboot封装返回结果
springboot/src/main/java/com/example/common/Result.java
(1)定义成员变量 code、msg、data (返回状态、返回消息、返回数据)
(2)生成getter、setter
(3)构造方法默认省略 public Result() {}
(4)定义常量 SUCCESS、ERROR (成功和错误状态)
(5)定义成功的静态方法，用于创建成功的响应
(6)定义错误的静态方法，用于创建失败的响应
[1]响应成功，返回状态 public static Result success(){}
[2]响应成功，返回状态和数据 public static Result success(Object data){}
[3]响应失败，返回状态和消息 public static Result error(String msg){}
##### [1].新建数据库表
1. 建表步骤
(1)新建数据库表并注释，如"用户信息表"
(2)添加字段
(3)保存并命名
(4)填充表数据
2. 建表信息
(1)注释
(2)字段
(3)SQL预览
(4)选项
(5)索引
(6)外键
(7)检查
(8)触发器
3. 建表字段
(1)字段
含"名、类型、长度、小数点、不是null、虚拟、键、注释"
(1)字段名
对应数据库表的每列属性
对应前端data(){return {}}
对应后端Entity层
(2)字段是主键ID
字段列：名"id"、类型"int"、勾选"键""不是null"
状态栏：勾选"自动递增"
(3)字段是字符类型
字段列：类型"varchar"、长度"255"
状态栏：字符集"utf8mb4" 排序规则"utf8mb4_unicode_ci"
4. 填充表数据
##### [2].前端业务逻辑
1. 创建页面视图
(1)创建前端页面vue/src/views/AdminView.vue
(2)添加页面路由vue/src/router/index.js
(3)创建页面布局 Element官网(Container 布局容器)：https://element.eleme.cn/#/zh-CN/component/container
(4)引入视图组件 Element官网(Table 表格)：https://element.eleme.cn/#/zh-CN/component/table
2. 编写业务逻辑
(1)封装请求对象request，设置后台访问端口`baseURL: 'http://localhost:8080'`
(2)导入封装好的 request 对象`import request from "@/utils/request";`
(3)编写组件创建时渲染的响应式数据`data() {return {}}`
(4)编写组件创建时调用的钩子函数`created() {}`
(5)编写实现组件事件处理和业务逻辑的方法`methods: {}`
(6)发送GET请求`request.get("/admin")`
(7)处理响应并渲染视图`.then(res => {})`
##### [3].后端业务逻辑
2. 创建Entity层，依次创建Controller、Service、Dao层
(1)springboot/src/main/java/com/example/
  common/
  exception/
  controller/ `XxxController.java`
  service/ `XxxService.java`
  dao/ `XxxDao.java(Interface)`
  entity/ `XxxEntity.java``Params.java`
(2)springboot/src/main/resources/
  mapper/ *XxxMapper.xml*
3. 创建Params.java (Entity层接收前端参数实体类)
(1)定义接收参数(参数名对应前端data() {return {}}绑定数据)
(2)生成getter、setter方法
4. 注解标记Entity层
(1)注解对应数据库表`@Table(name = "admin")`
(2)注解对应数据库主键`@Id`
(3)注解对应数据库主键自增`@GeneratedValue(strategy = GenerationType.IDENTITY)`
(4)注解对应数据库字段`@Column(name = "column-name")`
(4)生成getter、setter方法
5. 注解标记Controller层
(1)注解标记Controller层`@CrossOrigin`允许跨域请求访问当前控制器或方法
(2)注解标记Controller层`@RestController`定义一个返回 JSON/XML 数据的控制器
(3)注解标记Controller层`@RequestMapping("/admin")`定义控制器的根路径为 /admin
(4)注解引入Service层`@Resource` `private AdminService adminService;`
6. 注解标记Service层
(1)注解标记Service层`@Service`
(2)注解引入Dao层`@Resource` `private AdminDao adminDao;`
7. 注解标记Dao层
(1)注解标记Dao层`@Repository`
8. 创建Mapper.xml (Dao层映射)
(1)指定 XML 文件的版本和编码格式`version="1.0" encoding="UTF-8"`
(2)定义该 XML 文件遵循的 DTD`mybatis-3-mapper.dtd`，用于验证 Mapper XML 文件的格式是否正确
(3)定义 Mapper 的命名空间：`namespace`对应接口的全限定名
(4)查询标签`<select></select>`
(5)定义查询的唯一标识：`id`对应接口的方法名
(6)定义查询结果映射的 Java 类型：`resultType`对应实体类的全限定名
(7)编写SQL语句`select * from admin`
7. 创建
7. 后端业务逻辑
Controller=>Service=>Dao(Mapper)=>Entity=>数据库
8. 前端处理后端返回结果并渲染视图
#### 20250315 小结 （六）1.查(查询全部)
1. 实现内容
(1)在浏览器地址栏输入指定url
(2)返回对应页面
(3)后端查询数据库返回给前端
(4)前端在页面上展示查询的全部用户信息
2. 创建关于查询对象的数据库表
创建用户信息表 admin.sql
3. 前端页面创建
创建vue/src/views/AdminView.vue
4. 前端页面路由
在vue/src/router/index.js中写
(1)`import AdminView from '../views/AdminView.vue'`
(2)`{path: '/admin',name: 'home',component: AdminView}`
5. 前端页面组件
(1)引入 Table 表格`<el-table></el-table>`
(2)根据数据库表字段添加表格列
6. 绑定动态数据
(1)表格的"prop"属性对应数据库字段名，多个字段属性构成表格数据数组
(2)绑定数据`:data="tableData"`，表格内容随后端查询动态更新
7. 前端业务逻辑
(1)导入封装对象`import request from "@/utils/request";`
(2)编写响应式数据`data() {return {}}`
  `tableData: []`
(3)编写钩子函数`created() {}`
  `this.load();`
(4)编写事件方法`methods: {load() {}}`
  1发送GET请求`request.get("/admin")`
  2响应成功，处理响应`.then(res => {if (res.code === '0') {}})`
    `this.tableData = res.data;`
8. 创建Entity层，依次创建Controller、Service、Dao层
(1)springboot/src/main/java/com/example/
  common/
  exception/
  controller/ `AdminController.java`
  service/ `AdminService.java`
  dao/ `AdminDao.java(Interface)`
  entity/ `Admin.java`
(2)springboot/src/main/resources/
  mapper/ *AdminMapper.xml*
9. 在Entity.java中写
(1)注解对应数据库表`@Table(name = "admin")`
(2)注解对应数据库主键`@Id`主键自增`@GeneratedValue(strategy = GenerationType.IDENTITY)`
(3)注解对应数据库字段`@Column(name = "column-name")`
(4)生成getter、setter方法
10. 在Controller.java中写
(1)注解对应前端GET请求`@GetMapping`
(2)Controller层查询全部方法`public Result findAll(){}`
(3)调用Service层查询全部方法`List<Admin> list = adminService.findAll();`
(4)返回封装结果`return Result.success(list);`
(5)快捷键生成Service层查询全部方法`public List<Admin> findAll(){}`
11. 在Service.java中写 [1]Dao层基于tk.mybatis依赖查询数据库
(1)Service层查询全部方法`public List<Admin> findAll(){}`
(2)调用Dao层查询全部方法`adminDao.selectAll();`
(3)作为结果返回`return adminDao.selectAll();`
(4)Dao层基于tk.mybatis依赖查询数据库
11. 在Dao.java(Interface)中写 [1]Dao层基于tk.mybatis依赖查询数据库
(1)继承Mapper泛型接口，并指定泛型参数为Admin实体类`extends Mapper<Admin>{}`
(2)Dao层基于tk.mybatis依赖查询数据库
12. 在Service.java中写 [2]Dao层基于注解查询数据库
(1)Service层查询全部方法`public List<Admin> findAll(){}`
(2)调用Dao层查询全部方法`adminDao.getAll();`
(3)作为结果返回`return adminDao.getAll();`
(4)快捷键生成Dao层查询全部方法`List<Admin> getAll();`
12. 在Dao.java(Interface)中写 [2]Dao层基于注解查询数据库
(1)继承Mapper泛型接口，并指定泛型参数为Admin实体类`extends Mapper<Admin>{}`
(2)Dao层SQL注解`@Select("select * from admin")`
(3)Dao层查询全部方法`List<Admin> getAll();`
(4)Dao层基于注解查询数据库
13. 在Dao.java(Interface)中写 [3]Dao层基于映射查询数据库
(1)继承Mapper泛型接口，并指定泛型参数为Admin实体类`extends Mapper<Admin>{}`
(2)Dao层查询全部方法`List<Admin> getAll();`
(3)Dao层基于映射查询数据库
13. 创建Mapper.xml (Dao层映射) [3]Dao层基于映射查询数据库
(1)定义映射的命名空间`namespace="com.example.dao.AdminDao"`对应Dao层全限定名
(2)查询标签`<select></select>`
(3)定义查询的唯一标识`id="getAll"`对应Dao层方法名
(4)定义查询结果映射的 Java 类型`resultType="com.example.entity.Admin"`对应实体类的全限定名
(5)编写SQL语句`select * from admin`
(6)Dao层基于映射查询数据库
14. 后端业务逻辑
Controller=>Service=>Dao(Mapper)=>Entity=>数据库
15. 前端处理后端返回结果并渲染视图
##### [1].vue项目 index.js
vue/src/router/index.js
```js
import Vue from 'vue'
import VueRouter from 'vue-router'
import AdminView from '../views/AdminView.vue'//1.导入 AdminView 组件
Vue.use(VueRouter)
const routes = [//[路由规则数组]
  {path: '/admin',name: 'home',component: AdminView}]//2.添加路由
const router = new VueRouter({//[新建路由实例]
  mode: 'history',
  base: process.env.BASE_URL,
  routes
})
export default router
```
##### [2].vue项目 AdminView.vue
vue/src/views/AdminView.vue
```js
<el-table :data="tableData" style="width: 100%; margin: 15px 0px">
  <el-table-column prop="name" label="姓名" width="180"></el-table-column>
  <el-table-column prop="sex" label="性别" width="180"></el-table-column>
  <el-table-column prop="age" label="年龄" width="180"></el-table-column>
  <el-table-column prop="phone" label="电话" width="180"></el-table-column>
  <el-table-column prop="role" label="角色" width="180"></el-table-column>
  <el-table-column label="操作"></el-table-column>
</el-table>
```
```js
<script>
import request from "@/utils/request";// 1.导入封装好的 request 对象
export default {
  name: "AdminView",
  data() {//[响应式数据]定义组件的响应式数据
    return {
      tableData: []//2.清空假数据
    }
  },
  created() {//[生命周期钩子]组件创建时的生命周期钩子，用于初始化逻辑
    this.load();//3.调用加载方法
  },
  methods: {//[方法]定义组件的方法，用于事件处理和业务逻辑
    load() {
      request.get("/admin")//4.发送GET请求
        .then(res => {// 5.处理响应数据
          if (res.code === '0') {
            this.tableData = res.data;//6.把响应数据赋值给tableData
          }
        })
    }
}
</script>
```
##### [3].springboot项目 Admin.java
springboot/src/main/java/com/example/entity/Admin.java
```java
@Table(name = "admin")//1.对应数据库表
public class Admin {
    @Id//2.对应数据库主键
    @GeneratedValue(strategy = GenerationType.IDENTITY)//3.对应数据库自增
    private Integer id;
    @Column(name = "name")//4.对应数据库字段
    private String name;
    @Column(name = "password")
    private String password;
    @Column(name = "sex")
    private String sex;
    @Column(name = "age")
    private Integer age;
    @Column(name = "phone")
    private String phone;
    //5.生成对应getter、setter
}
```
##### [4].springboot项目 AdminController.java
springboot/src/main/java/com/example/controller/AdminController.java
```java
@CrossOrigin//[解决跨域问题]简化 CORS 配置，允许跨域请求访问当前控制器或方法
@RestController//[标记层]标记一个类为控制器，并且返回的数据不会被解析为视图模板，而是直接作为响应体返回给客户端。
//是一个组合注解，等同于 @Controller 和 @ResponseBody 的结合
@RequestMapping("/admin")//[对应前端请求路径]定义了当前控制器的根路径，所有访问该控制器的方法时，请求路径都会以 /admin 开头
public class AdminController {
    @Resource//1.引用层
    private AdminService adminService;
    @GetMapping//[对应GET请求路径]
    public Result findAll() {//2.查询全部
        List<Admin> list = adminService.findAll();//3.调用层
        return Result.success(list);//4.统一封装返回值public static Result success(Object data){}
    }
```
##### [5].springboot项目 AdminService.java
springboot/src/main/java/com/example/service/AdminService.java
```java
@Service//[标记层]
public class AdminService {
    @Resource//1.引用层
    private AdminDao adminDao;
    public List<Admin> findAll() {//2.查询全部
        return adminDao.selectAll();//3.调用层(作为返回结果)，adminDao基于tk.mybatis依赖查询数据库
    }
```
##### [6].springboot项目 AdminDao.java(Interface)
springboot/src/main/java/com/example/dao/AdminDao.java(Interface)
```java
@Repository//[标记层]
public interface AdminDao extends Mapper<Admin> {//1.继承Mapper泛型接口，指定实体类Admin为泛型参数
    //2.1 Dao层基于tk.mybatis依赖查询数据库
    //2.2 Dao层基于注解|映射查询数据库
    @Select("select * from admin")
    List<Admin> getAll();
}
```
##### [7].springboot项目 AdminMapper.xml
springboot/src/main/resources/mapper/AdminMapper.xml
```xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE mapper PUBLIC "-//mybatis.org//DTD Mapper 3.0//EN" "http://mybatis.org/dtd/mybatis-3-mapper.dtd">
<mapper namespace="com.example.dao.AdminDao">
    <select id="getAll" resultType="com.example.entity.Admin">
        select * from admin
    </select>
</mapper>
```
#### 20250404 小结 （六）1.查(条件查询)
1. 实现内容
(1)在查询全部基础上完成条件查询
(2)在页面输入框内输入查询条件(姓名、电话)
(3)点击查询按钮
(4)后端根据前端输入的内容(姓名、电话)查询数据库
(5)前端在页面上展示条件查询结果
(6)点击清空按钮
(7)前端在页面上重新加载查询的全部用户信息
2. 前端页面
vue/src/views/AdminView.vue
3. 前端页面组件
(1)引入 Input 输入框`<el-input></el-input>`
(2)引入 Button 按钮`<el-button></el-button>`
4. 绑定动态数据
(1)绑定数据`v-model="params.name"`，后端接收参数(姓名)随输入内容动态更新
(2)绑定数据`v-model="params.phone"`，后端接收参数(电话)随输入内容动态更新
(3)绑定事件`@click="findBySearch()"`，点击按钮进行条件查询
(4)绑定事件`@click="reset()"`，点击按钮进行清空条件查询
5. 前端业务逻辑
(1)导入封装对象`import request from "@/utils/request";`
(2)编写响应式数据`data() {return {}}`
  `params: {name: '',phone: ''}`
(3)编写钩子函数`created() {}`
  `this.findBySearch();`
(4)编写事件方法`methods: {findBySearch() {}}`
  1发送GET请求、传递参数`request.get("/admin/search",{params:this.params})`
  2响应成功，处理响应`.then(res => {if (res.code === '0') {}})`
    `this.tableData = res.data;`
  3响应失败，返回消息`else{}`
    `this.$message({message: res.msg,type: 'error'});`
(5)编写事件方法`methods: {reset() {}}`
  1清空输入框的绑定数据`this.params = {name: '',phone: ''}`
  2重新加载条件查询`this.findBySearch();`
6. 创建Entity层，依次创建Controller、Service、Dao层
(1)springboot/src/main/java/com/example/
  common/
  exception/
  controller/ `AdminController.java`
  service/ `AdminService.java`
  dao/ `AdminDao.java(Interface)`
  entity/ `Admin.java``Params.java`
(2)springboot/src/main/resources/
  mapper/ *AdminMapper.xml*
7. 创建Params.java (Entity层接收前端参数实体类)
(1)定义接收参数(参数名"params"对应前端data() {return {}}绑定数据)
  姓名`private String name;`
  电话`private String phone;`
(2)生成getter、setter方法
8. 在Controller.java中写
(1)注解对应前端GET请求`@GetMapping("/search")`
(2)Controller层条件查询方法`public Result findBySearch(Params params){}`
  (参数名"params"对应前端data() {return {}}绑定数据)
(3)调用Service层条件查询方法`List<Admin> list = adminService.findBySearch(params);`
(4)返回封装结果`return Result.success(list);`
(5)快捷键生成Service层条件查询方法`public List<Admin> findBySearch(Params params){}`
9. 在Service.java中写
(1)Service层条件查询方法`public List<Admin> findBySearch(Params params){}`
(2)调用Dao层条件查询方法`adminDao.findBySearch(params);`
(4)作为结果返回`return adminDao.findBySearch(params);`
(3)快捷键生成Dao层条件查询方法`List<Admin> findBySearch(Params params);`
10. 在Dao.java(Interface)中写
(1)继承Mapper泛型接口，并指定泛型参数为Admin实体类`extends Mapper<Admin>{}`
(2)Dao层条件查询方法`List<Admin> findBySearch(Params params);`
(3)注解标记方法参数`List<Admin> findBySearch(@Param("params")Params params);`
  @Param("params")为findBySearch方法的参数params指定了名称params。
  @Param注解通常用于在Repository接口中为方法参数命名，方便在SQL语句中引用这些参数。
  @Param注解的名称必须与方法参数的名称一致。
  Dao层基于SQL注解查询数据库时，就需要使用@Param注解来为参数命名。
  在@Query注解的SQL语句中，可以通过:params.name和:params.age来引用params对象中的name和age属性。
(4)Dao层基于映射查询数据库
11. 创建Mapper.xml (Dao层映射)
(1)定义映射的命名空间`namespace="com.example.dao.AdminDao"`对应Dao层全限定名
(2)查询标签`<select></select>`
(3)定义查询的唯一标识`id="findBySearch"`对应Dao层方法名
(4)定义查询结果映射的 Java 类型`resultType="com.example.entity.Admin"`对应实体类的全限定名
(5)编写SQL语句`select * from admin`
(5)编写SQL语句`<where></where>`标签
(5)编写SQL语句`<if></if>`标签
(6)Dao层基于映射查询数据库
11. <select> 标签
(1)`id`属性：`findBySearch`，该查询方法的唯一标识，可以在对应的 Mapper 接口中通过该方法名调用该查询。
(2)`parameterType`属性：`com.example.params.AdminSearchParams`，指定传入参数的类型。
(3)`resultType`属性：`com.example.entity.Admin`，指定查询结果映射到的 Java 类型。
11. <where> 标签
(1)`<where>` 是 MyBatis 提供的一个动态 SQL 标签，用于自动处理条件语句的拼接。
(2)它会根据内部的条件动态生成 WHERE 子句，并且会自动处理条件为空的情况，避免生成多余的 AND 或 OR 关键字。
11. <if> 标签 (条件判断)
(1)`<if>` 是 MyBatis 的条件判断标签，用于根据条件动态生成 SQL 片段。
(2)`params != null`确保传入的参数对象不为 null。
(3)`params.name != null`确保 name 字段不为 null。
(4)`params.name != ''`确保 name 字段不为空字符串。
11. <if> 标签 (SQL 片段)
(1)`and name like concat('%', #{params.name}, '%')`
  如果条件成立，则在 SQL 中添加 name 字段的模糊查询条件
(2)`'%', #{params.name}, '%'`
  表示将 % 符号添加到 params.name 的前后，形成一个模糊匹配的模式。
(3)`#{params.name}`
  MyBatis 的参数占位符，表示绑定 params 对象的 name 属性值。
  表示将 params 对象的 name 属性值动态插入到 SQL 中。
(4)`%`是一个通配符
  表示任意字符序列（包括空字符）
(5)`phone LIKE '%13800138000%'`
  表示查询 phone 字段中包含 13800138000 的所有记录，
  无论 13800138000 出现在字段的开头、中间还是结尾。
(6)`AND phone LIKE CONCAT('%', #{params.phone}, '%')`
  如果条件成立，则在 SQL 中添加 phone 字段的模糊查询条件
(7)使用 `#{}` 占位符可以有效防止 SQL 注入攻击，因为 MyBatis 会自动对参数进行预处理。
12. 后端业务逻辑
Controller=>Service=>Dao(Mapper)=>Entity=>数据库
13. 前端处理后端返回结果并渲染视图
##### [1].vue项目 AdminView.vue
vue/src/views/AdminView.vue
```js
<div>
  <el-input v-model="params.name" style="width: 200px; margin-right: 10px" placeholder="请输入姓名"></el-input>
  <el-input v-model="params.phone" style="width: 200px; margin-right: 10px" placeholder="请输入电话"></el-input>
  <el-button type="warning" @click="findBySearch()">查询</el-button>
  <el-button type="warning" @click="reset()">清空</el-button>
</div>
```
```js
<script>
import request from "@/utils/request";// 1.导入封装好的 request 对象
export default {
  name: "AdminView",
  data() {//[响应式数据]定义组件的响应式数据
    return {
      params:{name: '',phone: ''}//2.绑定参数
    }
  },
  created() {//[生命周期钩子]组件创建时的生命周期钩子，用于初始化逻辑
    this.findBySearch();
  },
  methods: {//[方法]定义组件的方法，用于事件处理和业务逻辑
    findBySearch(){
      request.get("/admin/search",{params:this.params})//4.发送GET请求
          .then(res =>{// 5.处理响应数据
        if(res.code === '0'){
          this.tableData = res.data;//6.把响应数据赋值给tableData
        }else{
          this.$message({message: res.msg,type: 'error'});//7.响应失败，返回消息
        }
      })
    },
    reset(){
      this.params = {
        name: '',
        phone: ''
      }
      this.findBySearch();
    }
}
</script>
```
##### [2].springboot项目 Params.java
springboot/src/main/java/com/example/entity/Params.java
```java
public class Params {
    private String name;
    private String phone;
    //getter、setter
}
```
##### [3].springboot项目 AdminController.java
springboot/src/main/java/com/example/controller/AdminController.java
```java
@CrossOrigin//[解决跨域问题]简化 CORS 配置，允许跨域请求访问当前控制器或方法
@RestController//[标记层]标记一个类为控制器，并且返回的数据不会被解析为视图模板，而是直接作为响应体返回给客户端。
//是一个组合注解，等同于 @Controller 和 @ResponseBody 的结合
@RequestMapping("/admin")//[对应前端请求路径]定义了当前控制器的根路径，所有访问该控制器的方法时，请求路径都会以 /admin 开头
public class AdminController {
    @Resource//1.引用层
    private AdminService adminService;
    @GetMapping("/search")//[对应GET请求路径]
    public Result findBySearch(Params params) {//2.条件查询
        List<Admin> list = adminService.findBySearch(params);//3.调用层
        return Result.success(list);//4.统一封装返回值public static Result success(Object data){}
    }
```
##### [4].springboot项目 AdminService.java
springboot/src/main/java/com/example/service/AdminService.java
```java
@Service//[标记层]
public class AdminService {
    @Resource//1.引用层
    private AdminDao adminDao;
    public List<Admin> findBySearch(Params params) {//2.条件查询
        return adminDao.findBySearch(params);//3.调用层(作为返回结果)
    }
```
##### [5].springboot项目 AdminDao.java(Interface)
springboot/src/main/java/com/example/dao/AdminDao.java(Interface)
```java
@Repository//[标记层]
public interface AdminDao extends Mapper<Admin> {//1.继承Mapper泛型接口，指定实体类Admin为泛型参数
    //2.Dao层基于映射查询数据库
    List<Admin> findBySearch(@Param("params")Params params);
}
```
##### [6].springboot项目 AdminMapper.xml
springboot/src/main/resources/mapper/AdminMapper.xml
```xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE mapper PUBLIC "-//mybatis.org//DTD Mapper 3.0//EN" "http://mybatis.org/dtd/mybatis-3-mapper.dtd">
<mapper namespace="com.example.dao.AdminDao">
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
#### 20250413 小结 （六）1.查(分页查询)
1. 实现内容
(1)在条件查询基础上完成分页查询
(2)在页面输入框内输入查询条件(姓名、电话)
(3)点击查询、清空按钮
(4)前端按照分页要求展示条件查询结果
(5)点击分页相关按钮(切换每页几条、当前页码、上一页、下一页)
(6)前端展示分页查询结果
2. 前端页面
vue/src/views/AdminView.vue
3. 前端页面组件
(1)引入 Pagination 分页`<el-pagination></el-pagination>`
(2)为分页组件添加模块`layout="total, sizes, prev, pager, next"`
(3)表示 总共几条、每页几条、切换上页、页码列表、切换下页`共0条|0条/页|<|1 2 3 ...|>`
4. 绑定动态数据
(1)绑定数据`:current-page="params.pageNum"`，当前页码随后端查询动态更新
(2)绑定数据`:page-sizes="[5, 10, 15, 20]"`，每页条数下拉列表
(3)绑定数据`:page-size="params.pageSize"`，每页条数
(4)绑定数据`:total="total"`，根据条件查询结果动态更新条目总数
(5)绑定事件`@size-change="handleSizeChange"`，点击对应下拉选项动态更新每页条数
(6)绑定事件`@current-change="handleCurrentChange"`，点击对应分页按钮动态更新当前页码
5. 前端业务逻辑
(1)导入封装对象`import request from "@/utils/request";`
(2)编写响应式数据`data() {return {}}`
  `params: {pageNum: 1, pageSize: 5}`
(3)编写钩子函数`created() {}`
  `this.findBySearch();`
(4)编写事件方法`methods: {findBySearch() {}}`
  1发送GET请求、传递参数`request.get("/admin/search",{params:this.params})`
  2响应成功，处理响应`.then(res => {if (res.code === '0') {}})`
    `this.tableData = res.data.list;`
    `this.total = res.data.total;`
  (由于进行了分页封装，前端接收后端查询数据有所变化)
  3响应失败，返回消息`else{}`
    `this.$message({message: res.msg,type: 'error'});`
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
6. 在pom.xml中写
(1)添加依赖(分页)pagehelper-spring-boot-starter
(2)点击Maven按钮刷新加载依赖
7. 在application.yml中写
(1)添加分页配置`pagehelper:`
(2)解决分页查询可能出现的循环依赖问题`spring: main: allow-circular-references: true`
8. 创建Entity层，依次创建Controller、Service、Dao层
(1)springboot/src/main/java/com/example/
  common/
  exception/
  controller/ `AdminController.java`
  service/ `AdminService.java`
  dao/ `AdminDao.java(Interface)`
  entity/ `Admin.java``Params.java`
(2)springboot/src/main/resources/
  mapper/ *AdminMapper.xml*
9. 在Params.java中写 (Entity层接收前端参数实体类)
(1)定义接收参数(参数名"params"对应前端data() {return {}}绑定数据)
  当前页码`private Integer PageNum;`
  每页条数`private Integer PageSize;`
(2)生成getter、setter方法
10. 在Controller.java写
(1)注解对应前端GET请求`@GetMapping("/search")`
(2)Controller层条件查询方法`public Result findBySearch(Params params){}`
  (参数名"params"对应前端data() {return {}}绑定数据)
(3)调用Service层条件查询方法`PageInfo<Admin> info = adminService.findBySearch(params);`
(4)返回封装结果`return Result.success(info);`
(5)快捷键生成Service层条件查询方法`public PageInfo<Admin> findBySearch(Params params){}`
11. 在Service.java中写
(1)Service层条件查询方法`public PageInfo<Admin> findBySearch(Params params){}`
(2)开启分页查询，传递参数(当前页码、每页条数)`PageHelper.startPage(params.getPageNum(), params.getPageSize());`
(3)调用Dao层条件查询方法`adminDao.findBySearch(params);`
(4)快捷键生成Dao层查询结果`List<Admin> list = adminDao.findBySearch(params);`
(5)将查询结果进行分页封装`PageInfo.of(list);`
(6)作为结果返回`return PageInfo.of(list);`
(7)快捷键生成Dao层条件查询方法`List<Admin> findBySearch(Params params);`
12. Dao.java(Interface) 内容同条件查询
13. Mapper.xml(Dao层映射) 内容同条件查询
14. 后端业务逻辑
Controller=>Service=>Dao(Mapper)=>Entity=>数据库
15. 前端处理后端返回结果并渲染视图
##### [1].vue项目 AdminView.vue
vue/src/views/AdminView.vue
```js
<el-pagination
  @size-change="handleSizeChange"
  @current-change="handleCurrentChange"
  :current-page="params.pageNum"
  :page-sizes="[5, 10, 15, 20]"
  :page-size="params.pageSize"
  layout="total, sizes, prev, pager, next"
  :total="total"
>
</el-pagination>
```
```js
<script>
import request from "@/utils/request";// 1.导入封装好的 request 对象
export default {
  name: "AdminView",
  data() {//[响应式数据]定义组件的响应式数据
    return {
      params:{pageNum: 1, pageSize: 5},//2.绑定参数
      total: 0
    }
  },
  created() {//[生命周期钩子]组件创建时的生命周期钩子，用于初始化逻辑
    this.findBySearch();
  },
  methods: {//[方法]定义组件的方法，用于事件处理和业务逻辑
    findBySearch(){
      request.get("/admin/search",{params:this.params})//4.发送GET请求
          .then(res =>{// 5.处理响应数据
        if(res.code === '0'){
          this.tableData = res.data.list;//6.把响应数据赋值给tableData
          this.total = res.data.total;//7.把响应数据赋值给total
        }else{
          this.$message({message: res.msg,type: 'error'});//8.响应失败，返回消息
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
    }
}
</script>
```
##### [2].springboot项目 pom.xml
pom.xml
springboot/pom.xml
```xml
<dependency>
	<groupId>com.github.pagehelper</groupId>
	<artifactId>pagehelper-spring-boot-starter</artifactId>
	<version>2.1.0</version>
</dependency>
```
##### [3].springboot项目 application.yml
springboot/src/main/resources/application.yml
```yml
spring:
  main:
    allow-circular-references: true
# 开启分页
pagehelper:
  helper-dialect: mysql
  reasonable: true
  support-methods-arguments: true
  params: count=countSql
```
##### [4].springboot项目 Params.java
springboot/src/main/java/com/example/entity/Params.java
```java
public class Params {
    private Integer PageNum;
    private Integer PageSize;
    //getter、setter
}
```
##### [5].springboot项目 AdminController.java
springboot/src/main/java/com/example/controller/AdminController.java
```java
@CrossOrigin//[解决跨域问题]简化 CORS 配置，允许跨域请求访问当前控制器或方法
@RestController//[标记层]标记一个类为控制器，并且返回的数据不会被解析为视图模板，而是直接作为响应体返回给客户端。
//是一个组合注解，等同于 @Controller 和 @ResponseBody 的结合
@RequestMapping("/admin")//[对应前端请求路径]定义了当前控制器的根路径，所有访问该控制器的方法时，请求路径都会以 /admin 开头
public class AdminController {
    @Resource//1.引用层
    private AdminService adminService;
    @GetMapping("/search")//[对应GET请求路径]
    public Result findBySearch(Params params) {//2.条件查询
        PageInfo<Admin> info = adminService.findBySearch(params);//3.调用层
        return Result.success(info);//4.统一封装返回值public static Result success(Object data){}
    }
```
##### [6].springboot项目 AdminService.java
springboot/src/main/java/com/example/service/AdminService.java
```java
@Service//[标记层]
public class AdminService {
    @Resource//1.引用层
    private AdminDao adminDao;
    public PageInfo<Admin> findBySearch(Params params) {//2.条件查询
        // 3.开启分页查询 (接下来的查询会自动按照当前开启的分页设置来查询)
        PageHelper.startPage(params.getPageNum(), params.getPageSize());
        List<Admin> list = adminDao.findBySearch(params);//4.调用层
        return PageInfo.of(list);//5.封装返回结果
    }
```
#### 20250414 小结 （六）2.增
1. 实现内容
2. 前端页面
3. 前端页面组件
4. 绑定动态数据
5. 前端业务逻辑
6. 创建Entity层，依次创建Controller、Service、Dao层
#### 20250--- 小结 （六）3.改
1. 实现内容
2. 前端页面
3. 前端页面组件
4. 绑定动态数据
5. 前端业务逻辑
6. 创建Entity层，依次创建Controller、Service、Dao层
#### 20250--- 小结 （六）4.删

#### 20250315 毕设项目
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
#### 20250315 毕设项目
题目	融创富文本音视频集合的文档社区平台的设计与实现
个人主页
账户管理：*登录、注册、(找回)
账户管理：昵称、头像、说明、账号设置
权限管理：公开隐藏主页
权限管理：公开隐藏访客
权限管理：公开隐藏关注
权限管理：公开隐藏内容
用户功能
文档协作：*在线协同编辑
内容编辑：*文本、图片、音频、视频、其他文件(支持类型)
内容编辑：*创作、保存、预览、发布、修改、删除(主要功能)
内容管理：我的发布、我的收藏(内容分类)
内容管理：图文、音频、视频、其他文件(默认分类)
内容管理：新增分类、修改分类、删除分类(自定义分类)
内容管理：搜索标题、搜索内容、搜索时间(查找方式)
用户互动
内容浏览：行业、兴趣、生活、地区、学校(内容板块)
内容浏览：关注、点赞、评论、收藏、转发(用户互动)
内容浏览：搜索标题、搜索内容、搜索时间(查找方式)
后台管理
顶级权限：用户管理、内容审核、内容板块

账户管理：用户可以注册账户。支持账号密码登录。用户可以修改个人资料，如昵称、头像等。
文件管理：支持多种格式文件的上传。用户可以下载自己上传的文件。用户可以为文档命名并进行分类管理。
文档编辑：支持富文本编辑功能，包括文字、图片、音视频的插入。用户可以将编辑好的文档发布到社区。支持文档协作，用户可以在线协同编辑文档文件。
互动功能：用户可以关注其他用户。用户可以对喜欢的内容进行点赞，收藏有价值的文档。用户可以将内容分享到其他社交平台。用户可以发表评论，进行讨论。
后台功能：管理员可以审核用户发布的内容。管理员可以对文档进行分类管理，批量删除等操作。

1、实现一个功能全面、用户友好的文档社区平台。
2、提供前后端分离的架构，确保系统的高扩展性和维护性。
3、支持富文本编辑、音视频播放等高级功能，满足用户对文档处理的多样化需求。
4、实现本地文件的上传下载预览功能，方便用户管理个人文档。
5、提供互动功能，增强用户间的交流与合作。

设计并实现一个功能完备、界面友好的文档社区平台。系统支持用户登录注册、个人信息管理、文章创作与发布等功能。能够集成富文本编辑器，允许用户在创作文章时灵活插入图片、音频、视频等多媒体元素，并实现这些元素的在线预览与播放。实现文档的分类管理以及搜索功能，方便用户快速查找特定内容，提高信息检索效率。拥有合理的用户互动模块，如评论、点赞、分享等，增强用户之间的交流与互动，营造良好的社区氛围。