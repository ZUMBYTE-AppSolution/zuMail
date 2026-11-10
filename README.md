<p align="center"><img src="assets/app-icon.png" width="112" height="112" alt="zuMail"></p>
<h1 align="center">zuMail</h1>
<p align="center">Korrespondenz mit Charakter.</p>
<p align="center"><a href="https://github.com/ZUMBYTE-AppSolution/zuMail/releases/tag/v0.1.0-alpha.6">Herunterladen</a> · <a href="docs/Anleitung.md">Anleitung</a> · <a href="CHANGELOG.md">Changelog</a> · <a href="https://www.zumbyte.de/support/">Support</a></p>
<p align="center"><img src="https://img.shields.io/badge/Windows-10%20%2F%2011%20x64-52d8f3?style=flat-square" alt="Windows x64"> <img src="https://img.shields.io/github/v/release/ZUMBYTE-AppSolution/zuMail?include_prereleases&amp;style=flat-square&amp;label=Alpha" alt="Aktuelle Alpha"></p>

**zuMail** ist ein nativer Windows-Mailclient von **Zumbyte - AppSolution**. Mehrere Arbeitsbereiche, Mailkonten, Profile und Kontakte bleiben übersichtlich erreichbar. Anthrazit oder Light Mode, eigene Akzentfarbe und verschiebbare Bereiche passen die Ansicht an deinen Alltag an.

| Ausgabe | Download |
| --- | --- |
| Windows 10 / 11 x64 · Installer | [Setup herunterladen](https://github.com/ZUMBYTE-AppSolution/zuMail/releases/download/v0.1.0-alpha.6/zuMail-0.1.0-alpha.6-win-x64-Setup.exe) |
| Windows x64 · ohne Installation | [Portable ZIP herunterladen](https://github.com/ZUMBYTE-AppSolution/zuMail/releases/download/v0.1.0-alpha.6/zuMail-0.1.0-alpha.6-win-x64-Portable.zip) |
| Prüfsummen | [SHA256SUMS.txt](https://github.com/ZUMBYTE-AppSolution/zuMail/releases/download/v0.1.0-alpha.6/SHA256SUMS.txt) |

Die benötigte .NET-Laufzeit und Chromium sind enthalten; Windows WebView2 ist nicht erforderlich. Der Installer richtet die Microsoft Visual-C++-Komponente bei Bedarf direkt über Microsoft ein; dafür sind Internet und gegebenenfalls eine Windows-Freigabe erforderlich. Im portablen Paket liegt dafür Runtime-Setup.cmd. Windows-Pakete sind derzeit unsigniert.

## Aktuelles Changelog · Alpha 6

- Überarbeitete Mailansicht mit abgestimmten Innenabständen, ruhigen Kartenflächen und kompakter Sidebar. Dark/Light Mode und die frei wählbare Akzentfarbe bleiben verfügbar.
- Schmale 4-Pixel-Scrollbars erscheinen nur im aktiven Bereich bei Maus, Tastaturfokus oder Ziehen. Die Inhaltsbreite bleibt beim Einblenden gleich; auch HTML-Mails verwenden schmale Scrollbars.
- Die separate Arbeitsbereichsleiste entfällt. Oben in der Sidebar stehen Arbeitsbereichsauswahl und „Neuer Arbeitsbereich“ zur Verfügung. Einstellungen sind in der oberen Werkzeugleiste erreichbar.

- Einstellungen in aufklappbaren Gruppen und einzelnen Unterseiten, mit Suche, klaren Einstellungsgruppen und einheitlichen Schaltern.
- Windows-Autostart und minimierter Autostart separat einstellbar unter App → Start & Hintergrund. Der normale Programmstart bleibt sichtbar; eine aktive PIN-Sperre bleibt beim minimierten Start erhalten.
- Konten und Ordner über Ziehgriffe in der Sidebar umsortieren, einschließlich automatischem Scrollen beim Ziehen. Die Reihenfolge wird verschlüsselt gespeichert. Ordner auf dem Mailserver werden dadurch nicht umbenannt oder verschoben.
- Versandkonto und zugehöriges Absenderprofil sind in jeder neuen Nachricht, Antwort und Weiterleitung direkt auswählbar. Antworten starten mit dem ursprünglichen Empfängerkonto.
- Mehrfachauswahl per Auswahlmodus, Strg oder Umschalt; alle auswählen, gelesen/ungelesen markieren, markieren, verschieben, archivieren oder in den Papierkorb legen. Sammelaktionen betreffen nur passende Mails im aktuellen Ordner, einschließlich mehrerer Konten bei Lesen/Archivieren; konversationsbezogene Antworten aus anderen Ordnern bleiben erhalten. Verschieben erfolgt innerhalb eines Kontos.
- Portable Chromium-Prüfung berücksichtigt die mitgelieferte .NET-Laufzeit auch ohne systemweite .NET-Installation.

Seit Alpha 5:

- Konversationsansicht standardmäßig aktiv: zusammengefasste Nachrichtenliste und auswählbarer Verlauf im Lesebereich, einschließlich bereits geladener Antworten aus Gesendet.
- Unter Einstellungen → Nachrichten lässt sich die Konversationsansicht abschalten; danach erscheinen Mails wieder einzeln.
- Zuordnung über Message-ID, In-Reply-To und References. Gleiche Betreffzeilen allein werden nicht zusammengelegt. Arbeitsbereiche bleiben getrennt; Kontoansichten bleiben auf ihr Konto begrenzt.
- Vorhandene verschlüsselte Nachrichten werden einmalig auf Antwortverweise geprüft. Die gespeicherten Originalmails bleiben erhalten.
- Alle Ordnerzähler zeigen ausschließlich ungelesene Nachrichten, unabhängig von der Konversationsgruppierung. Kräftige Pill-Badges verwenden die eingestellte Akzentfarbe und kontrastreiche, fette Ziffern; Nullwerte bleiben ausgeblendet.
- Beim Öffnen einer Konversationsnachricht wird nur diese als gelesen markiert. Kontoköpfe zeigen weiterhin ungelesene Mails im jeweiligen Posteingang.

Seit Alpha 4:

- Beim Öffnen werden Nachrichten sofort als gelesen markiert. Zähler aktualisieren sich direkt; ausstehende Serveränderungen werden verschlüsselt gespeichert und beim nächsten Abgleich nachgeholt.
- Die obere Sidebar-Rubrik **Alle Mailkonten** bündelt die Ordner aller Konten des aktiven Arbeitsbereichs. Jedes Konto hat darunter eine eigene, einklappbare Ordnersektion mit gespeichertem Zustand.
- HTML standardmäßig direkt im Lesebereich, mit mitgeliefertem Chromium/CEF statt Windows WebView2. Text lässt sich markieren und kopieren.
- Externe Bilder nur nach Freigabe: einmalig oder dauerhaft für die konkrete Absenderadresse. Freigaben lassen sich unter Einstellungen → Nachrichten entfernen. HTML-Seitenskripte bleiben immer deaktiviert.
- Rechtsklick oder Doppelklick öffnet Mails in einem eigenen Fenster, einschließlich Antworten, Weiterleiten und Speichern.
- Anhänge öffnen sich in einer Vorschau mit **Speichern unter**: Bilder, PDF und Text; reine Inhaltsvorschau für DOCX/XLSX/PPTX, OpenDocument und ZIP. Keine Office-Anwendung oder Makros werden gestartet.
- Eigener Business Chime bei neuen Nachrichten und Swoosh erst nach erfolgreicher SMTP-Annahme. Beide Töne separat abschaltbar und in den Einstellungen vorhörbar.

Bereits enthalten:

- IMAP/SMTP, Arbeitsbereiche, Absenderprofile und automatische Servererkennung.
- WYSIWYG-Nachrichten, Anhänge, Antworten, Weiterleiten und Entwürfe.
- Kontakte mit Empfängerwahl, Livevorschlägen und vCard-Import/-Export.
- Lokale und Serverordner über Rechtsklick; eigene Filter, Spamlisten und Automationen.
- Windows-Benachrichtigungen, IMAP IDLE, Hintergrundbetrieb, PIN und Autolock.
- Verschlüsselter Speicher, passwortgeschützte Backups und GitHub-Updater.
- Rastericon mit Brief, Z und Cyan-Glow; scharfe Buttontexte und linksbündige Navigation.

[Alle Änderungen](CHANGELOG.md) · [Versionen](https://github.com/ZUMBYTE-AppSolution/zuMail/releases)

## Funktionen

| Bereich | Enthalten |
| --- | --- |
| Mail | TLS-geschützte IMAP-/SMTP-Verbindungen, lokale Suche, Anhänge, Chromium-Leseansicht mit gesperrten Seitenskripten und freigabepflichtigen externen Bildern. |
| Verfassen | Formatierung, Listen, Links, Tabellen, eingebettete Bilder, Signaturen und Klartextalternative. Versand acht Sekunden lang stoppen. |
| Kontakte | Namen, mehrere Mailadressen und Telefonnummern, Firma, Anschriften, Daten, Foto, Notizen und weitere Felder. Wahlweise Anbieterabgleich. |
| Regeln | Absender, Betreff, Inhalt, Empfänger und Anhänge kombinieren. Verschieben, markieren, Schlagwörter und Spamaktionen; Vorschau und Verlauf. |
| Faden | Mails aus mehreren Konten eines Arbeitsbereichs mit Notizen und Aufgaben zu einem Projekt verbinden. Die Originalmails bleiben in ihren Ordnern. |
| Schutz | Lokaler AES-256-GCM-Speicher mit Windows-DPAPI, verschlüsselte Sicherungen, optionale 4-/6-stellige PIN, Quick-Lock und Autolock. |
| Ansicht | Dark/Light Mode, frei wählbare Akzentfarbe, drei Leselayouts, verstellbare Bereichsgrenzen. |

## Installation und erster Start

1. Setup ausführen oder die portable ZIP vollständig entpacken und zuMail.exe starten.
2. Einen Arbeitsbereich anlegen und **Konto verknüpfen** wählen.
3. Anbieter auswählen oder über **Freie Eingabe** die Server automatisch ermitteln lassen.
4. Mailadresse und unterstütztes Passwort bzw. App-Passwort eingeben, Serverdaten prüfen und verbinden.

Die App startet ohne vorgefertigte Konten, Mails oder Kontakte. Es gibt keinen Demo-Modus und keine Browser-Anmeldung. Anbieter, die ausschließlich Browser-OAuth erlauben, können in diesem Build nicht neu verknüpft werden. [Konten einrichten](docs/Anbieter-Anmeldung.md).

## Alpha-Stand und Daten

**176 automatische Prüfungen** einschließlich echter Chromium-Darstellung, Skript-/Netzwerksperre, großer HTML-Nachrichten, PDF-Ausgabe, Gelesen-Zählern und gespeicherten Sidebar-Zuständen. Installer und portable Ausgabe lokal erstellt; das installierte Paket wird nochmals mit dem Prüfprogramm getestet. Prüfdaten werden nicht mit der App ausgeliefert.

Pro geöffnetem IMAP-Ordner lädt dieser Build die letzten 100 Nachrichten; die Suche verwendet geladene Nachrichten. Serverlöschungen entfernen noch keine Cachekopien. Lokale Ordner lassen die Servernachricht bestehen. Neue Kontaktverbindungen verwenden CardDAV mit optionalem Zurückschreiben und Konfliktschutz. Bereits bestehende Anbieteranmeldungen bleiben gespeichert; neue Browser-Kontaktanmeldungen werden nicht angeboten. CardDAV benötigt die direkte Adressbuch-URL.

Windows-Benachrichtigungen benötigen eine laufende App bzw. Hintergrundbetrieb und beachten die Windows-Einstellungen. macOS, iOS, mobiler Push und OpenPGP/S/MIME folgen. Speicher- und Backupverschlüsselung sind bereits enthalten.

Profildaten liegen unter %LOCALAPPDATA%\Zumbyte\zuMail und bleiben bei Deinstallation erhalten. Für einen Gerätewechsel eine passwortgeschützte Sicherung exportieren.

## Hilfe und Kontakt

[Anleitung](docs/Anleitung.md) · [Fehler melden](https://github.com/ZUMBYTE-AppSolution/zuMail/issues) · [Support](https://www.zumbyte.de/support/)

Dieses Repository enthält Releases und Dokumentation. Der Entwicklungsquellcode liegt im privaten zuMail-dev-Repository. Drittkomponenten und ihre Lizenzen sind den Paketen beigefügt.

**Copyright by Zumbyte - AppSolution · made with ♥ by zumbyte**
