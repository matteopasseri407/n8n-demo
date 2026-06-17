# n8n Lead Qualifier — 65-Node Workflow Demo

**Public portfolio proof for AI automation, workflow orchestration, and agentic operations roles.**

---

## 🇬🇧 English

### What It Does

A self-hosted n8n workflow that automates the full B2B lead pipeline — from first inquiry to CRM update — with zero manual triage.

### The Problem

The intake form was receiving a flood of inquiries — most of them spam, noise, or barely coherent requests. Manual triage became impossible, and real paying clients were getting buried in the mess. There was also no way to recover leads who started the form but never finished it.

### What I Built

A **65-node** n8n workflow running on **Oracle Cloud / PostgreSQL** that classifies and scores inbound leads with LLM evaluation (Groq) for relevance, intent, and budget signals, routes inquiries via email triage with auto-tags for low-fit leads and priority flags for hot ones, updates the CRM (Notion) automatically with status, score, and classification notes, detects duplicates across multiple intake channels, sends real-time Telegram alerts for serious leads, handles fallback and recovery with automatic LLM retries and crash-proof webhooks, and follows up on abandoned forms with an automated recovery mechanism that brings back leads who dropped off before completing the funnel.

### Stack

`n8n` · `PostgreSQL` · `Groq (LLM)` · `Notion API` · `Telegram Bot API` · `Oracle Cloud` · `Docker`

### Screenshot

![Lead Qualifier Workflow](screenshots/lead-qualifier-overview.jpg)

---

## 🇮🇹 Italiano

### Cosa Fa

Un workflow n8n self-hosted che automatizza l'intera pipeline lead B2B — dal primo contatto all'aggiornamento CRM — senza triage manuale.

### Il Problema

Il form di contatto riceveva un diluvio di richieste — per lo più spam, rumore o richieste confuse. Il triage manuale era diventato insostenibile e i clienti paganti veri finivano sepolti nel casino. Inoltre non c'era modo di recuperare i lead che iniziavano il form senza completarlo.

### Cosa Ho Costruito

Un workflow n8n da **65 nodi** su **Oracle Cloud / PostgreSQL** che classifica e valuta i lead in ingresso con LLM (Groq) per pertinenza, intento e segnali di budget, instrada le richieste via triage email con auto-tag per lead a basso fit e flag di priorità per quelli caldi, aggiorna il CRM (Notion) automaticamente con stato, punteggio e note di classificazione, rileva duplicati tra più canali di acquisizione, invia notifiche Telegram in tempo reale per i lead seri, gestisce fallback e recovery con retry automatici delle chiamate LLM e webhook anti-crash, e segue i form abbandonati con un meccanismo di recupero automatico che riporta dentro i lead persi prima di completare il funnel.

### Stack

`n8n` · `PostgreSQL` · `Groq (LLM)` · `Notion API` · `Telegram Bot API` · `Oracle Cloud` · `Docker`

### Screenshot

![Lead Qualifier Workflow](screenshots/lead-qualifier-overview.jpg)

---

## Context

This workflow was originally built and operated in production for **ME3Design** (2024–2026), where it handled live B2B lead intake for an additive manufacturing operation. The screenshot shown here is a sanitized copy of the same architecture, now adapted to run a public portfolio funnel at [aienabledops.it](https://www.aienabledops.it).

---

## Perché è rilevante / Why This Matters

Non è il clone di un tutorial. È un workflow che ha girato in produzione su operazioni aziendali reali — il tipo di automazione end-to-end che questo portfolio esiste per dimostrare.

This isn't a tutorial clone. It's a production workflow that ran daily on live business operations — the kind of end-to-end automation this portfolio exists to prove.
