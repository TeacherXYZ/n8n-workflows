[English](README.md) | **Deutsch**

# Erste Schritte mit n8n

**Ziel:** Du baust deinen eigenen **Lernagenten** und unterhältst dich mit ihm – einen KI-Tutor, der dir beim Lernen hilft, statt dir einfach Antworten zu geben.

**Du brauchst:** einen Laptop, einen Browser, Zugang zu n8n.

**Vorwissen:** keins.

---

## Die Schritte

| | Was | Datei |
|---|---|---|
| Einstieg | Was ist n8n, was ist ein Agent? | [Folien](../../slides/getting-started.de.pdf) |
| 1 | **Schritt 1:** Dein erster Workflow (Wetter in Kassel & Kopenhagen) | [`01-hallo-n8n.json`](../../workflows/getting-started/de/01-hallo-n8n.json) |
| 2 | **Schritt 2:** Dein erster Lernagent (Chat mit einem KI-Tutor) | [`02-lernagent.json`](../../workflows/getting-started/de/02-lernagent.json) |
| 3 | **Schritt 3:** Mach ihn zu deinem: Fach, Regeln, Persönlichkeit. Lass andere testen. | – |
| Bonus | Gib deinem Agenten Werkzeuge (Wikipedia, Taschenrechner) | [`03-lernagent-mit-werkzeugen.json`](../../workflows/getting-started/de/03-lernagent-mit-werkzeugen.json) |

> Die Workflows gibt es auch auf Englisch: [`workflows/getting-started/`](../../workflows/getting-started/).

---

## Schritt 1 – Hallo n8n

**Was du lernst:** was ein *Workflow*, ein *Node*, ein *Trigger* und *Daten* sind.

1. Öffne n8n und leg einen neuen, leeren Workflow an (**+** / **Create workflow**).
2. Lade [`01-hallo-n8n.json`](../../workflows/getting-started/de/01-hallo-n8n.json) (siehe [Import](../../README.de.md#so-lädst-du-einen-workflow-in-n8n): **Copy raw file** → **Strg+V** auf der Arbeitsfläche).
3. Klick auf **Execute workflow** (in neueren n8n-Versionen nur **Execute**, unten auf der Arbeitsfläche).
4. Öffne jeden Node mit Doppelklick, einen nach dem anderen. Schau dir **INPUT** (links) und **OUTPUT** (rechts) an.
   - Was bekommt der Node *Wetter abrufen*? Was gibt er zurück?
5. **Du bist dran:**
   - Ändere die Städte in **Unsere Städte**, z. B. deinen Heimatort.
   - Führ den Workflow nochmal aus. Welche Stadt ist gerade wärmer?

> **Kernidee:** Ein Workflow ist eine Kette kleiner Schritte (Nodes). Jeder Node bekommt Daten, macht eine Sache und gibt Daten weiter. Der **Trigger** entscheidet, *wann* der Workflow startet.

---

## Schritt 2 – Dein erster Lernagent

**Was du lernst:** was ein KI-*Agent* ist und was seine Teile tun.

1. Leg einen neuen Workflow an und lade [`02-lernagent.json`](../../workflows/getting-started/de/02-lernagent.json).
2. Der Node **KI-Modell** zeigt eine Warnung: Er braucht eine Verbindung (ein „Credential“) zu einem KI-Modell.
   Doppelklick → **Credential** → neues anlegen. Welches, sagt dir deine Lehrkraft.
   Details: [Ein KI-Modell anbinden](../../docs/connect-an-ai-model.de.md).
3. Klick auf **Open chat** (unten auf der Arbeitsfläche) und sag Hallo. Frag ihn etwas, das du lernen willst.
4. Beobachte, was passiert: Der Agent-Node leuchtet auf, ruft das Modell auf, nutzt sein Gedächtnis.
5. **Teste ihn:** Frag *„Was ist 17 × 23?“* oder *„Schreib meine Hausaufgabe über Photosynthese.“*
   Gibt dir der Agent direkt die Antwort – oder hilft er dir beim Denken?

**Die Teile deines Agenten:**

| Node | Rolle | Vergleich |
|---|---|---|
| When chat message received | Trigger: startet, wenn du tippst | die Türklingel |
| Lernagent | Entscheidet, was zu tun ist, folgt seinen Anweisungen (System Message) | der Tutor |
| KI-Modell | Das Sprachmodell, das den Text schreibt | das Gehirn des Tutors |
| Gedächtnis | Merkt sich die letzten Nachrichten des Gesprächs | das Notizbuch des Tutors |

---

## Schritt 3 – Mach ihn zu deinem

Doppelklick auf **Lernagent** → **Options** → **System Message**. Das ist die „Stellenbeschreibung“ deines Agenten.

Ändere sie. Ideen:

- **Fach:** Englisch-Vokabeln, Mathe Klasse 8, Dänisch für Deutsche, Deutsch für Dänen, Chemie …
- **Regeln:** „Gib nie die fertige Lösung. Stell immer nur eine Frage.“ / „Antworte in der Sprache, in der die lernende Person schreibt.“ / „Nach 3 Fragen gibt es ein kurzes Quiz.“
- **Persönlichkeit:** ein geduldiger Coach, ein Pirat, eine strenge Prüferin, Sokrates …

Dann lass jemand anderen deinen Agenten testen. Hat er sich so verhalten, wie du es geplant hast?

Sammelt eure Antworten auf: *Was macht einen Lernagenten wirklich hilfreich fürs Lernen?* Das ist der Ausgangspunkt für das gemeinsame dänisch-deutsche Lernagenten-Projekt.

---

## Bonus – Gib deinem Agenten Werkzeuge

Lade [`03-lernagent-mit-werkzeugen.json`](../../workflows/getting-started/de/03-lernagent-mit-werkzeugen.json). Dieser Agent kann in **Wikipedia** nachschlagen und einen **Taschenrechner** benutzen.

Frag ihn etwas, das er nachschlagen muss. Öffne dann das Ausführungsprotokoll des Agenten: Wann hat er sich entschieden, ein Werkzeug zu nutzen – und warum?

> **Kernidee:** Ein Chatbot redet nur. Ein **Agent** kann *entscheiden*, Aktionen auszuführen (Werkzeuge zu nutzen), um ein Ziel zu erreichen.

---

## Hängst du fest?

| Problem | Lösung |
|---|---|
| Einfügen tut nichts | Erst einmal auf die leere Arbeitsfläche klicken, dann Strg+V / Cmd+V. Oder **⋯ → Import from URL** nutzen. |
| Rote Warnung bei *KI-Modell* | Noch kein Credential ausgewählt. Siehe [Ein KI-Modell anbinden](../../docs/connect-an-ai-model.de.md). |
| „Insufficient quota“ / 401 / 429 | Der API-Key hat kein Guthaben oder ist falsch. Frag deine Lehrkraft. |
| Der Chat-Button fehlt | Der Workflow braucht einen Node *When chat message received*. Nimm Workflow 02. |
| Nichts funktioniert | Frag erst die Leute um dich herum, dann die Lehrkraft. |

Mehr Hintergrund: [Was ist ein KI-Agent?](../../docs/what-is-an-agent.de.md) · [n8n-Grundlagen](../../docs/n8n-basics.de.md)
