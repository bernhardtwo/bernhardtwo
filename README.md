<h1 align="center">Bernardo Vega</h1>

<p align="center">
  <em>Cybersecurity Analyst @ NeuralGT | Application Security · Fullstack (Next.js, FastAPI) · ML for security | Fintech</em><br/>
  Hermosillo, México · open to remote roles and relocation to Canada
</p>

<p align="center">
  <a href="mailto:vega@bernhardtwo.com">
    <img src="https://img.shields.io/badge/Email-vega@bernhardtwo.com-EA4335?style=flat&logo=maildotru&logoColor=white" alt="Email"/>
  </a>
  <a href="https://www.linkedin.com/in/bernhardtwo/">
    <img src="https://img.shields.io/badge/LinkedIn-bernhardtwo-0A66C2?style=flat&logo=linkedin&logoColor=white" alt="LinkedIn"/>
  </a>
  <a href="https://bernhardtwo.com">
    <img src="https://img.shields.io/badge/Portfolio-bernhardtwo.com-0B0B0B?style=flat&logo=googlechrome&logoColor=3FE0C5" alt="Portfolio"/>
  </a>
  <a href="https://tidelog.app">
    <img src="https://img.shields.io/badge/Tidelog-tidelog.app-3FE0C5?style=flat&logoColor=0B0B0B" alt="Tidelog"/>
  </a>
</p>

---

## About

Cybersecurity analyst at [NeuralGT](https://github.com/NeuralGT), where I own application security for **Plenor**, a personal finance SaaS for the Chilean market, across its web and admin surfaces. I came into the role as the team's full-stack developer (FastAPI + PostgreSQL + Next.js) and still ship features, so I review code knowing how it gets built.

On the side, I build security tooling and connect it with Machine Learning: static malware analysis, evaluation harnesses, and agentic systems where isolation is enforced below the model, not in the prompt. Where I want to end up is digital forensics and cybercrime analysis.

B.Eng. in Software Development and Management (UTH 2026, 97/100 GPA).

---

## Security

### `atfs` *(private)*
**Static, defensive malware scanner for PE and ELF binaries**

<p>
  <img src="https://img.shields.io/badge/status-v0.3.0_in_development-D29922?style=flat-square"/>
  <img src="https://img.shields.io/badge/Python-3.11+-3776AB?style=flat-square&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/YARA-signatures-B22222?style=flat-square"/>
  <img src="https://img.shields.io/badge/pefile_·_LIEF-parsing-555555?style=flat-square"/>
  <img src="https://img.shields.io/badge/LightGBM-classifier-2E8B57?style=flat-square"/>
  <img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=github-actions&logoColor=white"/>
</p>

Classifies a binary as benign, suspicious, or malicious without executing it. Four layers run in order: hash reputation, YARA signatures, structural heuristics, and an ML classifier. Each layer contributes explainable evidence to the final score, so every verdict says why.

**Highlights**
- 0 false positives on 15,473 Windows system binaries (`System32` + `SysWOW64`), 95% Wilson upper bound 0.02%, under the project's FP < 0.1% target
- 0 false positives on 2,851 Linux system binaries and 747 kernel drivers; the report states these corpora are still too small to prove the target
- Heuristics recalibrated from 124 characterized false positives (W+X `INIT` sections on native images, entropy by section role, managed assemblies) with before/after baselines frozen in the repo
- Degraded runs are explicit: a missing or broken layer resource is reported and turns a benign exit into its own code, so a verdict is never silently unverified
- Stable JSON output with a schema version, CI exit codes per verdict, and a feature contract validated at model load

### [`caselens`](https://github.com/bernhardtwo/caselens)
**Cohere-native enterprise agentic assistant for warranty-claims triage**

<p>
  <img src="https://img.shields.io/badge/status-completed-2EA043?style=flat-square"/>
  <img src="https://img.shields.io/badge/Python-3.12-3776AB?style=flat-square&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white"/>
  <img src="https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=next.js&logoColor=white"/>
  <img src="https://img.shields.io/badge/Cohere-Command%20%C2%B7%20Embed%20%C2%B7%20Rerank-39594D?style=flat-square"/>
  <img src="https://img.shields.io/badge/pgvector-008BB9?style=flat-square"/>
  <img src="https://img.shields.io/badge/Azure_Container_Apps-0078D4?style=flat-square&logo=microsoft-azure&logoColor=white"/>
</p>

A Cohere-native agent that triages enterprise warranty claims: it answers policy questions grounded in a document corpus, works over a tenant-scoped claims database, and takes guarded actions, with every step audited. Built so that scoping and permissions live below the model, not in the prompt, so prompt injection cannot cross tenants.

**Highlights**
- Tenant isolation, RBAC, and immutable audit enforced below the model: `tenant_id` is bound in a closure and never exposed in the tool schema, so the model cannot reach another tenant's data
- Cross-tenant security scenarios in the agent evaluation suite, wired into CI as a release gate
- Human-in-the-loop confirmation for state-changing actions, gated by an allowed-transition state machine
- Command tool-use agent over Embed retrieval and Rerank, with native grounded citations aligned to the source text
- Deployed live on Azure Container Apps, with a connection pool and transaction-isolated audit

### Studying

HTB Academy on the CPTS path, with OSCP as the next goal. Networking fundamentals along the way.

My portfolio is part of the practice: [bernhardtwo.com](https://bernhardtwo.com) ships a hash-based CSP with no `unsafe-inline`, HSTS, the rest of the security headers, and a [`security.txt`](https://bernhardtwo.com/.well-known/security.txt).

---

## Building

### [Tidelog](https://tidelog.app) *(private beta)*
**A day planner in blocks for Mac and iPhone**

<p>
  <img src="https://img.shields.io/badge/status-private_beta-D29922?style=flat-square"/>
  <img src="https://img.shields.io/badge/Swift-F05138?style=flat-square&logo=swift&logoColor=white"/>
  <img src="https://img.shields.io/badge/SwiftUI-0D96F6?style=flat-square&logo=swift&logoColor=white"/>
  <img src="https://img.shields.io/badge/Cloudflare_Workers-F38020?style=flat-square&logo=cloudflare&logoColor=white"/>
</p>

Pick a Jira ticket and the Clockify or Toggl timer runs, pauses on every break, and the rest of the day shifts when you fall behind.

**Highlights**
- Native Swift and SwiftUI on macOS and iOS
- Flexible blocks move on their own when the day slips
- No analytics and no tracking; data stays in the user's iCloud
- Landing on Cloudflare Workers, served with `no-transform` so the CDN injects nothing

### [`ledger-lens`](https://github.com/bernhardtwo/ledger-lens)
**AI-native agentic financial analyst**

<p>
  <img src="https://img.shields.io/badge/status-deployed_·_polishing-2EA043?style=flat-square"/>
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white"/>
  <img src="https://img.shields.io/badge/NestJS-E0234E?style=flat-square&logo=nestjs&logoColor=white"/>
  <img src="https://img.shields.io/badge/Claude_Agent_SDK-D97757?style=flat-square&logo=anthropic&logoColor=white"/>
  <img src="https://img.shields.io/badge/MCP-000000?style=flat-square"/>
  <img src="https://img.shields.io/badge/Azure-0078D4?style=flat-square&logo=microsoft-azure&logoColor=white"/>
</p>

Upload bank statements and an agent extracts, categorizes, reconciles, and answers natural-language questions about your finances. Built **determinism-first**: the model decides what to compute and explains the result, while pure functions do the money math on currency-aware integers.

**Highlights**
- Read-only MCP server exposing 5 typed finance tools to the agent, scoped per account
- Eval harness with a 23-case golden set that runs in CI weekly and on dispatch, failing on a threshold miss
- CI/CD via GitHub Actions and OIDC, with no long-lived cloud secrets
- Deployed to Azure Container Apps with OpenTelemetry

---

## Other Projects

- **[`plenor`](https://github.com/NeuralGT)** *(private · NeuralGT)*: full-stack SaaS for personal finance in Chile. FastAPI and PostgreSQL backend, Next.js frontend with Feature-Sliced Design.
- **[`geoplay`](https://github.com/bernhardtwo/geoplay)**: ML pipeline for geo-contextual player segmentation and content ranking over 50,000 synthetic players and 146M events. HDBSCAN clustering on a 54-feature matrix, LightGBM ranking, and a partition-streaming feature pipeline. MLflow, FastAPI, Docker.
- **[`vgc-coach`](https://github.com/bernhardtwo/vgc-coach)**: local-LLM coach for Pokémon VGC replays. Damage, speed order and usage priors are computed in code and handed to the model as ground truth, so it never invents mechanics. Ollama, Pydantic, `@smogon/calc`.

---

## Tech Stack

**Security** &nbsp;
<img src="https://img.shields.io/badge/YARA-B22222?style=flat"/>
<img src="https://img.shields.io/badge/pefile-555555?style=flat"/>
<img src="https://img.shields.io/badge/LIEF-555555?style=flat"/>
<img src="https://img.shields.io/badge/Playwright-2EAD33?style=flat&logo=playwright&logoColor=white"/>

**Languages** &nbsp;
<img src="https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white"/>
<img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white"/>
<img src="https://img.shields.io/badge/Swift-F05138?style=flat&logo=swift&logoColor=white"/>
<img src="https://img.shields.io/badge/SQL-4479A1?style=flat&logo=postgresql&logoColor=white"/>

**Web** &nbsp;
<img src="https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white"/>
<img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white"/>
<img src="https://img.shields.io/badge/Pydantic-E92063?style=flat&logo=pydantic&logoColor=white"/>
<img src="https://img.shields.io/badge/NestJS-E0234E?style=flat&logo=nestjs&logoColor=white"/>
<img src="https://img.shields.io/badge/Next.js-000000?style=flat&logo=next.js&logoColor=white"/>
<img src="https://img.shields.io/badge/React-61DAFB?style=flat&logo=react&logoColor=black"/>
<img src="https://img.shields.io/badge/TanStack_Query-FF4154?style=flat&logo=react-query&logoColor=white"/>

**ML & Agents** &nbsp;
<img src="https://img.shields.io/badge/scikit--learn-F7931E?style=flat&logo=scikit-learn&logoColor=white"/>
<img src="https://img.shields.io/badge/LightGBM-2E8B57?style=flat"/>
<img src="https://img.shields.io/badge/MLflow-0194E2?style=flat&logo=mlflow&logoColor=white"/>
<img src="https://img.shields.io/badge/Claude_Agent_SDK-D97757?style=flat&logo=anthropic&logoColor=white"/>
<img src="https://img.shields.io/badge/MCP-000000?style=flat"/>

**Platform** &nbsp;
<img src="https://img.shields.io/badge/Linux-FCC624?style=flat&logo=linux&logoColor=black"/>
<img src="https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white"/>
<img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat&logo=github-actions&logoColor=white"/>
<img src="https://img.shields.io/badge/Cloudflare-F38020?style=flat&logo=cloudflare&logoColor=white"/>
<img src="https://img.shields.io/badge/Azure-0078D4?style=flat&logo=microsoft-azure&logoColor=white"/>
<img src="https://img.shields.io/badge/AWS-232F3E?style=flat&logo=amazon-aws&logoColor=white"/>

---

## Currently Focused On

- Owning application security for a production fintech: attack surface review, session and access control, dependency and CI supply chain hygiene
- The CPTS path on HTB Academy
- Getting Tidelog out of private beta
- Learning French

When I'm not coding, I write literary fiction (currently a novella anchored in Camus and Kierkegaard), explore FromSoftware games, and overthink internet culture.

---

## Find Me on the Field

A small Yanma to close. Field guide entry: Bug/Flying type, Generation II, Pokédex #193. Known for its compound eyes that see 360° around itself, a useful trait for someone who works with data from many angles :D

```
                            .::::@-   .-::$-
                             ;::;;;;#;:::;;+ -H#@
 *&&-        :      :*              *;H;+++;+++++++;.
 -:&;;;+#  ,&:     ::               :+++$@    @H+++#
   ;++++++;;;+*   ;;;             --H;*#
     #     .;;+  +++             -::;**
        +   ;;*+++++#H         :;::$*  #       ;+;;+@  @
           #+;;++$::::+*:::::@+&@;,        ;@*&@@+**&$$$@
          &;+:;;::::::;**;+;+&,$- .....        ;;;;;;;     -
          ,:$;++::::;:+**@,,,,,,.             ;+++;;;+
         H:+++++;::H #***&***@*+.-+*+H#H@HH&*$$#$$$#;
         @+++++++++$#&***$*H**# ;#@@@
          *@;;:*+**$@$****H*+@@$   $@$
           #+**H***@@@**@:@    &@   @@
           ;***&*@****&   @    @@   H**
             &#$&#       ,@    @@    ***
           @&#  .        @@   #@     *
         ***            @@    **
           H          #@@     +@
                     **+
                     @#;
```

---

<p align="center">
  <sub>Thanks for stopping by. Reach out anytime via <a href="mailto:vega@bernhardtwo.com">email</a> or <a href="https://www.linkedin.com/in/bernhardtwo/">LinkedIn</a>.</sub>
</p>
