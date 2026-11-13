# 01 · Wund-AI

> Prototyp für den AKKI Hackathon 2026. Nur Testbilder, kein Medizinprodukt, kein Ersatz für ärztliche Beurteilung.

**Bereich:** Stationär

**Idee:** Wundfoto hochladen, die KI schätzt den Verbrennungsgrad ein.

## Warum
Die Einschätzung der Verbrennungstiefe hängt stark von der untersuchenden Person ab und ist für die Therapieentscheidung zeitkritisch.

## Was am Ende stehen soll
- Foto einer Wunde hochladen oder aufnehmen
- Grad-Einschätzung (1–3) mit kurzer Begründung
- Ampel-Ausgabe und jederzeit sichtbarer Hinweis „Prototyp“

**Erfolgskriterium:** Demo mit den vorhandenen Testbildern des Teams.

## So startet ihr
1. Oben auf **Code → Download ZIP** klicken und entpacken.
2. Im entpackten Ordner ein Terminal öffnen und `claude` eingeben.
3. `SPICKZETTEL.md` öffnen und mit Block 1 beginnen.

## Was in diesem Repo liegt
| Datei | Wofür |
|---|---|
| `SPICKZETTEL.md` | Umsetzungsplan für 8 Stunden, Block für Block |
| `CLAUDE.md` | Regeln, an die sich Claude Code hält |
| `daten/QUELLEN.md` | Offene Bildquellen mit Lizenz |

## Stolpersteine
- Wenig eigenes Bildmaterial verfügbar
- Beleuchtung und Bildqualität beeinflussen das Ergebnis stark
- Ein Foto zeigt nie die ganze Klinik (Rekapillarisierung, Sensibilität, Verlauf): Das gehört in die Limitationen

## Für Erfahrene
- Freie Modellwahl: Claude Vision oder ein anderes Bildmodell
- Zusätzlich die betroffene Körperoberfläche schätzen lassen
- Zwei Modelle auf denselben Testbildern vergleichen
