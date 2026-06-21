# Gesichter-Collage – Web-App für iPhone

Diese Version läuft direkt im Safari-Browser deines iPhones – ganz ohne Mac,
Xcode oder Apple-Developer-Account. Über "Zum Home-Bildschirm hinzufügen"
bekommt sie ein eigenes App-Icon und startet im Vollbild.

## Was ist enthalten

- `index.html` – die komplette App (3×3-Raster, Kamera, Collage-Erstellung,
  Admin-Bereich für die Fragen)
- `manifest.json` – Metadaten für die "App-artige" Installation
- `icon-180.png` – Icon für den Home-Bildschirm

## Wichtig: HTTPS nötig

Kamera-Zugriff im Browser funktioniert nur über eine sichere Verbindung
(HTTPS). Die Datei lässt sich daher **nicht einfach per AirDrop oder Mail**
öffnen, sondern muss irgendwo mit HTTPS gehostet werden. Der einfachste
kostenlose Weg ohne eigenen Server: **GitHub Pages**.

## Schritt-für-Schritt: Hosting über GitHub Pages

1. **GitHub-Account erstellen** (falls noch nicht vorhanden): auf
   [github.com](https://github.com) registrieren – kostenlos, reicht eine
   E-Mail-Adresse.

2. **Neues Repository anlegen**: Oben rechts auf das "+"-Symbol → "New
   repository". Name z. B. `gesichter-collage`. Auf **"Public"** stellen
   (wichtig für kostenloses Hosting). "Create repository" klicken.

3. **Dateien hochladen**: Im neuen Repository auf "Add file" → "Upload
   files" klicken. Die drei Dateien (`index.html`, `manifest.json`,
   `icon-180.png`) per Drag & Drop reinziehen. Unten auf "Commit changes"
   klicken.

4. **GitHub Pages aktivieren**: Im Repository oben auf "Settings" →
   links im Menü auf "Pages". Unter "Build and deployment" → "Source":
   **"Deploy from a branch"** auswählen. Branch: **main**, Ordner: **/
   (root)**. Auf "Save" klicken.

5. **Kurz warten** (meist 1–2 Minuten), dann oben auf der Pages-Einstellungsseite
   die URL ablesen, z. B.:
   `https://DEIN-BENUTZERNAME.github.io/gesichter-collage/`

## Auf dem iPhone installieren

1. Die URL aus Schritt 5 in **Safari** auf dem iPhone öffnen (nicht Chrome
   oder eine andere App – das "Zum Home-Bildschirm"-Feature mit Kamera-
   Zugriff funktioniert zuverlässig nur in Safari).
2. Beim ersten Antippen einer Kachel fragt Safari nach der
   Kamera-Berechtigung – **"Erlauben"** antippen.
3. Unten auf das **Teilen-Symbol** (Quadrat mit Pfeil nach oben) tippen.
4. **"Zum Home-Bildschirm"** auswählen, Namen bestätigen, "Hinzufügen"
   tippen.
5. Ab jetzt liegt ein eigenes App-Icon auf dem Home-Bildschirm, das die
   App im Vollbild ohne Safari-Leiste öffnet.

## Bedienung

- Auf eine Kachel tippen → Frontkamera öffnet sich mit der Frage als
  Overlay → "Foto aufnehmen" tippen → 3-Sekunden-Countdown → Auslösung.
- Sind alle 9 Kacheln ausgefüllt, wird "Collage erstellen" aktiv.
- Im Ergebnis-Bildschirm: **"Teilen / Speichern"** öffnet den iOS-Share-Dialog,
  darüber lässt sich das Bild direkt in "Fotos" sichern. Falls der Dialog
  nicht erscheint: Bild gedrückt halten → "Zu Fotos hinzufügen".
- Über die drei Punkte (⋮) oben rechts gelangst du zu "Fragen bearbeiten".

## Bekannte Einschränkungen gegenüber einer nativen App

- Wird die Seite mitten in einer Runde neu geladen oder die App vom
  System aus dem Speicher geworfen, gehen die bereits aufgenommenen
  Fotos der aktuellen Runde verloren (sie liegen nur im Arbeitsspeicher
  der Seite). Die 9 Fragen-Texte bleiben aber dauerhaft gespeichert.
- Das Speichern ins Fotoalbum läuft über den iOS-Share-Dialog statt
  vollautomatisch.
