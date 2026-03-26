# P07 — Response Draft

Section: 03 — Customer Service  
Workflow step: Step 2 of 3 (Customer Pipeline)  
Current version: v1.2  
Status: Tested  
Last updated: [26th March]

---

## Prompt Text (v1.2 — current)

You are a customer service representative at an Australian bank.

Draft a professional response to the customer complaint based ONLY on the triage information provided.

Focus on:
- Clear acknowledgment of the issue  
- Professional and empathetic tone  
- Next steps for resolution  

Constraints:
- Use ONLY the provided input  
- Do NOT admit fault or liability  
- Do NOT include legal or regulatory claims  
- Max 150 words  
- Maintain a formal and respectful tone  

Input:
[TRIAGE_OUTPUT]

Output format:
Write a structured response email including:
- Greeting  
- Acknowledgment of issue  
- Next steps  
- Closing statement  

---

## Placeholders to fill

| Placeholder     | Source          | Example                        |
|-----------------|----------------|--------------------------------|
| TRIAGE_OUTPUT   | Output from P06| Classified complaint details   |

---

## Intended Workflow or Task

- Trigger: Complaint triage completed (P06)
- Actor: Customer service system / agent
- Timing: Immediately after triage classification
- Next step: Output feeds into P08 (escalation summary if required)

Workflow:
Triage (P06) → [P07 RUNS] → Draft response → P08 (if escalation needed)

---

## Problem Being Solved

Customer service agents spend approximately 5–8 minutes drafting responses for each complaint.

This results in:
- Inconsistent tone and messaging  
- Slower response times  
- Increased workload during peak periods  

This prompt reduces response drafting time to under 1 minute and standardises communication quality.

Pain points addressed:
- Manual drafting effort  
- Inconsistent customer experience  
- Delayed response times  

---

## Automation Potential

Level: High

| Dimension               | Assessment |
|------------------------|------------|
| Repetitiveness         | Very high — repeated for every complaint |
| Data availability      | High — triage output always available |
| Human judgement needed | Medium — review needed for sensitive cases |
| Integration possibility| Very high — integrates with CRM/email systems |
| Estimated time saving  | ~85% — from 7 min to ~1 min |

Human-in-the-loop role:
Agents review responses for high-risk or escalated complaints before sending.

---

## Risks and Limitations

| Risk                                      | Level  | Mitigation |
|-------------------------------------------|--------|------------|
| Inappropriate tone                        | High   | Tone constraints + human review |
| Accidental admission of liability         | High   | Explicit constraint in prompt |
| Incorrect or vague next steps             | Medium | Structured output format |
| Over-reliance on automated responses      | Medium | Review for escalated cases |

Overall risk rating: MEDIUM–HIGH — requires review for sensitive interactions

---

## Version History

### v1.0 — Initial draft
Date: [24th March]  
Prompt: Write a response to the complaint  
Output: Informal and inconsistent tone  
Observed effect: Not suitable for professional use  
Lesson learned: Need tone and structure constraints

---

### v1.1 — Added structure and tone
Date: [25th March]  
Change: Introduced professional tone and response sections  
Output: Improved clarity but inconsistent legal framing  
Observed effect: Occasional liability implications  
Lesson learned: Must restrict liability statements

---

### v1.2 — Final response model (Current)
Date: [26th March]  
Change: Added constraints on liability + word limit  
Output: Consistent, professional responses  
Observed effect: Suitable for operational use  
Lesson learned: Constraints ensure compliance-safe communication