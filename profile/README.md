<div align="center">

# CheapAIModel

**One API for every AI model — at the lowest price.**

OpenAI-compatible · Pay as you go · No lock-in

[Website](https://cheapaimodel.com) · [Docs](https://github.com/cheapaimodel/docs) · [Examples](https://github.com/cheapaimodel/examples)

</div>

---

## Why CheapAIModel?

- **One API, many models.** Call models from different providers through a single endpoint.
- **Low prices.** We route your requests to keep costs down.
- **OpenAI-compatible.** Already using the OpenAI SDK? Change the base URL and API key — that's it.
- **Pay as you go.** No subscriptions, no minimums.

## Quickstart

**Python**

```bash
pip install openai
```

```python
from openai import OpenAI

client = OpenAI(
    base_url="https://api.cheapaimodel.com/v1",
    api_key="YOUR_CHEAPAIMODEL_KEY",
)

res = client.chat.completions.create(
    model="gpt-4o-mini",
    messages=[{"role": "user", "content": "Hello!"}],
)
print(res.choices[0].message.content)
```

**JavaScript / TypeScript**

```bash
npm install openai
```

```ts
import OpenAI from "openai";

const client = new OpenAI({
  baseURL: "https://api.cheapaimodel.com/v1",
  apiKey: process.env.CHEAPAIMODEL_API_KEY,
});

const res = await client.chat.completions.create({
  model: "gpt-4o-mini",
  messages: [{ role: "user", content: "Hello!" }],
});
console.log(res.choices[0].message.content);
```

**cURL**

```bash
curl https://api.cheapaimodel.com/v1/chat/completions \
  -H "Authorization: Bearer $CHEAPAIMODEL_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{"model":"gpt-4o-mini","messages":[{"role":"user","content":"Hello!"}]}'
```

## Our open source

| Repo | What it is |
| --- | --- |
| [python-sdk](https://github.com/cheapaimodel/python-sdk) | Lightweight Python client, built on the OpenAI SDK |
| [typescript-sdk](https://github.com/cheapaimodel/typescript-sdk) | Lightweight TypeScript client, built on the OpenAI SDK |
| [examples](https://github.com/cheapaimodel/examples) | Ready-to-run examples: chat, streaming, tool calling, LangChain |
| [docs](https://github.com/cheapaimodel/docs) | API documentation |
| [awesome-cheapaimodel](https://github.com/cheapaimodel/awesome-cheapaimodel) | Tools and apps that work with CheapAIModel |

---

<div align="center">Made in Vietnam 🇻🇳 · Built for developers everywhere</div>
