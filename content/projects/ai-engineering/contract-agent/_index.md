---
title: "AI Contract Analysis"
draft: false
summary: "An AI Agent that Searches for and Analyses Contracts"
---
{{< video src="../static/videos/ContractAiAgent.mp4" width="600" autoplay="true" loop="true" >}}
This AI-powered contract analysis tool is built with Python and Streamlit, leveraging Hugging Face Transformers for text summarization and structured contract evaluation.

- Users input contract text or keywords, which are processed to find the closest matching contract from a local database.

- The BART (facebook/bart-large-cnn) model is applied via a text2text-generation pipeline to generate structured summaries, highlighting obligations, deadlines, penalties, high-risk clauses, and plain-language explanations.

- Device selection automatically uses GPU, Apple MPS, or CPU to optimize inference speed and efficiency.

- The Streamlit frontend provides an interactive, real-time interface, displaying AI-generated analyses alongside keyword-based highlights for clarity and readability.

[Back to AI Engineering]({{< relref "../_index.md" >}})