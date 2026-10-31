# Google und Microsoft für zuMail registrieren

Diese Registrierung benötigt der Herausgeber der App einmalig. Die Mailnutzer melden sich danach über den Browser des jeweiligen Anbieters an. In diesem Alpha-Build sind die Client-IDs noch nicht vorgegeben und lassen sich lokal unter **Konto verknüpfen → Gmail/Microsoft → Anmeldung einrichten** hinterlegen.

## Microsoft · Live.com, Outlook.com und Microsoft 365

Portal: https://entra.microsoft.com/#view/Microsoft_AAD_RegisteredApps/ApplicationsListBlade

1. **App-Registrierungen → Neue Registrierung**, Name **zuMail**.
2. Unterstützte Kontotypen: **Konten in beliebigen Organisationsverzeichnissen und persönliche Microsoft-Konten**.
3. Unter **Authentifizierung → Plattform hinzufügen → Mobile und Desktopanwendungen** die Umleitungs-URI **http://localhost/** hinterlegen. zuMail verwendet einen dynamischen lokalen Port; Microsoft ignoriert diesen Port beim Abgleich von localhost-Adressen.
4. Unter **API-Berechtigungen → Berechtigung hinzufügen → Von meiner Organisation verwendete APIs → Office 365 Exchange Online → Delegierte Berechtigungen** die Rechte **IMAP.AccessAsUser.All** und **SMTP.Send** hinzufügen.
5. Die Anmeldung fordert außerdem **openid, profile, email und offline_access** an. Für Kontakte verwendet zuMail separat **Microsoft Graph → Delegierte Berechtigungen → Contacts.Read**.
6. Organisationsrichtlinien können eine Administratorfreigabe verlangen. Ebenso müssen IMAP und SMTP AUTH für das betreffende Microsoft-365-Postfach zugelassen sein.
7. Unter **Übersicht** die **Anwendungs-ID (Client-ID)** kopieren und lokal in zuMail eintragen. Die öffentliche Desktop-App verwendet PKCE und benötigt kein Client-Secret.

Du benötigst Zugriff auf ein Microsoft-Entra-Verzeichnis mit Berechtigung zur App-Registrierung. Der private Live-/Outlook-Mailaccount allein stellt noch kein solches Verzeichnis bereit.

Offizielle Dokumentation:

- https://learn.microsoft.com/en-us/entra/identity-platform/quickstart-register-app
- https://learn.microsoft.com/en-us/entra/identity-platform/reply-url
- https://learn.microsoft.com/en-us/exchange/client-developer/legacy-protocols/how-to-authenticate-an-imap-pop-smtp-application-by-using-oauth

## Google · Gmail und Google Workspace

Portal: https://console.cloud.google.com/auth/clients

1. Ein Google-Cloud-Projekt für **zuMail** erstellen oder auswählen.
2. Unter **Google Auth Platform → Branding** Appname **zuMail**, Supportadresse und Entwicklerkontakt hinterlegen.
3. Unter **Audience / Zielgruppe** für private Gmail-Konten eine externe Zielgruppe wählen. Zunächst im Testbetrieb bleiben und die vorgesehenen Google-Konten als Testnutzer eintragen.
4. Unter **Data Access / Datenzugriff** die benötigten Bereiche vorsehen: **openid**, **profile**, **email** und **https://mail.google.com/**. Kontakte werden separat mit **https://www.googleapis.com/auth/contacts.readonly** angemeldet; hierfür die People API im Projekt aktivieren.
5. Unter **Clients → Client erstellen** den Anwendungstyp **Desktop-App** wählen.
6. Die erzeugte **Client-ID** und das zugehörige **Desktop-Client-Secret** lokal in zuMail hinterlegen.
7. Danach in zuMail **Mit Google anmelden** wählen. Die Desktop-App verwendet einen lokalen Loopback-Rückruf und PKCE; eine eigene öffentliche Rückruf-Webseite ist dafür nicht nötig.

Der vollständige Gmail-Zugriff ist ein eingeschränkter Google-Berechtigungsbereich. Eine allgemeine Veröffentlichung für beliebige Google-Nutzer erfordert die von Google verlangte Prüfung. Im Testbetrieb gelten die dort angezeigten Beschränkungen. Verwende die Registrierungsdaten der eigenen zuMail-App.

Offizielle Dokumentation:

- https://developers.google.com/identity/protocols/oauth2/native-app
- https://developers.google.com/workspace/gmail/imap/xoauth2-protocol

## In zuMail

**Anmeldung einrichten** speichert die Konfiguration verschlüsselt im lokalen Profil. Das Mailkonto selbst wird anschließend über **Mit Google/Microsoft anmelden** im Browser verknüpft. Passwörter und Zwei-Faktor-Abfragen des Mailkontos werden dort beim Anbieter eingegeben.

Die Browser-Rückkehr und der anschließende Zugriff auf das Postfach sind getrennte Schritte. Eine erfolgreiche Browser-Anmeldung allein bestätigt noch nicht, dass der Anbieter IMAP/SMTP für das Postfach freigegeben hat.
