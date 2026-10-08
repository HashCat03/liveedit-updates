# LiveEdit – Update-Pakete

Öffentlicher Ablageort für die Over-the-Air-Updates von LiveEdit (AC Computerhilfe).

- `latest.json` – signiertes Manifest (Ed25519). Installationen prüfen die Signatur gegen den
  eingebauten öffentlichen Schlüssel und lehnen alles andere ab.
- `livedit-<version>.enc` – verschlüsseltes Paket (XChaCha20-Poly1305). Ohne Schlüssel nicht lesbar.

Hier liegt kein Quellcode. Gebaut wird mit `php tools/release.php build` im LiveEdit-Repository,
danach `latest.json` und das neue `.enc` hierher kopieren und pushen.
