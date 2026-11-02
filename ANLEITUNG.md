# Deine Schmiede-App

Die Inhalte stammen aus deiner fertigen Skyrim-Schmiedestrategie.html. Alle fünf Materialien, Gegenstände, Farben und zusammengefassten Qualitätsbereiche bleiben erhalten. Die Zahlen an den Qualitätsnamen wurden unverändert übernommen. Auf schmalen Bildschirmen wählst du oben das Material; am Desktop siehst du alle Materialien gleichzeitig.

## Kostenlos über GitHub Pages bereitstellen

1. ZIP entpacken und bei https://github.com anmelden oder ein kostenloses Konto erstellen.
2. Über **New repository** ein neues **öffentliches** Repository namens `skyrim-schmiede` erstellen. Öffentlich bedeutet: Die hochgeladenen Dateien sind für andere sichtbar.
3. Im Repository **Add file → Upload files** wählen. Den gesamten Inhalt des entpackten Ordners `skyrim-pwa` hochladen, nicht den Ordner selbst oder das ZIP. `index.html`, `sw.js`, Manifest und die drei PNG-Dateien müssen direkt nebeneinander liegen. Mit **Commit changes** speichern. Die leere `.nojekyll` ist für diese einfachen Dateien optional.
4. **Settings → Pages** öffnen. Unter **Build and deployment → Source** die Option **Deploy from a branch** auswählen. Als Branch **main**, als Ordner **/(root)** wählen und **Save** drücken.
5. Nach erfolgreicher Bereitstellung erscheint dort die Webadresse, üblicherweise `https://DEIN-NAME.github.io/skyrim-schmiede/`. Das kann einige Minuten dauern. **Enforce HTTPS** aktivieren, falls auswählbar.
6. Diese Adresse auf dem iPhone in **Safari** öffnen.

Es wurde nichts in deinem Konto veröffentlicht. Die oben genannten Schritte führst du selbst aus.

## Auf dem iPhone installieren

1. Die HTTPS-Webadresse in Safari öffnen und auf **Offline bereit** warten.
2. **Teilen → Zum Home-Bildschirm** wählen. Falls vorhanden, **Als Web-App öffnen** aktivieren und **Hinzufügen** antippen.
3. Die App über ihr neues Amboss-Icon starten. Einmal mit Internet öffnen und auf **Offline bereit** warten, da die installierte App einen eigenen Speicher verwenden kann.
4. Flugmodus einschalten, die App schließen und über das Icon erneut öffnen. Die Tabelle und alle fünf Materialknöpfe sollen weiter funktionieren.

Falls „Zum Home-Bildschirm“ fehlt, im Teilen-Menü nach unten scrollen und gegebenenfalls **Aktionen bearbeiten** wählen.

**Für zuverlässige Installation und Service Worker ist HTTPS erforderlich.** Das bloße Öffnen einer lokalen HTML-Datei reicht dafür nicht. `localhost` ist lediglich eine Ausnahme für lokale Entwicklung. Die App enthält keine extern geladenen Schriften, Bilder oder anderen Laufzeitabhängigkeiten.

## Weiterhin am PC nutzen

Die gehostete Adresse funktioniert auch auf dem Desktop. Alternativ den entpackten Ordner behalten und `index.html` per Doppelklick öffnen: Die Tabelle und Auswahl funktionieren lokal ohne Internet; die PWA-Installation und der Service Worker stehen dabei nicht zur Verfügung. Über **Drucken** bleibt die vollständige Tabelle druckbar.

## Offline-Speicher und Änderungen

Offline funktioniert nach erfolgreichem Erstaufruf auf dem jeweiligen Gerät. Wird der Website-Speicher gelöscht oder vom System entfernt, ist erneut ein Online-Aufruf nötig.

Bei späteren Inhaltsänderungen in `sw.js` die Version `v1` erhöhen und die geänderten Dateien hochladen. Nach einem Online-Aufruf die App vollständig schließen und erneut öffnen, damit die neue Version aktiv werden kann.

## Prüfung dieser Lieferung

- Chromium-Browsertest bei 320, 375, 390 und 430 Pixeln Breite: kein horizontales Überlaufen.
- Desktop bei 1280 Pixeln: alle fünf Materialspalten sichtbar.
- Alle fünf Materialknöpfe und die Qualitätsmarkierung geprüft.
- Verdichtete Felder erhalten; in Gegenstandszellen stehen ausschließlich die ursprünglichen deutschen Itemnamen.
- Service Worker auf lokalem Testserver unter einem Unterpfad registriert; erneutes Laden von Startseite und `index.html` bei abgeschaltetem Netzwerk erfolgreich.
- Mobile und Desktop-Screenshots visuell geprüft; keine JavaScript-Fehler im Test.
- Keine Prüfung auf einem echten iPhone oder eines öffentlichen HTTPS-Deployments. Safari-Installation und Flugmodus bitte mit obigen Schritten prüfen.

## Dateien

`index.html`: Übersicht mit eingebautem Layout und Bedienung. `manifest.webmanifest`: Installationsdaten. `sw.js`: Offline-Speicher. `icon-192.png`, `icon-512.png`, `apple-touch-icon.png`: eigens gezeichneter geometrischer Amboss mit Funken, ohne fremdes Logo. `.nojekyll`: deaktiviert die für diese Seite unnötige Jekyll-Verarbeitung.

Offizielle Hilfe: [GitHub Pages einrichten](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site), [Website als iPhone-App hinzufügen](https://support.apple.com/guide/iphone/open-as-web-app-iphea86e5236/ios).
