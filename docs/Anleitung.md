# zuMail · Erste Schritte

## Arbeitsbereiche und Konten

Über das Plus links einen Arbeitsbereich anlegen. Darin **Konto verknüpfen** öffnen und einen Anbieter oder **Freie Eingabe** auswählen. Nach Eingabe der Mailadresse versucht zuMail, IMAP-/SMTP-Server und Ports zu ermitteln. Serverwerte, Benutzername und Passwort bzw. App-Passwort eintragen und **Speichern & verbinden** wählen. TLS-Zertifikate werden geprüft.

Browser-Anmeldung und OAuth-Einrichtung sind entfernt. Verwendet ein Anbieter ausschließlich Browser-OAuth, kann er in diesem Build nicht neu verknüpft werden. [Einrichtung und Grenzen](Anbieter-Anmeldung.md).

Die App startet mit einem leeren Profil. Es werden keine Beispieldaten angelegt. Vorhandene Profile und Nachrichten bleiben erhalten.

Mailprofile unter **Einstellungen → Konten & Profile** bestimmen Namen, Absenderadresse, Antwortadresse und Signatur. Der Versand nutzt die Verbindung des zugeordneten Kontos.

## Lesebereich und Sidebar

**Alle Mailkonten** zeigt die Sammelordner des aktiven Arbeitsbereichs. Die Kontorubriken darunter zeigen ausschließlich die Ordner des jeweiligen Kontos. Der Pfeil am Kontonamen klappt sie auf oder zu; die Auswahl wird verschlüsselt gespeichert.

Ein Klick auf eine Nachricht markiert sie sofort als gelesen und aktualisiert die Zähler. Eine automatische Vorauswahl beim Abruf zählt nicht als Öffnen. Bei fehlender Verbindung bleibt der neue Status lokal erhalten und wird später auf den Server übertragen. Die Zähler beziehen sich auf die lokal geladenen Nachrichten.

HTML wird standardmäßig im Detailbereich angezeigt. Mit **HTML / Text** lässt sich die Ansicht wechseln; die Vorgabe steht unter **Einstellungen → Nachrichten**. Text kann in beiden Ansichten markiert und mit Strg+C kopiert werden. Rechtsklick **In eigenem Fenster öffnen** oder Doppelklick öffnet eine eigene Leseansicht.

**Bilder laden** fragt vor dem Download externer Bilder. Ohne Häkchen gilt die Freigabe für diese Nachricht; mit **Bilder von … immer laden** für die konkrete Absenderadresse innerhalb dieses Arbeitsbereichs. Entfernen unter **Einstellungen → Nachrichten**. Die Freigabe erlaubt keine HTML-Seitenskripte, eingebetteten Webseiten oder automatischen Downloads. Bilder werden ohne Browsercookies abgerufen und vor der Darstellung eingebettet. Lokale Netzadressen sind gesperrt.

## Anhangvorschau und Töne

Auf einen Anhang klicken: Vorschaufenster mit **Speichern unter**. Unterstützt werden übliche Rasterbilder, PDF, Text und EML. DOCX/XLSX/PPTX sowie OpenDocument zeigen eine Inhaltsvorschau; ZIP zeigt seine Dateiliste. Makros und enthaltene Programme werden nicht ausgeführt. Office-Layouttreue und ältere binäre Office-Formate sind nicht enthalten. Die Vorschau ist auf 32 MiB begrenzt; Speichern bleibt auch bei größeren oder nicht unterstützten Dateien möglich.

Unter **Einstellungen → Allgemein** lassen sich **Business Chime** für neue Nachrichten und **Swoosh** nach erfolgreichem Versand unabhängig abschalten oder vorhören. Der Versandton ertönt nach Annahme durch den SMTP-Server, nicht während des Widerruf-Countdowns oder bei einem Fehler.

## Ordner, Regeln und Spam

Rechtsklick in die Ordnerleiste bzw. auf einen eigenen Ordner. Beim Erstellen entscheidet **Auf dem Mailserver erstellen**, ob der Ordner beim Anbieter oder nur in zuMail liegt. Eine lokale Einordnung lässt die Nachricht auf dem Server im bisherigen Ordner bestehen.

Nachrichten per Rechtsklick **Verschieben …** einordnen. Serverordner werden auf dem Server geändert; nur leere eigene Ordner können entfernt werden.

Unter **Regeln & Filter** Bedingungen und Aktionen kombinieren. Neue Nachrichten nach dem ersten Abruf werden automatisch geprüft. Auf vorhandene Nachrichten Regeln erst über die Vorschau anwenden. Freigaben, Sperrlisten und Schlüsselwörter steuern den lokalen Spamfilter.

## Nachrichten und Kontakte

**Verfassen** öffnet den WYSIWYG-Editor. An, Cc und Bcc bieten Kontakte beim Tippen an. Mit Pfeiltasten und Eingabe übernehmen oder das Kontaktsymbol für die Auswahl öffnen. Mehrere Adressen werden durch Kommas getrennt.

**Kontakte** verwaltet das Adressbuch des Arbeitsbereichs, importiert und exportiert vCards. Unter **Adressbücher** lässt sich die Synchronisierung je Anbieter aktivieren. Neue Browser-Kontaktanmeldungen sind entfernt; bestehende Kontakte bleiben erhalten. CardDAV benötigt die direkte HTTPS-Adresse des Adressbuchs; Zurückschreiben ist ein eigener Schalter.

## Sicherheit und Sicherung

Unter **Einstellungen → Sicherheit** vier- oder sechsstellige PIN und Autolock einrichten. Quick-Lock: Strg+Umschalt+L. Die PIN sperrt die Oberfläche. Lokale Kontodaten und der Nachrichtenspeicher sind mit AES-256-GCM verschlüsselt; Windows-DPAPI schützt den Schlüssel für das aktuelle Benutzerkonto.

Unter **Import & Export** Nachrichten bzw. eine passwortgeschützte Sicherung exportieren. Für Gerätewechsel diese Sicherung verwenden. Den Profilordner allein zu kopieren genügt wegen der Windows-Benutzerbindung nicht. Ein verlorenes Backup-Passwort kann nicht zurückgesetzt werden.

## Updates und Deinstallation

**Einstellungen → Updates** bietet Alpha- und stabile Versionen. Der Installer wird aus dem offiziellen Release-Repository bezogen und vor dem Start mit SHA-256 geprüft. Windows-Pakete sind noch nicht Authenticode-signiert.

Deinstallation entfernt Programm und Verknüpfungen, erhält jedoch Profildaten. Im portablen Paket bedeutet „portabel“ Start ohne Installation; das Profil bleibt standardmäßig im Windows-Benutzerverzeichnis.

## Bekannte Grenzen

Windows 10/11 x64. macOS/iOS und mobiler Push folgen. OpenPGP-/S/MIME-Nachrichtenverschlüsselung ist noch nicht enthalten. Chromium ist enthalten; Windows WebView2 wird nicht benötigt.

IMAP-Cache: standardmäßig die letzten 100 Nachrichten pro geöffnetem Ordner, einstellbar auf 20–1000. Suche findet geladene Nachrichten. Serverlöschungen werden noch nicht in den lokalen Cache übernommen.

Google/Microsoft-Kontakte: Abgleich vom Anbieter, Änderungen lokal. CardDAV: optional beide Richtungen mit ETags. Fehlende Serverkontakte bleiben als lokale Kopie erhalten. Weitere Microsoft-Kontaktunterordner, automatische CardDAV-Principalsuche und Kontaktfotoabruf über Google/Microsoft sind noch nicht enthalten.

Benachrichtigungen unter Windows verwenden den laufenden Client bzw. Hintergrundbetrieb. Das ist noch kein plattformübergreifender Pushdienst.

## Browser-Komponente und Lizenzen

Chromium/CEF und .NET sind enthalten. Falls die Microsoft-Visual-C++-Komponente fehlt, übernimmt der Installer die Einrichtung über einen Download direkt von Microsoft und prüft dessen digitale Signatur. Portable Nutzer können Runtime-Setup.cmd ausführen; die Einrichtung erfordert gegebenenfalls eine Windows-Administratorfreigabe. Das tatsächliche Neuinstallieren dieser Systemkomponente wurde auf dem Prüfgerät nicht benötigt.

Vollständige Drittanbieterhinweise liegen im Paket unter licenses/, einschließlich der Hinweise der tatsächlich ausgelieferten Chromium-Version. Chromium, CEF und CefSharp gestatten kommerzielle Nutzung unter ihren jeweiligen Lizenzbedingungen.
