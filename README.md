<h1 align="center">embroider-website-master</h1>

<br/>

## 项目说明

本刺绣网站的客户端和管理端使用 **Vue** 框架来实现，服务端使用 **Spring Boot + MyBatis** 来实现，数据库使用了 **MySQL**。实现思路可以看 **[这里](https://yin-hongwei.github.io/2019/03/04/music/#more)**；项目启动方法看文章末尾。

<br/>

## 项目预览

> **一、前台截图预览**
>
> 1、主页轮播图

![](C:\Users\choly\Desktop\images\home.png)<br/>

2、主页图片列表

![home2](C:\Users\choly\Desktop\images\home2.png)

3、刺绣介绍

![刺绣](C:\Users\choly\Desktop\images\刺绣.png)

4、工艺要求

![工艺](C:\Users\choly\Desktop\images\工艺.png)

5、工艺要求介绍

![工艺要求](C:\Users\choly\Desktop\images\工艺要求.png)

6、苗绣

![苗绣](C:\Users\choly\Desktop\images\苗绣.png)

7、苏绣

![苏绣](C:\Users\choly\Desktop\images\苏绣.png)



**二、后台管理界面截图预览**

1、主页

![首页](C:\Users\choly\Desktop\images\后台\首页.png)

2、前台用户管理

![前台](C:\Users\choly\Desktop\images\后台\前台.png)

3、后台用户管理

![后台](C:\Users\choly\Desktop\images\后台\后台.png)

4、更新前台用户

![更新用户](C:\Users\choly\Desktop\images\后台\更新用户.png)

5、添加轮播图列表

![轮播图](C:\Users\choly\Desktop\images\后台\轮播图.png)

<br/>





## 项目功能

- 用户登录注册
- 展示图片
- 展示文字
- 搜索图片，搜索用户
- 增删查改用户信息，管理员信息
- 后台对用户、轮播图、文字标题等的管理

<br/>

## 技术栈

### 后端

**SpringBoot + MyBatis**

### 前端

**Vue3.0 + TypeScript + Vue-Router + Vuex + Axios + ElementPlus**

<br/>



## ***项目结构***<u></u>

### 后端

```markdown
.
├── src
│   ├── main
│   │   ├── java
│   │   │   └── com.example.demo
│   │   │       ├── commen 		// 通用类R
│   │   │       ├── config 		// 配置（跨域）
│   │   │       ├── controller  // 控制层，接收请求返回响应
│   │   │       ├── model 		// 数据操作层
│   │   │   		|──domain	//数据库实体类
│   │   │   		|──request	//接受类型
│   │   │   		|──Return	//返回类型
│   │   │       ├── service		//业务逻辑层
│   │   │       └── DemoApplication.java // 项目入口
│   │   └── resources
│   │       ├── mapper 			// mapper.xml文件，操作数据库
│   │       ├── static 			//存放静态资源
│   │       ├── templates
│   │       ├── application.xml // 连接数据库
│   └── test
│       └── java
│           └── com.example.demo // 测试用的
├── pom.xml // 添加相关依赖和插件
└── target
```

### 前端

```markdown
.
├── build // webpack相关配置文件
├── vite.config.ts // vue基本配置文件
├── node_modules // 依赖包
├── node_modules // mock假数据，模拟开发
├── index.html // 入口页面
├── package.json // 管理包的依赖
├── src // 项目源码目录
│   ├── assets  // icon，图片、css 等
│   ├── api  	// 封装请求的 api
│   ├── components//组件
│   ├── img		//一些公共图片
│   ├── utils // 工具方法
│   ├── router // 路由
│   ├── store // 管理数据
│   ├── style // 封装样式
│   ├── views // 组件
│   │   ├── error
│   │   │   └── 404.vue // 404
│   │   ├── Home.vue // 首页
│   │   ├── culture
│   │   │   ├── jingxiu.vue // 京绣
│   │   │   ├── miaoxiu.vue // 苗绣
│   │   │   └── shuxiu.vue  // 蜀绣
│   │   │   └── suxiu.vue   // 苏绣
│   │   ├── introduce
│   │   │   └── briefIntro.vue  // 刺绣简介
│   │   │   └── techRequire.vue // 工艺简介
│   │   ├── register.vue 	// 登录区
│   │   ├── login.vue 		// 注册区
│   │   ├── joinUs.vue 		// 加入我们
│   ├── main.js // 入口js文件
│   └── App.vue // 根组件
├── static 	// 存放静态资源 
├── test 	// 测试文件目录
├── .babelrc // bable 编译配置
└── .gitignore // 提交忽略的文件配置
```



### 后端管理界面

```markdown
.
├── build // webpack相关配置文件
├── vite.config.ts // vue基本配置文件
├── node_modules // 依赖包
├── node_modules // mock假数据，模拟开发
├── index.html // 入口页面
├── package.json // 管理包的依赖
├── src // 项目源码目录
│   ├── assets  // icon，图片、css 等
│   ├── api  	// 封装请求的 api
│   ├── components//组件
│   ├── img		//一些公共图片
│   ├── utils // 工具方法
│   ├── router // 路由
│   ├── store // 管理数据
│   ├── style // 封装样式
│   ├── views // 组件
│   │   ├── error
│   │   │   └── 404.vue // 404
│   │   ├── Home.vue // 首页
│   │   ├── culture
│   │   │   ├── swipperList.vue // 轮播图管理
│   │   │   ├── titleText.vue // 标题文字管理
│   │   ├── usercontrol
│   │   │   └── afterend.vue  // 前台
│   │   │   └── frontend.vue  // 后台
│   │   ├── register.vue 	// 登录区
│   │   ├── login.vue 		// 注册区
│   ├── main.js // 入口js文件
│   └── App.vue // 根组件
├── static 	// 存放静态资源 
├── test 	// 测试文件目录
├── .babelrc // bable 编译配置
└── .gitignore // 提交忽略的文件配置
```



## 逻辑结构

#### 1）实体类（domain 目录下）

定义数据库表所对应的实体类。

#### 2）Mapper 层 / DAO 层（dao、mapper 目录下）

数据操作层：向数据库发送 SQL 语句，完成数据库操作。

分为 Mapper 接口 和 Mapper 接口映射文件。 Mapper 接口在 model目录下，定义操作数据库的函数（函数不能直接去进行 CURD）， Mapper 接口映射文件在 mapper 目录下，完成对数据库的访问。

#### 3）Service 层（service 目录下）

服务层：完成业务逻辑处理。调用 Mapper 层操作数据库。

#### 4）Controller 层（controller 目录下）

控制层：对请求和响应进行控制，调用 Service 层进行业务逻辑处理，最后将处理好的数据返回给前端。



### 数据库

![QQ图片20231205144753](C:\Users\choly\Desktop\images\后台\QQ图片20231205144753.png)



## 开发环境

JDK： java 1.8.0_391

MySQL：8.0.13（或者更高版本）

node：v16.20.0(nvm管理工具)

IDE：IntelliJ IDEA 2022、VSCode

<br/>

## 下载运行

### 1、下载项目到本地

```bash
暂未部署到github或gitee.
```

### 2、修改配置文件

1）创建数据库
将 `embroider` 文件夹中的 `cyb.sql` 文件导入数据库。

2）修改用户名密码
修改 `embroider/demo/src/main/resources/application.yml` 文件里的 `spring.datasource.username` 和 `spring.datasource.password`为你自己的数据库账号和密码。

### 3、启动项目

- **启动管理端**：进入 demo文件夹，运行下面命令启动服务器

```js
// 方法一
./mvnw spring-boot:run

// 方法二
mvn spring-boot:run // 前提装了 maven
```

- **启动客户端**：进入 client 目录，运行下面命令

```js
npm install // 安装依赖

npm run dev // 启动前台项目
```

- **启动管理端**：进入 server目录，运行下面命令

```js
npm install // 安装依赖

npm run dev // 启动后台管理项目
```

### 4、常见问题

常见启动问题整理如下：

1、![QQ图片20231205154949](C:\Users\choly\Desktop\images\后台\QQ图片20231205154949.png)

**mock中配置文件会报错,是因为vite-plugin-mock版本匹配导致的，在项目根目录：

```
pnpm i vite-plugin-mock@2.0.0
```

**还有pinia最新版也不匹配 可以安装时候 **

```
pnpm i pinia@2.0.34
```

<br/>



## 联系方式

**1、邮箱📮：3287507773@qq.com**

**2、电话：19171959570**

## License

Copyright (c) 2023 湖北民族大学智能科学与工程学院 信息安全  陈咏斌，黄席宇，张智

