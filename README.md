# Forward Deployed Engineer (FDE) - Node.js Track

Welcome to the **Forward Deployed Engineer (FDE)** repository dedicated to the **Node.js** track from Coder Army.

This repository is organized so you can either browse the code directly via folders on `main` or switch between dedicated lecture branches (`Lecture-1` through `Lecture-4`).

---

## 📂 Curriculum & Project Structure

| Lecture | Folder | Type | Description |
| :--- | :--- | :--- | :--- |
| **Lecture 01** | [`Lecture-01/`](./Lecture-01) | Notes & Architecture | Introduction to FDE, AI support chatbots (Rule-based vs ML classification vs Modern LLMs). |
| **Lecture 02** | [`Lecture-02/`](./Lecture-02) | Notes & Architecture | LLM foundations, next-token prediction, tokenization, context windows, and system prompts. |
| **Lecture 03** | [`Lecture-03/`](./Lecture-03) | Node.js / Express API | Support ticket summarizer using OpenAI responses endpoint (`POST /api/summarize`). Includes automated tests. |
| **Lecture 04** | [`Lecture-04/`](./Lecture-04) | Express Chatbot API | "Tomato" multi-turn customer support chatbot with conversational state and prompt guardrails (`POST /api/chat`, `DELETE /api`). |

---

## 🚀 Running the Projects

### Lecture 03: Ticket Summarizer
```bash
cd Lecture-03
npm install
npm start
```
Test the endpoint:
```bash
curl -X POST http://localhost:8080/api/summarize \
  -H "Content-Type: text/plain" \
  --data "Customers cannot complete checkout because the payment page times out."
```
Run tests:
```bash
npm test
```

### Lecture 04: Tomato Customer Support Chatbot
```bash
cd Lecture-04
npm install
npm start
```
Test the endpoint:
```bash
curl -X POST http://localhost:3000/api/chat \
  -H "Content-Type: text/plain" \
  --data "Where is my pizza order? It has been 45 minutes!"
```
Reset conversation session:
```bash
curl -X DELETE http://localhost:3000/api
```

---

## 🌿 Git Branches

If you prefer studying lecture-by-lecture with clean branch progression:
- `git checkout Lecture-1`
- `git checkout Lecture-2`
- `git checkout Lecture-3`
- `git checkout Lecture-4`
- `git checkout main` (All lectures included)

---

## 🔑 Environment Configuration

An OpenAI API key is configured locally in `.env` within `Lecture-03/` and `Lecture-04/`:
```env
OPENAI_API_KEY=your_openai_api_key_here
PORT=3000
OPENAI_MODEL=gpt-4o-mini
```
Refer to `.env.example` in each folder for options.
