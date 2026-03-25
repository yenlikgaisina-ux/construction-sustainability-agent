# Construction Sustainability Research Agent

[![Python](https://img.shields.io/badge/Python-3.11-blue?logo=python)](https://python.org)
[![Status](https://img.shields.io/badge/Status-Complete-brightgreen)]()
[![Framework](https://img.shields.io/badge/Framework-CrewAI-orange)]()
[![LLM](https://img.shields.io/badge/LLM-Gemini%201.5%20Pro-purple)]()
[![License](https://img.shields.io/badge/License-MIT-2D6A4F)]()

> Automating UK construction sustainability research using a three-agent CrewAI pipeline -- from raw query to structured briefing in under 10 minutes.

---

## Business Question

> "Can a multi-agent AI system autonomously research, analyse, and synthesise Scope 3 and embodied carbon intelligence for UK construction projects -- reducing research time from days to minutes?"

UK construction sustainability managers and project directors spend significant time manually researching Scope 3 emissions data, embodied carbon benchmarks, and regulatory requirements from fragmented sources (UKGBC, RICS, HM Treasury, GHG Protocol). This project automates that research pipeline using a three-agent CrewAI system.

---

## Agent Architecture

Each agent has a defined role, goal, and set of tools. They run sequentially:

```
INPUT: Research topic (e.g. "Scope 3 Category 1 for UK construction subcontractors 2024")
         |
         v
+-------------------+  Tools: web_search, scrape_url
| RESEARCHER AGENT  |  Finds primary sources: UKGBC, RICS,
|  Senior           |  HM Treasury, GHG Protocol
|  Sustainability   |
|  Researcher       |
+-------------------+
         |
         | raw findings (URLs, excerpts, data tables)
         v
+-------------------+  Tools: Python REPL
|  ANALYST AGENT    |  Cross-checks figures, identifies
|  Carbon Data      |  benchmarks, flags inconsistencies
|  Analyst          |
+-------------------+
         |
         | structured analysis (key metrics, gaps)
         v
+-------------------+  No external tools
|  WRITER AGENT     |  Synthesises: Executive Summary,
|  Technical Report |  Key Findings, Regulatory Context,
|  Writer           |  Recommended Actions
+-------------------+
         |
         v
OUTPUT: Structured Markdown briefing (delivered in under 10 minutes)
```

---

## Agents

| Agent | Role | Goal |
|-------|------|------|
| Researcher | Senior Sustainability Researcher | Surface current Scope 3, embodied carbon, and regulatory guidance from live UK sources |
| Analyst | Carbon Data Analyst | Cross-reference and validate findings; extract key metrics and identify data gaps |
| Writer | Technical Report Writer | Synthesise findings into a professional, action-oriented sustainability briefing |

---

## Tasks

| Task | Agent | Output |
|------|-------|--------|
| Search for recent regulatory guidance and industry data on the given topic | Researcher | List of verified sources with excerpts |
| Analyse extracted data: identify benchmarks, trends, inconsistencies, quantitative targets | Analyst | Structured summary with flagged gaps |
| Write professional briefing: Executive Summary, Regulatory Context, Key Findings, Recommended Actions | Writer | Final Markdown report |

---

## Key Findings

| Metric | Value |
|--------|-------|
| Agents in pipeline | 3 (Researcher, Analyst, Writer) |
| Sources consulted per run | 8--12 live regulatory sources |
| End-to-end briefing time | Under 10 minutes |
| Recommended actions per briefing | 3 concrete next steps |
| Research topics tested | 5 construction sustainability topics |
| Manual research time saved | Estimated >95% vs traditional desk research |

The pipeline consistently produced structured, source-cited briefings on Scope 3, embodied carbon, and BREEAM topics. The Analyst agent's cross-checking step materially improved output quality by flagging inconsistencies between sources before the Writer synthesised them.

---

## Sample Research Topics

The system has been run on the following construction sustainability topics:

1. Scope 3 Category 1 -- Purchased Goods & Services for UK general contractors (2024 reporting cycle)
2. Embodied carbon benchmarks for concrete-frame commercial buildings (RICS/LETI targets)
3. Whole-life carbon assessment requirements under UK Net Zero Carbon Buildings Standard
4. BREEAM UK New Construction 2018 -- Materials and Waste credits pathway
5. Circular economy procurement strategies for demolition and fit-out waste

---

## Technical Stack

| Component | Technology |
|-----------|------------|
| Agent Framework | CrewAI |
| LLM Backbone | Gemini 1.5 Pro (Google AI API) |
| Search Tool | SerperDev API |
| Orchestration | LangChain |
| Data Processing | Python, pandas |
| Notebook | Google Colab |
| Output Format | Markdown |

---

## Repository Structure

```
construction-sustainability-agent/
|-- notebook/
|   +-- construction_sustainability_agent.ipynb
+-- README.md
```

---

## Skills Demonstrated

`Python` `CrewAI` `LangChain` `Google Gemini API` `Agentic AI` `Multi-Agent Systems` `Prompt Engineering` `Scope 3 Emissions` `Embodied Carbon` `Construction Sustainability`

---

## Author

**Yenlik Gaisina** | Data & Analytics Consultant | Cambridge Data Science with ML & AI Programme

[LinkedIn](https://www.linkedin.com/in/yenlik-gaisina/) | [Portfolio](https://gaisina.co.uk/portfolio.html)
