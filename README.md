# Vokabeltrainer

Mobile Lern-App als einzelne HTML-Seite (PWA): läuft im Browser, lässt sich auf den Homescreen legen und funktioniert offline.

## Hosten mit GitHub Pages
1. Alle Dateien dieses Ordners in ein **öffentliches** Repo legen.
2. Settings → Pages → Branch `main`, Ordner `/ (root)` → Save.
3. Nach 1–2 Minuten läuft die App unter `https://<name>.github.io/<repo>/`.
4. Auf dem iPhone in Safari öffnen → Teilen → „Zum Home-Bildschirm“.

## Bedienung
- **Lernen:** aktuelle Liste wählen, Abfragerichtung wählen, Run starten.
- **Listen:** neue Liste anlegen (eine Vokabel pro Zeile, `Deutsch; Englisch`), bearbeiten, archivieren, aus dem Archiv wiederherstellen oder endgültig löschen.
  - Mehrere richtige Antworten mit `/` trennen: `Nachbar; neighbour/neighbor`
  - Text in Klammern zählt nicht zur Antwort: `(sich) erinnern`
- **Statistik:** Auswertung, Sicherung (JSON) und Tabelle (CSV für Excel), Import einer Sicherung.

## Ablauf und Score
- Runde 1: alle Vokabeln in beide Richtungen, gemischt
- Runde 2: alles, was in Runde 1 nicht sofort richtig war
- Runde 3: die Fehler aus Runde 2
- Score: 1 sofort richtig · 3 im zweiten Versuch · 5 zweimal falsch · 10 „Ich weiß es nicht“
- Ein Tippfehler (1 Buchstabe) oder falsche Groß-/Kleinschreibung ergibt „Fast richtig“ und einen zweiten Versuch.

## Daten
Listen und Statistik liegen nur im Browser-Speicher (localStorage) des jeweiligen Geräts. Nichts wird an GitHub oder einen Server geschickt. Jedes Gerät hat seinen eigenen Stand.
