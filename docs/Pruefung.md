# Prüfung · 0.1.0-alpha.2

- 86 automatische Prüfungen erfolgreich.
- IMAP und SMTP gegen einen getrennten lokalen Protokollserver: Anmeldung, MIME-Empfang, HTML-Versand, Bcc-Schutz, Gesendet-Kopie, Flags, Serverordner, Verschieben, Regelaktionen und IMAP IDLE.
- Windows-DPAPI und AES-GCM-Speicher: vollständiger Nachrichtenabruf, Manipulation und Abschneiden werden abgewiesen.
- Passwortsicherungen: Verifikation, falsches Passwort, beschädigter Import, unveränderte Quelldaten und korrekte Kontaktzuordnung beim Wiederherstellen.
- Kontakte: Arbeitsbereichstrennung, sekundäre Mailadressen, vCard-UTF-8 und unbekannte Felder, Google-/Microsoft-Testantworten, CardDAV-ETag-Konflikte.
- WYSIWYG: Formatierung, sichere Links, entfernte Skripte und Klartextalternative.
- Oberfläche: 32-px-Textfelder, Text außerhalb der Glow-Ebene, linksbündige Navigation, pixelgenaue Textdarstellung und Menürahmen.
- Updateprüfung: Versionsvergleich, fremde Downloadquellen, öffentlicher Releasefeed bei API-Limit und stabile Versionswahl.
- Browseranmeldung: externer Anbieteraufruf, Loopback-Rückkehr, falscher State, PKCE-Codeaustausch und Kontoübernahme für Google und Microsoft mit getrennten Testantworten. Ein neues Profil erhält die gemeinsame Google-Registrierung aus der kompilierten App. Die Gmail-Auswahl startet die Anmeldung direkt, ohne Formular oder Schlüssel-Eingabe.
- Migration: Herausgeber-Voreinstellungen für beide Anbieter; vorhandene Mail- und Kontaktanmeldungen behalten ihre ausstellende Client-ID. Die Token-Erneuerung verwendet nach dem Update diese ursprüngliche Registrierung.
- Tatsächlichen Alpha-2-Installer unter Windows installiert und deinstalliert. Installierte EXE stimmt per SHA-256 mit dem Build überein. Deinstallation entfernt das Programm und erhält fremde Dateien sowie ein Profilverzeichnis.
- Dark/Light, Empfängervorschlag, gespeicherter WYSIWYG-Entwurf und Kontextmenü wurden in Alpha 1 in der tatsächlichen WPF-Oberfläche geprüft. Alpha 2 ergänzt die automatischen Anmeldeprüfungen; keine neue Bildschirmbedienung oder echte Anbieteranmeldung durchgeführt.
- Abhängigkeiten: zum Prüfzeitpunkt keine bekannten anfälligen Pakete im NuGet-Audit.

Die Mailprotokollprüfungen verwenden ausschließlich synthetische Konten auf Loopback. Google-/Microsoft-Zugriffe wurden mit Anbieterantworten als Testdaten geprüft; eine echte Anmeldung wurde noch nicht durchgeführt. Die Google-Registrierung ist enthalten, ihre öffentliche Anbieterfreigabe wurde nicht geprüft. Die Microsoft-Anwendungs-ID des Herausgebers fehlt noch. Die Windows-Testbenachrichtigung wurde in Alpha 1 aus der App ausgelöst; eine Zustellung auf gesperrten mobilen Geräten wurde nicht geprüft. macOS/iOS und OpenPGP/S/MIME sind nicht Teil dieses Builds.

Maschinenlesbare Ergebnisse liegen im Release als verification.json und installer-verification.json.
