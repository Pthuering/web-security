# Roadmap: KI-Sicherheit

## Ziel-Zertifikate

### Primärer Pfad

| Zertifikat | Level | Kosten | Format | Status |
|------------|-------|--------|--------|--------|
| **CompTIA SecAI+ (CY0-001)** | Mittel | ~$425 | 60 Fragen, 60 Min, 600/900 | ✅ Live seit Feb 2026 |
| **CAISP (Certified AI Security Professional)** | Fortgeschritten, hands-on | ~$1.400 | 6h praktische Prüfung | ✅ Etabliert |

### Sekundär / Spezialisierung (optional, teuer)

| Zertifikat | Fokus | Kosten | Status |
|------------|-------|--------|--------|
| SANS SEC545 + GIAC Cert | GenAI/LLM App Security | ~$8.000+ | ⚡ Cert kommt 2026 |
| SANS SEC535 + GIAC Cert | Offensive AI | ~$8.000+ | ⚡ Cert kommt 2026 |
| EC-Council COASP | Offensive AI Red Teaming | ~$1.200 | ✅ Live |
| IAPP AIGP | AI Governance / Policy / Legal | ~$600 | ✅ Live |

### Rahmenwerke als Curriculum-Anker

| Framework | Herausgeber | Rolle im Curriculum |
|-----------|-------------|-------------------|
| **OWASP Top 10 for LLM Applications 2025** | OWASP | Zentrales Vulnerability-Framework — jede Kategorie = 1 Modul |
| **MITRE ATLAS** | MITRE | Adversarial Threat Landscape für AI — Angriffstechniken-Taxonomie |
| **NIST AI RMF 1.0** | NIST | Risk Management Framework — Map/Measure/Manage/Govern |
| **EU AI Act** | EU | Regulierung — Risikoklassen, Compliance-Anforderungen (Enforcement ab Aug 2026) |
| **ISO/IEC 42001** | ISO | AI Management System Standard |

---

## Phase 1: Fundamente (→ SecAI+ Domains 1 & 4)

SecAI+ Domänen: Basic AI Concepts (17%) | Securing AI Systems (40%) | AI for Security (24%) | AI GRC (19%)

| # | Modul | Cert-Mapping |
|---|-------|-------------|
| 1 | **AI/ML-Grundlagen für Security** — ML vs. DL vs. NLP, Transformer-Architektur, Training/Inference-Pipeline, Embeddings, Tokenization. Nur so viel Theorie wie nötig, um Angriffsflächen zu verstehen. | SecAI+ D1 (17%) |
| 2 | **LLM-Architektur & Datenflüsse** — Prompt → Model → Output Pipeline, RAG-Architektur, Vector Databases, Tool Use / Function Calling, Agent-Loops. Wo fließen Daten, wo entstehen Risiken? | SecAI+ D1 |
| 3 | **AI Threat Landscape & Frameworks** — MITRE ATLAS Überblick, OWASP LLM Top 10 als Landkarte, Threat-Actor-Motivationen, Abgrenzung zu klassischen Web-Threats | SecAI+ D1, CAISP |
| 4 | **AI Governance, Risk & Compliance** — NIST AI RMF (Map/Measure/Manage/Govern), EU AI Act Risikoklassen, ISO/IEC 42001, Responsible AI, Shadow AI | SecAI+ D4 (19%) |

---

## Phase 2: OWASP LLM Top 10 Deep Dive (→ SecAI+ Domain 2)

SecAI+ Domain 2 (Securing AI Systems) macht **40% der Prüfung** aus — hier liegt der Schwerpunkt.

### OWASP Top 10 for LLM Applications 2025

1. LLM01: Prompt Injection
2. LLM02: Sensitive Information Disclosure
3. LLM03: Supply Chain
4. LLM04: Data and Model Poisoning
5. LLM05: Improper Output Handling
6. LLM06: Excessive Agency
7. LLM07: System Prompt Leakage
8. LLM08: Vector and Embedding Weaknesses
9. LLM09: Misinformation
10. LLM10: Unbounded Consumption

### Module

| # | Modul | OWASP LLM | Querverweis Web-Track |
|---|-------|-----------|----------------------|
| 5 | **Prompt Injection** — Direkt vs. Indirekt, Jailbreaking, System Prompt Extraction; Defenses: Prompt Isolation, Input/Output Filtering, Instruction Hierarchy | LLM01 | ↔ XSS (Web 6) |
| 6 | **Sensitive Information Disclosure + System Prompt Leakage** — Training Data Extraction, PII Leakage, Prompt Leakage; Defenses: Data Sanitization, Output Filtering, Differential Privacy | LLM02 + LLM07 | ↔ Broken Auth (Web 8) |
| 7 | **Supply Chain Security** — Model Provenance, Poisoned Models (HuggingFace etc.), Dependency Risks, SBOM für AI, Model Signing | LLM03 | ↔ Supply Chain (Web) |
| 8 | **Data & Model Poisoning** — Training Data Manipulation, Backdoor Attacks, Fine-Tuning Risks; Defenses: Data Validation, Provenance Tracking | LLM04 | — |
| 9 | **Insecure Output Handling** — LLM-Output als Injection-Vektor in Downstream-Systeme, Output Encoding/Validation für LLM-Kontext | LLM05 | ↔ XSS + SQLi (Web 6–7) |
| 10 | **Excessive Agency** — Übermäßige Funktionalität/Permissions/Autonomie bei Agents, Least Privilege für Tools, Human-in-the-Loop | LLM06 | ↔ Access Control (Web 8) |
| 11 | **Vector & Embedding Weaknesses** — RAG Poisoning, Embedding Inversion, Vector DB Access Control, Similarity Manipulation | LLM08 | — (kein Web-Äquivalent) |
| 12 | **Misinformation & Unbounded Consumption** — Halluzination als Sicherheitsrisiko, Model DoS, Resource-Exhaustion, Rate Limiting für AI APIs | LLM09 + LLM10 | ↔ DoS / Rate Limiting (Web) |
| — | 🏁 **Konsolidierung: SecAI+ Mock-Prüfungsvorbereitung** | Alle Kategorien | |

---

## Phase 3: AI für Security Operations (→ SecAI+ Domain 3)

| # | Modul | Cert-Mapping |
|---|-------|-------------|
| 13 | **AI-gestützte Threat Detection** — Anomalie-Erkennung mit ML, Behavioral Analytics, AI in SIEM/SOAR, Detection-as-Code | SecAI+ D3 (24%) |
| 14 | **AI für Incident Response & Automation** — LLM-gestützte Triage, automatisierte Playbooks, AI-Agents in SOC-Workflows | SecAI+ D3 |
| 15 | **Secure AI Development Lifecycle (SAIDL)** — Security in ML-Pipelines, CI/CD für Modelle, Monitoring & Auditing in Produktion | SecAI+ D2 + D3 |

---

## Phase 4: Advanced & Emerging (→ CAISP / SANS / offenes Ende)

Diese Phase ist bewusst modular und offen. Module werden hinzugefügt oder aktualisiert, wenn sich Best Practices stabilisieren.

### Status-Legende
- ✅ **Etabliert** — Es gibt Frameworks, Tooling und dokumentierte Best Practices
- ⚡ **Sich entwickelnd** — Aktive Forschung, erste Tools und Methoden, aber noch keine Standardisierung
- 🔮 **Frontier** — Noch wenig Best Practices, primär Forschung und Exploration

| # | Modul | Status | Mapping |
|---|-------|--------|---------|
| 16 | **AI Red Teaming Hands-On** — Systematisches Testen von LLM-Anwendungen, Prompt Fuzzing, Jailbreak-Taxonomien, Red-Team-Reporting | ✅ | CAISP, COASP |
| 17 | **Agent Security & MCP** — Autonome Agenten absichern, Tool Use Risiken, MCP-Server Security, Sandbox-Strategien, Capability Control | ⚡ | — |
| 18 | **Adversarial ML Beyond LLMs** — Computer Vision Attacks, Evasion Attacks auf ML-Klassifikatoren, Gradient-basierte Angriffe (Konzepte) | ✅ | MITRE ATLAS |
| 19 | **AI-Powered Offensive Tools** — Deepfake Detection, AI-gesteuerte Phishing-Kampagnen, Polymorphic Malware via GenAI, Defensive Strategien | ⚡ | SecAI+ D1 |
| 20 | **Multi-Agent Systems Security** — Agent-zu-Agent Kommunikation, Trust Boundaries, Orchestration Security | 🔮 | — |
| 21 | **AI Supply Chain Deep Dive** — Model Cards, ML-BOMs, Container Security für ML, GPU-Infrastruktur-Sicherheit | ⚡ | CAISP |
| ?? | **[Platzhalter]** — Weitere Module nach Bedarf, z.B. Quantum-AI Security, AI in Critical Infrastructure, EU AI Act Enforcement Updates | 🔮 | — |

---

## Phase 5: Intensive Exam Preparation & Knowledge Consolidation

> **Trigger:** Alle Module (1–21+) abgeschlossen.  
> **Ziel:** Fehlende Definitionen nachliefern, Framework-Details verankern, praktische Prüfungsreadiness für SecAI+ und CAISP herstellen.

Die KI-Module bauen vor allem konzeptionelle Schemata (Angriffsvektoren, Verteidigungsarchitekturen, GRC-Rahmenwerke). Feinheiten wie exakte NIST-AI-RMF-Subkategorien, EU-AI-Act-Risikoklassen-Grenzfälle oder spezifische Jailbreak-Taxonomien wurden bewusst oberflächlich behandelt. Diese Phase schließt die Lücken gezielt.

---

### 5.1 Blind-Spot Assessment & Gap Analysis

- **Definitions-Map**: Jedes zentrale Fachwort aus NIST AI RMF, EU AI Act, ISO/IEC 42001, MITRE ATLAS und OWASP Top 10 for LLM Applications 2025 muss frei und präzise erklärt werden können.
- **Architecture-Drills**: RAG-Pipeline, Agent-Loop, Tool-Use-Ablauf und Prompt-Isolation-Mechanismen aus dem Kopf skizzieren und die jeweils 3–5 kritischsten Angriffsstellen benennen.
- **Framework-Details**: NIST AI RMF Funktionen (Map / Measure / Manage / Govern) und ihre Subkategorien, EU AI Act Risikoklassen (minimal / limited / high / unacceptable) mit konkreten Beispielen.
- **Error Log mit Kategorisierung**: Jeder Fehler wird einer Kategorie zugeordnet — GRC, Architektur, Angriffstechnik, Verteidigung — und nach einem Spaced-Repetition-Rhythmus (1 Tag, 3 Tage, 7 Tage) wiederholt.

---

### 5.2 Ziel-Zertifikat-spezifische Deep-Dives

| Zertifikat | Fokus der Prep-Phase | Beispiel-Ressourcen |
|------------|----------------------|---------------------|
| **SecAI+ CY0-001** | Domänen-Gewichtung (D2 *Securing AI Systems* = 40 %), Framework-Verankerung (OWASP LLM Top 10, NIST AI RMF), GRC-Details (AI Governance, Shadow AI, Responsible AI) | CompTIA CertMaster Practice SecAI+, Dion Training SecAI+ Practice Exams (Udemy), Official CompTIA SecAI+ Study Guide, OWASP LLM Top 10 2025 – Deep Dive |
| **CAISP** | 6h praktische Prüfung: Systematisches Testen von LLM-Apps, Prompt Injection, Jailbreaking, RAG Poisoning, Excessive Agency, Reporting | CAISP Official Lab Environment, PortSwigger Web Security Academy (indirekte Analogien zu Input-Validation / Injection), Lokale LLM-Test-App (Ollama / LM Studio) für hands-on Experimente, MITRE ATLAS Navigator für TTP-Mapping |

---

### 5.3 Mock-Exam-Rhythmus (4-Wochen-Plan)

| Woche | SecAI+ (theoretisch) | CAISP (hands-on) |
|-------|----------------------|------------------|
| **Woche 1** | 1× Vollsimulation unter Exam-Bedingungen (60 Min, 60 Fragen), Gap-Map aufbauen | 1× Assessment (2h): Prompt Injection (direkt + indirekt) + System Prompt Leakage |
| **Woche 2** | 2× Vollsimulation + Framework-Drill (NIST / EU AI Act), schwache Domänen repetieren | 1× Assessment (3h): RAG Poisoning + Vector DB Weaknesses + Excessive Agency |
| **Woche 3** | 3× Vollsimulation, nur noch die 2–3 schwächsten Domänen gezielt üben | 1× Assessment (4h): Full-Chain (Jailbreak → Tool Abuse / SSRF-Analogie → Data Exfiltration) |
| **Woche 4** | Finale Simulation, leichte Wiederholung häufigster Fehler, Exam-Buchung | 6h Prüfungs-Simulation unter Exam-Bedingungen inkl. Report-Schreiben |

---

### 5.4 Finale Readiness-Checkliste

- [ ] **OWASP LLM Top 10**: Alle 10 Kategorien + ihre primären Defenses frei und präzise erklärbar.
- [ ] **NIST AI RMF**: Die 4 Funktionen und mindestens 3 Subkategorien pro Funktion bekannt.
- [ ] **EU AI Act**: Risikoklassen korrekt zuordenbar, Compliance-Anforderungen für High-Risk-Systeme bekannt.
- [ ] **Mock-Exam-Score**: 80 % oder mehr in drei aufeinanderfolgenden Simulationen (SecAI+) bzw. 3/4 Labs erfolgreich (CAISP).
- [ ] **Hands-on CAISP**: Prompt Fuzzing, Jailbreak-Varianten und RAG-Manipulation können selbstständig durchgeführt und dokumentiert werden.
- [ ] **Logistik geklärt**: Testcenter / Online-Proctoring eingerichtet, ID gültig, Zeitzone bestätigt.

---

## Querverweise zum Web-Sicherheit-Track

| KI-Modul | Web-Modul | Verbindung |
|----------|-----------|------------|
| Prompt Injection (5) | XSS (Web 6) | User-Input wird zu Instruktion |
| Insecure Output Handling (9) | XSS + SQLi (Web 6–7) | Output wird zu Input eines Downstream-Systems |
| Supply Chain (7) | Vulnerability Mgmt (Web 11) | Vertrauen in Drittanbieter-Komponenten |
| Excessive Agency (10) | Broken Access Control (Web 8) | Least Privilege als universelles Prinzip |
| Data Poisoning (8) | SQL Injection (Web 7) | Datenintegrität manipulieren |
| AI Red Teaming (16) | Recon & Pentesting (Web 17, 23) | Methodische Angriffssimulation |
| Agent Security (17) | SSRF (Web 8) | Server-Side Calls aus User-Kontext |
| AI Incident Response (14) | Incident Response (Web 15) | Erkennung + Reaktion |
| Jailbreaking (5) | AV Evasion (Web 27) | Sicherheitsfilter umgehen |