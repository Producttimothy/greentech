# GreenTech Real Estate – statische Website

Diese Version besteht nur aus HTML, CSS und JavaScript. Sie kann ohne Build-Prozess auf GitHub Pages veröffentlicht werden.

## Inhalt

- `index.html` – Seiteninhalt und Anfrageformular
- `styles.css` – Design und responsive Darstellung
- `script.js` – mobiles Menü, Leistungsfilter, Preisrechner und Datenschutz-Hinweis
- `.nojekyll` – verhindert eine unnötige Jekyll-Verarbeitung auf GitHub Pages
- `_redirects` und Unterordner – Weiterleitungen der bisherigen Wix-Adressen

## Auf GitHub Pages veröffentlichen

1. Auf GitHub ein neues Repository anlegen.
2. Den **Inhalt dieses Ordners** in die oberste Ebene des Repositorys hochladen. `index.html` muss also direkt im Repository liegen.
3. Unter **Settings → Pages** bei **Source** „Deploy from a branch“ auswählen.
4. Branch `main` und Ordner `/(root)` auswählen, anschließend speichern.
5. Nach dem ersten Deployment zeigt GitHub unter „Pages“ die öffentliche Adresse an.

Für eine eigene Domain diese erst nach einem Test der GitHub-Adresse in den Pages-Einstellungen hinterlegen und dann die von GitHub genannten DNS-Einträge beim Domainanbieter setzen. Die bestehende Domain nicht vorab umstellen, damit die aktuelle Seite erreichbar bleibt.

## Anfrageformular über Formspree

GitHub Pages liefert nur statische Dateien aus. Das Anfrageformular ist deshalb bereits mit folgendem Formspree-Endpunkt verbunden:

`https://formspree.io/f/xyezyrjy`

Nach dem Upload eine echte Testanfrage absenden und im Formspree-Dashboard Empfänger, Betreff, Benachrichtigungen und Spam-Schutz prüfen.

Im Formular ist bereits ein unsichtbares Honeypot-Feld gegen einfache Bots enthalten. Für den Produktivbetrieb sollten zusätzlich die Datenschutzerklärung und der Vertrag zur Auftragsverarbeitung des gewählten Formularanbieters geprüft werden. Das ist besonders wichtig, weil Namen, Kontaktdaten und Objektdaten verarbeitet werden.

### Warum kein `mailto:`-Formular?

`mailto:` öffnet nur das lokale Mailprogramm der besuchenden Person, funktioniert auf vielen Geräten unzuverlässig und übermittelt das Formular nicht automatisch. Ein Formular-Endpunkt ist für Anfragen deutlich robuster.

## Cookies und Datenschutz-Hinweis

Die Website verwendet keine Analyse- oder Marketing-Cookies. Der Hinweis speichert nur `gt_privacy_notice_v2` im lokalen Browser-Speicher, damit er nicht bei jedem Seitenwechsel neu erscheint. Formspree wird erst beim Absenden einer Anfrage kontaktiert; Portal24 erst beim Öffnen des Kundenportals. Über „Cookie-Einstellungen“ im Footer kann der Hinweis erneut geöffnet werden.

Die Datenschutzerklärung enthält Angaben zu Formspree und Portal24 / Immoware24. Google Fonts sind nicht eingebunden. Sobald später Google Analytics, Google Maps, YouTube, Meta Pixel oder ein anderer externer Dienst aktiviert wird, müssen Hinweis und Datenschutzerklärung vorab angepasst werden.

## Bisherige Wix-Adressen

Die bekannten Wix-Pfade sind jeweils einer passenden neuen Seite zugeordnet. Die enthaltene Datei `_redirects` sorgt auf unterstützten Hostern für echte 301-Weiterleitungen. GitHub Pages wertet diese Datei nicht aus; deshalb sind zusätzlich gleichnamige Unterordner mit sofortigen browserseitigen Weiterleitungen enthalten. Diese Ordner beim Upload nicht auslassen.

Nach dem Domainwechsel sollten die alten Adressen in der Google Search Console geprüft und die neue `sitemap.xml` eingereicht werden. Für die bestmögliche SEO-Migration ist ein Hoster mit konfigurierbaren serverseitigen 301-Weiterleitungen geeigneter als GitHub Pages.

### Alternative ohne Formspree

Wer keine externe Formularplattform nutzen möchte, braucht einen eigenen serverseitigen Endpunkt, zum Beispiel eine Cloudflare Function oder eine kleine API auf dem bestehenden Hosting. Zugangsdaten für den Mailversand dürfen niemals in `index.html` oder `script.js` stehen, weil jeder sie dort lesen könnte.

## Vor Veröffentlichung prüfen

- Echtes Logo als lokale Bilddatei ergänzen, falls die Textmarke ersetzt werden soll.
- Alle Leistungen, Preise und Rechtstexte fachlich prüfen.
- Impressum und Datenschutz auf die endgültige Domain und den Formularanbieter abstimmen.
- Testanfrage auf Mobilgerät und Desktop durchführen.
- Alle alten Wix-Adressen nach dem Domainwechsel einmal direkt aufrufen und ihr Ziel prüfen.
- Die beigefügten Weiterleitungen mindestens zwölf Monate unverändert bestehen lassen.
