[English](what-is-an-agent.md) | **Deutsch**

# Was ist ein KI-Agent?

## Drei Stufen

| | Was es tut | Beispiel |
|---|---|---|
| **Sprachmodell (LLM)** | Sagt Text voraus. Text rein, Text raus. Kein Gedächtnis, keine Werkzeuge, kein Ziel. | GPT, Claude, Gemini, Mistral |
| **Chatbot** | Ein Sprachmodell + ein Gespräch. Unterhält sich mit dir. | Eine einfache Chat-Website |
| **Agent** | Ein Sprachmodell + **Anweisungen** + **Gedächtnis** + **Werkzeuge**. Er *entscheidet*, welche Schritte er geht, um ein Ziel zu erreichen – z. B. „Das muss ich erst nachschlagen“, dann nutzt er ein Werkzeug, liest das Ergebnis und antwortet. | Ein Tutor, der erst in Wikipedia nachschaut, dann erklärt und dich anschließend abfragt |

## Die vier Teile eines Agenten

```
                ┌────────────────────────────┐
  Du   ───────▶ │  AGENT                     │ ───────▶  Antwort
 (Nachricht)    │  - Anweisungen (Rolle)     │
                │  - Modell (das „Gehirn“)   │
                │  - Gedächtnis (Notizbuch)  │
                │  - Werkzeuge (Hände)       │
                └──────────┬─────────────────┘
                           │ entscheidet sich für
                ┌──────────▼─────────────────┐
                │  WERKZEUGE                 │
                │  Wikipedia, Taschenrechner,│
                │  E-Mail, Datenbank, …      │
                └────────────────────────────┘
```

1. **Anweisungen (System Message):** Wer bin ich? Was ist meine Aufgabe? Welche Regeln gelten?
   *„Du bist ein geduldiger Mathe-Tutor. Gib nie die fertige Lösung.“*
2. **Modell:** Das Sprachmodell, das Text versteht und schreibt.
3. **Gedächtnis:** Hält den bisherigen Gesprächsverlauf fest, damit der Agent weiß, was du vor drei Nachrichten gesagt hast.
4. **Werkzeuge:** Aktionen, die der Agent ausführen kann: suchen, rechnen, eine Nachricht senden, eine Datei lesen …

## Die Agenten-Schleife

1. Nachricht und Anweisungen lesen.
2. Überlegen: *Kann ich direkt antworten, oder brauche ich ein Werkzeug?*
3. Wenn ein Werkzeug nötig ist → benutzen → Ergebnis lesen → zurück zu 2.
4. Antworten.

In n8n kannst du diese Schleife beobachten: Öffne eine Ausführung des Agenten und schau dir das Protokoll des **AI Agent**-Nodes an.

## Warum ein *Lern*agent?

Ein normaler KI-Assistent ist dafür gebaut, **Antworten zu geben**. Das ist super, um Arbeit zu erledigen – aber schlecht fürs Lernen: Wenn die KI das Denken übernimmt, lernst du nichts.

Ein Lernagent ist dafür gebaut, **dich zum Denken zu bringen**:

- stellt Fragen, statt Lösungen zu liefern (sokratische Methode),
- gibt Schritt für Schritt Hinweise,
- prüft, was du schon weißt,
- passt sich deinem Niveau und deiner Sprache an,
- macht Fehler sichtbar – und okay.

Ob sich ein Agent so verhält, entscheiden fast ausschließlich seine **Anweisungen**. Genau die gestaltest du im Workshop.

## Grenzen – bleib kritisch

- Sprachmodelle können **überzeugt klingen und trotzdem falsch liegen** („Halluzination“). Wichtige Fakten prüfen.
- Keine **persönlichen Daten** (Namen, Noten, Gesundheit, Adressen) in KI-Werkzeuge eingeben.
- Der Agent weiß nur, was in seinem Modell, seinem Gedächtnis und seinen Werkzeugen steckt.
