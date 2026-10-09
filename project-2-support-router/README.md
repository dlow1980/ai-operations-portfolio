# AI Customer Support Triage & Escalation Pipeline

An automated support triage pipeline built on Make.com powered by Gemini.

## Architecture
- **Ingestion:** Webhook listener for incoming support tickets / emails.
- **Triage (Gemini):** Classifies incoming inquiries into `TIER_1` (Routine) or `TIER_2` (Urgent Escalation) using structured JSON output.
- **Tier 1 (Automated):** Fetches internal knowledge base from Google Drive and generates grounded resolution drafts.
- **Tier 2 (Escalation):** Automatically logs tickets to Google Sheets and dispatches priority alerts to team leads.

## How to Import
1. In Make.com, create a new scenario.
2. Click the `...` menu and select **Import Blueprint**.
3. Upload `blueprint.json`.
4. Connect your Google Drive, Gemini API Key, Google Sheets, and Slack/Email accounts.