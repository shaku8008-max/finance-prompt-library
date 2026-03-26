# Prompt Library — Banking Compliance & Operations

Assessment 1 | Generative AI for Business  
Student: [Your Name]  
Business Field: Finance — Banking (Australia)  
Model tested on: GPT-5.3  
Last updated: [Date]

---

## What This Library Does

This prompt library automates key workflows in **banking regulatory and operational documentation**.

It focuses on improving:
- Compliance documentation processing  
- Risk identification and prioritisation  
- Customer service handling  
- Regulatory reporting  

The prompts form a **linear workflow pipeline**, enabling end-to-end automation from document input to executive audit summary.

---

## Key Business Problem

Banks process large volumes of regulatory and operational documents manually.

This creates:
- High operational cost  
- Slow processing times  
- Inconsistent outputs  
- Increased regulatory risk  

This prompt library reduces processing time by up to **80–90%**, while improving consistency and standardisation.

---

## Folder Structure

prompt-library/

├── README.md  
│  
├── 01-compliance/  
│   ├── README.md  
│   ├── P01-document-summary.md  
│   ├── P02-policy-extraction.md  
│   ├── P03-compliance-checklist.md  
│  
├── 02-risk/  
│   ├── README.md  
│   ├── P04-risk-identification.md  
│   ├── P05-risk-prioritisation.md  
│  
├── 03-customer-service/  
│   ├── README.md  
│   ├── P06-complaint-triage.md  
│   ├── P07-response-draft.md  
│   ├── P08-escalation-summary.md  
│  
├── 04-reporting/  
│   ├── README.md  
│   ├── P09-regulatory-report.md  
│   ├── P10-audit-summary.md  

---

## Prompt Library Summary

| ID  | Prompt Name                | Workflow           | Automation Level |
|-----|---------------------------|------------------|------------------|
| P01 | Document Summary          | Compliance        | High             |
| P02 | Policy Extraction         | Compliance        | High             |
| P03 | Compliance Checklist      | Compliance        | High             |
| P04 | Risk Identification       | Risk              | High             |
| P05 | Risk Prioritisation       | Risk              | Medium–High      |
| P06 | Complaint Triage          | Customer Service  | Very High        |
| P07 | Response Draft            | Customer Service  | High             |
| P08 | Escalation Summary        | Customer Service  | Medium–High      |
| P09 | Regulatory Report         | Reporting         | Medium–High      |
| P10 | Audit Summary             | Reporting         | Medium           |

---

## Prompt Chaining Workflow

Compliance pipeline:
P01 → P02 → P03 → P04 → P05 → P09 → P10

Customer service pipeline:
P06 → P07 → P08

---

## Prompting Strategies Used

| Strategy              | Purpose |
|----------------------|--------|
| Role-based prompting | Ensures domain-specific outputs |
| Constraints          | Reduces hallucination risk |
| Structured outputs   | Improves consistency and usability |
| Chaining             | Enables workflow automation |
| Iteration (v1.0–v1.2)| Improves reliability over time |

---

## Automation Impact

Estimated improvements:
- 80–90% reduction in processing time  
- Increased consistency across outputs  
- Faster compliance reporting  
- Improved risk visibility  

---

## Risks and Governance

Key risks:
- Incorrect risk classification  
- Hallucinated outputs  
- Over-reliance on automation  
- This system is designed as decision-support, with human validation required for high-risk or regulatory-critical outputs.

Mitigation:
- Human-in-the-loop validation  
- Strict prompt constraints  
- Structured outputs for traceability  

---

## Iteration Evidence

Each prompt includes:
- v1.0 (initial)  
- v1.1 (improved structure)  
- v1.2 (final optimised version)  

This demonstrates continuous improvement and testing.

---

## Next Steps

Recommended implementation:
- Integrate prompts into internal systems  
- Apply human validation for high-risk outputs  
- Monitor performance and refine prompts over time  