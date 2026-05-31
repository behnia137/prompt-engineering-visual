# 🔄 Iterative Refinement

> **🧒 Explain Like I'm 5:** The first answer is a rough draft, not the final word. Tell the AI what to fix and it gets better each round — like editing with a writing buddy.

## 🖼️ The Picture

```mermaid
flowchart LR
    D["📝 Draft 1"] --> F1["🗣️ 'shorter, more punchy'"]
    F1 --> D2["📝 Draft 2"]
    D2 --> F2["🗣️ 'add a stat in line 1'"]
    F2 --> D3["✅ Draft 3 (nailed it)"]
    style D3 fill:#dcfce7,stroke:#22c55e,color:#14532d
```

## 🔧 How it actually works

**Iterative refinement** treats prompting as a conversation, not a one-shot vending machine. You get a draft, then steer it with specific feedback: "make it 30% shorter," "use a friendlier tone," "you dropped the call-to-action — add it back," "keep everything but rewrite the intro." The model remembers the prior turns (within its [context window](https://github.com/behnia137/ai-for-beginners-visual/blob/main/concepts/context-window.md)) and applies your notes.

The key is **specific, one-thing-at-a-time feedback**. Vague nudges ("make it better") give random changes; targeted edits ("replace the second paragraph with a concrete example") give controlled ones. It mirrors how you'd direct a human assistant — and it's usually faster than trying to craft the perfect mega-prompt up front.

A powerful variant is **self-critique**: ask the model to critique its own output and then improve it. "Here's your draft. List 3 weaknesses, then rewrite fixing them." The model is often a better editor of its work than a first-try author.

## 🌍 Real-world example

You ask for a cover letter, get a decent draft, then say "cut the clichés, mention my 5 years in retail, and end with enthusiasm, not a request." Two rounds later it's tailored and ready — far better than expecting perfection from prompt one.

## 🔗 Related

- [Clear Instructions](clear-instructions.md)
- [Prompt Chaining](prompt-chaining.md)
- [Self-Consistency](self-consistency.md)
