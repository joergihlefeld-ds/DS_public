# Claude Onboarding – Gut mit Claude arbeiten als PM

**Für**: PMs die beim DigitalService Claude neu bekommen

**Ziel**: eigenes Setup und Best Practices

**Basis**: [Product Discussion Club 22.10.2026 mit Julius Bauer (TeleClinic)](https://miro.com/app/board/uXjVGMjD2Ek=/?moveToWidget=3458764683612562749&cot=14)


## Grundprinzip von LLMs

- **Output = Basiert auf der Qualität des Inputs!**
    - Je besser der Kontext, desto kürzer kann der Prompt sein.
- **Effektiv:**
    - der richtige Kontext, nicht aller.
- **Effizient:**
    - geladen statt kopiert.
- **Agent statt Chat:**
    - Claude führt Aktionen aus, liest also Dateien, durchsucht z.B. Jira und legt Entwürfe an.

## Setup in 4 Schritten

| # | Hebel | Was | Start |
| --- | --- | --- | --- |
| 1 | **CLAUDE.md** | Anweisungen, die jede Session von Claude benutzt wird | Rolle, Ziele, Ordner-Index, Regeln. Kurz halten. |
| 2 | **Arbeitsordner** | Dein zentraler lokaler Ort für Kontext, navigiere da hin wo Claude lesen soll | `KPIs/ · Projekte/ · Wissen/ · Vorlagen/`, pro Projekt ein README mit Datum / Status |
| 3 | **Skills** | Wiederholbare Workflows | Dritte Wiederholung? Einmal durchspielen, dann „Claude Mach daraus einen Skill“. |
| 4 | **Connectors (MCP)** | Zugriff auf andere Tools | Können nur Kontext holen oder etwas ausführen. Welche bei DS erlaubt sind, regeln die Claude-Regeln für Non-Engineers. |

## 5 Regeln für die Arbeit mit Claude:

1. **Du verantwortest den Output.** Nicht „Claude hat das gemacht“, sondern „Ich mit Claude“.
2. **Immer prüfen.** Claude bringt dich zu 90–95 % ans Ziel, den Rest entscheidest du. Tipp: vorher 1–2 Runden „Prüf dich selbst“ laufen lassen.
3. **Nur Entwürfe, nie direkt senden!**
4. **„Last Edited“-Zeile in jeder Datei**, damit Claude weiß, was aktuell ist. Veraltetes archivieren statt löschen.
5. **Vertrauliches und personenbezogene Daten bleiben draußen.** 

## Kontext pflegen und teilen:

- **Aufwand:** ca. 2 Stunden pro Woche. Am besten per Routine automatisieren (Aufräumen, Tagesstart/-abschluss).
- **Indizes** in den obersten Dateien machen den Ordner für Claude leichter navigierbar (Kontext again).
- **Im Team:**
    - Artifacts zum Kommentieren teilen.
    - Kontext gemeinsam pflegen und reviewen (TeleClinic nutzt dafür ein GitLab-Repo).
    - Skills teilen, jeweils mit einer verantwortlichen Person.
- **DS-Vorteil:** Was bei uns ohnehin offen ist (Blogposts, Infos), kann Claude direkt als Kontext nutzen.

## Offen für DS

- Wer pflegt Standardvorgaben (CLAUDE.md-Vorlage, Regeln)?
- Wo teilen wir Skills?
- Gemeinsamer Kontext-Ordner für PMs?
- Folgeformat „DS-Claude-Routinen“: wer, bis wann?
