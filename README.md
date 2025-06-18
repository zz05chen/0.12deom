# 化点实验 Web - 全栈AI应用框架

这是一个基于 Vue3 (Vite + TS) 和 FastAPI (Python) 的现代化全栈AI应用开发框架。它专为化学学习应用打造，内置了完整的用户认证系统、化学知识库功能以及与大语言模型（LLM）交互的聊天接口。

## ✨ 已实现功能

- **现代技术栈**: Vue 3, Vite, TypeScript, Pinia, Element Plus, FastAPI, SQLAlchemy, Pydantic。
- **全功能用户系统**: 提供JWT认证的用户注册、登录和会话管理。
- **模块化API**: 后端API按功能（认证、聊天、化学知识库）划分，结构清晰。
- **按需加载AI模型**: FastAPI在首次API调用时才加载大语言模型，优化了启动速度。
- **化学知识库基础**: 实现了元素周期表功能，并预留了化合物、仪器的查询框架。
- **AI聊天助手**: 完全集成的AI聊天界面，支持与后端LLM实时交互，可通过侧边栏和首页卡片访问。
- **现代化UI布局**: 采用专业的后台管理布局，提供侧边栏导航和用户操作区域。

## 项目结构

```
.
├── backend/                # FastAPI 后端
│   ├── api/                # API 路由 (v1) 与依赖注入
│   ├── core/               # 核心配置 (JWT, 安全, 设置)
│   ├── crud/               # 数据库增删改查(CRUD)操作
│   ├── db/                 # 数据库会话、基类与数据填充脚本
│   ├── models/             # SQLAlchemy 数据模型
│   ├── schemas/            # Pydantic 数据校验模型
│   ├── main.py             # FastAPI 应用主入口
│   ├── model_utils.py      # 大语言模型工具
│   └── run.py              # Uvicorn 启动脚本
├── frontend/               # Vue3 前端
│   ├── src/
│   │   ├── assets/         # 静态资源 (图片, SVG，文字数据等)
│   │   ├── components/     # 可复用Vue组件 (如: 元素周期表)
│   │   ├── layouts/        # 主布局组件
│   │   ├── router/         # Vue Router 路由配置
│   │   ├── store/          # Pinia 状态管理
│   │   ├── views/          # 页面级视图组件
│   │   ├── App.vue         # Vue 应用根组件
│   │   └── main.ts         # 前端应用入口
│   └── ...                 # (其他配置文件: vite.config, tsconfig, etc.)
├── sql数据库/              # SQL脚本与数据库文件
├── .env.example            # 环境变量示例文件
├── start-and-install.ps1   # 首次安装与启动脚本
└── start-fast.ps1          # 快速启动脚本
```

## 开发路线图

项目当前已完成：
- ✅ 基础框架与用户系统
- ✅ 基础化学知识库功能
- ✅ 前端架构重构与UI美化
- ✅ AI聊天功能（包括UI集成与后端通信）

下一步计划：
- 知识库前端优化
- AI聊天功能增强
- 数据扩充与性能优化

## 技术栈

- 前端：Vue 3, Vite, TypeScript, Element Plus, Pinia
- 后端：FastAPI, Python 3.10+, SQLAlchemy 2.0, Pydantic V2
- 模型：默认支持Hugging Face Transformers，可按需扩展
- 数据库：**MySQL** (已对接)

## 潜在应用场景

利用本框架，您可以快速构建以下应用：

1. **私有知识库问答系统**：集成向量数据库，实现基于企业内部文档的智能问答。
2. **多模态交互应用**：扩展后端能力，支持图像、音频等多种输入。
3. **垂直领域专家系统**：通过精巧的提示工程和模型微调，打造特定领域的专业顾问。
4. **自动化工作流工具**：集成外部API和自动化脚本，实现复杂的任务处理流程。
5. **AI协作平台**：增加用户认证和多租户系统，构建可供团队使用的AI工具。
6. **教育与培训平台**：结合知识库与AI助教，为特定领域（如化学、法律、医学）提供交互式学习体验。
