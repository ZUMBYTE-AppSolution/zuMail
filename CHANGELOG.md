# Changelog

## 0.1.0-alpha.11

- **Änderungen im Updater formatiert lesen:** Überschriften, Listen, Hervorhebungen, Tabellen, Links und Screenshots werden direkt angezeigt. Text lässt sich markieren und kopieren. Die Ansicht passt sich dem hellen oder dunklen Design an.
- **zuMail erneut öffnen:** Ein weiterer Start holt das bereits geöffnete Fenster nach vorn. Minimierte oder im Infobereich versteckte Fenster werden wiederhergestellt; eine vorher maximierte Ansicht bleibt maximiert. Es erscheint keine Meldung „ist bereits geöffnet“ mehr.
- **Sperre und Arbeitsstand bleiben erhalten:** Die vorhandene Sitzung wird weiterverwendet. Eine aktive PIN-Sperre bleibt bestehen; ein zusätzlicher Windows-Autostart bleibt im Hintergrund.

285 automatische Prüfungen. Markdown in Dark/Light Mode, Fensterwiederherstellung und Anfragen zwischen getrennten Prozessen geprüft. Installer, Update-Neustart, Deinstallation und öffentliche Downloads geprüft. Neue Profile starten leer.

## 0.1.0-alpha.10

- **Kontakte neu gestaltet:** Adressbücher, Kontaktliste und alle Details nebeneinander. Die Suche findet auch Firmen, Telefonnummern, Anschriften und Notizen.
- **Kontakte übersichtlicher bearbeiten:** Eigene Bereiche für Person, Kontaktdaten, Adressen und weitere Angaben. Mehrere Mailadressen, Telefonnummern und Anschriften lassen sich einzeln ergänzen oder entfernen.
- **Farben direkt auswählen:** Farbfläche, Farbtonregler, Vorschau und Hex-Eingabe für die Akzentfarbe und Textfarben beim Verfassen.
- **Updates mit Fortschritt:** Anzeige von Prozent, geladener Datenmenge, Geschwindigkeit und geschätzter Restzeit. Downloads lassen sich abbrechen und erneut starten.
- **Nach dem Update weiterarbeiten:** Nach erfolgreicher Installation öffnet sich zuMail wieder mit dem bisherigen Profil. Konten, Einstellungen und eine eingerichtete PIN-Sperre bleiben erhalten.
- **Fehler beim Beenden behoben:** Das Hauptfenster schließt auch dann zuverlässig, wenn das Speichern sofort abgeschlossen ist.

268 automatische Prüfungen. Installer und portable Ausgabe geprüft; Installation, Update-Neustart mit bisherigem Testprofil und Deinstallation geprüft. Neue Profile starten leer.

## 0.1.0-alpha.9

- Neues Verfassen-Fenster mit klar getrennten Bereichen für Versandkonto und Profil, Empfänger, Betreff, Nachricht und Anhänge. Mehr Platz für den Nachrichtentext, kompakte Formatierungsleiste und direkt erreichbare Versandaktionen.
- Cc und Bcc bei Bedarf einblenden. Vorhandene Empfänger bleiben sichtbar; beim Öffnen von Entwürfen werden belegte Cc-/Bcc-Felder automatisch eingeblendet. Kontakteauswahl und Livesuche bleiben verfügbar.
- Anhänge als kompakte Dateikarten mit Entfernen-Aktion; mehrfach hinzugefügte Dateien werden zusammengefasst. Beim verzögerten Senden bleiben Absender, Inhalt und Anhänge geschützt, bis der Versand gestoppt oder abgeschlossen ist.
- Einheitliche zuMail-Fenstergestaltung für Verfassen, Einstellungen, Konten, Kontakte, Vorschauen und Bearbeitungsdialoge. Eigene Rückfragen, Fehler- und Eingabefenster ersetzen klassische System-Meldungsboxen. Windows-Dateiauswahlen bleiben die aktuellen systemeigenen Dateidialoge.
- Linkadresse und Linktext in einem Fenster bearbeiten; Textfarbe über Farbfelder oder eigene Hex-Eingabe wählen. Nicht erlaubte Linktypen werden direkt im Dialog abgewiesen.
- Sichtbare Scrollleisten nur 2 Pixel breit, mit größerer unsichtbarer Greiffläche in WPF. Sie erscheinen weiterhin nur im aktiven Bereich; auch HTML-Nachrichten verwenden 2-Pixel-Scrollleisten.

241 automatische Prüfungen. Nativer SMTP-Versand aus dem neuen Verfassen-Fenster, Bcc-Schutz, Entwürfe, Abbruch, Dialogantworten und kompakte Fenstergröße geprüft. Installer installiert/deinstalliert und dieselben Prüfungen gegen das installierte Paket ausgeführt. Neue Profile starten leer.

## 0.1.0-alpha.8

- Einheitliche Oberflächen, Abstände, Rundungen und Fokuszustände in Mailansicht, Einstellungen und Dialogen. Anthrazit und Light Mode bleiben neutral; Akzentfarben markieren Auswahl und Aktionen.
- Einstellungen mit aufklappbaren Kategorien, nachvollziehbarer Seitennavigation, Suche mit Trefferanzeige, ausgerichteten Feldern und erklärten Schaltern. Akzentfarben werden als echte Farbfelder dargestellt; Import und Sicherungen sind in eigene Bereiche gegliedert.
- Kontextmenüs mit einheitlichen Abständen, dezentem Schatten außerhalb der Texte, schmalem Rahmen und getrennten Aktionsgruppen. Papierkorb und Ordnerentfernung sind farblich erkennbar. Die Menüs im HTML-Lesebereich und Infobereich verwenden dieselbe Gestaltung.
- Nachrichtenfilter als zusammengehörige Auswahl; Sidebar-Ziele zeigen beim Ziehen nun den tatsächlichen Akzentrahmen. Auswahl, Serverabgleich und bestehende Sicherheitsabfragen bleiben erhalten.
- Business Chime und Versand-Swoosh deutlich abgesenkt und nach spektral gewichteter Signalenergie aneinander angeglichen. Beide verwenden dieselbe Lautstärkeeinstellung unter App → Benachrichtigungen, mit separaten Ein/Aus-Schaltern. 0 % ist stumm; ältere Profile erhalten die leisere Vorgabe von 60 %. Die Windows-Systemlautstärke wird nicht verändert.
- Tonvorschau funktioniert auch bei abgeschalteten Windows-Benachrichtigungen. Kompakte Eingabefelder, einheitliche Auswahllisten und klare Formatierungsfelder im Nachrichteneditor.

220 automatische Prüfungen. Einstellungen und Menüs als native WPF-Oberfläche kontrolliert, Audiopegel und Lautstärkeregler geprüft. Installer installiert/deinstalliert und Prüfungen gegen das installierte Paket ausgeführt. Neue Profile starten leer.

## 0.1.0-alpha.7

- Nachrichten direkt aus der Liste auf Ordner in der Sidebar ziehen, auch mehrere ausgewählte Mails und Konversationen auf einmal. Eine bestehende Mehrfachauswahl bleibt beim Ansetzen des Ziehens erhalten; Ziehen markiert keine Mail als gelesen.
- Serverordner führen echte IMAP-Verschiebeaktionen aus. Ziel-UIDs, verschlüsselte Speicherung, Nachrichtenliste und Ungelesen-Badges werden aktualisiert. Lokale Mails lassen sich in Serverordner hochladen.
- Gemeinsame Standardordner unter „Alle Mailkonten“ lösen das Ziel pro Konto auf. Kontoordner nehmen ausschließlich Nachrichten desselben Kontos an. „Markiert“ und „Entwürfe“ sind keine Verschiebeziele.
- Lokale Ordner ordnen Nachrichten lokal zu und erhalten das Original auf dem Mailserver. Bereits passende Ziele bleiben unverändert. Abgelehnte oder fehlgeschlagene Serveraktionen bleiben sichtbar; betroffene Originalmails behalten ihre bisherige Serverzuordnung.
- Zielmarkierung und automatisches Scrollen unterstützen das Ziehen in der Sidebar. Die bestehende Sortierung über Ziehgriffe bleibt verfügbar.
- Neues rasterbasiertes App-Icon: reduzierter Cyan-Brief mit integriertem Z auf Anthrazit, dezenter Glow, transparente Außenkante und geglättete PNG-/ICO-Größen für App und Installer.

202 automatische Prüfungen, einschließlich nativer WPF-Drop-Ereignisse, IMAP-MOVE, Mehrfachauswahl, erneuter Synchronisierung, lokalen Zielen, Upload und Verbindungsfehlern. Installer und portable Ausgabe geprüft. Neue Profile starten leer.

## 0.1.0-alpha.6

- Überarbeitete Mailansicht mit abgestimmten Innenabständen, ruhigen Kartenflächen und kompakter Sidebar. Dark/Light Mode und die frei wählbare Akzentfarbe bleiben verfügbar.
- Schmale 4-Pixel-Scrollbars erscheinen nur im aktiven Bereich bei Maus, Tastaturfokus oder Ziehen. Die Inhaltsbreite bleibt beim Einblenden gleich; auch HTML-Mails verwenden schmale Scrollbars.
- Die separate Arbeitsbereichsleiste entfällt. Oben in der Sidebar stehen Arbeitsbereichsauswahl und „Neuer Arbeitsbereich“ zur Verfügung. Einstellungen sind in der oberen Werkzeugleiste erreichbar.

- Einstellungen in aufklappbaren Gruppen und einzelnen Unterseiten, mit Suche, klaren Einstellungsgruppen und einheitlichen Schaltern.
- Windows-Autostart und minimierter Autostart separat einstellbar unter App → Start & Hintergrund. Der normale Programmstart bleibt sichtbar; eine aktive PIN-Sperre bleibt beim minimierten Start erhalten.
- Konten und Ordner über Ziehgriffe in der Sidebar umsortieren, einschließlich automatischem Scrollen beim Ziehen. Die Reihenfolge wird verschlüsselt gespeichert. Ordner auf dem Mailserver werden dadurch nicht umbenannt oder verschoben.
- Versandkonto und zugehöriges Absenderprofil sind in jeder neuen Nachricht, Antwort und Weiterleitung direkt auswählbar. Antworten starten mit dem ursprünglichen Empfängerkonto.
- Mehrfachauswahl per Auswahlmodus, Strg oder Umschalt; alle auswählen, gelesen/ungelesen markieren, markieren, verschieben, archivieren oder in den Papierkorb legen. Sammelaktionen betreffen nur passende Mails im aktuellen Ordner, einschließlich mehrerer Konten bei Lesen/Archivieren; konversationsbezogene Antworten aus anderen Ordnern bleiben erhalten. Verschieben erfolgt innerhalb eines Kontos.
- Portable Chromium-Prüfung berücksichtigt die mitgelieferte .NET-Laufzeit auch ohne systemweite .NET-Installation.

176 automatische Prüfungen. Installer, portable Ausgabe und Erhalt vorhandener Daten geprüft. Neue Profile bleiben leer.

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
