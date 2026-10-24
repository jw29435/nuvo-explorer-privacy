---
title: Datenschutzerklärung – Nuvo Explorer
---

# Datenschutzerklärung – Nuvo Explorer

Stand: September 2026 · Gilt für die Android- und iOS-App „Nuvo Explorer“.

> **Entwurf:** Die rechtlichen Angaben (Rechtsgrundlagen, Drittlandtransfer, Speicherdauer bei Google) sind nicht
> anwaltlich geprüft.

**Kurz:** Die App spricht mit dem NAS, das du selbst einträgst. Es gibt keine Werbung und keine Server des
Entwicklers. Daten gehen in zwei Fällen an Dritte:

- **Nur wenn du zustimmst:** Absturzberichte (Firebase Crashlytics) und eine Nutzungsstatistik (Google Analytics,
  dazu Hinweise über Firebase In-App Messaging) gehen an Google. Google verarbeitet sie auch in den USA. Ohne
  Zustimmung sendet die App nichts davon. Die App fragt einmal nach dem ersten Start; ändern kannst du das jederzeit
  unter Einstellungen › Datenschutz. Server-Adressen, Benutzernamen und Dateipfade gehen nie mit. Die Daten sind
  pseudonym (zufällige IDs), nicht anonym.
- **Feedback über Wiredash:** Inhalte (Text, Screenshot, E-Mail) gehen nur dorthin, wenn du selbst „Feedback senden“
  oder „Problem melden“ antippst und abschickst. Damit das funktioniert, meldet das eingebaute Wiredash-SDK beim
  App-Start außerdem technische Basisdaten (App- und Systemversion, eine zufällige Installations-ID) – ohne Inhalte und
  ohne Daten zu deinem NAS (siehe „Feedback“).

## Welche Daten verarbeitet werden und wo sie liegen

| Daten | Zweck | Ort |
| --- | --- | --- |
| Server-Profile (Name, Adressen, Benutzername) | Verbindung zum NAS | App-Datenbank auf dem Gerät |
| Session-ID, Geräte-Token (2FA), optional Passwort („Passwort merken“, standardmäßig aus) | Anmeldung am NAS | Android Keystore bzw. iOS Keychain |
| Bestätigte Zertifikats-Fingerprints | Schutz vor ausgetauschten Zertifikaten | Android Keystore bzw. iOS Keychain |
| Favoriten, Zuletzt geöffnet, Wiedergabepositionen, Einstellungen | Komfortfunktionen | App-Datenbank auf dem Gerät |
| Vorschaubilder und zwischengespeicherte Medien | schnellere Anzeige | App-eigenes Cache-Verzeichnis, Dateinamen als Hash |
| Offline-Dateien | Nutzung ohne Verbindung | App-eigenes Dokumente-Verzeichnis |
| Deine Dateien, Fotos und Videos | Anzeigen, Hoch- und Herunterladen | nur zwischen Gerät und deinem NAS |
| Einwilligungen (Absturzberichte, Nutzungsstatistik) | Einstellungen › Datenschutz | App-Datenbank auf dem Gerät |
| Zufällige Firebase-IDs (Installations-ID, App-Instanz-ID), noch nicht gesendete Absturzberichte | Firebase, nur mit Einwilligung aktiv (siehe unten) | App-eigener Speicher |
| Zufällige Wiredash-IDs, Startzähler, noch nicht gesendetes Feedback | Feedback (siehe unten) | App-eigene Einstellungen (SharedPreferences/UserDefaults) |

Nichts davon verlässt das Gerät, außer bei Anfragen an dein NAS, mit deiner Einwilligung an Firebase und beim
Feedback (siehe unten). Welche Daten das NAS selbst protokolliert (z. B.
Anmeldungen, Dateizugriffe), bestimmt dein DSM, nicht die App.

## Verbindung

- Nur zu den Adressen, die du einträgst (LAN, DDNS/Reverse Proxy, VPN). QuickConnect und andere Relay-Dienste werden
  nicht genutzt.
- HTTPS ist Standard. Selbstsignierte Zertifikate werden erst nach deiner Bestätigung per Fingerprint gepinnt; ändert
  sich das Zertifikat, blockiert die App die Verbindung. HTTP ist möglich, wird aber als unsicher markiert.
- Bei fehlerhafter Anmeldung versucht die App es nicht automatisch erneut (Schutz vor der DSM-Sperre).

## Berechtigungen

| Berechtigung | Wofür | Wann gefragt |
| --- | --- | --- |
| Fotos und Videos (Mediathek) | Auto-Upload neuer Aufnahmen; Lesen der Originale inkl. Aufnahmeort (EXIF) für eine vollständige Sicherung | erst beim Einschalten des Auto-Uploads |
| Fotos hinzufügen | „In Fotos speichern“ | beim ersten Speichern |
| Kamera | Foto aufnehmen und hochladen | beim ersten Aufnehmen |
| Benachrichtigungen | Fortschritt von Transfers, Player-Steuerung | beim ersten Transfer bzw. bei der Wiedergabe |
| Hintergrundausführung | Musik im Hintergrund, Auto-Upload (Android: WorkManager; iOS: vom System geplant) | – |

Standort, Kontakte, Mikrofon oder Werbe-IDs nutzt die App nicht.

## Löschen

- Einstellungen › Datenschutz: Schaltest du die Nutzungsstatistik aus, löscht die App die Analytics-Daten auf dem
  Gerät (neue App-Instanz-ID); schaltest du die Absturzberichte aus, verwirft sie noch nicht gesendete Berichte.
  Bereits an Google übertragene Daten löscht Google nach den unten genannten Fristen.
- Einstellungen › „Alle lokalen Daten löschen“ entfernt Cache, Offline-Dateien, Transfers, Session-IDs,
  Geräte-Tokens, gemerkte Passwörter und bestätigte Zertifikate.
- Ein Server-Profil zu löschen entfernt dessen Favoriten, Verlauf und Anmeldedaten.
- Deinstallieren der App entfernt alle App-Daten vom Gerät.
- Auf dem NAS gespeicherte Dateien (z. B. per Auto-Upload) bleiben dort, bis du sie löschst.

## Freigabelinks

Freigabelinks erzeugt dein NAS. Die App schlägt ein Ablaufdatum vor und kopiert Links nur nach deiner Bestätigung in
die Zwischenablage.

## Absturzberichte und Nutzungsstatistik (Firebase)

Anbieter ist Google Ireland Limited, Gordon House, Barrow Street, Dublin 4, Irland, als Auftragsverarbeiter
(Firebase-Datenverarbeitungsbedingungen). Google verarbeitet Daten auch bei Google LLC in den USA; die Übermittlung
stützt sich auf das EU-US Data Privacy Framework, unter dem Google zertifiziert ist, sowie auf
Standardvertragsklauseln.

**Einwilligung:** Rechtsgrundlage ist deine Einwilligung (Art. 6 Abs. 1 lit. a DSGVO, für den Zugriff auf das Gerät
§ 25 Abs. 1 TDDDG). Beide Punkte sind einzeln wählbar und standardmäßig aus. Die App fragt einmal nach dem ersten
Start (nie während Anmeldung, 2FA oder Zertifikatsprüfung) und erneut, wenn neue Datenarten dazukommen. Widerruf
jederzeit unter Einstellungen › Datenschutz; er wirkt sofort. Bis zur Einwilligung startet die App die Firebase-SDKs
gar nicht; es gibt keine Verbindung zu Google.

**Absturzberichte (Firebase Crashlytics)**, nur mit der Einwilligung „Absturzberichte“:

- Stacktrace und Art des Fehlers bei Abstürzen und unerwarteten Fehlern; Fehlertexte werden vorher bereinigt
  (Adressen, IPs, URLs, Pfade, Benutzer- und Servername, Sitzungsdaten und Tokens werden entfernt). Erwartbare
  Situationen (kein Netz, falsches Passwort, 2FA, fehlende Rechte) meldet die App nicht.
- Gerätemodell, Betriebssystem und Version, App-Version und Build, freier Speicher, Ausrichtung u. ä. technische Daten
  zum Zeitpunkt des Absturzes,
- Zusatzangaben der App: App-Version, Build, DSM-Hauptversion, Verbindungsart (LAN, extern, VPN), Design, App-Sprache,
- eine zufällige Crashlytics-Installations-UUID und die Firebase-Installations-ID. Eine Nutzer-ID setzt die App nicht.
- Speicherdauer laut Google: 90 Tage.

**Nutzungsstatistik (Google Analytics for Firebase, Firebase In-App Messaging)**, nur mit der Einwilligung
„Nutzungsstatistik“:

- Welche Bildschirme geöffnet werden, nur als Routen-Schema (z. B. „/files/folder“), nie mit Datei- oder
  Ordnernamen,
- wenige Ereignisse mit Kategorien statt Inhalten (Liste in `docs/ANALYTICS.md`): Server verbunden (Verbindungsart),
  Wiedergabe gestartet (Quelle, Dateiendung), Viewer geöffnet (Dateityp), Upload gestartet (Quelle), Freigabelink
  erstellt, Auto-Upload umgeschaltet, Feedback geöffnet,
- automatisch erfasste Ereignisse und Gerätedaten von Google Analytics (erster Start, Sitzungsbeginn, Nutzungsdauer,
  App-Update, Gerätemodell, Betriebssystem, Sprache, aus der IP-Adresse abgeleitetes Land bzw. Region – die IP-Adresse
  selbst speichert Google Analytics laut Google nicht),
- eine zufällige App-Instanz-ID und die Firebase-Installations-ID.
- Nicht genutzt: Werbe-ID (Android Advertising ID, IDFA), Google Signals, Anzeigenpersonalisierung, Datenfreigabe an
  andere Google-Produkte.
- In-App Messaging lädt mit der Firebase-Installations-ID Hinweise (z. B. auf Updates), die der Entwickler in der
  Firebase-Konsole anlegt, und zeigt sie beim Start an – nie während Anmeldung, 2FA oder Zertifikatsprüfung.
- Speicherdauer: Analytics-Ereignisse 2 Monate (Einstellung der Property); Firebase-Installations-IDs laut Google, bis
  sie gelöscht werden, danach höchstens 180 Tage in Sicherungen.

## Feedback

Die App enthält In-App-Feedback über [Wiredash](https://wiredash.com). Die Daten werden laut Anbieter in der EU
gespeichert.

**Wenn du Feedback abschickst** (Einstellungen › „Feedback senden“ oder „Problem melden“ bei einer Fehlermeldung),
gehen an Wiredash:

- dein Text,
- optional ein Screenshot der aktuellen Ansicht – du entscheidest im Feedback-Dialog, ob und welchen du anhängst,
  und kannst darauf markieren; auf dem Screenshot ist sichtbar, was gerade auf dem Bildschirm steht,
- optional deine E-Mail-Adresse, falls du eine Antwort möchtest,
- Geräte- und App-Infos: App-Version und Build, Betriebssystem und Version, Gerätesprache, Bildschirmgröße,
- diese Zusatzangaben der App: App-Sprache, Design (hell/dunkel), DSM-Hauptversion des aktiven Servers,
  Verbindungsart (LAN, extern, VPN) und bei „Problem melden“ Fehlertyp und -code sowie ein Fehlertext, aus dem
  Adressen, Pfade, Benutzer- und Servername sowie Sitzungsdaten vorher entfernt werden.

Nie übertragen werden NAS-Adressen, Hostnamen oder IP-Adressen, Benutzernamen, Server-Namen, Datei- oder
Ordnerpfade, Session-IDs, Tokens oder Passwörter.

**Beim App-Start** (höchstens alle 30 Minuten, etwa 5 Sekunden nach dem Start) sendet das Wiredash-SDK einen
technischen Ping: eine zufällige Installations-ID, App-Version, Build und Paketname, Umgebung (Test/Release),
Systemsprache, Betriebssystem und Version sowie die SDK-Version. Beim ersten Start kommt einmalig das Ereignis
„firstLaunch“ dazu. Das lässt sich im SDK nicht abschalten; Inhalte oder Daten zu deinem NAS enthält es nicht.
Umfragen (Promoter Score) nutzt die App nicht.

Feedback kann erst nach dem Absenden gelöscht werden, indem du über die Kontaktadresse unten darum bittest.
Die zufällige Installations-ID verschwindet mit „Alle lokalen Daten löschen“ nicht, wohl aber beim Deinstallieren.

## Kontakt

Fragen und Hinweise bitte als Issue auf [github.com/jw29435/nuvo-explorer-privacy](https://github.com/jw29435/nuvo-explorer-privacy/issues).

---

# Privacy policy (English summary)

> **Draft:** the legal statements have not been reviewed by a lawyer.

The app talks to the NAS you configure. There is no advertising and no developer server.

**Only with your consent** (asked once after the first start, never during sign-in, 2FA or certificate checks; both
options are off by default and can be changed at any time under Settings › Privacy) the app sends crash reports
(Firebase Crashlytics) and usage statistics (Google Analytics for Firebase, plus update notes via Firebase In-App
Messaging) to Google Ireland Limited as processor; Google also processes data in the USA (EU-U.S. Data Privacy
Framework, standard contractual clauses). Legal basis: consent (Art. 6(1)(a) GDPR, Section 25(1) TDDDG). Crash reports
contain the stack trace, device model, OS and app version and scrubbed error texts (no addresses, IPs, URLs, paths,
user or server names, sessions or tokens), plus app version, build, DSM major version, connection type, theme and app
language; retention 90 days. Usage statistics contain screen route templates (e.g. “/files/folder”, never file or
folder names), a few category-only events (see `docs/ANALYTICS.md`) and Google Analytics' automatic events and device
data; retention 2 months. Both use random installation/instance IDs (pseudonymous, not anonymous). No advertising ID,
no Google Signals, no ad personalization. Turning usage statistics off resets the analytics data on the device;
turning crash reports off discards unsent reports.

The other exception is in-app feedback via Wiredash (EU hosting according to the provider): only when you tap “Send feedback” or “Report a
problem” and submit, your text, an optional screenshot and optional e-mail address, device/app info (app version,
OS and version, language, screen size) and app details (app language, theme, DSM major version, connection type
LAN/external/VPN, and for problem reports the error type/code with addresses, paths, user and server names and
session data removed) are sent to Wiredash. NAS addresses, host names, IPs, user names, server names, file or folder
paths, session IDs, tokens and passwords are never sent. In addition, the Wiredash SDK sends a technical ping on app
start (at most every 30 minutes): a random installation ID, app version/build and package name, environment, system
language, OS and version and SDK version, plus a one-time “firstLaunch” event; it cannot be switched off in the SDK
and contains no content or NAS data. Surveys (promoter score) are not used. Sessions, device tokens, optional passwords and certificate pins are stored in the Android
Keystore / iOS Keychain; everything else (profiles, favorites, playback positions, cache, offline files) stays in the
app's private storage on your device. Photo library access is requested only when you turn on auto upload and is used
solely to copy new photos/videos to your NAS. “Delete all local data” in the settings removes cache, offline files,
transfers, tokens, saved passwords and trusted certificates.
