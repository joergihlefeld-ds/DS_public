---
title: "Warum KI im Produktmanagement? Nutzen, Use Cases und Reihenfolge"
---

> **Vorher:** Kläre, welche Daten und Tools du mit Claude nutzen darfst. Vertrauliche und personenbezogene Daten gehören nicht in Claude.


## Warum das Ganze? Wie verändert sich die Arbeit der Produktmanager:innen

Ein paar Thesen: 

1. Prototypen ersetzen Spezifikationen. Diskutiert wird am funktionierenden Artefakt, nicht am Dokument. Das verkürzt Feedbackschleifen mit Nutzenden und Auftraggebern deutlich.

2. Die Rollengrenzen verschwimmen. PMs werden technischer: Sie lesen Code, verstehen Architekturentscheidungen besser. Entwickler werden produktnäher: Sie bewerten Nutzerprobleme mit, weil sie schneller Varianten testen können. Die Diziplinen wachsen zusammen.

34. Kontext und Randfälle sind nicht mehr nur für Menschen, sondern auch für Agenten das Arbeitsmaterial. „Prompt-fähige“ Anforderungen werden ein Qualitätsmerkmal von Produktarbeit.

5. Qualitätssicherung und Verantwortung gewinnen an Gewicht. Mehr generierter Code bedeutet mehr Bedarf an Review, Tests, Sicherheit und Wartbarkeit. PMs müssen verstehen, dass „schnell gebaut“ nicht „schnell betriebsreif“ heißt. AI kann helfen das Dilemma zu lösen.

Speziell im öffentlichen Sektor kommen Besonderheiten hinzu: Vergabe- und Datenschutzvorgaben, Barrierefreiheit (BITV), Betriebsverantwortung und die Frage, welche KI-Werkzeuge überhaupt zulässig sind. 

Dort könnte die größte Veränderung sein, dass PM und Entwicklung früher gemeinsam mit Fachreferaten an Prototypen arbeiten und so Anforderungen in der Verwaltung schneller validieren.

Kurz gesagt: weniger Übergabe, mehr gemeinsames Gestalten. Wer als PM Probleme glasklar formulieren und Prototypen selbst anfassen kann, wird wertvoller. Das gilt ebenso für Entwickler, die Produktverständnis mitbringen und generierten Code kritisch prüfen.


## Use Cases für Produktmanager:innen

Diese Beispiele brauchen wenig oder gar keine Programmierkenntnisse. Die Spalte **Womit** zeigt, was du dafür brauchst:
- **Browser** heißt Claude auf <https://claude.ai> mit GitHub-Connector (ab Schritt 2).
- **VS Code** heißt Claude Code in VS Code (ab Schritt 3).

### Verstehen und nachfragen

| Use Case | So kannst du fragen | Womit |
|---|---|---|
| Ein Feature verstehen | „Erkläre mir ohne Fachbegriffe, wie die Anmeldung funktioniert.“ | Browser oder VS Code |
| Regeln im Produkt finden | „Welche Pflichtfelder hat das Antragsformular und welche Prüfungen gibt es?“ | Browser oder VS Code |
| Neu im Team einsteigen | „Gib mir einen Überblick über dieses Repo: Was liegt wo, was ist wichtig?“ | Browser oder VS Code |
| Aufwand besser einschätzen | „Welche Teile des Produkts wären betroffen, wenn wir ein drittes Login-Verfahren einführen?“ | VS Code: durchsucht das ganze Repo |
| Gespräche mit der Entwicklung vorbereiten | „Welche offenen Fragen sollte ich zu diesem Feature stellen?“ | Browser oder VS Code |

### Anforderungen und Planung

| Use Case | So kannst du fragen | Womit |
|---|---|---|
| User Storys schreiben | „Schreibe eine User Story mit Akzeptanzkriterien für den Export als PDF. Berücksichtige, wie der Export heute gebaut ist.“ | Browser oder VS Code |
| Anforderung mit dem Ist-Stand abgleichen | „Prüfe, ob diese Anforderung schon umgesetzt ist und was noch fehlt.“ | VS Code: durchsucht das ganze Repo |
| Release Notes erstellen | „Fasse die Änderungen der letzten zwei Wochen für Nutzer:innen in einfacher Sprache zusammen.“ | VS Code: braucht den Änderungsverlauf |
| Issues vorbereiten | „Formuliere aus meinen Notizen drei Issues mit Beschreibung und Akzeptanzkriterien.“ | Browser oder VS Code |

### Selbst kleine Änderungen machen

| Use Case | So kannst du fragen | Womit |
|---|---|---|
| Texte in der Anwendung verbessern | „Finde alle Fehlermeldungen im Formular und formuliere sie in einfacher Sprache um.“ | VS Code |
| Dokumentation pflegen | „Ergänze im README einen Abschnitt, wie man einen Antrag zurückzieht.“ | VS Code |
| Anleitungen und Konzepte schreiben | „Lege eine neue Anleitung nach unserer Vorlage an.“ (so entsteht auch dieses Repo) | VS Code |
| Einen Klickdummy bauen | „Baue eine einfache HTML-Seite, die den neuen Ablauf zeigt, zum Testen mit Nutzer:innen.“ | VS Code |
| Barrierefreiheit grob prüfen | „Prüfe diese Seite auf fehlende Alternativtexte und zu kleine Schriften.“ | VS Code |

> **Faustregel:** Fängst du gerade erst an? Dann starte mit „Verstehen und nachfragen“. Hier liest Claude nur und ändert nichts.

> **Hinweis:** Keine vertraulichen oder personenbezogenen Daten in Claude oder ins Repository geben. Im Zweifel vorher das Team fragen.

## Die Reihenfolge

Die Anleitungen bauen aufeinander auf. Arbeite sie am besten in dieser Reihenfolge durch.
Klicke auf einen Kasten oder auf einen Link in der Tabelle darunter, um die Anleitung zu öffnen.

```mermaid
flowchart TD
    A["1 · GitHub-Account einrichten<br/>Account, 2FA, Organisation"]
    B["2 · Git und Claude mit GitHub verbinden<br/>Git installieren, Repo klonen, Claude-Connector"]
    C["3 · VS Code einrichten<br/>VS Code, GitHub-Anmeldung, Claude Code"]
    D["4 · CLAUDE.md einrichten<br/>dauerhafte Anweisungen für Claude"]
    E["5 · Änderungen zu GitHub schicken<br/>(geplant)"]

    A --> B --> C --> D --> E

    click A "getting-started/github-account-einrichten.md"
    click B "getting-started/git-und-claude-mit-github-verbinden.md"
    click C "getting-started/vs-code-einrichten.md"
    click D "knowledge/claude-md-einrichten.md"

    style E stroke-dasharray: 5 5
```

> **Hinweis:** Nicht jede Ansicht unterstützt Klicks im Bild (GitHub zum Beispiel nicht). Nutze dann die Tabelle.

| Schritt | Anleitung | Darum geht es | Dauer |
|---|---|---|---|
| 1 | [GitHub-Account einrichten](getting-started/github-account-einrichten.md) | Account anlegen, Zwei-Faktor-Authentifizierung (2FA) einrichten, der Organisation beitreten | ca. 15 Min. |
| 2 | [Git und Claude mit GitHub verbinden](getting-started/git-und-claude-mit-github-verbinden.md) | Git installieren, ein Repository auf den Rechner holen, Claude im Browser mit GitHub verbinden | ca. 20 Min. |
| 3 | [VS Code einrichten](getting-started/vs-code-einrichten.md) | VS Code installieren, mit GitHub anmelden, Erweiterung Claude Code einrichten | ca. 20 Min. |
| 4 | [CLAUDE.md einrichten](knowledge/claude-md-einrichten.md) | Claude dauerhafte Regeln für ein Projekt mitgeben | ca. 10 Min. |
| 5 | Änderungen zu GitHub schicken | *geplant* | |

*Warum diese Reihenfolge?* Jeder Schritt braucht den vorherigen. Ohne GitHub-Account kein Zugriff auf Repositories. Ohne Git kann VS Code keine Repositories holen. Und die CLAUDE.md wirkt erst, wenn Claude in deinem Projektordner arbeitet.

## Wie hängt das alles zusammen?

Vier Bausteine arbeiten zusammen:

```mermaid
flowchart LR
    GH["GitHub<br/>gemeinsamer Speicher im Internet"]
    GIT["Git<br/>holt und schickt Dateien"]
    PC["Dein Projektordner<br/>auf dem Rechner"]
    VSC["VS Code<br/>Dateien ansehen und bearbeiten"]
    CW["Claude im Browser<br/>claude.ai"]
    CC["Claude Code<br/>in VS Code"]

    GH <-->|klonen / hochladen| GIT
    GIT <--> PC
    VSC --> PC
    CC --> PC
    CW -->|liest über Connector| GH
```

- **GitHub** ist der gemeinsame Speicher im Internet. Ein Projektordner dort heißt **Repository** (kurz: Repo).
- **Git** ist ein kleines Programm auf deinem Rechner. Es holt die Dateien aus GitHub und schickt deine Änderungen zurück.
- **VS Code** ist das Programm, in dem du die Dateien auf deinem Rechner ansiehst und bearbeitest.
- **Claude** gibt es auf zwei Wegen:
  - **Im Browser** (<https://claude.ai>): Claude liest Dateien direkt aus GitHub. Claude kann dort nur lesen, nicht ändern (Schritt 2).
  - **In VS Code** (Erweiterung Claude Code): Claude arbeitet in deinem Projektordner. Claude kann Dateien lesen und, wenn du zustimmst, auch ändern (Schritt 3).
- Die **CLAUDE.md** ist eine Datei im Projektordner. Claude Code liest sie zu Beginn jeder Sitzung (Schritt 4).

> **Faustregel:** Willst du nur Fragen zu Dateien stellen, reicht Claude im Browser. Willst du Dateien gemeinsam mit Claude bearbeiten, nutze Claude Code in VS Code.
