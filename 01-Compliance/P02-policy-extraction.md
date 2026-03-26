# P02 — Policy Extraction

Section: 01 — Compliance  
Workflow step: Step 2 of 7  
Current version: v1.2  
Status: Tested  
Last updated: [26th March]

---

## Prompt Text (v1.2 — current)

You are a compliance analyst at an Australian bank.

Extract key policy rules and requirements from the following document.

Focus only on:
- Explicit compliance obligations
- Required actions
- Responsible roles (if mentioned)

Constraints:
- Use ONLY the provided document
- Do NOT infer or add external knowledge
- Keep wording concise and precise
- - If information is unclear or missing, explicitly state "Insufficient information"

Document:
[DOCUMENT_TEXT]

Output format:
Respond in structured bullet points grouped under:
1. Policy Rules
2. Required Actions
3. Responsible Roles (if available)

---

## Placeholders to fill

| Placeholder     | Source                     | Example                  |
|-----------------|----------------------------|--------------------------|
| DOCUMENT_TEXT   | Internal policy document   | AML compliance policy    |

---

## Intended Workflow or Task

- Trigger: Output from P01 (document summary available)
- Actor: Compliance officer
- Timing: Immediately after summarisation
- Next step: Output feeds into P03

Workflow:
Document summary (P01) → [P02 RUNS] → Extracted rules → P03

---

## Problem Being Solved

Compliance teams manually extract policy requirements from long documents, taking approximately 15–25 minutes per document.

This leads to:
- Delays in compliance workflows
- Inconsistent interpretation across analysts
- Increased risk of missing critical obligations

This prompt reduces extraction time to under 2 minutes and standardises outputs across teams.

Pain points addressed:
- Manual effort
- Inconsistency
- Risk of omission

---

## Automation Potential

Level: High

| Dimension              | Assessment |
|-----------------------|------------|
| Repetitiveness        | Very high — same extraction task across documents |
| Data availability     | High — documents always available |
| Human judgement       | Medium — validation needed for edge cases |
| Integration possibility | High — output feeds into checklist generation |
| Estimated time saving | ~85% — from 20 min to ~3 min |

Human-in-the-loop role:
Compliance officer reviews extracted rules for high-risk regulatory documents.

---

## Risks and Limitations

| Risk                                   | Level  | Mitigation |
|----------------------------------------|--------|------------|
| Missing implicit requirements          | High   | Human validation for critical documents |
| Misclassification of roles             | Medium | Include "if mentioned" constraint |
| Hallucinated rules                     | Medium | "Use only provided document" constraint |
| Over-simplification of complex policies| Medium | Structured extraction format |

Overall risk rating: MEDIUM — suitable with review for critical policies

---

## Version History

### v1.0 — Initial draft
Date: [24th March]  
Prompt: Extract policy rules from the document  
Output: Unstructured text  
Observed effect: Inconsistent output; difficult to reuse  
Lesson learned: Need structured format

---

### v1.1 — Added structure
Date: [25th March]  
Change: Introduced grouped bullet sections  
Output: Improved clarity but inconsistent role extraction  
Observed effect: Missing role assignments  
Lesson learned: Explicitly request role extraction

---

### v1.2 — Structured + constrained extraction (Current)
Date: [26th March]  
Change: Added constraints and role requirement  
Output: Consistent structured extraction  
Observed effect: Reliable outputs across documents  
Lesson learned: Explicit structure + constraints improves reliability