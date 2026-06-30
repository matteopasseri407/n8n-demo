# n8n Lead Qualifier (65-node AI workflow)

A public, sanitized case study for AI automation, workflow orchestration, and operations roles.

![Lead Qualifier Workflow](screenshots/lead-qualifier-overview.jpg)

## What it is

A sanitized public demo of a real n8n lead qualification system, originally built and run for live B2B intake at ME3Design. It takes a lead from first inquiry to CRM record:

- pre-filters noisy or incomplete submissions before any LLM call
- checks for duplicate leads across intake channels
- enriches a submission with website and social context
- scores quality, intent, and budget signals with Groq
- updates the Notion CRM with status, score, and notes
- sends Telegram alerts for high-priority leads and for operational issues
- handles Calendly booking and cancellation events
- recovers abandoned forms with a delayed follow-up
- keeps fallback and recovery paths separate from the happy path

## Problem

The intake form took in too many low-quality, incomplete, or spammy requests for manual triage to stay reliable. Serious B2B opportunities got buried, duplicates were hard to track, and an abandoned form went nowhere. The point wasn't only to classify leads. It was to make the funnel safer to operate: fewer missed opportunities, fewer duplicate records, clearer handoffs for the prospects that mattered.

## Architecture highlights

| Area | Implementation |
| --- | --- |
| Intake | Webhook-based lead capture with deterministic pre-filtering |
| Deduplication | Notion lookup before creating or updating a record |
| Enrichment | Homepage, about-page, and social-context fetches when available |
| AI scoring | Groq LLM call with structured parsing and fallback handling |
| CRM | Notion records updated with status, score, classification, and notes |
| Alerts | Telegram notifications for hot leads, bookings, cancellations, and errors |
| Booking lifecycle | Calendly booked and canceled webhooks tied to lead records |
| Recovery | Delayed drop-off checks and a follow-up path for incomplete submissions |
| Resilience | Retry and fallback branches, crash-resistant webhook responses |

## Stack

`n8n` · `PostgreSQL` · `Groq` · `Notion API` · `Telegram Bot API` · `Calendly Webhooks` · `Oracle Cloud` · `Docker`

## What it shows

The point is end-to-end automation judgment rather than prompt writing:

- deterministic rules paired with LLM scoring, instead of sending everything to the model
- a design built around states, exceptions, retries, duplicates, and recovery
- several operational tools wired into one workflow
- a system that supports a real business handoff, not a form demo

## Public demo note

No credentials, customer data, production webhook URLs, or internal records are in this repository. The screenshot is a sanitized view of the workflow adapted for portfolio use.

## Sintesi in italiano

Workflow n8n self-hosted da 65 nodi per qualificare lead B2B: aggiorna il CRM Notion, rileva i duplicati, gestisce le prenotazioni Calendly, manda alert Telegram e recupera i form abbandonati.

Il valore non è il lead scoring con LLM da solo, ma l'orchestrazione completa: pre-filtri deterministici, fallback, retry, deduplica, recovery e handoff operativo. Non è un clone di tutorial, è la versione pubblica e sanificata di un sistema costruito per operazioni reali.
