# Cookie-Sicherheit - Zusammenfassung

## Teil 1: Szenarien-Analyse (nach Risiko sortiert)

### 1. Höchstes Risiko: Session Hijacking (Szenario A)

**Risiko:** Session Hijacking - Angreifer übernimmt komplette Kontrolle über Account
- Angriffsmethoden: XSS, Man-in-the-Middle, Network Sniffing
- Kritisch, weil voller Zugriff auf Nutzerdaten möglich

### 2. Hohes Risiko: Unverschlüsselte Übertragung (Szenario B)

**Risiko:** Data Exposure
- Cookies können in öffentlichen WLANs abgefangen werden
- Manipulation während Übertragung möglich

### 3. Mittleres Risiko: Zu breiter Cookie-Scope (Szenario D)

**Risiko:** Cookie Leakage
- Beispiel: banking.example.com Cookie auch auf blog.example.com verfügbar

### 4. Niedrigeres Risiko: Tracking ohne Zustimmung (Szenario C)
**Szenario:** Website setzt Tracking-Cookies ohne Nutzereinwilligung

**Risiko:** Datenschutzverletzung
- DSGVO-Verstoss (Bußgelder bis 20 Mio. € oder 4% Jahresumsatz)
- Privacy-Verletzung, aber kein direkter Sicherheitsangriff

---

## Teil 2: Drei Schutzmassnahmen

### 1. Secure-Flag
**Was:** Cookie wird nur über HTTPS übertragen
```
Set-Cookie: sessionId=abc123; Secure
```
**Schützt gegen:**
- Man-in-the-Middle (MITM)
- Network Sniffing

### 2. HttpOnly-Flag
**Was:** JavaScript kann nicht auf Cookie zugreifen
```
Set-Cookie: sessionId=abc123; Secure; HttpOnly
```
**Schützt gegen:**
- Cross-Site Scripting (XSS)

### 3. SameSite-Attribut
**Was:** Kontrolliert, ob Cookie bei Cross-Site Requests mitgesendet wird
```
Set-Cookie: sessionId=abc123; Secure; HttpOnly; SameSite=Strict
```

**Modi:**
- `Strict`: Nur bei gleicher Domain
- `Lax`: Bei Top-Level Navigation
- `None`: Immer (braucht Secure-Flag)

**Schützt gegen:**
- Cross-Site Request Forgery (CSRF)
- Clickjacking
- Bestimmte XSS-Szenarien

---

## Teil 3: Praktische Browser-Analyse

### Beispiel GitHub:

| Name | Domain | Secure | HttpOnly | SameSite | Bewertung |
|------|--------|--------|----------|----------|-----------|
| _gh_sess | .github.com | ✓ | ✓ | Lax | Gut |
| user_session | .github.com | ✓ | ✓ | Lax | Gut |
| preferred_color_mode | .github.com | ✓ | ✗ | Lax | Ok  |

**Bewertung:**
- Alle verwenden Secure
- Session-Cookies haben HttpOnly

### Könnte die Website ohne Zustimmung Tracking-Cookies verwenden?

**Antwort: Nein, aktuell nicht erkennbar**

### Warum?

1. **Keine Third-Party Cookies**: Alle Cookies kommen von `.github.com` selbst
2. **Nur funktionale Cookies**:
   - `_gh_sess` = Session (notwendig)
   - `user_session` = Login (notwendig)
   - `color_mode` = Präferenz (funktional)

GitHub nutzt nur notwendige und funktionale Cookies. Keine Tracking-Cookies ohne Zustimmung erkennbar.