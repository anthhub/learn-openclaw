[English](README-en.md) | 中文

# Learn OpenClaw 🦞🔒

> 从零开始，12 节课掌握 OpenClaw — 特别强调安全实践

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## 为什么做这个项目？

OpenClaw 是 2026 年最火的开源 AI Agent 框架（330K+ stars），但现有学习资源存在三大缺口：
1. **安全教学几乎空白** — ClawHavoc 供应链攻击影响 30 万用户，20% 的 Skill 被发现含恶意代码，CVE-2026-25253 (CVSS 8.8) 影响深远
2. **缺少项目驱动的实战课程** — 现有教程多为文档/视频，缺乏"边学边造"的体验
3. **企业级场景无人覆盖** — 多租户、审计日志、合规部署等内容散落各处

本项目参考 [learn-claude-code](https://github.com/shareAI-lab/learn-claude-code)（40K+ stars）的渐进式教学模式，每节课只引入一个核心机制，并用可运行的代码和真实场景驱动学习。

## 核心理念

> "Agent 是模型，不是框架。你的工作是构建安全的套具（harness）。"

- **渐进式**：12 节课，从安装到企业安全，每次只学一个机制
- **安全优先**：4/12 课时聚焦安全（Skills 审计、CVE 防御、沙箱、企业合规）
- **代码驱动**：每节课包含可运行的 TypeScript 代码，与 OpenClaw 生态一致
- **中英双语**：文档支持中文和英文

## 学习路径

### Phase 1：入门（s01-s03）— 你的第一只龙虾

| Session | 主题 | 核心机制 | 格言 |
|---------|------|----------|------|
| [s01](docs/zh/s01.md) | 初见 OpenClaw | 安装、首次对话、Gateway 架构 | "一只龙虾足以改变你的工作方式" |
| [s02](docs/zh/s02.md) | 接入消息频道 | Channel 系统：微信/飞书/钉钉/Telegram | "Agent 需要耳朵和嘴巴" |
| [s03](docs/zh/s03.md) | 模型配置 | LLM Provider：DeepSeek/Qwen/Claude/GPT | "龙虾的大脑可以自由选择" |

### Phase 2：能力扩展（s04-s07）— 让龙虾更强大

| Session | 主题 | 核心机制 | 格言 |
|---------|------|----------|------|
| [s04](docs/zh/s04.md) | Skills 技能系统 | ClawHub、安装、配置、触发 | "Skills 是龙虾的超能力" |
| [s05](docs/zh/s05.md) | 记忆系统 | Memory、RAG、长期记忆 | "没有记忆的 Agent 只是一个复读机" |
| [s06](docs/zh/s06.md) | MCP 协议 | MCP Server 连接、工具注册 | "MCP 让龙虾连接万物" |
| [s07](docs/zh/s07.md) | Skill 开发 | 创建自定义 Skill、Plugin SDK | "最好的 Skill 是你自己写的" |

### Phase 3：安全加固（s08-s10）— 🔒 保护你的龙虾

| Session | 主题 | 核心机制 | 格言 |
|---------|------|----------|------|
| [s08](docs/zh/s08.md) | 🔒 安全基础 | 权限模型、沙箱、信任边界 | "不设防的 Agent 是定时炸弹" |
| [s09](docs/zh/s09.md) | 🔒 Skill 安全审计 | ClawHavoc 分析、恶意 Skill 识别、VirusTotal 扫描 | "安装前先审计，否则后悔莫及" |
| [s10](docs/zh/s10.md) | 🔒 CVE 防御实战 | CVE-2026-25253 复现与防御、Prompt Injection 防护 | "知攻方能知防" |

### Phase 4：生产部署（s11-s12）— 龙虾上线

| Session | 主题 | 核心机制 | 格言 |
|---------|------|----------|------|
| [s11](docs/zh/s11.md) | Docker 部署 | Docker Compose、K8s、反向代理、监控 | "开发环境能跑不算数" |
| [s12](docs/zh/s12.md) | 🔒 企业安全部署 | 多租户、RBAC、审计日志、GDPR/国内合规 | "企业级不只是多加一台服务器" |

## 项目结构

```
learn-openclaw/
├── README.md                    # 项目导航（本文件）
├── agents/                      # 每节课的可运行代码
│   ├── s01_first_claw.ts
│   ├── s02_channels.ts
│   ├── s03_models.ts
│   ├── s04_skills.ts
│   ├── s05_memory.ts
│   ├── s06_mcp.ts
│   ├── s07_skill_dev.ts
│   ├── s08_security_basics.ts
│   ├── s09_skill_audit.ts
│   ├── s10_cve_defense.ts
│   ├── s11_docker_deploy.ts
│   ├── s12_enterprise.ts
│   └── s_full.ts               # 综合实现（Capstone）
├── docs/
│   ├── zh/                     # 中文文档
│   │   ├── s01.md ... s12.md
│   │   └── security-checklist.md
│   └── en/                     # English docs
│       └── s01.md ... s12.md
├── skills/                     # s07 使用的自定义 Skill 示例
│   ├── hello-skill/
│   │   └── SKILL.md
│   └── audit-skill/
│       └── SKILL.md
├── docker/                     # s11 使用的部署配置
│   ├── docker-compose.yml
│   └── Dockerfile
├── security/                   # 安全专题资料
│   ├── clawhavoc-analysis.md   # ClawHavoc 事件深度分析
│   ├── cve-2026-25253.md       # CVE 复现与防御
│   ├── skill-audit-guide.md    # Skill 审计完全指南
│   └── compliance-cn.md        # 中国合规指南（CNCERT/PIPL）
├── .env.example
├── package.json
├── tsconfig.json
└── LICENSE
```

## 安全特色 🔒

本项目是**首个系统覆盖 OpenClaw 安全教学**的开源课程：

- **ClawHavoc 事件深度分析**：1,184 个恶意 Skill 如何投毒 ClawHub
- **CVE-2026-25253 复现与防御**：CVSS 8.8 RCE 漏洞的完整攻防
- **Skill 安全审计实战**：使用 ClawGuard/ClawSecure/VirusTotal 检测恶意代码
- **Prompt Injection 防护**：间接注入攻击的识别与防御
- **中国合规指南**：对标 CNCERT 安全实践指南、PIPL、数据安全法

## 前置要求

- Node.js 18+ 和 npm
- TypeScript（通过 npm install 自动安装）
- Docker（s11-s12）
- 一个 LLM API Key（推荐 DeepSeek，性价比最高）

## 快速开始

```bash
git clone https://github.com/anthhub/learn-openclaw.git
cd learn-openclaw
npm install
cp .env.example .env
# 编辑 .env 填入你的 API Key
npm run s01
```

## 参考项目

- [learn-claude-code](https://github.com/shareAI-lab/learn-claude-code) — 本项目的结构灵感来源（40K+ stars）
- [hello-claw](https://github.com/datawhalechina/hello-claw) — Datawhale 出品的中文 OpenClaw 教程
- [claw0](https://github.com/shareAI-lab/claw0) — 从零构建 Agent 的底层原理课程
- [awesome-claw-cn](https://github.com/anthhub/awesome-claw-cn) — 中文 OpenClaw 生态资源精选
- [awesome-claw-opus](https://github.com/anthhub/awesome-claw-opus) — OpenClaw 安全/自托管/企业资源

## 贡献

欢迎 PR！特别欢迎：
- 安全相关的新教程或案例
- 中文/英文翻译改进
- 新的可运行代码示例

## License

MIT
