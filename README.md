# 古诗知识图谱系统

这是一个基于知识图谱的古诗问答系统，使用Flask框架开发，集成了Neo4j图数据库和MySQL数据库，提供丰富的古诗相关查询和交互功能。

## 功能特性

- 古诗创作：支持用户创作古诗
- 古诗问答：智能回答关于古诗的问题
- 诗人信息查询：查询诗人的生平、作品等信息
- 古诗查询：按朝代、作者、名称等条件查询古诗
- 知识图谱可视化：展示诗人、古诗、朝代之间的关系
- 智能对话：支持自然语言交互的问答系统

## 技术栈

- 后端框架：Flask
- 数据库：
  - Neo4j（图数据库）
  - MySQL（关系型数据库）
- 前端技术：HTML, CSS, JavaScript
- 自然语言处理：自定义问答系统

## 安装说明

1. 环境要求：
   - Python 3.x
   - Neo4j 数据库
   - MySQL 数据库

2. 安装依赖：
   ```bash
   pip install flask
   pip install py2neo
   pip install pandas
   ```

3. 数据库配置：
   - 配置Neo4j数据库连接（默认地址：http://localhost:7474）
   - 配置MySQL数据库连接

4. 启动应用：
   ```bash
   python app.py
   ```

## 项目结构

```
.
├── app.py                 # 主应用文件
├── chatbot_graph.py       # 问答系统核心
├── question_classifier.py # 问题分类器
├── question_parser.py     # 问题解析器
├── answer_search.py       # 答案搜索
├── templates/            # HTML模板
├── static/              # 静态资源
├── utils/               # 工具函数
└── dict/                # 数据字典
```

## 使用说明

1. 访问首页：`http://localhost:5000`
2. 主要功能入口：
   - 古诗创作：`/tz_create_poem`
   - 古诗问答：`/tz_chat_poem`
   - 诗人查询：`/author/<name>`
   - 古诗查询：`/tz_find_poem/<name>`

## API接口

系统提供丰富的API接口，包括：
- 诗人信息查询
- 古诗内容查询
- 朝代信息查询
- 关系图谱查询
- 智能问答接口

## 注意事项

1. 确保Neo4j和MySQL服务正常运行
2. 首次使用需要导入基础数据
3. 建议使用Chrome或Firefox浏览器访问

## 贡献指南

欢迎提交Issue和Pull Request来帮助改进项目。

## 许可证

MIT License 