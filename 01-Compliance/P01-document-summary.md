# P01 — Document Summary

Section: 01 — Compliance  
Workflow step: Step 1 of 7  
Current version: v1.2  
Status: Tested  
Last updated: [26th March]

---

## Prompt Text (v1.2 — current)

You are a compliance analyst at an Australian bank.

Summarise the following document for internal compliance review.

Focus only on:
- Key regulatory obligations  
- Operational processes  
- Any risks or gaps  

Constraints:
- Use ONLY the provided document  
- Do NOT include external knowledge or assumptions  
- Max 200 words  
- Professional tone
- If information is unclear or missing, explicitly state "Insufficient information"

Document:
[DOCUMENT_TEXT]

Output format:
Respond in structured bullet points under:
1. Key obligations  
2. Processes described  
3. Potential risks  

---

## Placeholders to fill

| Placeholder     | Source                     | Example                  |
|-----------------|----------------------------|--------------------------|
| DOCUMENT_TEXT   | Internal policy / report   | AML compliance document  |

---

## Intended Workflow or Task

- Trigger: New regulatory or operational document uploaded
- Actor: Compliance officer
- Timing: Immediate upon document ingestion
- Next step: Output feeds into P02

Workflow:
Document uploaded → [P01 RUNS] → Summary → P02

---

## Problem Being Solved

Compliance teams spend approximately 20–30 minutes manually reviewing each document.

At scale, this results in:
- High operational cost
- Delays in compliance processing
- Risk of missing key regulatory requirements

This prompt reduces review time to under 2 minutes per document while improving consistency across outputs.

Pain points addressed:
- Manual effort
- Processing delays
- Risk of omission

---

## Automation Potential

Level: High

| Dimension               | Assessment |
|------------------------|------------|
| Repetitiveness         | Very high — repeated across all documents |
| Data availability      | High — documents always available |
| Human judgement needed | Medium — critical documents require review |
| Integration possibility| High — feeds downstream prompts |
| Estimated time saving  | ~90% — from 25 min to ~2 min |

Human-in-the-loop role:
Compliance officer reviews summaries for high-risk or regulatory-critical documents.

---

## Risks and Limitations

| Risk                                   | Level  | Mitigation |
|----------------------------------------|--------|------------|
| Missing critical regulatory detail     | High   | Mandatory review for high-risk documents |
| Hallucination                          | Medium | "Use ONLY provided document" constraint |
| Over-summarisation                     | Medium | Structured output format enforced |
| Misinterpretation of complex policies  | Medium | Secondary validation step in P02 |

Overall risk rating: MEDIUM — suitable with targeted human oversight

---

## Version History

### v1.0 — Initial draft
Date: [24th March]  
Prompt: Summarise the document  
Output: Generic summary  
Observed effect: Lacked compliance focus; inconsistent outputs  
Lesson learned: Need structured sections and role context

---

### v1.1 — Added structure and role
Date: [25th March]  
Change: Introduced role + structured sections  
Output: Improved clarity but inconsistent risk identification  
Observed effect: Missing risk-related insights  
Lesson learned: Explicitly request risk identification

---

### v1.2 — Final structured version (Current)
Date: [26th March]  
Change: Added constraints + risk focus + word limit  
Output: Consistent and usable summaries  
Observed effect: Reliable outputs across multiple test cases  
Lesson learned: Constraints + structure ensure production-ready outputs