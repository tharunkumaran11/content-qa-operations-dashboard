# Metrics and data dictionary

## Reporting population

One row is one unique fictional sports-title QA task. 352 source records include five historical completions outside the window; they are retained for context but excluded from period completion/quality/productivity metrics. Eleven other pre-period receipts form opening backlog. There are 336 in-period arrivals and 310 in-period completions. All timestamps are IST, stored as Excel date/time serials. Period start is inclusive; each daily cutoff is inclusive at 23:59:59, except the final fixed snapshot at 18:00. Source timestamps are whole minutes.

## Metric definitions

| Metric | Numerator / denominator or rule | Excel location |
| --- | --- | --- |
| Completed | QA completion timestamp within reporting window | Daily D20; Dashboard C6 |
| Logged hours | Sum actual simulated daily QA work-log hours | Daily F20; Dashboard C7 |
| Productivity | Total completed / total logged hours; n.a. if zero hours | Daily G20; Dashboard C8 |
| Affected-title rate | Completed titles with ≥1 defect / completed titles | Daily K20; Dashboard C9 |
| Clean-title rate | 1 − affected-title rate | Daily L20; Dashboard C10 |
| Defects per check | Defect instances / completed-title checked opportunities | Dashboard C11 |
| SLA adherence | Completed at or before task deadline / all completed | Daily N20; Dashboard C12 |
| TAT | (Completed − Received) × 24, averaged across period completions | Queue Q; Daily O20; Dashboard C13 |
| Closing backlog | Opening + arrivals − completions, or received by cutoff and not completed by cutoff | Daily E; Dashboard C14 |
| Overdue backlog | Open at cutoff AND SLA deadline < cutoff | Daily P; Dashboard C15 |
| Backlog change | Closing − opening | Dashboard J14 |
| Age | (Snapshot − Received) × 24 for open tasks | Queue S |
| Input exceptions | Counts of REVIEW rows, plus reconciliation differences | Guide E16:E21 |

Rates use underlying counts. Example: overall SLA is 213/310 = 68.71%, not AVERAGE of daily SLA percentages. Overall TAT = summed elapsed TAT / 310. Nonzero backlog is not a defect in the workbook; it is a result to discuss.

Title rate versus issue density: 56 affected titles / 310 completed = 18.06%, whereas 69 defects / (310 × 8 opportunities) = 2.78%. A title with two issues adds one to affected titles and two to defect instances. Clean-title rate 81.94% is a content acceptance proxy, not audited reviewer accuracy, defect escape rate or first-pass remediation yield. No independent audit sample exists for those other metrics.

SLA deadline = Received + asset SLA hours / 24. In the simplified simulation: Highlights 8 h, Detail page 24 h, Replay 48 h. Exact deadline completion is on time. Exact deadline with an open task is not overdue until the deadline passes. SLA is calendar elapsed time; it is not working-time SLA. Missed completed SLAs and overdue open items are shown separately to avoid hiding late unprocessed work.

## Queue columns

| Columns | Meaning | Input or formula |
| --- | --- | --- |
| A–F | Unique ID, fictional title, sport, asset type, reviewer, received IST | Input |
| G | SLA deadline from asset-type lookup in Guide | Formula |
| H | Completed IST; blank means open | Input |
| I–K | Defect instances, major count, critical count | Input |
| L | Eight checks per title, applied to completed titles in metrics | Input |
| M–N | Primary category and source note | Input |
| O | Open or Complete from completion timestamp | Formula |
| P | 1 if completed title has ≥1 defect, else 0 | Formula |
| Q | Elapsed TAT hours for complete titles | Formula |
| R | 1 if complete within SLA, else 0 | Formula |
| S | Age hours for open titles at snapshot | Formula |
| T | 1 if open and overdue at snapshot | Formula |
| U | Completion calendar date | Formula |
| V | Duplicate ID/date/count/missing-input checks | Terminal check formula |

Open-task defect counts in the supplied simulation are zero placeholders, not verified clean findings. Open tasks are excluded from all completed-title defect/check denominators.

Hours A–D contain date, reviewer, logged QA hours and source note. E checks missing/invalid hours and duplicate date/reviewer rows. Source tables are filterable; filtering does not scope the dashboard. Blue text identifies input values, amber cells identify editable practice goals and SLAs, and dark text identifies calculations. All data remains visible; nothing is hidden behind macros.

## Capacity and fixed-window limits

COUNTIFS/SUMIFS references are deliberately bounded to Queue 5:504 and Hours 5:104. Guarded formulas support the next reserved row without expanding summary ranges. Adding a row beyond those bounds requires extending the formulas/ranges. The daily reporting window and snapshot are fixed, not unrestricted selectors. Invalid category paste may cause an explicit lookup error; correct inputs rather than masking it.

Missing hours yield n.a. productivity and an exception when a dated work-log row lacks hours. A missing defect count on a completed task is an exception, while a checked zero is valid. Check Guide before trusting results from edited data. Charts are designed for the populated baseline; investigate unavailable daily rates before interpreting a chart after removing hours or completions.
