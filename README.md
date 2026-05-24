<h1 align="center">Bernardo Vega</h1>

<p align="center">
  <em>Software Developer · Machine Learning Engineer in training</em><br/>
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

Full-stack developer at [NeuralGT](https://github.com/NeuralGT), where I build **Fintrack**, a personal finance SaaS for the Chilean market (FastAPI + PostgreSQL + Next.js).

On the side, I am transitioning into **Machine Learning Engineering**: shipping production-grade ML projects, studying graduate-level statistics and optimization, and aiming for a remote ML role by late 2026.

Recent CS graduate (UTH 2026, 97/100 GPA).

---

## Featured Project

### [`geoplay-recommender`](https://github.com/bernhardtwo/geoplay)
**Geo-contextual player segmentation & content ranking**

<p>
  <img src="https://img.shields.io/badge/status-in_progress-blue?style=flat-square"/>
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

---

## Other Projects

### [`fintrack`](https://github.com/NeuralGT) *(private · NeuralGT)*

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

**Backend**

<p>
  <img src="https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white"/>
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white"/>
  <img src="https://img.shields.io/badge/Pydantic-E92063?style=flat&logo=pydantic&logoColor=white"/>
  <img src="https://img.shields.io/badge/Alembic-484C50?style=flat"/>
</p>

**Frontend**

<p>
  <img src="https://img.shields.io/badge/Next.js-000000?style=flat&logo=next.js&logoColor=white"/>
  <img src="https://img.shields.io/badge/React-61DAFB?style=flat&logo=react&logoColor=black"/>
  <img src="https://img.shields.io/badge/Tailwind-06B6D4?style=flat&logo=tailwindcss&logoColor=white"/>
  <img src="https://img.shields.io/badge/TanStack_Query-FF4154?style=flat&logo=react-query&logoColor=white"/>
</p>

**Tooling**

<p>
  <img src="https://img.shields.io/badge/Git-F05032?style=flat&logo=git&logoColor=white"/>
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white"/>
  <img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat&logo=github-actions&logoColor=white"/>
  <img src="https://img.shields.io/badge/Linux-FCC624?style=flat&logo=linux&logoColor=black"/>
  <img src="https://img.shields.io/badge/uv-DE5FE9?style=flat"/>
  <img src="https://img.shields.io/badge/Ruff-D7FF64?style=flat&logo=ruff&logoColor=black"/>
</p>

---

## Currently Focused On

- Shipping `geoplay-recommender` end-to-end: clustering → ranking → MLflow → FastAPI → Docker
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
