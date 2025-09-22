# Domain 1 – General Security Concepts (SY0-701)

## 1.1 Security Controls
Security controls are methods used to protect information and systems.

- **Technical Controls** – implemented with technology  
  - Examples: Firewalls, IDS/IPS, encryption, authentication systems  
- **Administrative Controls** – policies and procedures  
  - Examples: Security training, background checks, change management policies  
- **Physical Controls** – protect physical assets  
  - Examples: Locks, fences, guards, CCTV  

**Control Functions**  
- **Preventive** – stop incidents before they happen (firewalls, MFA)  
- **Detective** – identify incidents in progress (IDS, SIEM monitoring)  
- **Corrective** – fix after an incident (patching, restoring backups)  
- **Deterrent** – discourage attackers (warning banners, guards)  
- **Compensating** – backup controls if the primary control fails  

---

## 1.2 CIA Triad
The three pillars of cybersecurity:

- **Confidentiality** – data is only accessible by authorized people (encryption, VPN, access controls)  
- **Integrity** – data cannot be modified without detection (hashing, digital signatures)  
- **Availability** – data/systems are accessible when needed (redundancy, backups, load balancing)  

---

## Non-Repudiation
Non-repudiation ensures that someone cannot deny an action they performed.

- Achieved with **digital signatures**, **hashing**, and **audit logs**.  
- Example: A user digitally signs an email → they cannot deny sending it later.  
- In a SOC, log analysis provides non-repudiation (proving an insider accessed files).  

---

## 1.3 AAA – Authentication, Authorization, and Accounting
- **Authentication** – verifying identity (username+password, biometrics, MFA)  
- **Authorization** – determining permissions (RBAC, ABAC, ACLs)  
- **Accounting (Auditing/Logging)** – tracking user actions (logins, file access, privilege use)  

**SOC Relevance:**  
- Authentication → alerts on failed login attempts  
- Authorization → escalation if users try to access restricted files  
- Accounting → logs used in forensic investigations  
