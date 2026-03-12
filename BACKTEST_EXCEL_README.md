# Backtest Excel Verifier (Local-only)

This repo now includes `Salary_Backtest_Verifier.xml` (SpreadsheetML) which opens directly in Microsoft Excel and behaves like a dynamic formula sheet.

## How to use
1. Open `Salary_Backtest_Verifier.xml` in Excel.
2. Edit **only column B input rows** (rows 4–27).
3. All tax and in-hand outputs auto-recompute.
4. Paste website outputs into the **App Cross-check** block (column D) to verify differences.

## What it verifies
- Old vs New regime taxable income flows.
- HRA/LTA/food/mobile/fuel/uniform/education/hostel exemptions.
- New controls logic:
  - LTA claim scaling.
  - Bill-backed reimbursement scaling.
- Standard deduction/professional tax behavior.
- Chapter VIII deduction limits used in the tool.
- Regime winner and monthly in-hand output.

## Notes
- This file is for **internal backtesting/audit** and not client presentation.
- To regenerate from source, run:
  - `python tools/generate_backtest_excel_xml.py`
