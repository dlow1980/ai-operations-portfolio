# Multimodal Invoice Processing & HITL Approval Pipeline

An automated Accounts Payable (AP) ingestion pipeline built with **Make.com**, **Google Gemini**, **Google Sheets**, and **AppSheet**. This workflow eliminates manual data entry, parses multi-page PDF invoices into structured schema, and enforces financial compliance via an automated Human-in-the-Loop (HITL) approval branch.

---

## 🏗️ System Architecture

1. **Document Ingestion:** Inbound PDF invoices uploaded to Google Drive trigger the pipeline.
2. **Binary Streaming:** The document data buffer is routed to Google AI Studio.
3. **Multimodal LLM Parsing:** Google Gemini processes the binary document and extracts vendor metadata, financial figures, line-item aggregates, and tax breakdowns into strict JSON format.
4. **Conditional Routing Engine:**
   - **Total Amount < $1,000 SGD:** Directly tagged as `Auto-Approved` and queued for payment disbursement.
   - **Total Amount ≥ $1,000 SGD:** Tagged as `Pending Review` to trigger compliance controls.
5. **Database Ingestion:** Records, timestamps, and direct Google Drive file view links are synchronized into `Invoice_Master_Database` on Google Sheets.
6. **HITL Governance (AppSheet):** High-value invoices appear in a dedicated queue on a custom AppSheet mobile/web app where purchasing managers can review the line items, inspect the original PDF via Drive, and record decisions (`Approved` or `Rejected`) with a single click.

---

## 🛠️ Tech Stack & Integrations

- **Orchestration:** Make.com
- **LLM / Vision Model:** Google Gemini (via Google AI Studio API)
- **Data Store:** Google Sheets API
- **Human-in-the-Loop UI:** AppSheet
- **Storage:** Google Drive API

---

## 📊 Sample Output
| Invoice ID | Vendor Name | Invoice Date | Total Amount | Status | File Link | Processed At |

| FHO-2026-0892 | Fresh Harvest Organics | 2026-09-12 | 485.60 | Auto-Approved | 2026-09-12 |

| AGP-2026-1408 | Apex Gourmet Suppliers | 2026-09-12 | 3,292.89 | Pending Review | 2026-09-12 |

---

## 🚀 How to Import This Workflow
1. Download `blueprint.json` from this repository.
2. In Make.com, create a new scenario.
3. Click the `...` menu on the bottom bar and select **Import Blueprint**.
4. Re-authenticate your Google Drive, Google AI Studio, and Google Sheets connections.

<img width="1768" height="572" alt="Project 1 scenario flow" src="https://github.com/user-attachments/assets/9a9b78a0-349d-4eb5-ab08-caddf5d85796" />

