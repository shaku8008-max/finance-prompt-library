# P03 — Compliance Checklist Generation

Section: 01 — Compliance  
Workflow step: Step 3 of 7  
Current version: v1.2  
Status: Tested  
Last updated: [Date]

---

## Prompt Text (v1.2 — current)

You are a compliance analyst at an Australian bank.

Using the extracted policy rules below, generate a compliance checklist for operational use.

Focus on:
- Actionable compliance tasks  
- Clear verification steps  
- Measurable completion criteria  

Constraints:
- Use ONLY the provided input  
- Do NOT add external rules or assumptions  
- Each checklist item must be specific and testable  
- Max 12 checklist items  

Input:
[POLICY_RULES]

Output format:
Respond as a structured checklist with:
- Item number  
- Requirement  
- Verification method  

Example format:
1. Requirement: [requirement]  
   Verification: [how to verify compliance]

---

## Placeholders to fill

| Placeholder     | Source                  | Example                         |
|-----------------|------------------------|----------------------------------|
| POLICY_RULES    | Output from P02        | Extracted AML policy rules       |

---

## Intended Workflow or Task

- Trigger: Policy rules extracted (P02 completed)
- Actor: Compliance officer / operations team
- Timing: Immediately after policy extraction
- Next step: Output feeds into P04 (risk identification)

Workflow:
Policy extraction (P02) → [P03 RUNS] → Checklist → P04

---

## Problem Being Solved

Compliance teams manually convert policy documents into actionable checklists, taking approximately 15–20 minutes per document.

This results in:
- Inconsistent checklist formats across teams  
- Missed verification steps  
- Delays in compliance audits  

This prompt reduces checklist creation time to under 2 minutes and standardises compliance verification processes.

Pain points addressed:
- Manual checklist creation  
- Inconsistent formatting  
- Risk of incomplete compliance tracking  

---

## Automation Potential

Level: High

| Dimension               | Assessment |
|------------------------|------------|
| Repetitiveness         | Very high — checklist generation is standardised |
| Data availability      | High — derived directly from policy rules |
| Human judgement needed | Medium — validation for regulatory edge cases |
| Integration possibility| High — can integrate into audit systems |
| Estimated time saving  | ~85% — from 20 min to ~3 min |

Human-in-the-loop role:
Compliance officer reviews checklist completeness for high-risk regulatory processes.

---

## Risks and Limitations

| Risk                                      | Level  | Mitigation |
|-------------------------------------------|--------|------------|
| Missing critical compliance step          | High   | Human validation for regulatory-critical checklists |
| Over-generalised checklist items          | Medium | Enforce "specific and testable" constraint |
| Incorrect interpretation of policy rules  | Medium | Dependency on accurate P02 output |
| Checklist too long or impractical         | Low    | Limit to max 12 items |

Overall risk rating: MEDIUM — effective with review for critical workflows

---

## Version History

### v1.0 — Initial draft
Date: [Date]  
Prompt: Generate a checklist from policy rules  
Output: Generic checklist  
Observed effect: Items too vague; not actionable  
Lesson learned: Need verification criteria

---

### v1.1 — Added structure
Date: [Date]  
Change: Introduced requirement + verification format  
Output: Improved clarity but inconsistent detail level  
Observed effect: Some checklist items still broad  
Lesson learned: Must enforce specificity

---

### v1.2 — Final structured checklist (Current)
Date: [Date]  
Change: Added constraints on specificity and item limits  
Output: Clear, actionable, audit-ready checklist  
Observed effect: Consistent and usable outputs  
Lesson learned: Constraints improve operational usability