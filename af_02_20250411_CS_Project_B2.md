## F 笔记
### Project_B 本科毕业设计-毕设论文
#### 20241208 [0].毕设安排
##### --- 时间安排 ---
##### --- 毕设要求 ---
##### --- 完成进度 ---
##### --- 参考资料 ---
#### 20241208 [1].选题
#### 20241226 [2].任务书
#### 20250115 [3].开题报告
#### 20250115 [4].开题答辩
#### 20250411 [5].外文翻译
#### 20240412 [6].文献综述
#### 2025---- [7].毕设论文*
#### 2025---- [8].毕业答辩*
#### 20250127 [9].指导记录*
#### 2025---- [10].查重降重

#### 20250408 小结 （一）项目简介
##### [0].README.md
##### [1].项目源码(PRJ_code)
1. 前端项目文件清单
vue/*vue.config.js*
vue/src/*main.js*
vue/src/router/*index.js*
vue/src/utils/*request.js*
vue/src/assets/*global.css*
vue/src/[App.vue]
vue/src/views/[HomeView.vue]
vue/src/views/[AboutView.vue]
vue/src/components/[HelloWorld.vue]
2. 后端项目文件清单
springboot/*pom.xml*
springboot/src/main/resources/*application.yml*
springboot/src/test/com/example/[SpringBootApplicationTests.java]
springboot/src/main/java/com/example/[SpringbootApplication.java]
springboot/src/main/java/com/example/entity/[Params.java]
springboot/src/main/java/com/example/controller/[Controller.java]
springboot/src/main/java/com/example/service/[Service.java]
springboot/src/main/java/com/example/dao/[Dao.java]
springboot/src/main/resources/mapper/*Mapper.xml*
springboot/src/main/java/com/example/entity/[Entity.java]
springboot/src/main/java/com/example/common/[Result.java]
3. 前端树形结构表示
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
4. 后端树形结构表示
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
##### [2].项目截图(PRJ_img)
##### [3].数据库表(PRJ_sql)
1. 用户信息表 admin.sql
主键ID：`id` int、不是null、键、自动递增
姓名：`name` varchar、255、utf8mb4、utf8mb4_unicode_ci
密码：`password` varchar、255、utf8mb4、utf8mb4_unicode_ci
性别：`sex` varchar、255、utf8mb4、utf8mb4_unicode_ci
年龄：`age` int
电话：`phone` varchar、255、utf8mb4、utf8mb4_unicode_ci
角色：`role` Varchar、255、utf8mb4、utf8mb4_unicode_ci
CREATE TABLE `admin` (
  `id` int NOT NULL AUTO_INCREMENT COMMENT '主键ID',
  `name` varchar(255) COLLATE utf8mb4_unicode_ci DEFAULT NULL COMMENT '姓名',
  `password` varchar(255) COLLATE utf8mb4_unicode_ci DEFAULT NULL COMMENT '密码',
  `sex` varchar(255) COLLATE utf8mb4_unicode_ci DEFAULT NULL COMMENT '性别',
  `age` int DEFAULT NULL COMMENT '年龄',
  `phone` varchar(255) COLLATE utf8mb4_unicode_ci DEFAULT NULL COMMENT '电话',
  `role` varchar(255) COLLATE utf8mb4_unicode_ci DEFAULT NULL COMMENT '角色',
  PRIMARY KEY (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=29 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_unicode_ci COMMENT='用户信息表';
2. 请假审核表 audit.sql
主键ID：`id` int、不是null、键、自动递增
请假原由：`name` varchar、255、utf8mb4、utf8mb4_unicode_ci
请假时期：`time` varchar、255、utf8mb4、utf8mb4_unicode_ci
请假天数：`day` varchar、255、utf8mb4、utf8mb4_unicode_ci
请假用户ID：`userId` int
审核状态：`status` varchar、255、utf8mb4、utf8mb4_unicode_ci
审核意见：`reason` Varchar、255、utf8mb4、utf8mb4_unicode_ci
CREATE TABLE `audit` (
  `id` int NOT NULL AUTO_INCREMENT COMMENT '主键ID',
  `name` varchar(255) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci DEFAULT NULL COMMENT '请假原由',
  `time` varchar(255) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci DEFAULT NULL COMMENT '请假时期',
  `day` varchar(255) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci DEFAULT NULL COMMENT '请假天数',
  `userId` int DEFAULT NULL COMMENT '请假用户ID',
  `status` varchar(255) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci DEFAULT NULL COMMENT '审核状态',
  `reason` varchar(255) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci DEFAULT NULL COMMENT '审核意见',
  PRIMARY KEY (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=14 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_unicode_ci COMMENT='请假审核表';
3. 图书信息表 book.sql
主键ID：`id` int、不是null、键、自动递增
图书名称：`name` varchar、255、utf8mb4、utf8mb4_unicode_ci
图书价格：`price` varchar、255、utf8mb4、utf8mb4_unicode_ci
图书作者：`author` varchar、255、utf8mb4、utf8mb4_unicode_ci
图书出版社：`press` varchar、255、utf8mb4、utf8mb4_unicode_ci
图书封面：`img` varchar、255、utf8mb4、utf8mb4_unicode_ci
图书分类ID：`typeId` int
图书介绍：`content` longtext、255、utf8mb4、utf8mb4_unicode_ci
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
) ENGINE=InnoDB AUTO_INCREMENT=10 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_unicode_ci COMMENT='图书信息表';
4. 酒店信息表 hotel.sql
主键ID：`id` int、不是null、键、自动递增
酒店名称：`name` varchar、255、utf8mb4、utf8mb4_unicode_ci
入住价格：`price` varchar、255、utf8mb4、utf8mb4_unicode_ci
酒店图片：`img` varchar、255、utf8mb4、utf8mb4_unicode_ci
剩余间数：`num` int
CREATE TABLE `hotel` (
  `id` int NOT NULL AUTO_INCREMENT COMMENT '主键ID',
  `name` varchar(255) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci DEFAULT NULL COMMENT '酒店名称',
  `price` varchar(255) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci DEFAULT NULL COMMENT '入住价格',
  `img` varchar(255) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci DEFAULT NULL COMMENT '酒店图片',
  `num` int DEFAULT NULL COMMENT '剩余间数',
  PRIMARY KEY (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=8 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_unicode_ci COMMENT='酒店信息表';
5. 操作日志表 log.sql
主键ID：`id` int、不是null、键、自动递增
操作内容：`name` varchar、255、utf8mb4、utf8mb4_unicode_ci
操作时间：`time` varchar、255、utf8mb4、utf8mb4_unicode_ci
操作人：`username` varchar、255、utf8mb4、utf8mb4_unicode_ci
操作人IP：`ip` varchar、255、utf8mb4、utf8mb4_unicode_ci
CREATE TABLE `log` (
  `id` int NOT NULL AUTO_INCREMENT COMMENT '主键ID',
  `name` varchar(255) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci DEFAULT NULL COMMENT '操作内容',
  `time` varchar(255) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci DEFAULT NULL COMMENT '操作时间',
  `username` varchar(255) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci DEFAULT NULL COMMENT '操作人',
  `ip` varchar(255) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci DEFAULT NULL COMMENT '操作人IP',
  PRIMARY KEY (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=83 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_unicode_ci COMMENT='操作日志表';
6. 系统公告表 notice.sql
主键ID：`id` int、不是null、键、自动递增
公告标题：`name` varchar、255、utf8mb4、utf8mb4_unicode_ci
公告内容：`content` text、255、utf8mb4、utf8mb4_unicode_ci
公告时间：`time` varchar、255、utf8mb4、utf8mb4_unicode_ci
CREATE TABLE `notice` (
  `id` int NOT NULL AUTO_INCREMENT COMMENT '主键ID',
  `name` varchar(255) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci DEFAULT NULL COMMENT '公告标题',
  `content` text CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci COMMENT '公告内容',
  `time` varchar(255) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci DEFAULT NULL COMMENT '公告时间',
  PRIMARY KEY (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=26 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_unicode_ci COMMENT='系统公告表';
7. 预定信息表 reserve.sql
主键ID：`id` int、不是null、键、自动递增
酒店ID：`hotelId` int
用户ID：`userId` int
预定时间：`time` varchar、255、utf8mb4、utf8mb4_unicode_ci
CREATE TABLE `reserve` (
  `id` int NOT NULL AUTO_INCREMENT COMMENT '主键ID',
  `hotelId` int DEFAULT NULL COMMENT '酒店ID',
  `userId` int DEFAULT NULL COMMENT '用户ID',
  `time` varchar(255) COLLATE utf8mb4_unicode_ci DEFAULT NULL COMMENT '预定时间',
  PRIMARY KEY (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=14 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_unicode_ci COMMENT='预定信息表';
8. 图书分类表 type.sql
主键ID：`id` int、不是null、键、自动递增
分类名称：`name` varchar、255、utf8mb4、utf8mb4_unicode_ci
分类时间：`description` varchar、255、utf8mb4、utf8mb4_unicode_ci
CREATE TABLE `type` (
  `id` int NOT NULL AUTO_INCREMENT COMMENT '主键ID',
  `name` varchar(255) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci DEFAULT NULL COMMENT '分类名称',
  `description` varchar(255) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci DEFAULT NULL COMMENT '分类介绍',
  PRIMARY KEY (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=22 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_unicode_ci COMMENT='图书分类表';
##### [4].项目组件
1. Container 布局容器：https://element.eleme.cn/#/zh-CN/component/container
2. Table 表格：https://element.eleme.cn/#/zh-CN/component/table
3. Input 输入框：https://element.eleme.cn/#/zh-CN/component/input
4. Button 按钮：https://element.eleme.cn/#/zh-CN/component/button
5. Pagination 分页：https://element.eleme.cn/#/zh-CN/component/pagination
##### [5].项目依赖
0. 复制依赖 MVNREPOSITORY：https://mvnrepository.com/
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
