# Draft only: sources for the case-study numbers

Delete this file before the README goes live; Tyler decides whether any citation stays public. All paths are in the private repository TWayneLabs/ai-orchestrator unless a PR is named.

## 1. CI bill
| Number | Source |
|---|---|
| $21.55 October overage | `research/R135-github-portfolio-and-scanning.md` §1, "Cost today" (billing usage API, 2026-10-22) |
| $0.108 a run to 0.67–1.33 Linux-equivalent minutes | `coordination/receipts/2026-10/actions-cost-20261006T0627Z.md`, "Before → after" table, ai-config row |
| 1,870 minutes a month, $0 (estimate) | same receipt, "Outcome in plain English" |
| Eleven PRs, six repositories | same receipt, "Pull requests" table: knowledge-vault #138, knowledge-os #44, dotfiles #37, ai-systems #407 and #409, ai-config #83 and #84, homelab-infra #432 and #435 |
| Slim broke main, moved back after 16 minutes | same receipt, ai-systems row ("Defect found") |
| Two self-hosted runners | homelab-infra PR #603 |

## 2. Scanners
| Number | Source |
|---|---|
| $49 per committer a month | `research/R135-github-portfolio-and-scanning.md` §1 ($30 + $19; vendor page, marked RC in R135, not re-read) |
| 22 alerts | ai-config#131 as cited in R135 §3.2 |
| Semgrep 1 of 15, Bandit 0 of 8 | R135 §3.2 table; evidence in `research/R135-data/scan/` |
| 11 repositories, one key no free tool flagged | R135 §3.3 |
| 14 of 15 | R135 §1, "The paid option" |
| Decision (don't buy) and answer | R135 §1; Tyler's answer "Follow R135: drop it, free tools" on ai-orchestrator#330 (2026-11-02) |

## 3. Search
| Number | Source |
|---|---|
| 2,021 searches in 4.27 days, ~14,200 a month | `research/R112-search-tools-20261008.md` §0 item 10 |
| 86.4%, 67.0–77.5%, no gap significant | same, §0 item 1 |
| ~$10 a month, $60–90 | same, §0 items 2 and 10 |
| Route order in use | `coordination/deliveries/2026-10/worker-brief-footer-p059-20261003.md`, line 13 (R112, log 803) |

Caveats carried from the sources: R112 is a 20-query exploratory test judged by rules a Claude model wrote; the R135 scanner comparison covers 15 alerts from one CodeQL run.
