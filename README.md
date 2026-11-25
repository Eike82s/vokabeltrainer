# Vokabeltrainer

Mobile Lern-App als einzelne HTML-Seite (PWA): läuft im Browser, lässt sich auf den Homescreen legen und funktioniert offline.

## Hosten mit GitHub Pages
1. Alle Dateien dieses Ordners ins Repo legen (Wurzel oder Ordner `docs/`).
2. Auf GitHub: Settings → Pages → Branch `main`, Ordner `/` (bzw. `/docs`) wählen.
3. Nach ca. einer Minute läuft die App unter `https://<name>.github.io/<repo>/`.
4. Auf dem Handy öffnen → „Zum Home-Bildschirm“.

## Vokabellisten
- Neue Liste als `.csv` in `decks/` ablegen, eine Vokabel pro Zeile: `Deutsch; Englisch`
- In `decks/index.json` eintragen: `{"file": "unit3.csv", "name": "Englisch Unit 3", "la": "Deutsch", "lb": "Englisch"}`
- Mehrere richtige Antworten mit `/` trennen (`about/approximately`), optionale Teile in Klammern (`(sich) erinnern`).
- Zeilen mit `#` am Anfang sind Kommentare.
- Listen lassen sich auch direkt in der App einfügen (bleiben dann nur auf dem Gerät).

## Ablauf und Score
- Runde 1: alle Vokabeln in beide Richtungen, gemischt
- Runde 2: alles, was in Runde 1 nicht sofort richtig war
- Runde 3: die Fehler aus Runde 2
- Score je Aufgabe: 1 sofort richtig · 3 im zweiten Versuch · 5 zweimal falsch · 10 „Ich weiß es nicht“

## Daten
Profile, Statistik und eigene Listen liegen im `localStorage` des Browsers. Unter „Statistik“ als JSON exportieren/importieren.
