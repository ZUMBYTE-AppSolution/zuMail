# Changelog

## 0.1.0-alpha.5

- Konversationsansicht standardmäßig aktiv: zusammengefasste Nachrichtenliste und auswählbarer Verlauf im Lesebereich, einschließlich bereits geladener Antworten aus Gesendet.
- Unter Einstellungen → Nachrichten lässt sich die Konversationsansicht abschalten; danach erscheinen Mails wieder einzeln.
- Zuordnung über Message-ID, In-Reply-To und References. Gleiche Betreffzeilen allein werden nicht zusammengelegt. Arbeitsbereiche bleiben getrennt; Kontoansichten bleiben auf ihr Konto begrenzt.
- Vorhandene verschlüsselte Nachrichten werden einmalig auf Antwortverweise geprüft. Die gespeicherten Originalmails bleiben erhalten.
- Alle Ordnerzähler zeigen ausschließlich ungelesene Nachrichten, unabhängig von der Konversationsgruppierung. Kräftige Pill-Badges verwenden die eingestellte Akzentfarbe und kontrastreiche, fette Ziffern; Nullwerte bleiben ausgeblendet.
- Beim Öffnen einer Konversationsnachricht wird nur diese als gelesen markiert. Kontoköpfe zeigen weiterhin ungelesene Mails im jeweiligen Posteingang.

143 automatische Prüfungen, Installer-/Deinstallationstest und Prüfung des installierten Pakets. Keine Beispieldaten.

## 0.1.0-alpha.4

- Beim Öffnen werden Nachrichten sofort als gelesen markiert. Zähler aktualisieren sich direkt; ausstehende Serveränderungen werden verschlüsselt gespeichert und beim nächsten Abgleich nachgeholt.
- Die obere Sidebar-Rubrik **Alle Mailkonten** bündelt die Ordner aller Konten des aktiven Arbeitsbereichs. Jedes Konto hat darunter eine eigene, einklappbare Ordnersektion mit gespeichertem Zustand.
- HTML standardmäßig direkt im Lesebereich, mit mitgeliefertem Chromium/CEF statt Windows WebView2. Text lässt sich markieren und kopieren.
- Externe Bilder nur nach Freigabe: einmalig oder dauerhaft für die konkrete Absenderadresse. Freigaben lassen sich unter Einstellungen → Nachrichten entfernen. HTML-Seitenskripte bleiben immer deaktiviert.
- Rechtsklick oder Doppelklick öffnet Mails in einem eigenen Fenster, einschließlich Antworten, Weiterleiten und Speichern.
- Anhänge öffnen sich in einer Vorschau mit **Speichern unter**: Bilder, PDF und Text; reine Inhaltsvorschau für DOCX/XLSX/PPTX, OpenDocument und ZIP. Keine Office-Anwendung oder Makros werden gestartet.
- Eigener Business Chime bei neuen Nachrichten und Swoosh erst nach erfolgreicher SMTP-Annahme. Beide Töne separat abschaltbar und in den Einstellungen vorhörbar.

117 automatische Prüfungen, Installer-/Deinstallationstest und Prüfung des tatsächlich installierten Chromium-Pakets. Keine OAuth-Browser-Anmeldung und keine Beispieldaten im Programm.

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
