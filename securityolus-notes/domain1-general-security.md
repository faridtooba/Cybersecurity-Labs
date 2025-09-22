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
  - Gap: Enforce MFA on remaining servers
