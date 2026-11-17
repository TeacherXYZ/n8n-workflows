# Facilitator guide – "Getting started" (60 min)

Principle: **max. 10 minutes of talking, 50 minutes of doing.** Everyone has a running agent before the hour is over.

## Before the session (15 min)

- [ ] Write the link on the board: **github.com/TeacherXYZ/n8n-workflows**
- [ ] Repo must be **public** (otherwise learners can't open it without a GitHub login).
- [ ] Decide how learners get AI access (see [Connecting an AI model](../../docs/connect-an-ai-model.md)):
  - n8n Cloud trial → free OpenAI credits (test once yourself!), **or**
  - one class API key with a low spending limit (delete it afterwards).
- [ ] Test workflow 02 yourself in a learner account: import → credential → chat. (5 min)
- [ ] Check: do all learners have a working n8n login? Those without one pair up with someone who has.
- [ ] Mixed pairs: 1 Danish + 1 German learner per laptop. One types, one navigates – switch after each step.

## Run sheet

| Min | Facilitator | Learners |
|---|---|---|
| 0–3 | "Today we build. In 60 minutes, every pair talks to their own AI tutor." Form pairs. | Open link, open n8n |
| 3–10 | Slides 1–8: n8n in one picture, what is an agent, what is a *learning* agent. | Listen, 1 question to the neighbour |
| 10–25 | **Step 1** – Show import + "Execute workflow" once on the projector (2 min), then let go. | Import 01, run, change cities |
| 25–45 | **Step 2** – Show credential + "Open chat" once (3 min). Walk around, fix credentials. | Import 02, connect model, chat, test the "homework" question |
| 45–55 | **Step 3** – "Change the system message. Then swap laptops." | Design own tutor, test another pair's tutor |
| 55–60 | 2–3 pairs show their tutor for 1 min each. Collect on the board: *What makes a learning agent helpful?* | Share |

Fast pairs: Bonus workflow 03 (tools). Slow pairs: skip Step 1 changes, go to Step 2 directly – the agent is the goal.

## The bridge to the joint project

The board list from the last 5 minutes ("What makes a learning agent helpful?") is the first requirements list for the Danish–German learning agent. Take a photo. Possible follow-ups:

- Which subject / which learners should the joint agent serve?
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
