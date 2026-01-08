# Backup-Dokumentation

## 1. Backup-Medium

**Gewählt**: Lokale Festplatte (Test)  
**Zukünftig**: Externe Festplatte

Für den Test wurde das Backup auf der gleichen Festplatte gemacht. Für echte Backups braucht es ein externes Medium (USB-Festplatte), damit die Daten bei einem Defekt geschützt sind.

---

## 2. Gesicherte Daten

**Test-Ordner**: `~/Documents/TBZ/M231/BackupTest/TestDaten`

Später sollen alle Schuldaten gesichert werden (Modul M231 und weitere Projekte).

---

## 3. Backup-Tool

**Tool**: `rsync`

`rsync` ist auf macOS bereits installiert und kopiert nur geänderte Dateien. Das spart Zeit bei regelmässigen Backups.

---

## 4. Backup-Befehl

```bash
rsync -av ~/Documents/TBZ/M231/BackupTest/TestDaten ~/Documents/TBZ/M231/BackupTest/BackupFolder
```

**Was macht der Befehl?**
- `-a` = Behält Berechtigungen und Zeitstempel
- `-v` = Zeigt Fortschritt an

**Für produktive Backups später**:
```bash
rsync -av --delete ~/Documents/TBZ/M231/ /Volumes/ExternalDrive/Backup/
```
Die Option `--delete` löscht Dateien im Backup, die im Original nicht mehr existieren.

---

## 5. Backup-Intervall

**Intervall**: Wöchentlich (jeden Sonntag)  
**Ausführung**: Manuell

Ein wöchentliches Backup reicht für Schuldaten. Automatisierung wäre mit `launchd` oder `cron` möglich.

---

## 6. Speicherort

**Test**: `~/Documents/TBZ/M231/BackupTest/BackupFolder/`  
**Später**: Externe Festplatte unter `/Volumes/ExternalDrive/Backup/`

---

## 7. Durchführung & Ergebnis

**Datum**: 08.01.2026

Das Backup wurde erfolgreich durchgeführt. Alle Dateien wurden kopiert und sind im Zielordner vorhanden.

---

## 8. Fazit

Das Tool `rsync` funktioniert gut für regelmässige Backups. Der Test war erfolgreich.

**Nächste Schritte**:
- Externe Festplatte besorgen
- Regelmässig (z.B. jeden Sonntag) Backup machen
- Optional: Backup automatisieren