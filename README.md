# n8n-workflows

Sammlung meiner n8n-Workflows mit Dokumentation.

## Struktur

| Ordner | Inhalt |
|---|---|
| `workflows/` | Exportierte Workflow-JSONs, gerne in Unterordnern nach Thema |
| `docs/` | Beschreibung pro Workflow: Zweck, Trigger, Abhängigkeiten |
| `credentials/` | Nur Hinweise/Vorlagen – **keine echten Secrets** |

## Workflow hinzufügen

1. In n8n: Workflow öffnen → `…` → **Download** (JSON-Export)
2. Datei unter `workflows/<thema>/<name>.json` ablegen
3. Vor dem Commit prüfen: keine API-Keys, Tokens oder privaten Webhook-URLs im JSON
4. Kurze Doku unter `docs/<name>.md` ergänzen

## Hinweis zu Secrets

n8n-Exporte enthalten nur Credential-*IDs*, nicht die Zugangsdaten selbst.
Werte, die direkt in Nodes eingetragen sind (z. B. Header mit API-Key, HTTP-URLs mit Token), landen aber im Export – diese vorher entfernen.
