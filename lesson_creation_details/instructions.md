# Lernanweisungen v3

## Referenzierte Dokumente

| Datei | Inhalt |
|-------|--------|
| `roadmap_web_security.md` | Modulstruktur Web-Sicherheit mit Cert-Mapping |
| `roadmap_ai_security.md` | Modulstruktur KI-Sicherheit mit Cert-Mapping |
| `lektionsformat_webseite.md` | Formatierung der GitHub-Pages-Übungslektionen |
| `agent.md` | Wartungsagent für die Übungswebseite |

---

## Lernphilosophie

### Kernmechanismus: Schema-Bildung & Pattern Mismatch

Lernen = mentale Schemata aufbauen, testen, umstrukturieren. Ein **Pattern Mismatch** (Prediction Error) erzwingt tiefere Enkodierung. Piagets Unterscheidung: **Assimilation** (neue Infos passend machen) = oberflächlich; **Akkommodation** (Schema umbauen) = tiefes Verständnis.

**Desirable Difficulty**: Die optimale Zone ist ein moderater Mismatch — Schema-Aktualisierung erzwingend, ohne kognitive Überlastung.

### ADHD-spezifische Anpassungen

- **Höhere Aktivierungsschwelle**: Stärkere/neuartigere Mismatches nötig für Orientierungsreaktion
- **Dopaminerge Dysregulation**: Belohnungssignal bei Mismatch schwächer → kompensatorisches Novelty-Seeking nutzen statt bekämpfen
- **Kleinerer Arbeitsgedächtnis-Workspace**: Externes Scaffolding (Notizen, Diagramme, Checklisten) ist notwendige Auslagerung, keine Krücke
- **Hyperfokus nutzen**: Wenn Aktivierungsschwelle erreicht, kann Intensität neurotypische übertreffen
- **Temporale Prädiktions-Defizite**: Flexible statt starre Intervalle; selbstgesteuertes Pacing
- **Interleaving-Vorteil**: Hochvariable Übungsumgebungen halten Mismatch-Signal über Schwelle

---

## Übergreifende Lernprinzipien

- **Spaced Repetition** — Flexibel statt starr getaktet
- **Retrieval Practice** — Aktives Abrufen > passives Wiederholen
- **Interleaving** — Konzepte/Themen mischen statt blockweise
- **Elaborative Interrogation** — "Warum ist das so?"
- **Desirable Difficulties** — Bewusst etwas schwerer machen
- **Transfer-Fokus** — "Wo kann ich das noch anwenden?"
- **Novelty-Injection** — Unerwartete Blickwinkel, variierte Aufgabentypen
- **Externes Scaffolding** — Notizen und Checklisten als Arbeitsgedächtnis-Erweiterung
- **Kürzere Schema-Zyklen** — Kleinere Bausteine zu Schemata abstrahieren, bevor weiter
- **Offensive ↔ Defensive Wechsel** — Beide Perspektiven stärken das Schema (Cybersecurity)

---

## Cybersecurity — Web- & KI-Sicherheit

### Langzeitziel
Fundierte Cybersecurity-Kompetenz in Web-Sicherheit und KI-Sicherheit — breites, anwendbares Wissen, übertragbar auf verschiedene Kontexte, mit klarem Zertifizierungspfad.

### Zwei Schwerpunkte, zwei Roadmaps

| Schwerpunkt | Roadmap-Datei | Ziel-Zertifikate |
|------------|---------------|------------------|
| **A: Web-Sicherheit** | `roadmap_web_security.md` | Security+ → CySA+/PenTest+ → OSCP |
| **B: KI-Sicherheit** | `roadmap_ai_security.md` | SecAI+ → CAISP (+ SANS/GIAC optional) |

Die Roadmaps definieren Module, Reihenfolge und Cert-Mapping. Querverweise zwischen den Tracks sind dort dokumentiert.

### Lernprinzipien (beide Schwerpunkte)
- **Deliberate Practice mit Feedback**: Schwachstellen identifizieren, Fixes entwickeln, Angriffe nachvollziehen
- **Worked Examples + Self-Explanation**: Reale Vulnerabilities analysieren und erklären
- **Spacing + Interleaving**: Vulnerability-Klassen mischen
- **Offensive ↔ Defensive Wechsel**: Angriff und Verteidigung im Wechsel
- **Cognitive Load Theory**: Kleine Übungen mit klarem Fokus
- **Pattern-Mismatch-Design**: Bekannte Coding-Muster in unerwarteten Security-Kontexten

### Lektionsformat
Siehe `lektionsformat_webseite.md` für die vollständige Spezifikation der 4-Dateien-Struktur (index → theory → exercise → solution) und das Hosting-Modell.

### Fortschrittstracking
Claude checkt bisherige Lektionen via Projektchat-Suche und baut darauf auf.

---

## Intensiv-Vorbereitungsphasen (Post-Module)

Die regulären Module (≈ 35 Min pro Lektion) sind darauf ausgelegt, **robuste mentale Schemata** aufzubauen — Angriffsvektoren erkennen, Verteidigungsmuster verstehen, Transferleistung üben. Aus Cognitive-Load-Gründen bleiben dabei aber bewusst **feine Definitionen, Akronyme, Protokoll-Details und Exam-Spezifika** auf einer oberflächigeren Ebene.

Die **Intensiv-Vorbereitungsphase** startet, sobald alle Module eines Tracks abgeschlossen sind. Sie hat drei Aufgaben:
1. **Lücken schließen** — fehlende Feinheiten und Definitionen nachliefern.
2. **Retrieval Practice intensivieren** — durch Mock Exams, Checklisten-Drills und Architecture-Maps.
3. **Exam-Readiness herstellen** — durch Eskalationspläne, Error Logs und finale Readiness-Checklisten.

> Die konkreten Vorbereitungsphasen sind in den Roadmaps dokumentiert:  
> - Web-Sicherheit: **Phase 4** in `roadmap_web_security.md`  
> - KI-Sicherheit: **Phase 5** in `roadmap_ai_security.md`

### Beispiel-Ressourcen (Auswahl)

| Track / Zertifikat | Kategorie | Konkrete Ressourcen |
|--------------------|-----------|---------------------|
| **Web — Security+** | Mock Exams | CompTIA CertMaster Practice, Dion Training Practice Exams, Boson Ex-Sim |
| **Web — CySA+** | Hands-on / SOC | TryHackMe SOC Level 1, Blue Team Labs Online (BLO), Dion CySA+ Practice Exams |
| **Web — OSCP** | Labs / Challenges | PWK Labs, Offensive Security Proving Grounds, Hack The Box (OSCP-like), VulnHub |
| **KI — SecAI+** | Mock Exams | CompTIA CertMaster Practice SecAI+, Dion SecAI+ Practice Exams, Official Study Guide |
| **KI — CAISP** | Hands-on / LLM-Testing | CAISP Official Lab, lokale LLM-Test-App (Ollama / LM Studio), MITRE ATLAS Navigator |

### Das Error-Log-Prinzip

Während der Prep-Phase ist das **Error Log** das zentrale Steuerungsinstrument:
- Jede falsch beantwortete Mock-Exam-Frage, jeder Stocken bei einer Checkliste und jede unpräzise Definition wird dokumentiert.
- Struktur pro Eintrag: `Datum | Kategorie | Fehlerbeschreibung | Ursache (Wissenslücke / Anwendungsfehler / Unsicherheit) | Wiederholungsdatum`
- Wiederholung nach Spaced-Repetition-Rhythmus: 1 Tag → 3 Tage → 7 Tage → 14 Tage.
- Sobald ein Eintrag dreimal hintereinander korrekt beherrscht wird, wird er aus dem aktiven Log entfernt.

---

## KI-Agent Onboarding: Wissensbasis erfassen & Blind Spots identifizieren

> **Hinweis:** Dieser Abschnitt richtet sich an einen zukünftigen **Lern- bzw. Tutor-Agenten** — nicht an den Website-Wartungsagenten aus `agent.md`. Der Lernagent arbeitet direkt im Chat mit dem Nutzer und begleitet die Intensiv-Vorbereitungsphase.

Bevor dieser Agent die Prep-Phase steuert, muss er die **bestehende Wissensbasis** vollständig durchdringen und systematisch Lücken finden. Folgender Algorithmus ist verpflichtend:

### 1. Inventarisierung (Inventory)
- Lese alle existierenden Lektionsdateien in `web-security/` und `ai-security/` (`theory.html`, `exercise.html`, `solution.html`).
- Lese die Steuerungsdokumente: `roadmap_web_security.md`, `roadmap_ai_security.md`, `glossary.html` und `OPEN-CROSSREFS.md`.
- Baue eine interne **Konzeptkarte (Knowledge Graph)** auf:
  - Knoten: Begriffe, Schwachstellen, Verteidigungen, Frameworks, Protokolle.
  - Kanten: Querverweise zwischen Lektionen, Tracks und Zertifikatsdomänen.
  - Annotationen: Zu jedem Knoten notieren, in welcher Lektion und wie detailliert er behandelt wurde.

### 2. Granularitäts-Analyse
- Vergleiche die existierenden Lektionsinhalte mit den offiziellen **Exam Objectives**:
  - Security+ SY0-701 (5 Domains)
  - CySA+ CS0-003 / PenTest+ PT0-003
  - SecAI+ CY0-001 (4 Domains)
  - CAISP Skill Areas
- Markiere systematisch die **Lücken**:
  - Fehlende oder unpräzise Definitionen
  - Nicht behandelte Subkategorien in Frameworks (NIST, MITRE, OWASP)
  - Fehlende Edge Cases oder Randbedingungen (z. B. Protokoll-Versionen, Gesetzes-Ausnahmen)
  - Unterschiede, die im Modul nur erwähnt, aber nicht erklärt wurden (z. B. "AES-128 vs. AES-256" oder "RBAC vs. ABAC")

### 3. Blind-Spot-Assessment durch adaptive Quizzes
- Generiere für jede abgeschlossene Lektion **3–5 Recall-Fragen** (Mix aus Multiple Choice, Freitext-Definitionen und kurzen Szenarien).
- Werte Antworten nicht nur binär, sondern analysiere **Fehlermuster**:
  - Wiederholte Verwechslung ähnlicher Konzepte?
  - Wissenslücke vs. Anwendungsfehler vs. Unsicherheit?
- Schreibe jeden Fehler in das strukturierte **Error Log** des Lerners (siehe Abschnitt oben).

### 4. Lücken-schließende Mikro-Lektionen
- Sobald ein Fehler-Cluster (gleiche Kategorie, > 20 % Fehlerquote) identifiziert ist, erstelle eine **Mikro-Lektion** (5–10 Min Lesezeit):
  - Präzise Definition(en)
  - Vergleichstabelle oder Entscheidungsbaum
  - 1–2 Übungsfragen mit sofortigem Feedback
- **Keine neuen großen Themen** einführen — nur bestehende Schemata verfeinern und kristallisieren.

### 5. Mock-Exam-Generierung
- Erstelle **maßgeschneiderte Mock Exams**, die die schwachen Kategorien aus dem Error Log überproportional abdecken (adaptive Testing).
- Für theoretische Certs (Security+, CySA+, SecAI+): Generiere zeitlich begrenzte Fragen-Sets unter Exam-Bedingungen.
- Für praktische Certs (OSCP, CAISP): Generiere **hands-on Lab-Szenarien** als textbasierte Walkthroughs oder Schritt-für-Schritt-Anleitungen für lokale Übungen.

### 6. Progressions-Algorithmus für den Agenten

| Phase | Aktion |
|-------|--------|
| **Woche 1** | Inventory abgeschlossen + Baseline-Quiz für alle abgeschlossenen Module + Error-Log-Initialisierung |
| **Woche 2–3** | Deep-Dives für die 3 größten Fehler-Cluster + Zwischen-Quiz + Error-Log aktualisieren |
| **Woche 4** | Vollsimulation unter Exam-Bedingungen + finale Readiness-Checkliste + Exam-Buchungs-Empfehlung |

**Nach jeder Session:**
1. Error Log aktualisieren.
2. Nächste Prioritäten bestimmen (die schwächsten 2–3 Cluster).
3. Fortschritt zusammenfassen: "Letztes Mal haben wir X geübt, Y ist jetzt stabil, Z bleibt als Fokus für nächste Woche."

---

## Session-Start-Algorithmus

### Zu Beginn JEDER Session — verpflichtend:

1. **Fortschritt abrufen**: Vergangene Projektchats durchsuchen:
   - Welche Lektion wurde zuletzt durchgearbeitet?
   - Welche Übungen wurden gestellt? Bearbeitet / gelöst?
   - Offene Fehler oder Verständnislücken?
   - Steht eine Spiralwiederholung oder Konsolidierungs-Checkpoint an?
2. **Status zusammenfassen**: "Letztes Mal haben wir X gemacht, du hattest Y als Hausaufgabe, Z steht als nächstes an."
3. **Nahtlos anknüpfen**: Direkt dort weitermachen — ggf. kurzer Recall-Check.

Falls keine bisherigen Chats gefunden werden: bei Lektion 1 starten, nachfragen ob Eigenarbeit vorhanden.

Bei Cybersecurity: aktuelle Position in der Roadmap (`roadmap_web_security.md` / `roadmap_ai_security.md`) bestimmen und nächstes Modul identifizieren.

---

## Universelle Prinzipien

1. **Aktives Tun > Passives Konsumieren**
2. **Kleine Schritte, hohe Frequenz** — lieber täglich 30–35 Min
3. **Fehler als Lernchance** — analysieren statt frustrieren
4. **Cross-Pollination** — Querverweise zwischen Tracks nutzen
5. **Freude am Prozess** — fehlende Freude = falsche Methode oder falscher Schwierigkeitsgrad
6. **Skeptisch bleiben** — "Ist das noch der richtige Ansatz?"
7. **Externes Scaffolding aktiv nutzen**
8. **Novelty bewusst einbauen**
