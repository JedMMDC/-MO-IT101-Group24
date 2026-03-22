# Project Tracking Log

## Project
MotorPH Payroll System (Excel-based Java implementation)

## Progress Entries

| Date | Task | Status | Issue Encountered | Resolution | Evidence |
|---|---|---|---|---|---|
| 2026-03-01 | Implement Excel data loading via Apache POI | Done | Java not reading Excel at runtime | Added Apache POI dependencies and workbook parsing | `loadExcelData()` working |
| 2026-03-01 | Configure build/run commands in PowerShell | Done | `javac` not in PATH | Used JDK full path and explicit classpath string | Successful compile/run |
| 2026-03-01 | Improve payroll staff menu flow | Done | Extra unnecessary submenu step | Simplified option flow for employee lookup | Faster user input path |
| 2026-03-02 | Update attendance scope and time rules | Done | Need month coverage and cutoff logic | Added dynamic month handling and 8:00-17:00 policy with grace period and lunch deduction | Verified with sample employees |
| 2026-03-02 | Update deduction basis | Done | Deductions previously not aligned with cutoff-combined requirement | Calculated monthly deductions from combined cutoff gross | Payroll values updated |
| 2026-03-02 | Improve display readability and modularity | Done | Repeated print blocks in payroll output | Extracted helper print methods and cleaner display format | `displayPayroll()` simplified |
| 2026-03-19 | Validate calculations with manual walkthrough | Done | Clarify decimal-hour interpretation | Converted hour fractions to hrs/min explanation and cross-checked sample days | Manual validation documented |

## Current Risks / Notes
- Excel source format changes (column order or sheet names) may break parsing.
- Government deduction tables may need periodic policy updates.

## Next Actions
1. Add automated unit checks for hour and deduction formulas.
2. Separate data model classes from UI/console flow for stronger modularity.
3. Add lightweight exception handling for malformed Excel rows.
