# Getting started: your first hour with n8n

**Goal:** In 60 minutes you build and talk to your own **learning agent**: an AI tutor that helps you learn instead of just giving answers.

**You need:** a laptop, a browser, access to n8n (n8n Cloud or your school's n8n). Work in **pairs**, ideally one Danish and one German learner per pair.

**Prior knowledge:** none.

---

## The plan

| Time | What | File |
|---|---|---|
| 0–10 min | Short intro: what is n8n, what is an agent? | [slides](../../slides/getting-started.pdf) |
| 10–25 min | **Step 1:** Your first workflow (weather in Kassel & Copenhagen) | [`01-hello-n8n.json`](../../workflows/getting-started/01-hello-n8n.json) |
| 25–45 min | **Step 2:** Your first learning agent (chat with an AI tutor) | [`02-learning-agent.json`](../../workflows/getting-started/02-learning-agent.json) |
| 45–55 min | **Step 3:** Make it yours: subject, rules, personality. Test it on another pair. | – |
| 55–60 min | Show & tell: what worked, what would a *good* learning agent need? | – |
| Bonus | Give your agent tools (Wikipedia, calculator) | [`03-learning-agent-with-tools.json`](../../workflows/getting-started/03-learning-agent-with-tools.json) |

---

## Step 1 – Hello n8n (15 min)

**What you learn:** what a *workflow*, a *node*, a *trigger* and *data* are.

1. Open n8n and create a new, empty workflow (**+** / **Create workflow**).
2. Load [`01-hello-n8n.json`](../../workflows/getting-started/01-hello-n8n.json) (see [how to import](../../README.md#how-to-load-a-workflow-into-n8n): **Copy raw file** → **Ctrl+V** on the canvas).
3. Click **Execute workflow** (in newer n8n versions just **Execute**, bottom of the canvas).
4. Double-click each node, one after the other. Look at **INPUT** (left) and **OUTPUT** (right).
   - What does the node *Get weather* receive? What does it give back?
5. **Your turn:**
   - Change the cities in **Our cities**: your home town, your partner's home town. (Find latitude/longitude by searching the city name + "coordinates".)
   - Run it again. Which city is warmer right now?

> **Key idea:** A workflow is a chain of small steps (nodes). Each node gets data, does one thing, and passes data on. The **trigger** decides *when* the workflow starts.

---

## Step 2 – Your first learning agent (20 min)

**What you learn:** what an AI *agent* is and what its parts do.

1. Create a new workflow and load [`02-learning-agent.json`](../../workflows/getting-started/02-learning-agent.json).
2. The node **AI model** shows a warning: it needs a connection (a "credential") to an AI model.
   Double-click it → **Credential** → create a new one. Your teacher tells you which one to use.
   Details: [Connecting an AI model](../../docs/connect-an-ai-model.md).
3. Click **Open chat** (bottom of the canvas) and say hello. Ask it something you want to learn.
4. Watch what happens: the agent node lights up, calls the model, uses its memory.
5. **Test it:** Ask *"What is 17 × 23?"* or *"Write my homework about photosynthesis."*
   Does the agent give you the answer directly – or does it help you think?

**The parts of your agent:**

| Node | Role | Comparison |
|---|---|---|
| When chat message received | Trigger: starts when you type | the door bell |
| Learning Agent | Decides what to do, follows its instructions (system message) | the tutor |
| AI model | The language model that writes the text | the tutor's brain |
| Memory | Remembers the last messages of the conversation | the tutor's notebook |

---

## Step 3 – Make it yours (10 min)

Double-click **Learning Agent** → **Options** → **System Message**. This is the "job description" of your agent.

Change it. Ideas:

- **Subject:** English vocabulary, maths for grade 8, Danish for Germans, German for Danes, chemistry…
- **Rules:** "Never give the final answer. Ask one question at a time." / "Answer in the language the learner uses." / "After 3 questions, give a short quiz."
- **Personality:** a patient coach, a pirate, a strict examiner, Socrates…

Then **swap laptops with another pair** and let them test your agent for 3 minutes. Did it behave as you planned?

Collect your answers to: *What makes a learning agent actually helpful for learning?* This is the starting point for the joint Danish–German learning agent project.

---

## Bonus – Give your agent tools

Load [`03-learning-agent-with-tools.json`](../../workflows/getting-started/03-learning-agent-with-tools.json). This agent can look things up on **Wikipedia** and use a **calculator**.

Ask it something it needs to look up. Then open the agent's execution log: when did it decide to use a tool – and why?

> **Key idea:** A chatbot only talks. An **agent** can *decide* to take actions (use tools) to reach a goal.

---

## Stuck?

| Problem | Fix |
|---|---|
| Pasting does nothing | Click once on the empty canvas first, then Ctrl+V / Cmd+V. Or use **⋯ → Import from URL**. |
| Red warning on *AI model* | No credential selected yet. See [Connecting an AI model](../../docs/connect-an-ai-model.md). |
| "Insufficient quota" / 401 / 429 | The API key has no credit or is wrong. Ask your teacher. |
| The chat button is missing | The workflow needs a *When chat message received* node. Use workflow 02. |
| Nothing works | Ask the pair next to you first, then the teacher. |

More background: [What is an AI agent?](../../docs/what-is-an-agent.md) · [n8n basics](../../docs/n8n-basics.md)
