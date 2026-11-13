# Datenquellen Wund-AI

In diesem Ordner liegen bewusst **noch keine Bilder**. Die offenen Datensätze unten sind frei lizenziert, aber die Herkunft der Fotos (Einwilligung der abgebildeten Personen) ließ sich nicht prüfen. Bitte im Team entscheiden, was ihr verwendet.

| Quelle | Inhalt | Lizenz laut Anbieter | Hinweis |
|---|---|---|---|
| [Roboflow: burn wound classification](https://universe.roboflow.com/binussss/burn-wound-classification) | ca. 3.700 Fotos mit Gradangabe | CC BY 4.0 | Download braucht ein kostenloses Roboflow-Konto. Herkunft der Bilder unklar. |
| [Roboflow: skin burn wound classification](https://universe.roboflow.com/binus-if3z9/skin-burn-wound-classification) | ca. 3.700 Fotos mit Gradangabe | CC BY 4.0 | Vermutlich derselbe Bildbestand. |
| [Zenodo 10.5281/zenodo.18870162](https://doi.org/10.5281/zenodo.18870162) | Code und Modelle zur Klassifikation 2. gegen 3. Grad, Begleitmaterial zu einem Artikel im European Burn Journal 2026 | MIT | 170 MB. Ob die Bilder enthalten sind, bitte nach dem Download prüfen. |
| [Wikimedia Commons, Kategorie „Burns“](https://commons.wikimedia.org/wiki/Category:Burns) | Einzelne Fotos, Lizenz je Bild angegeben | je Bild verschieden | Sehr gemischt, enthält auch historische und belastende Aufnahmen. Nur einzeln auswählen. |

## Empfehlung für den Hackathon
- 10 bis 15 Bilder reichen: je 3 bis 4 pro Grad plus 2 Kontrollen (gesunde Haut, Foto ohne Wunde).
- Zu jedem Bild Quelle, Lizenz und erwarteten Grad in `testbilder/referenz.csv` notieren.
- Keine eigenen Patientenfotos verwenden.
- Die Gradangaben der Datensätze sind nicht ärztlich bestätigt. Das Medizin-Team bewertet am Bild.

## Bei Verwendung angeben
Name des Datensatzes, Urheber, Link und Lizenz (CC BY verlangt die Namensnennung).
