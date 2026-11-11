# GLASSHOUSE | FLIGHT 4
## Independent native-browser operator mission

**Application:** [Isolated native Apps Script candidate](https://script.google.com/macros/s/AKfycbzPKIlNdRi4dsT1OAMngcQE9WQHA9aAVQqZJ21GFlue/dev)  
**Candidate release:** `OPERATION-ONE-LEDGER-4`  
**Candidate SHA:** `05e17b73bc75b1a3c7c60e1626e40109afc5e1e3`  
**Input pack:** [Flight 4 operator files](https://github.com/shoalosadmin/Statutory-Accounts-Builder/tree/glasshouse-flight4-operator-pack/flight4/operator)  
**Runbook:** `flight4/operator/README-OPERATOR.md`

### Authority and starting state

The owner has authorised this isolated test and accepted its commissioning audit. **Do not ask again for setup, release markers, audit output or permission to begin.** The native app has previously loaded with a connected backend and an empty portfolio. Confirm the current UI state and proceed.

Your role is an independent **browser operator**, not a developer. Use the native application's visible controls and the input pack. Do not inspect source files, pull requests, engineering evidence, code, test scripts, other GitHub branches, or any reference/expected-answer material. Do not call undocumented backend APIs or use a simulated application. Do not edit the app's code, project, deployment or GitHub repository.

The operator pack is now present in the repository. The pack's README was written for an earlier candidate. Where its **release identification, commissioning gate or assumptions about available controls** conflict with this mission or the current UI, follow this mission and record the discrepancy. Do **not** change the frozen input files.

Use only invented inputs and the dedicated test installation. Do not access employer data, the preserved older Glasshouse project, or any real account records. Do not invent or bypass Finance approval; do not file or publish statutory accounts.

### Journey A | Company and years

Using the native UI, create or, if already present from this same test session, locate:

- **Glasshouse Components Limited**, code `GLASSHOUSE`, effective `2023-11-01`.
- **FY2024**, `2023-11-01` to `2024-10-31`.
- **FY2025**, `2024-11-01` to `2025-10-31`, with FY2024 as the predecessor.

Record the IDs returned by the app and verify that the header, company-year view and One Ledger display the same selected context. Do not duplicate records that are already present.

### Journey B | Import the operator trial balances

Read `flight4/operator/README-OPERATOR.md` and use the two unchanged files under `valid/`:

- `GLASSHOUSE_TB_FY2024_as-of_2024-10-31.csv`
- `GLASSHOUSE_TB_FY2025_as-of_2025-10-31.csv`

For each year, select the context, choose the relevant file through the native input, inspect, stage, complete staging, preview acceptance and accept for working if the app and the instructions permit it. Record the displayed balance, warnings, dates, company matches, snapshot IDs and results.

Check that selections remain consistent when moving between the workbench and TB snapshots in **both directions**, and after browser reload/history navigation. If an unexpected company or year appears, document it and avoid actions that could change the wrong record.

**Native file chooser:** if you cannot operate a ChromeOS native picker, ask the owner to select the named file. Reading a CSV on GitHub is not the same as successfully uploading it. Do not report an import until the app shows evidence of one.

### Journey C | Accounting structure and totals

In the ordinary UI, inspect and propose source-class lines. Configure any necessary statement mapping, display signs, subtotals, reconciliation roles and formula dependencies using the controls available. Preview, confirm and assign a structure to both years where permitted.

Record all configured terms/signs and actual calculated amounts. Explore invalid formula/cycle/role configurations through the UI only, and record the actual response, not an anticipated one. Do not infer target figures from repository implementation or manually enter values intended solely to force a reconciliation.

### Journey D | Independently entered SOCIE

Read the relevant `valid/` SOCIE grid-layout and paste-block files. Enter the figures from those files through the visible SOCIE editor, independently of the trial balance and calculated statements. Save each year separately; inspect reconciliation and version history.

Record **exactly what is displayed**: amounts, source labels, status, variance, continuity and any refusals. A displayed PASS or FAIL is an observation, not independent proof of correct accounting.

### Journey E | Negative-control observations

Follow **section 4 of the operator pack README** precisely. The files and steps are pre-labelled NC-A through NC-F; those labels identify inputs, **not expected application answers**.

- NC-A, NC-B and NC-C: perform the specified inspection-only actions. Record the exact UI outcome. Do not stage or accept these inputs.
- NC-D, NC-E and NC-F: enter and save each supplied variant separately, attempt reconciliation, record each observed check and variance, and restore the valid version between attempts as instructed.
- Where a step cannot be completed safely through the UI, record `BLOCKED` or `NOT TESTED`, with a specific reason.

Do not interpret the expected result from the test name, and do not consult implementation tests or reference reports to find the intended result.

### Journey F | Draft document observation

If the UI permits a demonstration or explicitly unapproved draft **without Finance approval**, generate and inspect it. Do not create approval evidence or bypass a refusal.

Record the contents and presentation of the actual Word file, including company/period headings, current and comparative columns, statement amounts, signs, subtotals and SOCIE. Compare what appears only with your entered source figures and the visible UI, **not with a hidden expected document**. Record discrepancies without presuming which ones will occur.

### Evidence and handback

For each step, log the visible action, date/time, screen, selected company/year, input file, observed results, financial amounts and error messages. Preserve screenshots where possible. Use `PASS` (step completed as directed), `FAIL` (observed incorrect behaviour), `BLOCKED` or `NOT TESTED`, and distinguish usability problems from financial discrepancies. Do not hide errors or invent progress.

Provide one Flight 4 report covering:

1. Actual native URL and release context tested.
2. Journey A–F statuses, including what was genuinely completed.
3. Recorded IDs and figures for *later* independent checking.
4. Reproducible UI or financial defects and evidence.
5. Cross-view company/year behaviour.
6. Document presentation observations.
7. Work still blocked or untested.

**STOP after reporting.** No source changes, GitHub edits, new engineering campaigns, merges or deployment actions.

The objective is independent observed behaviour, not confirmation of an answer key.
