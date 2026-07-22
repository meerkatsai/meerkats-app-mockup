# Meerkats.ai — Product Mockup

Hi-fidelity interactive mockup of the Meerkats.ai growth intelligence product.

A single self-contained `index.html` — no build step, no dependencies.

## Structure

- **Chat** — conversational entry point, with History, Automations, and Library
- **Core Activities** — Cockpit, CRM (My Queue, All Leads, Team, Performance), Marketing Acquisition, Creative Analysis, Website Conversion, Customer Retention, Discovery
- **Data** — Data Spine (Dashboard, CDP Analytics, Ad Performance, Ingest Events, Google, Meta, Shopify, Attribution), Integrations, Settings

## Run locally

```bash
python3 serve.py
```

Then open http://localhost:4710

## Deploy

Static site — deploys to Vercel as-is with no configuration.
