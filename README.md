# mc-lab
This is an open-source personal information website, mainly for studying coding skills.

## Project Structure
project-root/
├── backend/                 # 后端(Spring Boot)代码
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/        # Java 源码目录
│   │   │   │   └── com/example/project/
│   │   │   │       ├── controller/   # 控制器层，处理HTTP请求，暴露RESTful API
│   │   │   │       ├── service/      # 业务逻辑层，编写核心逻辑
│   │   │   │       ├── repository/   # 数据访问层，连接MySQL数据库
│   │   │   │       ├── model/        # 实体类，对应数据库表
│   │   │   │       └── config/       # 配置类（数据库、跨域、安全等）
│   │   │   └── resources/
│   │   │       ├── application.yml   # Spring Boot 配置文件（数据库连接、端口等）
│   │   │       └── static/           # 静态资源目录（一般不用，前端独立部署）
│   │   └── test/                     # 后端测试代码
│   ├── pom.xml                       # Maven 配置文件（依赖管理）
│   └── target/                       # 构建输出目录（编译后生成）
│
├── frontend/                # 前端(React)代码
│   ├── public/              # 公共静态资源（HTML模板、favicon、图片等）
│   │   └── index.html       # React 根 HTML 文件
│   ├── src/                 # React 源码目录
│   │   ├── components/      # 通用组件目录（如导航栏、表单、按钮）
│   │   ├── pages/           # 页面组件（如登录页、主页、用户管理页）
│   │   ├── services/        # API 调用方法（封装 axios/fetch 调用后端 RESTful API）
│   │   ├── hooks/           # 自定义 React Hook
│   │   ├── utils/           # 工具函数（格式化日期、数据处理等）
│   │   ├── App.js           # React 根组件
│   │   └── index.js         # 项目入口，挂载 React 应用
│   ├── package.json         # 前端依赖和脚本配置
│   └── node_modules/        # 前端依赖库
│
├── database/                # 数据库相关文件
│   ├── schema.sql           # 数据库表结构定义
│   └── data.sql             # 初始数据
│
├── docs/                    # 项目文档（接口文档、设计文档、说明书等）
│
├── .gitignore               # Git 忽略规则
├── README.md                # 项目说明文件
└── docker-compose.yml       # 可选：Docker 容器编排文件（整合 MySQL + Spring Boot + React）
