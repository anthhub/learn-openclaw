English | [中文](README.md)

# Learn OpenClaw 🦞🔒

> Master OpenClaw in 12 sessions from scratch — with a strong emphasis on security practices

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## Why This Project?

OpenClaw is the hottest open-source AI Agent framework of 2026 (330K+ stars), but existing learning resources have three major gaps:
1. **Security education is nearly absent** — The ClawHavoc supply chain attack affected 300K users, 20% of Skills were found to contain malicious code, and CVE-2026-25253 (CVSS 8.8) has had lasting impact
2. **No project-driven hands-on courses** — Existing tutorials are mostly docs/videos, lacking a "learn by building" experience
3. **Enterprise scenarios are uncovered** — Multi-tenancy, audit logs, compliance deployment, etc. are scattered everywhere

This project draws on the progressive teaching model of [learn-claude-code](https://github.com/shareAI-lab/learn-claude-code) (40K+ stars), introducing only one core mechanism per session, driven by runnable code and real-world scenarios.

## Core Philosophy

> "An Agent is a model, not a framework. Your job is to build a secure harness."

- **Progressive**: 12 sessions, from installation to enterprise security, one mechanism at a time
- **Security-first**: 4 out of 12 sessions focus on security (Skill auditing, CVE defense, sandboxing, enterprise compliance)
- **Code-driven**: Every session includes runnable TypeScript code, consistent with the OpenClaw ecosystem
- **Bilingual**: Documentation available in both Chinese and English

## Learning Path

### Phase 1: Getting Started (s01-s03) — Your First Lobster

| Session | Topic | Core Mechanism | Motto |
|---------|-------|----------------|-------|
| [s01](docs/en/s01.md) | First Look at OpenClaw | Installation, first conversation, Gateway architecture | "One lobster is enough to change the way you work" |
| [s02](docs/en/s02.md) | Connecting Message Channels | Channel system: WeChat/Feishu/DingTalk/Telegram | "An Agent needs ears and a mouth" |
| [s03](docs/en/s03.md) | Model Configuration | LLM Provider: DeepSeek/Qwen/Claude/GPT | "The lobster's brain is free to choose" |

### Phase 2: Expanding Capabilities (s04-s07) — Make Your Lobster Stronger

| Session | Topic | Core Mechanism | Motto |
|---------|-------|----------------|-------|
| [s04](docs/en/s04.md) | Skills System | ClawHub, installation, configuration, triggering | "Skills are the lobster's superpowers" |
| [s05](docs/en/s05.md) | Memory System | Memory, RAG, long-term memory | "An Agent without memory is just a parrot" |
| [s06](docs/en/s06.md) | MCP Protocol | MCP Server connection, tool registration | "MCP connects the lobster to everything" |
| [s07](docs/en/s07.md) | Skill Development | Creating custom Skills, Plugin SDK | "The best Skill is the one you write yourself" |

### Phase 3: Security Hardening (s08-s10) — 🔒 Protect Your Lobster

| Session | Topic | Core Mechanism | Motto |
|---------|-------|----------------|-------|
| [s08](docs/en/s08.md) | 🔒 Security Basics | Permission model, sandboxing, trust boundaries | "An undefended Agent is a ticking time bomb" |
| [s09](docs/en/s09.md) | 🔒 Skill Security Audit | ClawHavoc analysis, malicious Skill detection, VirusTotal scanning | "Audit before installing, or regret it later" |
| [s10](docs/en/s10.md) | 🔒 CVE Defense in Practice | CVE-2026-25253 reproduction and defense, Prompt Injection protection | "Know the attack to know the defense" |

### Phase 4: Production Deployment (s11-s12) — Lobster Goes Live

| Session | Topic | Core Mechanism | Motto |
|---------|-------|----------------|-------|
| [s11](docs/en/s11.md) | Docker Deployment | Docker Compose, K8s, reverse proxy, monitoring | "Running in dev doesn't count" |
| [s12](docs/en/s12.md) | 🔒 Enterprise Security Deployment | Multi-tenancy, RBAC, audit logs, GDPR/China compliance | "Enterprise-grade is more than adding another server" |

## Project Structure

```
learn-openclaw/
├── README.md                    # Project navigation (Chinese)
├── README-en.md                 # Project navigation (English)
├── agents/                      # Runnable code for each session
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
│   └── s_full.ts               # Comprehensive implementation (Capstone)
├── docs/
│   ├── zh/                     # Chinese docs
│   │   ├── s01.md ... s12.md
│   │   └── security-checklist.md
│   └── en/                     # English docs
│       └── s01.md ... s12.md
├── skills/                     # Custom Skill examples used in s07
│   ├── hello-skill/
│   │   └── SKILL.md
│   └── audit-skill/
│       └── SKILL.md
├── docker/                     # Deployment configs used in s11
│   ├── docker-compose.yml
│   └── Dockerfile
├── security/                   # Security reference materials
│   ├── clawhavoc-analysis.md   # ClawHavoc incident deep analysis
│   ├── cve-2026-25253.md       # CVE reproduction and defense
│   ├── skill-audit-guide.md    # Complete Skill audit guide
│   └── compliance-cn.md        # China compliance guide (CNCERT/PIPL)
├── .env.example
├── package.json
├── tsconfig.json
└── LICENSE
```

## Security Highlights 🔒

This project is the **first open-source course to systematically cover OpenClaw security**:

- **ClawHavoc Incident Deep Analysis**: How 1,184 malicious Skills poisoned ClawHub
- **CVE-2026-25253 Reproduction and Defense**: Full attack-defense coverage of a CVSS 8.8 RCE vulnerability
- **Skill Security Audit in Practice**: Using ClawGuard/ClawSecure/VirusTotal to detect malicious code
- **Prompt Injection Protection**: Identifying and defending against indirect injection attacks
- **China Compliance Guide**: Aligned with CNCERT security practice guidelines, PIPL, and Data Security Law

## Prerequisites

- Node.js 18+ and npm
- TypeScript (auto-installed via npm install)
- Docker (s11-s12)
- An LLM API Key (DeepSeek recommended for best cost-performance)

## Quick Start

```bash
git clone https://github.com/anthhub/learn-openclaw.git
cd learn-openclaw
npm install
cp .env.example .env
# Edit .env and fill in your API Key
npm run s01
```

## Reference Projects

- [learn-claude-code](https://github.com/shareAI-lab/learn-claude-code) — The structural inspiration for this project (40K+ stars)
- [hello-claw](https://github.com/datawhalechina/hello-claw) — A Chinese OpenClaw tutorial by Datawhale
- [claw0](https://github.com/shareAI-lab/claw0) — A course on underlying Agent principles built from scratch
- [awesome-claw-cn](https://github.com/anthhub/awesome-claw-cn) — Curated Chinese OpenClaw ecosystem resources
- [awesome-claw-opus](https://github.com/anthhub/awesome-claw-opus) — OpenClaw security/self-hosted/enterprise resources

## Contributing

PRs welcome! Especially:
- New security-related tutorials or case studies
- Chinese/English translation improvements
- New runnable code examples

## License

MIT
