# Produktanforderungen – Qualitative Vertriebs-Datenbank

**Fachlicher Ausgangspunkt:** Eine Beratungsorganisation benötigt ein externes Research-Werkzeug, um das Firmenkundengeschäft deutscher Volks- und Raiffeisenbanken anhand **öffentlicher qualitativer Informationen** zu verstehen. Kein KPI-Dashboard, kein internes Bankenanalysetool.

## 1. Ziel und Nutzerwert
- Bank vor Kundenbesuch in wenigen Minuten verstehen.
- Firmenkundenstrategie, Zielgruppen, Schwerpunkte, Positionierung und Besonderheiten fundiert zusammenführen.
- Auf Faktenbasis verschiedene Genossenschaftsbanken vergleichen und strategische Entwicklungen beobachten.
- Alle Aussagen im Profil zu Originalquellen zurückverfolgen.
- Bereitstellung einer kompakten, professionellen **Management Summary** als Gesprächsvorbereitung.
- **Keine** Behauptung tatsächlicher Beratungsbedarfe oder interner Schwachstellen aus öffentlichen Indizien.

## 2. Die sieben Profilbereiche
### 2.1 Allgemeines Bankprofil
Vollständiger Name, Rechtsform, Hauptsitz, Geschäftsgebiet, Unternehmensstruktur soweit veröffentlicht, Vorstand/Ressortverteilung, öffentlich dokumentierte Fusionen und Kooperationen, geografische Marktpositionierung, besondere Identitätsmerkmale.

### 2.2 Firmenkundenstrategie
Öffentlich kommunizierte strategische Ausrichtung, Wachstumsfelder, Schwerpunktsetzungen, regionale/überregionale Ziele, Positionierung im Mittelstandsgeschäft, Bedeutung des Firmenkundengeschäfts, längerfristige Vorhaben. Aussagen der Bank als Selbstaussagen markieren.

### 2.3 Zielgruppen und Kundensegmente
Explizit angesprochene Segmente, z. B. Mittelstand, Gewerbe, Selbstständige, Freiberufler, Existenzgründer, Handwerk, Industrie, Landwirtschaft, Immobilienunternehmen, öffentliche/institutionelle Kunden. **Unterscheide** allgemeine Zielgruppenwerbung und ausdrücklich priorisierte Zielgruppen. Keine internen Umsatz-/Obligogrenzen.

### 2.4 Kreditgeschäft und Finanzierungsschwerpunkte
Öffentliche Finanzierungsausrichtung: Betriebsmittel, Investition, Immobilien, Projekt, Gründung, Wachstum, Nachfolge, Fördermittel, Spezialfinanzierung, Verbundlösungen. Unterscheide Angebot von strategisch hervorgehobenem Geschäftsfeld. Keine Kreditvolumina, interne Kompetenzen oder Prozessdetails.

### 2.5 Zahlungsverkehr und Cash Management
Qualitativ angebotenes Portfolio: Geschäftskontomodelle, nationales/internationales Payment, Cash- und Liquiditätsmanagement, elektronische Bankingsoftware, Terminals, Acquiring, E-Commerce, Kooperationen/Verbundpartner. Keine Transaktionszahlen, Nutzungsquoten oder Bewertung der operativen Zahlungsverkehrsprozesse.

### 2.6 Vertrieb und Marktpositionierung
Hausbank-/Kundenbindungsmodelle, genossenschaftlicher Beratungsansatz, Unternehmer-/Gründungs-/Nachfolgeberatung, Spezialistenleistungen, FinanzGruppe-/Verbundpartner-Einbindung, regionales Leistungsversprechen, erkennbares Differenzierungsmerkmal. Keine Vertriebs-KPIs oder vertriebsinternen Abläufe.

### 2.7 Strategische Entwicklungen
Datiert dokumentierte Fusionen, Kooperationen, neue Geschäftsfelder, neue Zielgruppen, geschäftspolitische Schwerpunktänderungen, Nachhaltigkeits-/ESG-/Transformationsausrichtung, Vorstand/Ressortänderungen, Unternehmenspublikationen und relevante Firmenkundeninitiativen. Chronologische Timeline.

## 3. Verbindlich ausgeschlossen
Bilanzsumme, CIR, Erträge, Forderungs-/Einlagenvolumen, Kundenzahlen als KPI, Größenklassen-/Renditerankings, Finanzdashboard, interne BWS/BAP/agree21-Verfahren, Kreditrisikorelevanz- und Offenlegungsgrenzen, Kompetenzstufen, Prozesskosten/-dauer, Automatisierung, Customer-Journey-Bewertung, digitale Reifegradscores. Ein veröffentlichtes Online-Produkt ist kein Nachweis intern eingesetzter Systeme.

## 4. Qualitäts- und Evidenzmodell
Jede Information: `bank_id, category, subcategory, title, narrative, tags, statement_type, review_status, time_validity, retrieved_at`.
Jede Beweiszuordnung: `source_id, source_url, publisher, published_at, retrieved_at, excerpt, page_or_section`.

### Aussagearten
- **Fakt:** direkt überprüfbare sachliche Angabe.
- **Selbstaussage:** Strategie/Positionierung in der Darstellung der Bank.
- **Interpretation:** gesondert markierte Ableitung, nie ungeprüft als Tatsache präsentieren.

### Status
- `nicht_recherchiert`
- `keine_information_gefunden` (kein negatives Leistungsurteil)
- `pruefung_erforderlich`
- `belegt`
- `widerspruechlich`
- `veraltet`
- `quelle_nicht_erreichbar`

Manuelle Freigabe für KI-generierte Fakten vor Veröffentlichung. Originalzitate nur kurz im erforderlichen Umfang; eigentliche Texte eigenständig formulieren.

## 5. Hauptansichten und Nutzungsflüsse

### Bankenübersicht
Volltextsuche, Geschäftsgebiet, Zielgruppen, strategische Schwerpunkte, Finanzierung und Zahlungsverkehr als Filter. Bankkarten mit Profilstatus und Aktualisierungsdatum. Kein numerisches KPI-Ranking.

### Bankdetailseite
Kopfbereich mit Name, Ort, Geschäftsgebiet, Website, Recherche-/Reviewstand. Darunter **Management Summary** (150–250 Wörter bei genügend Evidenz). Anschließend sieben thematische Sektionen, belegte Aussagen, Tags, Ausweis von Selbstaussagen, klickbare Evidenz. Nicht recherchierte Themen als solche ausweisen.

### Quelleninspektor
Quellenliste mit URL, Dokumenttitel, Herausgeber, Veröffentlichungs- und Abrufdatum, Verarbeitung, Extraktionshinweis, Kurzbeleg und Fundstelle. Nutzer kann Quellen manuell hinzufügen oder öffentlich zugängliche PDFs hochladen.

### Recherche und Prüfen
Bank wählen → offizielle Seite bestätigen → öffentliche Links/Docs einlesen → strukturierte Kandidatenaussagen erzeugen → deduplizieren → manuelle Freigabe → Profil aktualisieren. Informationen aus Suchergebnissen nur nach Öffnen/Prüfen des Originalbelegs aufnehmen. Ohne KI-Schlüssel kein Fake-Research: manuelle Erfassung und regelbasierte Text-/PDF-Extraktion soweit möglich.

### Entwicklungen
Datierte Timeline strategischer Entwicklungen; Links zu Primärquelle und Status.

### Bankenvergleich
Zwei bis vier Banken nebeneinander: Geschäftsgebiet, Strategie, Zielgruppen, Finanzierung, Payment, Marktpositionierung, Entwicklung. Leere Daten heißen `nicht öffentlich verifiziert`; daraus keine Nachteile ableiten.

## 6. Technische Zielarchitektur
Frontend bevorzugt Next.js + TypeScript + Tailwind, Backend bevorzugt FastAPI + Pydantic + SQLAlchemy + Alembic; SQLite Entwicklung, PostgreSQL-kompatibel für später. Das vorhandene statische HTML darf als Referenz verwendet werden. Separate API und Persistenz. Optionale KI-Extraktion hinter Interface mit validierter JSON-Struktur und nachvollziehbaren Promptversionen. Verwaltung von Scan-/Research-Jobs mit Status und Logs.

### Entitäten
- Bank
- Source
- QualitativeFinding
- FindingEvidence (n:m zwischen Findings und Quellen)
- BankSummary (Versionen, Quellenverweise)
- ResearchJob
- ReviewEvent
- optional StrategicEvent und Tag

## 7. Sicherheits-, Rechts- und Betriebsanforderungen
Nur erlaubte öffentliche Daten; Zugriffsbeschränkungen, robots.txt, Nutzungsbedingungen und Abruflimits respektieren. SSRF-Abwehr durch Einschränkung privater/Loopback-Adressen, Redirectprüfung, URL-Validierung, Timeouts, Downloadgrößenlimits. Uploadlimits; keine unsichere HTML-Ausgabe; API-Schlüssel nicht im Frontend; Logging ohne Secrets. Transparente Fehlermeldungen. Quellen dürfen bei Abruffehlern nicht gelöscht werden.

## 8. Pilot und Quellen
Pilotbank: **Hamburger Volksbank eG**, https://www.hamburger-volksbank.de
Priorisiere offizielle Firmenkundenseiten, Lage-/Geschäftsberichte und Presseinformationen; externe offizielle Stellen wie BVR für Struktur/Kontext. Es gibt bereits eine bestehende, eher quantitative `index.html` auf `main`. Diese enthält ggf. allgemeine Fakten/Quellen, ist aber nicht die verbindliche Qualitätsgrundlage: alle Aussagen neu validieren. Keine Beispielinhalte als verifiziert anzeigen.

## 9. Umsetzung und Akzeptanzkriterien
1. Ein lokal startbares MVP.
2. Bankprofil und manuelle Quellenanlage funktionieren.
3. Aussage mit Beleg und Reviewstatus lässt sich speichern und prüfen.
4. Sieben Kategorien inkl. sinnvoller Leerzustände.
5. Quellenbasierte Summary und Bankenvergleich, sobald genügend geprüfte Daten vorliegen.
6. Recherchemodul optional, aber real und transparent; Konfiguration über `.env.example`.
7. Versionierung, Dublettenprüfung und Quellenaktualisierung.
8. Tests für Fachregeln, Datenpersistenz, Pflichtbelege und relevante Negativfälle.
9. Klare Installations-/Startdokumentation.
10. Keine klassischen Finanz-/KPI-Widgets im Zielprodukt.
