# Nextcloud Hub installieren mit Docker: Komplette Anleitung für VPS-Setup, Verwaltung und Selbsthosting — lohnt sich der Videokurs?

Drei Stunden. So lange saß ich beim ersten Versuch, Nextcloud auf einem VPS zum Laufen zu bringen — und am Ende funktionierte SSL nicht, der Reverse Proxy spielte verrückt, und die Admin-Oberfläche warf Fehler, die ich nicht verstand. Wer Nextcloud Hub installieren möchte, stößt schnell an eine Grenze: Die Dokumentation ist ausführlich, aber zerstückelt. Zwischen offizieller Nextcloud-Doku, Forenbeiträgen und veralteten Blog-Tutorials bleibt man oft allein.

Genau das ist der Ausgangspunkt dieses Artikels — und der Grund, warum Videokurse für Nextcloud gerade so stark nachgefragt werden.

## Was ist Nextcloud Hub eigentlich?

**Nextcloud Hub** ist eine Open-Source-Plattform für selbstgehosteten Cloud-Speicher und kollaboratives Arbeiten. Sie umfasst Dateisynchronisation, Kalender, Kontakte, Online-Dokumentbearbeitung, Videochats über Nextcloud Talk und eine KI-Integration — alles unter eigener Kontrolle, ohne Abhängigkeit von Google Drive oder Dropbox.

**Nextcloud Hub All-in-One (AiO)** ist die offizielle Docker-basierte Installationsmethode, die seit Nextcloud Hub 4 empfohlen wird. Sie bündelt alle notwendigen Container (Nextcloud, Datenbank, Redis, Backup, Collabora) in einem einzigen Setup. Ein Befehl, ein Stack.

Das ist der entscheidende Unterschied zur klassischen Installation. Keine manuellen Datenbankeinrichtungen mehr, kein PHP-Chaos, kein Rätseln über fehlende Abhängigkeiten.

## Warum Nextcloud selbst hosten — und warum es ohne Anleitung trotzdem schmerzt

Das Argument fürs Selbsthosten ist schnell gemacht: volle Datenkontrolle, DSGVO-Konformität, keine monatlichen Abo-Kosten bei einem Cloud-Anbieter. Europäische Behörden setzen bereits auf Nextcloud, und laut dem Nextcloud-Blog nutzen weltweit über 400.000 Server-Instanzen die Plattform.

Dann kommt die Realität. Ein VPS ist schnell gemietet — bei Hetzner gibt es brauchbare Instanzen ab 4 Euro im Monat. Docker installieren ist in zehn Minuten erledigt. Aber dann?

Wer noch nie einen Reverse Proxy konfiguriert hat, stolpert beim Nextcloud-AiO-Setup über die Subdomain-Einrichtung. Wer kein Linux-Hintergrundwissen hat, weiß nicht, wie man BorgBackup sinnvoll einrichtet. Wer die Admin-Oberfläche zum ersten Mal aufruft, sieht Dutzende Einstellungen ohne klaren Einstiegspfad.

Das ist der Punkt, an dem strukturiertes Lernen echten Wert hat.

## Der Videokurs: Nextcloud HUB All-in-One von video-schulungen.de

Der Kurs **"Nextcloud HUB – All-in-One"** von ist ein deutschsprachiger Videokurs, der speziell für dieses AiO-Setup entwickelt wurde. Anbieter ist Trainstitute, eine österreichische E-Learning-Plattform, die sich auf IT-Schulungen und Mitarbeiterweiterbildung spezialisiert hat.

Was den Kurs von einer YouTube-Playlist unterscheidet: Er hat eine Struktur. Vom ersten Schritt bis zur produktiven Umgebung folgt alles einer logischen Reihenfolge — ohne Sprünge, ohne dass man selbst zwischen vier Tabs recherchieren muss.

### Was der Kurs abdeckt

Der Lehrplan ist aufgeteilt in drei Hauptbereiche:

**Installation und Serverkonfiguration** — Nextcloud AiO wird per Docker auf einem VPS mit kostenloser DuckDNS-Subdomain eingerichtet. Themen wie Sicherheitswarnungen in der Admin-Oberfläche (Phone Region, E-Mail-Server), Ressourcenüberwachung, Passwortverwaltung, Backup und Wiederherstellung mit BorgBackup und der Nextcloud-Sicherheitsscanner werden Schritt für Schritt erklärt.

**Nextcloud Verwaltung** — Dieser Abschnitt geht tief: Grundeinstellungen, Sharing-Konfiguration, Designanpassung, die KI-Integration, Groupware, Adminrechte, Volltextsuche mit Elasticsearch, Abläufe (Workflows), Talk- und Office-Einstellungen, Nutzungsberichte, Update-Verwaltung, Swap-Einrichtung unter Linux.

**Anwender-Abschnitt** — Benutzer und Gruppen anlegen, Dashboard, Client-Installation unter macOS und Windows 10/11, Kalender- und Kontaktsynchronisation per CalDAV/CardDAV, mobile Nutzung mit iOS und Android.

Das sind insgesamt mehr als 35 Lektionen — von "Was ist neu in Nextcloud Hub 6?" bis zur Fehlersuche im Forum und auf GitHub.

## Schritt-für-Schritt: So läuft die Nextcloud-AiO-Installation ab

Wer sich fragt, was genau beim Nextcloud Hub installieren passiert — hier der grobe Ablauf, wie er auch im Kurs behandelt wird:

1. **VPS bereitstellen** — einen Root-Server mit Ubuntu 22.04 oder 24.04 mieten (2 GB RAM Minimum, 4 GB empfohlen); öffentliche IPv4-Adresse notieren.

2. **Docker installieren** — offizieller Docker-Installationspfad über das apt-Repository; Docker Compose als Plugin einrichten.

3. **Domain konfigurieren** — eine kostenlose Subdomain bei DuckDNS anlegen und den DNS-Eintrag auf die Server-IP zeigen lassen.

4. **Nextcloud AiO starten** — mit einem einzigen `docker run`-Befehl den AiO-Master-Container starten; über den Browser auf Port 8080 aufrufen.

5. **AiO-Passphrase sichern** — die generierte Passphrase zwingend notieren; sie dient zur Wiederherstellung.

6. **Subdomain und Containerkonfiguration** — im AiO-Interface die eigene Domain eintragen, optionale Container (Collabora, Talk, Backup) aktivieren.

7. **Sicherheitseinstellungen** — Zwei-Faktor-Authentifizierung einrichten, Phone Region konfigurieren, serverseitige Verschlüsselung aktivieren.

8. **Backup einrichten** — BorgBackup-Ziel definieren (lokaler Pfad oder SFTP-Remote-Ziel), automatische Backup-Zeitpläne festlegen.

Jeder dieser Schritte hat seine eigenen Stolpersteine. Der Kurs zeigt, wo sie liegen — bevor man in sie hineintritt.

## Für wen ist der Kurs geeignet?

Ehrlich gesagt gibt es zwei Gruppen, die hier klar profitieren.

Die erste Gruppe: **IT-nahe Anwender ohne Admin-Vollausbildung**. Jemand, der Linux-Grundkenntnisse hat und ein bisschen mit der Kommandozeile umgehen kann, aber noch nie einen produktiven Server selbst aufgesetzt hat. Für diese Person ist der Kurs eine echte Abkürzung.

Die zweite Gruppe: **Systemadministratoren, die Nextcloud noch nicht kennen**. Wer täglich mit Linux-Servern arbeitet, wird manche Basiskapitel überspringen — aber der Verwaltungsabschnitt mit Elasticsearch-Volltextsuche, Workflow-Automatisierung und Talk-Konfiguration liefert auch hier konkreten Mehrwert.

Für absolute Linux-Einsteiger, die noch nie einen Terminal geöffnet haben: Der Kurs setzt ein Mindestmaß an technischem Verständnis voraus. Man wird nicht bei null abgeholt.

## Preisübersicht: Der Kurs im Detail

Es gibt genau ein Angebot — kein Abo, kein Monatsmodell, kein Preistierkaos.

| Kurs | Inhalt | Preis | Zugang |

|---|---|---|---|

| Nextcloud HUB – All-in-One | 35+ Lektionen, Installation, Verwaltung, Anwender | 99,00 € | Einmalzahlung, dauerhafter Zugang |

Das entspricht weniger als 2,85 € pro Lektion — für eine Plattform, bei der ein einziger Fehler in der Konfiguration Stunden kosten kann.

## Nextcloud Hub installieren: Was Anfänger unterschätzen

Es gibt ein paar Dinge, über die fast niemand spricht, der Nextcloud-Tutorials schreibt — weil sie offensichtlich klingen, bis man selbst daran hängt.

**Reverse Proxy ist kein optionales Extra.** Nextcloud AiO setzt voraus, dass Port 443 korrekt geroutet wird. Wer das nicht versteht, bekommt SSL-Fehler, die aussehen wie Installationsfehler. Der Kurs behandelt die Einrichtung der kostenfreien DuckDNS-Domain explizit, damit diese Hürde nicht zum Showstopper wird.

**Backups müssen vor dem ersten Datenverlust eingerichtet werden.** Das klingt trivial. Trotzdem sind Nextcloud-Foren voll mit Beiträgen von Leuten, die beim Update etwas kaputtgemacht haben — und kein Backup hatten. BorgBackup ist in AiO integriert, aber man muss es aktiv konfigurieren.

**Updates laufen nicht automatisch durch.** Nextcloud verlangt bei Major-Updates manuelle Bestätigung über die AiO-Oberfläche. Wer das nicht weiß und einfach auf "Update" klickt ohne Backup, lebt gefährlich.

## Nextcloud vs. Alternativen: Was spricht für den eigenen Server?

Eine kurze Einordnung, weil die Frage immer wieder auftaucht.

**Nextcloud vs. managed Cloud (z.B. Hetzner Storage Box, Strato HiDrive):** Bei verwalteten Angeboten zahlt man dauerhaft Monatsgebühren und gibt Kontrolle ab. Bei Nextcloud auf eigenem VPS: einmalig einrichten, dann laufende Serverkosten von ca. 4–8 € pro Monat — und volle Kontrolle über Daten und Funktionen.

**Nextcloud vs. ownCloud:** Nextcloud ist ein Fork von ownCloud aus 2016 und hat die aktivere Community und mehr kostenlose Apps. ownCloud gibt es weiterhin in einer kommerziellen Enterprise-Edition. Für die meisten Privatanwender und KMUs ist Nextcloud heute die erste Wahl.

**Nextcloud vs. Seafile:** Seafile ist schneller bei der reinen Dateisynchronisation, bietet aber keine vergleichbare App-Ökosystem-Tiefe. Wer auch Kalender, Kontakte, Office und Videochats unter einer Plattform will, ist bei Nextcloud besser aufgehoben.

## Häufig gestellte Fragen zum Nextcloud Hub installieren

**Kann ich Nextcloud Hub kostenlos installieren?**

Ja. Nextcloud selbst ist Open-Source und kostenlos. Du brauchst nur einen Server — ein VPS ab ca. 4 €/Monat reicht für den Anfang. Die Kosten entstehen durch den Server, nicht durch die Software.

**Was brauche ich, um mit dem Kurs zu starten?**

Einen gemieteten VPS (Ubuntu 22.04 oder 24.04), eine Domain oder DuckDNS-Subdomain, und grundlegendes Linux-Wissen — also wissen, wie man sich per SSH einloggt und Befehle ausführt. Tiefere Linux-Kenntnisse sind nicht vorausgesetzt.

**Funktioniert die AiO-Installation auch auf einem Raspberry Pi?**

Technisch ja, aber nicht empfohlen für produktiven Betrieb. Die Ressourcenanforderungen von AiO mit allen aktivierten Containern (inklusive Collabora Office) überfordern einen Raspberry Pi 4 schnell. Ein kleiner VPS ist die bessere Wahl.

**Wie lange dauert die Einrichtung von Nextcloud AiO komplett?**

Bei guter Vorbereitung und ohne unerwartete Fehler: 2–4 Stunden für Installation, Grundkonfiguration und Backup-Einrichtung. Der erste Durchlauf dauert länger. Wenn man weiß, was man tut: unter einer Stunde.

**Bekomme ich dauerhaften Zugang zum Kurs?**

Ja. Es handelt sich um eine einmalige Zahlung ohne Abo. Der Zugang zu allen Lektionen und zukünftigen Updates des Kurses bleibt bestehen.

**Ist der Kurs auf dem aktuellen Stand von Nextcloud Hub 6?**

Eine der Einführungslektionen behandelt explizit die Neuerungen in Nextcloud Hub 6. Der Kurs wird gepflegt und aktualisiert.

---

Selbsthosten ist keine Raketenwissenschaft — aber es ist auch kein Klick-und-Vergessen. Wer Nextcloud Hub installieren möchte und dabei nicht tagelang in Forensuchen stecken will, spart mit einem strukturierten Kurs schlicht Zeit. Und Zeit ist meistens das knappste Gut von allen. Den Kurs mit allen Lektionen zu Installation, Verwaltung und Anwendung gibt es auf [video-schulungen.de](https://www.digistore24.com/redir/489854/daninonicolesd9d7/).
