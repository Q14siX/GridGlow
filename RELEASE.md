# GridGlow · 20261113.145453

## Deutsch

- GitHub-Verzeichnis bereinigt: keine doppelte Installationsdatei, keine internen Veröffentlichungsnotizen oder Versionsmarker.
- `index.html` startet den vollständigen Installationsassistenten unmittelbar über GitHub Pages oder lokal.
- Alle sechs zu installierenden AWTRIX-Skripte liegen zusätzlich getrennt unter `clocks/TC001/` und `clocks/TC002/` und stimmen mit den eingebetteten Quellen überein.
- `README.md`, `RELEASE.md`, `LICENSE.md` und ausschließlich benötigte Bilder für die Veröffentlichung sind enthalten.
- FRITZ!Box-Standardnetz `192.168.178.0/24`, Multi-Uhr-Installation, Authentifizierung und Tibber-Einrichtung bleiben Bestandteil des Installers.

## English

- Minimal GitHub publishing directory with one standalone `index.html` installer.
- All six installable AWTRIX scripts are included separately under the two model folders and match the embedded installer bundle.
- README, release notes, license and only necessary publication images included.
- Existing multi-clock installation, authentication and Tibber setup are preserved.

Software verification does not constitute successful installation on physical clocks.


### Korrektur der Preisdiagramme
Die Kurve verwendet jetzt das tatsächliche Tagesminimum als untere und das Tagesmaximum als obere Skalenbegrenzung. Die Zeitmarkierung bleibt eine blinkende vertikale Linie. Die Kurve startet die Titelanzeige während derselben AWTRIX-App-Rotation nicht von selbst erneut. Eine Kurvenaktualisierung führt nicht zurück zur Titelanzeige.

### Price chart correction
The actual daily minimum maps to the bottom row and the maximum to the top row. The vertical time indicator continues blinking. No automatic chart-to-heading reset during the same AWTRIX app slot, even after refreshing data.
