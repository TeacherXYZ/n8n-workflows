# n8n Workflows – Build, don't just listen

Ready-to-import n8n workflows, short explanations and slides for learners.
No prior knowledge needed.

> **Start here:** [Getting started – your first hour with n8n](workshop/getting-started/README.md)

## What you find here

| Folder | What's inside |
|---|---|
| [`workshop/getting-started/`](workshop/getting-started/README.md) | Hands-on session (60 min): from "What is n8n?" to your own learning agent |
| [`workflows/`](workflows/) | Workflow files (`.json`) you can import into n8n |
| [`docs/`](docs/) | Short background reads: [What is an AI agent?](docs/what-is-an-agent.md) · [n8n basics](docs/n8n-basics.md) · [Connecting an AI model](docs/connect-an-ai-model.md) |
| [`slides/`](slides/) | Presentation for the session ([PDF](slides/getting-started.pdf)) |
| [`credentials/`](credentials/) | Notes on which accounts/keys a workflow needs – **never real secrets** |

## How to load a workflow into n8n

**Option A – Copy & paste (works everywhere)**
1. Open the workflow file on GitHub (e.g. [`01-hello-n8n.json`](workflows/getting-started/01-hello-n8n.json)).
2. Click the **Copy raw file** button (top right of the file view).
3. In n8n, create a new, empty workflow and press **Ctrl+V** / **Cmd+V** on the canvas.

**Option B – Import from URL**
1. In n8n, create a new workflow, open the **⋯** menu (top right) → **Import from URL…**
2. Paste the *raw* link of the file, e.g.
   `https://raw.githubusercontent.com/TeacherXYZ/n8n-workflows/main/workflows/getting-started/01-hello-n8n.json`

**Option C – Download**: download the `.json` file, then in n8n **⋯** → **Import from File…**

## Contributing workflows

1. In n8n: open the workflow → **⋯** → **Download**
2. Save it as `workflows/<topic>/<name>.json`
3. Before committing, check the JSON for API keys, tokens or private webhook URLs.
   n8n exports only contain credential *IDs*, but values typed directly into nodes (e.g. an API key in an HTTP header) are exported too.
4. Add a short description in `docs/` or in a README next to the workflow.
