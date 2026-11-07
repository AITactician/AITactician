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
- **Market intelligence tools** — trading analytics and prediction-market tooling (private; no public code yet)
- **Automation everywhere** — if I do it twice, an agent does it the third time

## 📊 Case studies

Three decisions from the estate I run, each with the evidence behind it.
Numbers are measured unless marked *estimate*.

### 1. Cutting a CI bill by fixing how jobs are billed

- **Problem.** GitHub Actions overage on one organization reached **$21.55 in October** (2026-10-22 billing read).
- **Decision.** GitHub bills every job at least one whole minute, so workflows split into many 10–20 second jobs paid 4–5 minutes per run. Each workflow now runs its checks as steps of one job, with the same required check name. Light jobs moved to GitHub's 1-CPU `ubuntu-slim` runner (a third of the Linux price). macOS now runs only when a Mac-only file changes.
- **Evaluation.** Billed minutes per run came from each job's start and end times, cross-checked against the usage API. One workflow went from **$0.108 a run to 0.67–1.33 Linux-equivalent minutes** on most commits. Moving to `slim` broke one repository's main branch; I moved it back 16 minutes later and wrote the defect up.
- **Deployment.** Eleven pull requests across six repositories, each merged on green required checks. Two self-hosted runners on the lab's own hardware followed for the remainder.
- **Number.** At September's volume the organization fits inside its 3,000 included minutes: about **1,870 a month, $0** (*estimate*).

### 2. Which security scanners can replace a paid tier

- **Problem.** A GitHub Advanced Security trial raised 22 code alerts and one secret alert. Keeping it costs about **$49 per committer per month**.
- **Decision.** Test the free tools against what the paid tier found before paying, and publish only fresh extracts rather than flipping private repositories to public.
- **Evaluation.** Semgrep and Bandit were rerun on the same commits CodeQL alerted on. Semgrep matched **1 of 15** alerts and Bandit **0 of 8** Python alerts. Across 11 repositories' full history, three secret scanners disagreed widely, and none flagged the one key GitHub's scanner did. The result is written up with the gaps it does not show: why the tools missed was not demonstrated.
- **Deployment.** Don't buy now. Fix and export the alerts, then move secrets scanning to a pre-commit hook plus a weekly full-history scan on self-hosted runners, with dependency alerts on in every repository.
- **Number.** **$0 extra a month**, with the paid option's measured advantage stated: 14 of 15 CodeQL alerts that no free configuration tested matched.

### 3. Choosing a web-search route for agents

- **Problem.** The agent gateway's search tool ran out of credits mid-test, and the free tiers rate-limited concurrent agents. Agents made **2,021 searches in 4.27 days** (about 14,200 a month).
- **Decision.** Fix the scoring rules before the runs: primary source first and current fact first. Then score five providers on 20 queries.
- **Evaluation.** Keyless Exa scored **86.4%**, the others 67.0–77.5%. After correcting for nine comparisons, **no pairwise gap was significant**, so availability, price and independent boards chose the first route instead. The test also showed what no search API found: a same-day release, and a niche issue only a keyword index returned.
- **Deployment.** Perplexity Fast first, keyless Exa second, Brave as fallback. For a release or an issue, go to the primary source with `gh`, because no search API found either test case.
- **Number.** About **$10 a month** at today's volume, against $60–90 for the measured winner.

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
