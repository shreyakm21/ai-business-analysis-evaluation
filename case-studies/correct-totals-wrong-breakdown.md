# Correct Totals, Wrong Channel Breakdown

## Business question

Which sales channel contributed to Maple & Main’s
September-over-August net-sales increase?

Maple & Main is a fictional retailer. All source data
in this project is synthetic.

## The failure

During a follow-up analysis, Microsoft Copilot reported
correct overall monthly net sales but allocated those sales
incorrectly between Online and Store.

It concluded that Store sales declined, although the source
data showed a small increase.

| Metric | AI follow-up output | Verified result |
|---|---:|---:|
| August Online net sales | INR 12,540 | INR 12,120 |
| August Store net sales | INR 15,160 | INR 15,580 |
| August total | INR 27,700 | INR 27,700 |
| September Online net sales | INR 19,950 | INR 17,550 |
| September Store net sales | INR 13,300 | INR 15,700 |
| September total | INR 33,250 | INR 33,250 |
| Online change | +INR 7,410 | +INR 5,430 |
| Store change | −INR 1,860 | +INR 120 |
| Online contribution to total increase | 133.51% | 97.84% |
| Store contribution to total increase | −33.51% | 2.16% |

Contributions above 100% or below zero can be valid when one
channel offsets another. Here, they were incorrect because
the underlying channel figures were wrong.

## How I validated the result

I used an Excel reference workbook to calculate line-level
net sales from the source data:

Net sales = (units sold − units returned)
            × unit price × (1 − discount rate)

I checked the month/channel groups against their source rows:

- August Online: L008, L010, L012
- August Store: L007, L009, L011
- September Online: L013, L015, L017
- September Store: L014, L016, L018

The verified total increase was INR 5,550:

- Online contributed INR 5,430, or 97.84%.
- Store contributed INR 120, or 2.16%.

## Why the error matters

Checking grand totals alone would not have detected the
incorrect allocation.

A manager relying on the AI summary could have wrongly
concluded that Store performance was deteriorating.

The original follow-up response was therefore marked as
not approved for decision use.

## Verification intervention

I submitted the same structured verification prompt to all
four evaluated tools. It required source rows, grouped
calculations, and an audit of earlier statements.

Copilot then corrected its channel figures, contributions,
and Store-decline conclusion, explicitly acknowledging
the earlier errors.

This correction was recorded separately. It did not replace
or erase the original failure.

## Governance control

Before decision use, a human reviewer must verify
decision-relevant calculations, groupings, and conclusions
against source evidence. Matching grand totals alone
is insufficient.

## Evidence

- [Original follow-up response](../outputs/P01-sales-pilot/P01_Copilot_Followup1.txt)
- [Verification response](../outputs/P01-sales-pilot/P01_Copilot_Verification1.txt)

Source data and the Excel evaluator workbook are provided
in the repository’s data and evaluation folders.

## Limitations and transparency

This is one observed conversation sequence using a small
synthetic dataset. It does not establish a general error
rate or overall ranking of AI tools.

The verification response demonstrates correction in this
instance, not guaranteed reliability.

AI assistance was used to prepare test materials, review
outputs, and draft documentation. I performed the Excel
validation and maintained the evaluation records.