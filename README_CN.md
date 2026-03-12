<div align="center">

<img src="docs/assets/logo.png" alt="Antigravity Workspace" width="200"/>

# Antigravity Workspace Template

**用于构建自主 AI 代理的生产级入门套件。**

*适用于任何 AI IDE · 任何 CLI · 任何 LLM*

语言: [English](README.md) | **中文** | [Español](README_ES.md)

[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)
[![Gemini](https://img.shields.io/badge/AI-Gemini_2.0_Flash-4285F4?style=for-the-badge&logo=google&logoColor=white)](https://ai.google.dev/)
[![OpenAI](https://img.shields.io/badge/OpenAI-Compatible-412991?style=for-the-badge&logo=openai&logoColor=white)](https://openai.com/)
[![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org/)

<br/>

<img src="https://img.shields.io/badge/Google_Antigravity-✓-4285F4?style=flat-square" alt="Antigravity"/>
<img src="https://img.shields.io/badge/Cursor-✓-000000?style=flat-square" alt="Cursor"/>
<img src="https://img.shields.io/badge/Windsurf-✓-06B6D4?style=flat-square" alt="Windsurf"/>
<img src="https://img.shields.io/badge/VS_Code_+_Copilot-✓-007ACC?style=flat-square" alt="VS Code"/>
<img src="https://img.shields.io/badge/Cline-✓-FF6B6B?style=flat-square" alt="Cline"/>
<img src="https://img.shields.io/badge/Aider-✓-8B5CF6?style=flat-square" alt="Aider"/>
<img src="https://img.shields.io/badge/Claude_Code-✓-D97757?style=flat-square" alt="Claude Code"/>
<img src="https://img.shields.io/badge/Gemini_CLI-✓-4285F4?style=flat-square" alt="Gemini CLI"/>
<img src="https://img.shields.io/badge/Codex-✓-412991?style=flat-square" alt="Codex"/>

</div>

<br/>

> **Clone → Rename → Prompt，即是工作流。**
>
> 在 AI IDE 如此丰富的今天，我希望企业级架构可以像三条命令一样简单。本模板在仓库中预埋了一套完整的**认知架构**——打开项目时，你的 IDE 不再只是编辑器，而是一位**懂行的架构师**。

---

## 🌍 全平台兼容

本模板**不绑定**任何特定 IDE，开箱即用于所有主流 AI 开发环境：

| 平台 | 工作方式 |
|:-----|:---------|
| **Google Antigravity** | 读取 `.antigravity/rules.md` 实现完整上下文感知 |
| **Cursor** | 读取 `.cursorrules` 获取项目级规则 |
| **Windsurf / VS Code + Copilot** | 利用 `.context/` 文件注入知识 |
| **Claude Code** | 读取 `AGENTS.md` + `CONTEXT.md` 获取项目规范 |
| **Gemini CLI** | 读取 `AGENTS.md` + `.context/` 注入知识 |
| **Codex (OpenAI)** | 读取 `AGENTS.md` + 目录约定 |
| **Cline / Aider** | 借助 `CONTEXT.md` 和目录约定 |
| **任何 OpenAI 兼容 Agent** | `src/tools/` 自动发现工具，标准 Python 入口 |

秘诀：架构编码在**文件**中，而不是 IDE 插件里。任何能读取项目文件的 Agent 都能受益。

---

## ⚡ 快速开始

### 自动安装（推荐）

**Linux / macOS：**
```bash
# 1. 克隆模板
git clone https://github.com/study8677/antigravity-workspace-template.git my-project
cd my-project

# 2. 运行安装脚本
chmod +x install.sh
./install.sh

# 3. 配置 API 密钥
nano .env

# 4. 运行 Agent
source venv/bin/activate
python src/agent.py
```

**Windows：**
```cmd
# 1. 克隆模板
git clone https://github.com/study8677/antigravity-workspace-template.git my-project
cd my-project

# 2. 运行安装脚本
install.bat

# 3. 配置 API 密钥（notepad .env）

# 4. 运行 Agent
python src/agent.py
```

<details>
<summary><b>📋 手动安装</b></summary>

```bash
git clone https://github.com/study8677/antigravity-workspace-template.git my-project
cd my-project
python3 -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
pip install -r requirements.txt
cp .env.example .env      #（如有）或手动创建 .env
nano .env
python src/agent.py
```
</details>

**就这么简单！** IDE 会自动加载配置，你可以直接开始提示。

---

## 🎯 这是什么？

这并**不**是另一个 LangChain 封装。它是一个极简、透明的工作区，用于构建 AI Agent：

| 特性 | 描述 |
|:-----|:-----|
| 🧠 **无限记忆** | 递归摘要自动压缩上下文 |
| 🧠 **真实思考** | 行动前使用思维链 (CoT) 进行"深度思考" |
| 🎓 **技能系统** | `src/skills/` 下的模块化能力，自动加载 |
| 🛠️ **通用工具** | Python 函数放入 `src/tools/` 即可自动发现 |
| 📚 **自动上下文** | 向 `.context/` 添加文件即自动注入提示 |
| 🔌 **MCP 支持** | 连接 GitHub、数据库、文件系统、自定义服务器 |
| 🤖 **Swarm Agent** | Router-Worker 模式的多 Agent 编排 |
| ⚡ **Gemini 原生** | 为 Gemini 2.0 Flash 做了优化 |
| 🌐 **LLM 无关** | 支持 OpenAI、Azure、Ollama 或任何兼容 API |
| 📂 **Artifact-First** | 约定优先的计划、日志、证据工作流 |
| 🔒 **沙盒执行** | 可选 local / microsandbox 执行环境 |

---

## 🏗️ 项目结构

```
src/
├── agent.py           # Agent 主循环
├── memory.py          # JSON 记忆管理
├── mcp_client.py      # MCP 集成
├── swarm.py           # 多 Agent 编排
├── agents/            # 专家型 Agent
├── tools/             # 自定义工具（自动发现）
└── skills/            # 模块化技能（自动加载）

.context/             # 知识库（自动注入）
.antigravity/         # Antigravity 规则
.cursorrules          # Cursor 规则
artifacts/            # 输出与证据
```

---

## 💡 30 秒创建一个工具

```python
# src/tools/my_tool.py
def analyze_sentiment(text: str) -> str:
    """Analyzes the sentiment of given text."""
    return "positive" if len(text) > 10 else "neutral"
```

**重启 Agent。** 完成！工具已可用于任何 AI IDE。

---

## 🎓 用 Skill 初始化新仓库

内置 `agent-repo-init` skill 支持两种模式：
- `quick`：最小化干净脚手架
- `full`：脚手架 + 运行时默认配置

```bash
python skills/agent-repo-init/scripts/init_project.py \
  --project-name my-new-agent \
  --destination-root /absolute/path/for/new/projects \
  --mode quick
```

<details>
<summary><b>Full 模式示例</b></summary>

```bash
python skills/agent-repo-init/scripts/init_project.py \
  --project-name my-new-agent \
  --destination-root /absolute/path/for/new/projects \
  --mode full --llm-provider openai --enable-mcp --disable-swarm \
  --sandbox-runtime microsandbox --init-git
```
</details>

---

## 🔌 MCP 集成

连接外部工具：

```json
{
  "servers": [
    {
      "name": "github",
      "transport": "stdio",
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-github"],
      "enabled": true
    }
  ]
}
```

---

## 🤖 多 Agent Swarm

分解复杂任务：

```python
from src.swarm import SwarmOrchestrator

swarm = SwarmOrchestrator()
result = swarm.execute("构建并审查一个计算器")
```

Swarm 自动路由到 Coder、Reviewer、Researcher Agent，综合结果并提供可检查的消息日志。

---

## 🔒 沙盒配置

| 变量 | 默认值 | 选项 |
|:-----|:------|:-----|
| `SANDBOX_TYPE` | `local` | `local` · `microsandbox` |
| `SANDBOX_TIMEOUT_SEC` | `30` | 秒 |
| `SANDBOX_MAX_OUTPUT_KB` | `10` | KB |

<details>
<summary><b>Microsandbox 额外变量</b></summary>

| 变量 | 默认值 |
|:-----|:------|
| `MSB_SERVER_URL` | `http://127.0.0.1:5555` |
| `MSB_API_KEY` | （可选） |
| `MSB_IMAGE` | `microsandbox/python` |
| `MSB_CPU_LIMIT` | `1.0` |
| `MSB_MEMORY_MB` | `512` |
</details>

---

## 📚 文档

| 语言 | 链接 |
|:-----|:-----|
| 🇬🇧 English | **[`/docs/en/`](docs/en/)** |
| 🇨🇳 中文 | **[`/docs/zh/`](docs/zh/)** |
| 🇪🇸 Español | **[`/docs/es/`](docs/es/)** |

---

## ✅ 项目进度

- ✅ 阶段 1-7：基础、DevOps、记忆、工具、Swarm、发现
- ✅ 阶段 8：MCP 集成（已完全实现）
- 🚀 阶段 9：企业核心（进行中）

详见 [Roadmap](docs/zh/ROADMAP.md)。

---

## 🤝 贡献

创意也是贡献！欢迎在 [issue](https://github.com/study8677/antigravity-workspace-template/issues) 中报告 bug、提出建议或提交架构方案。

## 👥 贡献者

- [@devalexanderdaza](https://github.com/devalexanderdaza) — 首位贡献者。实现了演示工具、增强了 Agent 功能、提出了 "Agent OS" 路线图，并完成 MCP 集成。
- [@Subham-KRLX](https://github.com/Subham-KRLX) — 添加了动态工具与上下文加载（修复 #4），以及多 Agent 集群协议（修复 #6）。

## ⭐ Star History

[![Star History Chart](https://api.star-history.com/svg?repos=study8677/antigravity-workspace-template&type=Date)](https://star-history.com/#study8677/antigravity-workspace-template&Date)

## 📄 许可证

MIT License. 详见 [LICENSE](LICENSE)。

---

<div align="center">

**[📚 查看完整文档 →](docs/zh/)**

*为 AI 原生开发时代而构建 ❤️*

</div>
