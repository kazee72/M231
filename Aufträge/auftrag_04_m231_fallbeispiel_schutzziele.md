# Fallbeispiele Schutzziele

## 1. Definition Schutzziele

- **Vertraulichkeit:**
    - Informationen werden nur für autorisierte Personen und oder Systeme zugänglich gemacht. Unbefugte dürfen keinen Zugriff auf diese Informationen haben.

- **Integrität:**
    - Daten sind vollständig, korrekt und unverändert. Informationen dürfen nicht unbemerkt oder unbefugt verändert oder verfälscht werden können.

- **Verfügbarkeit:**
    - Systeme, Dienste und Informationen sind jederzeit für autorisierte Personen verfügbar.

---

## 2. Bewertung Schutzziele mit Beispielen

### Entwicklung / Testing:

- **Vertraulichkeit:**
    - **Bsp:** Quellcode muss geschützt sein
    - **Risiko:** Diebstahl von Eigentum. Konkurrenz könnt code sehen.
    - **Massnahmen:** Zugriffskontrollen auf Git-Repos, NDA für Mitarbeiter

- **Intergrität:**
    - **Bsp:** Code-Changes müssen nachvollziehbar und dokumentiert sein.
    - **Risiko:** Fehler in Produktion.
    - **Massnahmen:** Versioncontroll (Git), Code-Reviews, Pipeline

- **Verfügbarkeit:**
    - **Bsp:** Test-Server muss zugänglich sein
    - **Risiko:** Projektverzögerung
    - **Massnahmen:** Redundante Testsysteme, Regelmässige Backups, Monitoring

### Buchhaltung:

- **Vertraulichkeit:**
    - **Bsp:** Finanzdaten, Gehälter
    - **Risiko:** Datenleaks können zu rechtlichen Problemen führen
    - **Massnahmen:** Verschlüsselte Datenbanken, 2FA, Rollenbasierter Zugriff

- **Integrität:**
    - **Bsp:** Rechnungen
    - **Risiko:** Falsche Buchhaltung führt zu Verlusten / rechtliche Probleme
    - **Massnahmen:** regelmässige Kontrolle, digitale Signaturen, 4-Augen Prinzip

- **Verfügbarkeit:**
    - **Bsp:** Buchhaltungssoftware muss zu kritischen Zeiten verfügbar sein
    - **Risiko:** Verpasste Fristen
    - **Massnahmen:** Notfall-Recovery, Backups, Redundante Systeme


### Server / Netzwerk

- **Vertraulichkeit:**
    - **Bsp:** Server Zugangsdaten
    - **Risiko:** Unbefugter Zugriff auf Server / Netzwerk
    - **Massnahmen:** Firewalls, verschlüsselte Verbindungen

- **Integrität:**
    - **Bsp:** Server Konfigurationen
    - **Risiko:** Veränderungen können ganze Server / Systeme lahmlegen
    - **Massnahmen:** Konfigurationsüberwachung

- **Verfügbarkeit:**
    - **Bsp:** Alle Services
    - **Risiko:** Kompletter Absturz von ganzem System / Netzwerk
    - **Massnahmen:** Redundante Systeme / Server, Disaster Revovery

--- 

## 3. Risikoanalyse

| Bereich | Scenario/Risiko |  Ursache | Schadensgrösse | Massnahme |
|---------|----------------|---------|----------------|-----------|
| Entwicklung/Testing | Code-Diebstahl  | Schwache Zugriffskontrolle | Hoch | 2FA, Verschlüsselung |
| Entwicklung/Testing | Code-Manipulation  | Fehlende Reviews | Sehr hoch | Code-Reviews, Pipeline |
| Entwicklung/Testing | Test-System-Ausfall  | Hardware-Defekt | Mittel | Redundanz, Monitoring |
| Buchhaltung | Datenleck | Phishing-Angriff | Sehr hoch | Schulungen, Verschlüsselung |
| Buchhaltung | Falsche Buchungen  | Insider-Betrug | Sehr hoch | Vier-Augen-Prinzip, Logs |
| Buchhaltung | Software-Ausfall  | Software-Bug | Hoch | Hochverfügbarkeit, Backups |
| Server/Netzwerk | DDoS-Angriff  | Externer Angriff | Sehr hoch | DDoS-Protection |
| Server/Netzwerk | Unbefugter Zugriff | Gestohlene Credentials | Sehr hoch | Verschlüsselte Verbindungen |
| Server/Netzwerk | Hardware-Ausfall | Alterung/Überhitzung | Sehr hoch | Redundante Hardware, USV |