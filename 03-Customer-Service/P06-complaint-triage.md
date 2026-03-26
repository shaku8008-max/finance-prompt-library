# P06 — Complaint Triage

Section: 03 — Customer Service  
Workflow step: Step 1 of 3 (Customer Pipeline)  
Current version: v1.2  
Status: Tested  
Last updated: [Date]

---

## Prompt Text (v1.2 — current)

You are a customer service triage analyst at an Australian bank.

Classify the following customer complaint and determine the appropriate handling path.

Focus on:
- Complaint category  
- Urgency level  
- Regulatory sensitivity  
- Recommended next action  

Constraints:
- Use ONLY the provided complaint text  
- Do NOT assume missing details  
- Be concise and consistent  
- Flag uncertainty if information is incomplete  

Input:
[COMPLAINT_TEXT]

Output format:
Respond in structured format:

- Complaint Category: [Billing / Transaction / Fraud / Service / Other]  
- Urgency Level: [Low / Medium / High]  
- Regulatory Sensitivity: [Low / Medium / High]  
- Recommended Action: [brief action step]  
- Escalation Required: [Yes / No]  
- Reason: [brief justification]

---

## Placeholders to fill

| Placeholder       | Source              | Example                          |
|-------------------|---------------------|----------------------------------|
| COMPLAINT_TEXT    | Customer message    | Disputed transaction complaint   |

---

## Intended Workflow or Task

- Trigger: Customer complaint received
- Actor: Customer service system / support team
- Timing: Immediate upon complaint intake
- Next step: Output feeds into P07 (response drafting)

Workflow:
Complaint received → [P06 RUNS] → Triage classification → P07

---

## Problem Being Solved

Customer complaints are manually triaged by agents, taking approximately 5–10 minutes per case.

This results in:
- Delays in response times  
- Inconsistent classification across agents  
- Missed high-risk or regulatory-sensitive cases  

This prompt reduces triage time to under 30 seconds and standardises classification across all complaints.

Pain points addressed:
- Manual classification effort  
- Slow response times  
- Risk of misrouting complaints  

---

## Automation Potential

Level: Very High

| Dimension               | Assessment |
|------------------------|------------|
| Repetitiveness         | Extremely high — every complaint requires triage |
| Data availability      | High — complaint text always available |
| Human judgement needed | Medium — edge cases require review |
| Integration possibility| Very high — fits into ticketing systems |
| Estimated time saving  | ~90% — from 8 min to <1 min |

Human-in-the-loop role:
Agents review high-urgency or regulatory-sensitive complaints.

---

## Risks and Limitations

| Risk                                   | Level  | Mitigation |
|----------------------------------------|--------|------------|
| Misclassification of complaint         | High   | Human review for high urgency cases |
| Incorrect urgency assessment           | High   | Escalation flag + review process |
| Missing regulatory sensitivity         | Medium | Explicit classification requirement |
| Over-reliance on automation            | Medium | Human oversight for escalations |

Overall risk rating: MEDIUM–HIGH — requires oversight for critical cases

---

## Version History

### v1.0 — Initial draft
Date: [Date]  
Prompt: Classify complaint  
Output: Basic category only  
Observed effect: Missing urgency and escalation logic  
Lesson learned: Need multi-factor classification

---

### v1.1 — Added structure
Date: [Date]  
Change: Introduced urgency and escalation fields  
Output: Better classification but inconsistent reasoning  
Observed effect: Weak justification of decisions  
Lesson learned: Must include reasoning field

---

### v1.2 — Final triage model (Current)
Date: [Date]  
Change: Added regulatory sensitivity + constraints  
Output: Consistent, structured triage output  
Observed effect: Reliable classification across cases  
Lesson learned: Multi-factor structure improves accuracy