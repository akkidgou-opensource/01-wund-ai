# Datenquellen Wund-AI

## Im Repo
| Ordner | Inhalt | Herkunft und Lizenz |
|---|---|---|
| `testbilder/` | 12 Fotos von Verbrennungen (Hand, Fuß, Schulter, Unterarm), ohne Gesichter, Dateinamen ohne Hinweis auf den Grad | Wikimedia Commons. Lizenz je Bild verschieden (CC0, CC BY, CC BY-SA, gemeinfrei). |
| `testbilder/referenz.csv` | Je Bild: Grad laut Beschreibung der Quelle, Originaltitel, Urheber, Lizenz, Link | automatisch aus den Angaben bei Wikimedia Commons erzeugt |

**Wichtig:**
- Die Gradangaben stammen von den Personen, die die Fotos hochgeladen haben, meist medizinische Laien. Sie sind nicht ärztlich bestätigt. Das Medizin-Team bewertet am Bild.
- Die Auswahl ist unausgewogen: fast nur Grad 2, ein Bild Grad 3, kein reines Grad-1-Bild. Für einen fairen Test braucht es mehr Bilder, siehe unten.
- Bei Weitergabe eines Bildes Urheber und Lizenz aus `referenz.csv` nennen. Bilder unter CC BY-SA dürfen nur unter derselben Lizenz weitergegeben werden.

## Weitere offene Quellen (nur verlinkt)
| Quelle | Inhalt | Lizenz laut Anbieter | Hinweis |
|---|---|---|---|
| [Roboflow: burn wound classification](https://universe.roboflow.com/binussss/burn-wound-classification) | ca. 3.700 Fotos mit Gradangabe | CC BY 4.0 | Download braucht ein kostenloses Roboflow-Konto. Herkunft der Bilder und Einwilligung der abgebildeten Personen sind unklar. |
| [Roboflow: skin burn wound classification](https://universe.roboflow.com/binus-if3z9/skin-burn-wound-classification) | ca. 3.700 Fotos mit Gradangabe | CC BY 4.0 | Vermutlich derselbe Bildbestand. |
| [Zenodo 10.5281/zenodo.18870162](https://doi.org/10.5281/zenodo.18870162) | Code und trainierte Modelle zur Unterscheidung von Grad 2 und 3 | MIT | Enthält keine Bilder (geprüft), nur Modelle und Auswertungen. |
| [Wikimedia Commons, Suche „burn“](https://commons.wikimedia.org/wiki/Category:Burns) | Weitere Einzelfotos | je Bild verschieden | Sehr gemischt, enthält auch historische und belastende Aufnahmen. Nur einzeln auswählen. |

## Empfehlung für den Hackathon
- Drei Bilder als Blind-Fälle beiseitelegen, bevor ihr mit dem Verbessern beginnt.
- Zwei Kontrollen selbst fotografieren: gesunde Haut und ein Foto ohne Wunde. Erwartet wird „nicht beurteilbar“.
- Keine eigenen Patientenfotos verwenden.
