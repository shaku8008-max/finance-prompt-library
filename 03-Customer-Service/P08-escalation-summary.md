# P08 — Escalation Summary

Section: 03 — Customer Service  
Workflow step: Step 3 of 3 (Customer Pipeline)  
Current version: v1.2  
Status: Tested  
Last updated: [26th March]

---

## Prompt Text (v1.2 — current)

You are an internal operations analyst at an Australian bank.

Summarise the escalated customer issue for internal review and routing.

Focus on:
- Core issue  
- Risk level  
- Reason for escalation  
- Recommended department  

Constraints:
- Use ONLY the provided input  
- Do NOT include assumptions or external information  
- Keep output concise and structured  
- Max 120 words  

Input:
[TRIAGE_OUTPUT_AND_RESPONSE]

Output format:
Respond in structured format:

- Issue Summary: [brief description]  
- Risk Level: [Low / Medium / High]  
- Escalation Reason: [why escalation is required]  
- Recommended Department: [Fraud / Compliance / Operations / Customer Support]  
- Suggested Action: [next step]

---

## Placeholders to fill

| Placeholder                     | Source            | Example                         |
|--------------------------------|------------------|----------------------------------|
| TRIAGE_OUTPUT_AND_RESPONSE     | P06 + P07 outputs| Complaint + drafted response     |

---

## Intended Workflow or Task

- Trigger: Complaint marked for escalation (from P06 or P07)
- Actor: Internal operations / escalation team
- Timing: Immediately after escalation decision
- Next step: Output feeds into internal handling or reporting systems

Workflow:
Triage + Response → [P08 RUNS] → Escalation summary → Internal routing

---

## Problem Being Solved

Escalated complaints require manual summarisation by agents, taking approximately 5–10 minutes per case.

This leads to:
- Delays in escalation handling  
- Inconsistent summaries across teams  
- Misrouting of issues to incorrect departments  

This prompt reduces summarisation time to under 1 minute and standardises escalation communication.

Pain points addressed:
- Manual summarisation effort  
- Routing inefficiencies  
- Delayed issue resolution  

---

## Automation Potential

Level: Medium–High

| Dimension               | Assessment |
|------------------------|------------|
| Repetitiveness         | High — repeated for escalated cases |
| Data availability      | High — inputs from P06 and P07 |
| Human judgement needed | Medium — validation for critical escalations |
| Integration possibility| High — integrates with ticketing systems |
| Estimated time saving  | ~85% — from 8 min to ~1 min |

Human-in-the-loop role:
Operations team reviews high-risk escalations before assignment.

---

## Risks and Limitations

| Risk                                   | Level  | Mitigation |
|----------------------------------------|--------|------------|
| Incorrect routing to department        | High   | Human validation for high-risk cases |
| Misinterpretation of escalation reason | Medium | Structured fields enforced |
| Oversimplified issue summary           | Medium | Include required fields |
| Over-reliance on automation            | Medium | Manual review for critical escalations |

Overall risk rating: MEDIUM–HIGH — requires oversight for sensitive cases

---

## Version History

### v1.0 — Initial draft
Date: [24th March]  
Prompt: Summarise escalation  
Output: Basic summary  
Observed effect: Missing routing and action details  
Lesson learned: Need structured fields

---

### v1.1 — Added structure
Date: [25th March]  
Change: Introduced risk level and department  
Output: Improved clarity but inconsistent action suggestions  
Observed effect: Weak next-step guidance  
Lesson learned: Must include suggested action

---

### v1.2 — Final escalation summary (Current)
Date: [26th March]  
Change: Added action + constraints + word limit  
Output: Clear, structured internal summary  
Observed effect: Reliable routing outputs  
Lesson learned: Structure ensures operational usability