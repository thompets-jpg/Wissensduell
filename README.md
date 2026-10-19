# Wissensduell

Grundwissen-Quiz zum Gegeneinanderspielen, direkt im Browser. Keine Installation, keine Anmeldung, läuft auf Handy, Tablet und PC.

## Spielmodi

**Duell (2 Spieler):** Das Handy liegt flach zwischen beiden Spielern, jeder hat seine eigene Bildschirmhälfte. Nach der Frage werden die Antworten kurz darauf freigegeben. Wer zuerst richtig tippt, bekommt den Punkt. Wer falsch tippt, ist für diese Frage gesperrt.

**Reihum (2–6 Spieler):** Das Handy wird weitergegeben. Jeder bekommt eigene Fragen und 20 Sekunden Zeit. Eine richtige Antwort bringt 10 Punkte plus bis zu 10 Punkte Zeitbonus. Am Ende gibt es für jeden eine Schulnote.

Am PC spielt man das Duell auch per Tastatur: unten mit `1` bis `4`, oben mit `7`, `8`, `9` und `0`.

## Inhalt

157 Fragen in sechs Fächern:

| Fach | Kürzel |
|---|---|
| Erdkunde | `geo` |
| Geschichte | `ges` |
| Naturwissenschaft | `nat` |
| Sprache & Kunst | `kul` |
| Sport | `spo` |
| Mathe & Alltag | `all` |

Vor dem Spiel lassen sich Fächer und Anzahl der Fragen (10, 15 oder 20) auswählen. Fragen, die gerade erst dran waren, kommen so schnell nicht wieder.

## Online stellen mit GitHub Pages

1. Auf GitHub ein neues, **öffentliches** Repository anlegen, z. B. `wissensduell`.
2. **Add file → Upload files**, dann `index.html` und `README.md` hochladen und mit **Commit changes** bestätigen.
3. Im Repository **Settings → Pages** öffnen. Bei **Source** „Deploy from a branch“ wählen, Branch `main` und Ordner `/ (root)`, dann **Save**.
4. Nach ein bis zwei Minuten ist das Spiel erreichbar unter
   `https://DEIN-NAME.github.io/wissensduell/`

Tipp: Den Link auf dem Handy öffnen und „Zum Home-Bildschirm hinzufügen“, dann startet das Quiz wie eine App.

## Eigene Fragen hinzufügen

Alle Fragen stehen in `index.html` in der Liste `Q`. Jede Zeile hat dieses Format:

```js
['geo','Was ist die Hauptstadt von Australien?','Canberra','Sydney','Melbourne','Perth'],
```

1. Fach-Kürzel (siehe Tabelle oben)
2. Frage
3. **richtige Antwort** (immer an dieser Stelle)
4. bis 6. drei falsche Antworten

Die Reihenfolge der Antworten wird beim Spielen automatisch gemischt. Innerhalb der Texte keine geraden Apostrophe (`'`) verwenden, sonst bricht die Zeile. Typografische Anführungszeichen wie „so“ sind kein Problem.

## Technik

- Eine einzige HTML-Datei, kein Build-Schritt, keine Bibliotheken.
- Einstellungen und zuletzt gespielte Fragen werden nur lokal im Browser gespeichert.
- Die Schriften (Bricolage Grotesque, Atkinson Hyperlegible) werden von Google Fonts geladen. Wer das nicht möchte, löscht die drei `<link>`-Zeilen zu `fonts.googleapis.com` und `fonts.gstatic.com` im Kopf der Datei. Dann werden die Systemschriften verwendet.
- Hell- und Dunkelmodus folgen automatisch der Einstellung des Geräts.
