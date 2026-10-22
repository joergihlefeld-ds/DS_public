# CLAUDE.md – Repo DS-Privat

Diese Datei beschreibt, wie in diesem Repository gearbeitet wird. Claude liest sie zu Beginn jeder Sitzung.

## Zweck des Repos

`DS-Privat` ist ein **privates** Repository. Es enthält Anleitungen für Kolleg:innen **ohne technischen Hintergrund**. Ziel: Jede Person soll eine Aufgabe allein und ohne Rückfragen erledigen können.

## Ablage

- Alle Anleitungen liegen im Ordner `anleitungen/`.
- Format: **Markdown** (`.md`), keine Word- oder PDF-Dateien.
- Dateinamen: Kleinbuchstaben, Wörter mit Bindestrich, keine Umlaute oder Leerzeichen.
  Beispiel: `github-account-einrichten.md`, `git-mit-claude-verbinden.md`
- Eine Anleitung = eine Aufgabe. Lange Themen lieber in mehrere Dateien aufteilen und verlinken.

## Sprache: einfach und verständlich

- Ansprache mit **du**.
- Kurze Sätze, ein Gedanke pro Satz.
- Fachbegriffe vermeiden. Wenn einer nötig ist: beim ersten Auftreten kurz erklären.
  Beispiel: „Repository (ein Ordner für Projektdateien auf GitHub)“
- Aktiv formulieren: „Klicke auf **Speichern**“ statt „Es muss gespeichert werden“.
- Sagen, **warum** ein Schritt wichtig ist, wenn er sonst übersprungen würde.
- Gendern mit Doppelpunkt: Kolleg:innen, Nutzer:innen.
- Keine Abkürzungen ohne Erklärung (beim ersten Mal ausschreiben, z. B. „Zwei-Faktor-Authentifizierung (2FA)“).

## Aufbau einer Anleitung

Vorbild ist `anleitungen/github-account-einrichten.md`. Jede Anleitung folgt diesem Muster:

1. **Titel** als `# Kurzanleitung: …`
2. **Dauer** und **Was du brauchst** direkt unter dem Titel
3. **Teile** (`## Teil 1 – …`) mit nummerierten Schritten
4. **Checkliste** zum Abhaken (`- [ ] …`)
5. **Häufige Probleme** als Tabelle (Problem | Lösung)
6. **Nächster Schritt** mit Hinweis auf die folgende Anleitung

## Formatierung

- Buttons und Menüpunkte **fett**, genau so geschrieben wie auf dem Bildschirm (auch englisch, z. B. **Settings**).
- Pfade durch Menüs mit Pfeil: **Settings → Emails**
- Wichtige Hinweise als Zitatblock: `> **Hinweis:** …`
- Eingaben, Befehle und Dateinamen in `Code-Schreibweise`.
- Befehle für das Terminal immer in einem eigenen Codeblock und mit einem Satz, was der Befehl tut.
- Links vollständig angeben: `<https://…>`

## Arbeitsweise für Claude

- Neue Anleitungen immer in `anleitungen/` anlegen.
- Vor dem Schreiben prüfen, ob es zum Thema schon eine Anleitung gibt – dann ergänzen statt doppelt anlegen.
- Bestehende Anleitungen mit „Nächster Schritt“ verlinken, wenn eine neue Anleitung daran anschließt.
- Fakten zu Programmen und Webseiten (Menünamen, Abläufe) im Zweifel aktuell prüfen, da sich Oberflächen ändern.
- Keine Passwörter, Tokens, Recovery Codes oder persönliche Daten in Dateien schreiben – auch nicht als Beispiel.
- Text vor dem Speichern noch einmal lesen: Versteht das jemand, der zum ersten Mal davon hört?

## Vorhandene Anleitungen

| Datei | Inhalt |
|---|---|
| `anleitungen/github-account-einrichten.md` | GitHub-Account anlegen, 2FA einrichten, Organisation beitreten |
| `anleitungen/git-und-claude-mit-github-verbinden.md` | Git installieren, Repo klonen, Claude mit GitHub verbinden |

Geplant (laut „Nächster Schritt“): Änderungen speichern und zu GitHub schicken.
