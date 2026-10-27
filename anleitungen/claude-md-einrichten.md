# Kurzanleitung: CLAUDE.md einrichten und pflegen

> **Hinweis:** Diese Anleitung wurde mit Unterstützung von Claude erarbeitet. Claude ist ein KI-Assistent (ein Programm mit künstlicher Intelligenz) der Firma Anthropic.

**Dauer:** ca. 10 Minuten
**Was du brauchst:** Claude Code in VS Code (siehe [VS Code einrichten](vs-code-einrichten.md)) **oder** Claude Desktop mit dem Code-Tab, einen Projektordner

---

## Was ist die CLAUDE.md?

Die **CLAUDE.md** ist eine Textdatei im Markdown-Format. Claude liest sie zu Beginn jeder Sitzung automatisch. Sie funktioniert wie ein dauerhaftes Briefing: Was dort steht, musst du nicht in jedem Chat neu erklären.

Das klappt auf zwei Wegen. Die Datei ist bei beiden dieselbe:

- **In VS Code** mit der Erweiterung **Claude Code**: Das hast du in der Anleitung [VS Code einrichten](vs-code-einrichten.md) eingerichtet.
- **In Claude Desktop** im **Code-Tab**: Claude Desktop ist das Programm von Claude für deinen Rechner. Im Code-Tab arbeitet Claude in einem Ordner auf deinem Rechner.

> **Hinweis:** Claude im Browser (<https://claude.ai>) und die normalen Chats in Claude Desktop lesen die CLAUDE.md nicht. Sie wirkt nur, wenn Claude in einem Ordner auf deinem Rechner arbeitet.

Typische Inhalte:

- **Projektkontext:** Worum geht es? Wie ist der Ordner aufgebaut?
- **Arbeitsanweisungen:** z. B. „Antworte auf Deutsch“, „Präsentationen immer in der BMDS-Vorlage“
- **Konventionen:** Schreibstil, Dateinamen, Gendern
- **Grenzen:** was Claude nicht tun oder nicht verändern soll
- **Befehle** (bei Code-Projekten): wie man Tests startet oder baut

## Teil 1 – Den richtigen Ort wählen

Wo die Datei liegt, entscheidet, wofür sie gilt:

| Ort | Gilt für |
|---|---|
| Ordner `.claude` in deinem Benutzerordner:<br>Windows: `C:\Users\<Name>\.claude\CLAUDE.md`<br>Mac: `/Users/<Name>/.claude/CLAUDE.md` | **alle** deine Sitzungen, nur für dich |
| `CLAUDE.md` im Projektordner | **dieses Projekt**; kann über Git mit dem Team geteilt werden |
| `CLAUDE.md` in einem Unterordner | wird zusätzlich gelesen, wenn Claude in diesem Unterordner arbeitet |

Gibt es mehrere Dateien, liest Claude alle. Die spezifischere Datei ergänzt die allgemeinere.

> **Faustregel:** Persönliche Vorlieben (Sprache, Tonfall) gehören in die Datei im Benutzerordner. Alles, was nur ein Projekt betrifft, gehört in den Projektordner.

## Teil 2 – CLAUDE.md anlegen

### Variante A: Claude macht einen Entwurf (empfohlen)

1. Claude mit deinem Projektordner öffnen:
   - **VS Code:** **Datei → Ordner öffnen** (bzw. **File → Open Folder**) und den Projektordner wählen. Dann oben rechts auf das **Claude-Symbol** klicken.
   - **Claude Desktop:** Den **Code-Tab** öffnen und eine neue Sitzung **mit deinem Projektordner** starten.
2. `/init` eingeben und absenden.
3. Claude schaut sich den Ordner an und schreibt eine erste `CLAUDE.md`. Vorher fragt Claude dich. Bestätige mit **Ja** bzw. **Yes**.
4. Entwurf lesen und anpassen: Unpassendes streichen, Fehlendes ergänzen.

### Variante B: Von Hand

1. Im Projektordner eine neue Datei mit dem Namen `CLAUDE.md` anlegen.
   - **In VS Code** geht das am einfachsten: In der Dateiliste links mit der rechten Maustaste auf den Projektordner klicken → **Neue Datei** (bzw. **New File**) → `CLAUDE.md` eintippen.
   - Achtung bei anderen Programmen: Windows blendet Endungen oft aus. Die Datei darf nicht `CLAUDE.md.txt` heißen.
2. Anweisungen hineinschreiben (Beispiel siehe Teil 3, Vorlage für PMs siehe Teil 4).
3. Speichern. Ab der nächsten Sitzung in diesem Ordner liest Claude die Datei.

### Variante C: Im Chat ergänzen lassen

Sag einfach in einer laufenden Sitzung:
> „Nimm in die CLAUDE.md auf, dass Präsentationen immer in der BMDS-Vorlage erstellt werden.“

Claude ergänzt die Datei dann selbst.

## Teil 3 – Beispiel

```markdown
# Projekt: Bürgerportal-Konzept

## Kontext
Konzeptpapiere und Präsentationen für das neue Bürgerportal.
Zielgruppe: Verwaltungsmitarbeitende, keine Technik-Profis.

## Regeln
- Antworte auf Deutsch, sachlich und in einfacher Sprache.
- Gendern mit Doppelpunkt (Nutzer:innen).
- Präsentationen immer in der BMDS-Vorlage.
- Dateinamen: klein, mit Bindestrich, ohne Umlaute (z. B. `konzept-login.md`).

## Ordner
- `recherche/` – Quellen, **nicht verändern**
- `entwuerfe/` – Arbeitsstände
- `final/` – abgestimmte Fassungen, nur nach Rückfrage ändern
```

## Teil 4 – Vorlage für Produktmanager:innen

Diese Vorlage kannst du kopieren und ausfüllen. Ersetze alles in eckigen Klammern. Abschnitte, die du nicht brauchst, löschst du einfach.

```markdown
# CLAUDE.md – [Produktname]

## Produktkontext
Produkt: [Name und ein Satz, worum es geht]
Phase: [Discovery / Pilot / Betrieb / Skalierung]
Aktueller Fokus: [Ziel des Quartals oder Thema des Sprints]
Werkzeuge im Team: [z. B. Jira, Figma, PostHog, GitHub]

## Wie ich arbeite
- Konzepte und Anforderungen: kurz. Problem → Lösung → Erfolgskriterien → offene Fragen.
- Auswertung von Interviews: Schmerzpunkte immer mit wörtlichen Zitaten belegen.
- Updates für Stakeholder: Zusammenfassung zuerst, Details darunter.
- Release Notes: Sprache der Nutzer:innen, keine Ticketnummern, keine Fachbegriffe.
- Antworte auf Deutsch, in einfacher Sprache. Gendern mit Doppelpunkt.

## Wichtige Dateien
- `kontext/produkt.md` – Überblick über Produkt und Strategie
- `kontext/nutzende.md` – Zielgruppen und Personas
- `kontext/team.md` – Team, Rollen, technische Rahmenbedingungen
- `recherche/` – Interviews (nur anonymisiert), Umfragen, Marktanalyse
- `vorlagen/` – Vorlagen für Konzepte, Release Notes, Agenden
- `arbeit/` – laufende Arbeitsstände

## Verbundene Tools
- [nur Tools, die laut Claude-Regeln erlaubt sind, z. B. Figma, PostHog]
- [GitHub: Repo-Name, nur wenn für das Projekt freigegeben]

## Standards für Ergebnisse
- Ergebnisse im passenden Ordner speichern, meist in `arbeit/` oder `recherche/`.
- Vor dem Überschreiben einer Datei immer fragen.
- Standardformat ist Markdown, außer ich sage etwas anderes.
- Nur Entwürfe erstellen. Nichts direkt senden oder veröffentlichen.
- Oben in jeder Datei eine Zeile „Zuletzt bearbeitet: [Datum]“ pflegen.
```

> **Wichtig:** Trag bei **Verbundene Tools** nur ein, was die Claude-Regeln deiner Organisation erlauben. Slack, Gmail, Google Kalender und Confluence über den Atlassian-Connector sind bei DigitalService zum Beispiel verboten. Interviews und Meeting-Notizen kommen nur anonymisiert in den Ordner `recherche/`.

*Quelle:* Übersetzt und angepasst nach [Claude Code for Product Managers](https://www.prodmgmt.world/resources/claude-code#getting-started) von Prodmgmt World. Dort gibt es auch fertige Prompts für typische PM-Aufgaben, zum Beispiel die Auswertung von Interviews oder Release Notes. Die Seite ist auf Englisch und wirbt am Ende für ein Bezahlprodukt. Das brauchst du nicht.

## Teil 5 – Tipps für eine gute CLAUDE.md

1. **Kurz halten.** Stichpunkte statt Fließtext. Eine bis zwei Bildschirmseiten reichen meistens.
2. **Konkret formulieren.** „Gendern mit Doppelpunkt“ statt „achte auf gute Sprache“.
3. **Nur Dauerhaftes aufnehmen.** Einmalige Aufgaben gehören in den Chat, nicht in die Datei.
4. **Keine Geheimnisse.** Keine Passwörter, Tokens oder personenbezogenen Daten. Projektdateien werden oft per Git geteilt.
5. **Regelmäßig pflegen.** Wenn du Claude etwas zum dritten Mal erklärst, gehört es in die CLAUDE.md.
6. **Andere Dateien einbinden (optional):** Mit `@pfad/zur/datei.md` kannst du auf eine weitere Datei verweisen, z. B. einen Styleguide. Claude liest sie dann mit.

---

## Checkliste

- [ ] Entschieden: persönliche Datei, Projektdatei oder beides
- [ ] `CLAUDE.md` angelegt (per `/init`, von Hand oder per Chat)
- [ ] Dateiname geprüft (keine versteckte Endung `.txt`)
- [ ] Kontext, Regeln und wichtige Ordner eingetragen
- [ ] Keine Passwörter oder vertraulichen Daten enthalten
- [ ] Neue Sitzung gestartet und getestet, ob Claude sich an die Regeln hält

## Häufige Probleme

| Problem | Lösung |
|---|---|
| Claude beachtet die Datei nicht | Prüfen, ob die Sitzung wirklich im richtigen Ordner läuft (VS Code: Ordner geöffnet? Claude Desktop: Code-Tab mit Ordner?). Sitzungen ohne Ordner lesen nur die persönliche Datei im Benutzerordner. Claude im Browser liest die Datei nie. |
| Änderungen wirken nicht | Die Datei wird zu Beginn einer Sitzung gelesen. Neue Sitzung starten. |
| Datei heißt `CLAUDE.md.txt` | Im Explorer unter *Ansicht → Einblenden → Dateinamenerweiterungen* aktivieren und umbenennen. |
| Ordner `.claude` im Benutzerordner fehlt | Einfach selbst anlegen. Windows: `C:\Users\<Name>\.claude`. Mac: `/Users/<Name>/.claude`. Der Mac versteckt Ordner mit Punkt am Anfang. Im Finder blendest du sie mit `Cmd + Umschalt + .` ein. |
| Claude hält sich nur teilweise an Regeln | Regeln kürzer und eindeutiger formulieren, Widersprüche entfernen. |

**Nächster Schritt:** Eine persönliche `CLAUDE.md` im Benutzerordner mit deinen Grundregeln (Sprache, Tonfall, Vorlagen) anlegen. Danach: Änderungen speichern und zu GitHub schicken (eigene Anleitung, geplant).
