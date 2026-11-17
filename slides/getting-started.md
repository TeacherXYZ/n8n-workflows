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

# Build, don't just listen

## Your first hour with n8n

**github.com/TeacherXYZ/n8n-workflows**

---

# Today's goal

<p class="big">In 60 minutes, every pair talks to<br>their own AI learning agent.</p>

- Work in pairs: one Danish + one German learner per laptop
- One types, one navigates – switch after each step
- Stuck? Ask your neighbours first, then the teacher

---

# What is n8n?

A tool to **connect blocks** into automations and AI agents – on a canvas, without programming.

| Word | Meaning |
|---|---|
| **Workflow** | the whole automation |
| **Node** | one block = one step |
| **Trigger** | the first node: *when* does it start? |
| **Connection** | data flows from left to right |

---

# A workflow in one picture

```
 [ Click ]  ──▶  [ Our cities ]  ──▶  [ Get weather ]  ──▶  [ Nice answer ]
  trigger         data                ask the internet       prepare result
```

That's **Step 1**: weather in Kassel and Copenhagen.

---

# Chatbot vs. agent

| | |
|---|---|
| **Language model** | text in → text out. No memory, no tools. |
| **Chatbot** | model + conversation |
| **Agent** | model + **instructions** + **memory** + **tools** → *decides* which steps to take |

---

# The four parts of an agent

| Part | In n8n | Compare to |
|---|---|---|
| Instructions | *System message* | the job description |
| Model | *AI model* node | the brain |
| Memory | *Memory* node | the notebook |
| Tools | Wikipedia, calculator, … | the hands |

---

# Why a *learning* agent?

Normal AI: **gives answers** → it does the thinking.

Learning agent: **makes you think**
- asks questions instead of giving solutions
- gives hints step by step
- adapts to your level and your language

Whether it does this depends on **its instructions**. You write them.

---

# Your hour

| Min | |
|---|---|
| 10–25 | **Step 1** – first workflow: weather |
| 25–45 | **Step 2** – first learning agent: chat with it |
| 45–55 | **Step 3** – make it yours, swap laptops, test |
| 55–60 | Show & tell |

Everything is in the repo: **workshop/getting-started**

---

# How to import a workflow

1. Open the `.json` file on GitHub
2. Click **Copy raw file** (icon top right)
3. In n8n: new empty workflow → click the canvas → **Ctrl+V / Cmd+V**
4. Click **Execute workflow** (or **Execute**)

---

# Stay critical

- AI can **sound sure and still be wrong** – check facts
- **No personal data** in AI tools (names, grades, addresses)
- An **API key** is like a password and a credit card – never share it, never paste it into a workflow field

---

<!-- _class: lead -->

# Let's build.

**github.com/TeacherXYZ/n8n-workflows**
→ workshop/getting-started

At the end: *What makes a learning agent actually helpful?*
