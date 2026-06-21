# SentinelX

## AI-Assisted Organizational Threat Triage Platform

SentinelX is a responsible AI-assisted organizational threat triage platform designed for NGOs, intervention organizations, investigators, and institutional safety teams supporting vulnerable individuals facing:

* stalking,
* coercion,
* cyber-harassment,
* exploitation,
* grooming,
* sextortion,
* and contextual abuse.

Rather than replacing human judgment, SentinelX was intentionally designed around **human-in-the-loop AI governance**.

The platform combines:

* contextual NLP,
* on-device threat classification,
* Explainable AI synthesis,
* and analyst-supervised intervention workflows

to help organizations transform fragmented safety signals into structured, reviewable intervention intelligence.

---

# Key Features

## 1. SOS Emergency Escalation

A non-AI emergency flow where users can trigger urgent alerts through a 3-second long press.

Alerts are routed directly to:

* emergency contacts,
* NGO dashboards,
* and intervention review queues.

---

## 2. Detect Threat (On-Device NLP)

A contextual spoken-threat detection pipeline using:

* speech transcription,
* on-device Bi-LSTM classification,
* and contextual NLP threat detection.

### Important Privacy Design

Audio is:

* never stored,
* never uploaded,
* and discarded immediately after transcription.

Only the classification result is transmitted.

---

## 3. Safe Chat + Evidence Upload

A guided 4-step contextual reporting system that allows users to:

* describe incidents,
* categorize abuse scenarios,
* indicate escalation patterns,
* and upload evidence files.

Reports remain inactive until an NGO analyst explicitly requests AI analysis.

---

## 4. Human-in-the-Loop AI Workflow

SentinelX intentionally prevents autonomous intervention.

AI:

* does NOT contact authorities,
* does NOT escalate cases,
* does NOT make enforcement decisions.

Human analysts remain responsible for:

* interpretation,
* escalation,
* prioritization,
* and intervention decisions.

---

### Multimodal Evidence Synthesis Workflow

For Safe Chat investigations, SentinelX also supports multimodal contextual evidence analysis through Gemini-powered synthesis workflows.

When a vulnerable user submits a Safe Chat report, they may optionally attach supporting evidence such as:

* screenshots,
* chat exports,
* voice notes,
* images,
* or short videos related to coercion, grooming, cyber-harassment, sextortion, stalking, or exploitation incidents.

Importantly, these uploads are not automatically analyzed upon submission.

The evidence remains in a static:

$$
\text{Pending Analysis}
$$

state until an authorized NGO analyst intentionally initiates review from the dashboard interface.

Once the analyst clicks:

[Analyze Report]

the Flask backend retrieves:

$$
\text{Narrative Description}
+
\text{Timing Metadata}
+
\text{Frequency Indicators}
+
\text{Uploaded Evidence}
$$

and securely routes the contextual payload into the Gemini multimodal synthesis pipeline.

The AI workflow evaluates:

* contextual behavioral framing,
* escalation patterns,
* intimidation progression,
* grooming indicators,
* coercive interaction structures,
* and cross-modal consistency between uploaded evidence and written narratives.

The synthesis engine can also assist analysts in identifying probable communication environments or digital platforms associated with the abuse context by analyzing recurring interface structures, conversational framing, and contextual interaction signals contained within uploaded evidence.

Rather than producing autonomous conclusions, the system generates explainable contextual synthesis outputs designed to help investigators transform fragmented reports into structured investigative intelligence.

The resulting synthesis is returned to the NGO dashboard as an Explainable AI investigative report containing:

* contextual risk observations,
* behavioral escalation indicators,
* narrative synthesis summaries,
* and transparent reasoning outputs for human review.

---

# Technology Stack

## Mobile Application

* React Native Expo

## NGO Dashboard

* React

## Backend

* Flask
* Python

## AI / NLP

* TensorFlow
* Keras
* Bi-LSTM
* Gemini API

## Database

* MongoDB

## Hosting

* Railway

---

# Repository Structure

```bash
SentinelX
│
├── Guide.pdf
│
├── Pitch_Deck/
│   ├── SentinelX_Pitch_Deck.pdf
│   └── SentinelX_Architecture_Diagram.png
│
├── Demo/
│   ├── SentinelX_Demo_Video.mp4
│   ├── Demo_Script.pdf
│   └── Demo_Screenshots/
│       ├── mobile_safechat.png
│       ├── analyst_dashboard.png
│       ├── analyze_report_flow.png
│       ├── xai_panel.png
│       └── threat_alert_queue.png
│
├── Documentation/
│   ├── About_The_Project.pdf
│   ├── AI_Architecture_Explanation.pdf
│   ├── Responsible_AI_Guardrails.pdf
│   ├── Human_in_the_Loop_Design.pdf
│   ├── Technical_Stack.pdf
│   └── Data_Sources.pdf
│
├── Prototype/
│   ├── Android_APK/
│   │   └── SentinelX.apk
│   │
│   ├── Dashboard_Screens/
│   │   ├── dashboard_home.png
│   │   ├── pending_analysis.png
│   │   ├── xai_report_panel.png
│   │   └── triaged_case.png
│   │
│   └── Mobile_App_Screens/
│       ├── safechat_step1.png
│       ├── safechat_step2.png
│       ├── safechat_step3.png
│       ├── safechat_step4.png
│       ├── sos_screen.png
│       └── detect_threat.png
│
├── Source_Summary/
│   ├── Folder_Structure.png
│   ├── Key_Code_Explanation.pdf
│   └── API_Workflow_Explanation.pdf
│
└── Team/
    ├── Team_Photo.jpg
    ├── Team_Members.pdf
    └── Team_Roles.pdf
```

---

# Important Files for Reviewers

## Start Here

Reviewers should begin with:

```bash
Guide.pdf
```

This document contains:

* complete prototype navigation instructions,
* reviewer walkthrough,
* dashboard testing steps,
* and AI workflow explanation.

---

# Pitch Materials

Located in:

```bash
Pitch_Deck/
```

Contains:

* final presentation deck,
* architecture diagram,
* and system workflow visuals.

---

# Demo Files

Located in:

```bash
Demo/
```

Contains:

* demo video: https://youtu.be/ZGMigidNDqo
* demo narration script,
* and supporting screenshots.

---

# Documentation Files

Located in:

```bash
Documentation/
```

Contains:

* About the Project,
* AI Architecture Explanation,
* Responsible AI Guardrails,
* Human-in-the-Loop Design,
* Technical Stack,
* and Data Sources.

---

# Prototype Files

Located in:

```bash
Prototype/
```

Contains:

* Android APK,
* mobile UI screenshots,
* and dashboard screenshots.

---

# Source Summary

Located in:

```bash
Source_Summary/
```

Contains:

* codebase overview,
* API workflow explanations,
* and architecture breakdowns.

---

# Team Information

Located in:

```bash
Team/
```

Contains:

* team photograph,
* team member information,
* and project role breakdowns.

---

# Installation Instructions

Navigate to 
```bash
https://drive.google.com/file/d/10m8aaiExI5jMwt9q6okJctM0zSe1Ljz7/view?usp=sharing
```
Here you can download the SentinelX app for your Android device
Install the App
# NGO DASHBOARD

Navigate to the dashboard via this link:

```bash
https://besafe-server-production.up.railway.app
```
---

# Usage Examples

# Example 1 — SOS Flow

## Purpose

Immediate emergency escalation.

## How to Use

1. Open mobile app
2. Press and hold SOS button for 3 seconds
3. Alert routes instantly to:

   * NGO Dashboard
   * emergency contacts

---

# Example 2 — Detect Threat

## Purpose

On-device spoken threat classification.

## How to Use

1. Toggle:

```bash
Detect Threat = ON
```

2. The app:

* transcribes speech locally,
* classifies contextual threats,
* discards audio immediately.

3. Threat signals appear on NGO dashboard.

---

# Example 3 — Safe Chat

## Purpose

Structured contextual reporting.

## How to Use

Users complete:

1. Category Selection
2. Narrative Description
3. Timing Tag
4. Frequency Tag

Optional:

* image upload,
* video upload,
* audio upload.

Submitted reports appear as:

```bash
Pending Analysis
```

until reviewed by an analyst.

---

# Prototype Navigation Guide

This section provides a step-by-step walkthrough for reviewers testing the SentinelX prototype.

---

# Mobile App SIGN UP

## Step 1

Download the APK located in:

```bash
 https://drive.google.com/file/d/10m8aaiExI5jMwt9q6okJctM0zSe1Ljz7/view?usp=sharing
```

Install on Android device.

---

## Step 2

Open the mobile application.

---

## Step 3

Allow SentinelX notification permissions (optional).

---

## Step 4

Click:

> Continue with Phone Number

---

## Step 5

Enter phone number and click:

> Send Code

---

## Step 6

For this MVP prototype, use hardcoded OTP:

```bash
2026
```

---

## Step 7

Allow location access.

---

## Step 8

Fill in:

* First Name
* Last Name
* Email

---

## Step 9

Add at least one emergency contact.

---

## Important Note

If the app gets stuck during onboarding:

* restart the app,
* and complete setup more quickly.

---

# NGO Dashboard Login

Dashboard URL:

```bash
https://besafe-server-production.up.railway.app
```

Login or sign up using NGO analyst credentials.

---

# Important Dashboard Note

Ensure your current location is enabled.

---

# After Login Reviewers Will See

* Overview Page
* Alert Queue
* Safe Chat Reports
* AI Analysis Controls

---

# Mobile App Walkthrough

The mobile application contains three major flows:

1. SOS
2. Detect Threat
3. Safe Chat + Evidence Upload

---

# A. SOS Flow (No AI)

## Purpose

Immediate emergency escalation without AI involvement.

## Steps

### Step 1

Press and hold the SOS button for approximately 3 seconds.

### Step 2

The system sends:

* emergency alerts,
* dashboard notifications,
* contextual emergency information.

### Step 3

Open the NGO dashboard and observe:

* incoming SOS alert,
* timestamp,
* priority indicator,
* and user information.

---

# Important Design Note

The SOS flow intentionally uses:

> NO AI

This preserves direct human-controlled escalation.

---

# B. Detect Threat Flow (On-Device AI)

## Purpose

Contextual spoken threat classification using NLP.

---

## Steps

### Step 1

Return to Home Screen.

### Step 2

Toggle:

> Detect Threat

to ON.

### Step 3

The app begins:

* local audio capture,
* local transcription,
* on-device Bi-LSTM classification.

### Step 4

If a threat is detected:

* a threat signal is routed to dashboard.

### Step 5

Open dashboard and observe:

* threat alert entry,
* transcript snippet,
* classification result.

---

# Important Privacy Design

Audio is:

* never stored,
* never uploaded,
* and discarded immediately after transcription.

Only the classification result leaves the device.

---

# C. Safe Chat + Evidence Flow

## Purpose

Structured contextual abuse reporting.

---

## Steps

### Step 1

Open:

> Safe Chat

from Home Screen.

### Step 2 — Category Selection

Select:

* stalking,
* cyber-harassment,
* coercion,
* exploitation,
* physical tracking.

### Step 3 — Narrative Description

Enter contextual description.

### Step 4 — Timing

Select:

* today,
* this week,
* months ago.

### Step 5 — Frequency

Select:

* first time,
* a few times,
* repeated escalation.

### Step 6 — Evidence Upload

Optional uploads:

* image,
* video,
* audio.

### Step 7 — Submit Report

Report appears on dashboard as:

```bash
Pending Analysis
```

---

# NGO Dashboard Walkthrough

The dashboard serves as the primary analyst workspace.

It contains:

* real-time alerts,
* Safe Chat reports,
* Explainable AI panels,
* AI analysis controls,
* and analyst workflows.

---

# A. Viewing Incoming Alerts

Navigate to:

> Alerts

Analysts can review:

* SOS alerts,
* Detect Threat signals,
* timestamps,
* contextual information,
* priority indicators.

Clicking an alert opens:

> Detail Panel

which displays:

* transcript snippets,
* timestamps,
* contextual details,
* analyst controls.

---

# B. Reviewing Safe Chat Reports

Navigate to:

> Reports

Reports initially appear as:

```bash
Pending Analysis
```

At this stage:

* no AI analysis has occurred,
* no synthesis has been generated.

This is intentional.

---

# C. Human-Triggered AI Analysis

## Important Responsible AI Workflow

AI analysis only begins after explicit analyst authorization.

---

## Steps

### Step 1

Open Safe Chat report.

### Step 2

Click:

```bash
[Analyze Report]
```

### Step 3

The backend:

* retrieves report,
* processes metadata,
* sends contextual payload,
* receives explainable synthesis.

### Step 4

Status updates from:

```bash
Pending Analysis
```

to:

```bash
Triaged
```

### Step 5

Explainable AI panel becomes visible.

The panel displays:

* contextual synthesis,
* escalation observations,
* explainable reasoning,
* risk indicators.

---

# D. Human-in-the-Loop Workflow

SentinelX intentionally prevents autonomous intervention.

Reviewers should note:

* AI never contacts authorities,
* AI never escalates automatically,
* AI never performs enforcement actions.

Human analysts remain responsible for:

* interpreting outputs,
* validating contextual findings,
* making intervention decisions.

---

# Recommended Reviewer Flow

For best demonstration experience:

1. Mobile App Home Screen
2. SOS Flow
3. Detect Threat Flow
4. Safe Chat Submission
5. NGO Dashboard Alert Queue
6. Safe Chat Report Queue
7. Analyze Report Trigger
8. Explainable AI Panel
9. Analyst Action Controls

This demonstrates:

* multi-signal ingestion,
* contextual NLP,
* Explainable AI,
* human-supervised AI governance.

---

# Responsible AI Design

SentinelX was intentionally designed to reduce:

* automation bias,
* privacy violations,
* over-reliance on AI,
* autonomous escalation risks.

---

# Core Safeguards

* Human-triggered AI only
* No autonomous intervention
* Explainable AI synthesis
* On-device transcription
* Audio deletion after transcription
* Transparent analyst review workflow

---

# Contributing Guidelines

We welcome contributions from:

* developers,
* researchers,
* NGOs,
* responsible AI practitioners,
* and safety-focused organizations.

---

# Contribution Areas

* NLP improvements
* UI/UX enhancements
* Dashboard improvements
* Security hardening
* Explainable AI tooling
* Accessibility support

---

# AI Tools Used

## AI Models

* Bi-LSTM
* Gemini API

## Frameworks

* TensorFlow
* Keras

## AI-Assisted Development

* ChatGPT
* GitHub Copilot
* Claude
* Gemini
* Lovable

---

# Dataset Information

The NLP model was trained using:

* public NLP datasets,
* contextual threat examples,
* synthetic escalation narratives.

Dataset size:

```bash
100,000+ labeled entries
```

Dataset split:

```bash
70% Training
20% Validation
10% Testing
```

---

# Team

## Fredrick

Team Lead / System Design / AI Research

## Tomna

Machine Learning Lead

## Solomon

Mobile Application Developer

## Habeeb

UI/UX Designer

## Adebayo

Asst. AI/ML lead

---

# Important Research Note

SentinelX is currently an MVP / pilot-stage prototype created during the USAII Hackathon.

The system is intended for:

* research,
* prototyping,
* organizational testing,
* and responsible AI experimentation.

It should not replace:

* law enforcement,
* emergency response systems,
* or professional crisis intervention services.

---

# LINKS:

SENTINEL_APK_LINK_TO_DOWNLOAD: https://drive.google.com/file/d/10m8aaiExI5jMwt9q6okJctM0zSe1Ljz7/view?usp=sharing

---

VIDEO_DEMO: https://youtu.be/ZGMigidNDqo

---

# License

This repository is currently released for:

* educational,
* research,
* and hackathon demonstration purposes only.
