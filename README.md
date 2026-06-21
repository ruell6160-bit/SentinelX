# SentinelX

## AI-Assisted Organizational Threat Triage Platform

SentinelX is a responsible AI-assisted threat triage platform designed for NGOs, intervention organizations, investigators, and institutional safety teams supporting vulnerable individuals facing:

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

# System Architecture

The platform consists of three distinct flows:

| Flow                 | AI Used     | Purpose                                 |
| -------------------- | ----------- | --------------------------------------- |
| SOS                  | No AI       | Immediate emergency escalation          |
| Detect Threat        | Bi-LSTM NLP | Contextual spoken threat classification |
| Safe Chat + Evidence | Gemini API  | Structured contextual evidence analysis |

---

# Technology Stack

## Mobile App

* React Native Expo

## Frontend Dashboard

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

# Installation Instructions

## Prerequisites

Ensure the following are installed:

* Node.js
* Python 3.10+
* MongoDB
* Expo CLI

---

# 1. Clone Repository

```bash
git clone https://github.com/your-username/SentinelX.git

cd SentinelX
```

---

# 2. Backend Setup

Navigate to backend folder:

```bash
cd backend
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Run Flask server:

```bash
python app.py
```

---

# 3. Mobile App Setup

Navigate to mobile app folder:

```bash
cd mobile-app
```

Install dependencies:

```bash
npm install
```

Start Expo development server:

```bash
npx expo start
```

---

# 4. Dashboard Setup

Navigate to dashboard folder:

```bash
cd dashboard
```

Install dependencies:

```bash
npm install
```

Start dashboard:

```bash
npm run dev
```

---

# Usage Examples

# Example 1 — SOS Flow

### Trigger Emergency Alert

1. Open mobile app
2. Press and hold SOS button for 3 seconds
3. Alert is routed to:

   * NGO Dashboard
   * Emergency Contacts

---

# Example 2 — Detect Threat

### Activate Threat Detection

1. Toggle:

```bash
Detect Threat = ON
```

2. The app:

* captures audio locally,
* transcribes speech,
* classifies text using Bi-LSTM,
* discards audio immediately.

3. If threat detected:

* alert appears on dashboard.

---

# Example 3 — Safe Chat Submission

### Submit Structured Report

Users complete:

1. Category Selection
2. Narrative Description
3. Timing Tag
4. Frequency Tag

Optional:

* image upload,
* audio upload,
* video upload.

Reports arrive on dashboard as:

```bash
Pending Analysis
```

---

# Prototype Navigation Guide

This section provides a step-by-step walkthrough for reviewers testing the SentinelX prototype.

---

# Mobile App Sign Up

## Step 1

Download the APK located in:

```bash
prototype/Android_APK/
```

Install on Android device.

---

## Step 2

Open SentinelX.

---

## Step 3

Allow notification permissions (optional).

---

## Step 4

Click:

```bash
Continue with Phone Number
```

---

## Step 5

Enter phone number.

---

## Step 6

Use hardcoded OTP:

```bash
2026
```

---

## Step 7

Allow location access.

---

## Step 8

Complete setup:

* First Name
* Last Name
* Email
* Emergency Contact

---

# NGO Dashboard Login

Dashboard URL:

```bash
https://besafe-server-production.up.railway.app
```

Use any NGO analyst credentials.

---

# Dashboard Features

After login reviewers will see:

* Overview Page
* Alert Queue
* Reports Queue
* AI Analysis Controls
* Explainable AI Panels

---

# Mobile App Walkthrough

The mobile app contains three flows:

1. SOS
2. Detect Threat
3. Safe Chat + Evidence Upload

---

# A. SOS Flow

## Purpose

Immediate emergency escalation.

## Steps

1. Hold SOS button for 3 seconds
2. Alert routed instantly
3. Observe dashboard alert

---

# B. Detect Threat Flow

## Purpose

On-device contextual threat classification.

## Steps

1. Toggle Detect Threat ON
2. Local transcription begins
3. Bi-LSTM classifies text
4. Threat signals appear on dashboard

---

# C. Safe Chat Flow

## Purpose

Structured contextual abuse reporting.

## Steps

1. Open Safe Chat
2. Select category
3. Enter narrative
4. Select timing
5. Select frequency
6. Upload evidence
7. Submit report

---

# NGO Dashboard Walkthrough

---

# A. View Alerts

Navigate to:

```bash
Alerts
```

Analysts can review:

* SOS alerts
* Detect Threat alerts
* timestamps
* contextual information

---

# B. Review Safe Chat Reports

Navigate to:

```bash
Reports
```

Reports initially appear as:

```bash
Pending Analysis
```

No AI processing occurs automatically.

---

# C. Human-Triggered AI Analysis

## Important Workflow

AI analysis only begins after explicit analyst authorization.

### Steps

1. Open report
2. Click:

```bash
[Analyze Report]
```

3. Flask backend:

* retrieves report,
* sends contextual payload,
* receives explainable synthesis output.

4. Report status updates to:

```bash
Triaged
```

5. Explainable AI panel appears.

---

# Responsible AI Design

SentinelX was intentionally designed to reduce:

* automation bias,
* privacy violations,
* over-reliance on AI,
* and autonomous escalation risks.

## Key Safeguards

* Human-triggered AI only
* No autonomous intervention
* Explainable AI synthesis
* On-device transcription
* Audio deletion after transcription
* Transparent analyst review workflows

---

# Contributing Guidelines

We welcome contributions from developers, researchers, and safety-focused organizations.

## Contribution Areas

* NLP improvements
* Dashboard enhancements
* UI/UX improvements
* Security hardening
* Responsible AI tooling
* Accessibility improvements

---

# How to Contribute

## Step 1

Fork the repository.

---

## Step 2

Create feature branch:

```bash
git checkout -b feature-name
```

---

## Step 3

Commit changes:

```bash
git commit -m "Added new feature"
```

---

## Step 4

Push branch:

```bash
git push origin feature-name
```

---

## Step 5

Open Pull Request.

---

# Important Research Notes

SentinelX is currently an MVP / pilot-stage prototype created during the USAII Hackathon.

The platform is intended for:

* research,
* prototyping,
* organizational testing,
* and responsible AI experimentation.

The system should not be treated as a replacement for:

* law enforcement,
* emergency response teams,
* or professional crisis intervention services.

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
* Gemini
* Claude
* Lovable

---

# Dataset Information

The NLP model was trained on:

* public NLP datasets,
* contextual threat statements,
* and synthetic escalation narratives.

Dataset size:

```bash
100,000+ labeled entries
```

Split:

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

Machine Learning Engineer

## Solomon

Mobile Application Developer

## Habeeb

UI/UX Designer

---

# License

This project is currently released for:

* educational,
* hackathon,
* and research purposes only.
