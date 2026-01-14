# Zweck und Grenzen von Backups

## 1. Was ist ein Backup?

Ein Backup ist eine Sicherungskopie von Daten, die auf einem separaten Speichermedium und oder an einem anderen Ort aufbewahrt wird. Das Ziel eines Backups ist es, Daten vor Verlust zu schützen und diese im Notfall wiederherstellen zu können. 

Beispiele für Backups:
- Dateien
- Datenbanken
- Systemkonfigurationen

## 2. Zweck von Backups und Anwendungsbeispiele

Der Hauptzweck von Backups ist es Datenverlust zu verhindern und die 24/7 availability sicherzustellen.

Beispiele: 

- **Schutz vor Hardwareausfall:** Daten werden auf Harddisks gespeichert. Wenn diese nun ausfallen / kaputt gehen, sind die Daten aufgrund von Backups nicht verloren.

- **Versehentliches Löschen:** Daten werden ausversehen gelöscht, können aber dank der Backups wiederhergestellt werden.

- **Schutz vor Ransomware:** Durch eine Ransomware sind alle Daten verschlüsselt, sind aber durch ein unabhöngiges Backup sicher und unverschlüsselt.

## 3. Grenzen und Risiken von Backups

- **Veraltete Sicherungen:** Wenn Backups nicht regelmäßig durchgeführt werden, können neuere Daten verloren gehen.

- **Fehlende Restore-Tests:** Viele Organisationen erstellen Backups, testen aber nie den Ernstfall. Wenn dieser dann antritt stellt sich dann heraus, dass das Backup beschädigt oder unvollständig ist, was zu kritischen Datenverlusten führen kann.

- **Benutzerfehler und mangelnde Schulung:** Wenn Mitarbeiter nicht ausreichend geschult sind, können fehlerhafte Backups erstellt werden oder wichtige Daten übersehen werden. Zudem können falsche Restore-Prozesse zu Dateninkonsistenzen führen.