# Architecture Description

This document explains the architectural design of the **Advanced Adversary Simulation Lab**, highlighting the network layout, component responsibilities, and centralized logging approach. The architecture is designed to realistically emulate an enterprise environment while enabling controlled offensive testing and detection validation.

---

## Network Design

The lab uses a segmented virtual enterprise network that mirrors real organizational infrastructure. It consists of an attacker machine, enterprise hosts, and a centralized security monitoring system, all connected within an isolated internal network.

This design allows safe execution of adversary techniques such as lateral movement and credential abuse while ensuring full visibility of attack activity through centralized logging.

---

## Component Roles

- **Kali Linux (Attacker):** Executes reconnaissance, exploitation, and post-exploitation activities using modern red-team tools and C2 frameworks.
- **Windows Server (Domain Controller):** Simulates enterprise Active Directory services and serves as a high-value target.
- **Linux / Windows Endpoints:** Act as initial access and lateral movement targets, generating endpoint telemetry.
- **ELK Stack:** Collects, processes, and visualizes logs for detection and alerting.

Each component has a clearly defined role to ensure realistic attack and detection workflows.

---

## Logging Strategy

A centralized logging model is implemented to provide end-to-end visibility of attacks.

**Log Flow:**

Endpoint → Beat Agent → Logstash → Elasticsearch → Kibana


Security-relevant logs such as authentication events, process execution, and network activity are normalized using Elastic Common Schema (ECS) for consistent analysis across platforms.

---

## Why Centralized ELK

ELK was chosen because it reflects industry-standard SIEM deployments and enables real-time correlation, detection validation, and alerting across multiple systems. It also allows measurement of detection gaps and false positives.

---

## Why Purple Team Approach

A Purple Team approach integrates offensive and defensive operations into a continuous feedback loop. Attacks are executed to validate detections, and findings are used to improve both attack realism and defensive coverage.

---

## Summary

This architecture provides a controlled yet realistic environment for simulating modern adversary behavior and validating security detections, making it suitable for enterprise-grade security assessment and learning.

