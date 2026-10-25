# Forward Deployed Engineer (FDE) - Node.js Track

Welcome to the **Forward Deployed Engineer (FDE)** curriculum repository dedicated to the **Node.js** track.

This repository tracks each lecture with dedicated Git branches. Switch between branches to view and run the code and notes for each lecture.

---

## 🌿 Branches Overview

| Branch | Lecture Title | Content Type | Summary |
| :--- | :--- | :--- | :--- |
| **[`Lecture-1`](#)** | Introduction to FDE & AI Chatbots | Notes & Architecture | Concepts: Rule-based bots vs ML classification vs Modern LLMs, customer support problem solving. |
| **[`Lecture-2`](#)** | LLM Foundations & Prompt Engineering | Notes & Architecture | Concepts: Tokens, context windows, prompt structure, system vs user instructions, embeddings. |
| **[`Lecture-3`](#)** | Support Ticket Summarizer | Node.js / Express Code | Raw support ticket summarizer API using OpenAI responses endpoint (`POST /api/summarize`). |
| **[`Lecture-4`](#)** | Tomato Customer Support Chatbot | Node.js / Express Code | Multi-turn conversational AI customer support API for food delivery (`POST /api/chat`, `DELETE /api`). |

---

## 🚀 Quick Navigation & How to Run

To explore and run a specific lecture, switch to its branch:

### Lecture 1:
```bash
git checkout Lecture-1
```
Contains notes and architectural diagrams for Lecture 1.

### Lecture 2:
```bash
git checkout Lecture-2
```
Contains notes and architectural diagrams for Lecture 2.

### Lecture 3 (Ticket Summarizer API):
```bash
git checkout Lecture-3
npm install
npm start
```
Test the API:
```bash
curl -X POST http://localhost:8080/api/summarize \
  -H "Content-Type: text/plain" \
  --data "Customers cannot complete checkout because the payment page times out."
```
Run tests:
```bash
npm test
```

### Lecture 4 (Tomato Customer Support Chatbot):
```bash
git checkout Lecture-4
npm install
npm start
```
Test the API:
```bash
curl -X POST http://localhost:3000/api/chat \
  -H "Content-Type: text/plain" \
  --data "Where is my pizza order? It has been 45 minutes!"
```
Clear chat session:
```bash
curl -X DELETE http://localhost:3000/api
```

---

## 🔑 Environment Configuration

An OpenAI API key is preconfigured in the `.env` file on code branches (`Lecture-3` and `Lecture-4`):
```env
OPENAI_API_KEY=your_openai_api_key_here
```
Refer to `.env.example` on each branch for available configuration options (e.g. `PORT`, `OPENAI_MODEL`).
