# P10 — Audit Summary

Section: 04 — Reporting  
Workflow step: Step 7 of 7  
Current version: v1.2  
Status: Tested  
Last updated: [Date]

---

## Prompt Text (v1.2 — current)

You are a senior audit analyst at an Australian bank.

Generate an executive-level audit summary based ONLY on the provided regulatory report. Outputs must be reviewed before use in regulatory or external reporting

Focus on:
- Key findings  
- Critical risks  
- Overall compliance position  
- Strategic recommendations  

Constraints:
- Use ONLY the provided report  
- Do NOT introduce external information  
- Maintain concise, executive tone  
- Max 200 words  

Input:
[REGULATORY_REPORT]

Output format:
Respond in structured format:

1. Audit Overview  
2. Key Findings  
3. Critical Risks  
4. Compliance Position (Compliant / Partially Compliant / Non-Compliant)  
5. Strategic Recommendations  

---

## Placeholders to fill

| Placeholder         | Source           | Example                      |
|---------------------|------------------|------------------------------|
| REGULATORY_REPORT   | Output from P09  | Generated compliance report  |

---

## Intended Workflow or Task

- Trigger: Regulatory report generated (P09)
- Actor: Audit team / senior management
- Timing: Final step in compliance workflow
- Next step: Executive review and decision-making

Workflow:
P09 → [P10 RUNS] → Audit summary → Management review

---

## Problem Being Solved

Audit summaries are manually created by senior analysts, taking approximately 20–30 minutes per report.

This results in:
- Delays in executive decision-making  
- Inconsistent summary quality  
- High dependency on senior staff  

This prompt reduces summary generation time to under 3 minutes and standardises executive-level reporting.

Pain points addressed:
- Manual summarisation effort  
- Delayed decision-making  
- Inconsistent executive communication  

---

## Automation Potential

Level: Medium

| Dimension               | Assessment |
|------------------------|------------|
| Repetitiveness         | Medium — depends on reporting cycles |
| Data availability      | High — structured report available |
| Human judgement needed | High — executive validation required |
| Integration possibility| High — integrates into reporting workflows |
| Estimated time saving  | ~80% — from 25 min to ~3–4 min |

Human-in-the-loop role:
Senior management reviews and approves audit summaries before strategic decisions.

---

## Risks and Limitations

| Risk                                   | Level  | Mitigation |
|----------------------------------------|--------|------------|
| Oversimplification of critical issues  | High   | Mandatory executive review |
| Misrepresentation of compliance status | High   | Use structured input only |
| Loss of important detail               | Medium | Ensure detailed upstream reports |
| Over-reliance on AI summaries          | Medium | Human oversight required |

Overall risk rating: HIGH — decision-support only, not autonomous

---

## Version History

### v1.0 — Initial draft
Date: [Date]  
Prompt: Summarise report  
Output: Basic summary  
Observed effect: Lacked executive focus  
Lesson learned: Need structured sections

---

### v1.1 — Added structure
Date: [Date]  
Change: Introduced audit sections  
Output: Improved clarity but lacked strategic insight  
Observed effect: Weak recommendations  
Lesson learned: Must include strategic recommendations

---

### v1.2 — Final audit summary (Current)
Date: [Date]  
Change: Added strategic recommendations + constraints  
Output: Clear, executive-ready summary  
Observed effect: Suitable for management use  
Lesson learned: Structure + constraints ensure usability