# 🐮 咚咚家族（Dong Labs）

> AI-Native CLI 工具集，让生活更有序

---

## 🎯 我们是谁

**咚咚家族**是一系列 AI-Native CLI 工具，帮助咕咚和他的朋友们管理日常生活、工作和项目。

---

## 🛠️ 工具列表

### 核心工具

| 工具 | 包名 | CLI 命令 | 功能 |
|------|------|----------|------|
| **记咚咚** | `dong-log` | `dong-log` | 日志管理 |
| **读咚咚** | `dong-read` | `dong-read` | 知识管理 |
| **仓咚咚** | `dong-cang` | `dong-cang` | 财务管理 |
| **思咚咚** | `dong-think` | `dong-think` | 灵感管理 |
| **事咚咚** | `dong-dida` | `dong-dida` | 待办管理 |
| **到期咚** | `dong-expire` | `dong-expire` | 到期日管理 |
| **密码咚** | `dong-pass` | `dong-pass` | 账号密码管理 |
| **时间咚** | `dong-timeline` | `dong-timeline` | 关键节点管理 |

---

## 🚀 快速开始

### 安装

```bash
# 安装所有工具
pipx install dong-log
pipx install dong-read
pipx install dong-cang
pipx install dong-think
pipx install dong-dida
pipx install dong-expire
pipx install dong-pass
pipx install dong-timeline
```

### 初始化

```bash
# 初始化数据库
dong-log init
dong-read init
dong-cang init
dong-think init
dong-dida init
dong-expire init
dong-pass init
dong-timeline init
```

---

## 💡 设计理念

### 1. 统一命名

所有 CLI 工具都使用 `dong-xxx` 命名格式：

```bash
dong-log      # 记咚咚
dong-read     # 读咚咚
dong-cang     # 仓咚咚
...
```

### 2. 统一数据目录

所有数据存储在 `~/.dong/` 目录：

```
~/.dong/
├── log.db       # 日志
├── read.db      # 知识
├── cang.db      # 财务
├── think.db     # 灵感
├── dida.db      # 待办
├── expire.db    # 到期日
├── accounts.db  # 账号密码
└── timeline.db  # 时间轴
```

### 3. AI 友好

所有命令都支持 JSON 输出，方便 AI 解析：

```bash
dong-log add "今天完成了什么"
# {"success": true, "data": {"id": 1, "content": "今天完成了什么"}}
```

### 4. 命令一致性

所有工具都遵循相同的命令模式：

```bash
dong-xxx init           # 初始化
dong-xxx add "内容"     # 添加
dong-xxx list           # 列出
dong-xxx get <id>       # 获取
dong-xxx update <id>    # 更新
dong-xxx delete <id>    # 删除
dong-xxx search "关键词" # 搜索
dong-xxx stats          # 统计
```

---

## 🎨 时间维度

| 工具 | 时间维度 | 用途 |
|------|---------|------|
| **timeline** | 过去 | 关键节点 |
| **log** | 现在 | 日常日志 |
| **think** | 现在 | 灵感想法 |
| **dida** | 未来 | 待办事项 |
| **expire** | 过去/未来 | 到期日 |

---

## 🏗️ 核心库

### dong-core

所有咚咚工具的核心依赖：

```python
from dong.db import Database, SchemaManager
from dong import json_output, DongError

class LogDatabase(Database):
    @classmethod
    def get_name(cls) -> str:
        return "log"
```

---

## 📊 统计

- **工具数量**：8 个
- **总下载量**：持续增长中
- **维护者**：咕咚
- **开源协议**：MIT

---

## 🔗 链接

- **GitHub 组织**：https://github.com/dong-labs
- **PyPI 组织**：https://pypi.org/user/gudongtx/
- **作者博客**：https://blog.gudong.site

---

## 🤝 贡献

欢迎贡献！请查看各项目的 CONTRIBUTING.md。

---

## 📝 许可证

所有项目均采用 MIT 许可证。

---

## 🐮 关于咚咚家族

咚咚家族是由咕咚创建的一系列 AI-Native CLI 工具，旨在通过命令行工具管理日常生活、工作和项目。

**核心理念**：
- **简洁**：CLI 工具，一行命令搞定
- **统一**：命名、数据目录、命令风格统一
- **AI 友好**：JSON 输出，方便 AI 解析
- **本地优先**：数据存储在本地，不依赖云端

---

*一家人整整齐齐！* 🐮💻✨
