# Network Traffic Analysis — DNS Incident Report

## Overview

This project documents the investigation of a real-world-style network incident in which a website (`www.yummyrecipesforme.com`) became completely inaccessible to users. Using tcpdump to analyse captured network traffic, I identified the root cause as a DNS resolution failure caused by an unreachable UDP port 53 on the DNS server — and produced a full incident report with root cause analysis and remediation steps.

---

## Objectives

- Identify the network protocol involved in the failure
- Trace the request-response exchange in the packet capture log
- Determine the root cause of the service disruption
- Recommend remediation steps to resolve and prevent recurrence
---

## Recommended Remediation

| Step | Action |
|------|--------|
| 1 | SSH into 203.0.113.2 and check DNS service status (named / bind9); restart if stopped |
| 2 | Review firewall rules (iptables or equivalent) for any blocks on UDP port 53 |
| 3 | Check server resource usage (CPU, memory, disk) to rule out crash by exhaustion |
| 4 | Set up a secondary/backup DNS server to eliminate single point of failure |
| 5 | Implement DNS monitoring and alerting to catch future failures before users report them |

---

## Skills Demonstrated

- Network traffic analysis (tcpdump)
- DNS and UDP protocol understanding
- ICMP error interpretation
- Incident report writing
- Root cause analysis
- Remediation and redundancy planning

---

## Tools Used

tcpdump
Purpose: Live packet capture and network traffic logging.

*Popoola Moses · Google Cybersecurity Certificate Program*
