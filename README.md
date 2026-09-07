Automatix — AI Lead Acquisition & Follow-Up System
An end-to-end, niche-agnostic AI automation system built in n8n that finds potential clients, researches and scores them with AI, generates personalized outreach, routes everything through human approval, follows up automatically, and tracks results — with zero manual lead-hunting.
Built as a real, working system (not a demo) — every workflow below has been tested end-to-end.
🚀 What It Does
1. Lead Discovery
Searches for target companies via search engines
AI researches each company and judges relevance + pain points against a configurable Ideal Customer Profile
Filters out irrelevant leads automatically
AI scores every relevant lead 0–100 with a reason
AI writes a personalized outreach message (subject + body) based on the company's specific situation
Sends the lead + message to Telegram/Whatsapp for human approval (Approve/Decline buttons) before anything goes out
On approval, sends the email automatically via SMTP
Saves every lead to a lightweight JSON-based CRM (score, status, message, date)
2. Follow-Up Automation
Automatically finds leads that went pending 3+ days ago
AI writes a polite, context-aware follow-up referencing the original message
Routes through the same Telegram approval step
Sends the follow-up and updates the lead's status in the CRM
3. Reply Monitoring
Monitors the inbox (IMAP) for real replies (filters out LinkedIn/Upwork notification noise)
AI classifies each reply: interested, not_interested, price_inquiry, unsubscribe, out_of_office, other
Interested replies trigger an instant 🔥 Hot Lead Telegram alert
Unsubscribe requests are automatically added to a Do-Not-Contact list — no manual tracking needed
4. Weekly Reporting
Automatically compiles total leads, pending count, followed-up count, average score, and top 5 leads
Sends a formatted summary report to Telegram every week
5. Safety & Reliability Layer
Daily rate limiting — caps outreach volume per day
Duplicate-contact checks — never emails the same company twice
Contact Eligibility Gate — blocks sending to anyone on the Do-Not-Contact list
Kill Switch — a single flag can halt the entire system instantly
Failure tracking — auto-disables outreach if 3+ sends fail within 24 hours (deliverability protection)
🧩 Why It's Different: Niche-Agnostic Design
The entire system runs off one configurable "Business Settings" workflow — business name, service, target industry, ideal customer profile, pain points, and offer. Change these settings and the exact same engine can be redeployed for a completely different business or industry, with no rebuilding required.
🛠️ Tech Stack
Component
Tool
Automation engine
n8n (self-hosted)
AI / LLM
Google Gemini API
Lead search
Serper.dev (Google Search API)
Approval & alerts
Telegram Bot API
Email (outbound)
Gmail SMTP
Email (inbound)
IMAP
Data storage
JSON-based lightweight CRM
Tunneling (dev)
ngrok
📂 Workflows in This Repo
00-business-settings.json — Central configuration (ICP, offer, tone, target industry)
01-lead-discovery.json — Search → AI Research → Filter → AI Score → AI Message → Approval → Email → Save to CRM
02-follow-up-checker.json — Finds stale leads → AI follow-up → Approval → Email → Status update
03-weekly-report.json — Reads CRM data → Compiles stats → Sends Telegram report
04-reply-monitoring.json — IMAP inbox check → AI classification → Hot lead alerts / DNC list update
(Note: credentials and API keys are not included in these exports — connect your own Gemini, Serper, Telegram, and Gmail credentials in n8n.)
📸 Screenshots
(Add screenshots of each workflow canvas here — see /screenshots folder)
💬 About This Project
This system was built to solve a real problem: manual lead-hunting and follow-up is slow and inconsistent. Automatix automates the entire pipeline — from finding a company to closing the loop on a reply — while keeping a human in control of every outbound message via the approval step.
Available for freelance / contract work building similar AI automation systems (n8n, AI agents, workflow automation, CRM integration).
📩 Open to discussing your specific use case.
