<div align="center">

# 📄 Proposal Automation

**Sales call → professional proposal → signed contract. In minutes, not 2–3 hours.**

[![Make](https://img.shields.io/badge/Make.com-Core-6D00CC?style=for-the-badge)](https://make.com)
[![OpenAI](https://img.shields.io/badge/OpenAI-GPT--4o-412991?style=for-the-badge&logo=openai&logoColor=white)](https://openai.com)
[![DocuSign](https://img.shields.io/badge/DocuSign-eSign-FFB600?style=for-the-badge)](https://docusign.com)
[![Google Docs](https://img.shields.io/badge/Google_Docs-Output-4285F4?style=for-the-badge&logo=googledocs&logoColor=white)](https://docs.google.com)

</div>

---

## The Problem

The gap between a great sales call and a sent proposal is where deals die.

The traditional flow:
1. Call ends (prospect is excited)
2. You go write the proposal manually — takes 2–3 hours
3. You send it the next day or two later
4. By then, the prospect has cooled down, talked to competitors, or simply moved on

Speed is part of the close. This system sends a polished proposal within minutes of the call ending — while the prospect's enthusiasm is at its peak.

---

## Full Flow

```
Sales Call Ends (Zoom / Google Meet / Phone)
         │
         ▼
┌────────────────────────────┐
│  Auto-Transcription        │  ← Fireflies.ai or Otter.ai
│                            │    Transcribes and timestamps the full call
└─────────────┬──────────────┘
              │
              ▼
┌────────────────────────────┐
│  AI Extraction             │  ← GPT-4o reads the transcript and extracts:
│  (GPT-4o)                  │    • Client name + company
│                            │    • Pain points discussed
│                            │    • Scope of work agreed on
│                            │    • Pricing discussed
│                            │    • Timeline mentioned
│                            │    • Objections raised + how addressed
└─────────────┬──────────────┘
              │
              ▼
┌────────────────────────────┐
│  Proposal Generation       │  ← Fills branded Google Docs template
│  (Google Docs API)         │    with extracted data + AI-written sections:
│                            │    • Executive summary
│                            │    • Scope of work
│                            │    • Investment breakdown
│                            │    • Timeline
│                            │    • Terms & next steps
└─────────────┬──────────────┘
              │
              ▼
┌────────────────────────────┐
│  Contract Attachment       │  ← Appends or generates a service agreement
│  (DocuSign)                │    pre-filled with client details + pricing
└─────────────┬──────────────┘
              │
              ▼
┌────────────────────────────┐
│  Send via Gmail            │  ← Personalized email with PDF proposal
│                            │    + DocuSign link attached
│                            │    Sent within minutes of call end
└─────────────┬──────────────┘
              │
              ▼
┌────────────────────────────┐
│  CRM Update                │  ← Deal stage → "Proposal Sent"
│  (Airtable / HubSpot)      │    Proposal stored, follow-up triggered
└────────────────────────────┘
```

---

## What the AI Extracts

Given a 45-minute transcript, GPT-4o produces:

```json
{
  "client_name": "Sarah Chen",
  "company": "Meridian Marketing",
  "problem": "Spending 15 hours/week manually pulling reports from 4 platforms into one spreadsheet. Team makes decisions on stale data.",
  "desired_outcome": "Automated daily dashboard with real-time data from all platforms by EOD",
  "scope": [
    "Audit current data sources (Google Analytics, Meta Ads, HubSpot, Shopify)",
    "Build automated ETL pipeline",
    "Design Looker Studio dashboard with 12 key metrics",
    "Set up daily email digest to leadership team"
  ],
  "investment": "$3,200 one-time setup + $350/month maintenance",
  "timeline": "2 weeks to delivery",
  "objections_addressed": ["Budget concern — offered payment plan", "Asked about ongoing support — included in monthly retainer"],
  "next_steps": "Sarah to forward to her business partner for final sign-off"
}
```

---

## Proposal Template Structure

```
┌─────────────────────────────────┐
│  [Company Logo]                 │
│  Prepared for: Sarah Chen       │
│  Meridian Marketing             │
│  Date: May 7, 2026              │
├─────────────────────────────────┤
│  EXECUTIVE SUMMARY              │  ← AI-written, references their exact words
├─────────────────────────────────┤
│  THE PROBLEM WE'RE SOLVING      │  ← Pain points from the call
├─────────────────────────────────┤
│  SCOPE OF WORK                  │  ← Extracted deliverables
├─────────────────────────────────┤
│  INVESTMENT                     │  ← Pricing discussed on the call
├─────────────────────────────────┤
│  TIMELINE                       │  ← Milestones + delivery date
├─────────────────────────────────┤
│  WHY US                         │  ← Static section (your credentials)
├─────────────────────────────────┤
│  NEXT STEPS                     │  ← Sign by [date] → kickoff scheduled
└─────────────────────────────────┘
```

---

## Follow-Up Sequence (Post-Send)

```
+0 min:   Proposal sent with warm personal email
+24 hrs:  "Just checking it landed okay" follow-up
+72 hrs:  Value-add follow-up (case study relevant to their industry)
+7 days:  Last touch — "still happy to answer any questions"
```

If DocuSign shows the proposal was opened but not signed, the system triggers a Slack alert so you can follow up at the right moment.

---

## Setup

### Required Accounts
- Make.com (Core or above)
- OpenAI API (GPT-4o)
- Fireflies.ai or Otter.ai (transcription)
- Google Workspace (Docs + Gmail)
- DocuSign
- Airtable or HubSpot (CRM)

### Config Variables
```yaml
proposal_template_id: "your-google-doc-template-id"
contract_template_id: "your-docusign-template-id"
from_name: "Rohan Mukherjee"
from_email: "texanrohan@gmail.com"
crm_base_id: "your-airtable-base"
```

---

## Results

```
Before: 2–3 hours per proposal, sent next day, cold prospects
After:  8–12 minutes end-to-end, sent same day, leads still warm

Time saved per proposal:   ~2.5 hours
Close rate improvement:    Significantly higher (prospect is still excited)
Proposal consistency:      100% — same quality every time, no off days
```

---

<div align="center">

**Built by [Rohan Mukherjee](https://github.com/rohan643)**

</div>
