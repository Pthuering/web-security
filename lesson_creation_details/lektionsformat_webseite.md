# Lektionsformat: Cybersecurity-Übungswebseite

## Überblick

Jede Cybersecurity-Lektion wird als Set von **4 HTML-Dateien** geliefert, die auf einer GitHub-Pages-Übungswebseite gehostet werden. Die Lektion findet primär auf der Webseite statt, nicht im Chat. Ein separater Agent (`agent.md`) pflegt die Webseite (Glossar, Querverweise, Landing Page etc.).

---

## Dateistruktur pro Lektion

```
lessons/
  {track}/          # web-security/ oder ai-security/
    {lesson-slug}/
      index.html    # Einstieg
      theory.html   # Theorie
      exercise.html # Rätsel
      solution.html # Lösung
```

---

## 1. Einstieg (index.html)

- Titel der Lektion
- Schwierigkeitsgrad (1–3)
- Zeitschätzung (~30 Minuten gesamt)
- Voraussetzungen (Links zu vorherigen Lektionen)
- Querverweise zu verwandten Lektionen im gleichen oder anderen Track (Web ↔ KI)
- Cert-Mapping: Welche Zertifikats-Domäne(n) diese Lektion abdeckt (siehe Roadmaps)

---

## 2. Theorie (theory.html)

### Spiral-Review (Anfang)
- 2–3 Recall-Fragen aus vorherigen Lektionen
- Klick-zum-Aufdecken Mechanismus
- Erzwingt Retrieval Practice vor neuem Material

### Konzept-Einführung
- Angriffsvektor / Verteidigungsmuster
- SVG-Diagramme für visuelle Erklärungen
- Codebeispiele mit Syntax-Highlighting
- Hervorhebungen für Notebook-Notizen

### Worked Example
- Kommentierter verwundbarer Code ODER dokumentierter Breach
- Offensive UND defensive Perspektive nebeneinander
- Erklärung warum das Muster gefährlich ist

### Zusammenfassung
- Kernbegriffe als kompakte Liste
- Begriffe gehen gleichzeitig ins zentrale Glossar

### Querverweise
- Explizite Links zu verwandten Lektionen (beide Tracks)

### Bewegungspause (Gate vor Exercise)
- Konkrete Körperübung (z.B. 10 Kniebeugen, Dehnung, kurzer Spaziergang)
- Fungiert als harter Übergang zwischen Theorie und Praxis
- Nicht optional — in die Seite eingebaut als visueller Blocker

---

## 3. Rätsel (exercise.html)

### Aufgabenstellung
- Klar formuliert im Kontext des gelernten Themas

### Hinweissystem (3 Stufen)
- Per Klick enthüllbar
- Hinweis 1: Breit — richtet die Aufmerksamkeit
- Hinweis 2: Konkreter — nennt die relevante Technik
- Hinweis 3: Fast die Lösung — beschreibt den Lösungsweg, ohne das Ergebnis zu verraten

### Verwundbare Komponente
- **Web-Security-Track:** Verwundbare Webseite/Formular/Komponente mit verstecktem Passwort
- **KI-Security-Track:** Verwundbarer Chatbot / Prompt-Interface / simulierte LLM-App mit verstecktem Geheimnis
- Das Passwort/Geheimnis ist **nur durch Anwendung der gelernten Technik** auffindbar

### Passwort-Eingabe
- Eingabefeld zur Lektionsabschluss-Bestätigung
- Visuelles Feedback bei korrekter/falscher Eingabe

### Design-Prinzip: Desirable Difficulty
- Lösbar mit Theorie + Hinweisen
- Erzwingt Schema-Aktualisierung (nicht einfach Copy-Paste aus der Theorie)
- Moderate Schwierigkeit — nicht trivial, nicht frustrierend

---

## 4. Lösung (solution.html)

### Schritt-für-Schritt-Lösungsweg
- Jeder Schritt nachvollziehbar dokumentiert
- Screenshots/Codeblöcke wo nötig

### Erklärung
- Warum die Schwachstelle existiert
- Gefixte Version zum Vergleich (vorher/nachher)

### Reflexions-Prompt
- "Was war der schwierigste Schritt?"
- "Wo hast du zuerst falsch gedacht?"

### Transfer-Frage
- "Wo könnte dir dieses Wissen in einem eigenen Projekt begegnen?"
- "Welche verwandte Schwachstelle im anderen Track funktioniert nach demselben Prinzip?"

---

## Hosting-Phasen

| Phase | Module | Hosting | Technologie |
|-------|--------|---------|-------------|
| Phase 1–2 | Web 1–21, KI 1–15 | GitHub Pages | Rein clientseitig (HTML/CSS/JS) |
| Phase 3 | Web 22+ | Lokal | Node.js/Express + SQLite |

Das Backend-Setup (Web-Modul 22) wird als eigene Übergangslektion eingeführt, die gleichzeitig als Lerninhalt dient (Server aufsetzen = Security-Relevanz verstehen).

---

## Wartung & Pflege

Folgende Elemente werden vom `agent.md`-Agenten gepflegt:

- **Zentrales Glossar**: Begriffe aus allen Lektionen, alphabetisch, mit Links zurück zur Lektion
- **Landing Page**: Übersicht aller verfügbaren Lektionen, nach Track und Phase sortiert
- **Querverweise**: Cross-Links zwischen Web- und KI-Track-Lektionen
- **Fortschritts-Visualisierung**: Welche Lektionen abgeschlossen sind (clientseitig, localStorage)