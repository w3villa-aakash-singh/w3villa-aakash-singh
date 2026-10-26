<div align="center">

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&height=270&color=0:0f2027,50:203a43,100:2c5364&text=Aakash%20Singh&fontColor=ffffff&fontSize=60&animation=fadeIn&fontAlignY=38&desc=Full-Stack%20Software%20Engineer%20|%20Python%20•%20FastAPI%20•%20React&descAlignY=58&descSize=20"/>

<img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&size=22&duration=3200&pause=900&color=00F7FF&center=true&vCenter=true&width=820&height=40&lines=Building+production+analytics+%26+reporting+systems;FastAPI+%E2%80%A2+React+%E2%80%A2+PostgreSQL+%E2%80%A2+Redis;SQL+performance+%E2%80%A2+Dashboards+%E2%80%A2+Excel+exports;OEE+%E2%80%A2+Audit+trails+%E2%80%A2+PLC+analytics;Always+learning+new+technologies"/>

<p>
<img src="https://komarev.com/ghpvc/?username=w3villa-aakash-singh&label=Profile+Views&style=for-the-badge&color=0e75b6"/>
<img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white"/>
<img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white"/>
<img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB"/>
<img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white"/>
<img src="https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white"/>
</p>

<p>
<a href="#about-me"><b>About</b></a> &nbsp;|&nbsp;
<a href="#what-i-do"><b>What I Do</b></a> &nbsp;|&nbsp;
<a href="#featured-project-kivo-eye-sswl"><b>Project</b></a> &nbsp;|&nbsp;
<a href="#tech-stack"><b>Stack</b></a> &nbsp;|&nbsp;
<a href="#github-activity"><b>Activity</b></a> &nbsp;|&nbsp;
<a href="#connect-with-me"><b>Connect</b></a>
</p>

<img src="assets/terminal.svg" width="100%" alt="Animated terminal: whoami, stack, projects, status"/>

</div>

<img src="assets/divider.svg" width="100%"/>

## About Me

I'm a full-stack engineer who builds data-heavy product features end to end: PostgreSQL queries and indexes, FastAPI services, and React dashboards that operations teams use every day. Right now I work on a manufacturing analytics platform, focusing on reporting, OEE metrics, audit search, and query performance.

```yaml
Name:       Aakash Singh
Role:       Full-Stack Software Engineer
Company:    W3Villa
Project:    Kivo Eye (SSWL)
Working on: Production analytics, reporting systems, real-time dashboards, SQL performance
Strengths:  FastAPI, React, PostgreSQL, Redis, SQLAlchemy
Learning:   FAISS, CUDA, TensorRT, Kafka, Kubernetes
Ask me:     FastAPI, React, PostgreSQL, Redis, JWT, Docker, WebSockets, Computer Vision,
            report and export workflows, index and query tuning
```

<img src="assets/divider.svg" width="100%"/>

## What I Do

<table>
<tr>
<td width="33%" valign="top">

### Backend APIs

FastAPI routers, controllers, and services with Pydantic validation, JWT/API-key auth, pagination, filtering, response caching, and streamed file downloads.

</td>
<td width="33%" valign="top">

### Data and SQL

SQLAlchemy models, PostgreSQL CTEs, partial and composite indexes, non-blocking index migrations, and shift-window calculations that respect IST.

</td>
<td width="33%" valign="top">

### Dashboards

React + Material UI report pages, filter and modal workflows, Recharts visuals, and formatted Excel exports that replace manual raw-data work.

</td>
</tr>
</table>

<img src="assets/divider.svg" width="100%"/>

## Featured Project: Kivo Eye (SSWL)

A production-line analytics platform for a wheel and paint manufacturing environment. It combines live conveyor monitoring, line-run and shift tracking, OEE reporting, production reports, audit logs, PLC drive-current analytics, camera streams, email notifications, and WebSocket updates.

**Stack:** FastAPI · SQLAlchemy 2 · PostgreSQL · Redis · Pydantic 2 · APScheduler · JWT · OpenPyXL · React 18 · Material UI · Recharts

It is a multi-author codebase. Everything below is what I personally built.

<div align="center">

<img src="assets/pipeline.svg" width="100%" alt="Request flow: React to FastAPI to Redis and PostgreSQL to JSON or Excel"/>

<br/><br/>

<img src="assets/numbers.svg" width="100%" alt="195 commits, 14 migrations, 15 test files, 173 files touched"/>

<br/><br/>

<img src="assets/timeline.svg" width="100%" alt="Timeline of features shipped, by pull request number"/>

</div>

### My contributions

| Area | What I built |
|---|---|
| **Reporting dashboard** | Paginated, shift-aware reporting API with Pydantic query validation, composite indexes, and a Material UI front end |
| **Production reports + Excel** | Contributed to a 13-endpoint reporting module with formatted `.xlsx` exports via OpenPyXL |
| **OEE calculation** | Availability × Performance × Quality across shift, FTD (for the day), and FTM (for the month) windows |
| **Audit search** | Filterable, paginated audit service with a 15-second Redis cache and a React UI |
| **PLC drive-current analytics** | Multi-bucket aggregation, per-drive peaks and averages, IST-aware shift mapping, and a high-current event log |
| **Query and index optimization** | CTE-based SQL, partial and composite indexes built with `CREATE INDEX CONCURRENTLY`, and Redis caching for repeated report reads |
| **Scheduled jobs** | APScheduler storage-retention cleanup with throttled deletes and audit records |

### The details

<details>
<summary><b>Reporting-lite dashboard</b></summary>
<br/>

- Paginated shift and run data with model and shift filtering, validated through Pydantic query schemas
- A dedicated backend query path plus a supporting index migration
- A Material UI page of roughly 1,400 lines, with its own test file

</details>

<details>
<summary><b>Production reports and Excel exports</b></summary>
<br/>

- Reports covered: hourly loading vs OK, daily production, monthly production, lot-wise tracking, dispatch/loading, and the loss dashboard
- Each report has filtering, pagination, server-side aggregation, and a formatted `.xlsx` export built with OpenPyXL
- Matching React report pages and API client methods
- Replaced several manual raw-data workflows with filterable UI reports

</details>

<details>
<summary><b>SQL and index optimization</b></summary>
<br/>

- Reworked line-run, paint-change, model-change, conveyor-stop, and missing-rim calculations into CTE-based SQL
- Added partial and composite PostgreSQL indexes through migrations
- Used `CREATE INDEX CONCURRENTLY` with invalid-index cleanup so production writes aren't blocked
- Added Redis TTL caching for repeated reads, with explicit invalidation groups

</details>

<details>
<summary><b>OEE KPI calculation</b></summary>
<br/>

- OEE = Availability × Performance × Quality, computed for shift, FTD, and FTM windows
- Performance logic uses expected output per hour, rim counts, actual runtimes, and inspection OK counts
- Wired into the OEE report table and page in the React app
- My part was the calculation work. The module was scaffolded and later revamped by teammates.

</details>

<details>
<summary><b>Audit-lite search</b></summary>
<br/>

- Search by hanger number, shift, assignment, and date range, with pagination
- A 15-second Redis cache and a supporting query-index migration
- A React interface of roughly 1,500 lines for operations users
- Gives operators a searchable history of hanger and line-run activity

</details>

<details>
<summary><b>PLC drive-current analytics</b></summary>
<br/>

- Buckets: 5, 10, and 30 minutes, hourly, per shift, and daily
- IST-aware shift mapping, per-drive averages and peaks
- A threshold-based high-current event log
- Targeted tests plus a substantially expanded React analytics page

</details>

<details>
<summary><b>Engineering practices</b></summary>
<br/>

- Every index change ships as a migration
- Targeted tests for caching, reporting-lite, OEE, PLC analytics, audit-lite, and history stats (130 passing)
- Layered structure: routes, controllers, services, schemas
- Cache invalidation designed alongside caching, not added later

</details>

<img src="assets/divider.svg" width="100%"/>

## Tech Stack

<div align="center">

<img src="assets/marquee.svg" width="100%" alt="Scrolling list of technologies"/>

**Languages**

<img src="https://skillicons.dev/icons?i=python,java,js,ts,html,css&theme=dark"/>

**Frontend**

<img src="https://skillicons.dev/icons?i=react,nextjs,redux,vite,angular,mui&theme=dark"/>

**Backend**

<img src="https://skillicons.dev/icons?i=fastapi,nodejs,spring&theme=dark"/>

**Databases**

<img src="https://skillicons.dev/icons?i=postgres,mysql,mongodb,redis,firebase,supabase&theme=dark"/>

**DevOps**

<img src="https://skillicons.dev/icons?i=docker,git,github,linux,vercel,heroku&theme=dark"/>

**Tools**

<img src="https://skillicons.dev/icons?i=figma,postman,vscode&theme=dark"/>

</div>

### Currently Learning

<p align="center">
<img src="https://img.shields.io/badge/FAISS-0467DF?style=for-the-badge&logo=meta&logoColor=white"/>
<img src="https://img.shields.io/badge/CUDA-76B900?style=for-the-badge&logo=nvidia&logoColor=white"/>
<img src="https://img.shields.io/badge/TensorRT-76B900?style=for-the-badge&logo=nvidia&logoColor=white"/>
<img src="https://img.shields.io/badge/Kafka-231F20?style=for-the-badge&logo=apachekafka&logoColor=white"/>
<img src="https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white"/>
</p>

<img src="assets/divider.svg" width="100%"/>

## Earlier Projects

<p align="center">
<a href="https://github.com/w3villa-aakash-singh/Mini-Project-backend">
<img src="https://github-readme-stats.vercel.app/api/pin/?username=w3villa-aakash-singh&repo=Mini-Project-backend&theme=tokyonight&hide_border=true"/>
</a>
<a href="https://github.com/w3villa-aakash-singh/Mini-Project-frontend">
<img src="https://github-readme-stats.vercel.app/api/pin/?username=w3villa-aakash-singh&repo=Mini-Project-frontend&theme=tokyonight&hide_border=true"/>
</a>
</p>

<img src="assets/divider.svg" width="100%"/>

## GitHub Activity

<p align="center">
<img height="170" src="https://github-readme-stats.vercel.app/api?username=w3villa-aakash-singh&show_icons=true&theme=tokyonight&hide_border=true&include_all_commits=true"/>
<img height="170" src="https://streak-stats.demolab.com?user=w3villa-aakash-singh&theme=tokyonight&hide_border=true"/>
</p>

> Most of my recent work lives in private repositories, so these cards undercount it.

### Contribution Snake

<p align="center">
<img src="https://raw.githubusercontent.com/w3villa-aakash-singh/w3villa-aakash-singh/output/github-contribution-grid-snake-dark.svg" alt="Contribution snake animation"/>
</p>

### 3D Contribution Calendar

<p align="center">
<img src="./profile-3d-contrib/profile-night-rainbow.svg" alt="3D contribution calendar"/>
</p>

<img src="assets/divider.svg" width="100%"/>

## Connect With Me

<p align="center">
<a href="https://github.com/w3villa-aakash-singh"><img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white"/></a>
<!-- Uncomment and fill in your real links:
<a href="https://linkedin.com/in/YOUR_LINK"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"/></a>
<a href="mailto:YOUR_EMAIL"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white"/></a>
-->
</p>

<p align="center">
<img src="https://quotes-github-readme.vercel.app/api?type=horizontal&theme=tokyonight"/>
</p>

<div align="center">

**Thanks for visiting!**

</div>

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&height=120&section=footer&color=0:0f2027,50:203a43,100:2c5364"/>
