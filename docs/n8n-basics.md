# n8n basics

**n8n** (say "n-eight-n", short for "nodemation") is a tool to build automations and AI agents by connecting blocks on a canvas – no or very little programming needed.

## Words you need

| Word | Meaning |
|---|---|
| **Workflow** | Your whole automation – everything on one canvas. |
| **Node** | One block = one step. E.g. "get weather data", "send an email", "ask the AI". |
| **Trigger** | The first node. Decides **when** the workflow starts: by click, on a schedule, when a chat message arrives, when a form is sent… |
| **Connection** | The line between nodes. Data flows along it from left to right. |
| **Item** | One piece of data, e.g. one city with its temperature. A node usually runs once per item. |
| **Execution** | One run of the workflow. You can look at every past run under **Executions**. |
| **Credential** | Saved login/API key for an external service (e.g. an AI model). Stored safely in n8n, **not** in the workflow file. |
| **Expression** | A small formula inside a field, written `{{ ... }}`. E.g. `{{ $json.city }}` = "take the field *city* from the incoming data". |

## The canvas

- **Execute workflow** (bottom): run the workflow now.
- **Double-click** a node: open it. Left = INPUT, middle = settings, right = OUTPUT.
- **+** on the right side of a node: add the next node.
- **Open chat** (bottom): only visible if the workflow starts with a chat trigger.
- Workflows auto-save; check the top bar.

## First steps – checklist

- [ ] Import a workflow and run it
- [ ] Open a node and find INPUT and OUTPUT
- [ ] Change a value and run again
- [ ] Add a new node with **+**
- [ ] Use an expression `{{ $json.something }}`
- [ ] Look at an old run under **Executions**

## Useful links

- n8n docs: <https://docs.n8n.io>
- Courses (text + video): <https://docs.n8n.io/courses/>
- Workflow templates from the community: <https://n8n.io/workflows/>
