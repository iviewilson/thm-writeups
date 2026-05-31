# TryHackMe Write-up: Blue Team Introduction
**Path:** SOC Level 1 | **Module:** Blue Team Introduction  
**Status:** ✅ Completed | **Badge Earned:** First Step into SOC  
**Author:** Ivie Wilson | [TryHackMe Profile](https://tryhackme.com/p/iivie56)

---

## 📋 Overview

This module introduced the foundational concepts of Blue Team operations and what it means to work as a Junior SOC Analyst. It covered the day-to-day responsibilities of a security analyst, how security operations centers function, and how analysts detect, investigate, and respond to threats.

---

## 🎯 Learning Objectives

- Understand the role and responsibilities of a Junior SOC Analyst
- Learn how a Security Operations Center (SOC) is structured
- Understand the difference between Blue Team and Red Team
- Learn how alerts are generated, triaged, and escalated
- Identify what tools SOC analysts use daily

---

## 🔑 Key Concepts Learned

### 1. What is a SOC?
A Security Operations Center is a team of security professionals who monitor, detect, investigate, and respond to cybersecurity threats 24/7. The SOC is the frontline defense of an organization's digital infrastructure.

**SOC Tiers:**
| Tier | Role | Responsibility |
|---|---|---|
| Tier 1 | Junior Analyst | Alert triage, initial investigation |
| Tier 2 | Senior Analyst | Deep investigation, threat hunting |
| Tier 3 | SOC Manager / IR | Incident response, escalation management |

### 2. Blue Team vs Red Team
| Blue Team | Red Team |
|---|---|
| Defensive security | Offensive security |
| Detect and respond to attacks | Simulate attacks to find weaknesses |
| SIEM, IDS/IPS, firewalls | Penetration testing, exploitation |
| Reactive and proactive | Adversarial mindset |

### 3. The Junior SOC Analyst Role
A Junior SOC Analyst (Tier 1) is responsible for:
- Monitoring security dashboards and SIEM alerts
- Performing initial triage on incoming alerts
- Investigating indicators of compromise (IOCs)
- Escalating confirmed threats to Tier 2
- Documenting findings in incident reports

### 4. The Alert Triage Process
When an alert comes in, a Tier 1 analyst follows this process:

```
Alert Received
    ↓
Is it a False Positive?
    ↓ No
Gather Evidence (IP, logs, timestamps)
    ↓
Check Threat Intelligence (VirusTotal, AbuseIPDB)
    ↓
Determine Severity (Low / Medium / High / Critical)
    ↓
Document Findings
    ↓
Escalate if confirmed malicious
```

### 5. Key SOC Tools
| Tool | Purpose |
|---|---|
| SIEM (Splunk, QRadar) | Aggregate and analyze security logs |
| Wireshark | Network packet analysis |
| VirusTotal | File and URL reputation checking |
| AbuseIPDB | IP address reputation lookup |
| TheHive | Incident management platform |
| MISP | Threat intelligence sharing |

---

## 🔬 Practical Exercise: Junior Analyst Simulation

In the hands-on lab, I played the role of a Junior SOC Analyst investigating a live alert.

**Scenario:** A suspicious IP address was flagged trying to connect to the organization's network.

**Steps taken:**
1. Received alert in the SOC dashboard
2. Noted the flagged IP: `221.181.185.159`
3. Searched the IP on AbuseIPDB → Found **47 abuse reports**
4. Identified threat categories: **C2 Server, Port Scanner, PlugX malware**
5. Determined country of origin: **China**
6. Classified severity as: **HIGH**
7. Added comment: *"Malicious IP — involved in 4 cyber attacks, C2 Server, PlugX malware, Port Scan activity"*
8. Blocked the IP and escalated to Tier 2 analyst

**Key finding:** The IP `221.181.185.159` was linked to the **China Mobile Communications Corporation** and had been actively involved in PlugX malware distribution — a known APT tool used by Chinese threat actors.

---

## 💡 What I Learned

1. **Triage is everything** — Not every alert is a real threat. The ability to quickly determine true positives vs false positives is the most valuable skill a Tier 1 analyst can have.

2. **Documentation matters** — Every action taken during an investigation must be documented. This creates an audit trail and helps senior analysts make faster decisions.

3. **Threat intelligence tools are essential** — AbuseIPDB, VirusTotal, and Shodan are free tools that can tell you in seconds whether an IP, file, or URL has been flagged before.

4. **Escalation is not failure** — Knowing when to escalate to Tier 2 is a sign of professionalism, not weakness. Junior analysts are not expected to resolve everything alone.

5. **Pattern recognition is key** — Over time, analysts develop intuition for what "normal" network traffic looks like, making anomalies easier to spot.

---

## 🏆 Badge Earned

**First Step into SOC** — Awarded for completing the Blue Team Introduction module on TryHackMe's SOC Level 1 path.

---

## 🔗 References & Tools Used

- [TryHackMe SOC Level 1 Path](https://tryhackme.com/path/outline/soclevel1)
- [AbuseIPDB](https://www.abuseipdb.com)
- [VirusTotal](https://www.virustotal.com)
- [MITRE ATT&CK Framework](https://attack.mitre.org)

---

## 📌 About the Author

**Ivie Wilson** — Cybersecurity Analyst| IT Support Specialist | Frontend Developer  
📍 Lagos, Nigeria · Available for Remote Roles  
🔗 [iviewilson.com](https://iviewilson.com) | [GitHub](https://github.com/iviewilson) | [LinkedIn](https://linkedin.com/in/iviewilson)

*Currently studying for CompTIA Security+ (SY0-701) · Google Cybersecurity Certificate ✅*
