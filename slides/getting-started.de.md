---
marp: true
theme: default
paginate: true
size: 16:9
style: |
  section { font-family: "Helvetica Neue", Arial, sans-serif; font-size: 28px; padding: 60px 70px; }
  h1 { color: #1f2937; }
  h2 { color: #ea4b71; }
  section.lead { text-align: center; justify-content: center; }
  section.lead h1 { font-size: 64px; }
  code { background: #f3f4f6; }
  table { font-size: 24px; }
  .big { font-size: 40px; font-weight: bold; }
---


<!-- _class: lead -->

# Bauen statt nur zuhören

## Erste Schritte mit n8n

**github.com/TeacherXYZ/n8n-workflows**

---

# Das Ziel

<p class="big">Baue deinen eigenen KI-Lernagenten<br>und unterhalte dich mit ihm.</p>

---

# Was ist n8n?

Ein Werkzeug, mit dem man **Bausteine verbindet** – zu Automatisierungen und KI-Agenten, auf einer Arbeitsfläche, ohne Programmieren.

| Wort | Bedeutung |
|---|---|
| **Workflow** | die ganze Automatisierung |
| **Node** | ein Baustein = ein Schritt |
| **Trigger** | der erste Node: *wann* geht es los? |
| **Verbindung** | Daten fließen von links nach rechts |

---

# Ein Workflow in einem Bild

```
 [ Klick ]  ──▶  [ Unsere Städte ]  ──▶  [ Wetter abrufen ]  ──▶  [ Schöne Antwort ]
  Trigger          Daten                  Internet fragen          Ergebnis vorbereiten
```

Das ist **Schritt 1**: das Wetter in Kassel und Kopenhagen.

---

# Chatbot oder Agent?

| | |
|---|---|
| **Sprachmodell** | Text rein → Text raus. Kein Gedächtnis, keine Werkzeuge. |
| **Chatbot** | Modell + Gespräch |
| **Agent** | Modell + **Anweisungen** + **Gedächtnis** + **Werkzeuge** → *entscheidet*, welche Schritte er geht |

---

# Die vier Teile eines Agenten

| Teil | In n8n | Vergleich |
|---|---|---|
| Anweisungen | *System Message* | die Stellenbeschreibung |
| Modell | Node *KI-Modell* | das Gehirn |
| Gedächtnis | Node *Gedächtnis* | das Notizbuch |
| Werkzeuge | Wikipedia, Taschenrechner, … | die Hände |

---

# Warum ein *Lern*agent?

Normale KI: **gibt Antworten** → sie übernimmt das Denken.

Lernagent: **bringt dich zum Denken**
- stellt Fragen, statt Lösungen zu liefern
- gibt Schritt für Schritt Hinweise
- passt sich deinem Niveau und deiner Sprache an

Ob er das tut, hängt von **seinen Anweisungen** ab. Die schreibst du.

---

# Die Schritte

| | |
|---|---|
| **Schritt 1** | erster Workflow: Wetter |
| **Schritt 2** | erster Lernagent: mit ihm chatten |
| **Schritt 3** | mach ihn zu deinem, lass andere testen |
| **Bonus** | gib deinem Agenten Werkzeuge |

Alles steht im Repo: **workshop/getting-started**

---

# So importierst du einen Workflow

1. Die `.json`-Datei auf GitHub öffnen
2. Auf **Copy raw file** klicken (Symbol oben rechts)
3. In n8n: neuer leerer Workflow → auf die Arbeitsfläche klicken → **Strg+V / Cmd+V**
4. Auf **Execute workflow** (oder **Execute**) klicken

---

# Bleib kritisch

- KI kann **überzeugt klingen und trotzdem falsch liegen** – Fakten prüfen
- **Keine persönlichen Daten** in KI-Werkzeuge (Namen, Noten, Adressen)
- Ein **API-Key** ist wie ein Passwort und eine Kreditkarte – nie weitergeben, nie in ein Workflow-Feld schreiben

---

<!-- _class: lead -->

# Los geht's.

**github.com/TeacherXYZ/n8n-workflows**
→ workshop/getting-started

Am Ende: *Was macht einen Lernagenten wirklich hilfreich?*
