# Prüfung · 0.1.0-alpha.7

- 202 automatische Prüfungen erfolgreich; isolierte Protokollserver und synthetische Postfächer, keine echten Konten verändert.
- Native WPF-Drop-Ereignisse und Auswahl beim Ansetzen des Ziehens; tatsächliches IMAP MOVE für mehrere Nachrichten, korrekte Ziel-UIDs, keine Duplikate nach erneuter Synchronisierung, lokale Zuordnung und Upload importierter Mails. Abgelehnte Einzelaktionen und Verbindungsfehler erhalten betroffene Originale. Kein automatisierter freihändiger Maus-Parcours.
- Neues Raster-Icon in PNG-Größen von 16 bis 1024 Pixeln und mehrstufigem ICO; transparente Außenkante und Darstellung bei kleiner Auflösung visuell geprüft.
- Konversationsketten mit gesendeten Antworten, fehlenden Eltern, Zyklen, gleichen Betreffzeilen und getrennten Arbeitsbereichen. Einmalige Bestandsindexierung erhält die originalen verschlüsselten MIME-Dateien.
- Tatsächliche WPF-Verlaufsauswahl, Abschalten in den Einstellungen, sofortige Zähleränderung je geöffneter Nachricht und fette Pill-Badges.
- Arbeitsbereichswechsel über das tatsächliche Dropdown mit Erstellen-Eintrag, schmale ausgeblendete Scrollbars und Scrolloffset-Synchronisierung des Overlay-Templates.
- Neue Oberfläche als WPF-Renderings in Dark/Light Mode, verschachtelte Einstellungen und Composer kontrolliert. Reale Konten bleiben unberührt.
- Autostart-Registrierung in isoliertem HKCU-Testschlüssel, unabhängige Minimierung und PIN-Sperre beim minimierten Start; kein echter Windows-Neustart oder Ab-/Anmeldevorgang automatisiert.
- Konten-/Ordnersortierung mit Persistenz und Bereichsschutz; Sammelauswahl liest nicht automatisch, Sammelaktionen bewahren konversationsbezogene Mails anderer Ordner und verhindern kontenfremdes Verschieben.
- Tatsächliche Konto-/Profilwahl beim Verfassen und Antworten, inklusive erzeugtem MIME-Absender und erhaltenen Antwortverweisen.
- Sofortige Gelesen-Markierung, PropertyChanged-Bindung, verschlüsselte Speicherung, ausstehende Änderungen bei Netzwerkfehlern und vorübergehend deaktivierten Konten; tatsächliches Seen-Flag am IMAP-Testserver.
- Sammelordner über mehrere Konten, Arbeitsbereichstrennung, gleichnamige Ordner, gespeicherte Aufklappzustände und tatsächliche WPF-Nachrichtenliste.
- Markierbarer Klartext mit nativem Kopierbefehl, eigenes Mailfenster und Rechtsklickmenü.
- Tatsächlich mitgeliefertes Chromium: HTML-Inhalt, deaktivierte Seitenskripte und blockierte externe Requests, Dokumente über 2 MiB, gerenderte PDF-Seite anhand eines Bildnachweises. Kein Windows WebView2 erforderlich.
- Externe Bilder nur nach Freigabe, Rasterbilder eingebettet, CSS-Bilder berücksichtigt, keine Browsercookies. Private Netzadressen, lokale Dateien, gefährliche Umleitungen und SVG-Antworten abgewiesen. Absendervertrauen gilt für die tatsächliche Adresse, nicht den Anzeigenamen.
- Anhangvorschau und Speichern erhalten die dekodierten Originalbytes; Office-Inhaltsvorschau ohne Office-Prozess, externe XML-Entitäten abgewiesen, ausführbare Dateien nicht gestartet.
- Benachrichtigungston und Versand-Swoosh als eigene PCM-Dateien; separate, gespeicherte Schalter. Audio wurde in der automatischen Prüfung nicht über Lautsprecher abgespielt.
- Bestehende Prüfungen für MIME/SMTP/Bcc, Serverordner, Regeln, IMAP IDLE, WYSIWYG, Kontakte, DPAPI/AES-GCM und Sicherungen weiterhin erfolgreich.
- Installer installiert und deinstalliert; vollständige Chromium-Ressourcen mit dem Build verglichen und Prüfprogramm gegen das installierte Paket ausgeführt. Fremde Testdateien und Profile erhalten. Keine Beispieldaten oder OAuth-Registrierung mitgeliefert.
- Signierter Microsoft-Runtime-Download geprüft. Auf dem Prüfgerät war die passende Visual-C++-Komponente bereits vorhanden; eine Neuinstallation auf einer Referenz-VM wurde nicht durchgeführt.

Die Rendererprüfung erzeugt ausschließlich eigene, unsichtbare Testfenster. Es wurden keine Konten, Mails oder Dokumente des Benutzers in die Tests aufgenommen. macOS/iOS, mobiler Push und OpenPGP/S/MIME bleiben außerhalb dieses Builds. Maschinenlesbare Ergebnisse liegen als verification.json und installer-verification.json im Release.
