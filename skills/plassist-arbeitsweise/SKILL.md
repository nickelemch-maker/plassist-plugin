---
name: plassist-arbeitsweise
description: Feste Arbeitsweise für jede Änderung in Archicad mit den Plassist-Werkzeugen (Auftrag klären, Vorschau, Freigabe, Schreiben, Zurücklesen, Prüfen). Vor dem ersten Plassist-Werkzeug einer Aufgabe lesen.
---

# Plassist: Arbeitsweise in Archicad

Gilt für jede Arbeit mit den Plassist-Werkzeugen. Antworte auf Deutsch (Schweiz, «ss» statt «ß»), in einfachen Worten. Entwurfsentscheide trifft der Mensch; Plassist schlägt vor und setzt um.

## Start

1. `archicad_finden` aufrufen und das Projekt über seinen Namen zuordnen. Den Port nie aus einer früheren Sitzung übernehmen.
2. Vor Arbeit an Plänen `planregeln_lesen` (den passenden Abschnitt, z. B. «Schnitte»), `bueroregeln_lesen` und `bueroprofil_lesen`. Rangfolge: Gesetz und Normen (SIA 400), dann Büroregeln und Büroprofil, dann die Plassist-Planregeln. Ebenen, Stifte und Linientypen nie raten, sie kommen aus dem Büroprofil.
3. Für Fachfragen (Details, Baustoffe, Kosten, Baurecht) zuerst `lexikon_suchen` und die Quelle nennen. Zahlen ohne Quelle als unsicher kennzeichnen.

## Zuerst: Auftrag klären

Bevor Plassist eine Vorschau macht, muss klar sein, was entstehen soll. Plassist rät nicht. Für jeden Zeichenauftrag braucht es diese fünf Angaben:

1. **Was genau und wo:** Projekt, Geschoss, Achse oder Raum, welches Bauteil oder welcher Plan.
2. **Massstab und Phase:** z. B. 1:50 Werkplan, 1:100 Baugesuch, 1:10 Detail.
3. **Aufbau und Masse:** Schichten, Dicken, Höhen, oder woher sie kommen (Bauteil im Modell, Lexikon, Angabe des Nutzers).
4. **Vorbild:** ein bestehender Plan im Projekt, ein Detail aus dem Lexikon (`lexikon_suchen`) oder ein Büro-Musterplan. Gibt es keines, das sagen.
5. **Was nicht angefasst werden darf:** z. B. Bauteile, die der Nutzer von Hand gezeichnet hat, andere Geschosse, fertige Pläne.

So vorgehen:

- Was sich sicher aus dem Auftrag, dem Modell oder dem Büroprofil ablesen lässt, selbst nachschauen statt fragen.
- Fehlt eine Angabe oder ist sie mehrdeutig, kurz nachfragen, alle offenen Punkte in einer Nachricht, höchstens fünf kurze Fragen. Wenn möglich einen Vorschlag machen («Ich würde den Aufbau von AW01 nehmen, passt das?»).
- Danach den Auftrag in zwei, drei Sätzen zusammenfassen: was, wo, Massstab, Aufbau, Vorbild, was bleibt. Erst nach dem Ja des Nutzers die Vorschau machen.
- Ändert der Nutzer später etwas am Auftrag, die Zusammenfassung kurz anpassen und nochmals bestätigen lassen.
- Kleine, eindeutige Aufträge (z. B. «Raumstempel im EG nachführen») brauchen keine Rückfrage. Die Zusammenfassung genügt dann als ein Satz vor der Vorschau.

## Fünf Schritte für jede Änderung

1. **Vorschau:** Erst wenn der Auftrag geklärt ist. Das Werkzeug ohne `bestaetigt=true` aufrufen. Es zeigt, was es ändern würde, und schreibt nichts. Die Vorschau dem Nutzer kurz und verständlich zeigen.
2. **Schreiben nach Freigabe:** Erst wenn der Nutzer zustimmt, mit `bestaetigt=true` und `sitzung=<Name dieser Sitzung>` aufrufen. Die Sitzung holt die Archicad-Sperre, damit nie zwei Sitzungen gleichzeitig schreiben.
3. **Zurücklesen:** Das Ergebnis unabhängig lesen und mit der Vorschau vergleichen. Ein zweiter Lauf muss «nichts zu tun» melden.
4. **Plangrafik prüfen:** Bei Plänen `plangrafik_pruefen` laufen lassen und ein Bild mit `fenster_als_bild` zeigen. Für Bilder immer einen vollen Dateinamen mit `.png` angeben, nie nur einen Ordner.
5. **Nicht speichern,** bis der Nutzer es sagt (`projekt_speichern`).

Nach der Arbeit `archicad_sperre(aktion="freigeben")`.

## Grundsätze

- Nur ändern, was der Auftrag verlangt. Was der Nutzer von Hand verschoben hat, bleibt liegen.
- Echte Bauteile statt Morphs; Konstruktion vollständig und baubar.
- Beschriftung ruhig, nichts überlappt.
- Fehler (Gebrauchstauglichkeit, Kollisionen, Plangrafik, Baurecht) selbst suchen und melden: `grundriss_plausibilitaet`, `kollisionen_pruefen`, `modell_pruefen`.
- Probe-Elemente weit ausserhalb des Modells setzen (x/y ≥ 50 m), danach löschen und nachzählen.
- Nie Dateien endgültig löschen.
- Meldet ein Werkzeug «keine_lizenz» oder «nicht_im_abo»: Skill `plassist-einstieg`, Abschnitt «Meldungen».
