# Prüfung · 0.1.0-alpha.11

285 automatische Prüfungen mit getrennten Testprofilen und eigenen IMAP-/SMTP-Testservern. Es wurden keine echten Mailkonten, Kontakte oder Dokumente verändert.

## Neu in Alpha 11 geprüft

- Echte lokale Aktivierungsanfragen zwischen getrennten Prozessen, mehrere gleichzeitige Starts, ungültige Anfragen, Abbruch und Trennung verschiedener Profile.
- Wiederherstellung des tatsächlichen minimierten und versteckten WPF-Hauptfensters. Maximierte Ansichten bleiben maximiert; PIN-Sperre und verborgener Mailinhalt bleiben erhalten.
- Die Windows-Freigabe für den Vordergrundwechsel wird beim ausdrücklichen Zweitstart an die bestehende Instanz übergeben. Die automatisierten Fensterprüfungen verwenden unsichtbare Testfenster ohne Eingriff in den Desktop des Benutzers; ein manueller Start aus Explorer wurde nicht automatisiert.
- Native Markdown-Darstellung mit tatsächlichen Überschriften, Listen, fettem Text, Tabellen, Code und funktionierenden Links. Kopierbarer Text und Dark/Light Mode geprüft.
- Screenshots aus begrenzten Rasterdaten angezeigt. Nur Bilder aus der offiziellen Releasequelle werden automatisch geladen; fremde Bilder bleiben verlinkt. Skript- und lokale Dateilinks sind nicht ausführbar; HTML bleibt Text.

## Weiterhin geprüft

- Kontakte: Suche über mehrere Felder, Arbeitsbereichs- und Adressbuchgrenzen, leere Ergebnisse, strukturierte Bearbeitung, ungültige Mailadressen und Speicherung im verschlüsselten Profil.
- Datenbestand: Bearbeiten und Abbrechen verändern die Originalkontakte nicht vor dem Speichern. Zusätzliche vCard-Felder, Anbieterzuordnung und ETags bleiben erhalten. Abbrechen der Adressbuchbearbeitung erhält bestehende Zugangsdaten.
- Farbauswahl: HSV-Farbberechnung, Vorschau und Übernehmen im tatsächlichen WPF-Fenster. Gemeinsamer Picker für Akzent- und Textfarbe.
- Update-Download: gestreamte HTTP-Antworten, bekannte und unbekannte Dateigröße, Zwischenfortschritte, Abbruch, unvollständige und beschädigte Dateien. Ein vorhandener gültiger Download bleibt bei Fehlern erhalten; unvollständige Dateien werden entfernt.
- Updatefenster: tatsächliche Anzeige von Prozent, Datenmenge und Geschwindigkeit, unbestimmter Fortschritt sowie Abbruch über den Button. Download und Dateiprüfung sind getrennte Phasen.
- Installer: Installation und erneute Update-Installation im getrennten Prüfverzeichnis. Warten auf den bisherigen Prozess und anschließender Start mit demselben PIN-geschützten Testprofil; Profilpfad enthält Leerzeichen und Umlaute. Der verschlüsselte Profilschlüssel bleibt unverändert.
- Hauptfenster: Schließen nach unmittelbar abgeschlossenem Speichern ohne erneuten Aufruf innerhalb des laufenden Schließereignisses.

## Bestehende Funktionen

- Native WPF-Bedienung von Konten, Konversationen, Zählern, Mehrfachauswahl, Regeln, Verfassen, Entwürfen und Absenderprofilen.
- IMAP MOVE mit mehreren Nachrichten, Ziel-UIDs, erneute Synchronisierung, lokale Zuordnung und Upload. Serverfehler lassen betroffene Originale erhalten.
- SMTP-Versand aus dem Verfassen-Fenster, Bcc-Schutz und Abbruch des verzögerten Versands.
- Mitgeliefertes Chromium: HTML-Inhalt, auswählbarer Text, blockierte Seitenskripte und externe Requests, PDF-Seite anhand einer Bildprüfung. Anhangspeicherung erhält die Originalbytes.
- Einheitliche Dialoge und Kontextmenüs, Dark/Light Mode, Einstellungsnavigation, tatsächlich 2 Pixel breite Scrollleisten und gespeicherte Sidebar-Reihenfolge.
- Tondateien mit abgesenktem Pegel, gemeinsame Lautstärke und separate Schalter. Kein automatisierter Hörtest über Lautsprecher.
- Verschlüsselter Speicher, PIN, Sicherungen und Windows-Autostart in einem getrennten Registrierungsschlüssel. Kein automatisierter Windows-Ab-/Anmeldevorgang.

## Pakete

- Dieselben 285 Prüfungen gegen das tatsächlich installierte Paket ausgeführt.
- Installierte Programmdatei und Chromium-Ressourcen mit dem Build verglichen. Portable ZIP Datei für Datei gegen den Build geprüft.
- Deinstallation entfernt die Programmdateien und erhält fremde Testdateien und Profile. Bestehende Startmenüverknüpfungen und Registrierungseinträge des Prüfgeräts werden nach dem Test wiederhergestellt.
- Keine Beispieldaten, vorbereiteten Profile oder OAuth-Registrierungen enthalten. Inhalte der Screenshots stammen ausschließlich aus den getrennten Testläufen.
- Prüfsummen der öffentlichen Downloads mit den lokalen Paketen verglichen. Berichte: `verification.json` und `installer-verification.json` in den Release-Dateien.

Die Fensterprüfungen nutzen eigene unsichtbare WPF-Fenster. Eine Neuinstallation der Visual-C++-Komponente auf einer Referenz-VM wurde nicht geprüft; auf dem Prüfgerät ist sie vorhanden. Windows-Pakete sind derzeit unsigniert. macOS/iOS, mobiler Push und OpenPGP/S/MIME sind nicht Bestandteil dieses Builds.
