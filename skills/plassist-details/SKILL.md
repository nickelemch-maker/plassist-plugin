---
name: plassist-details
description: Fester Ablauf für Details 1:10 in Archicad mit Plassist, zuerst für Fensterdetails (Vertikal- und Horizontalschnitt). Verwenden bei «Detail», «Fensterdetail», «Anschlussdetail», «Detail 1:10», «Brüstung/Sturz/Leibung zeichnen».
---

# Plassist: Details 1:10, zuerst Fensterdetails

Ein Detail ist Werkplan-Arbeit, keine Skizze. Es muss baubar und fachlich richtig sein. Plassist zeichnet ein Detail darum nie aus dem Stand, sondern immer nach diesem Ablauf. Zuerst den Skill `plassist-arbeitsweise` lesen, dazu `planregeln_lesen` Abschnitte «Fenster» und «Details 1:10».

## 1. Auftrag klären (Pflicht, vor jeder Zeichnung)

Was aus dem Modell lesbar ist, selbst lesen. Nur fragen, was fehlt, alles in einer Nachricht, mit Vorschlag.

| Angabe | Woher | Werkzeug |
|---|---|---|
| Welches Fenster, welcher Schnitt (vertikal: Brüstung/Sturz; horizontal: Leibung) | Nutzer | `fenster_tueren_details` (Element-ID) |
| Wandaufbau mit allen Schichten und Dicken | Modell (Wand-Composite) | `waende_auflisten`, Tapir-Eigenschaften der Wand |
| Bauweise: Kompaktfassade, hinterlüftet, Zweischalen, Holzrahmen, Beton | Modell, sonst fragen | Lexikon OE-001 bis OE-005 |
| Einbaulage und Anschlag (aussenbündig Kern, in Dämmebene, Abstand) | Fensterobjekt | `fenster_tueren_details` |
| Rahmenmaterial und Bautiefe (Holz 68, Kunststoff 76, Holz-Metall 84–105) | fragen, sonst Vorschlag Holz-Metall | Lexikon OE-020 |
| Fensterbank aussen (Metall, Gefälle, Tropfkante) und Sims innen | Fensterobjekt, sonst Regel | Lexikon OE-007 bis OE-010 |
| Sturz und Storen (Betonsturz, Storenkasten, Nischenhöhe) | Modell und Fensterobjekt | Lexikon OE-011 bis OE-013, OE-015 |
| Boden- und Deckenaufbau, Höhenkoten roh und fertig | Modell (Platten, Geschosse) | Tapir-Eigenschaften der Decke |
| Vorbild | Büro-Musterplan oder Lexikon-Eintrag | `musterplaene_auflisten`, `lexikon_lesen` |

Dann den Auftrag in drei Sätzen zusammenfassen, zum Beispiel: «Vertikalschnitt durch Fenster F12 im OG, Kompaktfassade Backstein 175 + EPS 200, Fenster Holz-Metall aussenbündig am Kern mit 3 cm Überdämmung, Alu-Fensterbank 5° mit Tropfkante 3 cm, Betonsturz mit Raffstorenkasten 31 cm. Vorbild OE-001, OE-008, OE-013. Passt das?» Erst nach dem Ja weiter.

Fehlt eine wichtige Angabe und der Nutzer will nicht entscheiden, den Wert aus dem Lexikon nehmen und im Detail als Annahme kennzeichnen.

## 2. Fachliche Prüfliste Fensterdetail (vor der Vorschau abhaken)

Jeder Punkt muss im Detail sichtbar und richtig sein. Was fehlt, nicht weglassen, sondern zeichnen oder als offen melden.

**Vertikalschnitt unten (Brüstung)**
- Rahmen unten ohne Anschlag, auf Tragklötzen, darunter das Fensterbankanschlussprofil.
- Aussen: Sekundärabdichtung unter der Fensterbank, am Rahmen hochgezogen. Fensterbank mit 5° Gefälle nach aussen, Tropfkante mindestens 30 mm vor der fertigen Fassade, seitliche Borde.
- Innen: Sims auf der Brüstung, Luftdichtband zwischen Rahmen und Kern. Sims tiefer als 12 cm und tiefer als 65 cm über Boden ist begehbar (Absturzsicherung ab OK Sims).
- Brüstungshöhe ab OK fertig Boden bemasst.

**Vertikalschnitt oben (Sturz)**
- Sturz tragend (Betonsturz, Decke oder Sturzbrett), innen bündig mit dem Kern.
- Storenkasten in der Dämmebene, nicht innen. Nischenhöhe nach Lichthöhe (z. B. LH 1.50 ergibt 31 cm), Tiefe mindestens 120 mm. Dämmung hinter und über dem Kasten.
- Aussen durchgehend gedämmt, kein Kern sichtbar an der Fassade.

**Horizontalschnitt (Leibung)**
- Anschlag 4 cm am Kern, Rahmen aussenbündig Kern (Kompaktfassade), Dämmung überdeckt den Rahmen 20–30 mm.
- In Betonwänden kein gestufter Anschlag.
- Storenführungsschiene im Kern befestigt, nie nur in der Dämmung.
- Fuge in drei Ebenen: innen luftdicht, Mitte gedämmt, aussen schlagregendicht und diffusionsoffen. Aussen Fensteranschlussprofil zum Putz.

**Rahmen und Glas**
- Blendrahmen, Flügel und Glas (3-fach) mit richtiger Bautiefe, nicht als ein Rechteck.

**Darstellung nach den Planregeln (Details 1:10)**
- Je Detail ein Arbeitsblatt, Massstab 1:10 setzen (`zeichnungsmassstab`), bevor Texte und Masse entstehen.
- Schraffuren nach SIA 400. Dämmung quer zur Schicht schraffiert.
- Strichstärken: Aussenkontur Stift 4, tragende Schichten Stift 3, Fugen Stift 1, Abdichtungen Stift 3.
- Beschriftung nur mit dem Etikett-Werkzeug. Aufbau-Blöcke rechts, Zeiger kreuzen sich nicht, Etiketten ausserhalb der Schraffuren.
- Alle Schichtdicken als Kette, dazu Brüstung, Sturz, Überstand Fensterbank, Höhenkoten roh (gefüllt) und fertig (leer) mit dem Bemassungswerkzeug.

## 3. Vorschau, Freigabe, Zeichnen, Prüfen

1. **Vorschau als Bild** (PNG) mit allen Schichten, Massen und Beschriftungen. Darunter die Prüfliste aus Abschnitt 2 mit Haken oder «offen». Nichts in Archicad schreiben.
2. Nach der Freigabe ins Arbeitsblatt zeichnen (`sitzung=` mitgeben).
3. **Zurücklesen** und mit der Vorschau vergleichen, `plangrafik_pruefen` mit massstab=10, Bild mit `fenster_als_bild` (voller Dateiname `.png`).
4. Die Prüfliste nochmals am fertigen Bild durchgehen und dem Nutzer melden, was offen oder angenommen ist.
5. Nicht speichern, bis der Nutzer es sagt.

## Grenzen offen sagen

- Herstellerprofile (Rahmen, Storen) sind schematisch. Für die Ausführung gelten die Herstellerdetails.
- Ohne Wandaufbau im Modell und ohne Angaben des Nutzers kein Detail zeichnen, sondern nachfragen.
- Andere Details (Küche, Möbel, Sockel, Dachrand) nach dem gleichen Muster: zuerst Auftrag klären mit den Angaben aus dem Lexikon, dann Vorschau. Für Küchen- und Möbelpläne braucht es Fronten, Masse und Geräteliste vom Nutzer.
