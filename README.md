# MotorPH Payroll System (Java + Excel)

Single-file Java payroll system that reads employee and attendance data from an Excel file at runtime.

## Included Files

- `PayrollSystemExcel.java` (main program)
- `MotorPH_Employee Data.xlsx` (source data)
- Required library JARs:
  - `poi-5.2.3.jar`
  - `poi-ooxml-5.2.3.jar`
  - `poi-ooxml-lite-5.2.3.jar`
  - `xmlbeans-5.1.1.jar`
  - `commons-collections4-4.4.jar`
  - `commons-compress-1.21.jar`
  - `commons-io-2.11.0.jar`
  - `log4j-api-2.18.0.jar`

## Prerequisites

- Java JDK 21 (or compatible JDK)
- PowerShell (for the commands below)

If `javac`/`java` are not in PATH, use full JDK paths (example below uses Corretto):

- `C:\Users\jedgb\.jdks\corretto-21.0.7\bin\javac`
- `C:\Users\jedgb\.jdks\corretto-21.0.7\bin\java`

## Compile (PowerShell)

```powershell
cd "c:\Users\jedgb\OneDrive\MotorPH Payroll System - New"
$jars = (Get-ChildItem *.jar | ForEach-Object { $_.Name }) -join ";"
& "C:\Users\jedgb\.jdks\corretto-21.0.7\bin\javac" -cp $jars PayrollSystemExcel.java
```

## Run (PowerShell)

```powershell
cd "c:\Users\jedgb\OneDrive\MotorPH Payroll System - New"
$jars = ".;" + ((Get-ChildItem *.jar | ForEach-Object { $_.Name }) -join ";")
& "C:\Users\jedgb\.jdks\corretto-21.0.7\bin\java" -cp $jars PayrollSystemExcel
```

## Login Credentials

- Employee account: `employee`
- Payroll staff account: `payroll_staff`
- Password: `12345`

## Notes

- The program reads data from `MotorPH_Employee Data.xlsx` in the same folder.
- If you see this warning:
  - `Log4j2 could not find a logging implementation...`
  it is non-fatal and does not stop the program.
- Output values may include many decimal places to avoid rounding in displayed computations.

## Repository Contents

This repository is runnable when it includes:

1. `PayrollSystemExcel.java`
2. `MotorPH_Employee Data.xlsx`
3. all required `.jar` files
4. this `README.md`
