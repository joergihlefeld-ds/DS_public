# Kurzanleitung: CLAUDE.md in Claude Desktop nutzen

**Dauer:** ca. 10 Minuten
**Was du brauchst:** Claude Desktop (Code-Tab), einen Projektordner, einen Texteditor (z. B. VS Code oder Notepad)

---

## Was ist die CLAUDE.md?

Die **CLAUDE.md** ist eine Textdatei im Markdown-Format. Claude liest sie zu Beginn jeder Sitzung im Code-Tab automatisch. Sie funktioniert wie ein dauerhaftes Briefing: Was dort steht, musst du nicht in jedem Chat neu erklären.

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
| `C:\Users\<Name>\.claude\CLAUDE.md` | **alle** deine Sitzungen, nur für dich |
| `CLAUDE.md` im Projektordner | **dieses Projekt**; kann über Git mit dem Team geteilt werden |
| `CLAUDE.md` in einem Unterordner | wird zusätzlich gelesen, wenn Claude in diesem Unterordner arbeitet |

Gibt es mehrere Dateien, liest Claude alle. Die spezifischere Datei ergänzt die allgemeinere.

> **Faustregel:** Persönliche Vorlieben (Sprache, Tonfall) gehören in die Datei im Benutzerordner. Alles, was nur ein Projekt betrifft, gehört in den Projektordner.

## Teil 2 – CLAUDE.md anlegen

### Variante A: Claude macht einen Entwurf (empfohlen)

1. In Claude Desktop den **Code-Tab** öffnen.
2. Eine neue Sitzung **mit deinem Projektordner** starten.
3. `/init` eingeben und absenden.
4. Claude schaut sich den Ordner an und schreibt eine erste `CLAUDE.md`.
5. Entwurf lesen und anpassen: Unpassendes streichen, Fehlendes ergänzen.

### Variante B: Von Hand

1. Im Projektordner eine neue Datei mit dem Namen `CLAUDE.md` anlegen.
   - Achtung: Windows blendet Endungen oft aus. Die Datei darf nicht `CLAUDE.md.txt` heißen.
2. Anweisungen hineinschreiben (Beispiel siehe Teil 3).
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

## Teil 4 – Tipps für eine gute CLAUDE.md

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
| Claude beachtet die Datei nicht | Prüfen, ob die Sitzung wirklich im richtigen Ordner läuft. Sitzungen ohne Ordner lesen nur die persönliche Datei im Benutzerordner. |
| Änderungen wirken nicht | Die Datei wird zu Beginn einer Sitzung gelesen. Neue Sitzung starten. |
| Datei heißt `CLAUDE.md.txt` | Im Explorer unter *Ansicht → Einblenden → Dateinamenerweiterungen* aktivieren und umbenennen. |
| Ordner `.claude` im Benutzerordner fehlt | Einfach selbst anlegen: `C:\Users\<Name>\.claude` |
| Claude hält sich nur teilweise an Regeln | Regeln kürzer und eindeutiger formulieren, Widersprüche entfernen. |

**Nächster Schritt:** Eine persönliche `CLAUDE.md` im Benutzerordner mit deinen Grundregeln (Sprache, Tonfall, Vorlagen) anlegen.
