# Content QA operations reporting SOP

Version 1.0 — 25 November 2026. Training simulation for a content QA associate. All example values and thresholds are fictional.

## 1. Set up the reporting window

Use the fixed 2–15 November 2026 period and 15 November 18:00 IST snapshot for this exercise. Review Guide before editing. Ensure the computer understands all stored timestamps as IST; Excel values do not carry time-zone metadata. Practice SLAs run continuously in calendar hours, including overnight and weekends. Actual teams must use their approved SLA policy instead.

## 2. Capture a task once

Enter a unique Task ID, fictional title, Cricket/Football sport, asset type, assigned reviewer and received timestamp in Queue. The exercise provides 352 examples and has space through row 504. G is the calculated SLA deadline; O:V are formulas. Never overwrite those formula cells. Multiple defects in one title remain one processed title.

The eight planned content checks are: title/competition metadata, participants/date/time, detail-page links/availability, image, subtitles, audio, video and player/accessibility behavior. They describe simulated QA scope; no actual media was reviewed in this project. In a real task, carry out each authorized check and capture evidence before entering a completion.

## 3. Complete QA and record findings

Only enter Completed IST when the QA review is finished and a disposition/escalation has been recorded. Enter zero for a genuinely checked title with no defects. Leave Completed blank when the QA task remains open. Defect instances, major and critical counts must be nonnegative, major plus critical cannot exceed total, and total cannot exceed the eight checked opportunities in this simplified model. Each opportunity can record at most one defect here.

Select a primary defect category when a defect is found: Metadata, Image, Subtitles, Audio or Video. Multiple instances may occur in a title; the primary-category chart counts affected titles once and is not an issue-instance breakdown. Critical/major counts are practice classifications and require team definitions before real use.

Completing QA does not mean all defects are fixed. Hold/escalate critical issues and track correction/retest separately; do not treat a completed review as permission to publish. This dashboard tracks the intake/review queue, not the remediation queue.

## 4. Record time honestly

In Hours, enter one row per reviewer and date, including logged QA hours spent reviewing, documenting and progressing open tasks. Exclude breaks, training and unrelated activity. All 56 provided rows are simulated. Never create hours by dividing completed titles by a target. Productivity is completed titles divided by total logged QA hours, not a simple average of individual rates.

## 5. Review the dashboard and triage

First inspect Guide input/reconciliation checks; all counts/differences should be zero. Filter Queue to Input check = REVIEW if needed, fix source inputs and confirm the exceptions clear. Do not hide invalid inputs by suppressing formula errors.

Then filter Open and Overdue flag = 1. Review deadlines, open age and customer impact; escalate critical issues promptly through an approved channel. Use the sport/reviewer summaries to ask about workload and task complexity. An affected-title rate measures defects detected in content, not mistakes made by the associate. Keep detection quality and productivity balanced.

Discuss daily trends with their denominators. A daily spike with 17 completed tasks is different from one with 100. Compare SLA compliance for completed tasks with overdue open backlog; a good completed-task percentage can hide unprocessed late work. The simulation has 37 open and 24 overdue titles at the snapshot.

## 6. Check calculations before sharing

Confirm opening + receipts − completions = closing each day. Reconcile sport/reviewer completions to the total and primary-category titles to affected titles. Check zero-hours days display n.a. for productivity, and do not interpret n.a. as zero or as meeting a target. The final day stops at 18:00; other days stop at 23:59:59.

Targets in Guide are practice assumptions only. No team or Amazon performance standard should be inferred. For this fixed exercise, change numeric assumptions or task inputs within the existing period. Changing the period/snapshot requires extending or rebuilding Daily dates and captions and verifying the new cohort; this is not an unrestricted date-selector dashboard.

## 7. Export and preserve provenance

Save a dated workbook, keep raw CSV inputs, check all chart labels, and review the simulation banner before sharing. When source data changes, CSV/JSON snapshots and the PNG preview must be re-exported; they are static and do not automatically follow later Excel edits. Reconcile all outputs and regenerate checksums after packaging changes. Keep the simulation label and AI-assistance disclosure visible in GitHub and interviews.
