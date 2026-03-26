# P09 — Regulatory Report Generation

Section: 04 — Reporting  
Workflow step: Step 6 of 7  
Current version: v1.2  
Status: Tested  
Last updated: [Date]

---

## Prompt Text (v1.2 — current)

You are a compliance reporting analyst at an Australian bank.

Generate a structured regulatory report based ONLY on the provided inputs. Outputs must be reviewed before use in regulatory or external reporting

Focus on:
- Summary of compliance findings  
- Key risks identified  
- Compliance status  
- Recommended actions  

Constraints:
- Use ONLY the provided inputs  
- Do NOT introduce external knowledge  
- Maintain professional, formal tone  
- Max 300 words  
- If information is unclear or missing, explicitly state "Insufficient information"

Input:
[DOCUMENT_SUMMARY]  
[POLICY_RULES]  
[COMPLIANCE_CHECKLIST]  
[RISK_PRIORITISATION]

Output format:
Respond in structured report format:

1. Executive Summary  
2. Key Compliance Findings  
3. Identified Risks  
4. Compliance Status (Compliant / Partially Compliant / Non-Compliant)  
5. Recommended Actions  

---

## Placeholders to fill

| Placeholder              | Source              | Example                        |
|--------------------------|--------------------|--------------------------------|
| DOCUMENT_SUMMARY         | Output from P01    | Document summary               |
| POLICY_RULES             | Output from P02    | Extracted policy rules         |
| COMPLIANCE_CHECKLIST     | Output from P03    | Compliance checklist           |
| RISK_PRIORITISATION      | Output from P05    | Ranked risk list               |

---

## Intended Workflow or Task

- Trigger: Risk prioritisation completed (P05)
- Actor: Compliance reporting team
- Timing: End of compliance analysis workflow
- Next step: Output feeds into P10 (audit summary)

Workflow:
P01 → P02 → P03 → P04 → P05 → [P09 RUNS] → Report → P10

---

## Problem Being Solved

Regulatory reports are manually compiled by analysts, taking approximately 30–60 minutes per report.

This results in:
- High labour cost  
- Delayed reporting timelines  
- Inconsistent reporting formats  

This prompt reduces report generation time to under 5 minutes while ensuring structured and consistent outputs.

Pain points addressed:
- Manual report creation  
- Inconsistent formatting  
- Delays in regulatory reporting  

---

## Automation Potential

Level: Medium–High

| Dimension               | Assessment |
|------------------------|------------|
| Repetitiveness         | High — repeated across compliance cycles |
| Data availability      | High — all inputs available from prior steps |
| Human judgement needed | High — final approval required |
| Integration possibility| High — can integrate into reporting systems |
| Estimated time saving  | ~85% — from 45 min to ~5–7 min |

Human-in-the-loop role:
Compliance manager reviews report before submission to regulators.

---

## Risks and Limitations

| Risk                                   | Level  | Mitigation |
|----------------------------------------|--------|------------|
| Incorrect compliance status            | High   | Mandatory managerial review |
| Misrepresentation of risks             | High   | Use structured inputs only |
| Over-simplification of complex issues  | Medium | Ensure detailed inputs from prior steps |
| Hallucinated content                   | Medium | Strict "use only input" constraint |

Overall risk rating: HIGH — requires human validation before external use

---

## Version History

### v1.0 — Initial draft
Date: [Date]  
Prompt: Generate compliance report  
Output: Unstructured report  
Observed effect: Inconsistent format; missing key sections  
Lesson learned: Need defined report structure

---

### v1.1 — Added structure
Date: [Date]  
Change: Introduced report sections  
Output: Improved clarity but inconsistent compliance status  
Observed effect: Weak classification of compliance  
Lesson learned: Must explicitly define compliance status

---

### v1.2 — Final report model (Current)
Date: [Date]  
Change: Added constraints + compliance status field  
Output: Structured, professional report  
Observed effect: Consistent outputs across cases  
Lesson learned: Structure ensures business usability