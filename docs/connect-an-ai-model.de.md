[English](connect-an-ai-model.md) | **Deutsch**

# Ein KI-Modell anbinden

Die Agenten-Workflows (02 und 03) brauchen Zugang zu einem Sprachmodell. n8n spricht mit dem Modell über einen **API-Key**, der als **Credential** gespeichert wird.

> Die Workflow-Dateien in diesem Repo enthalten **niemals Keys**. Nach dem Import wählt oder erstellt jede lernende Person das Credential in ihrem eigenen n8n.

## Welche Variante?

| Variante | Aufwand | Gut für |
|---|---|---|
| **A. Gratis-Guthaben in n8n Cloud** | am geringsten | Du nutzt n8n Cloud (Testphase). |
| **B. Klassen-Key von der Lehrkraft** | gering | Die ganze Gruppe, kurze Session. |
| **C. Eigener kostenloser Key** | 5–10 Min. | Weiterarbeiten nach dem Workshop. |
| **D. Claude (Anthropic)** | gering, kostenpflichtig | Du oder deine Schule habt ein Anthropic-API-Konto. |

### A. n8n Cloud: Gratis-Guthaben für OpenAI

In n8n Cloud bietet der Dialog für das OpenAI-Credential neuen Konten eventuell **kostenloses OpenAI-API-Guthaben** an.
Doppelklick auf **KI-Modell** → **Credential to connect with** → **Create new credential** → nach dem Gratis-Angebot schauen und annehmen.

### B. Klassen-Key von der Lehrkraft

1. Doppelklick auf **KI-Modell** → **Credential to connect with** → **Create new credential**.
2. Den API-Key einfügen, den dir deine Lehrkraft gibt → **Save**.
3. Der Node sollte von rot auf normal wechseln.

### C. Eigener kostenloser Key

Einige Anbieter haben ein kostenloses Kontingent (Regeln und Limits ändern sich – auf der Seite des Anbieters nachsehen):

- **Mistral AI** (Europa): <https://console.mistral.ai> → API keys
- **Google Gemini**: <https://aistudio.google.com> → Get API key (Altersgrenzen beachten)
- **Groq**: <https://console.groq.com> → API keys

Dann [den Modell-Node austauschen](#modell-node-austauschen).

### D. Claude (Anthropic)

1. Auf <https://platform.claude.com> anmelden (eigener Login, unabhängig von claude.ai).
2. **Billing**: Guthaben aufladen – ohne läuft die API nicht, auch nicht mit einem claude.ai-Abo.
3. **API Keys** → **Create Key**. Sofort kopieren; der Key wird nur einmal angezeigt.
4. [Den Modell-Node austauschen](#modell-node-austauschen) und **Anthropic Chat Model** wählen.
5. **Model**: aus der Liste wählen oder auf **By ID** umstellen und die ID eintippen:

| Modell | ID | Preis pro 1 Mio. Tokens (rein / raus) |
|---|---|---|
| Claude Opus 5.5 | `claude-opus-5-5` | 4 $ / 20 $ |
| Claude Sonnet 5.5 | `claude-sonnet-5-5` | 2 $ / 10 $ |
| Claude Haiku 5.5 | `claude-haiku-5-5` | 0,10 $ / 0,50 $ |

Kommt eine Fehlermeldung zu **temperature**, **top_p** oder **thinking**: Im Anthropic-Node **Options** öffnen und diese Einstellungen entfernen – aktuelle Claude-Modelle akzeptieren sie nicht.

## Modell-Node austauschen

1. Den Node **KI-Modell** löschen.
2. Am Node **Lernagent** auf das **+** unter **Chat Model** klicken.
3. Anbieter wählen (z. B. *Anthropic Chat Model*, *Mistral Cloud Chat Model*, *Google Gemini Chat Model*, *Groq Chat Model*).
4. Das Credential mit deinem Key anlegen und ein Modell aus der Liste wählen.

## Sicherheitsregeln für API-Keys

- Ein API-Key ist wie ein Passwort **und** eine Kreditkarte: Wer ihn hat, kann ihn nutzen – und du zahlst womöglich.
- Einen Key nie in ein Workflow-Feld, einen Screenshot, einen Chat oder ein Git-Repo schreiben. Nur in den **Credential**-Dialog.
- Lehrkräfte: Für einen Klassen-Key beim Anbieter ein **niedriges Ausgabelimit** setzen und den Key nach der Session **löschen**.
