# Anbieter-Anmeldung · Für den Herausgeber

Mailnutzer benötigen keine eigenen OAuth-Schlüssel. Die gemeinsame Google-Registrierung ist ab Alpha 2 enthalten. **Konto verknüpfen → Gmail** startet direkt die Browser-Anmeldung. Microsoft ist für diesen Build zurückgestellt und ohne Herausgeberregistrierung in der Anbieterauswahl ausgeblendet.

## Google veröffentlichen

Im [zuMail-Projekt der Google Auth Platform](https://console.cloud.google.com/auth/overview):

1. Unter **Branding** Appname, Supportadresse, Entwicklerkontakt, Startseite und Datenschutzerklärung hinterlegen. Verwendete Domains gegebenenfalls verifizieren.
2. Unter **Audience / Zielgruppe** eine externe Zielgruppe für private Gmail-Konten verwenden. Im Testmodus die vorgesehenen Testnutzer eintragen. Für den allgemeinen Betrieb die App veröffentlichen.
3. Unter **Data Access / Datenzugriff** openid, profile, email und **https://mail.google.com/** angeben. Der vollständige Gmail-Zugriff wird für IMAP/SMTP benötigt. Kontakte werden separat mit **https://www.googleapis.com/auth/contacts.readonly** angefordert; hierfür die People API aktivieren.
4. Unter **Clients** den Typ **Desktop-App** verwenden. zuMail nutzt PKCE und einen lokalen Loopback-Rückruf. Eine öffentliche Rückruf-Webseite ist nicht nötig.
5. Die erforderliche Prüfung eingeschränkter Gmail-Berechtigungen beantragen, einschließlich Begründung der Berechtigungen und Vorführung der Anwendung.

Die Registrierung und Prüfung sind Aufgaben des Herausgebers. Testmodus und veröffentlichte, noch ungeprüfte Apps können Zugriffsbeschränkungen und Warnungen haben. Ein GitHub-Release allein schaltet den Zugriff bei Google nicht frei. Der aktuelle Freigabestatus wurde nicht geprüft; eine echte Google-Anmeldung wurde noch nicht durchgeführt.

Offizielle Quellen: [Desktop-OAuth](https://developers.google.com/identity/protocols/oauth2/native-app), [Gmail OAuth](https://developers.google.com/workspace/gmail/imap/xoauth2-protocol), [Prüfung eingeschränkter Berechtigungen](https://developers.google.com/identity/protocols/oauth2/production-readiness/restricted-scope-verification).

## Release-Konfiguration

Release-Builds lesen die Herausgeberdatei unter `%LOCALAPPDATA%\Zumbyte\BuildCredentials\zuMail\publisher-oauth.json` mit GoogleClientId, GoogleClientSecret und MicrosoftClientId. Sie bleibt außerhalb von Git; der Build bettet die gemeinsame Desktop-Registrierung in die App ein.

Desktop-Apps sind öffentliche OAuth-Clients. Ein eingebettetes Desktop-Client-Secret lässt sich nicht vertraulich halten. PKCE schützt den Codeaustausch. Die App enthält kein Mailpasswort des Herausgebers. Kontotoken und Nutzerdaten werden getrennt im verschlüsselten lokalen Profil gespeichert.

Vorhandene Anmeldungen behalten beim Update ihre ursprüngliche Client-Zuordnung für die Token-Erneuerung.

## Microsoft später

Microsoft ist auf Wunsch für diesen Build zurückgestellt. Die Protokollunterstützung bleibt für eine spätere gemeinsame Herausgeberregistrierung erhalten. Auch dann brauchen Mailnutzer keine eigene Entwicklerregistrierung.

Später: [Microsoft Entra App-Registrierung](https://entra.microsoft.com/#view/Microsoft_AAD_RegisteredApps/ApplicationsListBlade), persönliche und Organisationskonten, Plattform **Mobile und Desktopanwendungen**, Umleitungs-URI **http://localhost/**. Delegierte Exchange-Rechte IMAP.AccessAsUser.All und SMTP.Send sowie openid/profile/email/offline_access; Kontakte separat über Microsoft Graph Contacts.Read. Kein Client-Secret für die öffentliche Desktop-App. Die gemeinsame Anwendungs-ID wird per App-Update verteilt.

Offizielle Quellen: [App registrieren](https://learn.microsoft.com/en-us/entra/identity-platform/quickstart-register-app), [Loopback-Rückruf](https://learn.microsoft.com/en-us/entra/identity-platform/reply-url), [IMAP-/SMTP-OAuth](https://learn.microsoft.com/en-us/exchange/client-developer/legacy-protocols/how-to-authenticate-an-imap-pop-smtp-application-by-using-oauth).

Browser-Anmeldung und Postfachfreigabe sind getrennte Schritte. Nach der Browser-Rückkehr prüft zuMail auch IMAP und SMTP.
