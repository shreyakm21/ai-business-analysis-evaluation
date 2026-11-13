# Benchmark Prompts

These prompts were submitted with the corresponding source
file in a fresh chat for each tool.

Tools: ChatGPT, Claude, Microsoft Copilot, and Gemini.
Each case was tested once per tool.

Only the source material was supplied—not the evaluator
workbook or answer key. Original responses are preserved
without corrections.

## E01 — Customer Email Drafting

Source: `E01_Return_Request_Source.txt`

```text
You are a customer-service agent for Maple & Main.

Using only the attached source material, draft a reply to
Alex Morgan's return request.

Provide a subject line and an email body of no more than
180 words, excluding the subject line.

The reply should:
- Address the customer's requests.
- Apply the supplied policy accurately.
- Request any information still needed.
- Explain the applicable refund amount, return-shipping
  arrangement, and refund timing.
- Give a clear next step.
- Use an empathetic, professional tone.

Do not invent procedures, contact details, approvals, or
exceptions. Do not include analysis or internal notes:
provide only the customer-facing email.
```

## M01 — Meeting Notes

Source: `M01_Meeting_Source.txt`

```text
You are a business analyst supporting Maple & Main.

Using only the attached meeting transcript, prepare meeting
notes for the participants.

Include:
1. A brief meeting summary.
2. Confirmed decisions.
3. An action register with columns:
   Action, Status, Owner, Deadline, Dependency or approval.
4. Proposals and conditional future work.
5. Open questions and unconfirmed explanations.

Preserve the distinction between agreed actions, proposals,
and work awaiting assignment. Where an owner or deadline
was not agreed, state that explicitly.

Do not invent commitments, approvals, dates, or causes.
Keep the complete response to no more than 450 words.
```

## R01 — Operations Report Briefing

Source: `R01_Operations_Report_Source.txt`

```text
You are a business analyst supporting Maple & Main.

Using only the attached October operations report, prepare
a management briefing of no more than 400 words.

Include:
1. An executive summary.
2. A performance table covering sales, delivery, returns,
   and customer feedback. Show relevant calculations,
   comparisons, and targets where available.
3. Data-quality issues and limitations that affect
   interpretation.
4. Approved actions with owners and deadlines.
5. Proposals awaiting approval.

Clearly distinguish actual results from targets, calculated
figures from conflicting reported claims, and established
findings from hypotheses.

Do not silently resolve conflicting evidence, generalize
survey findings beyond the supported population, or invent
causes, approvals, or profitability conclusions.
```

## Evaluation notes

Acceptance checks and reference answers were established
before reviewing each benchmark case's outputs.

The evaluation checks:
- Final answer accuracy
- Supporting accuracy
- Requirement completion
- Evidence boundaries
- Useful depth

Presentation was not assessed for these benchmark cases.
Pilot prompts and conversation stages are documented separately.