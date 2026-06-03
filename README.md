# Audit Script for Microsoft Windows 11 Enterprise Edition

A PowerShell-based security audit toolkit for Windows 11 Enterprise, built in accordance with the **CIS (Center for Internet Security) Benchmark Level 1** controls.

## Overview

This project automates the auditing of Windows 11 Enterprise security configurations. It checks system settings against CIS Benchmark Level 1 standards and generates a report of satisfied and non-satisfied controls.

## Features

- 12 modular PowerShell audit scripts covering key security domains
- Checks for password policies, account lockout, user rights assignments, and privilege controls
- Outputs results to `satisfied.txt` and `not_satisfied.txt` for easy review
- Python GUI (`audit_results_gui.py`) to visualize audit results

## Security Domains Covered

- Password Policy (CIS 1.1.x)
- Account Lockout Policy (CIS 1.2.x)
- User Rights Assignment (CIS 2.2.x)
- Security Options
- Firewall Settings
- Audit Policies

## How to Run

1. Open PowerShell as **Administrator**
2. Run each script individually:
3. Check `satisfied.txt` and `not_satisfied.txt` for results
4. Run `audit_results_gui.py` with Python to view results visually

## Contributors

- Tanish Arora
- Vallabh SD

## References

- [CIS Benchmarks](https://www.cisecurity.org/cis-benchmarks)
- [NIST National Vulnerability Database](https://nvd.nist.gov/)
