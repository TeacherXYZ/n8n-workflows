**English** | [Deutsch](connect-an-ai-model.de.md)

# Connecting an AI model

The agent workflows (02 and 03) need access to a language model. n8n talks to the model via an **API key**, saved as a **credential**.

> The workflow files in this repo **never contain keys**. After importing, every learner selects or creates the credential in their own n8n.

## Which option?

| Option | Effort | Good for |
|---|---|---|
| **A. n8n Cloud free credits** | lowest | You use n8n Cloud (trial). |
| **B. Class key from the teacher** | low | The whole group, short session. |
| **C. Your own free key** | 5–10 min | Working on after the workshop. |
| **D. Claude (Anthropic)** | low, paid | You or your school have an Anthropic API account. |

### A. n8n Cloud: free OpenAI credits

On n8n Cloud, the OpenAI credential dialog may offer **free OpenAI API credits** for new accounts.
Double-click **AI model** → **Credential to connect with** → **Create new credential** → look for the free credits offer and accept it.

### B. Class key from the teacher

1. Double-click **AI model** → **Credential to connect with** → **Create new credential**.
2. Paste the API key your teacher gives you → **Save**.
3. The node should turn from red to normal.

### C. Your own free key

Several providers have a free tier (rules and limits change – check the provider's page):

- **Mistral AI** (Europe): <https://console.mistral.ai> → API keys
- **Google Gemini**: <https://aistudio.google.com> → Get API key (age limits apply)
- **Groq**: <https://console.groq.com> → API keys

Then [swap the model node](#swap-the-model-node).

### D. Claude (Anthropic)

1. Sign in at <https://platform.claude.com> (separate from claude.ai).
2. **Billing**: add credit – the API does not work without it, even with a claude.ai subscription.
3. **API Keys** → **Create Key**. Copy it right away; it is shown only once.
4. [Swap the model node](#swap-the-model-node) and choose **Anthropic Chat Model**.
5. **Model**: pick from the list, or switch to **By ID** and type the ID:

| Model | ID | Price per 1M tokens (in / out) |
|---|---|---|
| Claude Opus 5.5 | `claude-opus-5-5` | $4 / $20 |
| Claude Sonnet 5.5 | `claude-sonnet-5-5` | $2 / $10 |
| Claude Haiku 5.5 | `claude-haiku-5-5` | $0.10 / $0.50 |

If you get an error about **temperature**, **top_p** or **thinking**: open **Options** in the Anthropic node and remove those settings – current Claude models don't accept them.

## Swap the model node

1. Delete the node **AI model**.
2. On the **Learning Agent** node, click the **+** under **Chat Model**.
3. Choose your provider (e.g. *Anthropic Chat Model*, *Mistral Cloud Chat Model*, *Google Gemini Chat Model*, *Groq Chat Model*).
4. Create the credential with your key and pick a model from the list.

## Safety rules for API keys

- An API key is like a password **and** a credit card: whoever has it can use it – and you may pay.
- Never put a key into a workflow field, a screenshot, a chat or a Git repo. Only into the **credential** dialog.
- Teachers: for a class key, set a **low spending limit** at the provider and **delete the key** after the session.
