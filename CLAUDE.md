# CLAUDE.md – Repo DS_public

Diese Datei beschreibt, wie in diesem Repository gearbeitet wird. Claude liest sie zu Beginn jeder Sitzung.

## Zweck des Repos

`DS_public` ist ein **öffentliches** Repository und wird als Webseite veröffentlicht. Es enthält Anleitungen für Kolleg:innen **ohne technischen Hintergrund**. Ziel: Jede Person soll eine Aufgabe allein und ohne Rückfragen erledigen können.

## Ablage

- Alle Anleitungen liegen im Ordner `anleitungen/`.
- Regeln und Onboarding (Datenschutz, erlaubte Tools, Lizenz) liegen in `onboarding/`. Neue Anleitungen dürfen diesen Regeln nicht widersprechen, z. B. bei erlaubten Connectors.
- Leitfäden für die tägliche Arbeit (keine Schritt-für-Schritt-Anleitungen) liegen in `gut-mit-claude-arbeiten/`.
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
   Direkt darunter der KI-Hinweis:
   `> **Hinweis:** Diese Anleitung wurde mit Unterstützung von Claude erarbeitet. Claude ist ein KI-Assistent (ein Programm mit künstlicher Intelligenz) der Firma Anthropic.`
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

## Webseite (GitHub Pages)

- Das Repo wird über GitHub Pages mit Jekyll als Webseite veröffentlicht, im Corporate Design von DigitalService.
- Layout: `_layouts/default.html`, Gestaltung: `assets/css/style.css`, Einstellungen: `_config.yml`.
- Vorbild für die Gestaltung ist das Design System „DigitalServiceWeb“ (<https://claude.ai/artifact/Q6baZvHFHqTJ3phAwXNhxD>), abgeleitet von digitalservice.bund.de. Farben, Abstände und Schriftstile in `style.css` tragen dieselben Token-Namen (z. B. `--brand`, `--ink`, `--surface-blue`). Neue Gestaltung nur mit diesen Tokens.
- Die Navigation in Header und Footer steht in `_config.yml` unter `navigation`.
- Logo, Favicon und die Schrift Inter liegen in `assets/` und stammen aus dem DigitalService-Design-System. Nicht verändern.
- Neue Anleitungen brauchen keinen Front Matter. Sie bekommen das Layout automatisch.
- Mermaid-Diagramme werden auf der Webseite gezeichnet. Links im Diagramm (`click`) mit `.md` schreiben, die Webseite macht daraus `.html`.
- `CLAUDE.md` und `README.md` werden nicht veröffentlicht.
- Suchmaschinen sind über `<meta name="robots" content="noindex, …">` im Layout ausgeschlossen. Nicht entfernen. Keine `robots.txt` mit `Disallow` anlegen: Dann sieht Google das `noindex` nicht.
- Das Banner „Work in Progress“ schaltest du in `_config.yml` mit `wip: true` bzw. `wip: false` ein und aus.

## Arbeitsweise für Claude

- Neue Anleitungen immer in `anleitungen/` anlegen.
- Vor dem Schreiben prüfen, ob es zum Thema schon eine Anleitung gibt – dann ergänzen statt doppelt anlegen.
- Bestehende Anleitungen mit „Nächster Schritt“ verlinken, wenn eine neue Anleitung daran anschließt.
- Fakten zu Programmen und Webseiten (Menünamen, Abläufe) im Zweifel aktuell prüfen, da sich Oberflächen ändern.
- Keine Passwörter, Tokens, Recovery Codes oder persönliche Daten in Dateien schreiben – auch nicht als Beispiel.
- Das Repo ist öffentlich: keine Namen von Kolleg:innen, keine Links auf interne Entwürfe oder Slack-Kanäle und keine Abläufe nur für Admins aufnehmen.
- Text vor dem Speichern noch einmal lesen: Versteht das jemand, der zum ersten Mal davon hört?

## Vorhandene Anleitungen

| Datei | Inhalt |
|---|---|
| `anleitungen/uebersicht.md` | Nutzen und Use Cases, Reihenfolge aller Anleitungen und wie die Bausteine zusammenhängen (bei neuen Anleitungen ergänzen) |
| `anleitungen/github-account-einrichten.md` | GitHub-Account anlegen, 2FA einrichten, Organisation beitreten |
| `anleitungen/git-und-claude-mit-github-verbinden.md` | Git installieren, Repo klonen, Claude mit GitHub verbinden |
| `anleitungen/vs-code-einrichten.md` | VS Code installieren, mit GitHub anmelden, Erweiterung Claude Code einrichten |
| `anleitungen/claude-md-einrichten.md` | CLAUDE.md anlegen und pflegen |
| `onboarding/claude-regeln-fuer-non-engineers.md` | Regeln für Non-Engineers: Datenschutz, Datenkategorien, Output-Prüfung, erlaubte Connectors, Weg zur Lizenz (WIP) |
| `gut-mit-claude-arbeiten/gut-mit-claude-arbeiten-als-pm.md` | Grundregeln, Setup und Kontextpflege für PMs (Basis: Product Discussion Club 22.10.2026) |

Geplant (laut „Nächster Schritt“): Änderungen speichern und zu GitHub schicken.
