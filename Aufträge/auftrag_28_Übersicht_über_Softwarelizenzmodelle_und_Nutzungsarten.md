# Software-Lizenzen

Software-Lizenzen definieren, wie Software genutzt, verändert und verbreitet werden darf.

## Freie Lizenzen

Diese erlauben grosse Freiheit mit minimalen Einschränkungen.

| Lizenz | Beschreibung |
|--------|--------------|
| **MIT** | Sehr einfach, erlaubt fast alles, solange der Lizenztext beibehalten wird. Beliebt für Bibliotheken. |
| **Apache 2.0** | Ähnlich wie MIT, enthält aber explizite Patentgewährung und verlangt die Dokumentation von Änderungen. |

## Copyleft-Lizenzen

Diese verlangen, dass abgeleitete Werke dieselbe Lizenz verwenden.

| Lizenz | Beschreibung |
|--------|--------------|
| **GPL (v2, v3)** | Wenn du den Code veränderst und verbreitest, musst du deinen Quellcode ebenfalls unter GPL veröffentlichen. Diese "virale" Eigenschaft hält Code offen. |
| **LGPL** | Schwächeres Copyleft; erlaubt die Verlinkung mit proprietärer Software, ohne dass das gesamte Projekt GPL werden muss. |
| **AGPL** | Wie GPL, gilt aber auch für Software, die über ein Netzwerk zugänglich ist. |

## Proprietär

Der Quellcode ist nicht verfügbar und die Nutzung wird durch eine EULA geregelt. Die meiste kommerzielle Software fällt hierunter.

## Creative Commons

Nicht für Code konzipiert, wird aber manchmal für Dokumentation, Assets oder Datensätze verwendet. Verschiedene Kombinationen:

- **BY** – Namensnennung erforderlich
- **SA** – Weitergabe unter gleichen Bedingungen
- **NC** – Nur nicht-kommerzielle Nutzung
- **ND** – Keine Bearbeitungen erlaubt

## Praktische Richtlinien

### Lizenz für dein eigenes Projekt wählen

- **MIT / Apache 2.0** – Verwende diese, wenn du möchtest, dass andere deinen Code frei und mit minimalen Einschränkungen nutzen können.
- **GPL** – Verwende diese, wenn du sicherstellen willst, dass alle abgeleiteten Werke Open-Source bleiben.

### Bibliotheken in deinem Projekt verwenden

Prüfe die Lizenzkompatibilität:

- **MIT-lizenzierter Code** kann fast überall verwendet werden (proprietär oder Open-Source).
- **GPL-Code** kann nicht in proprietäre Projekte eingebunden werden – das gesamte Projekt muss GPL werden.
- **LGPL-Code** kann mit proprietärer Software verlinkt werden, ohne diese zu "infizieren".

## Schnellvergleich

| Lizenz | Permissiv | Copyleft | Patentgewährung | Netzwerk-Klausel |
|--------|:---------:|:--------:|:---------------:|:----------------:|
| MIT | ✓ | ✗ | ✗ | ✗ |
| Apache 2.0 | ✓ | ✗ | ✓ | ✗ |
| BSD | ✓ | ✗ | ✗ | ✗ |
| GPL v3 | ✗ | ✓ | ✓ | ✗ |
| LGPL | ✗ | Schwach | ✓ | ✗ |
| AGPL | ✗ | ✓ | ✓ | ✓ |