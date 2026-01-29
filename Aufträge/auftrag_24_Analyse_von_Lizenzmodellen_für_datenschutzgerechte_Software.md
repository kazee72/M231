# Auftrag 24 – Lizenzmodelle und Datenschutz

## 1. Softwarelösungen

### Proton Drive
- **Lizenzmodell:** Open Source
- **Anbieter:** Proton AG (Schweiz)
- **Features:** Ende-zu-Ende-Verschlüsselung, Schweizer Datenschutz

### Google Drive
- **Lizenzmodell:** Proprietär (geschlossener Quellcode)
- **Anbieter:** Google LLC (USA)
- **Features:** Integration ins Google-Ökosystem, grosse Speicherkapazität

### Nextcloud
- **Lizenzmodell:** Open Source (AGPLv3)
- **Anbieter:** Nextcloud GmbH (Deutschland)
- **Features:** Komplette Kontrolle über Server und Daten, Self-Hosting möglich

---

## 2. Analyse der Lizenzbedingungen

### Proton Drive (Open Source)
 
Open Source mit Freemium-Geschäftsmodell. Der Quellcode ist öffentlich einsehbar und kann von jedem überprüft werden. Die Nutzung ist kostenlos möglich, erweiterte Funktionen sind kostenpflichtig.

**Bedingungen für Datenschutz und Datensicherheit:**
- Ende-zu-Ende-Verschlüsselung: Nur der Nutzer kann seine Daten lesen
- Serverstandort in der Schweiz → Schweizer Datenschutzgesetz (DSG) gilt
- Cloud-Nutzung: Ja, aber vollständig verschlüsselt
- Quellcode einsehbar → unabhängige Sicherheitsaudits sind möglich
- Updates werden regelmässig vom Anbieter bereitgestellt

**Mögliche Risiken:**
- Abhängigkeit vom Anbieter (falls Proton den Dienst einstellt)
- Kostenpflichtig für grössere Speichermengen
- Keine Self-Hosting-Option (Daten liegen immer bei Proton)

---

### Google Drive (Proprietär)

 Proprietär/Closed Source mit Freemium-Modell. Der Quellcode ist geschlossen und nicht einsehbar. Die Nutzung ist nur gemäss den Google-Nutzungsbedingungen erlaubt. Modifizierung und Weiterverbreitung sind nicht gestattet.

**Bedingungen für Datenschutz und Datensicherheit:**
- Verschlüsselung während Übertragung und Speicherung (aber Google hat Zugriff auf die Daten)
- Server weltweit, hauptsächlich in den USA → US-Gesetze (z.B. CLOUD Act) sind anwendbar
- Cloud-Nutzung: Ja, ausschliesslich (kein Self-Hosting)
- Quellcode nicht einsehbar → keine unabhängige Sicherheitsüberprüfung möglich
- Updates werden automatisch eingespielt

**Mögliche Risiken:**
- Fehlende Kontrolle über die eigenen Daten
- Google kann Daten für Werbezwecke analysieren
- Datenweitergabe an US-Behörden ist möglich
- Starke Abhängigkeit vom Google-Ökosystem
- Eingeschränkte Transparenz bezüglich Datenverarbeitung

---

### Nextcloud (Open Source)

**Lizenzmodell in eigenen Worten:**  
Open Source unter der AGPLv3-Lizenz. Die Software ist vollständig frei nutzbar, modifizierbar und kann auf eigenen Servern betrieben werden. Der Quellcode ist öffentlich und darf weiterverbreitet werden.

**Bedingungen für Datenschutz und Datensicherheit:**
- Self-Hosting möglich → volle Kontrolle über den Serverstandort
- Quellcode offen → Community und Sicherheitsexperten können den Code prüfen
- Verschlüsselung kann optional aktiviert werden
- Updates müssen bei Self-Hosting selbst eingespielt werden
- Keine automatische Datenübermittlung an Drittanbieter

**Mögliche Risiken:**
- Bei Self-Hosting: Eigene IT-Kompetenz für Wartung und Sicherheit erforderlich
- Eingeschränkter Support (Community-basiert, ausser bei kostenpflichtiger Enterprise-Version)
- Sicherheitslücken müssen selbständig gepatcht werden
- Initialaufwand für Einrichtung und Konfiguration

---

## 3. Vergleich der Lizenzmodelle

| Kriterium | Proton Drive | Google Drive | Nextcloud |
|-----------|--------------|--------------|-----------|
| **Lizenzmodell** | Open Source | Proprietär | Open Source |
| **Serverstandort** | Schweiz | USA/weltweit | Frei wählbar |
| **Datenkontrolle** | Mittel | Gering | Hoch |
| **Quellcode einsehbar** | Ja | Nein | Ja |
| **Verschlüsselung** | E2E (Standard) | Transport/Speicher | Optional |
| **Self-Hosting** | Nein | Nein | Ja |
| **Kosten** | Freemium | Freemium | Kostenlos (+ Serverkosten) |
| **Support** | Bezahlt/Community | Google Support | Community/Enterprise |
| **DSGVO/DSG-Konformität** | Hoch | Problematisch | Sehr hoch |

### Beurteilung

Unter rechtlichen und datenschutztechnischen Gesichtspunkten sind **Proton Drive** und **Nextcloud** deutlich besser geeignet als Google Drive:

- Beide sind Open Source und ermöglichen Transparenz
- Beide können europäischem bzw. schweizerischem Datenschutzrecht unterstellt werden
- Keine Datenanalyse durch den Anbieter zu Werbezwecken
- Keine Gefahr der Datenweitergabe an US-Behörden (bei korrekter Konfiguration)

**Google Drive** ist für sensible Kundendaten problematisch, da der US-amerikanische Serverstandort und die geschlossene Software keine ausreichende Kontrolle und Transparenz bieten.

---

## 4. Empfehlung und Begründung

### Empfehlung: Nextcloud (Self-Hosted)

Für den Einsatz mit sensiblen Kundendaten eignet sich **Nextcloud** am besten.

### Begründung

**Lizenzmodell:**  
Das Open-Source-Lizenzmodell (AGPLv3) ermöglicht volle Transparenz. Der Quellcode kann jederzeit auf Sicherheitslücken und Hintertüren geprüft werden. Dies schafft Vertrauen und erfüllt Compliance-Anforderungen.

**Datenschutz:**  
Durch Self-Hosting behält das Unternehmen die komplette Kontrolle über seine Daten:
- Der Serverstandort ist frei wählbar (z.B. eigenes Rechenzentrum in der Schweiz)
- Keine Abhängigkeit von Drittanbietern
- Keine Daten verlassen die eigene Infrastruktur
- Volle Konformität mit dem Schweizer DSG und der EU-DSGVO garantierbar

**Datensicherheit:**  
Das Unternehmen ist selbst für Verschlüsselung, Backups, Zugriffskontrollen und Updates verantwortlich. Bei sensiblen Kundendaten ist dies ein Vorteil, da keine externen Parteien Zugriff auf die Systeme haben.

### Alternative

Falls das Unternehmen keine eigene IT-Infrastruktur betreiben möchte oder kann, ist **Proton Drive** eine gute Alternative:
- Schweizer Server und Schweizer Datenschutzgesetz
- Ende-zu-Ende-Verschlüsselung ohne eigenen Aufwand
- Kein Self-Hosting-Aufwand nötig