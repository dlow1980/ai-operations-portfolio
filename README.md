# AI Operations & Automation Portfolio

Production-grade AI operations, document intelligence, intelligent agent routing, and automated research workflows engineered across the **Google Cloud (GCP) and Google Workspace ecosystems**.

---

## Executive Summary

Manual data entry, fragmented communication channels, and manual market surveillance drain enterprise bandwidth. This repository demonstrates three operational AI systems deployed with the Google ecosystem—combining **Gemini multimodal foundation models**, **Google Cloud Vertex AI**, **AppSheet Automation**, and **Google Workspace orchestration** to drive end-to-end operational efficiency.

1. **Autonomous Invoice Processing Agent:** Lowers processing turnaround from hours to seconds by pairing multimodal Gemini extraction with structured JSON schemas and AppSheet database sync.
2. **Support Ticket Triage & Resolution Router:** Streamlines Tier-1 operations via intent classification, semantic RAG search over Drive/Knowledge docs, and Google Chat/Gmail dispatch.
3. **Competitive Intelligence Gathering Agent:** Runs automated market syntheses using Google Search-grounded Gemini workflows and automatically compiles executive PDF briefs into Google Drive.

---

## Projects Matrix

| Project | Primary Stack | Core Model / Service | Business Impact | Deep Dive |
| :--- | :--- | :--- | :--- | :--- |
| **01. Invoice Agent** | Google AppSheet, Apps Script, Drive API | Gemini 1.5 / 2.0 Flash (Multimodal) | 95%+ reduction in manual entry; enforces zero-shot structured JSON extraction | [View Project](./project-1-invoice-agent/) |
| **02. Support Router** | Vertex AI Search / RAG, Gmail, Google Chat | Gemini Flash (Agent Routing & Triage) | Decreases first-touch latency (MTTR); automatically escalates priority incidents | [View Project](./project-2-customer-support-router/) |
| **03. Research Agent** | Apps Script / Cloud Functions, Google Docs | Grounded Gemini (Search Tools) | Delivers 5+ hours/week analyst savings via hands-free briefing distribution | [View Project](./project-3-competitive-research-agent/) |

---

## Project Deep Dives & Demos

### 1. Autonomous Invoice Extraction Agent
*Multimodal document pipeline parsing semi-structured invoices directly into relational Google AppSheet records.*

* **Objective:** Ingest heterogeneous invoice PDFs/images, bypass fragile legacy OCR templates, and enforce strict JSON schemas to populate relational tables and financial approval bots.
* **Google Stack:** Google Drive trigger $\rightarrow$ Apps Script / Cloud Run parser $\rightarrow$ Gemini Multimodal API with `gemini_schema.json` $\rightarrow$ AppSheet Database sync & approval bot.
* **Key Artifacts:**
  * [Workflow Architecture Blueprint](./project-1-invoice-agent/workflow_blueprint.json)
  * [Gemini Document Schema (`gemini_schema.json`)](./project-1-invoice-agent/gemini_schema.json)
  * [AppSheet Views & Audit Logs](./project-1-invoice-agent/screenshots/)
* **Video Walkthrough:** [Watch Loom Demo (3 mins)](#) *(Insert Loom link)*

---

### 2. Intelligent Support Ticket Router & Triage
*Multi-stage classification and RAG pipeline running across Google Workspace communication channels.*

* **Objective:** Parse incoming queries from Gmail and Google Chat, classify sentiment and intent, perform retrieval against Drive knowledge docs, and draft grounded responses or escalate to teams.
* **Google Stack:** Gmail/Chat Webhook $\rightarrow$ Vertex AI Search / Text Embeddings $\rightarrow$ Contextual RAG synthesis $\rightarrow$ Automated draft creation or human-in-the-loop escalation.
* **Key Artifacts:**
  * [Visual Triage Blueprint](./project-2-customer-support-router/workflow_blueprint.json)
  * [Sample Grounding Knowledge Base](./project-2-customer-support-router/knowledge_base_sample.md)
  * [Routing Logic Documentation](./project-2-customer-support-router/)
* **Video Walkthrough:** [Watch Loom Demo (4 mins)](#) *(Insert Loom link)*

---

### 3. Autonomous Competitive Research Agent
*Scheduled synthesis engine combining Google Search grounding with dynamic document generation.*

* **Objective:** Monitor competitors, industry signals, and pricing updates; generate grounded syntheses, and compile executive-ready PDF briefs exported directly to Google Drive.
* **Google Stack:** Time-driven Apps Script / Cloud Scheduler $\rightarrow$ Gemini with Google Search Grounding $\rightarrow$ Google Docs / PDF Engine $\rightarrow$ Shared Drive delivery.
* **Key Artifacts:**
  * [Workflow Execution Blueprint](./project-3-competitive-research-agent/workflow_blueprint.json)
  * [Generated Sample Briefing Report (PDF)](./project-3-competitive-research-agent/sample_briefing_report.pdf)
  * [Grounding Prompts & Methodology](./project-3-competitive-research-agent/)
* **Video Walkthrough:** [Watch Loom Demo (3 mins)](#) *(Insert Loom link)*

---

## Repository Structure

```text
ai-operations-portfolio/
│
├── README.md                           # Portfolio overview & executive summaries
│
├── project-1-invoice-agent/
│   ├── README.md                       # Process narrative & architecture diagram
│   ├── workflow_blueprint.json         # Workflow blueprint (Apps Script / n8n Google nodes)
│   ├── gemini_schema.json              # Structured JSON extraction schema
│   └── screenshots/                    # AppSheet interface & execution logs
│
├── project-2-customer-support-router/
│   ├── README.md                       # Routing logic & Vertex AI / RAG documentation
│   ├── workflow_blueprint.json         # Visual triage flow blueprint
│   └── knowledge_base_sample.md        # Reference knowledge base sample
│
└── project-3-competitive-research-agent/
    ├── README.md                       # Grounding prompts & report generation rules
    ├── workflow_blueprint.json         # Scheduled agent workflow configuration
    └── sample_briefing_report.pdf      # Autonomous output artifact
