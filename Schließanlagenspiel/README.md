# Burg Kriebstein Schliessanlagenspiel

### Installation
```
npm install
```

### Karte / Wege / Türen, etc.

Die Karte wurde aus der Illustrator-Datei "map/map.ai" exportiert 
und als "assets/spielplan.jpg" gespeichert.

Die Daten für Wege und Türen werden aus der Illustrator-Datei generiert. Dazu in Illustrator 
das Skript "map/exportMap.js" ausführen. Es wird die Datei "map/map.json" erzeugt, die in das Verzeichnis
"public" kopiert werden muss.

Die Illustrator-Datei muss dazu die folgende Struktur haben:
- Auf oberster Ebene muss es zwei Ebenen "Paths" und "Doors" geben
- Unter "Paths" sollten nur die Pfade (grüne Linien) liegen
- Unter "Doors" soll es für jede Türengruppe eine benannte Ebene geben
- unter jeder Türgruppe sind die zugeordneten Türen
- Türen können benannt werden; wenn sie initial offen sein sollen, muss der Namen mit "open" enden

Die Anwendung läuft nicht aus dem Dateisystem, sondern benötigt einen Webserver.
Dafür kann die Datei "public/map.json" einfach ausgetauscht werden ohne dass neu kompiliert werden muss.

### Status / Todo
- Koordinaten und exportierte Grafik leicht verschoben
- Routen der Figuren werden von zwei Anfangspositionen zufällig berechnet  
- Bisher keine Kollisionsbehandlung der zwei Figuren
- Figuren bleibt bei/an geschlossenen Türen stehen

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

