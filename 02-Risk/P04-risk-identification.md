# P04 — Risk Identification

Section: 02 — Risk  
Workflow step: Step 4 of 7  
Current version: v1.2  
Status: Tested  
Last updated: [Date]

---

## Prompt Text (v1.2 — current)

You are a risk analyst at an Australian bank.

Identify potential risks based ONLY on the compliance checklist provided.

Focus on:
- Regulatory risks  
- Operational risks  
- Financial risks  
- Reputational risks  

Constraints:
- Use ONLY the provided checklist  
- Do NOT introduce external assumptions  
- Flag uncertainty where information is insufficient  
- Be concise and precise 
- If information is unclear or missing, explicitly state "Insufficient information"

Input:
[COMPLIANCE_CHECKLIST]

Output format:
Respond in structured format:

For each risk:
- Risk Type: [Regulatory / Operational / Financial / Reputational]  
- Description: [clear explanation]  
- Severity: [Low / Medium / High]  
- Reason: [why this risk exists based on input]  

Limit to maximum 8 risks.

---

## Placeholders to fill

| Placeholder              | Source          | Example                         |
|--------------------------|----------------|----------------------------------|
| COMPLIANCE_CHECKLIST     | Output from P03| AML compliance checklist         |

---

## Intended Workflow or Task

- Trigger: Compliance checklist generated (P03 completed)
- Actor: Risk analyst
- Timing: Immediately after checklist generation
- Next step: Output feeds into P05 (risk prioritisation)

Workflow:
Checklist (P03) → [P04 RUNS] → Risk list → P05

---

## Problem Being Solved

Risk identification is currently performed manually by analysts, taking approximately 20–30 minutes per checklist.

This leads to:
- Inconsistent risk identification across analysts  
- Delayed escalation of critical risks  
- Increased exposure to regulatory breaches  

This prompt reduces identification time to under 3 minutes while improving consistency and coverage.

Pain points addressed:
- Manual risk assessment  
- Delayed detection  
- Inconsistent risk classification  

---

## Automation Potential

Level: High

| Dimension               | Assessment |
|------------------------|------------|
| Repetitiveness         | Very high — repeated across all compliance workflows |
| Data availability      | High — checklist always available |
| Human judgement needed | High — critical decisions require oversight |
| Integration possibility| High — feeds into prioritisation systems |
| Estimated time saving  | ~85% — from 25 min to ~3–4 min |

Human-in-the-loop role:
Risk analyst reviews high-severity risks before escalation.

---

## Risks and Limitations

| Risk                                           | Level  | Mitigation |
|------------------------------------------------|--------|------------|
| Missing critical risks                         | High   | Mandatory review for high-risk outputs |
| Incorrect severity classification              | High   | Secondary validation in P05 |
| Over-reliance on incomplete checklist          | Medium | Ensure checklist quality from P03 |
| Hallucinated risks                             | Medium | "Use ONLY input" constraint |

Overall risk rating: HIGH — requires human validation for decision-making

---

## Version History

### v1.0 — Initial draft
Date: [Date]  
Prompt: Identify risks from checklist  
Output: Unstructured list  
Observed effect: No severity; inconsistent categorisation  
Lesson learned: Need structured classification

---

### v1.1 — Added structure
Date: [Date]  
Change: Introduced risk type and severity  
Output: Better organisation but inconsistent reasoning  
Observed effect: Weak justification of risks  
Lesson learned: Must include reasoning field

---

### v1.2 — Final structured risk output (Current)
Date: [Date]  
Change: Added reasoning + constraints + limit  
Output: Clear, structured, and consistent risks  
Observed effect: Reliable identification across cases  
Lesson learned: Explicit reasoning improves reliability