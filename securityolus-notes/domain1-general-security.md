# Domain 1 – General Security Concepts (SY0-701)

This file contains my notes and portfolio-style explanations of Domain 1 concepts for the CompTIA Security+ SY0-701 exam.  
I also connect them to real SOC analyst work where possible.  

---

## 1.1 Security Controls
Security controls are safeguards to protect information and systems.  

### Types of Controls
- **Technical Controls** – technology-based  
  - Examples: Firewalls, IDS/IPS, encryption, authentication systems  
- **Administrative Controls** – policies & procedures  
  - Examples: Security training, background checks, change management  
- **Physical Controls** – protect physical assets  
  - Examples: Locks, fences, guards, CCTV  

### Control Functions
- **Preventive** – stop incidents (MFA, firewalls)  
- **Detective** – identify incidents (IDS, SIEM alerts)  
- **Corrective** – fix after incidents (patches, backups)  
- **Deterrent** – discourage attackers (warning banners, guards)  
- **Compensating** – backup controls when primary fails  

**SOC Relevance:** Analysts often investigate alerts triggered by detective controls and confirm whether preventive controls worked or failed.  

---

## 1.2 CIA Triad
The three pillars of cybersecurity:  

- **Confidentiality** – restricts access to authorized users (encryption, VPNs).  
- **Integrity** – ensures data isn’t altered without detection (hashing, digital signatures).  
- **Availability** – ensures systems are accessible when needed (redundancy, backups).  

**SOC Relevance:** Many alerts fall under CIA concepts, e.g., ransomware attacks threaten both **integrity** and **availability**.  

---

## Non-Repudiation
- **Definition:** Proof that someone performed an action, and they cannot deny it later.  
- **Achieved with:**  
  - Digital signatures  
  - Hashing + encryption  
  - Audit logs  

**Example:** A signed email or logged VPN connection provides evidence the action really happened.  

**SOC Relevance:** Analysts rely on log integrity and timestamps to prove insider activity during investigations.  

---

## 1.3 AAA – Authentication, Authorization, and Accounting
- **Authentication:** Verifies identity (passwords, biometrics, tokens, MFA).  
- **Authorization:** Determines what actions a user can perform (RBAC, ABAC).  
- **Accounting (Auditing):** Tracks user actions (logins, file access).  

**SOC Relevance:**  
- Authentication → alerts on failed logins.  
- Authorization → escalation when users attempt to access restricted files.  
- Accounting → log trails are critical in incident response and forensics.  

---

## Gap Analysis
- **Definition:** Comparing current security posture vs desired state to find gaps.  
- **Example:**  
  - Policy: All servers must use MFA.  
  - Current: Only 50% of servers use MFA.  
  - Gap: Enforce MFA on remaining servers.  

**Home Lab Example:**  

| Control Requirement | Current State | Gap / Issue | Action Needed |
|------------------------------|--------------------------|------------------------|--------------------------|
| Multi-factor authentication | Only password login on VM| Missing MFA | Implement MFA (e.g. Duo) |
| Patch management | Manual updates monthly | No automation | Enable auto-updates |
| Log retention | 7 days | SOC requires 30 days | Increase retention |

**SOC Relevance:** Analysts often flag configuration weaknesses as part of incident reports, which helps management perform gap analysis.  

---

# ✅ Summary of Domain 1
So far, I’ve studied and documented:  
- Security Controls (types + functions)  
- CIA Triad  
- Non-repudiation  
- AAA framework  
- Gap Analysis  

Next up: Threat Actors and Attack Vectors (Domain 1.4).  

---
