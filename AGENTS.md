# Arbeitsanweisungen für Codex – Vertriebs-Datenbank

## Mission
Entwickle aus diesem Repository eine **webbasierte qualitative Firmenkundenprofil-Datenbank für Volks- und Raiffeisenbanken**. Die Anwendung soll öffentlich zugängliche Informationen recherchieren, fachlich strukturieren, belegen, prüfen, zusammenfassen und zwischen Banken vergleichen. **Pilotbank: Hamburger Volksbank eG.** Sprache der Oberfläche und Inhalte: Deutsch.

Lies vor Änderungen `docs/PRODUKTANFORDERUNGEN.md` und `docs/CODEX_START.md`.

## Verbindliche fachliche Leitplanken
- Ausschließlich **qualitative öffentlich zugängliche** Informationen; keine interne Datenanbindung.
- Themenbereiche: (1) allgemeines Bankprofil, (2) Firmenkundenstrategie, (3) Zielgruppen/Kundensegmente, (4) Kreditgeschäft/Finanzierungsschwerpunkte, (5) Zahlungsverkehr/Cash Management, (6) Vertrieb/Marktpositionierung, (7) strategische Entwicklungen.
- **Explizit ausgeschlossen:** quantitative Finanz- und Vertriebskennzahlen, Bilanz- und Kreditvolumen, KPI-Grafiken, interne Prozessinformationen, BWS/BAP/agree21, Risikorelevanzgrenze, Kreditkompetenzen, Automatisierungsgrade, Prozess- und Effizienzbewertungen, Reifegrad-/Ranking-Scores.
- Eine beworbene Leistung ist **kein** Nachweis für ihren Einsatz oder für einen strategischen Schwerpunkt. `nicht gefunden` bedeutet **nicht** `nicht vorhanden`.
- Unterscheide strikt **belegte Tatsache**, **Selbstaussage der Bank** und **Interpretation/Hypothese**. Interpretationen nicht zu Fakten erheben.
- Jede veröffentlichte Profilbehauptung braucht mindestens eine nachvollziehbare Quelle, URL und möglichst Fundstelle/Seite. KI-Extraktionen zuerst als *prüfung erforderlich*, nicht als verifiziert speichern.
- Keine erfundenen Rechercheergebnisse. Demo- und Testdaten immer klar kennzeichnen.

## Bestehender Code
Das Repository enthält auf `main` eine umfangreiche statische `index.html`-Pilotoberfläche zu Hamburger Volksbank, die derzeit auch numerische KPI-Elemente enthält. Bewahre diesen Stand über Git-Historie und Branching. Nutze ihn als visuelle / inhaltliche Referenz, **übernimm die quantitativen Bestandteile aber ausdrücklich nicht** in die Zielanwendung. Migriere schrittweise, ohne bestehende Dateien ohne Grund zu zerstören.

## Implementierung
- Priorität: robustes, lokal ausführbares **MVP**, kein rein visuelles Mockup.
- Bevorzugt: Next.js/React/TypeScript/Tailwind für Frontend; Python/FastAPI/SQLAlchemy/Alembic für Backend; SQLite lokal, PostgreSQL-kompatibles Schema. Prüfe vorher den Ist-Zustand und begründe Abweichungen.
- Entitäten mindestens: Bank, Source, QualitativeFinding, FindingEvidence, BankSummary, ResearchJob, ReviewHistory.
- Recherche aus erlaubten öffentlichen HTML-Seiten/PDFs und manuell hinterlegten URLs; optionale Websuche/LLM via ENV-Konfiguration. Ohne API-Schlüssel müssen manuelle Quellenverwaltung, Profilansicht und Review funktionieren.
- Quellen: Titel, Herausgeber, URL, Veröffentlichungsdatum, Abrufdatum, Inhaltshash, Belegauszug, Seiten-/Abschnittsfundstelle, Prüfstatus.
- Qualität: deduplizieren, versionieren, widersprüchliche Angaben markieren; fehlgeschlagene Quellenabrufe nicht als Löschgrund behandeln.
- Sicherheitsstandards: SSRF-Schutz, URL-Allowlisting/Validierung, Timeouts, Größen- und Download-Limits; `robots.txt`/Nutzungsbedingungen beachten; keine Paywalls oder Zugriffssperren umgehen; Keys nur serverseitig.
- Benutzeroberfläche: Bankenliste mit Filtern, einzelne Bankprofile mit sieben Tabs, Management Summary (150–250 Wörter nur bei belastbarer Evidenz), Quelleninspektor, Review-Workflow, Entwicklungstimeline, qualitativer Vergleich für 2–4 Banken.
- Keine funktionlosen Buttons. Klare Leer-, Lade- und Fehlerzustände.

## Arbeitsweise
1. Repository inspizieren und Bestandsaufnahme dokumentieren.
2. Kleines umsetzbares Phasen-/Dateikonzept entwickeln, dann implementieren.
3. Funktionierenden End-to-End-MVP priorisieren: Bank anlegen → Quelle hinzufügen → Aussage extrahieren/manuell erfassen → prüfen → Profil anzeigen → mit Quellenbeleg öffnen.
4. Pilotbank mit tatsächlich verifizierten öffentlichen Quellen erfassen; Netz-/API-Ausfall als Limitierung ausweisen.
5. Tests für Datenmodell, Quellenbelegpflicht, Statuslogik, Deduplizierung, fehlende Informationen, URL-Sicherheit und kritische UI-Flows.
6. README, `.env.example`, Migrations- und Startanweisungen vollständig halten.

## Abnahmekriterien
- Mehrere Banken ohne Umbaumaßnahmen verwaltbar.
- Nachweisbar belegte qualitative Firmenkundenprofile.
- Keine numerischen KPI-Cards oder interne Prozessanalysen in der Ziel-UI.
- Anzeige ohne API-Keys benutzbar; Recherchefunktionen degradieren transparent.
- Hamburger Volksbank als Pilotbank angelegt, ohne unbelegte Fakten zu behaupten.
- Tests/Build ausgeführt und deren Ergebnis dokumentiert.
