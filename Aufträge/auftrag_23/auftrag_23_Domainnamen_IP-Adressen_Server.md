# Auftrag 23

## Beispiel https://sbb.ch

### Wichtige Seiten

Impressum: https://www.sbb.ch/de/meta/legallines/impressum.html?hidebanner=true

DSE: https://www.sbb.ch/de/meta/legallines/datenschutz.html?hidebanner=true#sbbac20b9

Barrierefreiheit: https://www.sbb.ch/de/meta/legallines/barrierefreiheit.html

Rechtlicher Hinweis: https://www.sbb.ch/de/meta/legallines/rechtlicher-hinweis.html



### Domain

https://sbb.ch

### Subdomains

-> subdomains.txt


### Services

https://sbb.ch [301] [301 Moved Permanently] [Apache HTTP Server,HSTS,Varnish]

- **Apache HTTP Server:** Web Server -> Open-Source-Webserver, der HTTP-Anfragen verarbeitet, statische Dateien bereitstellt und Anfragen an Backend-Anwendungen weiterleitet.

**Varnish:** Caching Reverse Proxy -> Sitzt vor dem Webserver und speichert Antworten im Cache.

**HSTS:** Sicherheitsheader -> HTTP Strict Transport Security — eine Sicherheitsrichtlinie, die Browser zwingt, nur HTTPS-Verbindungen zu verwenden. 


### CH Registry

**SWITCH** -> Organisation die alle .CH-Domains verwaltet. Der "Herausgeber" aller Schweizer Domains.

### Domain sbb.ch

**Registrar: CSC Corporate Domains, Inc.**
Das ist die Firma, über die SBB ihre Domain registriert hat. CSC ist ein US-amerikanischer Enterprise-Registrar.

### Nameserver

Das sind die **Server**, die auflösen, wohin sbb.ch zeigt:

- ns-1254.awsdns-28.org
- ns-1739.awsdns-25.co.uk
- ns-73.awsdns-09.com
- ns-967.awsdns-56.net

Das sind **AWS-Nameserver** (Amazon Web Services).

ns.sbb.ch	*[91.230.140.140]*

Das ist der eigene Namenserver von der SBB. Ip -> 91.230.140.140


## Visuelle Darstellung

```Mermaid
graph TB
    CLIENT[Benutzer]
    DOMAIN[sbb.ch Domain]
    DNS[DNS Nameserver<br/>AWS + SBB]
    
    VARNISH[Varnish Cache]
    APACHE[Apache Webserver]
    BACKEND[Backend<br/> Datenbank]
    SWITCH[SWITCH<br/>CH Registry]

    SWITCH -->|verwaltet| DOMAIN
    CLIENT -->|Fragt IP-Adresse| DNS
    DNS -->|kennt| DOMAIN
    DNS -.->|gibt IP zurück| CLIENT
    CLIENT -->|HTTPS Request| VARNISH
    VARNISH --> APACHE
    APACHE --> BACKEND
    BACKEND -.->|Response| CLIENT
```

