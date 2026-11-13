# Datenquellen Wund-AI

## Im Repo
| Ordner | Inhalt | Herkunft und Lizenz |
|---|---|---|
| `testbilder/` | Rund 35 Fotos von Verbrennungen und ähnlichen Hautschäden (Hand, Fuß, Schulter, Rücken, Unterarm), ohne Gesichter, Dateinamen ohne Hinweis auf den Grad | Wikimedia Commons. Lizenz je Bild verschieden (CC0, CC BY, CC BY-SA, gemeinfrei). |
| `testbilder/referenz.csv` | Je Bild: Grad laut Beschreibung der Quelle, Ursache (thermisch, Sonnenbrand, chemisch, Strom, Reibung, Blitz), Originaltitel, Urheber, Lizenz, Link | automatisch aus den Angaben bei Wikimedia Commons erzeugt |
| `kontrollbilder/gesund/` | 40 Fotos gesunder Füße und Unterschenkel | [Lower Limb and Feet Wound Image Dataset, Mendeley Data, doi:10.17632/hsj38fwnvr.3](https://doi.org/10.17632/hsj38fwnvr.3), CC BY 4.0 |
| `kontrollbilder/andere_wunden/` | 60 Fotos chronischer Wunden an Bein und Fuß, also Wunden, die **keine** Verbrennungen sind | wie oben |

## Was ihr über die Bilder wissen müsst
- **Gradangaben sind Laienangaben.** Sie stammen von den Personen, die ihre eigenen Verletzungen fotografiert und hochgeladen haben. Bei vielen Bildern fehlt der Grad ganz („nicht angegeben“). Das Medizin-Team bewertet am Bild.
- **Die Auswahl ist unausgewogen.** Viele Bilder zeigen Grad 2 oder Sonnenbrand, nur wenige Grad 1, ein einziges Grad 3. Tiefe Verbrennungen aus der Klinik fehlen, weil es dafür keine frei nutzbaren Fotos mit geklärter Einwilligung gibt.
- **Nicht jede Rötung ist eine Verbrennung.** Die Bilder mit chemischer Ursache, Reibung oder Blitz und der ganze Ordner `kontrollbilder/` sind dafür da, zu prüfen, ob eure App auch „keine Verbrennung“ oder „nicht beurteilbar“ sagen kann.
- **Kontrollbilder sind klein** (331 × 331 Pixel) und zeigen nur Füße und Unterschenkel.
- **Weitergabe:** Urheber und Lizenz aus `referenz.csv` nennen. Bilder unter CC BY-SA dürfen nur unter derselben Lizenz weitergegeben werden.

## Weitere offene Quellen (nur verlinkt)
| Quelle | Inhalt | Lizenz laut Anbieter | Hinweis |
|---|---|---|---|
| [Roboflow: burn wound classification](https://universe.roboflow.com/binussss/burn-wound-classification) | ca. 3.700 Fotos mit Gradangabe | CC BY 4.0 | Download braucht ein kostenloses Roboflow-Konto. Herkunft der Bilder und Einwilligung der abgebildeten Personen sind unklar, deshalb nicht im Repo. |
| [Zenodo 10.5281/zenodo.18870162](https://doi.org/10.5281/zenodo.18870162) | Code und trainierte Modelle zur Unterscheidung von Grad 2 und 3 | MIT | Enthält keine Bilder (geprüft). |
| [Wikimedia Commons, Kategorie „Burns“](https://commons.wikimedia.org/wiki/Category:Burns) | Weitere Einzelfotos | je Bild verschieden | Sehr gemischt, enthält auch historische und belastende Aufnahmen. Nur einzeln auswählen. |

## Empfehlung für den Hackathon
- Drei Verbrennungsbilder und zwei Kontrollbilder als Blind-Fälle beiseitelegen, bevor ihr mit dem Verbessern beginnt.
- Zuerst im Medizin-Team für jedes Testbild den erwarteten Grad festlegen und in eine eigene Spalte schreiben.
- Keine eigenen Patientenfotos verwenden.

## Bei Verwendung angeben
Für die Kontrollbilder: Islam MM. Lower Limb and Feet Wound Image Dataset for Medical Analysis. Mendeley Data, V3, 2026. doi:10.17632/hsj38fwnvr.3 (CC BY 4.0). Für die Testbilder: Angaben je Bild in `referenz.csv`.
