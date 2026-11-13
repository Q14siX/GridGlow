# GridGlow

AWTRIX NG app for Ulanzi TC001 and TC002 · Version `20261113.145453`  
[Deutsch](#deutsch) · [English](#english)

**[Installationsassistent öffnen / Open installer](https://q14six.github.io/GridGlow/)**

## Deutsch

GridGlow zeigt Tibber-Strompreise in **ct/kWh**, Tagespreisdiagramme sowie verfügbare historische Energie- und Kostenwerte an. Jede installierte Anzeige zeigt genau einen ausgewählten Wert. Pro Uhr holt `gridglow_data` die Daten zentral; alle Anzeigen verwenden `gridglow_view` zur Darstellung. Es wird keine separate Bridge benötigt.

### Installation

`index.html` ist der vollständig eigenständige Installationsassistent. Er enthält die sechs AWTRIX-Skripte direkt, sodass GitHub Pages keinen externen Anwendungsserver benötigt. Dieselben sechs Skripte stehen zusätzlich als einzelne Dateien in `clocks/TC001/` und `clocks/TC002/` zur Verfügung. **Diese Dateien nicht weglassen.**

1. Lade den **Inhalt** dieses GitHub-Ordners in das Stammverzeichnis des Repositorys `Q14siX/GridGlow` (Branch `main`).
2. Aktiviere unter **Settings → Pages → Build and deployment** die Veröffentlichung aus **main** und **/(root)**.
3. Öffne danach den obigen Link. Es ist kein separates lokales Installerprogramm nötig.
4. Suche die Uhren im vorbelegten FRITZ!Box-Netz `192.168.178.0/24` oder gib ihre Adressen ein. Bei geschützten Uhren Benutzername und Kennwort angeben. Mehrere Uhren können in einem Installationslauf ausgewählt werden.
5. Wähle die Ansicht(en), prüfe den Plan und bestätige die Installation bzw. Aktualisierung. Vorhandene Einstellungen bleiben soweit möglich erhalten.

Die TC001 verwendet einen persönlichen Tibber GraphQL-Token. Auf der TC002 erfolgt die Anmeldung an der Tibber Data API über den nativen AWTRIX-OAuth-Dialog auf der Uhr (Client-ID und Client-Secret müssen dort hinterlegt werden). Redirect URI: `https://awtrix.de/oauth/callback`. Optional lassen sich historische Hauswerte über einen GraphQL-Token auf der TC002 abrufen. Der Installer speichert keine Kennwörter oder Tibber-Zugangsdaten in Exportdateien.

**Browser-Hinweis:** Ein von HTTPS (GitHub Pages) gestarteter Browserzugriff auf lokale HTTP-Uhren kann wegen Private Network Access, Mixed Content oder CORS blockiert werden. In diesem Fall die enthaltene `index.html` lokal öffnen und die Browserzugriffe entsprechend den Sicherheitsmeldungen freigeben; die erfolgreiche Installation auf echter Hardware ist noch zu prüfen.

## English

GridGlow displays Tibber electricity prices per kWh, daily price charts, and available historical energy/cost information on AWTRIX NG clocks. Each installed display shows one selected view. `gridglow_data` fetches data once per clock and `gridglow_view` is the common drawing module. No separate always-on bridge is needed.

`index.html` is a complete standalone installer with all six scripts embedded. Identical standalone scripts are also provided in `clocks/TC001/` and `clocks/TC002/`. Publish this folder's **contents** at the repository root and enable GitHub Pages from the `main` branch and `/(root)`; then open the installation link above. The default search range is `192.168.178.0/24`; protected clocks and multiple clocks per installation are supported.

TC001 uses a personal Tibber GraphQL token; TC002 uses the clock's native OAuth login and may optionally use a GraphQL token for history. Registered redirect URI: `https://awtrix.de/oauth/callback`. The exportable installer configuration does not contain passwords or API credentials.

Browsers may restrict HTTPS-to-local-HTTP requests; use the standalone `index.html` locally when necessary. Actual-device verification remains pending.


### Korrektur der Preisdiagramme
Die Kurve verwendet jetzt das tatsächliche Tagesminimum als untere und das Tagesmaximum als obere Skalenbegrenzung. Die Zeitmarkierung bleibt eine blinkende vertikale Linie. Die Kurve startet die Titelanzeige während derselben AWTRIX-App-Rotation nicht von selbst erneut. Eine Kurvenaktualisierung führt nicht zurück zur Titelanzeige.

### Price chart correction
The actual daily minimum maps to the bottom row and the maximum to the top row. The vertical time indicator continues blinking. No automatic chart-to-heading reset during the same AWTRIX app slot, even after refreshing data.
