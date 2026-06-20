# README_FIRST

# SentinelX

### Responsible AI-Assisted Organizational Threat Triage Platform

Track: USAII Hackathon — Track A
Project Name: SentinelX
Project Type: AI-Assisted Organizational Safety & Threat Intelligence Platform

---

# 1. Project Overview

SentinelX is a responsible AI-assisted organizational threat triage platform designed for NGOs, intervention organizations, safety teams, and investigators supporting vulnerable individuals facing:

* cyber-harassment,
* coercion,
* stalking,
* grooming,
* sextortion,
* contextual abuse,
* and physical safety threats.

The platform combines:

* contextual Natural Language Processing (NLP),
* Explainable AI synthesis,
* human-supervised threat analysis,
* and structured organizational workflows

to help organizations transform fragmented safety signals into actionable contextual intelligence while preserving human accountability in high-stakes intervention environments.

SentinelX was intentionally designed around one principle:

> AI should assist human judgment in sensitive safety environments — not replace it.

The system therefore enforces:

* explicit human-triggered analysis,
* explainable AI outputs,
* non-autonomous escalation,
* and analyst-controlled intervention workflows.

---

# 2. The Problem We Are Solving

Organizations protecting vulnerable individuals often receive fragmented safety signals arriving through different channels:

* panic alerts,
* incomplete narratives,
* voice reports,
* screenshots,
* evidence uploads,
* or contextual descriptions of escalating abuse.

These reports are frequently:

* disconnected,
* difficult to prioritize,
* time-sensitive,
* and emotionally complex.

Traditional reporting systems rely heavily on:

* manual interpretation,
* static forms,
* or keyword-based systems

which struggle to understand:

* escalation patterns,
* contextual coercion,
* repeated harassment,
* grooming behaviors,
* or narrative progression.

This creates a major operational challenge for NGO analysts and investigators who must decide:

* which cases require immediate attention,
* which situations show escalation patterns,
* and how to allocate limited organizational resources responsibly.

SentinelX was built specifically for:

* NGO analysts,
* intervention caseworkers,
* digital safety organizations,
* and protection-focused institutions

who need structured contextual intelligence without surrendering decision-making authority to autonomous systems.

---

# 3. Core Innovation

What makes SentinelX different is not just the use of AI — it is how the AI is controlled.

Unlike autonomous surveillance or fully automated intervention systems, SentinelX enforces a strict human-supervised workflow where:

* AI never escalates cases automatically,
* AI never contacts authorities,
* AI never performs autonomous intervention,
* and all real-world decisions remain human-controlled.

The platform introduces several core innovations:

## Human-Gated AI Analysis

Incoming reports remain inactive until an authorized analyst explicitly initiates AI processing through the dashboard.

## Structured Safe Chat Intake

Instead of overwhelming vulnerable users with long forms, SentinelX uses a guided 4-Step contextual intake system that improves:

* clarity,
* contextual consistency,
* and explainability.

## Explainable AI Synthesis

The platform produces:

* contextual synthesis reports,
* escalation reasoning,
* and explainable intelligence summaries

instead of opaque black-box classifications.

## Multi-Signal Organizational Workflow

SentinelX unifies:

* SOS alerts,
* contextual voice threat signals,
* and Safe Chat reports

into a single triaged organizational dashboard.

## Responsible AI Governance

The architecture was intentionally designed to reduce:

* automation bias,
* over-reliance on AI,
* uncontrolled surveillance,
* and non-consensual analysis.

---

# 4. System Workflow

SentinelX operates through three distinct signal pipelines.

---

# A. SOS Flow (No AI)

The SOS system is intentionally simple and direct.

### Workflow

1. User long-presses the SOS button for 3 seconds
2. Emergency alert is immediately sent
3. Alert is routed to:

   * emergency contacts
   * NGO dashboard
4. Dashboard receives:

   * user details
   * timestamp
   * location information
5. Human analysts determine next steps

### Important Design Choice

The SOS pipeline uses no AI analysis.

This was intentional because emergency escalation must remain:

* immediate,
* deterministic,
* and human-controlled.

---

# B. Detect Threat Flow (On-Device AI)

Detect Threat is an optional user-controlled listening mode.

### Workflow

1. User manually enables Detect Threat
2. Audio is captured locally on-device
3. Audio is transcribed into text
4. Original audio is immediately discarded
5. Only transcription text is processed
6. On-device Bi-LSTM model classifies:

   * threat
   * or non-threat
7. If classified as threat:

   * a signal is sent to the dashboard
8. Human analyst reviews the signal

### Important Privacy Design

* Audio is never stored
* Audio is never uploaded
* Audio is discarded immediately after transcription

Only the text classification result leaves the device.

---

# C. Safe Chat + Evidence Flow

Safe Chat is a guided reporting system designed for vulnerable users experiencing:

* coercion,
* stalking,
* digital exploitation,
* grooming,
* sextortion,
* or contextual abuse.

The workflow was intentionally designed to reduce stress during reporting.

---

## Step 1 — Category Selection

User selects:

* stalking,
* harassment,
* coercion,
* physical tracking,
* exploitation,
* or related contexts.

---

## Step 2 — Narrative Description

User describes the situation in free text.

---

## Step 3 — Timing Context

User selects:

* today,
* this week,
* or months ago.

---

## Step 4 — Frequency Context

User selects:

* first time,
* a few times,
* or repeated escalation.

---

## Evidence Upload

Users may optionally upload:

* images,
* voice notes,
* videos,
* or supporting files.

---

## Human-Gated AI Processing

After submission:

* reports are stored as:

  > Pending Analysis

No AI processing occurs automatically.

Only when an analyst clicks:

> [Analyze Report]

does the system:

1. retrieve the contextual report,
2. prepare the evidence payload,
3. initiate contextual AI analysis,
4. generate explainable synthesis outputs,
5. and update the dashboard.

---

# 5. Organizational Dashboard

The NGO Dashboard is the operational center of SentinelX.

It was designed specifically for:

* analysts,
* investigators,
* safety teams,
* and intervention organizations.

The dashboard provides:

* real-time alerts,
* structured report triage,
* explainable AI synthesis,
* contextual escalation summaries,
* evidence review,
* and analyst-controlled case management.

---

# Dashboard Capabilities

## Real-Time Alert Queue

Displays:

* SOS alerts,
* Detect Threat signals,
* Safe Chat reports,
* timestamps,
* priority states,
* and contextual categories.

---

## Human-Controlled Analysis

Every report contains an explicit:

> [Analyze Report]

button.

AI analysis only occurs after this deliberate analyst action.

---

## Explainable AI Panel

After analysis, the dashboard surfaces:

* contextual synthesis reports,
* escalation indicators,
* risk observations,
* narrative reasoning,
* and explainable intelligence outputs.

---

## Case Review Workflow

Analysts can:

* review,
* prioritize,
* acknowledge,
* resolve,
* or close cases.

---

# 6. Responsible AI Design

Responsible AI governance was one of the central architectural priorities of SentinelX.

The platform was intentionally designed to avoid:

* autonomous intervention,
* opaque decision-making,
* uncontrolled monitoring,
* and over-reliance on AI.

---

# Human-in-the-Loop Oversight

SentinelX intentionally does NOT:

* contact authorities autonomously,
* escalate cases automatically,
* trigger enforcement actions,
* or make final intervention decisions.

Humans remain responsible for:

* contextual interpretation,
* intervention decisions,
* escalation review,
* and organizational accountability.

---

# Explainability

Instead of black-box outputs, the platform generates:

* explainable synthesis reports,
* contextual reasoning,
* escalation observations,
* and structured summaries.

This helps analysts understand:

* why a signal was surfaced,
* what contextual patterns were detected,
* and how the AI reasoning process contributed to analysis.

---

# Privacy Protection

The system was intentionally designed around consent and minimal data exposure.

### Detect Threat Safeguards

* Audio discarded after transcription
* Audio never stored
* Audio never uploaded
* Classification occurs locally

### Evidence Analysis Safeguards

* No automatic evidence analysis
* Human-triggered review only
* Explicit analyst authorization required

---

# Reduction of Automation Bias

To reduce over-reliance on AI:

* analysis requires manual initiation,
* outputs remain advisory,
* and analysts remain final decision-makers.

The AI supports organizational reasoning rather than replacing it.

---

# 7. AI Architecture Summary

SentinelX combines multiple AI systems within a human-supervised organizational workflow.

---

# AI Components

## Contextual NLP

Used for:

* threat understanding,
* contextual interpretation,
* escalation analysis,
* and narrative synthesis.

---

## Bi-LSTM Threat Classification

Used within Detect Threat mode for:

* contextual language classification,
* on-device threat prediction,
* and spoken threat recognition.

---

## Gemini API Contextual Synthesis

Used for:

* evidence analysis,
* contextual synthesis generation,
* explainable reporting,
* and organizational intelligence workflows.

---

# Backend Infrastructure

Built using:

* Python
* Flask
* MongoDB
* WebSockets / Socket.IO
* JWT Authentication

---

# Frontend & Mobile

Built using:

* React Native Expo

Dashboard UI supports:

* analyst review workflows,
* real-time triage,
* and explainable intelligence rendering.

---

# 8. Tech Stack

| Layer            | Technology        |
| ---------------- | ----------------- |
| Mobile App       | React Native Expo |
| Backend          | Flask             |
| Database         | MongoDB           |
| AI Model         | Bi-LSTM           |
| AI APIs          | Gemini API        |
| Authentication   | JWT               |
| Real-Time Events | Socket.IO         |
| Hosting          | Railway           |
| Maps             | Mapbox            |

---

# 9. Prototype Status

Current Stage:

* Functional prototype
* Organizational dashboard operational
* Mobile app operational
* AI analysis workflow operational
* Real-time alerting operational
* Pilot testing stage

Additional optimization and scaling are ongoing.

---

# 10. Team Information

| Team Member | Role                                               |
| ----------- | -------------------------------------------------- |
| Fredrick    | Team Lead, System Architecture, AI Workflow Design |
| Tomna       | AI Engineer & Backend AI Integration               |
| Solomon     | Mobile App Developer                               |
| Habeeb      | UI/UX Designer                                     |

---

# 11. AI Tools Used

Development involved:

* Gemini API
* TensorFlow
* Keras
* ChatGPT
* GitHub Copilot
* Claude
* Google Gemini
* Lovable

Lovable was used primarily for:

* dashboard workflow ideation,
* UI inspiration,
* and organizational interface exploration.

---

# 12. Recommended Review Order

## 1. Demo Video

Watch the project walkthrough first.

Location:
`/Demo/`

---

## 2. Pitch Deck

Contains:

* architecture,
* workflow,
* and responsible AI design.

Location:
`/Pitch_Deck/`

---

## 3. APK / Mobile Prototype

Demonstrates:

* SOS,
* Detect Threat,
* and Safe Chat workflows.

Location:
`/Prototype/`

---

## 4. Dashboard Screenshots

Shows:

* triage queue,
* XAI synthesis,
* and analyst workflows.

Location:
`/Dashboard_Screens/`

---

# 13. Future Vision

The long-term vision for SentinelX is to become a scalable responsible AI infrastructure supporting:

* NGOs,
* intervention organizations,
* campus safety systems,
* and protection-focused institutions.

Future goals include:

* multilingual contextual analysis,
* stronger explainable AI workflows,
* collaborative organizational triage systems,
* improved contextual risk modeling,
* and broader accessibility for low-resource organizations.

---

# 14. Final Note

SentinelX was built around the belief that AI should strengthen human judgment in sensitive intervention environments rather than replace it.

Every major architectural decision in the platform was intentionally designed to preserve:

* accountability,
* explainability,
* privacy,
* and human oversight.

Our goal is not autonomous intervention.

Our goal is helping organizations detect contextual risk earlier while ensuring humans remain fully in control of what happens next.
