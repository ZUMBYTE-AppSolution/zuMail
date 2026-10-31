# Changelog

## 0.1.0-alpha.3

- Browser-Anmeldung für Mail und Kontakte entfernt; manuelle IMAP-/SMTP-Einrichtung mit Passwort oder App-Passwort.
- Gemeinsame Google-Registrierung aus dem Programm entfernt.
- Beispieldaten-Generator und Demo-Modus entfernt. Neue Profile starten vollständig leer.
- Keine Demo-Dateien oder Demo-Verknüpfungen in Installer und Portable-Paket. Installer entfernt alte Demo-Startoptionen beim Update.
- Vorhandene Profile, Nachrichten und Kontakte bleiben erhalten. Neue Kontaktverbindungen über CardDAV, weiterhin vCard-Import/-Export.
- 79 automatische Prüfungen sowie Installer- und Paketprüfung.

## 0.1.0-alpha.2

- Gemeinsame Google-Desktop-Registrierung mit der App ausgeliefert. Mailnutzer brauchen keine eigenen OAuth-Schlüssel.
- Gmail-Auswahl startet direkt die Anmeldung im Standardbrowser; nach Zustimmung automatische Kontoübernahme und Verbindungsprüfung.
- Entwicklerkonfiguration aus dem normalen Anmeldeablauf und den Einstellungen entfernt.
- Bestehende Mail- und Kontaktanmeldungen behalten ihre ursprüngliche Client-Zuordnung für die Token-Erneuerung.
- Fehlende Microsoft-Herausgeberregistrierung wird durch ein App-Update ergänzt; keine Einrichtung durch Mailnutzer.
- 86 automatische Prüfungen und separat geprüfter Windows-Installer.

Google-Testmodus und öffentliche Gmail-Freigabe bleiben Aufgaben des Herausgebers. Die Microsoft-Anwendungs-ID liegt noch nicht vor. Keine echte Google-/Microsoft-Kontoanmeldung durchgeführt.

## 0.1.0-alpha.1

Erster nutzbarer Windows-Alpha-Build.

- WPF mit Dark/Light, Akzentwahl, verschiebbaren Bereichen und kompakten Textfeldern.
- Arbeitsbereiche, IMAP/SMTP, Mailprofile und automatische Servererkennung.
- Empfang, Versand, Anhänge, Entwürfe und WYSIWYG.
- Lokale und IMAP-Serverordner über Rechtsklick.
- Kontakte, vCards, Empfängerwahl und Livevorschläge; optionale Anbieteranbindung.
- Filter, Spamlisten, Automationen, Vorschau und Verlauf.
- Faden für projektbezogene Mails, Notizen und Aufgaben.
- Windows-Benachrichtigungen und Hintergrundbetrieb.
- Verschlüsselter Speicher, Backups, PIN und Autolock.
- GitHub-Updater, lokal gebauter Installer und portable Ausgabe.
- Flaches Cyan-Mailicon mit Z, dezentem Glow und mehreren Rasterauflösungen.
- Scharfe Buttonbeschriftungen durch getrennten Glow; linksbündige Navigation in Mailansicht und Einstellungen.
- Kontextmenüs ohne weißen Systemrahmen und neutrale Scrollleisten.
- Updateprüfung mit öffentlichem Releasefeed als Ausweichweg bei GitHub-Anfragelimits.
- Gmail und Live/Outlook starten mit „Mit Google/Microsoft anmelden“. Browser-Rückkehr, automatische Kontoübernahme und eigener Assistent für die notwendige Anbieterregistrierung.

Google-/Microsoft-App-Registrierungen sind noch einzurichten. macOS, iOS, mobiler Push und OpenPGP/S/MIME folgen. Grenzen und Datenverhalten: siehe README.
