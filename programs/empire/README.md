# EMPIRE für den C64 (Deutsch)

Eine C64-Umsetzung des Strategie-Spiels „Empire Wargame“ (1 Spieler pro Computer) mit einem selbst entwickelten Userport-Netzwerk für bis zu vier C64.

© 1991 Gordon Axmann (Assembler, Netzwerk und KI), Michael Abramowski (Grafik, Karten & BASIC)

## Dateien

- Anleitung (PDF): [`Anleitung_Empire_C64.pdf`](Anleitung_Empire_C64.pdf)

## Über das Spiel

Ziel ist es, den Titel *Imperator* zu erlangen: Dazu müssen mehr als 50% aller Städte erobert und diese Mehrheit für 2 Runden gehalten werden.

„Empire C64“ ist ein Fog-of-War-Spiel: Anfangs ist die Karte unerforscht; Städte und Landschaft müssen erst aufgeklärt werden. Gegnerische Einheiten werden nur in unmittelbarer Nähe eigener Einheiten sichtbar; alles andere kann veraltet sein.

Das Spiel ist rundenbasiert. Einheiten erhalten Marschbefehle und können warten; Transporter und Züge können Einheiten laden/entladen. Pioniere können Gleise bauen, die auch zerstört werden können.

## Mehrspieler-Modus und Userport-Netzwerk (historisch)

Das Spiel wurde für ein selbst entwickeltes Userport-Netzwerk (bis zu vier C64) gebaut. Die Spezifikation des vieradrigen Bus-Kabels ist verloren gegangen; daher ist der Mehrspielerbetrieb heute im Emulator nicht rekonstruierbar.

Aus der Anleitung:
- Die Rechner tauschten Spielzüge über das Netzwerk aus; ein Rechner war Host.
- Die Verbindung war so schnell, dass der Host die Programm-Software darüber an die Clients verteilt hat (schneller als VC1541 mit Speeddos).
- Der Host hatte eine Floppy; Clients benötigten nur eine Datasette und luden eine kleine (~1,5 KB) Netzwerk-Software.

Falls du Informationen zum Kabel/Schaltplan/Pinout oder zu ähnlichen Userport-Netzwerken hast: bitte ein GitHub-Issue eröffnen oder Kontakt aufnehmen.

## Anleitung

Die PDF beschreibt Spielziel, Steuerung, Einheiten, Kampf/Erfahrung, Sichtsystem (Fog of War) sowie Tools rund um Karten (Map-Creator, Map-Editor, Startpositionen, Map-Adder). Auch enthalten: Speichern über Pos1/Home (im Mehrspieler als Pause-für-alle).

## Lizenz (Kurzfassung)

Das Programm wurde für rein private Unterhaltungszwecke erstellt; gewerbliche Nutzung ist untersagt. Verbindlich ist der Wortlaut in der PDF-Anleitung.
