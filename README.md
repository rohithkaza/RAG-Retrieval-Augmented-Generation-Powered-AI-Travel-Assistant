# Travel Companion 🌍
**A RAG (Retrieval-Augmented Generation) Powered AI Travel Assistant for Global Landmark Exploration**

## 🔍 Overview
Travel Companion is a smart AI chatbot designed to deliver concise, trustworthy, and role-specific answers about world landmarks. It combines a dense semantic retriever (Sentence-BERT) with an instruct-tuned language model (Qwen2.5-1.5B-Instruct) to generate context-grounded responses based on a curated Wikipedia travel corpus.

This project demonstrates how Retrieval-Augmented Generation (RAG) can improve answer accuracy and reduce hallucination in LLM outputs—especially in domain-specific tasks like travel planning.

---

## 💡 Key Features
- **RAG Architecture**: Real-time answer generation grounded in retrieved Wikipedia passages.
- **Dense Retriever**: Uses Sentence-BERT for semantic similarity over a 100K+ entry travel corpus.
- **Role-Based Prompting**: User selects a persona (e.g., historian, travel guide), influencing tone and content.
- **LLM Integration**: Generates responses with Qwen2.5-1.5B-Instruct using structured prompts and retrieved evidence.
- **Interactive UI**: Gradio interface enables live chat with dropdown-based role selection.
- **Minimized Hallucinations**: Answers are always backed by real data passages.

---

## 🧠 Tech Stack
- **LLM**: [Qwen2.5-1.5B-Instruct](https://huggingface.co/Qwen)
- **Retriever**: `all-MiniLM-L6-v2` (via Sentence-BERT)
- **Frontend**: [Gradio](https://gradio.app/) for real-time interaction
- **Backend**: Python, NumPy, Pandas
- **Data**: Custom Wikipedia corpus of global travel landmarks (filtered to 100K+ high-quality entries)

---

## 🗂 Architecture
1. **Corpus Construction**: Filtered and preprocessed travel-related Wikipedia entries (name, description, year, country).
2. **Embedding Generation**: Encoded passages with Sentence-BERT; stored dense vectors for similarity search.
3. **Query Retrieval**: Real-time semantic search over precomputed embeddings using cosine similarity.
4. **Prompt Formatting**: Structured prompts based on selected user role and top-k retrieved docs.
5. **LLM Inference**: Generated grounded answers using Qwen2.5 with role-conditioned prompts.
6. **Frontend Delivery**: Deployed an interactive Gradio interface for clean, user-friendly access.

---

## 🧪 Sample Queries
> **User Role**: Travel Guide  
> **Query**: “Famous mountain ranges in Switzerland”  
> **Response**: “The Swiss Alps, including the Jungfrau-Aletsch region (a UNESCO World Heritage Site), are among the most iconic mountain ranges in Switzerland.”

> **User Role**: Historian  
> **Query**: “What is the Terracotta Army in China?”  
> **Response**: “The Terracotta Army consists of thousands of clay soldiers buried with China’s first emperor, Qin Shi Huang, to protect him in the afterlife.”

---

## 📈 Future Improvements
- Hybrid retrieval (BM25 + dense vectors)
- User preference personalization (e.g., architecture vs. natural history)
- Multilingual support
- Feedback-based answer refinement loop

---

## 🙋 About Me
Hi, I'm Rohith — a Master’s student in Computer Science at Rice University, specializing in Machine Learning & AI. This project reflects my passion for building useful, grounded AI systems that go beyond just generating text—they solve real user problems.

Feel free to connect: [LinkedIn](https://linkedin.com/in/rohith-kumar-kaza)

---

