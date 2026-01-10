# EMPIRE für den C64 (Deutsch)

Ein C64-Strategie-Spiel, inspiriert vom Spielkonzept „Empire Wargame“ (1 Spieler pro Computer), mit einem selbst entwickelten Userport-Netzwerk für bis zu vier C64.

*Hinweis: „Empire Wargame“ ist ein eigenständiges Werk; alle Rechte daran liegen bei den jeweiligen Rechteinhabern. Dieses Projekt ist nicht mit diesen Rechteinhabern verbunden, wird von ihnen nicht unterstützt und ist nicht von ihnen lizenziert.*

© 1991 Gordon Axmann (Assembler und KI; Netzwerkfähigkeit © 1997), Michael Abramowski (Grafik, Karten & BASIC)

## Dateien

- Anleitung (PDF): [`Anleitung_Empire_C64.pdf`](Anleitung_Empire_C64.pdf)

## Über das Spiel

Ziel ist es, den Titel *Imperator* zu erlangen: Dazu müssen mehr als 50% aller Städte erobert und diese Mehrheit für 2 Runden gehalten werden.

„Empire C64“ ist ein Fog-of-War-Spiel: Anfangs ist die Karte unerforscht; Städte und Landschaft müssen erst aufgeklärt werden. Gegnerische Einheiten werden nur in unmittelbarer Nähe eigener Einheiten sichtbar; alle anderen optischen Informationen können veraltet/falsch sein.

Das Spiel ist rundenbasiert. Einheiten erhalten Marschbefehle oder können warten; Transporter und Züge können Einheiten laden/entladen. Pioniere können Gleise bauen, die auch zerstört werden können.

## Mehrspieler-Modus und Userport-Netzwerk (historisch)

Das Spiel wurde für ein selbst entwickeltes Userport-Netzwerk (bis zu vier C64) gebaut. Die Spezifikation des vieradrigen Bus-Kabels findest du in der Datei `USERPORT-CABLE.md`.
VICE simuliert den Userport nicht korrekt; für den Netzwerkbetrieb werden echte C64 benötigt.

## Anleitung

Die PDF beschreibt Spielziel, Steuerung, Einheiten, Kampf/Erfahrung, Sichtsystem (Fog of War) sowie Tools rund um Karten (Map-Creator, Map-Editor, Startpositionen, Map-Adder).

## Lizenz

Siehe [`LICENSE.md`](LICENSE.md).
