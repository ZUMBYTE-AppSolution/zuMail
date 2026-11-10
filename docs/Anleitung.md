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

## Konversationsansicht und Ungelesen-Zähler

- Konversationsansicht standardmäßig aktiv: zusammengefasste Nachrichtenliste und auswählbarer Verlauf im Lesebereich, einschließlich bereits geladener Antworten aus Gesendet.
- Unter Einstellungen → Nachrichten lässt sich die Konversationsansicht abschalten; danach erscheinen Mails wieder einzeln.
- Zuordnung über Message-ID, In-Reply-To und References. Gleiche Betreffzeilen allein werden nicht zusammengelegt. Arbeitsbereiche bleiben getrennt; Kontoansichten bleiben auf ihr Konto begrenzt.
- Vorhandene verschlüsselte Nachrichten werden einmalig auf Antwortverweise geprüft. Die gespeicherten Originalmails bleiben erhalten.
- Alle Ordnerzähler zeigen ausschließlich ungelesene Nachrichten, unabhängig von der Konversationsgruppierung. Kräftige Pill-Badges verwenden die eingestellte Akzentfarbe und kontrastreiche, fette Ziffern; Nullwerte bleiben ausgeblendet.
- Beim Öffnen einer Konversationsnachricht wird nur diese als gelesen markiert. Kontoköpfe zeigen weiterhin ungelesene Mails im jeweiligen Posteingang.

Konversationen verwenden lokal geladene Nachrichten des aktiven Arbeitsbereichs. Eine Kontoansicht berücksichtigt nur dieses Konto; Spam und Papierkorb erscheinen nicht als zusätzlicher Verlauf in normalen Ordnern. Antworten werden über ihre Mail-Header zugeordnet. Ohne Antwortverweise bleibt eine Mail einzeln. Entwürfe bleiben separat. Die Suche und Filter bestimmen, welche Konversationen angezeigt werden; zugehörige geladene Nachrichten bleiben im Verlauf erreichbar. Die Ordnerzähler zählen ungelesene Mails, keine Konversationen.

## Oberfläche und Bedienung ab Alpha 6

- Überarbeitete Mailansicht mit abgestimmten Innenabständen, ruhigen Kartenflächen und kompakter Sidebar. Dark/Light Mode und die frei wählbare Akzentfarbe bleiben verfügbar.
- Schmale 4-Pixel-Scrollbars erscheinen nur im aktiven Bereich bei Maus, Tastaturfokus oder Ziehen. Die Inhaltsbreite bleibt beim Einblenden gleich; auch HTML-Mails verwenden schmale Scrollbars.
- Die separate Arbeitsbereichsleiste entfällt. Oben in der Sidebar stehen Arbeitsbereichsauswahl und „Neuer Arbeitsbereich“ zur Verfügung. Einstellungen sind in der oberen Werkzeugleiste erreichbar.

- Einstellungen in aufklappbaren Gruppen und einzelnen Unterseiten, mit Suche, klaren Einstellungsgruppen und einheitlichen Schaltern.
- Windows-Autostart und minimierter Autostart separat einstellbar unter App → Start & Hintergrund. Der normale Programmstart bleibt sichtbar; eine aktive PIN-Sperre bleibt beim minimierten Start erhalten.
- Konten und Ordner über Ziehgriffe in der Sidebar umsortieren, einschließlich automatischem Scrollen beim Ziehen. Die Reihenfolge wird verschlüsselt gespeichert. Ordner auf dem Mailserver werden dadurch nicht umbenannt oder verschoben.
- Versandkonto und zugehöriges Absenderprofil sind in jeder neuen Nachricht, Antwort und Weiterleitung direkt auswählbar. Antworten starten mit dem ursprünglichen Empfängerkonto.
- Mehrfachauswahl per Auswahlmodus, Strg oder Umschalt; alle auswählen, gelesen/ungelesen markieren, markieren, verschieben, archivieren oder in den Papierkorb legen. Sammelaktionen betreffen nur passende Mails im aktuellen Ordner, einschließlich mehrerer Konten bei Lesen/Archivieren; konversationsbezogene Antworten aus anderen Ordnern bleiben erhalten. Verschieben erfolgt innerhalb eines Kontos.
- Portable Chromium-Prüfung berücksichtigt die mitgelieferte .NET-Laufzeit auch ohne systemweite .NET-Installation.

**Auswählen:** Den Auswahlknopf neben den Listenfiltern nutzen oder Strg/Umschalt beim Klicken halten. In der Auswahlleiste stehen die Sammelaktionen bereit. Mit Fertig oder Esc die Auswahl beenden. Die Auswahl allein markiert keine Mail als gelesen.

**Windows-Start:** Einstellungen → App → Start & Hintergrund. Autostart bei Windows-Anmeldung registriert die aktuelle Programmdatei für dieses Benutzerkonto. Autostart minimiert ist eine unabhängige Vorgabe für den automatischen Start. Ein normales Öffnen der App bleibt sichtbar. Für die portable Ausgabe muss der Ordner dauerhaft an seinem Platz bleiben. Die Deinstallation entfernt nur einen Autostart-Eintrag, der auf genau diese Installation zeigt. Windows kann den Start verzögern oder einen Eintrag in seinen eigenen Starteinstellungen deaktivieren.

**Reihenfolge:** Konten am Griff der Kopfzeile ziehen; Ordner am Griff links vom Namen. Die Markierung zeigt, ob vor oder nach dem Ziel eingefügt wird. Ordner lassen sich innerhalb ihres Kontos anordnen. Den ursprünglichen Ordneraufbau unter Einstellungen → Darstellung → Layout & Sidebar wiederherstellen.


## Mails mit der Maus verschieben

Eine Mail aus der Liste auf einen Ordnernamen in der Sidebar ziehen. Für mehrere Mails vorher Strg/Umschalt oder den Auswahlmodus verwenden und die Auswahl auf den Zielordner ziehen. Beim Ansetzen des Ziehens bleibt die Gruppe ausgewählt. Das Ziel erhält einen Akzentrahmen; am Rand scrollt die Sidebar automatisch. Esc bricht das Ziehen ab.

Serverordner werden mit dem Mailserver abgeglichen; lokale Ordner erhalten das Serveroriginal und ordnen die Mail nur in zuMail lokal zu. Ein gemeinsames Ziel unter Alle Mailkonten verschiebt jede Mail in den entsprechenden Ordner ihres eigenen Kontos. Für einen konkreten Kontoordner ausschließlich Mails dieses Kontos auswählen. Markiert und Entwürfe sind keine Verschiebeziele. Eine aktive Serververbindung ist erforderlich; fehlgeschlagene Einzelaktionen werden unten angezeigt und verändern die betroffenen Originale nicht.


## Oberfläche und App-Töne

Einstellungen sind in aufklappbaren Kategorien organisiert. Die Suche findet auch Unterseiten anhand ihrer Optionen, zum Beispiel Signatur oder Lautstärke. Mit Strg+F die Einstellungssuche fokussieren. Fertig speichert und schließt die Einstellungen. Dark/Light Mode und die Akzentfarbe unter Darstellung → Erscheinungsbild wechseln.

Unter App → Benachrichtigungen steuert ein gemeinsamer Regler die Lautstärke von Business Chime und Versand-Swoosh. Beide Audiodateien sind deutlich leiser abgestimmt. Bei 0 % bleiben beide stumm; die Töne lassen sich weiterhin einzeln ausschalten. Die Vorschau verwendet denselben Pegel wie der spätere App-Ton. Die Windows-Lautstärke bleibt unverändert.


## Nachricht verfassen

Versandkonto und Absenderprofil stehen oben direkt zur Auswahl. Über Cc und Bcc die zusätzlichen Empfängerfelder öffnen. Belegte Felder lassen sich erst nach Entfernen ihrer Empfänger ausblenden; gespeicherte Entwürfe zeigen vorhandene Cc-/Bcc-Adressen automatisch. Kontakte auswählen oder beim Tippen Vorschläge übernehmen.

Anhänge über Anhang hinzufügen oder Dateien auf das Verfassen-Fenster ziehen. Dateikarten zeigen die Anhänge und bieten eine Entfernen-Aktion. Linkadresse und angezeigten Linktext gemeinsam eingeben; Textfarben über Farbfelder oder Hex-Wert wählen. Senden oder Strg+Enter startet den Versand. Während der Widerrufszeit stoppt Senden stoppen den Vorgang.

Beim Schließen einer geänderten Nachricht ausdrücklich Entwurf speichern, Verwerfen oder Weiter bearbeiten wählen. Das Schließsymbol der Rückfrage bricht den Schließwunsch ab. Alle zuMail-eigenen Dialoge verwenden den gemeinsamen Fensterrahmen; Dateien werden über die aktuelle Windows-Dateiauswahl gewählt. Scrollleisten erscheinen als sehr schmale 2-Pixel-Linien.
