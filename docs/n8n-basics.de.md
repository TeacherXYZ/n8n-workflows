[English](n8n-basics.md) | **Deutsch**

# n8n-Grundlagen

**n8n** (gesprochen „n-eight-n“, kurz für „nodemation“) ist ein Werkzeug, mit dem man Automatisierungen und KI-Agenten baut, indem man Bausteine auf einer Arbeitsfläche verbindet – ganz ohne oder mit sehr wenig Programmieren.

## Wörter, die du brauchst

| Wort | Bedeutung |
|---|---|
| **Workflow** | Deine ganze Automatisierung – alles auf einer Arbeitsfläche. |
| **Node** | Ein Baustein = ein Schritt. Z. B. „Wetterdaten holen“, „E-Mail senden“, „KI fragen“. |
| **Trigger** | Der erste Node. Entscheidet, **wann** der Workflow startet: per Klick, nach Zeitplan, wenn eine Chat-Nachricht kommt, wenn ein Formular abgeschickt wird … |
| **Verbindung** | Die Linie zwischen Nodes. Daten fließen darauf von links nach rechts. |
| **Item** | Ein Datenpaket, z. B. eine Stadt mit ihrer Temperatur. Ein Node läuft meist einmal pro Item. |
| **Execution** (Ausführung) | Ein Durchlauf des Workflows. Alle bisherigen Durchläufe findest du unter **Executions**. |
| **Credential** (Zugang) | Gespeicherter Login/API-Key für einen externen Dienst (z. B. ein KI-Modell). Sicher in n8n abgelegt, **nicht** in der Workflow-Datei. |
| **Expression** (Ausdruck) | Eine kleine Formel in einem Feld, geschrieben `{{ ... }}`. Z. B. `{{ $json.city }}` = „nimm das Feld *city* aus den ankommenden Daten“. |

## Die Arbeitsfläche

- **Execute workflow** (unten): Workflow jetzt ausführen.
- **Doppelklick** auf einen Node: öffnen. Links = INPUT, Mitte = Einstellungen, rechts = OUTPUT.
- **+** rechts an einem Node: nächsten Node hinzufügen.
- **Open chat** (unten): nur sichtbar, wenn der Workflow mit einem Chat-Trigger beginnt.
- Workflows speichern automatisch; schau in die obere Leiste.

## Erste Schritte – Checkliste

- [ ] Einen Workflow importieren und ausführen
- [ ] Einen Node öffnen und INPUT und OUTPUT finden
- [ ] Einen Wert ändern und nochmal ausführen
- [ ] Mit **+** einen neuen Node hinzufügen
- [ ] Eine Expression `{{ $json.etwas }}` benutzen
- [ ] Einen alten Durchlauf unter **Executions** ansehen

## Nützliche Links

- n8n-Doku (Englisch): <https://docs.n8n.io>
- Kurse (Text + Video): <https://docs.n8n.io/courses/>
- Workflow-Vorlagen aus der Community: <https://n8n.io/workflows/>
