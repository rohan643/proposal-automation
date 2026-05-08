<div align="center">

# 📄 Proposal Automation

### From sales call to signed proposal — in minutes, not hours.

<br>

| Before | After |
|--------|-------|
| 2–3 hours writing | 8 minutes automated |
| Sent next day | Sent same day |
| Cold prospect | Prospect still excited |
| Inconsistent quality | Same quality every time |

<br>

![n8n](https://img.shields.io/badge/n8n-Core_Workflow-EA4B71?style=for-the-badge&logo=n8n&logoColor=white)
![OpenAI](https://img.shields.io/badge/OpenAI-GPT--4o-412991?style=for-the-badge&logo=openai&logoColor=white)
![Google Docs](https://img.shields.io/badge/Google_Docs-Template-4285F4?style=for-the-badge&logo=googledocs&logoColor=white)
![DocuSign](https://img.shields.io/badge/DocuSign-eSign-FFB600?style=for-the-badge)

</div>

---

## The Workflow

```
① Call ends (Zoom / Google Meet)
        ↓
② Fireflies transcribes automatically
        ↓
③ GPT-4o extracts: client, scope, pricing, timeline, objections
        ↓
④ Google Doc proposal generated from branded template
        ↓
⑤ DocuSign contract attached and pre-filled
        ↓
⑥ Sent via Gmail while prospect is still warm
        ↓
⑦ CRM updated: stage → "Proposal Sent", follow-up triggered
```

---

## What GPT-4o Extracts

```json
{
  "client_name": "Sarah Chen",
  "company": "Meridian Marketing",
  "problem": "15 hrs/week pulling reports manually from 4 platforms",
  "scope": ["ETL pipeline", "Looker Studio dashboard", "daily digest"],
  "investment": "$3,200 setup + $350/mo",
  "timeline": "2 weeks",
  "objections_addressed": ["budget — offered payment plan"],
  "next_steps": "Sarah to confirm with business partner"
}
```

---

## Files

| File | Purpose |
|------|---------|
| `workflow/proposal-generator.json` | n8n workflow — full automation |
| `config/config.yaml` | Template IDs, email settings |
| `templates/proposal.md` | Proposal structure template |
| `templates/email-cover.md` | Cover email sent with proposal |

---

## Setup

1. Import `workflow/proposal-generator.json` into n8n
2. Set template IDs in `config/config.yaml`
3. Connect: Fireflies → n8n → Google Docs → DocuSign → Gmail
4. Activate — trigger fires when Fireflies webhook posts a transcript

**Required credentials:** OpenAI, Google OAuth, DocuSign, Gmail, Airtable/HubSpot

---

<div align="center">
<sub>Built by <a href="https://github.com/rohan643">@rohan643</a></sub>
</div>
