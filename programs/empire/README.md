# EMPIRE für den C64 (Deutsch)

Eine C64-Umsetzung des Strategie-Spiels „Empire Wargame“ (1 Spieler pro Computer) mit einem selbst entwickelten Userport-Netzwerk für bis zu vier C64.

© 1991 Gordon Axmann (Assembler und KI; Netzwerkfähigkeit © 1997), Michael Abramowski (Grafik, Karten & BASIC)

## Dateien

- Anleitung (PDF): [`Anleitung_Empire_C64.pdf`](Anleitung_Empire_C64.pdf)

## Über das Spiel

Ziel ist es, den Titel *Imperator* zu erlangen: Dazu müssen mehr als 50% aller Städte erobert und diese Mehrheit für 2 Runden gehalten werden.

„Empire C64“ ist ein Fog-of-War-Spiel: Anfangs ist die Karte unerforscht; Städte und Landschaft müssen erst aufgeklärt werden. Gegnerische Einheiten werden nur in unmittelbarer Nähe eigener Einheiten sichtbar; alle anderen optischen Informationen können veraltet/falsch sein.

Das Spiel ist rundenbasiert. Einheiten erhalten Marschbefehle oder können warten; Transporter und Züge können Einheiten laden/entladen. Pioniere können Gleise bauen, die auch zerstört werden können.

## Mehrspieler-Modus und Userport-Netzwerk (historisch)

Das Spiel wurde für ein selbst entwickeltes Userport-Netzwerk (bis zu vier C64) gebaut. Die Spezifikation des vieradrigen Bus-Kabels findest du in der Datei `USERPORT-CABLE.md`. VICE simuliert den Userport nicht korrekt. Man braucht echte C64 für den Netzwerkbetrieb!

***You find the specification of the userport cable for the C64 in the file `USERPORT-CABLE.md`. Please note that VICE doesn's simulate the userport correctly. You do need real, not emulated C64 for this to work.***

Aus der Anleitung:
- Die Rechner tauschten Spielzüge über das Netzwerk aus; ein Rechner war Master.
- Die Verbindung war so schnell, dass der Master anfangs die Programm-Software darüber an die Clients verteilt hat (schneller als VC1541 mit Speeddos).
- Der Master hatte eine Floppy; Clients benötigten nur eine Datasette und luden eine kleine (~1,5 KB) Netzwerk-Software.

## Anleitung

Die PDF beschreibt Spielziel, Steuerung, Einheiten, Kampf/Erfahrung, Sichtsystem (Fog of War) sowie Tools rund um Karten (Map-Creator, Map-Editor, Startpositionen, Map-Adder).

## Lizenz (Kurzfassung)

Das Programm wurde für rein private Unterhaltungszwecke erstellt; gewerbliche Nutzung ist untersagt. Verbindlich ist der Wortlaut in der PDF-Anleitung.
