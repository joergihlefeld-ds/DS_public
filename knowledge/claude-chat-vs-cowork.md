# Claude Chat vs. Claude Cowork – Unterschiede und Anleitung

Oct 30, 2026 · @Jörg

## Kurzüberblick

**Chat** ist für Fragen und Gespräche: Claude antwortet direkt im Verlauf. **Cowork** ist für Aufgaben: Claude arbeitet mehrere Schritte selbstständig ab, liest und schreibt Dateien, führt Code aus und liefert ein fertiges Ergebnis.

Wichtig: Anthropic führt Chat und Cowork schrittweise zu **einer** Oberfläche zusammen. Wer im Eingabefeld noch die Auswahl „Chat“ / „Cowork“ sieht, hat die alte Variante. In der neuen Variante entscheidet Claude selbst, welche Werkzeuge es braucht – alles, was vorher nur Cowork konnte, geht dann aus jeder Unterhaltung.

## Vergleich auf einen Blick

| Merkmal | Claude Chat | Claude Cowork |
| --- | --- | --- |
| Arbeitsweise | Frage → Antwort im Gespräch | Ziel beschreiben → Claude plant und erledigt mehrere Schritte |
| Dateien | Hochladen und im Chat besprechen | Erstellt fertige Dateien (Excel mit Formeln, PowerPoint, Dokumente) |
| Lokale Ordner | Kein Zugriff | Liest und schreibt in freigegebenen Ordnern (nur über Desktop-App) |
| Code & Web | Begrenzt | Führt Code aus, sucht im Web, bedient Websites im Browser |
| Laufzeit | Solange man im Gespräch ist | Cloud-Aufgaben laufen weiter, auch wenn der Laptop zu ist |
| Zeitgesteuert | Nein | Geplante Aufgaben möglich |
| Geräte | Web, Desktop, Mobil | Web, Desktop, Mobil; lokale Dateien nur mit geöffneter Desktop-App |
| Verbrauch | Gering | Höher, da mehrere Schritte |

## Wann nehme ich was?

Faustregel: Willst du eine **Antwort**, nimm Chat. Willst du ein **Ergebnis** (eine Datei, eine erledigte Aufgabe), nimm Cowork.

**Chat passt für:**

- „Formuliere diese Mail freundlicher.“
- „Erkläre mir den Unterschied zwischen OZG und OZG 2.0.“
- Brainstorming, kurze Texte, Fragen zu einem hochgeladenen Dokument

**Cowork passt für:**

- „Fasse alle PDFs in meinem Projektordner in einer Excel-Tabelle zusammen.“
- „Erstelle aus diesen Notizen eine Präsentation in unserer Vorlage.“
- „Benenne die Dateien in meinem Ordner nach Datum um.“
- Wiederkehrende Aufgaben, z. B. jeden Montag einen Wochenbericht

In der neuen, zusammengeführten Oberfläche musst du nicht wählen: Beschreibe einfach, was du brauchst.

## Anleitung: Cowork-Aufgabe starten und Ordner hinzufügen

Voraussetzung: ein bezahlter Plan (Pro, Max, Team oder Enterprise) und für lokale Ordner die Claude Desktop-App (Windows, macOS, Linux Beta).

1. **Desktop-App öffnen** und auf die neueste Version aktualisieren.
2. **Neue Aufgabe starten.** Siehst du im Eingabefeld „Chat“ und „Cowork“, wähle „Cowork“. Fehlt die Auswahl, hast du schon die neue Oberfläche – dann einfach losschreiben.
3. **Ordner hinzufügen.** Klicke in der Desktop-App auf „Ordner hinzufügen“ bzw. „Add folder“ und wähle den Ordner aus. Claude kann nur in Ordnern lesen und schreiben, die du so freigibst.
4. **Ziel beschreiben.** Schreibe, was am Ende herauskommen soll, z. B. „Erstelle aus allen Protokollen im Ordner eine Übersicht als Excel-Datei“.
5. **Vorgehen prüfen.** Claude zeigt seinen Plan. Prüfe ihn und lass es dann arbeiten.
6. **Ergebnis abholen.** Fertige Dateien erscheinen neben der Unterhaltung und, wenn gewünscht, direkt im freigegebenen Ordner.

Tipps:

- Freigegebene Ordner findest du unter **Einstellungen → Trusted folders**. Dort kannst du Freigaben auch wieder entfernen.
- Gib nur die Ordner frei, die für die Aufgabe nötig sind.
- Bei Aktionen mit Folgen (Mails senden, wichtige Dateien ändern) die Berechtigung auf „Manuell“ stellen: Dann fragt Claude vor jedem Schritt. Dateien löscht Claude nie ohne ausdrückliche Erlaubnis.

## Fehlerbehebung

| Problem | Wahrscheinliche Ursache | Lösung |
| --- | --- | --- |
| „Ordner hinzufügen“ fehlt | Aufgabe im Browser, in der Mobile-App oder im Chrome-Seitenpanel geöffnet | Aufgabe in der Desktop-App öffnen |
| „Ordner hinzufügen“ fehlt | Cloud-Aufgabe ist nicht mit diesem Rechner verknüpft | In der Desktop-App „Link to this computer“ wählen oder dort eine neue Aufgabe starten |
| „Ordner hinzufügen“ fehlt | Normaler Chat (alte Oberfläche) statt Cowork | Im Eingabefeld „Cowork“ wählen |
| „Ordner hinzufügen“ fehlt oder Ordner wird abgelehnt | Admin-Richtlinie: Cowork deaktiviert (`secureVmFeaturesEnabled`) oder Pfade eingeschränkt (`allowedWorkspaceFolders`) | IT bzw. Org-Owner fragen |
| „Ordner hinzufügen“ fehlt | Veraltete App-Version | Desktop-App aktualisieren und neu starten |
| Claude erreicht den Ordner plötzlich nicht mehr | Desktop-App geschlossen oder Rechner im Ruhezustand | Rechner wecken, App offen lassen; die Verbindung kommt meist von selbst zurück |
| Keine Dateien oder kein Code im Chat | Inkognito-Chat (nutzt die alte Oberfläche) | Normale Unterhaltung starten |

## Quellen

- [Claude Cowork and chat are one Claude](https://support.claude.com/en/articles/16761823-claude-cowork-and-chat-are-one-claude)
- [Get started with Claude Cowork](https://support.claude.com/en/articles/13345190-get-started-with-claude-cowork)
- [Use Claude Cowork on web, desktop, and mobile](https://support.claude.com/en/articles/15520349-use-claude-cowork-on-web-desktop-and-mobile)
- [Enterprise configuration for Claude Desktop](https://support.claude.com/en/articles/12622667-enterprise-configuration-for-claude-desktop)
