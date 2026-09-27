# Kreta Kompass - Das Insel-Wiki
## Version 1.0

Ein spielerisches, deutschsprachiges Wiki für Kinder ab etwa sieben Jahren: griechische Mythologie, Neugriechisch und die Insel Kreta. Ohne Konto, Punkte, Lernfortschritt oder Zeitdruck. Für Smartphone-Querformat gestaltet, auch im Hochformat sowie auf Tablet und Computer bedienbar.

## Inhalt

- **Götter und Sagen:** 28 Figuren, drei Stammbaum-Ansichten, acht neu formulierte Kurzgeschichten, Querverbindungen und Sagenrätsel.
- **Griechisch:** 24 Buchstaben, zehn Buchstabenverbindungen, eine griechische Bildschirmtastatur, 165 Ferienwörter und Wendungen sowie die Zahlwörter 0 bis 100. Buchstaben-, Zahlen- und Wörterquiz ohne Punkte.
- **Kreta:** interaktive Karte mit 18 Orten, Zoom und Verschieben, Ortsfilter, acht Kartensuchrätsel, zwölf Wissenskarten und Inselquiz.

Die Wiki-Suche findet Figuren, Geschichten, Orte, Buchstaben und Wörter. Vorlesen nutzt die verfügbaren Stimmen des Geräts. Alle eigentlichen Wiki-Inhalte und Illustrationen sind in `index.html` eingebettet. Kein Build-Schritt, keine API-Schlüssel, keine externen JavaScript-Bibliotheken und keine externen Schriftdateien erforderlich.

## Auf GitHub Pages veröffentlichen

1. Ein Repository anlegen, zum Beispiel `kreta-kompass`.
2. Das ZIP entpacken und seinen **Inhalt direkt in das Hauptverzeichnis** hochladen. Dort muss `index.html` liegen, nicht erst in einem zusätzlichen Unterordner. Den Ordner `licenses` mit hochladen. Die Dateien nicht umbenennen.
3. Die Dateien im Branch `main` speichern (Commit).
4. Im Repository unter **Settings > Pages > Build and deployment** als Source **Deploy from a branch** wählen. Branch **main**, Ordner **/ (root)**, dann **Save**.
5. Nach dem erfolgreichen Deployment die in GitHub angezeigte Website-Adresse öffnen. Der Dateilink zur HTML-Datei im Repository ist nicht die veröffentlichte Website.

Offizielle Anleitung: https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

GitHub Pages macht die Website in der Regel öffentlich zugänglich. Dieses Paket enthält keine persönlichen Angaben zum Kind oder zur Familie.

## Auf dem iPhone und für die Reise

Die veröffentlichte Website zuerst **mit Internet in Safari** öffnen. Unten auf **Offline bereit** warten. Danach über **Teilen > Zu Home-Bildschirm hinzufügen** ablegen; falls angezeigt, **Als Web-App öffnen** aktivieren. Einmal über das neue Symbol mit Internet starten und wieder auf den Offline-Hinweis warten.

**Vor der Abreise im Flugmodus testen:** die App neu öffnen, in alle drei Bereiche wechseln, eine Geschichte aufrufen und ein Wort eintippen. Browser können Offline-Daten wieder entfernen. Ein gespeicherter Home-Bildschirm-Link allein garantiert noch keinen Offline-Inhalt. Nach dem Löschen von Website-Daten erneut mit Internet laden.

Quellenlinks und Google Übersetzer brauchen Internet. Ob deutsche und griechische Stimmen vorhanden sind und offline sprechen können, hängt vom Gerät ab. Die App meldet fehlende Stimmen, statt griechische Wörter mit einer falschen Sprachstimme vorzulesen.

Offizielle Apple-Anleitung: https://support.apple.com/de-de/guide/iphone/iphea86e5236/ios

## Wort-Werkstatt: Bedeutung ist nicht Aussprache

Zum Testen: **Ν + Ε + Ρ + Ο** ergibt **νερό - Wasser - ne-RO**.

Gross- und Kleinbuchstaben sowie fehlende Akzente werden beim Nachschlagen toleriert. Akzente können aber die Bedeutung ändern: **πορτοκάλι** bedeutet die Orange, **πορτοκαλί** die Farbe Orange. Bei mehrdeutiger Eingabe zeigt die App beide Formen zur Auswahl.

Das lokale Ferienwörterbuch ist **kein allgemeiner Satzübersetzer**. Nicht jede gebeugte Wortform ist enthalten. Bei unbekannten Wörtern erscheint nur eine klar als solche bezeichnete, ungefähre Lesehilfe. Der Knopf zum Online-Nachschlagen öffnet zuerst einen Hinweis für die gemeinsame Nutzung mit einem Erwachsenen. Erst der dortige Link übergibt den Text an Google Übersetzer. Es gibt keinen automatischen Hintergrundaufruf.

Die Zahlenansicht zeigt heutige griechische Zahlwörter, nicht ein antikes Buchstaben-Zahlensystem. Für Preise und Zahlen verwendet man im heutigen Griechenland dieselben Ziffern wie hier.

## Dateien

`index.html`: vollständiges Wiki mit eingebetteten Daten, Stilen und SVG-Illustrationen.

`sw.js`: Service Worker für die Offline-Speicherung. Funktioniert auf HTTPS, zum Beispiel GitHub Pages. Er ist auf das jeweilige Repository-Verzeichnis begrenzt.

`manifest.webmanifest`, `icon.svg`, `icon-192.png`, `icon-512.png`: App-Name und Symbole für den Home-Bildschirm.

`coastline.json`, `licenses/`, `NOTICE.md`: bearbeitbare Küstenkoordinaten, Datenherkunft und Lizenzen.

`.nojekyll`: kennzeichnet ein direkt auslieferbares statisches Paket.

Eine separate Einzeldatei `Kreta_Kompass_V1.0.html` wird zusätzlich bereitgestellt. Sie enthält ebenfalls alle Wiki-Inhalte, aber nicht die separate Service-Worker-Installation. Am Computer kann sie direkt in einem JavaScript-fähigen Browser geöffnet werden. Für das iPhone ist die veröffentlichte GitHub-Pages-Seite der einfachere Weg; reine Dateivorschauen führen die App möglicherweise nicht aus.

## Inhalte anpassen

In `index.html` enthält der Block `<script id="wiki-data" type="application/json">` die Inhalte: `gods`, `stories`, `alphabet`, `pairs`, `words`, `numbers`, `places`, `facts`, `quiz` und `sources`. Der gesamte Code ist lesbar und ohne Paketmanager editierbar. Nach inhaltlichen Änderungen die Seite mit Internet neu laden. Bei einer technischen Versionserhöhung die Cache-Version in `sw.js` und in `prepareOffline()` in `index.html` gemeinsam erhöhen.

## Quellen und Grenzen

Die Quellen stehen in den jeweiligen Einträgen sowie unter **Quellen & Hinweise**. Stand: 27. September 2026. Sagen sind ausdrücklich von Geschichte und geografischen Fakten getrennt. Mehrere Überlieferungen werden kenntlich gemacht; Stammbäume und Geschichten sind altersgerecht vereinfacht.

Die Karte ist eine Entdeckerkarte mit ungefähren Ortsmarkierungen, **keine Navigationskarte**. Aktuelle Wegsperrungen, Eintrittspreise, Öffnungszeiten, Wetter und Anreise müssen Erwachsene gesondert prüfen.

Keine Anmeldung, Werbung, Punktespeicherung oder eingebautes Nutzungs-Tracking. Eingaben liegen nur im laufenden Arbeitsspeicher der App. Es gelten zusätzlich die technischen Zugriffe des gewählten Hosters sowie bei externen Links oder Gerätestimmen die Bedingungen der jeweiligen Anbieter.

## Funktionsprüfung

275 automatisierte Prüfungen in Chromium ohne JavaScript-Laufzeitfehler, darunter alle Figuren und Geschichten, Buchstaben, Übersetzungen, Zahlen, Quizvarianten, Kartenpunkte, Suche und fünf Bildschirmgrössen. Zusätzlich wurden Touch-Auswahl, Zweifinger-Zoom und Verschieben emuliert. Die Service-Worker-Logik wurde isoliert mit simuliertem Cache und Netzausfall geprüft. Ein vollständiger Offline-Ende-zu-Ende-Test und ein Test auf einem echten iPhone/Safari waren hier nicht möglich. Deshalb den obigen Flugmodus-Test auf dem Reisegerät durchführen.
