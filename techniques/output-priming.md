# ✍️ Output Priming

> **🧒 Explain Like I'm 5:** Start the answer *for* the AI. Write the first word or two, and it happily continues in exactly the shape you began.

## 🖼️ The Picture

```mermaid
flowchart TB
    P["📝 Prompt ends with:<br/>'...Return JSON.'<br/><br/>Then you pre-write:<br/>{ \"name\":"]
    P --> AI[🤖 continues from there]
    AI --> R["✅ \"name\": \"Mug\", \"price\": 9.99 }"]
    style R fill:#dcfce7,stroke:#22c55e
```

The AI finishes the pattern you started.

## 🔧 How it actually works

**Output priming** (also called *prefilling* or *priming the response*) means you begin the model's answer yourself, and it continues from your starting point. Because an [LLM](https://github.com/YOUR_GITHUB_USERNAME/ai-for-beginners-visual/blob/main/concepts/llm.md) is fundamentally a *next-word predictor*, whatever it's handed to continue strongly shapes what comes next — so seeding the first tokens locks in the format and tone.

It's a precision tool for **forcing structure**. End your instruction and then prime with `{` to force JSON, with `1.` to force a numbered list, with ` ```python ` to force a code block, or with "Sure! Here's the summary:" to skip preamble and jump straight to content. The model treats your opener as established context it must stay consistent with.

This is most powerful via an API, where many providers let you supply a partial "assistant" message that the model literally continues. In a chat box you can approximate it by saying "Begin your answer with `{` and output only JSON." It pairs beautifully with [output formatting](output-format.md) when you need machine-readable results every single time.

## 🌍 Real-world example

A data tool needs clean JSON from the model with zero chatty intro. It prefills the assistant's reply with `{"items": [` — so the model has no choice but to continue valid JSON, and the app never has to strip out "Sure, here you go!" again.

## 🔗 Related

- [Output Formatting](output-format.md)
- [Constraints & Negatives](constraints.md)
- [Few-Shot Prompting](few-shot.md)
