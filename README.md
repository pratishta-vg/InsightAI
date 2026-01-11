# Multimodal RAG Chatbot 🤖📚🖼️

A multimodal Retrieval-Augmented Generation (RAG) chatbot that can understand and answer questions about **documents, images, and YouTube videos**, with optional **web search** and **UI generation** tools.

- **Check it out**:[(https://insight-ai-theta.vercel.app/)]🚀


---

## Overview 🧭

This project lets you:

- 📄 Upload PDFs and images.
- 📺 Ingest YouTube videos via their subtitles.
- 💬 Ask natural language questions about your content.
- 🔍 Retrieve and combine relevant text and image information via vector search.
- 🧰 Optionally call tools (web search, UI generator) when the model decides they are helpful.

The goal is to provide a lightweight but powerful demo of a multimodal RAG system built with modern tooling on both the frontend and backend.

---

## Features ✨

- **Document upload (PDFs & images)** 📎  
  - PDFs: text is extracted, chunked, embedded, and stored in Pinecone.  
  - Images: captioned using an OpenAI vision model; captions are embedded and stored for retrieval.

- **Multimodal RAG** 🧠  
  - Uses the same text embedding space for:  
    - Document text chunks  
    - Image captions  
  - Answers questions grounded in retrieved context (text + images).

- **YouTube ingestion** 🎬  
  - Accepts a YouTube URL.  
  - Fetches the transcript (if available), indexes it, and generates a concise summary.  
  - Lets you chat about the video as if it were a document.

- **Web search tool** 🌐  
  - Uses Tavily API to search the web and summarize results when local context is not enough.

- **UI generation tool** 🎨  
  - Given a textual spec, asks an LLM to generate a small React/TSX component.

- **Clean chat UI** 💬  
  - Document list with active selection.  
  - Chat history with user and bot messages.  
  - Light/dark theme toggle 🌞🌙.

---

## Tech Stack (Brief) 🛠️

- **Frontend** ⚛️  
  - Next.js (App Router)  
  - React + TypeScript  
  - Axios  
  - Deployed on Vercel  

- **Backend** 🐍  
  - FastAPI + Uvicorn  
  - OpenAI API (chat, vision, embeddings)  
  - Pinecone (vector database)  
  - PyPDF2, PyMuPDF (PDF handling)  
  - youtube-transcript-api (YouTube subtitles)  
  - Deployed on Render  
