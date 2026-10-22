# Kurzanleitung: GitHub mit Git auf dem Rechner und mit Claude verbinden

**Dauer:** ca. 20 Minuten
**Was du brauchst:** deinen GitHub-Account mit 2FA (siehe [GitHub-Account einrichten](github-account-einrichten.md)), Zugang zur GitHub-Organisation, einen Rechner mit Windows oder Mac, einen Claude-Account

> **Worum geht es?**
> **GitHub** ist eine Webseite, auf der Dateien gemeinsam gespeichert werden. Ein Projektordner auf GitHub heißt **Repository** (kurz: Repo).
> **Git** ist ein kleines Programm auf deinem Rechner. Es holt die Dateien aus GitHub auf deinen Rechner und schickt deine Änderungen zurück.
> **Claude** kann die Dateien in GitHub lesen, wenn du es erlaubst. Dann kann Claude dir Fragen zu diesen Dateien beantworten.

---

## Teil 1 – Git installieren

### Windows

1. Öffne <https://git-scm.com/downloads> und klicke auf **Windows**.
2. Lade das Installationsprogramm herunter und starte es.
3. Klicke dich mit **Next** durch. Die vorgeschlagenen Einstellungen passen.
   Wichtig: Der **Git Credential Manager** ist dabei schon enthalten. Er kümmert sich später um die Anmeldung bei GitHub.
4. Am Ende auf **Finish** klicken.

> **Hinweis:** Darfst du auf deinem Dienstrechner keine Programme installieren? Dann wende dich an die IT oder das Plattform-Team.

### Mac

1. Öffne das Programm **Terminal** (über die Lupe oben rechts „Terminal“ suchen).
2. Tippe folgenden Befehl ein und drücke die Eingabetaste:

   ```
   git --version
   ```

   Der Befehl prüft, ob Git schon installiert ist.
3. Ist Git noch nicht da, fragt der Mac, ob er die „Befehlszeilenentwickler-Tools“ installieren soll. Klicke auf **Installieren** und warte, bis es fertig ist.
4. Für die Anmeldung bei GitHub zusätzlich den **Git Credential Manager** installieren: Öffne <https://github.com/git-ecosystem/git-credential-manager/releases>, lade beim neuesten Eintrag die Datei mit der Endung `.pkg` herunter und öffne sie per Doppelklick.

### Prüfen, ob es geklappt hat

Öffne das Terminal (Mac) bzw. das Programm **Git Bash** (Windows, über das Startmenü) und tippe:

```
git --version
```

Erscheint eine Zeile wie `git version 2.…`, ist alles bereit.

## Teil 2 – Git sagen, wer du bist

Git schreibt bei jeder Änderung dazu, wer sie gemacht hat. Dafür braucht es deinen Namen und eine E-Mail-Adresse.

1. **Deine geschützte E-Mail-Adresse holen:** Öffne auf GitHub **Settings → Emails**. Dort steht eine Adresse, die auf `@users.noreply.github.com` endet. Kopiere sie.
   *Warum?* So bleibt deine echte E-Mail-Adresse privat (das hast du in der ersten Anleitung eingestellt).
2. Tippe im Terminal bzw. in Git Bash diese zwei Befehle. Ersetze dabei den Text in Anführungszeichen:

   ```
   git config --global user.name "Vorname Nachname"
   git config --global user.email "deine-adresse@users.noreply.github.com"
   ```

   Die Befehle geben keine Rückmeldung. Das ist normal.

## Teil 3 – Ein Repository auf den Rechner holen

Das Herunterladen eines Repos heißt bei Git **klonen**. Dabei meldest du dich zum ersten Mal bei GitHub an.

1. Öffne auf GitHub das Repo, mit dem du arbeiten willst.
2. Klicke auf den grünen Button **Code** und dann auf **HTTPS**. Kopiere die Adresse (sie endet auf `.git`).
3. Wechsle im Terminal bzw. in Git Bash in den Ordner, in dem das Repo liegen soll, z. B. „Dokumente“:

   ```
   cd ~/Documents
   ```

4. Repo klonen (die kopierte Adresse einfügen):

   ```
   git clone https://github.com/ORGANISATION/REPO.git
   ```

5. **Anmelden:** Bei privaten Repos öffnet sich jetzt ein Fenster oder dein Browser. Wähle **Sign in with your browser**, melde dich bei GitHub an und bestätige mit deinem zweiten Faktor (2FA). Klicke danach auf **Authorize**.
6. Fertig: Im Ordner „Dokumente“ gibt es jetzt einen neuen Ordner mit den Dateien des Repos.

> **Gut zu wissen:** Die Anmeldung merkt sich der Git Credential Manager. Du musst dich also nicht jedes Mal neu anmelden. Ein Passwort oder einen Code in Git einzutippen ist nicht nötig.

## Teil 4 – Claude mit GitHub verbinden

1. Öffne <https://claude.ai> und melde dich an.
2. Unten links auf deinen Namen → **Einstellungen** (bzw. **Settings**) → **Connectors**.
3. Bei **GitHub** auf **Verbinden** (bzw. **Connect**) klicken.
4. Du wirst zu GitHub weitergeleitet. Melde dich an und bestätige mit 2FA.
5. **Zugriff festlegen:** GitHub fragt, auf welche Repos Claude zugreifen darf. Wähle **Only select repositories** und nur die Repos, die du wirklich brauchst.
   *Warum?* Claude sieht dann nur das, was es sehen soll.

> **Hinweis zu Repos der Organisation:** Repos der Organisation kannst du oft nicht selbst freigeben. GitHub schickt dann automatisch eine Anfrage an die Verantwortlichen. Sag dem Plattform-Team kurz Bescheid, damit die Freigabe nicht liegen bleibt. Sobald sie erteilt ist, kannst du das Repo in Claude nutzen.

## Teil 5 – Ein Repo in Claude verwenden

**Im Chat:**

1. Klicke im Eingabefeld auf das **+**.
2. Wähle **Add from GitHub**.
3. Suche das Repo oder füge seine Adresse ein.
4. Wähle die Dateien oder Ordner aus, um die es gehen soll.
5. Stelle deine Frage und sende die Nachricht ab. Claude liest die ausgewählten Dateien und antwortet dazu.

**In einem Projekt** (wenn du mit den Dateien öfter arbeitest):

1. Öffne das Projekt in Claude.
2. Bei **Wissen** (bzw. **Project knowledge**) auf **+** und dann auf **GitHub** klicken.
3. Repo suchen und Dateien auswählen. Sie stehen dann in jedem Chat des Projekts zur Verfügung.

> **Wichtig:** Claude bekommt Änderungen im Repo nicht automatisch mit. Wurde das Repo geändert, klicke beim Repo auf **Sync now**, um den neuesten Stand zu holen.

---

## Checkliste

- [ ] Git installiert und mit `git --version` geprüft
- [ ] Git Credential Manager vorhanden (Windows: automatisch, Mac: extra installiert)
- [ ] Name und `noreply`-E-Mail in Git eingetragen
- [ ] Ein Repo geklont und dabei im Browser angemeldet
- [ ] Claude unter **Connectors** mit GitHub verbunden
- [ ] Nur die benötigten Repos für Claude freigegeben
- [ ] Freigabe für Organisations-Repos beim Plattform-Team angefragt
- [ ] Ein Repo in einem Chat oder Projekt in Claude ausprobiert

## Häufige Probleme

| Problem | Lösung |
|---|---|
| `git` wird nicht gefunden | Terminal bzw. Git Bash schließen und neu öffnen. Hilft das nicht, Git erneut installieren |
| Beim Klonen erscheint `Repository not found` | Adresse prüfen. Bist du schon in der Organisation (Einladung angenommen)? Hast du Zugriff auf dieses Repo? Sonst Plattform-Team fragen |
| Git fragt nach Benutzername und Passwort | Der Git Credential Manager fehlt. Windows: Git neu installieren. Mac: Teil 1, Schritt 4 wiederholen |
| Claude zeigt das Repo nicht an | Auf GitHub unter **Settings → Applications** beim Eintrag **Claude** prüfen, ob das Repo freigegeben ist. Bei Organisations-Repos die Freigabe abwarten |
| Claude zeigt einen Hinweis zu „SSO“ | Die Organisation verlangt eine zusätzliche Freigabe. Auf GitHub **Settings → Applications** öffnen, beim Eintrag **Claude** die Organisation freigeben. Trennen und neu verbinden in Claude hilft hier nicht |
| Claude kennt die neuesten Änderungen nicht | Beim Repo in Claude auf **Sync now** klicken |

**Nächster Schritt:** [VS Code installieren und mit GitHub und Claude verbinden](vs-code-einrichten.md). Danach: Änderungen speichern und zu GitHub schicken (eigene Anleitung).

Weitere Infos zur Verbindung mit Claude: <https://support.claude.com/en/articles/10167454-using-the-github-integration>
