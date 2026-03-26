# P05 — Risk Prioritisation

Section: 02 — Risk  
Workflow step: Step 5 of 7  
Current version: v1.2  
Status: Tested  
Last updated: [26th March]

---

## Prompt Text (v1.2 — current)

You are a senior risk analyst at an Australian bank.

Prioritise the identified risks based ONLY on the input provided. Outputs must be reviewed before use in regulatory or external reporting.


Focus on:
- Severity of impact  
- Likelihood of occurrence  
- Potential business impact (financial, regulatory, reputational)  

Constraints:
- Use ONLY the provided risks  
- Do NOT introduce new risks  
- Be consistent in scoring  
- Keep explanations concise  

Input:
[RISK_LIST]

Output format:
Respond in structured format:

For each risk:
- Risk ID: [number]  
- Risk Type: [Regulatory / Operational / Financial / Reputational]  
- Severity: [Low / Medium / High]  
- Likelihood: [Low / Medium / High]  
- Priority Score: [1–5 scale, where 5 = highest priority]  
- Priority Rank: [1 = highest]  
- Justification: [brief explanation]  

Sort output from highest to lowest priority.

Limit to maximum 8 risks.

---

## Placeholders to fill

| Placeholder   | Source          | Example                     |
|---------------|----------------|-----------------------------|
| RISK_LIST     | Output from P04| Identified compliance risks |

---

## Intended Workflow or Task

- Trigger: Risk identification completed (P04)
- Actor: Risk analyst / compliance manager
- Timing: Immediately after risk identification
- Next step: Output feeds into P09 (regulatory reporting)

Workflow:
Risk list (P04) → [P05 RUNS] → Prioritised risks → P09

---

## Problem Being Solved

Risk prioritisation is typically manual and subjective, taking approximately 20–30 minutes per case.

This results in:
- Inconsistent prioritisation across analysts  
- Delayed response to high-impact risks  
- Poor allocation of compliance resources  

This prompt reduces prioritisation time to under 3 minutes and introduces a structured scoring system.

Pain points addressed:
- Subjective decision-making  
- Delayed risk response  
- Inefficient resource allocation  

---

## Automation Potential

Level: Medium–High

| Dimension               | Assessment |
|------------------------|------------|
| Repetitiveness         | High — repeated for each risk set |
| Data availability      | High — derived from P04 |
| Human judgement needed | High — final decisions require oversight |
| Integration possibility| High — feeds into reporting and escalation |
| Estimated time saving  | ~80% — from 25 min to ~5 min |

Human-in-the-loop role:
Risk manager validates top-priority risks before action or reporting.

---

## Risks and Limitations

| Risk                                      | Level  | Mitigation |
|-------------------------------------------|--------|------------|
| Incorrect prioritisation                  | High   | Human validation for top-ranked risks |
| Oversimplified scoring                    | Medium | Use structured criteria and justification |
| Bias in likelihood estimation             | Medium | Keep scoring constrained and transparent |
| Over-reliance on AI output                | High   | Require managerial approval before decisions |

Overall risk rating: HIGH — decision-support only, not fully autonomous

---

## Version History

### v1.0 — Initial draft
Date: [Date]  
Prompt: Rank risks  
Output: Basic ranking  
Observed effect: No scoring logic; unclear reasoning  
Lesson learned: Need scoring system

---

### v1.1 — Added scoring
Date: [Date]  
Change: Introduced severity and likelihood  
Output: Improved ranking but inconsistent justification  
Observed effect: Weak explanation of priorities  
Lesson learned: Must include justification field

---

### v1.2 — Final prioritisation model (Current)
Date: [Date]  
Change: Added scoring scale + ranking + constraints  
Output: Structured and consistent prioritisation  
Observed effect: Reliable decision-support outputs  
Lesson learned: Structured scoring improves decision quality