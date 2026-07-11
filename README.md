<div align="center">

# Hey, I'm Twayne 👋

**AI-first builder · solo entrepreneur · homelab operator**

I ship products and automation with natural language at the wheel — AI agents write the code,
rigorous pipelines keep it honest.

[![GitHub](https://img.shields.io/badge/GitHub-AITactician-181717?logo=github)](https://github.com/AITactician)
[![Org](https://img.shields.io/badge/Org-TWayneLabs-0A66C2?logo=githubsponsors&logoColor=white)](https://github.com/TWayneLabs)
![Location](https://img.shields.io/badge/Base-Phoenix%2C%20AZ-orange)

</div>

---

## 🚀 What I build

- **AI agent systems** — multi-agent teams (research, content, ops) running on self-hosted
  infrastructure, orchestrated from a single M4 Max cockpit
- **Market intelligence tools** — trading analytics, arbitrage scanners, and prediction-market
  tooling ([Polytrader](https://github.com/AITactician/Polytrader),
  [Trading-Platform](https://github.com/AITactician/Trading-Platform))
- **Automation everywhere** — if I do it twice, an agent does it the third time

## 🏗️ How I work

**Vibe coding, engineered.** Natural language → AI agents → shipped code — but wrapped in the
discipline of a DevOps pipeline:

- Every commit passes a **gitleaks secrets gate** before an AI writes the message and ships it
- Dotfiles + machine config fully reproducible via **chezmoi** (secrets live in Proton Pass,
  never in git)
- Infrastructure as code: **Ansible + Terraform + Docker Compose** across the fleet

## 🖥️ The lab

A 5-node homelab doing real work (IaC in [TWayneLabs](https://github.com/TWayneLabs)):

| Node | Role |
|------|------|
| `ai-01` · RTX 3090 | Local LLM inference (Ollama), agent runtime, MCP gateway |
| `pi-watch` | Observability — Grafana · Prometheus · Loki · AdGuard |
| `pi-auto` | Home Assistant + n8n automation |
| `zb1` / `zb2` | Storage (Immich, OpenCloud) · services hub (Authentik, NetBox, LiteLLM, n8n) |

UniFi network, VLAN-segmented, Tailscale mesh, CrowdSec at the edge.

## 🧰 Stack

![TypeScript](https://img.shields.io/badge/-TypeScript-3178C6?logo=typescript&logoColor=white)
![Next.js](https://img.shields.io/badge/-Next.js-000000?logo=nextdotjs)
![Python](https://img.shields.io/badge/-Python-3776AB?logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/-FastAPI-009688?logo=fastapi&logoColor=white)
![Docker](https://img.shields.io/badge/-Docker-2496ED?logo=docker&logoColor=white)
![Ansible](https://img.shields.io/badge/-Ansible-EE0000?logo=ansible)
![Terraform](https://img.shields.io/badge/-Terraform-844FBA?logo=terraform&logoColor=white)
![Claude](https://img.shields.io/badge/-Claude-D97757?logo=anthropic&logoColor=white)

<div align="center">

![Stats](https://github-readme-stats.vercel.app/api?username=AITactician&show_icons=true&theme=tokyonight&hide_border=true&count_private=true)

</div>
