<div align="center">

# 🤖 From RNN to Transformers
### Understanding the Evolution of Modern NLP

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=24&pause=1000&color=00BFFF&center=true&vCenter=true&width=700&lines=Understanding+RNN;Understanding+LSTM;Encoder-Decoder+Architecture;Attention+Mechanism;Transformers;Foundation+of+Large+Language+Models"/>

---

<img src="https://img.shields.io/badge/NLP-DeepLearning-blue"/>
<img src="https://img.shields.io/badge/LLM-Transformers-red"/>
<img src="https://img.shields.io/badge/Python-3.11-yellow"/>
<img src="https://img.shields.io/badge/Learning-2026-green"/>

</div>

---

# 📚 Table of Contents

- Why RNN?
- What is Hidden State?
- Problems with RNN
- LSTM
- Cell State
- Hidden State
- Encoder Decoder
- Context Vector
- Attention Mechanism
- Transformers
- Why Transformers Changed AI

---

# 🧠 Evolution

```text
RNN
   │
   ▼
LSTM
   │
   ▼
Seq2Seq
(Encoder → Decoder)
   │
   ▼
Attention
   │
   ▼
Transformer
   │
   ▼
GPT • BERT • Llama • Qwen
```

---

# 1️⃣ Recurrent Neural Network (RNN)

RNN processes words **one at a time**.

```
Input

I

↓

love

↓

AI

↓

Output
```

Every new word updates the model's memory.

---

# Hidden State

Hidden State is simply the model's current understanding.

```
"I"

↓

Hidden State

↓

"I love"

↓

Hidden State

↓

"I love AI"
```

Think of it as your brain's understanding while reading a sentence.

---

# ❌ Problem with RNN

Suppose we have

```
The boy who won the competition
after training for years
finally thanked his coach.
```

By the time RNN reaches

```
coach
```

it may forget

```
boy
```

because information gradually fades.

---

# 2️⃣ Long Short-Term Memory (LSTM)

LSTM improves RNN by adding **long-term memory**.

Instead of storing only

```
Hidden State
```

it stores

```
Hidden State

+

Cell State
```

---

# LSTM Animation

```text
          Previous Cell State
                   │
                   ▼
          ┌─────────────────┐
Input ───►│      LSTM       │────► Hidden State
          │                 │
Prev H ──►│                 │────► Cell State
          └─────────────────┘
```

---

# Hidden State

Current understanding.

```
Current Memory
```

---

# Cell State

Long-term memory.

Stores important information.

Imagine carrying a notebook.

Important information stays inside.

---

# Example

Sentence

```
My name is Vedant.
```

The model remembers

```
Name = Vedant
```

inside the Cell State.

---

# 3️⃣ Encoder Decoder

Used for Machine Translation.

Example

```
English

I love AI

↓

Encoder

↓

Context Vector

↓

Decoder

↓

French

J'aime l'IA
```

---

# Encoder

Reads the entire sentence.

```
I

↓

love

↓

AI
```

Produces

```
Context Vector
```

---

# What is Context Vector?

Think of it as a summary.

Movie

↓

Summary

Entire Sentence

↓

One Vector
```

The Context Vector stores the overall meaning of the sentence.

---

# Problem

Imagine compressing

```
100 words
```

into

```
1 vector
```

Important information can be lost.

---

# 4️⃣ Attention

Instead of using

```
ONE Context Vector
```

Attention allows the decoder to access

```
Word 1

Word 2

Word 3

Word 4

...

Whenever Needed
```

No more bottleneck.

---

# Attention Animation

```
Encoder Outputs

Word1

Word2

Word3

Word4

      ↘
       ↘
        ↘
       Decoder
```

The decoder focuses only on relevant words.

---

# 5️⃣ Transformer

Transformer removes recurrence completely.

Instead of reading

```
Word1

↓

Word2

↓

Word3
```

it reads

```
Word1

Word2

Word3

Word4

Word5
```

all at the same time.

---

# Why Transformers are Better

| LSTM | Transformer |
|-------|-------------|
| Sequential | Parallel |
| Slower | Faster |
| Limited Context | Global Context |
| Memory Bottleneck | Self-Attention |
| Difficult Scaling | Billion Parameter Models |

---

# Impact

✅ ChatGPT

✅ GPT

✅ BERT

✅ Llama

✅ Qwen

✅ Mistral

✅ Gemini

are all based on Transformers.

---

# Learning Roadmap

```
Python

↓

Machine Learning

↓

Deep Learning

↓

RNN

↓

LSTM

↓

Seq2Seq

↓

Attention

↓

Transformer

↓

LLMs

↓

Fine Tuning

↓

RAG

↓

Agentic AI
```

---

# Resources

📖 Attention Is All You Need (2017)

📖 The Illustrated Transformer

📖 Stanford CS224N

📖 Hugging Face Course

---

# ⭐ If you found this repository helpful

Please consider giving it a ⭐

It motivates me to continue documenting my AI learning journey.
