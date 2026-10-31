# zuMail · Erste Schritte

## Arbeitsbereiche und Konten

Über das Plus links einen Arbeitsbereich anlegen. Darin **Konto verknüpfen** öffnen und einen Anbieter oder **Freie Eingabe** auswählen. Nach Eingabe der Mailadresse versucht zuMail, IMAP-/SMTP-Server und Ports zu ermitteln. Die ermittelten Werte lassen sich prüfen und ändern.

TLS-Zertifikate werden geprüft. Unterstützt ein Anbieter normale Passwörter nicht, sein App-Passwort oder die Browseranmeldung verwenden. Google/Microsoft benötigen zunächst eine eigene registrierte Desktop-App: **Einstellungen → Sicherheit → Anbieter-Anmeldung vorbereiten**. In diesem Alpha-Build sind keine gemeinsamen Client-IDs vorgegeben.

**Gmail und Live/Outlook:** Anbieter auswählen, **Mit Google/Microsoft anmelden** klicken und das Konto im Browser bestätigen. Die Kontoübernahme setzt Server und Ports automatisch. Falls der Anbieter keine Mailadresse zurückgibt, wird nach der Browser-Anmeldung nur diese Adresse abgefragt. Zugangsdaten zum Mailkonto werden im Browser des Anbieters eingegeben.

**Anmeldung einrichten** öffnet direkt in diesem Ablauf den Registrierungsassistenten. Google: OAuth-Client vom Typ Desktop-App und Testbenutzer einrichten. Microsoft: persönliche und Organisationskonten, Plattform Mobile/Desktop und Umleitungs-URI http://localhost/ eintragen; delegierte IMAP-/SMTP-Berechtigungen freigeben. Die Client-ID wird einmalig lokal hinterlegt.

Mailprofile unter **Einstellungen → Konten & Profile** bestimmen Namen, Absenderadresse, Antwortadresse und Signatur. Der Versand nutzt die Verbindung des zugeordneten Kontos.

## Ordner, Regeln und Spam

Rechtsklick in die Ordnerleiste bzw. auf einen eigenen Ordner. Beim Erstellen entscheidet **Auf dem Mailserver erstellen**, ob der Ordner beim Anbieter oder nur in zuMail liegt. Eine lokale Einordnung lässt die Nachricht auf dem Server im bisherigen Ordner bestehen.

Nachrichten per Rechtsklick **Verschieben …** einordnen. Serverordner werden auf dem Server geändert; nur leere eigene Ordner können entfernt werden.

Unter **Regeln & Filter** Bedingungen und Aktionen kombinieren. Neue Nachrichten nach dem ersten Abruf werden automatisch geprüft. Auf vorhandene Nachrichten Regeln erst über die Vorschau anwenden. Freigaben, Sperrlisten und Schlüsselwörter steuern den lokalen Spamfilter.

## Nachrichten und Kontakte

**Verfassen** öffnet den WYSIWYG-Editor. An, Cc und Bcc bieten Kontakte beim Tippen an. Mit Pfeiltasten und Eingabe übernehmen oder das Kontaktsymbol für die Auswahl öffnen. Mehrere Adressen werden durch Kommas getrennt.

**Kontakte** verwaltet das Adressbuch des Arbeitsbereichs, importiert und exportiert vCards. Unter **Adressbücher** lässt sich die Synchronisierung je Anbieter aktivieren. Google und Microsoft verwenden eine separate Kontaktanmeldung mit Leserechten. CardDAV benötigt die direkte HTTPS-Adresse des Adressbuchs; Zurückschreiben ist ein eigener Schalter.

## Sicherheit und Sicherung

Unter **Einstellungen → Sicherheit** vier- oder sechsstellige PIN und Autolock einrichten. Quick-Lock: Strg+Umschalt+L. Die PIN sperrt die Oberfläche. Lokale Kontodaten und der Nachrichtenspeicher sind mit AES-256-GCM verschlüsselt; Windows-DPAPI schützt den Schlüssel für das aktuelle Benutzerkonto.

Unter **Import & Export** Nachrichten bzw. eine passwortgeschützte Sicherung exportieren. Für Gerätewechsel diese Sicherung verwenden. Den Profilordner allein zu kopieren genügt wegen der Windows-Benutzerbindung nicht. Ein verlorenes Backup-Passwort kann nicht zurückgesetzt werden.

## Updates und Deinstallation

**Einstellungen → Updates** bietet Alpha- und stabile Versionen. Der Installer wird aus dem offiziellen Release-Repository bezogen und vor dem Start mit SHA-256 geprüft. Windows-Pakete sind noch nicht Authenticode-signiert.

Deinstallation entfernt Programm und Verknüpfungen, erhält jedoch Profildaten. Im portablen Paket bedeutet „portabel“ Start ohne Installation; das Profil bleibt standardmäßig im Windows-Benutzerverzeichnis.

## Bekannte Grenzen

Windows 10/11 x64. macOS/iOS und mobiler Push folgen. OpenPGP-/S/MIME-Nachrichtenverschlüsselung ist noch nicht enthalten. Die optionale HTML-Leseansicht benötigt WebView2.

IMAP-Cache: standardmäßig die letzten 100 Nachrichten pro geöffnetem Ordner, einstellbar auf 20–1000. Suche findet geladene Nachrichten. Serverlöschungen werden noch nicht in den lokalen Cache übernommen.

Google/Microsoft-Kontakte: Abgleich vom Anbieter, Änderungen lokal. CardDAV: optional beide Richtungen mit ETags. Fehlende Serverkontakte bleiben als lokale Kopie erhalten. Weitere Microsoft-Kontaktunterordner, automatische CardDAV-Principalsuche und Kontaktfotoabruf über Google/Microsoft sind noch nicht enthalten.

Benachrichtigungen unter Windows verwenden den laufenden Client bzw. Hintergrundbetrieb. Das ist noch kein plattformübergreifender Pushdienst.
