# Kurzanleitung: GitHub-Account einrichten (inkl. 2FA)

**Dauer:** ca. 15 Minuten
**Was du brauchst:** E-Mail-Adresse, Smartphone mit Authenticator-App (z. B. Microsoft Authenticator, Google Authenticator, 1Password) oder einen Hardware-Schlüssel/Passkey, Passwortmanager

---

## Teil 1 – Account anlegen

1. **Registrieren:** Öffne <https://github.com/signup>.
2. **E-Mail eingeben:** Nutze die Adresse, die intern dafür vorgesehen ist (im Zweifel die Dienstadresse). Weitere Adressen kannst du später ergänzen.
3. **Passwort festlegen:** Mindestens 15 Zeichen oder 8 Zeichen mit Zahl und Kleinbuchstaben. Empfehlung: im Passwortmanager generieren und speichern.
4. **Benutzernamen wählen:** Kurz, wiedererkennbar, ohne Sonderzeichen (z. B. `vorname-nachname`). Der Name ist öffentlich sichtbar und taucht in Commits und URLs auf.
5. **Captcha lösen** und auf **Create account** klicken.
6. **E-Mail bestätigen:** Den Code aus der Bestätigungsmail eingeben.
7. **Plan:** *Free* reicht. Zugriffe auf Organisations-Repos kommen über eine Einladung der Organisation.

## Teil 2 – Profil kurz einrichten

1. Oben rechts auf das Profilbild → **Settings** → **Public profile**.
2. **Name** eintragen (Vor- und Nachname), damit Kolleg:innen dich finden.
3. Optional: Profilbild hochladen.
4. **Settings → Emails:** Haken bei **Keep my email addresses private** setzen. GitHub nutzt dann eine `…@users.noreply.github.com`-Adresse für Commits.

## Teil 3 – Zwei-Faktor-Authentifizierung (2FA) aktivieren

1. **Settings** → **Password and authentication**.
2. Unter *Two-factor authentication* auf **Enable two-factor authentication** klicken.
3. **Methode wählen – empfohlen: Authenticator-App**
   - QR-Code mit der Authenticator-App scannen.
   - Den 6-stelligen Code aus der App eingeben → **Continue**.
   - *Alternative:* SMS ist möglich, gilt aber als weniger sicher.
4. **Recovery Codes sichern (wichtig!)**
   - GitHub zeigt 16 Wiederherstellungscodes an.
   - **Download** und sicher ablegen, am besten im Passwortmanager.
   - Ohne diese Codes ist der Account bei Verlust des Smartphones kaum wiederherstellbar.
   - Bestätigen mit **I have saved my recovery codes**.
5. **Zweite Methode ergänzen (empfohlen)**
   - Unter *Two-factor methods* einen **Passkey** oder **Security Key** hinzufügen bzw. die **GitHub Mobile App** aktivieren.
   - So bleibt der Zugang erhalten, falls eine Methode ausfällt.
6. **Testen:** Abmelden und neu anmelden – nach dem Passwort wird der 2FA-Code abgefragt.

> **Hinweis:** GitHub fordert nach ca. 28 Tagen einen kurzen „2FA-Check-up“ an. Einfach einmal mit dem zweiten Faktor bestätigen.

## Teil 4 – Organisation beitreten

Wichtig: Erledige zuerst Teil 3 (2FA). Ohne 2FA kannst du der Organisation nicht beitreten.

1. **Plattform-Team ansprechen:** Melde dich beim Plattform-Team und bitte um Aufnahme in die GitHub-Organisation.
2. **GitHub-Benutzernamen mitteilen:** Nenne deinen Benutzernamen aus Teil 1 (z. B. `vorname-nachname`). Du findest ihn oben rechts, wenn du auf dein Profilbild klickst.
3. **Team mitteilen:** Sag dazu, in welchem Team du arbeitest. So bekommst du gleich Zugriff auf die richtigen Repositories.
4. **Einladung abwarten:** Das Plattform-Team lädt dich ein. Du bekommst eine E-Mail von GitHub.
5. **Einladung annehmen:** Klicke in der E-Mail auf den Link oder öffne <https://github.com/settings/organizations> und bestätige dort.

---

## Checkliste

- [ ] Account angelegt und E-Mail bestätigt
- [ ] Passwort im Passwortmanager gespeichert
- [ ] Name im Profil eingetragen, E-Mail auf privat gestellt
- [ ] 2FA mit Authenticator-App aktiviert
- [ ] Recovery Codes sicher gespeichert
- [ ] Zweite 2FA-Methode (Passkey/Security Key/GitHub Mobile) eingerichtet
- [ ] Login mit 2FA getestet
- [ ] Plattform-Team angesprochen (Benutzername und Team mitgeteilt)
- [ ] Einladung der Organisation angenommen

## Häufige Probleme

| Problem | Lösung |
|---|---|
| Code aus der App wird abgelehnt | Uhrzeit auf dem Smartphone auf „automatisch“ stellen, neuen Code abwarten |
| Smartphone verloren | Mit Recovery Code oder zweiter 2FA-Methode anmelden, dann 2FA neu einrichten |
| Keine Bestätigungsmail | Spam-Ordner prüfen, unter *Settings → Emails* erneut senden |
| `git push` verlangt Passwort und schlägt fehl | Mit 2FA funktioniert das Passwort nicht für Git – stattdessen Git Credential Manager, SSH-Schlüssel oder Personal Access Token nutzen (eigene Anleitung) |

**Nächster Schritt:** GitHub mit Git auf dem Rechner und mit Claude verbinden.
