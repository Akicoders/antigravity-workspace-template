<div align="center">

<img src="docs/assets/logo.png" alt="Antigravity Workspace" width="200"/>

# Antigravity Workspace Template

**Production-grade starter kit for autonomous AI agents.**

*Works with any AI IDE · Any CLI · Any LLM*

Language: **English** | [中文](README_CN.md) | [Español](README_ES.md)

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

> **Clone → Rename → Prompt. That's the workflow.**
>
> In a world full of AI IDEs, I want enterprise-grade architecture to be as simple as three commands. This template pre-embeds a complete **cognitive architecture** in the repo—when you open it, your IDE stops being an editor and becomes an **industry-savvy architect**.

---

## 🌍 Universal Compatibility

This template is **not** tied to any specific IDE. It works everywhere:

| Platform | How It Works |
|:---------|:-------------|
| **Google Antigravity** | Reads `.antigravity/rules.md` for full context awareness |
| **Cursor** | Reads `.cursorrules` for project-level rules |
| **Windsurf / VS Code + Copilot** | Uses `.context/` files for knowledge injection |
| **Claude Code** | Reads `AGENTS.md` + `CONTEXT.md` for project conventions |
| **Gemini CLI** | Reads `AGENTS.md` + `.context/` for knowledge injection |
| **Codex (OpenAI)** | Reads `AGENTS.md` + directory conventions |
| **Cline / Aider** | Leverages `CONTEXT.md` + directory conventions |
| **Any OpenAI-compatible agent** | Auto-discovered tools in `src/tools/`, standard Python entry |

The secret: architecture is encoded in **files**, not in IDE-specific plugins. Any agent that reads project files can benefit.

---

## ⚡ Quick Start

### Automated Installation (Recommended)

**Linux / macOS:**
```bash
# 1. Clone the template
git clone https://github.com/study8677/antigravity-workspace-template.git my-project
cd my-project

# 2. Run the installer
chmod +x install.sh
./install.sh

# 3. Configure your API keys
nano .env

# 4. Run the agent
source venv/bin/activate
python src/agent.py
```

**Windows:**
```cmd
# 1. Clone the template
git clone https://github.com/study8677/antigravity-workspace-template.git my-project
cd my-project

# 2. Run the installer
install.bat

# 3. Configure your API keys (notepad .env)

# 4. Run the agent
python src/agent.py
```

<details>
<summary><b>📋 Manual Installation</b></summary>

```bash
git clone https://github.com/study8677/antigravity-workspace-template.git my-project
cd my-project
python3 -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt
cp .env.example .env      # (if available) or create .env manually
nano .env
python src/agent.py
```
</details>

**That's it!** The IDE auto-loads configuration and you're ready to prompt.

---

## 🎯 What Is This?

This is **not** another LangChain wrapper. It's a minimal, transparent workspace for building AI agents that:

| Feature | Description |
|:--------|:------------|
| 🧠 **Infinite Memory** | Recursive summarization compresses context automatically |
| 🧠 **True Thinking** | "Deep Think" step using Chain-of-Thought before acting |
| 🎓 **Skills System** | Modular capabilities in `src/skills/` with auto-loading |
| 🛠️ **Universal Tools** | Drop Python functions in `src/tools/` → auto-discovered |
| 📚 **Auto Context** | Add files to `.context/` → auto-injected into prompts |
| 🔌 **MCP Support** | Connect GitHub, databases, filesystems, custom servers |
| 🤖 **Swarm Agents** | Multi-agent orchestration with Router-Worker pattern |
| ⚡ **Gemini Native** | Optimized for Gemini 2.0 Flash |
| 🌐 **LLM Agnostic** | Use OpenAI, Azure, Ollama, or any compatible API |
| 📂 **Artifact-First** | Convention-first workflow for plans, logs, and evidence |
| 🔒 **Sandbox** | Configurable code execution (local / microsandbox) |

---

## 🏗️ Project Structure

```
src/
├── agent.py           # Main agent loop
├── memory.py          # JSON memory manager
├── mcp_client.py      # MCP integration
├── swarm.py           # Multi-agent orchestration
├── agents/            # Specialist agents
├── tools/             # Your custom tools (auto-discovered)
└── skills/            # Modular skills (auto-loaded)

.context/             # Knowledge base (auto-injected)
.antigravity/         # Antigravity rules
.cursorrules          # Cursor rules
artifacts/            # Outputs & evidence
```

---

## 💡 Build a Tool in 30 Seconds

```python
# src/tools/my_tool.py
def analyze_sentiment(text: str) -> str:
    """Analyzes the sentiment of given text."""
    return "positive" if len(text) > 10 else "neutral"
```

**Restart the agent.** Done! The tool is now available to any AI IDE.

---

## 🎓 Initialize a New Repo with Skill

The built-in `agent-repo-init` skill supports two modes:
- `quick`: minimal clean scaffold
- `full`: scaffold + runtime profile defaults (`.env`, mission, context profile, init report)

```bash
python skills/agent-repo-init/scripts/init_project.py \
  --project-name my-new-agent \
  --destination-root /absolute/path/for/new/projects \
  --mode quick
```

<details>
<summary><b>Full mode example</b></summary>

```bash
python skills/agent-repo-init/scripts/init_project.py \
  --project-name my-new-agent \
  --destination-root /absolute/path/for/new/projects \
  --mode full --llm-provider openai --enable-mcp --disable-swarm \
  --sandbox-runtime microsandbox --init-git
```
</details>

---

## 🔌 MCP Integration

Connect to external tools seamlessly:

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

## 🤖 Multi-Agent Swarm

Decompose complex tasks automatically:

```python
from src.swarm import SwarmOrchestrator

swarm = SwarmOrchestrator()
result = swarm.execute("Build and review a calculator")
```

The swarm automatically routes to Coder, Reviewer, and Researcher agents, synthesizes results, and exposes logs via `get_message_log()`.

---

## 🔒 Sandbox Configuration

| Variable | Default | Options |
|:---------|:--------|:--------|
| `SANDBOX_TYPE` | `local` | `local` · `microsandbox` |
| `SANDBOX_TIMEOUT_SEC` | `30` | seconds |
| `SANDBOX_MAX_OUTPUT_KB` | `10` | KB |

<details>
<summary><b>Microsandbox extra variables</b></summary>

| Variable | Default |
|:---------|:--------|
| `MSB_SERVER_URL` | `http://127.0.0.1:5555` |
| `MSB_API_KEY` | (optional) |
| `MSB_IMAGE` | `microsandbox/python` |
| `MSB_CPU_LIMIT` | `1.0` |
| `MSB_MEMORY_MB` | `512` |
</details>

---

## 📚 Documentation

| Language | Link |
|:---------|:-----|
| 🇬🇧 English | **[`/docs/en/`](docs/en/)** |
| 🇨🇳 中文 | **[`/docs/zh/`](docs/zh/)** |
| 🇪🇸 Español | **[`/docs/es/`](docs/es/)** |

---

## ✅ Progress

- ✅ Phase 1-7: Foundation, DevOps, Memory, Tools, Swarm, Discovery
- ✅ Phase 8: MCP Integration (fully implemented)
- 🚀 Phase 9: Enterprise Core (in progress)

See [Roadmap](docs/en/ROADMAP.md) for details.

---

## 🤝 Contributing

Ideas are contributions too! Open an [issue](https://github.com/study8677/antigravity-workspace-template/issues) to report bugs, suggest features, or propose architecture.

## 👥 Contributors

- [@devalexanderdaza](https://github.com/devalexanderdaza) — First contributor. Implemented demo tools, enhanced agent functionality, proposed the "Agent OS" roadmap, and completed MCP integration.
- [@Subham-KRLX](https://github.com/Subham-KRLX) — Added dynamic tools and context loading (Fixes #4) and the multi-agent cluster protocol (Fixes #6).

## ⭐ Star History

[![Star History Chart](https://api.star-history.com/svg?repos=study8677/antigravity-workspace-template&type=Date)](https://star-history.com/#study8677/antigravity-workspace-template&Date)

## 📄 License

MIT License. See [LICENSE](LICENSE) for details.

---

<div align="center">

**[📚 Explore Full Documentation →](docs/en/)**

*Built with ❤️ for the AI-native development era*

</div>
