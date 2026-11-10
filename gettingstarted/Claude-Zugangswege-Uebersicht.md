# Claude – Zugangswege und Ressourcen im Überblick

Stand: November 2026 – Funktionen und Namen ändern sich häufig. Details: <https://support.claude.com>

---

## 1. Die Zugangswege

### 🌐 Browser (claude.ai)
- Aufruf über die Webseite, keine Installation nötig
- Volle Chat-Funktionen: Projekte, Artefakte, Websuche, Datei-Uploads, Connectors (z. B. Google Drive, Gmail)
- **Grenze:** kein direkter Zugriff auf deinen Rechner
- **Nicht verwechseln:** *Claude in Chrome* ist eine Browser-Erweiterung, mit der Claude in deinem echten Chrome mit deinen Logins Webseiten bedient

### 📱 Mobile App (iOS/Android)
- Gleicher Account, gleiche Chats wie im Browser (synchronisiert)
- Dazu: Sprachmodus (auch CarPlay), Kamera/Fotos als Eingabe, Push-Benachrichtigungen
- Zugriff auf den Rechner nur, wenn dort die Desktop-App läuft und der Chat damit verbunden ist

### 🖥️ Desktop-App (Windows/macOS)
- „Claude Desktop“ ist **kein eigenes Produkt**, sondern die Desktop-App von Claude
- Dasselbe Claude wie im Browser, **aber mit Zugang zu deinem Rechner**:
  - lokale Ordner freigeben (lesen/schreiben)
  - Computer Use: Desktop-Programme per Bildschirm, Klick und Tastatur bedienen
  - eingebauter Browser mit eigenen Logins
  - lokale MCP-Server (z. B. Home Assistant, Dateisystem)
  - Claude Code integriert
  - Brücke für andere Geräte: ein Chat in der Mobile App kann über die laufende Desktop-App auf den Rechner zugreifen

### ⌨️ Terminal (Claude Code CLI)
- Claude Code als Kommandozeilen-Werkzeug
- Arbeitet direkt in einem lokalen Projektordner bzw. Repo: Dateien, Befehle, Git

### 🧩 VS Code (Erweiterung „Claude Code für VS Code“)
- Technisch Claude Code, aber mit Editor-Oberfläche (Seitenleiste, `@`-Dateiverweise, Kontext aus der Auswahl)
- **Änderungen als Diff im Editor**: vor der Übernahme annehmen oder ablehnen
- Zugriff auf den geöffneten Workspace
- Mit **Remote-SSH** arbeitet Claude auf dem entfernten Rechner (z. B. Raspberry Pi, Server)
- **Nicht verwechseln:** GitHub Copilot in VS Code kann ebenfalls Claude-Modelle nutzen. Das ist aber Copilot und nicht Claude Code (anderes Abo, andere Funktionen).

---

## 2. Claude vs. Claude Code

| | **Claude** | **Claude Code** |
|---|---|---|
| Zweck | Allgemeiner Assistent: Texte, Recherche, Analyse, Dokumente, Präsentationen | Programmieren mit Agenten: Code schreiben, ändern, testen |
| Arbeitsweise | Vor allem Chat, dazu längere Aufgaben in einer Cloud-Umgebung | Arbeitet direkt im Code-Projekt bzw. Repository, führt Befehle aus, macht Git-Commits |
| Wo | Browser, Mobile App, Desktop-App | Terminal, VS Code, Desktop-App, Web, Mobile |
| Zielgruppe | Alle | Entwickler und technisch Versierte |

**Kurz gesagt:** Claude ist der Assistent für alles. Claude Code ist das Werkzeug für Softwareprojekte. Beide nutzen dieselben Modelle (Opus, Sonnet, Haiku).

---

## 3. Matrix: Welcher Zugang erreicht welche Ressourcen?

| Ressource | 🌐 Browser | 📱 Mobile App | 🖥️ Desktop-App | ⌨️ Terminal (CLI) | 🧩 VS Code |
|---|:-:|:-:|:-:|:-:|:-:|
| Chat, Websuche | ✅ | ✅ | ✅ | ✅ (auf Code ausgerichtet) | ✅ (auf Code ausgerichtet) |
| Artefakte, Dokumente, Präsentationen | ✅ | ✅ | ✅ | ❌ | ❌ |
| Online-Dienste (Gmail, Drive …) über Connectors | ✅ | ✅ | ✅ | ⚠️ über MCP einrichtbar | ⚠️ über MCP einrichtbar |
| **GitHub-Repo in der Cloud** | ✅ | ✅ | ✅ | – | – |
| **Lokale Dateien/Ordner** | ❌ <sup>3 | ⚠️¹ | ✅ | ✅ | ✅ (geöffneter Workspace) |
| **Lokales Repo** inkl. Git & Befehlen | ❌ | ⚠️¹ | ✅ (Claude Code) | ✅ | ✅ |
| Änderungen als Diff im Editor prüfen | ❌ | ❌ | ⚠️ eingeschränkt | ❌ | ✅ |
| Lokale Programme bedienen (Computer Use) | ❌ | ⚠️¹ | ✅ | ❌ | ❌ |
| Lokale Erweiterungen (MCP) | ❌ | ⚠️¹ | ✅ | ✅ | ✅ |
| Webseiten mit deinen Logins bedienen | ⚠️² | ⚠️¹ | ✅ (eingebauter Browser) | ❌ | ❌ |

¹ Nur wenn die Desktop-App auf dem Rechner läuft und der Chat damit verbunden ist.
² Nur mit der Chrome-Erweiterung *Claude in Chrome*.

> **Kernidee:** Alles, was **auf deinem Rechner** liegt, braucht Desktop-App, Terminal oder VS Code.
> Alles, was **online** liegt (GitHub, Gmail, Drive, Web), geht von überall.

> <sup>3</sup> **Achtung:** Eine einmal hergestellte Verbindung von Claude-Desktop-App zu einem Ordner auf Deinem Rechner, wirkt auch, wenn Du Claude im Browser aufrufst



---

## 4. Wege zu einem Repo

| Weg | Wo liegt das Repo? | Womit? | PC muss laufen? |
|---|---|---|:-:|
| **Cloud** | GitHub; Claude klont es in eine Cloud-Arbeitsumgebung | Browser, Mobile App, Desktop-App | Nein |
| **Lokal mit Claude Code** | Ordner auf deinem Rechner | Desktop-App (Claude Code), Terminal | Ja |
| **Lokal im Editor** | geöffneter Workspace in VS Code (auch per Remote-SSH) | VS Code-Erweiterung | Ja |
| **Lokal im Chat** | freigegebener Ordner | Desktop-App (normaler Chat) | Ja |

---

## 5. Schnellwahl: Was will ich tun?

| Ziel | Empfohlener Zugang |
|---|---|
| Text, Recherche, Dokument | Browser genügt |
| Unterwegs mit Sprache arbeiten | Mobile App |
| GitHub-Repo bearbeiten, ohne dass der PC an ist | Browser oder App (Cloud) |
| Lokales Repo, ich will jede Änderung sehen und prüfen | **VS Code** |
| Lokales Repo, Claude soll selbstständig arbeiten | Desktop-App (Claude Code) oder Terminal |
| Dateien in meinen Ordnern bearbeiten | Desktop-App |
| Programm auf dem PC bedienen lassen | Desktop-App (Computer Use) |
| Webseite mit meinem Login bedienen | Desktop-App (eingebauter Browser) oder Claude in Chrome |
