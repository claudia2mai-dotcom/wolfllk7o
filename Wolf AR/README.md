# AR ohne Marker mit model-viewer

## Zweck

Diese Variante nutzt keinen Marker. Der QR-Code öffnet die Webseite. Danach wird die Szene über den AR-Button im Raum platziert.

## Ablauf

1. Ordner auf GitHub Pages oder Netlify veröffentlichen.
2. Link auf dem Smartphone öffnen.
3. AR-Button auswählen.
4. Raum mit der Kamera erfassen.
5. Szene platzieren.

## Dateien

```text
index.html
assets/
```

## Eigene Szene einsetzen

Für Android und WebXR:

```text
assets/szene.glb
```

Für iPhone:

```text
assets/szene.usdz
```

In `index.html` diese Stellen ändern:

```html
src="assets/szene.glb"
ios-src="assets/szene.usdz"
```

Ein GLB kann ein einzelnes Objekt oder eine ganze kleine Szene enthalten.

## Unterschied zur Marker-AR

| Variante | Was passiert? | Geeignet für |
|---|---|---|
| AR.js mit Marker | Szene erscheint an einem Marker | Plakate, Karten, Schwellen, Trigger im Raum |
| model-viewer ohne Marker | Szene wird frei im Raum platziert | Objekte, kleine Szenen, schnelle Smartphone-Tests |

## Hinweise

- iPhone braucht zusätzlich `.usdz`.
- Android nutzt `.glb`.
- Der Link muss mit `https://` beginnen.
- Dateinamen klein schreiben.
- Keine Leerzeichen.
- Keine Umlaute in Dateinamen.
