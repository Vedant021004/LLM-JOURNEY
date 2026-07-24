# 🚀 LLM Foundations

> A structured roadmap to master the fundamental concepts behind Large Language Models before diving into Transformers and modern LLM architectures.

---

## 📖 Overview

This repository covers the essential concepts required to understand how modern LLMs work. Each module includes:

* 📚 Theory
* 📝 Notes
* 📄 Research Papers
* 💻 Implementations
* 🎯 Exercises
* 📺 Learning Resources

---

# 📚 Curriculum

| Module                      | Description                                          | Resources                                                                                                                                                            |
| --------------------------- | ---------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **01. NLP Evolution**       | Evolution from Rule-Based NLP to Foundation Models   | [📂 Notes](./01_NLP_Evolution/) • [📄 Papers](./papers/nlp_evolution.md) • [🎥 Stanford CS224N](https://web.stanford.edu/class/cs224n/)                              |
| **02. Language Modeling**   | N-Grams, Neural Language Models, Causal & Masked LMs | [📂 Notes](./02_Language_Modeling/) • [💻 Code](./implementations/language_modeling/) • [🎥 Karpathy - Let's Build GPT](https://www.youtube.com/watch?v=kCc8FmEb1nY) |
| **03. Information Theory**  | Entropy, Cross-Entropy, KL Divergence, Perplexity    | [📂 Notes](./03_Information_Theory/) • [🎥 StatQuest](https://www.youtube.com/@statquest) • [📘 CS224N](https://web.stanford.edu/class/cs224n/)                      |
| **04. Tokenization Basics** | BPE, WordPiece, SentencePiece, TikToken              | [📂 Notes](./04_Tokenization/) • [🤗 Hugging Face Course](https://huggingface.co/learn/nlp-course)                                                                   |
| **05. Embeddings**          | Word2Vec, GloVe, FastText, Contextual Embeddings     | [📂 Notes](./05_Embeddings/) • [📘 Jurafsky Book](https://web.stanford.edu/~jurafsky/slp3/)                                                                          |
| **06. Sequence Modeling**   | RNN, LSTM, GRU, Long-Term Dependencies               | [📂 Notes](./06_Sequence_Modeling/) • [🎥 DeepLearning.AI](https://www.coursera.org/specializations/deep-learning)                                                   |
| **07. Attention Intuition** | Query, Key, Value, Self-Attention                    | [📂 Notes](./07_Attention_Intuition/) • [📖 Illustrated Transformer](https://jalammar.github.io/illustrated-transformer/)                                            |
| **08. Scaling Laws**        | Compute, Data, Model Scaling, Chinchilla             | [📂 Notes](./08_Scaling_Laws/) • [📄 Chinchilla Paper](https://arxiv.org/abs/2203.15556)                                                                             |

---

# 🗂 Repository Structure

```text
LLM-Foundations/
│
├── README.md
│
├── 01_NLP_Evolution/
├── 02_Language_Modeling/
├── 03_Information_Theory/
├── 04_Tokenization/
├── 05_Embeddings/
├── 06_Sequence_Modeling/
├── 07_Attention_Intuition/
├── 08_Scaling_Laws/
│
├── implementations/
├── papers/
├── resources/
└── diagrams/
```

---

# 📺 Recommended Courses

| Course                                          | Link                                                   |
| ----------------------------------------------- | ------------------------------------------------------ |
| Stanford CS224N                                 | https://web.stanford.edu/class/cs224n/                 |
| Hugging Face NLP Course                         | https://huggingface.co/learn/nlp-course                |
| DeepLearning.AI Sequence Models                 | https://www.coursera.org/specializations/deep-learning |
| Andrej Karpathy – Neural Networks: Zero to Hero | https://www.youtube.com/@AndrejKarpathy                |
| Sebastian Raschka                               | https://www.youtube.com/@SebastianRaschka              |

---

# 📚 Recommended Books

| Book                                               | Link                                                                    |
| -------------------------------------------------- | ----------------------------------------------------------------------- |
| Speech and Language Processing (Jurafsky & Martin) | https://web.stanford.edu/~jurafsky/slp3/                                |
| Build a Large Language Model (From Scratch)        | https://www.manning.com/books/build-a-large-language-model-from-scratch |

---

# 📄 Essential Research Papers

| Paper                                                   | Link                                                        |
| ------------------------------------------------------- | ----------------------------------------------------------- |
| Attention Is All You Need                               | https://arxiv.org/abs/1706.03762                            |
| Neural Probabilistic Language Model                     | https://www.jmlr.org/papers/volume3/bengio03a/bengio03a.pdf |
| Efficient Estimation of Word Representations (Word2Vec) | https://arxiv.org/abs/1301.3781                             |
| GloVe                                                   | https://aclanthology.org/D14-1162/                          |
| Chinchilla Scaling Laws                                 | https://arxiv.org/abs/2203.15556                            |
| LLaMA                                                   | https://arxiv.org/abs/2302.13971                            |

---

# 🎯 Learning Path

```text
NLP Evolution
      │
      ▼
Language Modeling
      │
      ▼
Information Theory
      │
      ▼
Tokenization
      │
      ▼
Embeddings
      │
      ▼
Sequence Modeling
      │
      ▼
Attention Intuition
      │
      ▼
Scaling Laws
      │
      ▼
Transformers
```

---

# 🚀 Next Repository

After completing this repository:

➡️ **LLM Transformers**

* Multi-Head Attention
* Positional Encoding
* Encoder
* Decoder
* Transformer Architecture
* GPT from Scratch
* Vision Transformers
* RoPE
* FlashAttention

---

## ⭐ If you find this repository useful

Consider giving it a ⭐ to support the project and help others discover this learning roadmap.
