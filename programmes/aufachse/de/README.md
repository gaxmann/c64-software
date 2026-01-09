# „Auf Achse, Computerspieler“ für C64 (Deutsch)

Dieses Programm ist ein Computer-Spieler (KI) für das Brettspiel „Auf Achse“ (F.X. Schmid, 1987). Es wird am Spieltisch parallel zum Brettspiel verwendet: Ein menschlicher Spieler würfelt und zieht den grauen Lkw, das Programm trifft die Entscheidungen (belädt, bietet mit, plant Routen).

Copyright (c) 1988 Gordon Axmann

**Dateien**

Disk-Image (D64): `Auf_Achse.d64`  
Anleitung (PDF): `Anleitung_Auf_Achse_C64.pdf`

**Start**

VICE: Disk-Image per Autostart laden (Menü „Datei“ → „Autostart von Disk/Band-Image“). Wenn der Bildschirm schwarz wird, läuft das Programm.

`x64 -autostart ~/Software.d64`

Auf echter Hardware oder in anderen Emulatoren das Disk-Image an Laufwerk 8 hängen, dann:

```
LOAD"*",8
RUN
```

**Wichtig**

Die Bedienung erfolgt ausschliesslich über Tastatureingaben. Bitte die Anleitung lesen, sonst ist das Programm kaum sinnvoll nutzbar.

**Spielvorbereitung (Kurzüberblick)**

Zu Beginn werden abgefragt: Anzahl der Auftragskarten im Spiel und die Startposition (Stadt in deren Nähe der Computer startet). Danach gibst du die drei Auftragskarten ein, die der Computer „auf der Hand“ hat (Nr. 1 bis 3), sowie die vier offenen Angebote am Spielbrettrand (F1 bis F4). Anschliessend berechnet der Computer seine Taktik.

**Während des Spiels (Kurzüberblick)**

Das Programm gibt die Fahrtrichtung vor (zum Beispiel „Fahre nach Hamburg“) und gelegentlich ein Alternativziel. Du ziehst den grauen Lkw entsprechend auf dem Brett. Bei Ereignissen und Auktionen informierst du das Programm per Taste.

**Tasten (Auszug)**

H: Hilfe (Tastaturbelegung)  
F1, F2, F3, F4: Ein menschlicher Spieler bietet auf eines der vier offenen Angebote (Versteigerung). Das Programm sagt, ob es mitbietet; dann Schritt für Schritt weiterklicken, bis die Karte vergeben ist. Danach fordert das Programm die Eingabe des nachgezogenen Auftrags.  
Leertaste: Der Computer-Lkw ist in einer Stadt angekommen, die nicht die Zielstadt ist (Name eingeben). Bei Spiel nach neueren Regeln auch beim ersten Computerzug zur Erfassung der Startstadt verwenden.  
Enter: Der Computer-Lkw ist in der Zielstadt angekommen.  
G: Geldstrafe (Ereigniskarte).  
A: Sonderauftrag (Ereigniskarte).  
F8: Ein Spieler hat das Spiel beendet.  
Pos1 (Home): Spielstand speichern.

**Regelwerke**

Das Programm ist für die alten Regeln (1987) erstellt. Regeländerungen der Neuauflage (2007) beeinflussen die Spielstärke leicht negativ (Details in der Anleitung).

**Lizenz (Kurzfassung)**

Nutzung und Weitergabe sind nur für nicht-kommerzielle Zwecke und nur in unveränderter Form erlaubt.
Alle Hinweise und Credits müssen erhalten bleiben; die Urheberschaft darf nicht beansprucht werden.
Die Verbreitung geänderter Versionen (einschliesslich Bugfixes, Hacks, Übersetzungen oder veränderter bzw.
neu verpackter Disk-Images) ist ohne vorherige schriftliche Erlaubnis nicht erlaubt. Der Name "ANABASIS"
darf ohne Erlaubnis nicht für geänderte Versionen verwendet werden. Keine Gewährleistung.

Verbindlicher Lizenztext: [`../LICENSE.txt`](../LICENSE.txt).


