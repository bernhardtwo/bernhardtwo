<h1 align="center">Bernardo Vega</h1>

<p align="center">
  <em>Software Developer · Machine Learning Engineer</em><br/>
  Hermosillo, México · open to remote ML & data roles
</p>

<p align="center">
  <a href="mailto:rruizveg@gmail.com">
    <img src="https://img.shields.io/badge/Email-rruizveg@gmail.com-EA4335?style=flat&logo=gmail&logoColor=white" alt="Email"/>
  </a>
  <a href="https://www.linkedin.com/in/bernardo-vega-237791295/">
    <img src="https://img.shields.io/badge/LinkedIn-bernardo--vega-0A66C2?style=flat&logo=linkedin&logoColor=white" alt="LinkedIn"/>
  </a>
  <a href="https://github.com/bernhardtwo">
    <img src="https://img.shields.io/badge/GitHub-bernhardtwo-181717?style=flat&logo=github&logoColor=white" alt="GitHub"/>
  </a>
</p>

---

## About

Full-stack developer at [NeuralGT](https://github.com/NeuralGT), where I build **Plenor**, a personal finance SaaS for the Chilean market (FastAPI + PostgreSQL + Next.js).

On the side, I am transitioning into **Machine Learning & AI-native Engineering**: shipping production-grade ML and agentic projects, studying graduate-level statistics and optimization, and aiming for a remote ML role by late 2026.

Recent CS graduate (UTH 2026, 97/100 GPA).

---

## Featured Projects

### [`geoplay-recommender`](https://github.com/bernhardtwo/geoplay)
**Geo-contextual player segmentation & content ranking**

<p>
  <img src="https://img.shields.io/badge/status-completed-2EA043?style=flat-square"/>
  <img src="https://img.shields.io/badge/Python-3.12-3776AB?style=flat-square&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikit-learn&logoColor=white"/>
  <img src="https://img.shields.io/badge/HDBSCAN-clustering-4B8BBE?style=flat-square"/>
  <img src="https://img.shields.io/badge/LightGBM-ranking-2E8B57?style=flat-square"/>
  <img src="https://img.shields.io/badge/H3-spatial-FF6B35?style=flat-square"/>
  <img src="https://img.shields.io/badge/MLflow-tracking-0194E2?style=flat-square&logo=mlflow&logoColor=white"/>
  <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white"/>
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white"/>
</p>

Production-grade ML pipeline simulating a Pokémon GO–style game with **50,000 synthetic players, 162M events, and 5 behavioral archetypes** (commuter, casual evening, weekend explorer, hardcore raider, lunch player). The pipeline clusters players via HDBSCAN on a 54-feature matrix (temporal density, H3 spatial footprint, session behavior) and ranks content with LightGBM.

**Highlights**
- Partition-streaming feature pipeline bounded to ~3 GB constant memory on 162M events
- 54 engineered features across three families: temporal (39), spatial with H3 (7), behavioral (8)
- Strict tooling: `uv`, `ruff`, `mypy`, pre-commit hooks
- MLflow experiment tracking, FastAPI serving layer, Dockerized deployment, GitHub Actions CI/CD

### [`ledger-lens`](https://github.com/bernhardtwo/ledger-lens)
**AI-native agentic financial analyst**

<p>
  <img src="https://img.shields.io/badge/status-completed-2EA043?style=flat-square"/>
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white"/>
  <img src="https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=next.js&logoColor=white"/>
  <img src="https://img.shields.io/badge/NestJS-E0234E?style=flat-square&logo=nestjs&logoColor=white"/>
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white"/>
  <img src="https://img.shields.io/badge/Drizzle-C5F74F?style=flat-square&logo=drizzle&logoColor=black"/>
  <img src="https://img.shields.io/badge/Claude_Agent_SDK-D97757?style=flat-square&logo=anthropic&logoColor=white"/>
  <img src="https://img.shields.io/badge/MCP-000000?style=flat-square"/>
  <img src="https://img.shields.io/badge/Zod-3E67B1?style=flat-square&logo=zod&logoColor=white"/>
  <img src="https://img.shields.io/badge/Vitest-6E9F18?style=flat-square&logo=vitest&logoColor=white"/>
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white"/>
  <img src="https://img.shields.io/badge/Azure-0078D4?style=flat-square&logo=microsoft-azure&logoColor=white"/>
</p>

An AI-native financial analyst built TypeScript-first. Upload bank statements and an agent extracts, categorizes, reconciles, and answers natural-language questions about your finances, with deterministic money math and a rigorous evaluation harness behind every LLM feature.

Built **determinism-first**: the model decides what to compute and explains the result, while pure functions do the money math. Money is stored as currency-aware integers, so floating-point drift is never possible in financial figures.

**Highlights**
- Streaming agent chat with live tool calls over SSE
- Read-only MCP server exposing 5 typed finance tools to the agent, scoped per account
- Deterministic ingestion and currency-aware integer money, with no FX
- Eval harness with a 23-case golden set wired into CI as a gate
- Deployed to Azure Container Apps with OpenTelemetry, CI/CD via GitHub Actions and OIDC (no long-lived cloud secrets)

---

## Other Projects

### [`plenor`](https://github.com/NeuralGT) *(private · NeuralGT)*

<p>
  <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white"/>
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white"/>
  <img src="https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=next.js&logoColor=white"/>
  <img src="https://img.shields.io/badge/TanStack_Query-FF4154?style=flat-square&logo=react-query&logoColor=white"/>
  <img src="https://img.shields.io/badge/AWS_RDS-527FFF?style=flat-square&logo=amazon-aws&logoColor=white"/>
</p>

Full-stack SaaS for personal finance in Chile. FastAPI backend with Alembic migrations, PostgreSQL on AWS RDS, Next.js frontend with Feature-Sliced Design. Integrations with Floid (banking sync), Binance, and mindicador.cl.

---

## Tech Stack

**Languages**

<p>
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white"/>
  <img src="https://img.shields.io/badge/SQL-4479A1?style=flat&logo=postgresql&logoColor=white"/>
</p>

**Machine Learning & Data**

<p>
  <img src="https://img.shields.io/badge/scikit--learn-F7931E?style=flat&logo=scikit-learn&logoColor=white"/>
  <img src="https://img.shields.io/badge/pandas-150458?style=flat&logo=pandas&logoColor=white"/>
  <img src="https://img.shields.io/badge/NumPy-013243?style=flat&logo=numpy&logoColor=white"/>
  <img src="https://img.shields.io/badge/MLflow-0194E2?style=flat&logo=mlflow&logoColor=white"/>
  <img src="https://img.shields.io/badge/Jupyter-F37626?style=flat&logo=jupyter&logoColor=white"/>
</p>

**AI-native & Agents**

<p>
  <img src="https://img.shields.io/badge/Claude_Agent_SDK-D97757?style=flat&logo=anthropic&logoColor=white"/>
  <img src="https://img.shields.io/badge/MCP-000000?style=flat"/>
  <img src="https://img.shields.io/badge/Zod-3E67B1?style=flat&logo=zod&logoColor=white"/>
</p>

**Backend**

<p>
  <img src="https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white"/>
  <img src="https://img.shields.io/badge/NestJS-E0234E?style=flat&logo=nestjs&logoColor=white"/>
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white"/>
  <img src="https://img.shields.io/badge/Pydantic-E92063?style=flat&logo=pydantic&logoColor=white"/>
  <img src="https://img.shields.io/badge/Alembic-484C50?style=flat"/>
  <img src="https://img.shields.io/badge/Drizzle-C5F74F?style=flat&logo=drizzle&logoColor=black"/>
</p>

**Frontend**

<p>
  <img src="https://img.shields.io/badge/Next.js-000000?style=flat&logo=next.js&logoColor=white"/>
  <img src="https://img.shields.io/badge/React-61DAFB?style=flat&logo=react&logoColor=black"/>
  <img src="https://img.shields.io/badge/Tailwind-06B6D4?style=flat&logo=tailwindcss&logoColor=white"/>
  <img src="https://img.shields.io/badge/TanStack_Query-FF4154?style=flat&logo=react-query&logoColor=white"/>
</p>

**Tooling & Cloud**

<p>
  <img src="https://img.shields.io/badge/Git-F05032?style=flat&logo=git&logoColor=white"/>
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white"/>
  <img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat&logo=github-actions&logoColor=white"/>
  <img src="https://img.shields.io/badge/Azure-0078D4?style=flat&logo=microsoft-azure&logoColor=white"/>
  <img src="https://img.shields.io/badge/Linux-FCC624?style=flat&logo=linux&logoColor=black"/>
  <img src="https://img.shields.io/badge/uv-DE5FE9?style=flat"/>
  <img src="https://img.shields.io/badge/Ruff-D7FF64?style=flat&logo=ruff&logoColor=black"/>
</p>

---

## Currently Focused On

- Designing and shipping AI-native, full-stack systems end to end, from data layer to agent to deployment
- Strengthening statistics and optimization fundamentals for graduate-level ML work
- Building fluent technical English for international remote collaboration

When I'm not coding, I write literary fiction (currently a novella anchored in Camus and Kierkegaard), explore FromSoftware games, and overthink internet culture.

---

## Find Me on the Field

A small Yanma to close. Field guide entry: Bug/Flying type, Generation II, Pokédex #193. Known for its compound eyes that see 360° around itself a useful trait for someone who works with data from many angles :D

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
  <sub>Thanks for stopping by. Reach out anytime via <a href="mailto:rruizveg@gmail.com">email</a> or <a href="https://www.linkedin.com/in/bernardo-vega-237791295/">LinkedIn</a>.</sub>
</p>
