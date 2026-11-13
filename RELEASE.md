# GridGlow · 20261113.152513

## Deutsch

- Online-Installer statt einer 12-MB-HTML-Datei: schlanke `index.html`.
- App-Dateien werden beim Installieren direkt aus `clocks/` geladen und gegen SHA-256 aus `release.json` geprüft.
- Vorschauen und GIFs werden bei Bedarf aus `images/` abgerufen.
- FRITZ!Box-Standardbereich, geschützte Uhren, Tibber-Eingaben, gemeinsame Datenabfrage und zwei parallele Uhren bleiben erhalten.
- Lokaler Offline-Installer ist nicht mehr Teil dieses Pakets.
- Browser können Anfragen von HTTPS-Seiten an lokale HTTP-Uhren blockieren; dies wurde nicht auf realen Geräten verifiziert.

## English

- Lightweight GitHub Pages installer with remote, hash-checked `.ax` downloads and lazy-loaded previews.
- All required clock scripts, images, GIFs, README, release notes and license included.
- Existing multi-clock selection and configuration features remain available.
- No downloaded offline installer. Access to local HTTP clocks from HTTPS is subject to browser security restrictions.
