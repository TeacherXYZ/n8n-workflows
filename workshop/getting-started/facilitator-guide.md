# Facilitator notes – "Getting started"

Building blocks and practical notes. Timing, grouping and order are up to you – adapt them to the situation.

## Before the session

- [ ] Share the link: **github.com/TeacherXYZ/n8n-workflows**
- [ ] Repo must be **public** (otherwise learners can't open it without a GitHub login).
- [ ] Decide how learners get AI access (see [Connecting an AI model](../../docs/connect-an-ai-model.md)).
- [ ] Test workflow 02 yourself in a learner account: import → credential → chat.
- [ ] Check that learners can log in to n8n.

## Building blocks

| Block | Content | Material |
|---|---|---|
| Intro | What is n8n? What is an agent? Why a *learning* agent? | [slides](../../slides/getting-started.pdf), [docs](../../docs/) |
| Step 1 | First workflow without AI: trigger, nodes, data flow | [`01-hello-n8n.json`](../../workflows/getting-started/01-hello-n8n.json) |
| Step 2 | First learning agent: connect a model, chat, test the "homework" question | [`02-learning-agent.json`](../../workflows/getting-started/02-learning-agent.json) |
| Step 3 | Change the system message: subject, rules, personality; let others test it | – |
| Bonus | Agent with tools (Wikipedia, calculator) | [`03-learning-agent-with-tools.json`](../../workflows/getting-started/03-learning-agent-with-tools.json) |
| Reflection | *What makes a learning agent actually helpful?* | – |

Step 1 can be skipped if the focus is on the agent. Steps 2 and 3 work on their own.

## The bridge to the joint project

The answers to *"What makes a learning agent actually helpful?"* can serve as a first requirements list for a joint learning agent. Possible follow-up questions:

- Which subject / which learners should the agent serve?
- Which rules should it follow (language, hints vs. answers, level)?
- Which tools would it need (course material, quiz generator, vocabulary list…)?

## Common issues

| Symptom | Cause / fix |
|---|---|
| Paste does nothing | Click into the empty canvas first. Or **⋯ → Import from URL** with the raw link. |
| GitHub asks for login / 404 | Repo is still private. |
| `401` / `Incorrect API key` | Key mistyped or deleted. |
| `429` / `insufficient_quota` | No credit on the key, or too many requests at once – wait 30 s, try again. |
| `model not found` | Open *AI model* node and pick another model from the list. |
| Chat answers in the wrong language | Add to the system message: "Always answer in the language the learner writes in." |
