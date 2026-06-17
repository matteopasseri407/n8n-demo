# n8n Lead Qualifier - 65-Node AI Workflow

Public portfolio case study for AI automation, workflow orchestration, and operations engineering roles.

![Lead Qualifier Workflow](screenshots/lead-qualifier-overview.jpg)

## Portfolio Snapshot

This is a sanitized public demo of a real n8n lead qualification system originally built and operated for live B2B intake at **ME3Design**.

It automates the lead pipeline from first inquiry to CRM update:

- pre-filters noisy or incomplete submissions before using an LLM
- checks duplicate leads across intake channels
- enriches submissions with website and social context
- scores lead quality, intent, and budget signals with Groq
- updates Notion CRM records with status, score, and notes
- sends Telegram alerts for high-priority leads and operational issues
- handles Calendly booking and cancellation events
- recovers abandoned forms with a delayed follow-up path
- keeps fallback and recovery paths separate from the happy path

## Problem

The intake form was receiving too many low-quality, incomplete, or spammy requests for manual triage to stay reliable. Serious B2B opportunities risked being buried, duplicates were hard to track, and abandoned forms had no recovery path.

The goal was not just to classify leads, but to make the funnel operationally safer: fewer missed opportunities, fewer duplicate records, and clearer handoffs for serious prospects.

## Architecture Highlights

| Area | Implementation |
| --- | --- |
| Intake | Webhook-based lead capture with deterministic pre-filtering |
| Deduplication | Notion lookup before creating or updating lead records |
| Enrichment | Homepage, about-page, and social-context fetches when available |
| AI scoring | Groq LLM call with structured parsing and fallback handling |
| CRM | Notion records updated with lead status, score, classification, and notes |
| Alerts | Telegram notifications for hot leads, bookings, cancellations, and errors |
| Booking lifecycle | Calendly booked/canceled webhooks connected to lead records |
| Recovery | Delayed drop-off checks and follow-up path for incomplete submissions |
| Resilience | Retry/fallback branches and crash-resistant webhook responses |

## Stack

`n8n` · `PostgreSQL` · `Groq` · `Notion API` · `Telegram Bot API` · `Calendly Webhooks` · `Oracle Cloud` · `Docker`

## What This Demonstrates

This project is meant to show end-to-end automation judgment, not just prompt writing:

- combining deterministic rules with LLM scoring instead of sending everything to the model
- designing around states, exceptions, retries, duplicates, and recovery
- integrating multiple operational tools into one workflow
- building a system that supports real business handoff, not just a form demo

## Public Demo Note

No credentials, private customer data, production webhook URLs, or internal records are included in this repository. The screenshot shows a sanitized version of the workflow architecture adapted for portfolio use.

## Sintesi in Italiano

Workflow n8n self-hosted da **65 nodi** per qualificare lead B2B, aggiornare il CRM Notion, rilevare duplicati, gestire prenotazioni Calendly, inviare alert Telegram e recuperare form abbandonati.

Il valore non e' solo il lead scoring con LLM, ma l'orchestrazione completa: pre-filtri deterministici, fallback, retry, deduplica, recovery e handoff operativo.

Questo non e' un clone di tutorial: e' una versione pubblica e sanificata di un sistema costruito per operazioni aziendali reali.
