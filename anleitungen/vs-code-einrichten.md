# Kurzanleitung: VS Code installieren und mit GitHub und Claude verbinden

**Dauer:** ca. 20 Minuten
**Was du brauchst:** deinen GitHub-Account mit 2FA (siehe [GitHub-Account einrichten](github-account-einrichten.md)), Git auf deinem Rechner (siehe [GitHub mit Git und Claude verbinden](git-und-claude-mit-github-verbinden.md), Teil 1 und 2), einen Claude-Account mit Bezahl-Plan (z. B. Team oder Enterprise), einen Rechner mit Windows oder Mac

> **Worum geht es?**
> **VS Code** (Visual Studio Code) ist ein kostenloses Programm von Microsoft zum Bearbeiten von Dateien. Du siehst darin alle Dateien eines Projektordners auf einen Blick.
> Du kannst VS Code mit **GitHub** verbinden. Dann holst du Repositories (Projektordner auf GitHub) mit wenigen Klicks auf deinen Rechner.
> Mit der Erweiterung **Claude Code** arbeitet Claude direkt in VS Code mit. Claude kann dann die Dateien im geöffneten Ordner lesen und auf Wunsch bearbeiten.

---

## Teil 1 – VS Code installieren

### Windows

1. Öffne <https://code.visualstudio.com/download> und klicke auf **Windows**.
2. Starte die heruntergeladene Datei.
3. Bestätige die Lizenzbedingungen und klicke auf **Weiter**.
4. Bei **Zusätzliche Aufgaben auswählen** diese Haken setzen:
   - **Aktion „Mit Code öffnen“ dem Dateikontextmenü hinzufügen**
   - **Aktion „Mit Code öffnen“ dem Verzeichniskontextmenü hinzufügen**
   - **Zu PATH hinzufügen** (meist schon gesetzt)

   *Warum?* So kannst du später jeden Ordner per Rechtsklick direkt in VS Code öffnen.
5. Klicke auf **Installieren** und am Ende auf **Fertigstellen**.

> **Hinweis:** Darfst du auf deinem Dienstrechner keine Programme installieren? Dann wende dich an die IT oder das Plattform-Team. Oft gibt es VS Code auch im Software-Katalog deines Rechners.

### Mac

1. Öffne <https://code.visualstudio.com/download> und klicke auf **Mac**.
2. Öffne die heruntergeladene Datei im Ordner **Downloads** per Doppelklick. Es erscheint das Programm **Visual Studio Code**.
3. Ziehe **Visual Studio Code** in den Ordner **Programme**.
   *Warum?* Sonst bleibt das Programm im Download-Ordner und lässt sich nicht richtig aktualisieren.
4. Starte VS Code aus dem Ordner **Programme**. Fragt der Mac nach, ob du das Programm öffnen willst, klicke auf **Öffnen**.

### Auf Deutsch umstellen (optional)

VS Code startet oft auf Englisch. Meist zeigt es unten rechts von selbst einen Hinweis zum Sprachpaket an. Klicke dann auf **Install and Restart**.

Kommt kein Hinweis:

1. Drücke `Strg + Umschalt + P` (Mac: `Cmd + Umschalt + P`). Oben öffnet sich ein Eingabefeld.
2. Tippe `Configure Display Language` und wähle den Eintrag aus.
3. Wähle **Deutsch** und starte VS Code neu.

> **Hinweis:** In dieser Anleitung stehen Menünamen auf Deutsch und in Klammern auf Englisch. So findest du dich in beiden Sprachen zurecht.

## Teil 2 – VS Code mit GitHub verbinden

### Anmelden

1. Klicke in VS Code unten links auf das **Personen-Symbol** (**Konten** bzw. **Accounts**).
2. Wähle **Mit GitHub anmelden** (bzw. **Sign in with GitHub**). Wird der Eintrag nicht angezeigt, wähle **Einstellungen sichern und synchronisieren** (bzw. **Backup and Sync Settings**) und dann **Mit GitHub anmelden**.
3. Dein Browser öffnet sich. Melde dich bei GitHub an und bestätige mit deinem zweiten Faktor (2FA).
4. Klicke auf **Authorize Visual Studio Code**.
5. Der Browser fragt, ob er VS Code öffnen darf. Klicke auf **Öffnen** bzw. **Zulassen**.
6. Zurück in VS Code: Unter dem Personen-Symbol steht jetzt dein GitHub-Benutzername.

> **Hinweis:** VS Code bietet dir vielleicht **GitHub Copilot** an. Das ist ein anderer KI-Assistent. Für diese Anleitung brauchst du ihn nicht. Du kannst den Hinweis schließen.

### Ein Repository auf den Rechner holen

Hast du das Repo schon mit der Git-Anleitung geklont? Dann öffne einfach den Ordner: **Datei → Ordner öffnen** (bzw. **File → Open Folder**). Sonst geht es so:

1. Klicke links in der Seitenleiste auf das Symbol mit den drei verbundenen Punkten (**Quellcodeverwaltung** bzw. **Source Control**).
2. Klicke auf **Repository klonen** (bzw. **Clone Repository**).
3. Wähle **Von GitHub klonen** (bzw. **Clone from GitHub**).
4. Tippe den Namen des Repos ein und wähle es aus der Liste.
5. Wähle einen Ordner, in dem das Repo liegen soll, z. B. „Dokumente“.
6. VS Code fragt, ob es das Repo öffnen soll. Klicke auf **Öffnen** (bzw. **Open**).
7. Fragt VS Code, ob du den Autor:innen der Dateien vertraust, klicke bei Repos deiner Organisation auf **Ja, ich vertraue den Autoren** (bzw. **Yes, I trust the authors**).

Links siehst du jetzt alle Dateien des Repos. Ein Klick auf eine Datei öffnet sie.

## Teil 3 – Claude mit VS Code verbinden

### Erweiterung installieren

Eine **Erweiterung** ist ein Zusatzprogramm für VS Code.

1. Klicke links in der Seitenleiste auf das Symbol mit den vier Quadraten (**Erweiterungen** bzw. **Extensions**).
2. Tippe oben in das Suchfeld `Claude Code`.
3. Wähle den Eintrag **Claude Code for VS Code**. Prüfe, dass darunter **Anthropic** als Herausgeber steht.
   *Warum?* Es gibt ähnlich benannte Erweiterungen von anderen Anbietern.
4. Klicke auf **Installieren** (bzw. **Install**).

### Bei Claude anmelden

1. Klicke oben rechts im Editor auf das **Claude-Symbol** (ein orangefarbener Stern). Alternativ links in der Seitenleiste auf **Claude Code**.
   Rechts öffnet sich das Claude-Fenster.
2. Wähle die Anmeldung mit deinem **Claude-Account** (Eintrag mit **Claude.ai** oder **Subscription**).
3. Dein Browser öffnet sich. Melde dich bei Claude an, so wie du es von <https://claude.ai> kennst.
4. Klicke auf **Autorisieren** (bzw. **Authorize**).
5. Zurück in VS Code: Das Claude-Fenster zeigt jetzt ein Eingabefeld.

## Teil 4 – Claude in VS Code ausprobieren

1. Öffne einen Projektordner in VS Code (siehe Teil 2).
2. Öffne das Claude-Fenster (Claude-Symbol oben rechts).
3. Tippe zum Beispiel:
   > „Erkläre mir in drei Sätzen, was in diesem Ordner liegt.“
4. Sende die Nachricht mit der Eingabetaste ab. Claude schaut sich die Dateien an und antwortet.

> **Wichtig:** Will Claude eine Datei ändern oder einen Befehl ausführen, fragt es dich vorher. Lies die Anfrage und klicke erst dann auf **Ja** bzw. **Yes**. So behältst du die Kontrolle über deine Dateien.

> **Tipp:** Liegt im Projektordner eine `CLAUDE.md`, liest Claude sie zu Beginn automatisch. Wie du sie anlegst, steht in [CLAUDE.md einrichten](claude-md-einrichten.md).

---

## Checkliste

- [ ] VS Code installiert und gestartet
- [ ] Optional: Sprache auf Deutsch umgestellt
- [ ] In VS Code mit GitHub angemeldet (Benutzername unten links sichtbar)
- [ ] Ein Repo geklont oder geöffnet
- [ ] Erweiterung **Claude Code** von **Anthropic** installiert
- [ ] Mit dem Claude-Account angemeldet
- [ ] Eine erste Frage an Claude gestellt

## Häufige Probleme

| Problem | Lösung |
|---|---|
| **Repository klonen** fehlt oder VS Code meldet „Git nicht gefunden“ | Git ist nicht installiert. Teil 1 der [Git-Anleitung](git-und-claude-mit-github-verbinden.md) erledigen und VS Code neu starten |
| Nach der Anmeldung im Browser passiert in VS Code nichts | Im Browser erneut auf **Öffnen** klicken. Hilft das nicht, VS Code schließen, neu öffnen und die Anmeldung wiederholen |
| Das Repo erscheint nicht in der Liste | Bist du schon in der Organisation (Einladung angenommen)? Hast du Zugriff auf das Repo? Sonst Plattform-Team fragen |
| Das Claude-Symbol fehlt | Eine Datei im Editor öffnen, dann erscheint es oben rechts. Sonst VS Code neu starten. Prüfen, ob die Erweiterung unter **Erweiterungen** installiert und aktiviert ist |
| Claude meldet, dass der Plan nicht passt | Die Erweiterung braucht einen Bezahl-Plan (z. B. Team oder Enterprise). Im Team nachfragen, wie du Zugang bekommst |
| Claude sieht die Dateien nicht | In VS Code über **Datei → Ordner öffnen** einen Ordner öffnen. Einzelne Dateien ohne Ordner reichen nicht |
| VS Code ist nach dem Neustart wieder Englisch | Teil 1, „Auf Deutsch umstellen“, wiederholen und **Deutsch** auswählen |

**Nächster Schritt:** Änderungen speichern und zu GitHub schicken (eigene Anleitung).

Weitere Infos zu Claude in VS Code: <https://code.claude.com/docs/en/vs-code>
