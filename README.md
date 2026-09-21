# CareBridge 🌿
### AI-Powered Early Health Triage for Underserved Rural Communities in India

> **College Project — Well-Being and Good Health**  
> SDG 3 (Good Health & Well-Being) · SDG 10 (Reduced Inequalities)

---

## Overview

**CareBridge** is an AI-powered early health triage assistant designed to bridge the healthcare access gap in rural India. It uses IBM Granite large language models, Retrieval-Augmented Generation (RAG), agentic AI workflows, entity extraction, summarization, and multimodal inputs to help patients describe symptoms and receive an urgency-graded triage response — all without requiring a doctor to be physically present.

CareBridge does **not** diagnose illness. It is a **decision-support and escalation tool** that empowers ASHA (Accredited Social Health Activist) workers and Primary Health Centres (PHCs) to deliver faster, smarter, and fairer first-contact care.

---

## The Problem

| Metric | Value |
|---|---|
| Rural population of India | ~65% (≈ 900 million people) |
| Rural doctor-to-patient ratio | 1 : 11,082 (WHO standard: 1 : 1,000) |
| Average travel time to district hospital | ~5 hours from remote villages |
| Preventable deaths from delayed care | ~40% of all rural preventable deaths |
| ASHA workers serving as sole health contact | 880 million+ citizens |

---

## SDG Alignment

### SDG 3 — Good Health & Well-Being
- Extends first-contact triage to the last mile
- Supports maternal & child health (Target 3.1)
- Enables management of non-communicable diseases (Target 3.4)
- Advances universal health coverage (Target 3.8)

### SDG 10 — Reduced Inequalities
- Removes geographic, linguistic, and literacy barriers to healthcare
- Ensures equitable AI performance across gender, caste, religion, and region
- Provides equal access regardless of socioeconomic status (free at point of use)

---

## Key Features

- 🎙️ **Multimodal inputs** — Voice, text, image, and document
- 🧠 **IBM Granite LLM** — Clinical reasoning and natural language understanding
- 📖 **RAG pipeline** — Grounded answers from verified MOHFW/WHO guidelines
- 🏷️ **Entity extraction** — Structured symptom, severity, and history extraction
- 📝 **Summarization** — SOAP-format case summaries for health workers
- 🤖 **Agentic workflow** — End-to-end autonomous intake-to-escalation pipeline
- 🔴🟡🟢 **Triage scoring** — Red / Yellow / Green urgency classification
- 📲 **Escalation alerts** — Automated SMS/call to ASHA workers and PHCs
- ⚖️ **Responsible AI** — Fairness auditing, explainability, human-in-the-loop

---

## Technology Stack

| Component | Technology |
|---|---|
| Foundation LLM | IBM Granite 13B Chat, Granite 8B Instruct |
| AI Platform | IBM watsonx.ai |
| RAG Vector Store | Milvus / watsonx Discovery |
| Agentic Orchestration | watsonx Orchestrate + LangGraph |
| Entity Extraction | Granite NER + UMLS medical ontology |
| Speech-to-Text | IBM Watson Speech to Text |
| Vision / Document | IBM Watson Visual Recognition + OCR |
| AI Governance | IBM watsonx.governance, AI Fairness 360 |
| Explainability | SHAP-based explanations |
| Compliance | DISHA (Digital Information Security in Healthcare Act) |
| Languages | Hindi, Tamil, Telugu, Bengali, Marathi, Gujarati, Kannada, Odia, Punjabi, Malayalam (10+) |

---

## How It Works — Triage Pipeline

```
Multimodal Input (Voice / Text / Image / Document)
        ↓
   Watson STT / OCR / Vision
        ↓
   Granite NER — Entity Extraction
   (symptoms, severity, duration, history)
        ↓
   RAG Retrieval — MOHFW / WHO Guidelines
        ↓
   Granite LLM — Urgency Reasoning
        ↓
   Agentic Workflow — Triage Scoring
   🔴 Red | 🟡 Yellow | 🟢 Green
        ↓
   Case Summary Generation (SOAP format)
        ↓
   ┌─────────────────────────────────────────┐
   │  Red  → PHC Alert + ASHA SMS + Ambulance│
   │  Yellow → ASHA notification + schedule  │
   │  Green  → Home-care guidance (local lang)│
   └─────────────────────────────────────────┘
```

---

## Responsible AI Principles

| Principle | Implementation |
|---|---|
| **No Self-Diagnosis** | Outputs are triage levels + summaries, never diagnoses |
| **Fairness** | AI Fairness 360 audits across gender, caste, region |
| **Explainability** | Human-readable rationale for every triage output |
| **Privacy** | No PII stored; E2E encryption; DISHA-compliant; session data purged |
| **Human-in-the-Loop** | All Red-level escalations reviewed by health worker before action |
| **Governance** | watsonx.governance monitors drift, bias, and accuracy in real time |

---

## Expected Impact

- **500,000+** target beneficiaries in pilot districts (Year 1)
- **< 3 minutes** average triage completion time
- **92%** target accuracy vs. PHC nurse triage benchmark
- **10+** Indian languages supported at launch
- **₹0** cost to patient — free at point of use, NHM-subsidised
- **~60%** reduction in ASHA documentation burden

---

## Project Structure

```
carebridge/
├── index.html          ← Single-page website (this project)
├── README.md           ← Project overview and documentation
└── implementation.txt  ← Technical implementation details
```

---

## Disclaimer

> CareBridge is a decision-support and early triage tool. It does **not** diagnose illness, prescribe medication, or replace qualified medical personnel. All clinical decisions remain solely with licensed healthcare professionals. The system is designed to **augment — never replace** — human judgment in healthcare delivery.

---

*Built with IBM Granite · watsonx.ai · watsonx.governance*  
*College Project — Well-Being and Good Health*
