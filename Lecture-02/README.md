# Lecture 02: LLM Foundations, Next-Token Prediction & Tokenization

## 📖 Overview
Lecture 2 explores how Large Language Models work internally, how text is converted into embeddings and tokens, and how probabilities guide token generation.

### Key Concepts Covered:
1. **Next-Token Prediction**:
   - LLMs generate text auto-regressively by computing softmax probability distributions over a fixed vocabulary given prior context tokens.
2. **Tokenization (BPE & Tiktoken)**:
   - Converting characters into sub-word tokens with integer IDs.
   - Understanding token costs and efficiency across different languages.
3. **Context Window & Attention Mechanisms**:
   - How self-attention allows the model to reference earlier parts of the prompt regardless of distance.
4. **Prompt Roles**:
   - Distinguishing between `system`, `user`, and `assistant` messages to establish behavioral guardrails.

---

## 📂 Resources in this Lecture
- [notes/Notes.pdf](notes/Notes.pdf) - Annotated lecture notes.
- [notes/Excalidraw-Notes.svg](notes/Excalidraw-Notes.svg) - Visual diagrams on tokenization and probabilities.

> *Next: In Lecture 3, we build our first Node.js summarizer API calling OpenAI.*
