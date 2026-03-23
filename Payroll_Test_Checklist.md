# Payroll System Test Checklist

## Scope
Validation checklist for payroll calculations, attendance handling, and output behavior.

## Functional Checks

- [x] Program loads employee and attendance data from Excel at runtime.
- [x] Login accepts `employee` and `payroll_staff` with valid password.
- [x] Invalid credentials are rejected with clear message.
- [x] Employee lookup handles non-existent employee numbers.
- [x] Payroll processing works for one employee and all employees.

## Attendance & Hour Computation Checks

- [x] Login at or before 8:10 AM is treated as 8:00 AM.
- [x] Login after 8:10 AM uses actual login time.
- [x] Logout after 5:00 PM is capped at 5:00 PM.
- [x] Logout before 5:00 PM uses actual logout time.
- [x] One-hour lunch break is deducted per working day.
- [x] Negative computed hours are clamped to 0.
- [x] Month display is based on months found in attendance data.

## Payroll & Deduction Checks

- [x] Cutoff 1 and cutoff 2 gross values are computed from hours × hourly rate.
- [x] Deductions (SSS, PhilHealth, Pag-IBIG, Tax) use combined monthly gross.
- [x] Total deductions and net salary are shown for cutoff 2.
- [x] Results display without numbered output labels.

## Manual Edge-Case Spot Checks

- [x] Late login day produces fractional hours correctly.
- [x] Day with early logout (< 5:00 PM) computes correctly.
- [x] Day with grace-period login still yields full 8 hours (before deductions/lunch policy).
- [x] Decimal-hour interpretation confirmed (`5h 55m = 5.916667`).

## Evidence
- Console runs completed with employee samples 10001 and 10034.
- Manual date-level walkthrough performed for June and September cutoffs.
