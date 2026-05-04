# Internal Network Security Assessment & Risk Analysis

**Prepared by:** Paul Manu  
**Assessment Type:** Internal network enumeration and exposure review  
**Environment:** Authorized lab simulation  
**Primary Scan Evidence:** User-supplied Nmap output and companion screen recording  
**Primary Command:** `nmap -A -T4 192.168.2.0/24`  
**Assessment Period:** March 24-30, 2026  

## 1. Executive Summary
An authorized internal network assessment was performed against the `192.168.2.0/24` subnet to identify live hosts, exposed TCP services, and visible attack surface. The evidence showed 256 IP addresses reviewed, 20 live hosts identified, and 6 major findings prioritized for remediation.

The highest-priority exposures were an unauthenticated SOCKS5 proxy, Android Debug Bridge exposed on media/Android devices, and broad service exposure on the network gateway/router. The work was enumeration-focused and did not include exploitation, credential attacks, or unauthorized access.

## 2. Business Context
This assessment simulates what a cybersecurity analyst or junior security consultant would provide to an organization after an internal exposure review. The purpose is to reduce attack surface, improve visibility, and help technical stakeholders decide which systems require hardening first.

## 3. Scope and Limitations
**In scope:** Host discovery, TCP service enumeration, service interpretation, risk classification, and remediation planning.

**Out of scope:** Exploitation, brute force, credential guessing, malware, traffic interception, destructive testing, and unauthorized access attempts.

## 4. Methodology
Nmap was used to perform discovery, service/version detection, OS fingerprinting, selected script checks, and traceroute. Results were interpreted through a defensive lens: open ports were treated as exposure indicators, not proof of compromise.

## 5. Key Metrics
| Metric | Result |
|---|---:|
| IP addresses reviewed | 256 |
| Live hosts identified | 20 |
| Major findings | 6 |
| High severity | 2 |
| Medium severity | 3 |
| Low severity | 1 |

## 6. Findings Overview
| ID | Severity | Host(s) | Finding |
|---|---|---|---|
| F1 | Medium | 192.168.2.1 | Gateway/router exposes multiple services |
| F2 | High | 192.168.2.18 / 192.168.2.57 | ADB exposed on Android/Amazon devices |
| F3 | High | 192.168.2.128 | SOCKS5 proxy reports no authentication |
| F4 | Medium | 192.168.2.42 | Windows/VMware management services exposed |
| F5 | Medium | Multiple IoT/media devices | Casting/control services visible on LAN |
| F6 | Low | 192.168.2.101 | Apple AirTunes/RTSP service visible |

## 7. Security Analysis
Internal networks are often over-trusted. A single exposed debug interface, proxy service, or unsegmented IoT device can increase lateral movement risk. This project demonstrates how an analyst moves from raw scan output to business-relevant security decisions.

## 8. Remediation Roadmap
### Immediate: 0-7 Days
- Disable ADB where not required.
- Identify and secure/remove the SOCKS5 proxy.
- Restrict router administrative and discovery services.

### Near Term: 1-4 Weeks
- Validate Windows/VMware services.
- Apply host firewall restrictions.
- Document intended services and asset owners.

### Ongoing
- Segment IoT devices from laptops/workstations.
- Maintain firmware and OS updates.
- Schedule periodic re-scans and track drift.

## 9. Portfolio Value
This project demonstrates practical cybersecurity analysis: safe enumeration, prioritization, business-impact writing, and remediation planning. It is designed to be shared with recruiters, hiring managers, and interviewers as proof of work.
