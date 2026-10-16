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
| **01. Invoice Agent** | Google AppSheet, Apps Script, Drive API | Gemini 3.5 Flash (Multimodal) | 95%+ reduction in manual entry; enforces zero-shot structured JSON extraction | [View Project](./project-1-invoice-agent/) |
| **02. Support Router** | Vertex AI Search / RAG, Gmail, Google Chat | Gemini 3.5 Flash (Agent Routing & Triage) | Decreases first-touch latency (MTTR); automatically escalates priority incidents | [View Project](./project-2-support-router/) |
| **03. Research Agent** | Apps Script / Cloud Functions, Google Docs | Grounded Gemini (Search Tools) | Delivers 5+ hours/week analyst savings via hands-free briefing distribution | [View Project](./project-3-market-intelligence-agent/) |

---

## Project Deep Dives & Demos

### 1. Autonomous Invoice Extraction Agent
*Multimodal document pipeline parsing semi-structured invoices directly into relational Google AppSheet records.*

* **Objective:** Ingest heterogeneous invoice PDFs/images, bypass fragile legacy OCR templates, and enforce strict JSON schemas to populate relational tables and financial approval bots.
* **Google Stack:** Google Drive trigger $\rightarrow$ Apps Script / Cloud Run parser $\rightarrow$ Gemini Multimodal API $\rightarrow$ AppSheet Database sync & approval bot.
* **Key Artifacts:**
  * [Workflow Architecture Blueprint](project-1-invoice-agent/blueprint.json)
  * [Assets Workflow](project-1-invoice-agent/assets)
---

### 2. Intelligent Support Ticket Router & Triage
*Multi-stage classification and RAG pipeline running across Google Workspace communication channels.*

* **Objective:** Parse incoming queries from Gmail and Chat, classify sentiment and intent, perform retrieval against Drive knowledge docs, and draft grounded responses or escalate to teams.
* **Google Stack:** Chat Webhook $\rightarrow$ Vertex AI Search / Text Embeddings $\rightarrow$ Contextual RAG synthesis $\rightarrow$ Automated draft creation or human-in-the-loop escalation.
* **Key Artifacts:**
  * [Visual Triage Blueprint](./project-2-support-router/blueprint.json)
  * [Sample and FAQ](./project-2-support-router/samples/customer-support-FAQ.md)
 ---

### 3. Autonomous Competitive Research Agent
*Scheduled synthesis engine combining Google Search grounding with dynamic document generation.*

* **Objective:** Monitor competitors, industry signals, and pricing updates; generate grounded syntheses, and compile executive-ready PDF briefs exported directly to Google Drive.
* **Google Stack:** Time-driven Apps Script / Cloud Scheduler $\rightarrow$ Gemini with Google Search Grounding $\rightarrow$ Google Docs / PDF Engine $\rightarrow$ Shared Drive delivery.
* **Key Artifacts:**
  * [Workflow Free RSS Blueprint](./project-3-market-intelligence-agent/workflows/blueprint-free-rss.json)
  * [Workflow Google Grounding Blueprint](./project-3-market-intelligence-agent/workflows/blueprint-pro-search-grounding.json)
  * [Generated Sample Briefing Report](./project-3-market-intelligence-agent/sample/email-1.png)
 
 
---

## Repository Structure

```text
ai-operations-portfolio/
│
├── README.md                           # Portfolio overview & executive summaries
│
├── project-1-invoice-agent/
│   ├── README.md                       # Process narrative & architecture diagram
│   ├── blueprint.json                  # blueprint (Apps Script)
│   ├── Asset                           # Structured workflow interface
│   └── Sample                          # Sample
│
├── project-2-customer-support-router/
    ├── README.md                       # Routing logic & Vertex AI / RAG documentation
    ├── blueprint.json                  # Visual triage flow blueprint
    └── sample                          # Reference knowledge base sample
