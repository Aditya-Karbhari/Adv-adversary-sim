# Lessons Learned

## What Was Successfully Detected
- Command-and-control communication via Sliver
- Credential dumping attempts
- PowerShell-based post-exploitation
- SSH brute-force attacks on Linux endpoints

## What Was Missed
- Certain persistence mechanisms
- Low-noise Active Directory reconnaissance
- Short-lived lateral movement attempts

## Improvements Identified
- Add registry and scheduled-task monitoring rules
- Improve baseline profiling for normal user behavior
- Introduce correlation rules across multiple data sources
- Enhance alert severity using contextual risk scoring

## Key Takeaway
Effective detection requires continuous tuning and correlation rather than reliance on isolated alerts.
