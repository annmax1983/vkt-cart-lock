# VKT Cart Lock

[English](../README.md) | [中文](README_zh.md) | Deutsch | [Español](README_es.md) | [日本語](README_ja.md) | [Français](README_fr.md)

**Eine harte Bedenkzeit-Sperre für deinen Warenkorb.** Klick auf den Checkout und der Timer startet. Der Checkout bleibt blockiert, bis der Timer endet — dann öffnet er sich von selbst.

Auf Chinesisch auch als **冷静锁** bekannt.

> Chromium · Manifest V3 · 6 Sprachen · Kein Tracking · Local-first

---

## Warum VKT Cart Lock?

Die meisten „Impulskauf"-Tools lassen eine Tür offen: Schlummern, Überspringen, vorzeitiges Entsperren. VKT Cart Lock nicht. Der Sinn ist, die Entscheidung, die du bereits getroffen hast, vor der Version von dir zu schützen, die um Mitternacht auf einen Checkout-Button starrt.

- **Kein Überspringen, kein Schlummern, kein vorzeitiges Entsperren.** Die Deinstallation der Erweiterung ist der einzige Weg daran vorbei.
- **Der Timer läuft auch außerhalb der Seite weiter.** Tab schließen, Browser neu starten, morgen wiederkommen: Die Sperre ist immer noch da.
- **Ablauf ist standardmäßig still.** Der Checkout öffnet sich einfach wieder. Premium kann eine letzte Bestätigung hinzufügen.
- **Ein abgeschlossener Kauf startet eine neue Sperre.** Kaufen ändert die Gewohnheit nicht.
- **Local first.** Timer, Einstellungen, Nachrichten und Statistiken bleiben in deinem Browser. Keine Analyse, keine Werbung, keine Browserhistorie verlässt das Gerät.

---

## Funktionen

### Kostenlos

| Funktion | Beschreibung |
|---------|-------------|
| Harte Checkout-Sperre | Klicks, Checkout-Links, Formular-Absenden und Checkout-Seiten werden abgefangen |
| 24 Website-Presets + generische Erkennung | Handabgestimmte Regeln für große Shops, plus Text- und Selektor-Fallbacks überall sonst |
| Bedenkzeit-Presets | 1 Stunde, 6 Stunden, 24 Stunden oder 72 Stunden |
| Website-weite Timer | Eine aktive Sperre pro Website, gestartet durch den ersten Checkout-Klick |
| Eigene Nachrichten | Bis zu 20 Zeilen, fest, rotierend oder zufällig angezeigt |
| Drei Sounds | Schlag, Glockenspiel oder sanft, plus Stummschalter |
| Kleinbetrags-Ausnahme | Lass das Nötigste unter einem gewählten Betrag passieren |
| Erlaubnisliste und Zwangssperren | Überspringe einen vertrauenswürdigen Shop oder zwinge den Schutz auf einen kleinen unabhängigen Laden |
| Ruhezeit bei Sales | Black Friday, Prime Day und Double 11 verlängern die Bedenkzeit automatisch auf 72 Stunden |
| Passwortgeschützte Einstellungen | Eine 4–8-stellige PIN schützt die Einstellungsseite |
| Gefühls-Tags | Markiere den Moment — spät in der Nacht, Sale, wütend, gelangweilt, einfach nur haben wollen |
| Fehlblockaden-Feedback | Markiere einen Fehlalarm und schließe dieses Element beim nächsten Mal aus |
| Badge-Countdown | Das Toolbar-Symbol zeigt verbleibende Stunden oder Minuten |
| Ledger-Basics | Gesamtzahl blockierter Checkouts und gesperrter Betrag, inklusive des aktuellen Monats |

### Premium

| Funktion | Beschreibung |
|---------|-------------|
| Eigene Bedenkzeiten | Alles von 10 Minuten bis 30 Tage |
| Artikelbezogene Timer | Eine Sperre pro Produkt statt pro Website |
| Start bei „In den Warenkorb" | Der Timer startet, sobald ein Artikel in den Warenkorb kommt |
| Unbegrenzte Nachrichten | Nur begrenzt durch das Sync-Budget über Geräte hinweg (ca. 60 Zeilen) |
| Ruhezeiten | Kein Sound während gewählter Stunden; die Sperre funktioniert trotzdem |
| Bestätigung nach Ablauf | Ein letzter „Ich will es immer noch"-Klick nach dem Timerende |
| Geräteübergreifende Synchronisierung | Einstellungen und Timer folgen deinem Chrome-/Edge-Konto |
| 12-Monats-Berichte | Monatlicher Trend, Website-Ranking und Gefühls-Aufschlüsselung |
| CSV-Export | Nimm den Verlauf in eine Tabelle mit |
| JSON-Backup | Vollständiger Export und Import von Einstellungen, Nachrichten, Timern und Statistiken |

Die Premium-Aktivierung ist optional. Alles oberhalb der Premium-Linie funktioniert ohne Konto oder Lizenzschlüssel.

---

## So funktioniert es

1. **Erster Checkout-Klick.** Der Schutz fängt den Klick ab, startet den Timer und zeigt den Sperrbildschirm. Die Bestellung wird nicht abgeschickt.
2. **Jeder weitere Versuch danach.** Der Checkout bleibt blockiert, und das Overlay zählt die verbleibende Zeit herunter.
3. **Der Timer ist maßgeblich.** Er lebt im Erweiterungsspeicher, nicht im Tab. Seite schließen, Shop neu öffnen oder Browser neu starten verkürzt ihn nicht.
4. **Wenn die Zeit um ist.** Die Sperre löst sich still und der Checkout ist wieder erlaubt. Premium-Nutzer können zuerst einen Bestätigungsklick verlangen.
5. **Nach einem Kauf.** Eine abgeschlossene Bestellung startet eine frische Bedenkzeit, sodass der nächste Kauf dieselbe Pause durchläuft.

Der Schutz arbeitet nur in der Seite. Er hängt sich nie in Netzwerkanfragen und berührt nie Zahlungs-Iframes oder Zahlungsanbieter-Seiten (Stripe, PayPal, Adyen, checkout.com, Braintree und ähnliche Hosts sind ausgenommen).

---

## Installation

1. Öffne `chrome://extensions/` in Chrome oder `edge://extensions/` in Edge.
2. Aktiviere den **Entwicklermodus**.
3. Klicke auf **Entpackte Erweiterung laden** und wähle diesen Ordner.
4. Hefte die Erweiterung an die Toolbar.

Für einen paketierten Build nutze die Zip in `publish/` oder lade während der Entwicklung den Ordner manuell.

---

## Verwendung

- **Bedenkzeit festlegen.** Öffne die Erweiterungsoptionen und wähle ein Preset oder mit Premium eine eigene Dauer.
- **Schreib deine eigene Zeile.** Der Sperrbildschirm kann deine Worte statt der eingebauten Zitate zeigen. Der Rotationsmodus verhindert, dass es zur Tapete wird.
- **Regeln hinzufügen.** Setze eine Lebensmittel-Seite auf die Erlaubnisliste, erzwinge die Sperre bei einem kleinen Shop oder befreie Bestellungen unter einem festgelegten Betrag.
- **Beobachte das Badge.** Der Toolbar-Countdown ist die stille Erinnerung, dass die Sperre noch aktiv ist.
- **Prüfe das Ledger.** Das Dashboard zeigt, was blockiert wurde, was es gekostet hätte, welche Websites und Stimmungen die meisten Checkouts auslösen, und einen 12-Monats-Trend.
- **Sichern (Premium).** Nutze den JSON-Export vor einem Gerätewechsel. Sync stellt Einstellungen und Timer wieder her, lokale Statistiken reisen jedoch nicht mit.

Die Deinstallation der Erweiterung löscht ihre lokalen Daten. Wenn Premium-Sync aktiviert ist, kehren Nachrichten und Einstellungen nach der Neuinstallation zurück; Statistiken und der lokale Verlauf nicht.

---

## Unterstützte Websites

Handabgestimmte Presets decken 24 Shops ab, darunter Amazon, eBay, Etsy, Walmart, Target, Best Buy, Home Depot, Lowe's, Newegg, Wayfair, Mercari, AliExpress, Temu, Alibaba, DHgate, Shopee, Lazada, Rakuten, SHEIN, TikTok Shop, bol.com, Allegro, Otto und Cdiscount.

Jeder andere Shop wird durch generisches Abgleichen von Checkout-Button-Text und Selektoren abgedeckt. Ändert eine Website ihr Markup, sagt dir der Selbsttest-Hinweis im Popup, dass der Schutz eventuell erneut geprüft werden sollte.

---

## Unterstützte Browser

| Browser | Status |
|---------|--------|
| Google Chrome | Vollständig unterstützt |
| Microsoft Edge | Vollständig unterstützt |
| Andere Chromium-basierte Browser | Sollte funktionieren |

---

## Daten und Datenschutz

- **Lokal gespeichert:** Einstellungen, Timer, Statistiken, Selbsttest-Notizen, die optionale Einstellungs-PIN (nur gesalzener SHA-256-Hash) und der Premium-Lizenzdatensatz.
- **Synchronisiert (Premium, Opt-in):** Einstellungen, eigene Nachrichten und schlanke Timer-Datensätze über `chrome.storage.sync`. Die Einstellungs-PIN wird nie synchronisiert.
- **An den Lizenzserver gesendet:** nur beim Aktivieren, Validieren oder Deaktivieren von Premium — Lizenzschlüssel, eine zufällige Installations-ID, die Plugin-ID und grundlegende Browser-Metadaten (Browser-Version, Sprache, Zeitzone, User-Agent).
- **Nicht erfasst:** Seiteninhalte, Browserverlauf, Warenkorbinhalte, Zahlungsdaten, Tastatureingaben oder Analysedaten.

Es gibt kein Konto, keine Werbung und keinen Datenverkauf. Die Deinstallation der Erweiterung entfernt lokale Daten; serverseitige Lizenzdatensätze können durch vorheriges Deaktivieren der Lizenz entfernt werden.

Die vollständige Richtlinie findest du unter [privacy-policy.html](../privacy-policy.html).

---

## Berechtigungen

| Berechtigung | Warum sie benötigt wird |
|------------|------------------|
| `storage` | Einstellungen, Timer und Statistiken lokal speichern; für Premium synchronisieren |
| `alarms` | Den Countdown genau halten und Sperren pünktlich freigeben |
| `notifications` | Eine lokale Desktop-Benachrichtigung zeigen, wenn eine neue Sperre startet |
| `host_permissions: <all_urls>` | Einen Checkout-Button auf jedem Shop erkennen, da Shops beliebige Domains nutzen |
| `host_permissions: api.annmax1983.com` | Eine optionale Premium-Lizenz aktivieren und validieren |

Das Content-Skript läuft in allen Frames, um Checkout-Buttons in Shopfront-Widgets zu erwischen, aber Zahlungsanbieter-Hosts sind ausdrücklich ausgenommen.

---

## Sprachen

English, 简体中文, 日本語, Deutsch, Español und Français. Oberfläche, eingebaute Zitate und Shop-Beschreibungen sind lokalisiert.

---

## Lizenz

VKT Cart Lock ist eine kommerzielle Erweiterung. Die kostenlose Stufe ist ohne Lizenz nutzbar. Premium-Funktionen erfordern einen aktiven Lizenzschlüssel von [annmax1983.com](https://www.annmax1983.com/).
