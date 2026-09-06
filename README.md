# Autonomous Solar Inbound Lead Engine & CRM Architecture

An automated lead qualification, scheduling, and CRM pipeline built for residential solar lead conversion. The system pairs **GoHighLevel (GHL)** for frontend funnels, pipelines, and booking calendars with an **n8n workflow engine** (self-hosted via Docker on a Hostinger VPS) for webhook handling, data normalization, and AI-driven qualification.

---

## System Architecture & Workflow

![Solar Lead Inbound CRM & AI Qualification Pipeline](./Solar%20Lead%20Inbound%20CRM%20%26%20AI%20Qualification%20Pipeline%20%28GHL%20%2B%20n8n%29.jpg)

---

## Core Problems Solved

* **Speed-to-Lead Delay:** Eliminated a 4-to-18 hour manual follow-up lag by triggering instant engagement within 30 seconds of submission.
* **Unqualified Consultations:** Prevented sales reps from wasting hours on non-viable leads (renters, sub-$100 utility bills) via automated qualification scoring.
* **Scheduling Friction:** Removed manual phone tag by embedding a direct, self-service roof survey calendar right after intake.
* **Pipeline Blindness:** Replaced scattered spreadsheets with a structured, probability-weighted 6-stage sales CRM board.

---

## Key Features

* **High-Converting Inbound Funnel:** Clean landing page with an intake form collecting homeownership status, monthly electric bill, address, and roof condition.
* **Sub-30s Speed-to-Lead SMS:** Automated two-way text dispatches immediately upon form submission with a direct link to book a site inspection.
* **Embedded Survey Calendar:** Configured 45-minute appointment slots (`solar-site-survey`) with built-in buffer times to prevent double bookings.
* **n8n Workflow Engine (Hostinger VPS / Docker):** Ingests webhooks, cleans phone formats to E.164, and uses an AI Agent node (Gemini) to evaluate and score lead quality.
* **6-Stage Opportunity Pipeline:** Automatically generates a $15,000 deal card and updates win probabilities dynamically across the sales lifecycle:
  * `New Lead` (10%)
  * `AI Qualified` (30%)
  * `Site Survey Booked` (50%)
  * `Proposal Presented` (75%)
  * `Contract Signed / Won` (100%)
  * `Disqualified / Lost` (0%)

---

## Repository Structure

```text
├── workflows/
│   └── apex-solar-n8n-workflow.json   # Exported n8n workflow JSON
├── Solar Lead Inbound CRM & AI Qualification Pipeline (GHL + n8n).jpg
├── technical-delivery-report.md       # Detailed system delivery report
└── README.md
