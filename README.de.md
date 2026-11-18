[English](README.md) | **Deutsch**

# n8n-Workflows – Bauen statt nur zuhören

Workflows zum direkten Importieren in n8n, kurze Erklärungen und Folien für Lernende.
Kein Vorwissen nötig.

> **Hier starten:** [Erste Schritte mit n8n](workshop/getting-started/README.de.md)

## Was du hier findest

| Ordner | Inhalt |
|---|---|
| [`workshop/getting-started/`](workshop/getting-started/README.de.md) | Praxis: von „Was ist n8n?“ bis zum eigenen Lernagenten |
| [`workflows/`](workflows/README.de.md) | Workflow-Dateien (`.json`) zum Importieren in n8n – [deutsche Versionen](workflows/getting-started/de/) |
| [`docs/`](docs/) | Kurze Hintergrundtexte: [Was ist ein KI-Agent?](docs/what-is-an-agent.de.md) · [n8n-Grundlagen](docs/n8n-basics.de.md) · [Ein KI-Modell anbinden](docs/connect-an-ai-model.de.md) |
| [`slides/`](slides/) | Präsentation ([PDF Deutsch](slides/getting-started.de.pdf) · [PDF English](slides/getting-started.pdf)) |
| [`credentials/`](credentials/README.de.md) | Hinweise, welche Zugänge/Keys ein Workflow braucht – **niemals echte Zugangsdaten** |

## So lädst du einen Workflow in n8n

**Variante A – Kopieren & Einfügen (funktioniert überall)**
1. Öffne die Workflow-Datei auf GitHub (z. B. [`01-hallo-n8n.json`](workflows/getting-started/de/01-hallo-n8n.json)).
2. Klick auf den Button **Copy raw file** (oben rechts in der Dateiansicht).
3. Leg in n8n einen neuen, leeren Workflow an und drück auf der Arbeitsfläche **Strg+V** / **Cmd+V**.

**Variante B – Import über URL**
1. Leg in n8n einen neuen Workflow an, öffne das Menü **⋯** (oben rechts) → **Import from URL…**
2. Füge den *Raw*-Link der Datei ein, z. B.
   `https://raw.githubusercontent.com/TeacherXYZ/n8n-workflows/main/workflows/getting-started/de/01-hallo-n8n.json`

**Variante C – Herunterladen**: `.json`-Datei herunterladen, dann in n8n **⋯** → **Import from File…**

## Eigene Workflows beitragen

1. In n8n: Workflow öffnen → **⋯** → **Download**
2. Speichern als `workflows/<thema>/<name>.json`
3. Vor dem Commit prüfen: keine API-Keys, Tokens oder privaten Webhook-URLs im JSON.
   n8n-Exporte enthalten nur die *IDs* der Zugänge – Werte, die direkt in Nodes eingetragen sind (z. B. ein API-Key im HTTP-Header), werden aber mit exportiert.
4. Eine kurze Beschreibung in `docs/` oder als README neben dem Workflow ergänzen.
