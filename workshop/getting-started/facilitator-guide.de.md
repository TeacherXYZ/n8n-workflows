[English](facilitator-guide.md) | **Deutsch**

# Hinweise für die Moderation – „Erste Schritte“

Bausteine und praktische Hinweise. Zeit, Gruppen und Reihenfolge legst du selbst fest – passend zur Situation.

## Vor der Session

- [ ] Link weitergeben: **github.com/TeacherXYZ/n8n-workflows**
- [ ] Das Repo muss **öffentlich** sein (sonst können Lernende es ohne GitHub-Login nicht öffnen).
- [ ] Entscheiden, wie die Lernenden Zugang zur KI bekommen (siehe [Ein KI-Modell anbinden](../../docs/connect-an-ai-model.de.md)).
- [ ] Workflow 02 selbst mit einem Lernenden-Zugang testen: Import → Credential → Chat.
- [ ] Prüfen, ob sich die Lernenden bei n8n anmelden können.

## Bausteine

| Baustein | Inhalt | Material |
|---|---|---|
| Einstieg | Was ist n8n? Was ist ein Agent? Warum ein *Lern*agent? | [Folien](../../slides/getting-started.de.pdf), [Doku](../../docs/) |
| Schritt 1 | Erster Workflow ohne KI: Trigger, Nodes, Datenfluss | [`01-hallo-n8n.json`](../../workflows/getting-started/de/01-hallo-n8n.json) |
| Schritt 2 | Erster Lernagent: Modell anbinden, chatten, die „Hausaufgaben“-Frage testen | [`02-lernagent.json`](../../workflows/getting-started/de/02-lernagent.json) |
| Schritt 3 | System Message ändern: Fach, Regeln, Persönlichkeit; von anderen testen lassen | – |
| Bonus | Agent mit Werkzeugen (Wikipedia, Taschenrechner) | [`03-lernagent-mit-werkzeugen.json`](../../workflows/getting-started/de/03-lernagent-mit-werkzeugen.json) |
| Reflexion | *Was macht einen Lernagenten wirklich hilfreich?* | – |

Alle Workflows gibt es auch auf Englisch in [`workflows/getting-started/`](../../workflows/getting-started/).
Schritt 1 kann entfallen, wenn der Fokus auf dem Agenten liegt. Schritt 2 und 3 funktionieren auch für sich.

## Die Brücke zum gemeinsamen Projekt

Die Antworten auf *„Was macht einen Lernagenten wirklich hilfreich?“* können als erste Anforderungsliste für einen gemeinsamen Lernagenten dienen. Mögliche Anschlussfragen:

- Für welches Fach / welche Lernenden soll der Agent da sein?
- Welche Regeln soll er befolgen (Sprache, Tipps statt Antworten, Niveau)?
- Welche Werkzeuge bräuchte er (Kursmaterial, Quiz-Generator, Vokabelliste …)?

## Häufige Probleme

| Symptom | Ursache / Lösung |
|---|---|
| Einfügen tut nichts | Erst in die leere Arbeitsfläche klicken. Oder **⋯ → Import from URL** mit dem Raw-Link. |
| GitHub verlangt Login / 404 | Das Repo ist noch privat. |
| `401` / `Incorrect API key` | Key falsch eingegeben oder gelöscht. |
| `429` / `insufficient_quota` | Kein Guthaben auf dem Key oder zu viele Anfragen gleichzeitig – 30 Sekunden warten, nochmal versuchen. |
| `model not found` | Node *KI-Modell* öffnen und ein anderes Modell aus der Liste wählen. |
| Chat antwortet in der falschen Sprache | In der System Message ergänzen: „Antworte immer in der Sprache, in der die lernende Person schreibt.“ |
