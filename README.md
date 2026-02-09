# Advanced Adversary Simulation Lab (Purple Team Capstone)

This project implements an enterprise-grade adversary simulation lab using a Purple Team methodology. 
A full attack lifecycle was executed—from initial access and command-and-control to credential dumping, 
Active Directory enumeration, persistence, and lateral movement—mapped to MITRE ATT&CK techniques.

The lab uses modern red-team tooling (Sliver C2, SharpHound, BloodHound) and validates detections 
using an ELK-based SIEM with Sysmon and Winlogbeat telemetry. Each attack phase is correlated with 
real-time detections, alert rules, and risk scoring to demonstrate practical security monitoring.

## Tools Used
Kali Linux, Sliver C2, SharpHound, BloodHound, Sysmon, Winlogbeat, Elasticsearch, Logstash, Kibana, MITRE ATT&CK

## Disclaimer
This project was performed in a controlled lab environment for educational purposes only.
