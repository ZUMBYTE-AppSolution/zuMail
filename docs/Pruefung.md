# Prüfung · 0.1.0-alpha.3

- 79 automatische Prüfungen erfolgreich.
- Tatsächlicher Startloader: neues Profil ohne Arbeitsbereiche, Nachrichten, Kontakte oder Verlauf; bestehendes verschlüsseltes Profil bleibt erhalten.
- Keine eingebettete Herausgeberregistrierung, kein Demo-Generator und kein Demo-Modus in der Anwendung.
- Keine interaktiven Browser-Anmeldefunktionen in Mail- und Kontaktdiensten. Gmail öffnet die manuelle App-Passwort-Einrichtung mit TLS-Serverdaten.
- Öffnen bestehender Kontoeinstellungen verändert weder Zugangsdaten noch Token. Vorhandene Token können ohne Browser mit ihrer ursprünglichen Client-Zuordnung erneuert werden.
- IMAP/SMTP gegen isolierten lokalen Testserver: Anmeldung, MIME-Empfang, HTML-Versand, Bcc-Schutz, Gesendet-Kopie, Flags, Serverordner, Verschieben, Regeln und IMAP IDLE.
- DPAPI/AES-GCM: Speicher, Manipulation, Abschneiden; passwortgeschützte Backups, fehlerhafter Import und Erhalt der Quelldaten.
- Kontakte: Arbeitsbereichstrennung, vCard-UTF-8 und unbekannte Felder, CardDAV-Konfliktschutz. Vorhandene Google-/Microsoft-Datenzuordnung mit Testantworten geprüft.
- WYSIWYG, sichere Links, entfernte Skripte und Klartextalternative; kompakte Textfelder, Text außerhalb der Glow-Ebene, linksbündige Navigation und Menürahmen.
- Installer unter Windows installiert und deinstalliert. EXE stimmt per SHA-256 mit dem Build überein. Frühere Demo-Startdateien und die Beispieldaten-Verknüpfung werden entfernt. Fremde Testdateien und Testprofil bleiben erhalten.
- Portable-Inhalt mit Builddateien verglichen; keine vorgefertigten Profile, Demo-Startdateien oder Herausgeber-Konfiguration enthalten.

Alle Testkonten und Testdaten sind isolierte Prüffixtures und werden nicht mit der App ausgeliefert. Keine echten Postfächer verändert. Native Bildschirmbedienung wurde in diesem Update nicht durchgeführt; die Oberflächenprüfungen verwenden die WPF-Komponenten direkt. macOS/iOS, mobiler Push und OpenPGP/S/MIME sind nicht Teil dieses Builds.

Maschinenlesbare Ergebnisse: verification.json und installer-verification.json im Release.
