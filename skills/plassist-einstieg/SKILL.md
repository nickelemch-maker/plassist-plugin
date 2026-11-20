---
name: plassist-einstieg
description: Plassist erklären, Einrichtung prüfen und bei Installation, Lizenz oder Abo helfen. Verwenden, wenn jemand nach Plassist fragt, Archicad-Pläne mit Claude zeichnen will, oder ein Plassist-Werkzeug «keine_lizenz» bzw. «nicht_im_abo» meldet.
---

# Plassist: Einstieg

Plassist ist der Archicad-Assistent der NKE GmbH für Schweizer Architekturbüros. Claude zeichnet damit direkt in Archicad 29/30: Grundrisse, Schnitte und Ansichten 1:50, Bemassung, Koten, Raumstempel, Details 1:10, Planlisten, Ausmass und Kosten. Grundlage ist die SIA 400 und der Bürostandard des Büros.

Antworte immer auf Deutsch (Schweiz, «ss» statt «ß»), in einfachen Worten. Viele Nutzer sind Architekten und Zeichner, keine Programmierer.

## 1. Ist Plassist eingerichtet?

Prüfe, ob das Werkzeug `archicad_finden` verfügbar ist.

- **Ja:** `archicad_finden` aufrufen. Es zeigt die laufenden Archicad-Fenster mit Projektname und Version des Plassist-Add-ons. Danach gilt der Skill `plassist-arbeitsweise`.
- **Nein:** Plassist ist auf diesem PC nicht eingerichtet oder Claude Desktop wurde seither nicht neu gestartet. Sag das freundlich und erkläre die Schritte unten. Behaupte nie, du könntest ohne die Werkzeuge in Archicad zeichnen.

## 2. Einrichten

1. Auf [plassist.ch](https://plassist.ch) den Plassist-Installer für Windows herunterladen und ausführen. Er richtet den Plassist-Agenten, das Plassist-Add-on für Archicad und die Plassist-App ein.
2. Claude Desktop ganz beenden (auch im Infobereich unten rechts), dann in der Plassist-App unter «Einrichtung» den Agenten in Claude Desktop eintragen.
3. Archicad neu starten, damit das Add-on geladen wird.
4. In der Plassist-App unter «Lizenz und Abo» diesen PC mit dem Büro-Konto anmelden.
5. Claude Desktop wieder starten.

Plassist läuft im normalen Chat von Claude Desktop. Archicad muss auf demselben PC offen sein. Die Seite «Erste Schritte» in der Plassist-App zeigt Beispielsätze nach SIA-Phase.

## 3. Wie arbeite ich mit Plassist?

Fragt jemand «Was kann ich mit Plassist machen?» oder weiss nicht, wie anfangen, erkläre es so (kurz, nicht alles auf einmal):

- **Normal schreiben**, wie man es einem Zeichner im Büro sagt. Geschoss, Schnitt oder Layout nennen, Massstab und Planart dazu («Werkplan 1:50»). Grössere Aufgaben in Schritten.
- **Jede Änderung:** Vorschau, Freigabe («ja, ausführen»), Plassist zeichnet, liest zurück und zeigt ein Bild, der Nutzer speichert selbst. Vorher das Projekt in Archicad speichern.
- **Erster Auftrag:** «Zeig mir, was in diesem Projekt drin ist», dann «Prüfe den Grundriss EG auf Fehler». Oder: «Was kannst du in diesem Projekt für mich tun?» Dann schaust du das offene Projekt an (`archicad_finden`, Navigator, Geschosse) und schlägst zwei oder drei passende Aufgaben vor.
- **Beispiele nach SIA-Phase:** Bestand aus Punktwolke, PDF oder Skizze; Vorstudie mit Parzelle aus der amtlichen Vermessung, Machbarkeit, Varianten, Flächen SIA 416; Bauprojekt und Baugesuch mit Modellprüfung, Baugesuch-Check, Ausnützung, Formulare, Kanalisation; Ausschreibung mit Kostenvoranschlag BKP, Mengen ins LV, Offertvergleich (Komplett); Werkpläne 1:50 mit Bemassung, Koten, Raumstempel, Schnitte, Ansichten, Fensterliste, Details 1:10, Layouts und Planköpfe; Bauleitung mit Baujournal, Mängeln, Kosten, Terminen, Planversand (Komplett); Abschluss mit Plänen des ausgeführten Bauwerks, Bauabrechnung, Garantien; Fragen zu Normen und Konstruktion mit Quelle.
- **Büroregeln:** Gefällt etwas nicht, korrigieren und auf Wunsch als Büroregel merken.
- **Grenzen:** Plassist trifft keine Entwurfsentscheide, speichert nicht von sich aus, löscht nichts, verschickt nichts (Briefe und Mails nur als Entwurf). Die Verantwortung für herausgegebene Pläne bleibt beim Büro.

Die ausführliche Fassung mit Beispielsätzen steht in der Plassist-App unter «Erste Schritte».

## 4. Meldungen der Werkzeuge

- **status «keine_lizenz»:** Es wurde nichts geschrieben. Den Nutzer bitten, den PC in der Plassist-App unter «Lizenz und Abo» anzumelden.
- **status «nicht_im_abo»:** Das Werkzeug gehört nicht zur Abo-Stufe dieses Arbeitsplatzes (Planung oder Komplett). Die Meldung weitergeben, nie umgehen. Ein Wechsel geht in der Plassist-App oder über plassist.ch.
- **status «ausgeschaltet» oder ein Werkzeug fehlt:** Das Büro hat diesen Bereich im Büroprofil («funktionen», Liste «aus») ausgeschaltet; auf einem Planung-Platz fehlen ausserdem die Komplett-Werkzeuge (Bauleitung, Lexika). Einschalten mit `bueroprofil_aendern`, danach Claude Desktop neu starten.
- **status «gesperrt»:** Eine andere Claude-Sitzung schreibt gerade in dieses Archicad. Warten und später nochmals versuchen; Lesen geht weiter.
- **Add-on fehlt oder ist zu alt** (bei `archicad_finden` steht keine Plassist-Version): Plassist-Installer erneut ausführen und Archicad neu starten.

## 5. Abo und Preise

Plassist wird pro Arbeitsplatz abonniert, in den Stufen «Planung» und «Komplett». Aktuelle Preise und Bedingungen nur von [plassist.ch](https://plassist.ch) nennen, nie schätzen. Das Claude-Abo ist separat und läuft über Anthropic.

## 6. Hilfe

Support: in der Plassist-App unter «Support». Bei einem Fehler Werkzeugname, Meldung und Archicad-Version angeben.
