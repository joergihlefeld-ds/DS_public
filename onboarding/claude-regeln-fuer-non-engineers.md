# Claude-Regeln für Non-Engineers

## 1. Rechtlicher Rahmen & Datenverarbeitung

- **Lizenzmodell:** Wir nutzen derzeit **Teams-Lizenzen**.
- **Ort der Datenverarbeitung:** Aufgrund der aktuellen Lizenzen findet die Datenverarbeitung derzeit auch auf Servern in den **USA** statt.
- **Modell-Training durch Anthropic:**
    - **Standard:** Anthropic nutzt Eingaben und Ausgaben aus unseren Teams-Lizenzen **nicht** zum Trainieren von Modellen.
    - ⚠️ **WICHTIGE AUSNAHME (Feedback-Button):** Sobald du den **Daumen-hoch / Daumen-runter Button** in Claude klickst oder explizit Feedback sendest, gibst du die entsprechenden Chats für das Modelltraining frei. Diese “Daumen hoch” Funktion wird in unserem Zugang ausgeschaltet. 
- **Account-Nutzung:** Anmeldungen dürfen **ausschließlich mit der persönlichen Arbeitsmail** erfolgen. Anmeldungen über Teammails oder die Nutzung privater Accounts für Arbeitsmaterial sind strikt untersagt.


## 2. Dateneingabe je nach Datenkategorie:

Siehe hierzu auch →[DigitalService Datenschutzkonzept](https://digitalservicebund.atlassian.net/wiki/spaces/DP/pages/1942388893/DigitalService+Datenschutzkonzept)

| **Daten:** | **Status:** |  |
| --- | --- | --- |
| Externe personenbezogene Daten | ❌ Verboten | Kundendaten & externe Personenbezüge dürfen niemals eingegeben werden. (Ausnahme: Eigene Daten des Mitarbeiters sind erlaubt). |
| Anonymisierte / Pseudonymisierte Daten | ✅ Erlaubt | Pseudonymisierung von Namen ist okay. Meeting-Notizen dürfen nur verarbeitet werden, wenn alle Personenbezüge vorab vollständig anonymisiert wurden. |
| Verträge & Vereinbarungen | ⚠️ Bedingt | Nur erlaubt, wenn Namen und Preise vorab vollständig gelöscht wurden! (Struktur an A2J-Verträgen der Website orientieren). |
| Slides & Dokumente | ⚠️ Bedingt | Erlaubt, wenn gefiltert und frei von Personenbezügen. Das DigitalServiceTemplate ist freigegeben; das BMDS-Template muss angefragt werden (außer wenn öffentlich). |


Wenn du eine der folgenden Fragen mit Ja beantworten kannst dürfen die Daten nicht auf Claude verarbeitet werden:

- **Verschlusssache:** Sind die Daten unter Verschlusssache?
- **NDA (Geheimhaltungsvereinbarung):** Fallen die Daten unter einen NDA?
- **Personenbezug:** Werden externe personenbezogene Daten verarbeitet?
- **Vertragsspezifika:** Werden Vertragsdetails wie Namen und Preise verarbeitet?

## 3. Datenausgabe/ Output

Alle durch KI generierten Ergebnisse (Outputs) müssen vor der Weiterverwendung oder Veröffentlichung stets von einer geeigneten Person geprüft werden. Die Art der Prüfung richtet sich nach dem jeweiligen Anwendungsfall:

- **Einfache interne Kommunikation (z. B. Mails oder Nachrichten an Kolleg:innen):**

  *Prüfung durch dich selbst.* Lies den generierten Text sorgfältig durch und passe ihn an, bevor du ihn absendest. Du trägst die finale Verantwortung für deine Nachricht.
- **Dokumente & offizielle Inhalte (z. B. Kunden-Mails, Berichte, Präsentationen):**

  *Prüfung durch eine zweite Person (Vier-Augen-Prinzip).* Lass den Output vor der Weitergabe von einer qualifizierten Kollegin oder einem qualifizierten Kollegen gegenlesen.
- **Generierter Code:**

  *Freigabe durch einen Engineer.* KI-generierter Code darf erst nach Überprüfung und expliziter Freigabe durch eine geeignete Person genutzt oder gepusht werden.

  *Hinweis:* Wir arbeiten aktuell an einem internen Prozess, wie eigenständig gebaute Tools in Zukunft standardisiert freigegeben werden können.

 

## 4. Tool-Anbindungen & MCP-Konnektoren (Wird global durch IT eingestellt)

| Tool / Integration | Status | Nutzungsvorgaben & Schutzmaßnahmen |
| --- | --- | --- |
| **Figma** | ✅ **Erlaubt** | Darf ohne Einschränkungen mit Claude genutzt werden. |
| **Posthog** | ✅ **Erlaubt** | Darf ohne Einschränkungen mit Claude genutzt werden. |
| **GitHub** | ⚠️ **Bedingt** | Erlaubnis der Anbindung hängt vom jeweiligen Projekt ab. |
| **Jira** | ⚠️ **Bedingt** | Nur erlaubt, wenn zwingend ein **Backup existiert** und Claude nichts zerstören kann (*Human in control*). |
| **Google Drive** | ⚠️ **Bedingt** | Anbindung nur über einen **einzelnen, dedizierten Ordner** auf dem Computer The Google workspace - MCP connection would be done by the platform if necessary. This is due to the Platform team are admins for the Google Cloud projects. |
| **Miro** | ⚠️ **Bedingt** | Nur in einer extra gesicherten Umgebung als Teil des MCP-Test-Accounts. Der Zugriff auf ein über Claude erstelltes Miro-Board erfolgt über den Account, mit dem das Board erstellt wurde. |
| **Slack** | ❌ **Verboten** | Darf nicht angebunden / verbunden werden. |
| **GMail** | ❌ **Verboten** | Darf nicht angebunden / verbunden werden. |
| **Google Kalender** | ❌ **Verboten** | Darf nicht angebunden / verbunden werden. |
| **Claude Code mit Chrome verwenden** | ❌ **Verboten** | Darf nicht angebunden / verbunden werden. |
| **Confluence (via Atlassian-Connector)** | ❌ **Verboten** | Darf nicht angebunden / verbunden werden. |
| Confluence via Custom MCP | ⚠️ Bedingt | |

 


## 5. Onboarding for non Engineers

Das Onboarding besteht aus 2 Teilen: Compliance Schulung & inhaltliche Onboarding. Wenn alle 2 erledigt sind & das Budget erfolgreich beantragt wurde lädt der:die Admin den:die Nutzer:in zu Claude ein.

### Onboarding:

Schritt 1: Compliance Schulung durchlaufen und Test bestehen:

→ Wird aktuell noch erstellt 

Schritt 2: Disziplin- bzw. projektspezifisches Onboarding durchlaufen und bei der für dich verantwortlichen Person eine Lizenz anfragen.

## 6. Regelmäßige Aktualisierung

Diese Regeln werden JÄHRLICH/HALBJÄHRLICH aktualisiert. Dafür wird ein Threat Modeling Workshop durchgeführt und auf Basis der Ergebnisse die Guidelines ggf. angepasst. 

Der Erste soll im September 2026 stattfinden, um die Guidelines aufzusetzen. 



## 7. Technisches Set-Up

Sämtliche Sicherheitseinstellungen bezüglich der Freigabe von Inhalten (z. B. Teilen von Chats, Prompts oder Artefacts) werden zentral durch die IT-Administration für den gesamten Organisation-Account gesteuert.

**Dokumentation der IT-Konfiguration:** Eine detaillierte Übersicht aller aktuell eingestellten Sicherheits- und Teilen-Optionen im Claude-Account findest du in der IT-Dokumentation.

**Änderungsanfragen:** Sollte eine Einstellung deine Arbeit blockieren oder angepasst werden müssen, damit du eine bestimmte Aufgabe durchführen kannst, darf diese Änderung **ausschließlich in Abstimmung mit Legal** und **Durchführung durch die IT** erfolgen.

 
