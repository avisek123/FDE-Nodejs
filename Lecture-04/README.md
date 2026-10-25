# Lecture 04: Tomato Customer Support Chatbot (Multi-Turn Chat API)

## 📖 Overview
In Lecture 4, we build **Tomato Chat**, a customer-support conversational API for a food ordering app named "Tomato".

### Key Concepts Covered:
1. **Multi-turn Conversation State**:
   - Accumulating user and assistant messages into an in-memory `history` array.
2. **System Prompt Guardrails**:
   - Confining the assistant's domain strictly to food orders, delivery tracking, refunds, and company policy.
   - Forcing refusal on general-purpose prompts outside food support.
3. **Promise Queue Serialization**:
   - Using a sequential Promise queue to prevent concurrent user turns from interleaving message history.
4. **Session Reset**:
   - `DELETE /api` clearing the active conversation state.

---

## 🚀 Running the Project

```bash
cd Lecture-04
npm install
npm start
```

API runs at `http://localhost:3000`.

### Test with cURL:
```bash
curl -X POST http://localhost:3000/api/chat \
  -H "Content-Type: text/plain" \
  --data "Where is my pizza order? It has been 45 minutes!"
```

### Reset Conversation:
```bash
curl -X DELETE http://localhost:3000/api
```

---

## 📂 Resources in this Lecture
- [src/app.js](src/app.js) - Express app and chat handler.
- [src/server.js](src/server.js) - Server entrypoint.
- [notes/Notes.pdf](notes/Notes.pdf) - Annotated lecture notes.
