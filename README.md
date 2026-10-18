<picture>
  <source media="(max-width: 600px) and (prefers-color-scheme: dark)" srcset="assets/banner-dark-mobile.svg">
  <source media="(max-width: 600px)" srcset="assets/banner-light-mobile.svg">
  <source media="(prefers-color-scheme: dark)" srcset="assets/banner-dark.svg">
  <img alt="Mingyun Chae — Founder of TriAstra. Senior Backend & AI Agent Platform Engineer. 776 TriAstra PRs merged in the last 7 days; approximately 10 AI agent roles and 100+ peak concurrent OMP coding agents, excluding Aside. 7 open-source fixes merged upstream, 4 hackathon first places, and US and Korean patent registrations. Snapshot: October 18, 2026; agent figures approximate from OMP logs." src="assets/banner-light.svg" width="100%">
</picture>

<p align="center">
  <a href="https://www.linkedin.com/in/mg-chae/"><img alt="LinkedIn: mg-chae" src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"></a>
  <a href="mailto:coalsrbs7@gmail.com"><img alt="Email" src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white"></a>
  <a href="https://mg-mg-mg.github.io/agentic-engineering/"><img alt="Engineering case study" src="https://img.shields.io/badge/Case_study-24292F?style=for-the-badge&logo=github&logoColor=white"></a>
  <a href="https://triastra.ai"><img alt="TriAstra" src="https://img.shields.io/badge/TriAstra-5B4BDB?style=for-the-badge"></a>
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

<table>
  <tr>
    <td><b>Languages</b></td>
    <td><img alt="Rust, TypeScript, JavaScript, Python, Dart, Java, Ruby" src="https://skillicons.dev/icons?i=rust,ts,js,py,dart,java,ruby" height="40"><br>
      <img alt="SQL" src="https://img.shields.io/badge/SQL-336791?style=flat-square"></td>
  </tr>
  <tr>
    <td><b>Backend</b></td>
    <td><img alt="Django, NestJS, Spring Boot, Ruby on Rails" src="https://skillicons.dev/icons?i=django,nestjs,spring,rails" height="40"><br>
      <img alt="Axum" src="https://img.shields.io/badge/Axum-8B4513?style=flat-square"> <img alt="Tokio" src="https://img.shields.io/badge/Tokio-000000?style=flat-square&logo=tokio&logoColor=white"> <img alt="Fastify" src="https://img.shields.io/badge/Fastify-000000?style=flat-square&logo=fastify&logoColor=white"> <img alt="REST / OpenAPI" src="https://img.shields.io/badge/REST%20%2F%20OpenAPI-6BA539?style=flat-square&logo=openapiinitiative&logoColor=white"> <img alt="WebSockets · SSE" src="https://img.shields.io/badge/WebSockets%20%C2%B7%20SSE-4A4A55?style=flat-square"></td>
  </tr>
  <tr>
    <td><b>Frontend & mobile</b></td>
    <td><img alt="React, Flutter, Vite, Tailwind CSS" src="https://skillicons.dev/icons?i=react,flutter,vite,tailwind" height="40"></td>
  </tr>
  <tr>
    <td><b>Data</b></td>
    <td><img alt="PostgreSQL, MySQL, Redis, Kafka, Prisma" src="https://skillicons.dev/icons?i=postgres,mysql,redis,kafka,prisma" height="40"><br>
      <img alt="BigQuery" src="https://img.shields.io/badge/BigQuery-669DF6?style=flat-square&logo=googlebigquery&logoColor=white"> <img alt="SQLx" src="https://img.shields.io/badge/SQLx-DEA584?style=flat-square"></td>
  </tr>
  <tr>
    <td><b>Cloud & delivery</b></td>
    <td><img alt="AWS, GCP, Cloudflare, Docker, Kubernetes, Terraform, GitHub Actions" src="https://skillicons.dev/icons?i=aws,gcp,cloudflare,docker,kubernetes,terraform,githubactions" height="40"><br>
      <img alt="Spinnaker" src="https://img.shields.io/badge/Spinnaker-139BB4?style=flat-square"></td>
  </tr>
  <tr>
    <td><b>Observability & testing</b></td>
    <td><img alt="Grafana, Sentry, Vitest, Jest" src="https://skillicons.dev/icons?i=grafana,sentry,vitest,jest" height="40"><br>
      <img alt="OpenTelemetry" src="https://img.shields.io/badge/OpenTelemetry-425CC7?style=flat-square&logo=opentelemetry&logoColor=white"> <img alt="Datadog" src="https://img.shields.io/badge/Datadog-632CA6?style=flat-square&logo=datadog&logoColor=white"> <img alt="New Relic" src="https://img.shields.io/badge/New%20Relic-1CE783?style=flat-square&logo=newrelic&logoColor=white"> <img alt="PostHog" src="https://img.shields.io/badge/PostHog-F54E00?style=flat-square&logo=posthog&logoColor=white"> <img alt="Playwright" src="https://img.shields.io/badge/Playwright-2EAD33?style=flat-square"></td>
  </tr>
  <tr>
    <td><b>AI & agents</b></td>
    <td><img alt="OpenAI API" src="https://img.shields.io/badge/OpenAI%20API-412991?style=flat-square"> <img alt="Gemini API" src="https://img.shields.io/badge/Gemini%20API-8E75B2?style=flat-square&logo=googlegemini&logoColor=white"> <img alt="Claude Code" src="https://img.shields.io/badge/Claude%20Code-D97757?style=flat-square&logo=claude&logoColor=white"> <img alt="Codex" src="https://img.shields.io/badge/Codex-10A37F?style=flat-square"> <img alt="MCP" src="https://img.shields.io/badge/MCP-000000?style=flat-square&logo=modelcontextprotocol&logoColor=white"> <img alt="OpenAI Apps SDK" src="https://img.shields.io/badge/OpenAI%20Apps%20SDK-412991?style=flat-square"></td>
  </tr>
  <tr>
    <td><b>Web3</b></td>
    <td><img alt="Solidity" src="https://skillicons.dev/icons?i=solidity" height="40"><br>
      <img alt="Ethereum" src="https://img.shields.io/badge/Ethereum-3C3C3D?style=flat-square&logo=ethereum&logoColor=white"> <img alt="Solana" src="https://img.shields.io/badge/Solana-9945FF?style=flat-square&logo=solana&logoColor=white"></td>
  </tr>
</table>

<sub>Technologies I have used in production or shipped projects, per my CV and repositories.</sub>

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

<sub>Live activity cards, not dated evidence: the streak card (streak-stats.demolab.com) and the snake (regenerated daily by this repository’s GitHub Action) read GitHub’s public contribution calendar for this account, which counts private-repository work only as anonymous totals. Contribution totals and streaks are activity counts, not a productivity or delivery metric, and are separate from the dated merged-PR figures above. Upstream star counts are live from shields.io.</sub>

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
