# Spickzettel Wund-AI · 8 Stunden

Acht Blöcke. Jeden Prompt in Claude Code kopieren, das Ergebnis prüfen, dann weiter. Wer schneller ist, überspringt die Prompts und baut frei, die „Fertig, wenn“-Punkte gelten trotzdem.

| Block | Zeit | Thema |
|---|---|---|
| 1 | 30 Min. | Setup |
| 2 | 45 Min. | Medizinische Vorgaben |
| 3 | 60 Min. | Foto-Upload mit Vorschau |
| 4 | 60 Min. | KI-Anbindung |
| 5 | 75 Min. | Strukturierter Befund mit Ampel |
| 6 | 75 Min. | Testen und Prompt verbessern |
| 7 | 45 Min. | Robustheit |
| 8 | 60 Min. | Ergebnis, Demo, Pitch |

Bleiben 30 Minuten Puffer.

## Block 1 · Setup
Schlüssel eintragen: `.env.example` zu `.env` kopieren und den ausgehändigten Schlüssel eintragen (im Texteditor, nicht über Claude Code).
```
Lies README.md und CLAUDE.md. Prüfe, ob Node.js ab Version 20 installiert ist, und lege die leeren Ordner testbilder, prompt und ergebnisse an. Sag mir in drei Sätzen, was als Nächstes kommt.
```
**Fertig, wenn:** Node passt, `.env` existiert, Ordner sind da.

## Block 2 · Medizinische Vorgaben (ohne Code)
Das Medizin-Team schreibt in `spec.md`, was die App sagen darf:
- Definition der Grade 1, 2a, 2b, 3 mit sichtbaren Zeichen (mit Quelle)
- Ampel: Wann ROT, GELB, GRÜN, GRAU („nicht beurteilbar“)?
- Was die App nie tut (keine Therapieempfehlung, keine Medikamente)
- Über- oder Untertriage: Was ist im Zweifel die sichere Seite?

**Fertig, wenn:** `spec.md` von zwei Personen gegengelesen ist.

## Block 3 · Foto-Upload mit Vorschau
```
Baue die Grundversion: server.js und public/index.html. Ein großer Button „Wunde fotografieren / Bild wählen“, danach Vorschau mit den Buttons „Analysieren“ und „Anderes Bild“. Verkleinere das Bild im Browser auf höchstens 1600 Pixel Kantenlänge (JPEG). Der Hinweis aus CLAUDE.md ist immer sichtbar. Zeige beim Start die Adresse für den Laptop und für Handys im selben WLAN. Starte den Server und prüfe, dass die Seite erreichbar ist.
```
**Fertig, wenn:** Bild wählen und Vorschau funktionieren auf Laptop und Handy.

## Block 4 · KI-Anbindung
```
Binde die KI an: neuer Endpunkt POST /api/analyse, der das Bild an die Anthropic Messages API schickt. Den System-Prompt liest der Server bei jeder Anfrage frisch aus prompt/system.md. Lege diese Datei an mit: „Du bewertest Fotos von Verbrennungswunden für einen Prototyp. Beschreibe, was du siehst, und schätze den Grad ein.“ Schlüssel und Modell kommen nur aus .env. Zeige die Antwort zunächst als Rohtext. Fehler erscheinen als kurze deutsche Meldung.
```
**Fertig, wenn:** ein Testbild eine Antwort liefert und der Schlüssel nirgends in `public/` steht.

## Block 5 · Strukturierter Befund mit Ampel
```
Stelle die Ausgabe auf JSON um mit den Feldern: beurteilbar (ja/nein), grad, begruendung, sichtbare_zeichen, unsicherheiten, ampel, konfidenz. Übernimm die Grad- und Ampel-Definitionen WORTGETREU aus spec.md in prompt/system.md. Zeige oben einen breiten Ampelbalken (Farbe plus Text), darunter Grad und Begründung. Bei ungültiger Antwort einmal wiederholen. Mit ?demo=1 zeigt die Seite drei feste Beispielbefunde ohne Netz.
```
**Fertig, wenn:** Ampel ohne Scrollen sichtbar ist und der Demo-Modus läuft.

## Block 6 · Testen und Prompt verbessern
1. Die Bilder aus `daten/testbilder/` in den Ordner `testbilder` kopieren. Drei davon beiseitelegen (Blind-Fälle). Herkunft und Grenzen der Bilder stehen in `daten/QUELLEN.md`.
2. Tabelle anlegen: Bild, erwarteter Grad, KI-Grad, Bewertung.
```
Baue testlauf.js: schickt alle Bilder aus testbilder durch dieselbe Auswertung und schreibt eine CSV nach ergebnisse/ mit Datei, KI-Grad, Ampel, Konfidenz und einer leeren Spalte Bewertung. Bewerte nichts selbst.
```
3. Pro Durchlauf nur **eine** Prompt-Änderung, dann erneut testen.

**Fertig, wenn:** drei Testläufe dokumentiert sind und ein Bild ohne Wunde als GRAU endet.

## Block 7 · Robustheit
```
Mache die App robuster, ohne prompt/system.md zu ändern: zu kleine oder zu dunkle Bilder ablehnen, verständliche Meldungen bei fehlendem Netz und Zeitüberschreitung mit Button „Erneut versuchen“, Ladeanzeige mit Sekunden, kein Doppelklick während der Analyse.
```
**Fertig, wenn:** nie eine leere Seite erscheint.

## Block 8 · Ergebnis, Demo, Pitch
- Blind-Fälle **einmal** laufen lassen, Ergebnis nicht nachbessern
- `ergebnis.md`: Aufbau, Zahlen, Limitationen (kleine Fallzahl, Bildherkunft, keine Klinik)
- Demo zweimal durchspielen, Screenshots als Backup
- Pitch: Problem, Live-Demo, wie getestet, nächste Schritte

Nur Aussagen wie „bei 3 Blindfällen …“, nie „erkennt zuverlässig“.
