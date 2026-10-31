# Prüfung · 0.1.0-alpha.1

- 79 automatische Prüfungen erfolgreich.
- IMAP und SMTP gegen einen getrennten lokalen Protokollserver: Anmeldung, MIME-Empfang, HTML-Versand, Bcc-Schutz, Gesendet-Kopie, Flags, Serverordner, Verschieben, Regelaktionen und IMAP IDLE.
- Windows-DPAPI und AES-GCM-Speicher: vollständiger Nachrichtenabruf, Manipulation und Abschneiden werden abgewiesen.
- Passwortsicherungen: Verifikation, falsches Passwort, beschädigter Import, unveränderte Quelldaten und korrekte Kontaktzuordnung beim Wiederherstellen.
- Kontakte: Arbeitsbereichstrennung, sekundäre Mailadressen, vCard-UTF-8 und unbekannte Felder, Google-/Microsoft-Testantworten, CardDAV-ETag-Konflikte.
- WYSIWYG: Formatierung, sichere Links, entfernte Skripte und Klartextalternative.
- Oberfläche: 32-px-Textfelder, Text außerhalb der Glow-Ebene, linksbündige Navigation, pixelgenaue Textdarstellung und Menürahmen.
- Updateprüfung: Versionsvergleich, fremde Downloadquellen, öffentlicher Releasefeed bei API-Limit und stabile Versionswahl.
- Browseranmeldung: externer Anbieteraufruf, Loopback-Rückkehr, falscher State, PKCE-Codeaustausch und Kontoübernahme für Google und Microsoft mit getrennten Testantworten. Gmail-/Live-Oberfläche bietet vor der manuellen Eingabe den Browser-Login an.
- Tatsächlicher Installer unter Windows ausgeführt. Installierte EXE stimmt per SHA-256 mit dem Build überein. Programmstart und native Oberfläche geprüft. Deinstallation entfernt Programm und Verknüpfungen und erhält fremde Dateien sowie ein Profilverzeichnis.
- Dark/Light, Empfängervorschlag, gespeicherter WYSIWYG-Entwurf und Kontextmenü in der tatsächlichen WPF-Oberfläche geprüft.
- Abhängigkeiten: zum Prüfzeitpunkt keine bekannten anfälligen Pakete im NuGet-Audit.

Die Mailprotokollprüfungen verwenden ausschließlich synthetische Konten auf Loopback. Google-/Microsoft-Zugriffe wurden mit Anbieterantworten als Testdaten geprüft; echte OAuth-Anmeldung erfordert noch die eigene Anbieterregistrierung. Die Windows-Testbenachrichtigung wurde aus der App ausgelöst; eine Zustellung auf gesperrten mobilen Geräten wurde nicht geprüft. macOS/iOS und OpenPGP/S/MIME sind nicht Teil dieses Builds.

Maschinenlesbare Ergebnisse liegen im Release als verification.json und installer-verification.json.
