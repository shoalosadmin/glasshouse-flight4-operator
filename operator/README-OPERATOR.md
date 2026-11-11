# OPERATION GLASSHOUSE | FLIGHT 4 — Operator pack (blind browser acceptance)

You are the blind browser operator. This pack contains **inputs and instructions only**. It deliberately contains no
expected results. Record exactly what the application shows; do not correct, round or interpret figures. The expected
outcomes are held separately and will be shared after your observations are complete.

Company: **Glasshouse Components Limited** (fictional), stable code **`GLASSHOUSE`**.
FY2024 = 1 Nov 2023 – 31 Oct 2024. FY2025 = 1 Nov 2024 – 31 Oct 2025 (comparative year FY2024).
Application: Statutory Accounts Studio, release `OPERATION-ONE-LEDGER-2`, commit `600d733cd805f258685acc133c825e3d43c768d6`.

## STOP: gates before you start

1. **Do not start** until the owner confirms in writing that the Flight 3 P1 defect is closed. That defect is: opening TB snapshots from an FY2025 workbench can land on FY2024. The owner must also authorise imports into the Glasshouse workspace.
2. Use only the authorised synthetic Glasshouse workspace. Never load these files into a REAL workspace.
3. **Before every Inspect, read the financial year shown on screen and the as-of date you typed.** Record both in the log, and take a screenshot.
4. Nothing you do approves anything. Do not create, request or simulate Finance approval evidence.
5. Inspecting a file writes a provenance record to the workspace, and it makes the last validation stale. This is expected; note it if you see it.

## Files

| File | Use |
| --- | --- |
| `valid/GLASSHOUSE_TB_FY2024_as-of_2024-10-31.csv` | FY2024 trial balance (wide CSV, UTF-8, LF line endings) |
| `valid/GLASSHOUSE_TB_FY2025_as-of_2025-10-31.csv` | FY2025 trial balance |
| `valid/GLASSHOUSE_SOCIE_FY2024_grid-layout.csv` | FY2024 SOCIE: rows, labels, classifications and figures (for setting up and checking the grid) |
| `valid/GLASSHOUSE_SOCIE_FY2024_paste-block.tsv` | FY2024 SOCIE figures only (6 rows × 4 reserves), to paste into the grid |
| `valid/GLASSHOUSE_SOCIE_FY2025_grid-layout.csv` / `..._paste-block.tsv` | FY2025 SOCIE (5 rows × 4 reserves) |
| `negative-controls/NC-*` | Negative controls. **Follow §4 exactly.** Never stage or accept a negative-control TB. |
| `observation-log.csv` | Your log: one row per step |
| `MANIFEST.sha256` | Check the files before you start: `sha256sum -c MANIFEST.sha256` |

TB format: columns `Nominal Number, Nominal Name, GLASSHOUSE, Financial statement, Line item, Line item 2`. Amounts are
signed GBP with two decimals: debits are positive and credits negative. Do not open the files in a spreadsheet and
save them again, because that can change number formats or nominal numbers. Upload the CSV files as they are.

## 1. Load the trial balances

For each year, FY2024 first and then FY2025:

1. Open the company and the year, then go to **Trial balance snapshots**. Confirm on screen that the selected year is the intended one. Record it.
2. Source: **CSV** upload. Choose the matching `valid/` file. As-of date: the year end (`2024-10-31` or `2025-10-31`).
3. Select **Inspect**. Record:
   - every company column, with its match status and blocking codes;
   - the nominal count, total and balance status;
   - the profile, taxonomy and any warnings;
   - any existing revisions listed.

   If the `GLASSHOUSE` header is unresolved, choose the Glasshouse company explicitly and record that you had to.
4. **Stage**, then continue until staging is complete. Record the rows staged and the snapshot status.
5. **Acceptance preview**: record which revisions it would supersede. Then **Accept**. Record the result and the coverage status.

## 2. Accounting structure

1. One Ledger → **Accounting structure** → **Propose from source classes** for FY2025. Record:
   - the statement values;
   - the number of proposals;
   - the unclassified nominals;
   - the class conflicts;
   - each proposal's label and company amount (screenshot).
2. Map `Profit and loss` → **PL** and `Balance sheet` → **BS**. Display signs: **PL −1, BS −1, OTHER +1**. Record the signs you used. Accept all proposals, then preview and confirm the structure version.
3. **Assign to companies** for **FY2025**, then switch the year to **FY2024** and assign again. For each, record unmapped, unallocated, residual and balance-sheet figures from the preview.
4. If the UI offers no way to add totals such as Gross profit or Net assets, or no way to mark a profit line or a balance-sheet equity line, record that as an observation. Do not work around it outside the UI.

## 3. Statements and SOCIE

1. Company-year workbench, **FY2025**:
   - Record every P&L and balance-sheet line with its current and comparative value and status (screenshot).
   - Record whether these lines appear: gross profit, operating profit, profit before tax, profit for the year, net current assets, net assets and total shareholders' funds.
   - Repeat for **FY2024**.
2. **SOCIE, FY2024**:
   1. Open the grid. Set the closing balances to **Entered**.
   2. Arrange 4 reserves in this order: `Called up share capital`, `Share premium account`, `Revaluation reserve`, `Profit and loss account`. Rename the default columns and delete the unused ones.
   3. Arrange the rows exactly as in the layout CSV: the same order, labels and classifications. Choose each classification explicitly. The layout codes match these screen options: `PROFIT_OR_LOSS` = "Profit or loss for the period", `CONTRIBUTION` = "Contribution from owners", `DISTRIBUTION` = "Distribution to owners", `RESERVE_TRANSFER` = "Transfer between reserves". Closing mode "entered by me" = Entered.
   4. Click the top-left figure cell (the opening balance, first reserve). Paste the whole `paste-block.tsv` content.
   5. Compare the grid cell by cell with the layout CSV, then **Save**.
   6. Record the SOCIE status, row totals, closing totals and version.
3. **SOCIE, FY2025**: do the same with the FY2025 files. There are 3 movement rows and no share issue. Record whether the previous closing balances are shown for reference.
4. **Reconcile** FY2025, then FY2024. Record every check row: check, period, status, code, expected, actual, variance and sources (screenshot).
5. Run **Validation** for each year. Record the `SOCIE_RECON` status and every blocker shown. If you try controlled generation, record the refusal. If you try a marked draft, record its markers.

## 4. Negative controls (inspect or save only, as stated)

Before each control, take a screenshot. After it, record the exact codes and messages.

| ID | What to do | Never |
| --- | --- | --- |
| NC-A | Year **FY2025**, as-of `2025-10-31`, CSV `negative-controls/NC-A_GLASSHOUSE_TB.csv`, **Inspect only**. | Stage or accept |
| NC-B | Year **FY2025**, as-of `2025-10-31`, CSV `negative-controls/NC-B_GLASSHOUSE_TB.csv`, **Inspect only**. Record everything shown, including any existing revisions. | **Stage or accept** (that would replace the FY2025 source) |
| NC-C | Year **FY2025**, as-of **`2024-10-31`**, CSV `valid/GLASSHOUSE_TB_FY2025_as-of_2025-10-31.csv`, **Inspect**. | Change the year to make it pass |
| NC-D, NC-E, NC-F | Do each one separately, in this order: open the **FY2025** SOCIE, paste the matching `negative-controls/NC-x_..._paste-block.tsv` at the top-left figure cell, **Save**, **Reconcile**. Record the SOCIE status and every non-passing check with its variance. If Save is refused, record the code. Then go to **history** and **restore the valid FY2025 version** (it is restored as a new version). Reconcile again and record the version numbers. | Leave a negative SOCIE as the current version |

## 5. Log

Use `observation-log.csv`. Fill in one row per step: step id, timestamp, screen, the financial year shown on screen,
the as-of date, the action, the status, codes and messages, figures (copied exactly as shown), a screenshot file name,
and notes. Record what you saw, not what you expected. If a screen lands on a different year from the one you chose,
stop that step and record it as a defect.
