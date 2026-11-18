**English** | [Deutsch](what-is-an-agent.de.md)

# What is an AI agent?

## Three levels

| | What it does | Example |
|---|---|---|
| **Language model (LLM)** | Predicts text. Gets text in, gives text out. Has no memory, no tools, no goal. | GPT, Claude, Gemini, Mistral |
| **Chatbot** | A language model + a conversation. Talks with you. | A simple chat website |
| **Agent** | A language model + **instructions** + **memory** + **tools**. It *decides* which steps to take to reach a goal – e.g. "I need to look this up first", then it uses a tool, reads the result, and answers. | A tutor that checks Wikipedia before explaining, then quizzes you |

## The four parts of an agent

```
                ┌────────────────────────────┐
  You  ───────▶ │  AGENT                     │ ───────▶  Answer
 (message)      │  - Instructions (role)     │
                │  - Model (the "brain")     │
                │  - Memory (the notebook)   │
                │  - Tools (hands)           │
                └──────────┬─────────────────┘
                           │ decides to use
                ┌──────────▼─────────────────┐
                │  TOOLS                     │
                │  Wikipedia, Calculator,    │
                │  Email, Database, …        │
                └────────────────────────────┘
```

1. **Instructions (system message):** Who am I? What is my job? What are my rules?
   *"You are a patient maths tutor. Never give the final answer."*
2. **Model:** The language model that understands and writes text.
3. **Memory:** Keeps the conversation so far, so the agent knows what you said 3 messages ago.
4. **Tools:** Actions the agent can take: search, calculate, send a message, read a file…

## The agent loop

1. Read the message and the instructions.
2. Think: *Can I answer directly, or do I need a tool?*
3. If a tool is needed → use it → read the result → back to 2.
4. Answer.

In n8n you can watch this loop: open an execution of the agent and look at the log of the **AI Agent** node.

## Why a *learning* agent?

A normal AI assistant is built to **give answers**. That's great for getting work done, but bad for learning: if the AI does the thinking, you don't learn.

A learning agent is built to **make you think**:

- asks questions instead of giving solutions (Socratic method),
- gives hints step by step,
- checks what you already know,
- adapts to your level and your language,
- makes mistakes visible and okay.

Whether an agent behaves like this is decided almost entirely by its **instructions**. That's what you design in the workshop.

## Limits – stay critical

- Language models can **sound sure and still be wrong** ("hallucination"). Check important facts.
- Don't type **personal data** (names, grades, health, addresses) into AI tools.
- The agent only knows what's in its model, its memory and its tools.
