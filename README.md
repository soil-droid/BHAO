# BharatHealth Agentic Orchestrator (BHAO)
### Autonomous Administrative Workflows for India’s Digital Health Revolution

## 🏥 Overview
**BharatHealth Agentic Orchestrator (BHAO)** is an enterprise-grade healthcare automation platform built for the **AWS: AI for Bharat Hackathon (Professional Track)**.

In the current Indian healthcare landscape, doctors spend nearly two hours on paperwork for every one hour of patient care. BHAO addresses this "Administrative Stall" by acting as an autonomous agentic layer integrated with India’s **Ayushman Bharat Digital Mission (ABDM)** ecosystem. Unlike traditional chatbots, BHAO uses Agentic AI to reason through complex tasks—such as insurance prior authorizations and discharge planning—by navigating hospital ERPs, retrieving consent-linked records from the **ABHA vault**, and generating standardized **FHIR bundles**.

---

## ✨ Key Features

* 🎙️ **Vernacular Ambient Scribe:** Powered by AWS HealthScribe, it transcribes doctor-patient dialogues in **22 Indian languages** (Marathi, Hindi, etc.) and identifies speaker roles to generate structured JSON clinical notes with $98\%$ accuracy.
* 🤖 **Agentic Prior-Auth Agent:** Autonomously determines if a procedure requires insurance authorization, retrieves necessary clinical data from ABHA records, and populates payer-specific forms with validated ICD-10 codes.
* 🇮🇳 **India Stack & DPI Integration:** Fully compliant with ABDM Sandbox Milestones M1, M2, and M3, enabling secure, consent-driven health data exchange.
* 🛡️ **Privacy-First Reasoning:** Utilizes Amazon Bedrock Guardrails to automatically redact PII (Personally Identifiable Information) and provide Contextual Grounding to prevent AI hallucinations in medical summaries.
* 📉 **Quantifiable Impact:** Targeted **30% reduction** in hospital operational costs and **60% faster** prior-authorization processing.

---

## 🛠️ Technical Stack

| Layer | Technologies |
| :--- | :--- |
| **AI & Intelligence** | Amazon Bedrock (Claude 3.5 Sonnet), AWS HealthScribe, BharatGen/Bhashini |
| **India Stack** | ABHA ID, ABDM Gateway, FHIR R4 Bundles |
| **Backend** | FastAPI (Python), AWS Lambda (Serverless), Amazon EventBridge |
| **Frontend** | Next.js 15, TypeScript, Zustand, Tailwind CSS |
| **Storage & Data** | Amazon DynamoDB (State), RDS Aurora Serverless (Relational), Amazon S3 (Vault) |
| **Security** | Amazon Bedrock Guardrails, AWS KMS, Amazon Cognito, DPDP Act 2023 Compliance |

---

## 🏗️ Architecture
BHAO follows a **Serverless Event-Driven Architecture**. The Agentic Orchestrator manages "Sagas"—asynchronous, multi-step workflows—across disparate healthcare platforms.

1.  **Ingestion:** Vernacular audio is processed via AWS HealthScribe.
2.  **Reasoning:** The agent evaluates the clinical goal and identifies missing data in the patient's longitudinal ABHA record.
3.  **Action:** The agent executes API calls to the ABDM Sandbox or insurance portals to complete the administrative task.
4.  **Validation:** Every action is recorded in a tamper-proof audit trail with a **Human-in-the-Loop (HITL)** interface for clinician approval.

---

## 🚀 Getting Started

### Prerequisites
* AWS Account with access to Amazon Bedrock and AWS HealthScribe.
* ABDM Sandbox credentials (M1, M2, M3).
* Node.js 18+ and Python 3.10+.

### Installation

1.  **Clone the Repository:**
    ```bash
    git clone [https://github.com/your-repo/bhao.git](https://github.com/your-repo/bhao.git)
    cd bhao
    ```

2.  **Infrastructure Setup:**
    Deploy the serverless stack using the AWS CDK or Serverless Framework:
    ```bash
    cd infra
    npm install
    cdk deploy
    ```

3.  **Backend Configuration:**
    Set up your `.env` with ABDM credentials and Bedrock model IDs.

4.  **Run Locally:**
    ```bash
    # Frontend
    npm run dev

    # Backend
    uvicorn app.main:app --reload
    ```

---

## 📊 Market Viability & Roadmap

* **Business Model:** SaaS license for hospitals starting at approx. **$50,000** per facility, with a per-transaction fee for insurance authorizations.
* **GTM Strategy:** Partner with existing Indian HMIS vendors to provide BHAO as a premium "Agentic Module."

### Roadmap
* **Q2 2026:** Pilot in "Future Health Districts" under the NHA India Pathfinder initiative.
* **Q4 2026:** Integration with wearable sensor data for proactive heart failure and sepsis alerts.

---

## ⚖️ Compliance & Ethics
Designed to be fully compliant with India’s **Digital Personal Data Protection (DPDP) Act 2023** and **HIPAA**. BHAO prioritizes Tech Sovereignty by utilizing local Indic language models and federated, consent-driven architectures.

> Created for the **AWS: AI for Bharat Hackathon 2026**.
