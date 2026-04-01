# Roadmap: Web-Sicherheit

## Ziel-Zertifikate (in Reihenfolge)

| Zertifikat | Level | Kosten | Format | Empfohlene Erfahrung |
|------------|-------|--------|--------|---------------------|
| **CompTIA Security+ (SY0-701)** | Einstieg | ~$400 | 90 Fragen, 90 Min, 750/900 | 2 Jahre IT + Network+ |
| **CompTIA CySA+ (CS0-003)** | Mittel, defensiv | ~$400 | 85 Fragen, 165 Min | Security+ + 2 Jahre |
| **CompTIA PenTest+ (PT0-003)** | Mittel, offensiv | ~$400 | 90 Fragen, 165 Min | 3–4 Jahre Pentest |
| **OSCP+ (PEN-200)** | Fortgeschritten, hands-on | ~$1.600+ | 24h praktische Prüfung + Report | Networking, Scripting, Linux/Windows Admin |
| *CISSP (optional, langfristig)* | *Senior/Leadership* | *~$750* | *100–150 Fragen, 3h* | *5 Jahre Berufserfahrung* |

---

## Phase 1: Fundamente (→ CompTIA Security+ SY0-701)

Security+ Domänen: General Security Concepts (12%) | Threats/Vulns/Mitigations (22%) | Security Architecture (18%) | Security Operations (28%) | Program Management (20%)

| # | Modul | Cert-Mapping (SY0-701 Domain) |
|---|-------|-------------------------------|
| 1 | **CIA-Triad, Security Controls & Grundkonzepte** — Vertraulichkeit, Integrität, Verfügbarkeit; technische vs. administrative vs. physische Controls | Domain 1 (12%) |
| 2 | **Kryptografie-Grundlagen** — Symmetrisch/Asymmetrisch, Hashing, digitale Signaturen, Zertifikate, TLS-Handshake | Domain 1 |
| 3 | **Threat Actors & Attack Surfaces** — Motivationen, APTs, Insider, Attack Surface Mapping, Threat Intelligence Basics | Domain 2 (22%) |
| 4 | **Netzwerk-Sicherheit Basics** — TCP/IP-Security, Firewalls, VPNs, Segmentierung, Secure Protocols | Domain 3 (18%) |
| 5 | **Identity & Access Management** — Authentifizierung vs. Autorisierung, MFA, SSO, RBAC/ABAC, Federation | Domain 3 |
| 6 | **Web-Schwachstellen I: XSS (Reflected, Stored, DOM)** — Angriff + Verteidigung, Output Encoding, CSP | Domain 2 |
| 7 | **Web-Schwachstellen II: SQL Injection** — Union, Error-based, Blind; Parameterized Queries, ORM-Safety | Domain 2 |
| 8 | **Web-Schwachstellen III: CSRF, SSRF, Broken Auth** — Token-basierte Defenses, Session Management, Secure Headers | Domain 2 |
| 9 | **Secure Architecture & Hardening** — Defense in Depth, Zero Trust, Secure Baselines, Cloud Models (IaaS/PaaS/SaaS) | Domain 3 |
| 10 | **Security Operations Basics** — Logging, Monitoring, SIEM-Konzepte, Incident Response Lifecycle, Alerting | Domain 4 (28%) |
| 11 | **Vulnerability Management** — Scanning (Nessus-Konzepte), CVE/CVSS, Patch Management, Risk Assessment | Domain 4 |
| 12 | **Governance, Risk & Compliance** — Frameworks (NIST, ISO 27001), Policies, Risk Register, Compliance, Audits | Domain 5 (20%) |
| — | 🏁 **Konsolidierung: Security+ Standortbestimmung** | Alle Domains |

---

## Phase 2: Spezialisierung Defensiv + Offensiv (→ CySA+ / PenTest+)

CySA+ Domänen: Threat Management | Vulnerability Management | Incident Response | Compliance
PenTest+ Domänen: Engagement Management (13%) | Recon & Enumeration (21%) | Vulnerability Discovery (17%) | Attacks & Exploits (35%) | Post-Exploitation (14%)

| # | Modul | Cert-Mapping |
|---|-------|-------------|
| 13 | **Threat Intelligence & Hunting** — IoCs, Threat Feeds, MITRE ATT&CK, proaktive Suche in Logs | CySA+ |
| 14 | **SIEM Deep Dive & Log Analysis** — Korrelation, Detection Rules, Anomalie-Erkennung, ELK/Splunk-Konzepte | CySA+ |
| 15 | **Incident Response & Forensics Basics** — IR-Playbooks, Evidence Handling, Chain of Custody, Recovery | CySA+ |
| 16 | **Engagement Planning & Scoping** — Rules of Engagement, Legal/Compliance, Scoping, Reporting-Struktur | PenTest+ D1 (13%) |
| 17 | **Reconnaissance & Enumeration** — Passive OSINT, Active Scanning (Nmap), DNS/SMB/SNMP Enumeration | PenTest+ D2 (21%) |
| 18 | **Vulnerability Discovery & Analysis** — Vulnerability Scanner, Ergebnis-Analyse, False Positives, Priorisierung | PenTest+ D3 (17%) |
| 19 | **Web Application Attacks (Advanced)** — Directory Traversal, File Inclusion (LFI/RFI), File Upload Vulns, Command Injection | PenTest+ D4 (35%) |
| 20 | **Authentication Attacks & Password Cracking** — Brute Force, Credential Stuffing, Hash Cracking, Password Spraying | PenTest+ D4 |
| 21 | **Post-Exploitation & Lateral Movement** — Privilege Escalation Konzepte, Persistence, Pivoting-Theorie, Reporting | PenTest+ D5 (14%) |
| — | 🏁 **Konsolidierung: CySA+ / PenTest+ Standortbestimmung** | Alle Domains |

---

## Phase 3: Hands-On Offensive (→ OSCP PEN-200)

Ab hier: lokales Backend (Node.js/Express + SQLite). Das Backend-Setup ist die Brückenlektion.

PEN-200 Module: Information Gathering | Web Applications | SQL Injection | Client-Side | Exploit Location | AV Evasion | Password Attacks | Windows/Linux PrivEsc | Tunneling | Metasploit | Active Directory

| # | Modul | Cert-Mapping (PEN-200) |
|---|-------|----------------------|
| 22 | 🔧 **Backend-Setup-Lektion** — Node.js/Express/SQLite, lokale Lab-Umgebung einrichten | Infrastruktur |
| 23 | **Information Gathering Hands-On** — Nmap Deep Dive, Service Enumeration, Scripting für Automation | Information Gathering |
| 24 | **Web App Pentesting Hands-On** — Burp Suite, OWASP Testing Guide, manuelle Exploitation | Web Applications |
| 25 | **SQL Injection Hands-On** — Manual SQLi (Union/Error/Blind), SQLmap, Code Execution via DB | SQL Injection |
| 26 | **Client-Side Attacks** — Office Macros, Library Files, Social Engineering Vektoren | Client-Side |
| 27 | **Antivirus Evasion** — Detection Engines, manuelle Evasion, Payload-Obfuscation | AV Evasion |
| 28 | **Linux Privilege Escalation** — SUID, Cron Abuse, Kernel Exploits, Credential Harvesting | Linux PrivEsc |
| 29 | **Windows Privilege Escalation** — Service Hijacking, DLL Hijacking, Unquoted Paths, Token Abuse | Windows PrivEsc |
| 30 | **Port Forwarding & Tunneling** — SSH Tunneling, Chisel, DNS Tunneling, Pivoting | Tunneling |
| 31 | **Active Directory Enumeration & Angriffe** — BloodHound, Kerberoasting, Pass-the-Hash, DCSync | Active Directory |
| 32 | **AD Lateral Movement & Persistence** — WMI, PsExec, Golden Tickets, Shadow Copies | AD Persistence |
| 33 | **Assembling the Pieces** — Full-Chain Pentest Simulation: Recon → Foothold → PrivEsc → Lateral → Domain Compromise | Capstone |
| — | 🏁 **OSCP-Readiness: Challenge Lab Simulation** | Prüfungsvorbereitung |

---

## Phase 4: Intensive Exam Preparation & Knowledge Consolidation

> **Trigger:** Alle Module (1–33) abgeschlossen.  
> **Ziel:** Fehlende Granularität nachliefern, Definitionen verankern, Exam-Readiness herstellen.

Die Module in den Phasen 1–3 haben robuste mentale Schemata gebaut. Sie haben aber aus Platz- und Cognitive-Load-Gründen nicht jedes Akronyon, jede Protokoll-Detailtiefe oder jeden Randfall abdecken können. Diese Phase schließt die Lücken systematisch, **bevor** die Prüfung gebucht wird.

---

### 4.1 Blind-Spot Assessment & Gap Analysis

- **Definitions-Drill**: Systematischer Durchlauf aller Module mit Fokus auf feine Unterschiede (z. B. AES-128 vs. AES-256, symmetrisch vs. asymmetrisch, RBAC vs. ABAC, XSS-Typ-Unterscheidung).
- **Protokoll- & Port-Listen**: TCP/UDP-Ports, Secure-Protokoll-Details (TLS-Versionen, Cipher-Suites), Hashing-Algorithmen auswendig reproduzieren.
- **Checklisten aus dem Kopf**: Windows/Linux PrivEsc-Checklisten, Nmap-Scan-Parameter, OWASP Testing Guide-Schritte.
- **Error Log führen**: Jede falsch beantwortete Recall-Frage oder jeder Stocker wird dokumentiert (Kategorie, Ursache, Wiederholungsdatum). Im zweiten Durchlauf werden nur noch Error-Log-Einträge wiederholt.

---

### 4.2 Ziel-Zertifikat-spezifische Deep-Dives

| Zertifikat | Fokus der Prep-Phase | Beispiel-Ressourcen |
|------------|----------------------|---------------------|
| **Security+ SY0-701** | 1.200+ Begriffe, Protokoll-Details, GRC-Framework-Vergleiche (NIST vs. ISO 27001), Incident Response Reihenfolge | CompTIA CertMaster Practice SY0-701, Dion Training Practice Exams (Udemy), Professor Messer Study Groups, Boson Ex-Sim SY0-701 |
| **CySA+ CS0-003** | SIEM-Log-Analyse (Splunk/ELK), Threat Hunting Queries, IR-Playbook-Schritte, Compliance-Mapping | Dion CySA+ Practice Exams, CertMaster Practice CS0-003, TryHackMe SOC Level 1 Path, Blue Team Labs Online (BLO) |
| **PenTest+ PT0-003** | Scoping-Berechnungen, Legal/Compliance-Fragen, Exploit-Selektion, Report-Schreibstruktur, Scripting-Output-Analyse | Dion PenTest+ Practice Exams, Hack The Box CPTS-ähnliche Module, CompTIA CertMaster Practice PT0-003 |
| **OSCP PEN-200** | 24h-Exam-Simulation, Active Directory Kill Chain, Buffer Overflow-Schritt-für-Schritt, Report-Qualität | PWK Labs (90 Tage), Offensive Security Proving Grounds (PG Practice), Hack The Box OSCP-like machines, VulnHub VMs |

---

### 4.3 Mock-Exam-Rhythmus (4-Wochen-Plan)

| Woche | Security+ / CySA+ / PenTest+ | OSCP |
|-------|------------------------------|------|
| **Woche 1** | 1× Vollsimulation unter Exam-Bedingungen (zeitlich begrenzt), Error-Log aufbauen, schwache Domänen identifizieren | 1× "Journey"-Lab (leicht/mittel), Checklisten optimieren, Buffer-Overflow-Template repetieren |
| **Woche 2** | 2× Vollsimulation + detailliertes Review, Cluster mit >20% Fehlerquote wiederholen | 1× "Proof"-Lab (mittel), AD-Enumeration-Chain üben, lokale PrivEsc-Repetition |
| **Woche 3** | 3× Vollsimulation, Fokus nur noch auf verbleibende Schwachstellen-Cluster | 1× "Trailblazer"-Lab (schwer), Full-Chain von Recon bis Domain Compromise |
| **Woche 4** | 1× finale Simulation, leichte Wiederholung der häufigsten Fehler, Exam-Buchung | 24h Challenge-Lab-Simulation (PG Practice / HTB), Report-Schreiben unter Zeitdruck |

---

### 4.4 Finale Readiness-Checkliste

- [ ] **Error Log abgearbeitet**: Alle dokumentierten Fehler wurden mindestens einmal korrekt wiedergeholt.
- [ ] **Mock-Exam-Score**: 80 % oder mehr in drei aufeinanderfolgenden Simulationen (theoretische Certs) bzw. 3/4 Labs erfolgreich ohne Hinweise (OSCP).
- [ ] **Checklisten auswendig**: Kritische Prozeduren (Nmap, PrivEsc, IR-Lifecycle, OWASP-Test-Schritte) können frei reproduziert werden.
- [ ] **Hands-on Tools**: Für OSCP: Burp Suite, Nmap, Sqlmap, BloodHound, Impacket-Tools sind Routine.
- [ ] **Logistik geklärt**: Pearson VUE / Proctoring eingerichtet, ID gültig, Zeitzone bestätigt.

---

## Querverweise zum KI-Sicherheit-Track

| Web-Modul | KI-Modul | Verbindung |
|-----------|----------|------------|
| XSS (6) | Prompt Injection (5) | User-Input wird zu Instruktion |
| SQL Injection (7) | Data Poisoning (8) | Datenintegrität manipulieren |
| CSRF/SSRF (8) | Excessive Agency (10) / Agent Security (17) | Server-Side Calls aus User-Kontext |
| Input Validation (8) | Insecure Output Handling (9) | Output wird zu Input eines Downstream-Systems |
| Vulnerability Management (11) | Supply Chain (7) | Vertrauen in Drittanbieter-Komponenten |
| Recon & Pentesting (17, 23) | AI Red Teaming (16) | Methodische Angriffssimulation |
| AV Evasion (27) | Jailbreaking & Prompt Obfuscation (5) | Sicherheitsfilter umgehen |
| Incident Response (15) | AI Incident Response (14) | Erkennung + Reaktion auf Angriffe |