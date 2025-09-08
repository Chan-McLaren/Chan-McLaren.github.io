---
title: "Customer Support Chatbot"
draft: false
summary: "A RAG Chatbot built with Python"
---

{{< video src="../static/videos/chatbotvid.mp4" width="600" autoplay="true" loop="true" >}}

This chatbot is a Retrieval-Augmented Generation (RAG) system built using Python, FastAPI, React, and TailwindCSS. It combines LangChain, Chroma vector database, and sentence-transformer embeddings to provide context-aware answers from your documentation.

- LangChain orchestrates the workflow, retrieving relevant document chunks from Chroma and feeding them into the Google Flan-T5 LLM for natural language       response generation.

- Documents are embedded with all-MiniLM-L6-v2 embeddings, allowing semantic search across your FAQ or knowledge base.

- The frontend is a React app with a responsive, dynamic chat UI built with TailwindCSS. It supports automatic scrolling, live typing indicators, and seamless interaction with the backend.

- This architecture ensures your chatbot can answer questions accurately based on the documents provided, while remaining scalable for additional knowledge sources.

---
You can find the code for this project in my
[Github Repo](https://github.com/Chan-McLaren/customer-support-chatbot)

---
[Back to AI Engineering]({{< relref "../_index.md" >}})