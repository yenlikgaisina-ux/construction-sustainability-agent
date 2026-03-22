# Construction Sustainability Research Agent

![Python](https://img.shields.io/badge/Python-3.11-3776AB?logo=python&logoColor=white)
![CrewAI](https://img.shields.io/badge/CrewAI-0.28-FF6B35?logo=robot&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-0.1-1C3C3C?logo=chainlink&logoColor=white)
![Gemini](https://img.shields.io/badge/Gemini-1.5_Pro-4285F4?logo=google&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-2D6A4F)

> **Business Question**
> > Can a multi-agent AI system autonomously research, analyse, and synthesise up-to-date Scope 3 emissions and embodied carbon data to produce professional sustainability briefings for UK construction project teams -- reducing research time from days to minutes?
> >
> > ---
> >
> > ## Overview
> >
> > This project implements an **agentic AI pipeline** for sustainable construction management. Three specialised AI agents collaborate in sequence -- a Researcher, an Analyst, and a Report Writer -- each with distinct tools, goals, and constraints, to automate the production of structured sustainability intelligence briefings.
> >
> > **Target users:** Sustainability managers, project directors, and procurement leads at UK construction firms navigating Scope 3 reporting obligations, BREEAM certification, and embodied carbon compliance under UK Net Zero Carbon Buildings Standard.
> >
> > ---
> >
> > ## Agent Architecture
> >
> > ```
> > INPUT: Research Topic (e.g. "Scope 3 Category 1 reporting for UK subcontractors 2024")
> >          |
> >          v
> > +-------------------+  SerperDev Search Tool
> > | RESEARCHER AGENT  |---> web_search(), scrape_url()
> > |  Role: Senior     |     Finds primary sources: UKGBC, RICS,
> > |  Sustainability   |     HM Treasury, GHG Protocol docs
> > |  Researcher       |
> > +-------------------+
> >          |
> >          | raw findings (URLs, excerpts, data tables)
> >          v
> > +-------------------+  Python REPL Tool
> > |  ANALYST AGENT    |---> parse_emissions_data()
> > |  Role: Carbon     |     Cross-checks figures, identifies
> > |  Data Analyst     |     benchmarks, flags inconsistencies
> > +-------------------+
> >          |
> >          | structured analysis (tables, key metrics, gaps)
> >          v
> > +-------------------+
> > |  WRITER AGENT     |  No external tools -- pure synthesis
> > |  Role: Technical  |  Produces structured Markdown report:
> > |  Report Writer    |  Executive Summary, Findings, Actions
> > +-------------------+
> >          |
> >          v
> > OUTPUT: Professional sustainability briefing (Markdown + HTML)
> > ```
> >
> > ---
> >
> > ## Agents
> >
> > | Agent | Role | Goal | Tools |
> > |-------|------|------|-------|
> > | Researcher | Senior Sustainability Researcher | Surface current Scope 3, embodied carbon, and BREEAM regulatory data from authoritative UK sources | SerperDev Web Search, URL Scraper |
> > | Analyst | Carbon Data Analyst | Cross-reference and validate findings; extract key metrics and benchmarks; identify data gaps | Python REPL, structured data parser |
> > | Writer | Technical Report Writer | Synthesise findings into a professional, action-oriented sustainability briefing with executive summary and recommendations | None (pure synthesis) |
> >
> > ---
> >
> > ## Tasks
> >
> > | # | Task | Agent | Output |
> > |---|------|-------|--------|
> > | 1 | Search for recent regulatory guidance and industry data on the given topic | Researcher | List of 8-12 validated sources with key excerpts |
> > | 2 | Analyse extracted data: identify benchmarks, trends, inconsistencies, quantitative targets | Analyst | Structured analysis table with key metrics |
> > | 3 | Write professional briefing: Executive Summary, Regulatory Context, Key Findings, Recommended Actions | Writer | 800-1200 word Markdown briefing |
> >
> > ---
> >
> > ## Sample Research Topics
> >
> > The system has been demonstrated on the following construction sustainability topics:
> >
> > 1. **Scope 3 Category 1 -- Purchased Goods & Services** for UK general contractors (2024 reporting cycle)
> > 2. 2. **Embodied carbon benchmarks** for concrete-frame commercial buildings (RICS/LETI targets)
> >    3. 3. **Whole-life carbon assessment** requirements under UK Net Zero Carbon Buildings Standard
> >       4. 4. **BREEAM UK New Construction 2018** -- Materials and Waste credits pathway
> >          5. 5. **Circular economy procurement** strategies for demolition and fit-out waste
> >            
> >             6. ---
> >            
> >             7. ## Key Findings (Sample Output Excerpt)
> >            
> >             8. From a demonstration run on *"Scope 3 Category 1 for UK construction subcontractors, 2024"*:
> >
> > - UK construction accounts for approximately **13% of national Scope 3 emissions** through supply chain procurement (UKGBC, 2023)
> > - - The GHG Protocol Technical Guidance requires Category 1 to cover all purchased goods and services -- estimated to represent **70-80% of total Scope 3** for most contractors
> >   - - RICS Professional Standard PS3 mandates whole-life carbon reporting for projects over GBP 5M from April 2024
> >     - - Average embodied carbon for UK commercial concrete-frame buildings: **600-900 kgCO2e/m2** (LETI benchmark data 2023)
> >       - - **3 recommended agent actions** produced per briefing: data collection, procurement policy update, supplier engagement
> >        
> >         - ---
> >
> > ## Repository Structure
> >
> > ```
> > construction-sustainability-agent/
> > |-- notebook/
> > |   `-- construction_sustainability_agent.ipynb  # Main Colab notebook
> > |-- src/
> > |   |-- agents.py   # Agent definitions (roles, goals, backstory)
> > |   |-- tasks.py    # Task definitions and expected outputs
> > |   |-- tools.py    # Custom tool wrappers (search, scrape, parse)
> > |   `-- crew.py     # Crew assembly and kickoff
> > |-- outputs/
> > |   `-- sample_briefing.md  # Example agent output
> > |-- requirements.txt
> > `-- README.md
> > ```
> >
> > ---
> >
> > ## Technical Stack
> >
> > | Component | Technology |
> > |-----------|------------|
> > | Agent Framework | CrewAI 0.28 |
> > | LLM Backbone | Gemini 1.5 Pro (Google AI API) |
> > | Search Tool | SerperDev API |
> > | Orchestration | LangChain 0.1 |
> > | Data Processing | Python, pandas |
> > | Notebook | Google Colab |
> > | Output Format | Markdown + HTML |
> >
> > ---
> >
> > ## Skills Demonstrated
> >
> > `Python` `CrewAI` `LangChain` `Google Gemini API` `Agentic AI` `Multi-Agent Systems` `Prompt Engineering` `Sustainability Analytics` `Scope 3 Reporting` `Embodied Carbon` `BREEAM`
> >
> > ---
> >
> > ## Author
> >
> > Yenlik Gaisina | MPH | Cambridge Data Science with Machine Learning & AI
