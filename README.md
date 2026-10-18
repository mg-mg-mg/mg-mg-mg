<picture>
  <source media="(max-width: 600px) and (prefers-color-scheme: dark)" srcset="assets/banner-dark-mobile.svg">
  <source media="(max-width: 600px)" srcset="assets/banner-light-mobile.svg">
  <source media="(prefers-color-scheme: dark)" srcset="assets/banner-dark.svg">
  <img alt="Mingyun Chae — Founder of TriAstra. Senior Backend & AI Agent Platform Engineer. 776 TriAstra PRs merged in the last 7 days; approximately 10 AI agent roles and 100+ peak concurrent OMP coding agents, excluding Aside. 7 open-source fixes merged upstream, 4 hackathon first places, and US and Korean patent registrations. Snapshot: October 18, 2026; agent figures approximate from OMP logs." src="assets/banner-light.svg" width="100%">
</picture>

<p align="center">
  <a href="https://www.linkedin.com/in/mg-chae/"><img alt="LinkedIn: mg-chae" src="https://img.shields.io/badge/LinkedIn-mg--chae-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"></a>
  <a href="mailto:coalsrbs7@gmail.com"><img alt="Email" src="https://img.shields.io/badge/Email-coalsrbs7%40gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white"></a>
  <a href="https://mg-mg-mg.github.io/agentic-engineering/"><img alt="Engineering case study" src="https://img.shields.io/badge/Case_study-Agentic_engineering-24292F?style=for-the-badge&logo=github&logoColor=white"></a>
  <a href="https://triastra.ai"><img alt="TriAstra" src="https://img.shields.io/badge/Product-TriAstra-5B4BDB?style=for-the-badge"></a>
  <br>
  <img alt="Open to remote opportunities and relocation" src="https://img.shields.io/badge/Open_to-remote_%26_relocation-2EA44F?style=flat-square">
  <img alt="Based in Seoul, South Korea" src="https://img.shields.io/badge/Based_in-Seoul%2C_KR-6E7781?style=flat-square">
</p>

<p align="center">
  <img alt="Building TriAstra solo with an AI agent team. Making the tools behind AI agents reliable. Incidents become automated guardrails." src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=20&duration=3200&pause=900&color=8B7CF6&center=true&vCenter=true&width=900&lines=Building+TriAstra+solo+with+an+AI+agent+team;Making+the+tools+behind+AI+agents+reliable;Incidents+become+automated+guardrails">
</p>

### Building

**[TriAstra](https://triastra.ai)** — a multilingual product I build and operate as a solo engineer with an AI agent team: Rust services, web and mobile clients, and a ChatGPT integration.

<div align="center">

| Registered users | Languages | Rust server-library tests | Merged PRs (7 days · 30 days) |
| :---: | :---: | :---: | :---: |
| **1,700+** | **7** | **3,635** | **776 · 1,051** |

</div>

<sub>Merged PRs: product repository, counted October 18, 2026, all authors including bots. User and Rust server-library test figures are October 15–17, 2026 snapshots.</sub>

[How the agent team works →](https://mg-mg-mg.github.io/agentic-engineering/)

### Reliability log

| Incident | Guardrail |
| --- | --- |
| A release-path change merged before its required verification evidence was recorded | Recorded the miss without backdating, completed the evidence afterwards, and made the merge tool refuse release-path changes without it |
| Independent review reproduced cleanup races that could delete a replaced file | Fixed before merge with atomic quarantine rename and identity/content verification |
| Production build sizing | Budgeted 32 GB; measured a sampled 14.7 GB peak RSS and zero swap during one build, not a universal capacity guarantee |
| A test fixture most likely inherited a Git hook's `GIT_*` environment and flipped `core.bare` in the shared repository | Fixed with isolated Git environments; the same bug class is proposed upstream in [Flutter #194429](https://github.com/flutter/flutter/pull/194429) (open) |

<sub>Private-operation accounts, not publicly reproducible incident records. [Methods, limits and current practice →](https://mg-mg-mg.github.io/agentic-engineering/)</sub>

### Open source

Fixes for problems I hit while running coding agents on real work.

**7 merged PRs** across [oh-my-pi](https://github.com/can1357/oh-my-pi) and [jcode](https://github.com/1jehuang/jcode), including shell execution, agent coordination and Korean IME input; **5 open proposals** across those projects, OpenTelemetry Rust, ts-rs and Flutter. Counted October 18, 2026.

| Project | Fix | Status |
| --- | --- | :---: |
| [oh-my-pi](https://github.com/can1357/oh-my-pi)<br>![stars](https://img.shields.io/github/stars/can1357/oh-my-pi?style=flat-square&logo=github&label=%E2%98%85&color=30363D) | Agent replies sent over messaging are acknowledged instead of reported as “no output.” | [![Merged](https://img.shields.io/badge/merged-8250DF?style=flat-square&logo=github&logoColor=white)](https://github.com/can1357/oh-my-pi/pull/15834) |
| [jcode](https://github.com/1jehuang/jcode)<br>![stars](https://img.shields.io/github/stars/1jehuang/jcode?style=flat-square&logo=github&label=%E2%98%85&color=30363D) | Contiguous typing, including Korean IME input, undoes in one step. | [![Merged](https://img.shields.io/badge/merged-8250DF?style=flat-square&logo=github&logoColor=white)](https://github.com/1jehuang/jcode/pull/1714) |
| [OpenTelemetry Rust](https://github.com/open-telemetry/opentelemetry-rust)<br>![stars](https://img.shields.io/github/stars/open-telemetry/opentelemetry-rust?style=flat-square&logo=github&label=%E2%98%85&color=30363D) | A failed export is no longer hidden by a later successful batch during a flush. | [![Open](https://img.shields.io/badge/open-1F883D?style=flat-square&logo=github&logoColor=white)](https://github.com/open-telemetry/opentelemetry-rust/pull/3791) |
| [Flutter](https://github.com/flutter/flutter)<br>![stars](https://img.shields.io/github/stars/flutter/flutter?style=flat-square&logo=github&label=%E2%98%85&color=30363D) | Keep Flutter SDK Git queries from inheriting a Git hook’s repository environment. | [![Open](https://img.shields.io/badge/open-1F883D?style=flat-square&logo=github&logoColor=white)](https://github.com/flutter/flutter/pull/194429) |

[All contributions →](CONTRIBUTIONS.md)

### Stack

<p align="left">
  <a href="#stack"><img alt="Rust, TypeScript, Python, PostgreSQL, Redis, Kafka, AWS, GCP, Cloudflare, Terraform, Kubernetes" src="https://skillicons.dev/icons?i=rust,ts,py,postgres,redis,kafka,aws,gcp,cloudflare,terraform,kubernetes&perline=11"></a>
</p>

<sub>Rust · TypeScript · Python · PostgreSQL · Redis · Kafka · AWS · GCP · Cloudflare · Terraform · Kubernetes</sub>

### GitHub activity

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://streak-stats.demolab.com?user=mg-mg-mg&theme=github-dark-blue&hide_border=true&date_format=M%20j%5B%2C%20Y%5D">
    <img alt="GitHub contribution streak for mg-mg-mg" src="https://streak-stats.demolab.com?user=mg-mg-mg&theme=default&hide_border=true&date_format=M%20j%5B%2C%20Y%5D">
  </picture>
</p>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/mg-mg-mg/mg-mg-mg/output/github-snake-dark.svg">
  <img alt="Contribution graph eaten by a snake, regenerated daily by a GitHub Action" src="https://raw.githubusercontent.com/mg-mg-mg/mg-mg-mg/output/github-snake.svg" width="100%">
</picture>

<sub>Counts include private-repository contributions shown on this profile. The snake is regenerated daily by a GitHub Action.</sub>

### Hackathon awards

| Result | Event | Track | |
| :---: | --- | --- | --- |
| 🥇 1st | DAO Global Hackathon 2023 (Aragon) | Most Creative Use of Aragon OSx | [Project](https://github.com/0xKYC/0xkyc-1vote-aragon-plugin) |
| 🥇 1st | Aptos Seoul Hack 2023 | Gaming | [Project](https://github.com/catze-labs/AptosSeoulHack2023-AptoPlay-info) |
| 🥇 1st | Coinbase Hackathon: Buidl The Future | XDC Open Ideas | [Project](https://github.com/catze-labs/CoinbaseBuidlTheFuture-R3plica-info) |
| 🥇 1st | Klaymakers22 Global Hackathon | NFT & Metaverse | [Project](https://github.com/catze-labs/Klaymakers2022-KUP-info) |
| 🥈 2nd | BNB Chain Innovation Hackathon Seoul | — | [Project](https://github.com/catze-labs/BNBChainInnovationHackathon-r3plica-info) |
| 🏅 Prizes | ETHGlobal Tokyo | Polygon Pool Prize & Scroll (Just Deploy) | [Project](https://github.com/catze-labs/jury-dao-info) |

### Patent

Named inventor at **Hyperconnect** ([acquired by Match Group for $1.725B](https://ir.mtch.com/investor-relations/news-events/news-events/news-details/2021/Match-Group-Closes-Acquisition-of-Hyperconnect/default.aspx)) — *Report evaluation device and operation method thereof*, a learning-model-based method for evaluating the reliability of user reports.

[![US12137302B2](https://img.shields.io/badge/US_patent-US12137302B2-0B5394?style=flat-square)](https://patents.google.com/patent/US12137302B2/en)
[![KR102503049B1](https://img.shields.io/badge/KR_patent-KR102503049B1-C60C30?style=flat-square)](https://patents.google.com/patent/KR102503049B1/en)

### Background

- Previously built payments and Web3 backends.
- **B.S. in Computer Engineering**, Inha University (March 2014 – August 2021).
- **Exchange Program in Computer Engineering**, TU Chemnitz, Germany (October 2020 – February 2021).
