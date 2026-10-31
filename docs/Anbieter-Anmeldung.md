# Konten einrichten

Unter **Konto verknüpfen** einen Anbieter oder **Freie Eingabe** wählen. Für neue Konten verwendet zuMail IMAP und SMTP mit Passwort bzw. einem vom Anbieter unterstützten App-Passwort. Die App enthält keine Browser-Anmeldung, keine Schlüssel-Eingabe und keine gemeinsame OAuth-Registrierung.

1. Arbeitsbereich anlegen und **Konto verknüpfen** öffnen.
2. Anbieter auswählen. Gmail und iCloud haben vorbereitete Serverdaten; **Freie Eingabe** ermittelt die Konfiguration nach Eingabe der Mailadresse.
3. Mailadresse, Anzeigename und Passwort bzw. App-Passwort eintragen. Benutzername kann leer bleiben, wenn er der Mailadresse entspricht.
4. IMAP-/SMTP-Server, Ports und sichere Verbindung prüfen. **Speichern & verbinden** prüft Empfang und Versand, bevor das Konto übernommen wird.

Nicht jeder Anbieter erlaubt die Anmeldung mit dem normalen Kontopasswort. Ein erforderliches App-Passwort wird beim jeweiligen Mailanbieter erstellt. Wenn ein Anbieter ausschließlich Browser-OAuth erlaubt, ist eine neue Kontoverknüpfung in diesem Build nicht möglich.

Kontakte lassen sich lokal verwalten und als vCards importieren/exportieren. Unter **Adressbücher** eine direkte HTTPS-CardDAV-Adresse mit Benutzername und Passwort/App-Passwort hinterlegen. Das Zurückschreiben von Änderungen ist optional.

Vorhandene Konten, verschlüsselte Profile und Kontakte bleiben erhalten. Frühere OAuth-Verbindungen werden nicht gelöscht; solange der Anbieter die gespeicherte Anmeldung akzeptiert, kann sie ohne neue Browser-Anmeldung weiter genutzt werden. Beim Speichern einer Umstellung auf Passwort wird die neue Verbindung zuerst geprüft.

Neue Installationen enthalten keine Arbeitsbereiche, Konten, Nachrichten oder Kontakte. Es werden keine Beispieldaten erzeugt. Installer und Portable-Paket enthalten keine Demo-Startoption.
