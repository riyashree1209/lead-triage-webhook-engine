# ⚡ Inbound Lead Triage & Real-Time Alert Engine

An event-driven automation engine built with Python to parse raw inbound web inquiries, calculate urgency and budget priority, synchronize records to a persistent CRM ledger, and trigger real-time webhook notifications to team channels (Discord / Microsoft Teams).

---

## 📌 Business Problem & Impact

In high-growth sales teams, inbound contact inquiries often sit unread in generic email inboxes for 4–8 hours before manual review. Studies show that contacting a qualified lead within 5 minutes increases pipeline conversion rates by nearly 400% compared to a delayed response.

### Key Outcomes:
- **Triage Latency:** Reduced from hours to **< 60 seconds**.
- **Operational Efficiency:** Eliminates repetitive manual data entry into CRM sheets.
- **Speed to Lead:** Ensures high-intent, high-budget opportunities receive immediate sales rep engagement.

---

## 🛠 Technical Workflow
1. **Extraction & Context Parsing:** Reads raw message inputs and evaluates indicators like project budget, delivery urgency, and request type.
2. **Dynamic Priority Scoring:** Categorizes inbound submissions into tiered priority levels (`HIGH`, `MEDIUM`, `LOW`).
3. **Audit Ledger Sync:** Automatically records structured details, submission timestamps, and draft responses to a persistent CSV database.
4. **Instant Webhook Notification:** Pushes rich visual alert cards directly to an operations channel whenever a `HIGH` priority prospect reaches out.

---

## 📸 Proof of Execution

### 1. Real-Time Channel Alert (Webhook Integration)
Rich embed cards sent to the team channel with immediate context for high-priority leads:

<img width="1591" height="770" alt="image" src="https://github.com/user-attachments/assets/b95470e8-a7a2-4c8b-a52d-185b84a06eb3" />


### 2. Execution Log & Pipeline Processing
Pipeline execution evaluating incoming leads and scoring priority in real time:

<img width="736" height="127" alt="image" src="https://github.com/user-attachments/assets/1968e86a-f573-44ce-870e-a583d0da1fc8" />


### 3. Synchronized CRM Ledger (`crm_leads.csv`)
Clean tabular output ready for ingestion by downstream reporting tools or CRMs:



---

## 💻 Tech Stack

- **Language:** Python 3.10+
- **HTTP Client:** `requests` (for Webhook payload delivery)
- **Data Persistence:** Python Standard Library (`csv`, `datetime`, `os`)
- **Integration Targets:** Discord Webhooks / Microsoft Teams Connectors

---

## 🚀 Getting Started

### 1. Clone the Repository
```bash
git clone [https://github.com/](https://github.com/)<your-username>/lead-triage-webhook-engine.git
cd lead-triage-webhook-engine
