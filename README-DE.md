# XT-IDE 8-Bit IDE Controller für Robotron EC1834

Dies ist eine modifizierte Version des Original Glitchworks XT-IDE rev 4 controllers.

Der ISA Randverbinder wurde mit einem DIN 41612 Verbinder ausgeführt, wie er im Robotron EC1834 PC benutzt wird.

Das Layout der Original Platine wurde angepasst, damit die Platine und die Slotblende passen.

Diese Modifikation wurde von Mario Gögel durchgeführt.

**WICHTIGE HINWEISE ZU Rev. 4b (Revision nicht aufgedruckt)**
Der Gedanke, für die 74LS688 auf pull up zu wechseln, war eine schlechte Idee, weil ich einiges übersehen habe.
Montiert wie vorgesehen, wird der Controller nicht funktionieren.
Benötigte Änderungen:
    Pin 2 von RN2 muss getrennt werden
    Dafür muss ein 10K Widerstand an U1 von Pin 12 zu GND gelegt werden (am besten zu GND auf C1)
    
    Die Beschreibung auf der Platine für SW2, ENA+WR stimmen nicht - da keine Verbindung zu RP2 besteht, passt die Orignal Beschreibung
    SW2 8K könnte außer Funktion sein - oder 28C256 ROMs funktionieren nicht. Ungetestet, 28C64B funktionieren.

In Revision 4c wurde das behoben.

**Ausschluss:**
Ich übernehme keine Verantwortung für Schäden, die durch diese Anpassung entstehen. Alles wurde nach bestem Wissen und Gewissen angepasst.
Benutzung auf eigene Gefahr!

### Bill of Materials

Die BOM mit Mouser Bestellnummer ist [hier](https://github.com/glitchwrks/xt_ide/blob/master/bill_of_materials.md). 
Vermutlich müssen bei mouser (u.a.) andere Artikel gewählt werden. Zum Zeitpunkt der Erstellung (Mär-Jul 2022) ist die Liefersituation sehr schwierig.
Einen Bausatz kann man hier bestellen: [The Glitch Works](http://www.glitchwrks.com/xt-ide)
Dort fehlt aber der DIN Verbinder.

### Jumper Settings

[modem7](http://minuszerodegrees.net/) hat gute Diagramme zur Konfiguration der Karte auf [dieser Seite](http://www.minuszerodegrees.net/xtide/rev_4/XT-IDE%20Rev%204%20-%20general.htm).

### Slot 8 Support

Wurde komplett gestrichen, weil nicht benötigt

### Contributors

* Mario Goegel: Anpassung des Designs an den EC1834
* Scott Christensen: inspriation 16-bit ATA interface for the 8-bit ISA bus
* Jeff Leyda/Hargle: original production board work, original BIOS work
* Andrew Lynch/N8VEM: layout work, initial group buy(s) on earlier revisions
* modem7: documentation, switch/jumper drawings

**Please contact me or send a pull request to get your name added to the list!**

There were no authors/contributors listed in the XT-IDE rev 2 schematics/board layout I started with. If you have contributed to this project and would like your name here, on the schematic, or on the board layout, please let me know. You can open an issue or submit a pull request.
