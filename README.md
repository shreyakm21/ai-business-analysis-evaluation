# AI-Assisted Business Analysis: Evaluation & Validation

**Status: In progress**

Evaluating four freely accessed AI assistants on retail
business tasks, using Excel-verified answers, documented
failure analysis, and human-review controls.

**Tools evaluated:** ChatGPT, Claude, Microsoft Copilot,
and Gemini.

**Business scenario:** Maple & Main, a fictional retailer.
All business data and documents are synthetic.

## Start here

**[Case study: Correct totals, wrong channel breakdown](case-studies/correct-totals-wrong-breakdown.md)**

An AI response reported correct monthly sales totals but
incorrect channel figures, falsely concluding that Store
sales declined. I checked the source rows against Excel
calculations and documented a verification workflow that
corrected the breakdown.

The original failure and corrected response are preserved
separately.

## Business objective

Identify where AI assistants can support routine business
analysis and operations, what errors require human review,
and what evidence is needed before outputs reach stakeholders.

This project evaluates observed performance on defined cases.
It does not claim a universally best AI tool.

## Completed work

| Case | Task | Evidence |
|---|---|---|
| P01 | Sales-analysis pilot, follow-up, and verification | [12 responses](outputs/P01-sales-pilot/) |
| E01 | Customer email drafting against a return policy | [4 responses](outputs/E01-email/) |
| M01 | Meeting summaries and action tracking | [4 responses](outputs/M01-meeting/) |
| R01 | Operations-report summarization | [4 responses](outputs/R01-report/) |

**Current evidence: 24 saved AI responses.**

The 12 pilot responses are exploratory and reported separately
from the 12 benchmark responses across three completed cases.

## Evaluation workflow

1. Prepare synthetic source material and reference answers.
2. Validate numerical reference answers in Excel.
3. Give each tool the same source and prompt for each case.
4. Preserve the first response unchanged.
5. Check answers against predefined acceptance criteria.
6. Record errors, limitations, scores, and review status.
7. Translate observed failures into proposed governance controls.

The benchmark uses these content dimensions:

- Final answer accuracy
- Supporting calculation and factual accuracy
- Requirement completion
- Evidence boundaries
- Useful depth

Each dimension is scored from 0 to 3, with written reasons.
Scores remain separate; no combined ranking is calculated.

Visual presentation was assessed informally during the pilot
and is not assessed in the completed benchmark cases.

## Selected findings

| Observed issue | Business implication | Proposed control |
|---|---|---|
| Correct totals concealed incorrect channel allocations | A summary could misdirect channel decisions | Verify subgroup calculations against source rows |
| An email omitted the requested refund amount | The customer could receive an incomplete answer | Check required outputs against a policy checklist |
| Meeting notes overstated a dependency | Teams could act on commitments that were never made | Verify owners, deadlines, dependencies, and approvals |
| Report summaries sometimes omitted required facts or added an unstated relationship | Stakeholders could receive incomplete or overstated findings | Check completeness and distinguish evidence from inference |

These are observations from individual cases, not estimates
of how often each tool will fail.

## Method and progress

- [Evaluation methodology](methodology.md)
- [Completed work and next milestones](progress.md)

## Repository guide

| Folder | Contents |
|---|---|
| [data](data/) | Synthetic datasets and source documents |
| [outputs](outputs/) | Original AI responses, including errors |
| [evaluation](evaluation/) | Excel reference calculations, answer keys, and review records |
| [case-studies](case-studies/) | Worked examples of failures, validation, and controls |

Exact prompts are available for the
[completed benchmark cases](prompts/benchmark-prompts.md)
and the [three-stage sales pilot](prompts/pilot-prompts.md).

## My contribution and use of AI

I ran the tool tests, recorded outputs, built and checked
Excel calculations, and maintained the evaluation workbook.

AI assistance supported source-material preparation,
output review, scoring suggestions, and documentation.
The recorded scores are AI-assisted assessments reviewed
by me, rather than independent or blinded evaluations.

## Scope and limitations

- All tools were accessed through accounts reported as free.
- Results describe the tested interfaces and available modes;
  they do not establish performance of paid or enterprise plans.
- Model names are user-reported, not independently verified.
- Each completed benchmark case was tested once per tool.
  Repeatability has not been assessed.
- Pilot follow-ups and verification were conducted in existing
  chats; benchmark cases used fresh chats.
- Response times were recorded for the pilot but not consistently
  for later cases.
- Human review time, correction time, and a controlled manual
  baseline have not been measured. No productivity-saving claim
  is made.
- The cases are small and synthetic, limiting generalization.
- Governance controls are proposed project controls, not a
  certification or evidence of regulatory compliance.

## Next milestones

- [ ] Complete Q01: data Q&A with missing information
- [ ] Add a fresh spreadsheet-analysis benchmark case
- [ ] Publish exact prompts and detailed methodology
- [ ] Consolidate the comparison scorecard
- [ ] Develop the risk register and governance checklist
- [ ] Map selected controls to relevant NIST AI RMF outcomes
- [ ] Prepare a stakeholder decision memo and presentation