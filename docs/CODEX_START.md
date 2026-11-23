# Codex-Auftrag: Vertriebs-Datenbank umsetzen

## Kontext
Dieses Repository gehört zur Entwicklung einer webbasierten **qualitativen externen Vertriebs-Datenbank für das Firmenkundengeschäft von Volks- und Raiffeisenbanken**. Die fachlichen Anforderungen sind in `docs/PRODUKTANFORDERUNGEN.md`, die Agentenregeln in `AGENTS.md` festgehalten.

Der Nutzer möchte **eine lauffähige Anwendung**, kein Konzeptdokument und keine fiktive Demonstration. Erste Pilotbank: Hamburger Volksbank eG.

## Wichtige aktuelle Erkenntnis
`index.html` auf `main` ist eine bestehende statische Prototypseite mit quantitativen Kennzahlen. Diese wurde **vor** der fachlichen Fokussierung erstellt. Sie ist kein Modell für die Zielinhalte. Für das neue Produkt gilt ausnahmslos: **nur qualitative öffentlich belegte Firmenkundendaten, keine Prozess- und Finanz-KPIs**.

## Arbeitspaket
1. Inspiziere das Repository und seine vorhandenen Funktionen; fasse kurz zusammen, was wiederverwendet werden kann.
2. Implementiere auf dieser Entwicklungsbranch ein lokal startbares MVP mit persistierter Banken-/Quellen-/Aussagenverwaltung und moderner, deutscher Dashboard-Oberfläche.
3. Baue das Bankprofil in genau sieben Kategorien: Bankprofil, Firmenkundenstrategie, Zielgruppen, Finanzierungsschwerpunkte, Zahlungsverkehr/Cash Management, Vertrieb/Marktpositionierung, strategische Entwicklungen.
4. Erstelle eine Quellenverwaltung mit URL/PDF-Upload, Belegstellen und manueller Verifikations-/Freigabefunktion.
5. Implementiere eine zulässige HTML-/PDF-Einlesefunktion. Bereite optionale KI-Extraktion per API-Schlüssel vor; verwende strukturierte Ausgaben und setze extrahierte Erkenntnisse standardmäßig auf `Prüfung erforderlich`.
6. Füge die Hamburger Volksbank als Bankstammdatensatz hinzu, recherchiere belegbare qualitative Aspekte nur mit tatsächlich abgerufenen Quellen.
7. Implementiere die quellenbasierte Management Summary, eine qualitative Vergleichsansicht für zwei bis vier Banken sowie eine Timeline dokumentierter strategischer Entwicklungen.
8. Sorge für sinnvolle Tests und Start-/Build-Checks; erstelle README und `.env.example`.

## Technische Präferenzen
Next.js/React/TypeScript/Tailwind + Python/FastAPI + SQLAlchemy/Alembic + SQLite für lokal. Passe an den Ist-Zustand an, wenn eine andere wartbare Lösung deutlich effizienter ist. Dokumentiere Architekturentscheidungen.

## Kritische Abnahmebedingungen
- Funktionierende Interaktionen statt Fake-Buttons.
- Niemals unbelegte Inhalte als verifizierte Bankinformationen darstellen.
- Produkte nicht als strategische Prioritäten ausgeben, sofern das nicht explizit belegt ist.
- Keine Rückschlüsse auf die interne Technik/Prozesslage der Banken.
- Die App funktioniert ohne externe KI-API mindestens für Bank-, Quellen- und Profilverwaltung.
- Keine KPI-/Bilanzdiagramme oder Zahlenrankings.
- Vorhandener Stand bleibt über Git erhalten; entwickle inkrementell.

## Erste Schritte
Beginne mit `AGENTS.md` und `docs/PRODUKTANFORDERUNGEN.md`. Prüfe die `index.html`; lege anschließend das neue Projektgerüst an und implementiere das Kernfeature Ende-zu-Ende. Dokumentiere am Ende die tatsächlich ausgeführten Befehle, Testergebnisse, offenen Limitierungen und die nächsten sinnvollen Schritte.
