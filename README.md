# Bootcamp_chatbotmed
# 🩺 Health Assistant Chatbot (RAG-Based)

This project was developed as part of the **Akbank GenAI Bootcamp** to demonstrate a **Retrieval-Augmented Generation (RAG)**-based Generative AI application in the healthcare domain.

The chatbot provides **general health information** based on a dataset of medical question pairs.  
It uses **open-source models** (no API keys required) and can answer simple health-related questions safely and informatively.

---

## 🚀 Project Overview

- **Goal:** Create a GenAI-powered chatbot that gives health-related information.
- **Approach:**  
  - Implement a **RAG pipeline** that retrieves similar questions from a medical dataset.  
  - Use the **FLAN-T5 model** to generate short, informative responses.  
  - Build an interactive **web interface** using **Gradio** for user interaction.
- **Platform:** Developed and tested on **Google Colab**.

---

## 🧩 Tech Stack

| Component | Library / Tool | Description |
|------------|----------------|--------------|
| Model | `google/flan-t5-large` | Open-source LLM used for generation |
| Vector Store | `FAISS` | Fast similarity search between questions |
| Embedding | `SentenceTransformer` | Converts text into numerical vectors |
| Framework | `LangChain` | Manages RAG pipeline logic |
| Interface | `Gradio` | Simple web UI for chatbot testing |
| Environment | `Google Colab` | Development and testing platform |

---

## 🧠 RAG Architecture

1. **Retrieval:**  
   The input question is embedded and compared with the dataset using FAISS to find similar questions.  
2. **Augmentation:**  
   The most similar questions are combined into a short context.  
3. **Generation:**  
   The FLAN-T5 model generates a response based on that context.

This process ensures the model’s answers are **grounded in relevant data** rather than pure language generation.

---

## 💬 Example Interaction

**User:** What are the symptoms of COVID-19?  
**Chatbot:** Symptoms of COVID-19 include fever, chills, coughing, and loss of taste or smell.  
Some patients may also feel tired or have a sore throat.

---
