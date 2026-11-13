# P01 — Sales Pilot Prompts

Source file: `sales_validation_v0.csv`

Four tools were tested: ChatGPT, Claude, Microsoft Copilot,
and Gemini.

The initial prompt was submitted in a fresh chat with the
source CSV attached. The follow-up and verification prompts
were submitted in that same conversation for each tool.

No evaluator workbook or answer key was supplied.

These three stages are exploratory pilot evidence.
They are not three independent benchmark runs.

## Stage 1 — Initial Analysis

```text
You are assisting the operations manager of Maple & Main,
a fictional retailer.

Analyze only the attached synthetic sales dataset. Do not use
external sources.

Definitions:
- Each row represents one product line from a separate order.
- Units_Sold includes units subsequently returned.
- Discount_Rate applies to every unit on that line.
- Returned units receive the discounted purchase price.
- Returns occur in the original sale month.
- All monetary amounts are INR, excluding tax and shipping.

Net sales = (Units_Sold - Units_Returned) × Unit_Price_INR
            × (1 - Discount_Rate).

Produce:
1. Total net sales.
2. Net sales by month.
3. Month-over-month net sales growth for August and September.
4. Net sales by channel and the difference between channels.
5. A short management summary, no more than 120 words,
   separating observed findings from possible explanations.
6. State whether the data establishes:
   a. Which channel is more profitable.
   b. Whether successful marketing caused September's growth.

Show your calculation method. Round monetary amounts to two
decimal places and growth percentages to two decimal places.
Clearly identify questions the supplied data cannot answer.
```

## Stage 2 — Follow-up Analysis

The CSV was not reattached. No tool requested reattachment.

```text
Using the same attached sales dataset, explain September’s
net-sales increase compared with August.

1. Show August and September net sales for Online and Store.
2. Calculate each channel’s absolute change and its percentage
   contribution to the total net-sales increase.
3. State whether the dataset lets us investigate changes in
   units sold, returns, discounts, and product mix. Distinguish
   numerical analysis from evidence of external causes.
4. Can we conclude that marketing caused the increase?
5. Finish with a management summary of no more than 80 words.
   Make every growth comparison period explicit.

Use only the supplied dataset. Show your method and flag any
limitations.
```

## Stage 3 — Structured Verification

The same audit instruction was submitted to all four tools.
No tool requested reattachment.

```text
Audit your previous September-versus-August analysis against
the original attached CSV. Do not assume your earlier figures
or statements are correct.

1. List all 12 August and September source rows, showing:
   Line_ID, month, channel, product, units sold, units returned,
   unit price, discount rate, and calculated net sales.

2. Recalculate monthly net sales by channel directly from
   those rows. Show the contributing Line_IDs for each group.

3. Recalculate each channel's absolute change and percentage
   contribution to the total September-over-August increase.

4. Check your previous factual statements about units,
   returns, prices, discounts, and product mix against the
   source data. Distinguish numerical contributions from
   external causes.

5. List any errors or misleading statements in your previous
   response and correct them. If you find none, say so.
   Do not invent an error simply because an audit was requested.

6. Provide a corrected management summary of no more than
   80 words, making comparison periods explicit.

Use only the original CSV. If you cannot access it, state
that limitation and request reattachment rather than guessing.
```

## Recorded Response Completion Times

Seconds from prompt submission until the answer finished
displaying, including thinking and analysis where present.
File upload and human review are excluded.

| Tool | Initial | Follow-up | Verification |
|---|---:|---:|---:|
| ChatGPT | 20.00 | 28.65 | 32.65 |
| Claude | 21.00 | 30.36 | 45.59 |
| Microsoft Copilot | 28.36 | 23.66 | 36.74 |
| Gemini | 47.66 | 19.93 | 34.59 |

Initial tests were recorded on 28 October 2026.
Dates for later stages are not confirmed in this document.

Each time is a single observation, not a reliable speed
ranking. These timings do not establish productivity savings.

## Evidence and Interpretation

- [Original responses](../outputs/P01-sales-pilot/)
- [Worked failure case study](../case-studies/correct-totals-wrong-breakdown.md)

The verification stage corrected Copilot's incorrect channel
breakdown in this conversation. It did not erase the earlier
failure or establish that verification always succeeds.

Gemini's verification response retained or introduced
inaccurate commentary, demonstrating why self-audits still
require independent checking.