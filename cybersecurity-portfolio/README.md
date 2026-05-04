# 🔐 Internal Network Security Assessment & Risk Analysis

**Author:** Paul Manu  
**Role Demonstrated:** Cybersecurity Analyst / Junior SOC Analyst / Security Consultant  
**Project Type:** Authorized lab simulation and defensive exposure review  
**Primary Tool:** Nmap  

## Executive Overview
This portfolio project demonstrates a professional internal network security assessment. The goal was to identify live hosts, enumerate exposed TCP services, classify security risk, and recommend defensive remediation without exploitation.

The project converts a broad `/24` internal subnet into a prioritized security roadmap that a business or IT team could act on.

## Key Results
| Metric | Result |
|---|---:|
| IP addresses reviewed | 256 |
| Live hosts identified | 20 |
| Major findings documented | 6 |
| High severity findings | 2 |
| Medium severity findings | 3 |
| Low severity findings | 1 |

## Top Findings
1. **Unauthenticated SOCKS5 proxy exposure** - potential traffic relay and policy-bypass risk.
2. **Android Debug Bridge (ADB) exposed on media/Android devices** - unnecessary debug interface exposure.
3. **Gateway/router broad service profile** - sensitive infrastructure device exposing multiple services.
4. **Windows/VMware management surface** - management ports requiring validation and restriction.
5. **IoT/media device concentration** - lateral movement risk if not segmented.

## Skills Demonstrated
- Network enumeration
- Port and service analysis
- Risk classification
- Defensive reporting
- Remediation planning
- Security documentation
- Business-impact communication

## Repository Structure
```text
network-security-assessment/
├── README.md
├── report.md
├── findings-summary.md
├── nmap-output-template.txt
├── screenshots/
└── evidence/

scripts/
├── log-analyzer.py
└── safe-port-inventory-parser.py
```

## Ethical Scope
This project is strictly defensive and educational. It does not include credential attacks, exploitation, malware, bypass instructions, or unauthorized access attempts.

## Interview Summary
> I performed an internal network assessment across a 256-IP subnet, identified 20 live hosts, documented 6 security findings, and produced a remediation roadmap focused on attack-surface reduction, segmentation, and service hardening.
