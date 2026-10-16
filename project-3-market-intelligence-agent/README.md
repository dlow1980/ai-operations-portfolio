# Autonomous Market & Competitive Intelligence Agent

An automated weekly briefing pipeline built on [Make.com](https://make.com) that extracts live market movements, synthesizes them using **Gemini**, and delivers a formatted HTML digest directly to executive leads via Gmail.

## Architecture

```
[ Scheduled Trigger ] ──> [ Google News / RSS ] ──> [ Text Aggregator ] ──> [ Gemini API (HTML Synthesis) ] ──> [ Gmail Distribution ]
```

## Versions Included

| Version | Data Ingestion | Gemini Role | Cost Tier |
| :--- | :--- | :--- | :--- |
| **Free (Default)** | Google News RSS Feed | Text Synthesis & HTML Formatting | **100% Free** |
| **Pro (Alternative)** | Google Search Grounding Tool | Live Search + Synthesis + Citations | Google AI Pay-as-you-go |

## Quickstart & Installation

1. Clone or download this repository.
2. In [Make.com](https://make.com), create a new scenario and select **Import Blueprint**.
3. Choose `workflows/blueprint-free-rss.json`.
4. Open module **HTTP: Make a request**:
   - Update the URL with your Gemini API key
   `https://generativelanguage.googleapis.com/v1beta/models/gemini-3.5-flash:generateContent?key=YOUR_API_KEY`
5. Connect your own Gmail account in module **Gmail: Send an Email**.
6. Set your recipient address and click **Run Once** to test.

## Environment & Secrets Notice
Never commit real API keys or personal emails into Make blueprints. Ensure placeholder tokens (`YOUR_API_KEY`) are configured upon import.