# Calculation and package verification

Verified 25 November 2026. Result: PASS for the checks described below. The data is simulated.

## Independent calculation checks

Read the delivered CSVs independently with Python and reopened the saved XLSX with openpyxl in read-only analysis mode. Checked 8,072 values against independently computed expectations: all populated Queue inputs and calculated outputs, 56 hour-log records, every daily metric, headline metrics, sport/reviewer summaries, defect categories, open-age buckets, guarded blank rows and reconciliation checks.

Confirmed 352 unique source IDs, 310 in-period completions, 217 QA hours, 11 opening titles, 336 arrivals and 37 closing titles. Five completed-before-period records are excluded. The 14 daily balances reconcile; their closing queues are independently counted from timestamps. Checked weighted rates and turnaround, exact period boundaries and final partial-day cutoff. No saved Excel error cells were found.

See validation/Independent_readback.json for results and chart references.

## Live input and boundary checks

The authoring calculation engine was exercised with temporary edits. All edits were restored before export.

- Increasing logged hours by 1 changes overall TPH to completed/(hours+1).
- Completion exactly at deadline passes SLA; one minute after fails.
- A day with zero logged hours displays n.a. for TPH.
- Future completions and missing completed-title defect counts are flagged REVIEW; zero defects is valid.
- Completing one open task adds one completion and removes one backlog title.
- Adding a task in the next reserved row updates completed volume without editing summary ranges.
- Duplicate task IDs flag both affected rows.
- Open title exactly at its deadline is not overdue; one minute later is overdue.
- Two defects on one previously clean title add one affected title, not two.
- Duplicate date/reviewer work logs are flagged on both rows.

## Charts and usability

Verified six native charts and their saved range references, chart series and line strokes in XLSX XML. All series reference Daily calculated cells, not static screenshots. Source filtering, reserved-row formulas, dropdown/number validation and freeze panes are present. Visually reviewed the complete Dashboard and representative data/calculation views on all five sheets. Corrected the defect-category axis so all five labels are shown. The final dashboard PNG is included as a preview.

## What was not tested

Native desktop Excel was not available, so the build does not claim live Excel engine interaction, printing or Excel-version compatibility testing. Standard Excel formulas and charts were used; authoring recalculation and saved XLSX results were checked. The dashboard has a fixed reporting window and bounded reserved rows. It is not an unrestricted live date selector or production dashboard. No sports media, physical device or actual Amazon workflow was tested.

## Packaging

The final archive contains the workbook, simulated source data, definitions, SOP, README, resume/interview preparation, role-source/provenance notes, preview and validation reports. Local Markdown links were checked. SHA256SUMS.txt covers every other file. The ZIP was reopened, CRC-checked and its file bytes compared with the finalized folder. No credentials or working scripts are included. Publication was subsequently requested for https://github.com/tharunkumaran11/content-qa-operations-dashboard. Uploaded file hashes are checked against local content before publication.
