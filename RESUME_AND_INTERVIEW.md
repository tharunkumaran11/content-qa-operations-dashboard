# Resume description and interview preparation

## Resume entry

**Content QA Operations and Performance Dashboard — Excel Portfolio Simulation**

- Built an AI-assisted Excel dashboard using 352 simulated cricket and football QA tasks across a 14-day reporting period, tracking productivity, content defects, SLA adherence, turnaround time and backlog.
- Used COUNTIFS, SUMIFS, IF and lookup formulas with six native charts, input validation and documented metric definitions; reconciled daily queue balances and tested calculation boundaries.
- Documented an operations SOP and triage recommendations, clearly separating synthetic results from real work experience and Amazon performance standards.

Short version: Created an Excel content QA operations dashboard from a simulated sports-title dataset, with formula-driven KPIs, daily trends, SLA/backlog tracking and a repeatable reporting SOP.

Do not claim Amazon employment, production use, actual sports streams reviewed, or a real productivity/SLA improvement. Explain AI assistance honestly: AI helped generate synthetic data and build the workbook; you should personally understand the logic and reproduce the checks before claiming independent Excel proficiency.

## Ninety-second project walkthrough

“I built this independent portfolio simulation to understand the operational side of sports content QA. It has 352 fictional cricket and football tasks, four fictional reviewers and 14 days of work logs. The dashboard measures how many titles are completed per logged QA hour, the share of titles with defects, SLA completion, elapsed turnaround and open work.

“I separated title defects from issue counts: one title can have multiple issues. I also kept overdue open work visible instead of relying only on completed-task SLA percentages. In the simulated period, 310 tasks were completed in 217 QA hours, so throughput is 1.43 titles per hour. The closing queue is 37 titles, including 24 overdue. That tells me to investigate capacity, aging work and high-impact defects, rather than simply telling people to go faster.

“The figures are simulated, and the targets are practice assumptions. I checked them against the row data and tested exact SLA deadlines, zero hours, duplicate IDs and closing an open task. I included an SOP so the process can be explained and repeated.”

## Questions and concise answers

**1. Why this project for the DSC Associate role?** The same-role Amazon posting emphasizes processing productivity, content-quality checks and delivery/latency SLAs. This exercise connects routine title QA records to those measures. It demonstrates familiarity, not knowledge of internal Amazon targets.

**2. How did you calculate titles per hour?** Total period completions divided by logged period QA hours: 310 / 217 = 1.4286. I did not average each reviewer’s or each day’s TPH because their hours differ. Logged hours include documentation and work on still-open tasks.

**3. What is the defect rate?** I name the denominator explicitly. Affected-title rate is 56/310 = 18.06%; issue density is 69/2,480 checks = 2.78%. Clean-title rate is the complement of affected-title rate. These are not reviewer error rates.

**4. How is SLA different from turnaround time?** TAT is elapsed receipt-to-completion time. SLA asks whether that time met the assigned deadline. A 14-hour TAT passes a 24-hour task but misses an 8-hour task. At the exact deadline, completion counts as on time.

**5. Why show backlog and overdue work?** Completed-task SLA can look healthy even while unprocessed work is late. Backlog shows unfinished volume; overdue backlog adds the missed-deadline dimension. I would inspect age, deadline and impact when prioritizing.

**6. Why isn’t everything green?** I designed a simulation with a growing queue and missed practice targets. A useful QA dashboard exposes the issue and helps frame a response; it should not manufacture a success story.

**7. What would you do first in this scenario?** Check input integrity, then triage the 24 overdue open titles and escalate critical issues. Compare incoming volume with capacity, investigate recurrent metadata issues and discuss workload. I would use the approved SOP and escalation process rather than invent release decisions.

**8. Did you improve SLA or reduce defects?** No real improvement experiment occurred. I identified simulated risk and proposed next steps. To show improvement, I would need comparable measured before/after data, consistent denominators and consideration of workload mix.

**9. How did you validate the workbook?** Independent row-by-row calculations were compared with saved Excel results; daily balances and sport/reviewer totals reconciled. Temporary input edits tested hours, SLA equality, missing data, duplicate IDs and queue completion. Charts are bound to calculated cells. Native desktop Excel interaction was not available in the build session.

**10. How would you handle an unclear SOP instruction?** Avoid guessing a pass. Record the ambiguity and evidence, pause the affected decision if needed, ask the responsible lead through the approved channel and document the clarified instruction. Do not quietly change thresholds.

**11. Is the dataset actual Amazon data?** No. Every team, task, timestamp, reviewer, hour and defect is fictional and labelled simulated. The requested job page could not be retrieved; an accessible official listing for the same role informed the public-duty alignment.

**12. Could this unfairly rank reviewers?** Yes, if used without context. Task length/type, queue mix, investigation effort and open work differ. The reviewer section supports questions about workload; it is not a performance rating or a fair ranking by itself.

## Practice STAR answer

Situation: “In a portfolio simulation, I modeled a sports content QA queue with mixed cricket/football tasks and increasing unfinished work.”

Task: “I wanted a simple way to explain throughput, content-quality signals, SLA compliance and backlog together.”

Action: “I defined each denominator, built row calculations and daily summaries, added charts, wrote an SOP, and checked the results with independent calculations and boundary edits.”

Result: “The completed dashboard showed 310 simulated completions, 1.43 titles per hour, 68.71% SLA and 37 open tasks. It made overdue work and content-defect spikes visible. The deliverable is a reproducible training project; it did not create a real operational improvement.”

## Hands-on rehearsal

1. Point to a Queue row and explain receipt, deadline, completion, defects and elapsed TAT.
2. Reproduce 310/217 and 213/310 with a calculator.
3. Explain 11 + 336 − 310 = 37 without adding daily backlog snapshots.
4. Add one hour to an existing Hours row and explain why TPH falls. Restore the value.
5. Set a completion exactly to its deadline and explain why SLA met = 1. Restore it.
6. Filter overdue open tasks, describe an escalation priority, and explain why the filter does not change totals.
7. Say clearly what AI assisted and what you personally checked or learned.
