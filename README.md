<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:12172B,50:1E3A8A,100:3457F5&height=180&section=header&text=ARYAN%20GUPTA&fontSize=48&fontColor=FFFFFF&fontAlignY=45&desc=Founder%20%E2%80%94%20Madhav.ai%20%7C%20Justice%20Reimagined&descAlignY=62&descSize=16&descColor=A9BBFF&animation=fadeIn" width="100%"/>

<br/>

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&size=20&duration=2800&pause=1200&color=6C8CFF&center=true&vCenter=true&width=680&lines=Case+No.+2026%2FAI-LEGAL%2F001;PLAINTIFF%3A+Fragmented+Legal+Workflows;DEFENDANT%3A+Aryan+Gupta+%2B+Madhav.ai;RULING%3A+Justice+Reimagined." alt="Typing SVG" />

</div>

<br/>

<table align="center">
<tr>
<td align="center" width="100%">

**IN THE MATTER OF: ARYAN GUPTA**
*B.Tech ECE, BIT Mesra ('27) · Founder, Madhav AI Jurisprudence Pvt. Ltd. · Ranchi, India*

</td>
</tr>
</table>

<p align="center">
  <a href="https://www.madhav-ai.com/"><img src="https://img.shields.io/badge/Madhav.ai-3457F5?style=for-the-badge&logo=googlechrome&logoColor=white" /></a>
  <a href="https://www.linkedin.com/in/aryan-iconic/"><img src="https://img.shields.io/badge/LinkedIn-3457F5?style=for-the-badge&logo=linkedin&logoColor=white" /></a>
  <a href="https://github.com/aryan-iconic"><img src="https://img.shields.io/badge/GitHub-12172B?style=for-the-badge&logo=github&logoColor=white" /></a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Status-Open_to_Remote_%26_OSS_Work-6C8CFF?style=flat-square&labelColor=12172B" />
</p>

---

### 📁 EXHIBIT A — Statement of the Case

I build systems that turn messy, high-stakes information into something a professional can actually *reason* with.

**⚖️ Madhav.ai — Justice Reimagined**
An AI-native legal intelligence and workflow platform for Indian lawyers and law firms — not a chatbot wrapper, but an operating layer that takes a lawyer from raw legal information → understanding → analysis → research → drafting → execution. It's a full platform, not a single tool:

| Module | What it does |
|---|---|
| 🔍 **Search Engine** | Purpose-built legal search across Indian judgments, cases, and authorities |
| 📚 **Research Engine** | Deep legal research over a ~1.5 TB legal corpus using RAG + vector retrieval |
| 🗂️ **CaseSpace** | Per-case workspace — structures evidence, facts, timelines, contradictions, and gaps from uploaded case documents |
| ✍️ **Drafting Engine** | AI-assisted drafting (bail applications, petitions, etc.), aware of the IPC → BNS transition, verification-first |
| 📋 **Universal Drafting Studio** | Structured, schema-driven drafting across 60+ Indian legal document types — no generic chatbot flow |
| 🤝 **Collaboration** | Teams, matters, role-based access, ethical walls, and auditability for firms |

Built on `FastAPI` · `PostgreSQL + pgvector` · `HNSW` · multi-stage LLM pipelines (small models for triage, larger models with validation for deep reasoning) — because a hallucinated legal authority isn't a minor bug. Currently pre-launch, heading toward a private beta with a focused group of litigation and criminal-law practitioners.

<a href="https://www.madhav-ai.com/"><img src="https://img.shields.io/badge/Visit_Madhav.ai-3457F5?style=flat-square&logo=googlechrome&logoColor=white" /></a>

---

**🧠 MemoryOS**
My flagship open-source project, built on the side — a local-first, model-agnostic, three-tier AI memory library, published on PyPI as `memoryos-local`. Built so any LLM application can retain context, preferences, and decisions without shipping user data to someone else's server.

`Python` `Local-First` `PyPI`

<a href="https://pypi.org/project/memoryos-local/"><img src="https://img.shields.io/pypi/v/memoryos-local?color=3457F5&label=PyPI&style=flat-square" /></a>
<a href="https://github.com/aryan-iconic/MemoryOS"><img src="https://img.shields.io/badge/View_Repository-12172B?style=flat-square" /></a>

---

### 📁 EXHIBIT B — Evidence (Docket Activity)

<div align="center">
<img src="https://raw.githubusercontent.com/aryan-iconic/aryan-iconic/main/metrics.svg" width="100%" />
</div>

<div align="center">
<img src="https://streak-stats.demolab.com?user=aryan-iconic&theme=dark&hide_border=true&background=12172B&stroke=1E3A8A&ring=3457F5&fire=6C8CFF&currStreakLabel=FFFFFF" />
</div>

<div align="center">

<!-- snake animation — see setup note below -->
<img src="https://raw.githubusercontent.com/aryan-iconic/aryan-iconic/output/github-contribution-grid-snake-dark.svg" width="100%" />

</div>

<details>
<summary><b>⚙️ One-time setup for the metrics card above (click to expand)</b></summary>

<br/>

The old <code>github-readme-stats.vercel.app</code> cards are gone — that shared public instance is chronically rate-limited (it hits GitHub's own API quota because everyone uses the same demo URL), which is why they showed as broken images. This replaces both cards with one self-generating <b>metrics.svg</b> baked directly into your repo, so nothing depends on a stranger's server being up.

Add this file at <code>.github/workflows/metrics.yml</code> in your <code>aryan-iconic/aryan-iconic</code> profile repo:

```yaml
name: Generate Metrics
on:
  schedule:
    - cron: "0 */6 * * *"
  workflow_dispatch:
  push:
    branches: [ main ]

permissions:
  contents: write

jobs:
  metrics:
    runs-on: ubuntu-latest
    steps:
      - uses: lowlighter/metrics@latest
        with:
          filename: metrics.svg
          token: ${{ secrets.GITHUB_TOKEN }}
          theme: dark
          base: header, activity, community, repositories
          config_timezone: Asia/Kolkata
          plugin_languages: yes
          plugin_languages_analysis_timeout: 15
          plugin_languages_limit: 8
```

It commits <code>metrics.svg</code> straight to your <code>main</code> branch on a schedule — no separate output branch needed, and no shared rate limit to hit.

<br/>

One-time setup for the snake graph below it:

```yaml
name: Generate Snake
on:
  schedule:
    - cron: "0 */6 * * *"
  workflow_dispatch:
  push:
    branches: [ main ]

permissions:
  contents: write

jobs:
  generate:
    runs-on: ubuntu-latest
    steps:
      - uses: Platane/snk@v3
        with:
          github_user_name: aryan-iconic
          outputs: |
            dist/github-contribution-grid-snake.svg
            dist/github-contribution-grid-snake-dark.svg?palette=github-dark
      - uses: crazy-max/ghaction-github-pages@v4
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```

It runs itself after that — nothing to maintain.

</details>

---

### 📁 EXHIBIT C — Tools of the Trade

<div align="center">
<img src="https://skillicons.dev/icons?i=py,ts,js,react,nextjs,fastapi,django,postgres,docker,git,github,cloudflare&theme=dark" />
</div>

---

### 📁 CLOSING ARGUMENT

<table align="center">
<tr><td align="center">

I'd rather ship one real product than demo ten toy ones. Currently building <code>Madhav.ai</code> into the operating layer for legal professionals in India, and open-sourcing <code>MemoryOS</code> for everyone else.

**Open to remote roles and open-source collaboration** — backend/AI engineering, agents, memory systems, or legal-tech. If that's you, my inbox is open.

</td></tr>
</table>

<div align="center">
<img src="https://capsule-render.vercel.app/api?type=waving&color=0:3457F5,50:1E3A8A,100:12172B&height=100&section=footer" width="100%"/>
</div>
