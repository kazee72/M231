# Arbeitsauftrag 13 - *Datenschutzanalyse einer Anwendung (DSVGO/DSG)* (PROTON)

## A. Grundlagenrechere

### Rechtmässigkeit

Personendaten dürfen nur rechtmässig verarbeitet werden, d.h. es muss eine gesetzliche Grundlage vorliegen (z.B. Einwilligung, Vertragserfüllung, berechtigtes Interesse oder gesetzliche Pflicht). Die Verarbeitung muss nach Treu und Glauben erfolgen.

### Datenminimierung

Es dürfen nur jene Daten erhoben werden, die für den spezifischen Zweck tatsächlich notwendig sind. Überflüssige oder "nice-to-have" Daten sind zu vermeiden. Dies reduziert das Risiko bei Datenlecks.

### Zweckbindung

Personendaten dürfen ausschliesslich für den ursprünglich festgelegten Zweck verwendet werden. Eine nachträgliche Zweckänderung ist nur unter strengen Voraussetzungen möglich und erfordert erneute Information oder Einwilligung.

### Transparenz

Betroffene Personen müssen klar, verständlich und umfassend über die Datenverarbeitung informiert werden. Dies umfasst Zweck, Umfang, Empfänger, Speicherdauer und Rechtsgrundlage der Verarbeitung.

### Betroffenenrechte

Nutzer haben das Recht auf Auskunft, Berichtigung, Löschung (Recht auf Vergessenwerden), Datenübertragbarkeit, Widerspruch und Einschränkung der Verarbeitung. Diese Rechte müssen einfach ausübbar sein.

### Datensicherheit

Technische und organisatorische Massnahmen müssen den Schutz der Daten gewährleisten. Dazu gehören Verschlüsselung, Zugriffskontrolle, Pseudonymisierung, Backup-Systeme und Incident-Response-Prozesse.


## B. Analyse der Anwendung Proton

Proton ist ein Schweizer Anbieter für datenschutzorientierte Online-Dienste (Proton Mail, VPN, Drive, Calendar, Pass).

### Erhobene Daten: 

- E-Mail
- Benutzername
- Passwort (verschlüsselt --> nicht zugänglich für Proton)
- Zahlungsinformationen (bei kostenpflichtigen Plänen)
- IP-Adresse (temporär beim Login)
- Geräte-Information
- Metadaten (Absender, Empfänger, Timestamps)
- Nutzungsstatistiken (anonymisiert)

### Nicht erhobene Daten: 

- E-Mail-Inhalte (End-To-End-Encrypted)
- Betreffzeilen (Encrypted)
- Anhänge (Encrypted)

### Datenschutz-Checkliste

---

### A. Allgemeine Datenschutzgrundsätze

| Punkt | Ja/Nein | Kommentar |
|-------|---------|-----------|
| Die Anwendung erhebt nur Daten, die für den Zweck notwendig sind (Datenminimierung) | **Ja** | Minimale Datenerhebung, E-Mail-Wiederherstellung ist optional |
| Es gibt eine klare Rechtsgrundlage für jede Datenverarbeitung | **Ja** | Vertragserfüllung und berechtigtes Interesse |
| Die Daten werden nur für den angegebenen Zweck verwendet (Zweckbindung) | **Ja** | Klare Zweckdefinition in Privacy Policy |
| Die Daten werden nicht länger gespeichert als notwendig (Speicherbegrenzung) | **Ja** | IP-Adressen werden nicht dauerhaft gespeichert, gelöschte E-Mails sind permanent entfernt |
| Es existiert ein System zur Sicherstellung der Datenrichtigkeit | **Ja** | Nutzer können Profildaten jederzeit korrigieren |

---

### B. Einwilligung & Transparenz

| Punkt | Ja/Nein | Kommentar |
|-------|---------|-----------|
| Nutzer werden vorab transparent über die Datenverarbeitung informiert | **Ja** | Ausführliche Privacy Policy, transparent dokumentiert |
| Eine freiwillige und informierte Einwilligung wird eingeholt, falls nötig | **Ja** | Bei Registrierung und optionalen Funktionen |
| Die Einwilligung kann leicht widerrufen werden | **Ja** | Account-Löschung jederzeit möglich, klare Opt-out-Optionen |

---

### C. Datensicherheit

| Punkt | Ja/Nein | Kommentar |
|-------|---------|-----------|
| Daten werden verschlüsselt übertragen | **Ja** | TLS 1.3 für Übertragung, Ende-zu-Ende-Verschlüsselung für Inhalte |
| Daten werden sicher gespeichert | **Ja** | Zero-Access-Verschlüsselung, Proton kann Inhalte nicht lesen |
| Zugriff auf Daten ist auf notwendige Personen beschränkt | **Ja** | Strikte Zugriffskontrollen, Schweizer Rechenzentren |
| Es existieren technische und organisatorische Massnahmen gegen Datenverlust | **Ja** | Redundante Systeme, regelmässige Sicherheitsaudits |

---

### D. Weitergabe an Dritte

| Punkt | Ja/Nein | Kommentar |
|-------|---------|-----------|
| Die Anwendung informiert darüber, ob Daten an Dritte weitergegeben werden | **Ja** | Keine Weitergabe an Dritte, explizit dokumentiert |
| Es bestehen Verträge zur Auftragsdatenverarbeitung (sofern nötig) | **Ja** | Zahlungsabwicklung über externe Partner mit ADV-Verträgen |
| Die Dritten befinden sich in Ländern mit angemessenem Datenschutzniveau | **Ja** | Primär Schweiz (angemessenes Niveau), EU-Partner DSGVO-konform |

---

### E. Rechte der Betroffenen

| Punkt | Ja/Nein | Kommentar |
|-------|---------|-----------|
| Nutzer können Auskunft über ihre Daten verlangen | **Ja** | Datenexport-Funktion verfügbar |
| Daten können korrigiert oder gelöscht werden (Recht auf Vergessenwerden) | **Ja** | Account-Löschung führt zu vollständiger Datenlöschung |
| Nutzer haben das Recht auf Datenportabilität | **Ja** | Export in standardisierten Formaten möglich (.eml, .ics) |
| Es gibt eine klare Kontaktstelle für Datenschutzanliegen | **Ja** | DPO@proton.me, Support-Team für Datenschutzfragen |

---

## Zusammenfassung

**Gesamtbewertung:** Alle Checklistenpunkte erfüllt (100%)

**Stärken:**
- Vorbildliche Datensicherheit durch Zero-Access-Verschlüsselung
- Transparente Datenschutzerklärung
- Minimale Datenerhebung
- Schweizer Rechtsstandort mit starkem Datenschutz

**Kritische Punkte:**
- Metadaten bei externen E-Mails teilweise sichtbar
- Temporäre IP-Speicherung beim Login (für Sicherheit notwendig)




