# Hacktiv8-Gemini-Chatbot-API

The AI acts as the brain for the chatbot, creating the conversational replies.
1. The user sends a message from the frontend.
2. Node.js backend receives this message.
3. The backend passes the user's message to the Gemini AI model (gemini-2.0-flash).
4. The AI model processes the message and generates a new, relevant text response.
5. Backend sends this AI-generated response back to the frontend to be displayed in the chatbox.

Node Js 2025-07-15, Version 22.17.1 'Jod' (LTS) \
Gemini API

```
npm install express dotenv cors @google/generative-ai
```

This setup prepares a Node.js project using Express and integrates the Gemini 2.0 Flash API through the @google/generative-ai package, enabling support for text, audio, image, or document input handling.

- express: Sets up the REST API.
- dotenv: Loads the Gemini API key securely from a .env file.
- @google/generative-ai: Connects to the Gemini API (including Flash 1.5).
- cors: Allow requests from any origin to access this server’s endpoints.

.env : This file holds environment variables, especially sensitive credentials like your Gemini API key. i.e :
```
GEMINI_API_KEY=your_credential_key
```


index.js contains all the logic for the REST endpoints that interact with Gemini AI. It:
- Sets up an Express app
- Connects to Gemini 2.0 Flash model
- Defines endpoints POST api/chat
- Handles request parsing, file uploads, error management, and responses

script.js – Handles frontend logic, such as sending user input to the Gemini API via HTTP requests.

This organization allows you to:
- Run your Gemini backend API with Node/Express. ```node index.js```
- Access the chatbot frontend via ```http://localhost:3000``` after starting the server.
