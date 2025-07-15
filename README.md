
# 📘 AI-Powered Book Publication Workflow

![Python](https://img.shields.io/badge/Python-3.11%2B-blue?logo=python)
![Gradio](https://img.shields.io/badge/Gradio-UI-orange?logo=gradio)
![Playwright](https://img.shields.io/badge/Playwright-WebScraping-green?logo=playwright)
![License: Custom](https://img.shields.io/badge/license-custom-lightgrey)

## 🔥 Project Theme: AI-Driven Content Spinning with Human Reinforcement

This project is an automated, intelligent content rewriting system that leverages AI to rephrase literary chapters from public domain sources. It features a reinforcement learning-style reward system, enabling users to iteratively refine and rate AI-generated content. Human reviewers are integral to the feedback loop, blending AI creativity with human editorial judgment.

**Key Use Cases:**
- Educational rephrasing of difficult texts
- Audiobook or podcast script preparation
- Creating accessible versions of classic literature
- Enhancing editorial workflows in content agencies


---

## 🎯 Objective

Build a modular pipeline to:
- Scrape chapter content from web sources
- Apply AI "spinning" (rewriting) logic using LLMs
- Enable voice and text input for refining or querying content
- Allow human editors to guide improvements
- Capture star ratings as reinforcement signals
- Store versioned content snapshots for future analysis or finetuning


---

## 🛠️ Tech Stack Overview

| Tool/Library              | Role                                              |
|---------------------------|---------------------------------------------------|
| Python                    | Core language for scripting and orchestration     |
| Gradio                    | Interactive user interface                        |
| Playwright                | Web scraping and screenshot capture               |
| HuggingFace Transformers  | LLMs (e.g., OpenAI Whisper, text-generation)      |
| ChromaDB / FAISS          | Semantic retrieval and version search             |
| Torch + CUDA              | GPU acceleration for ASR and transformer inference|
| JSON                      | Lightweight versioning format                     |


---

## ✨ Key Features

1. **Chapter Scraping + Screenshot**
   - Fetches chapter content from sources like [Wikisource](https://en.wikisource.org/wiki/The_Gates_of_Morning/Book_1/Chapter_1)
   - Uses Playwright to render and capture a full-page screenshot for archival

2. **AI Chapter Rewriter (Content Spinner)**
   - Choose from multiple rewrite styles: Simplified, Formal, Creative
   - Built on transformers with custom prompt engineering

3. **Human-in-the-Loop**
   - Users can manually edit output, submit improvement instructions, and iterate through cycles of edits
   - Simulates a professional editor's workflow with AI assistance

4. **Versioning + Metadata**
   - Each new version is saved in `versions.json`:
     ```json
     {
       "chapter": "1",
       "version": "version_1720012745",
       "content": "...updated chapter...",
       "reward": 4
     }
     ```
   - Allows tracking of edits, feedback quality, and model performance over time

5. **Semantic Chatbot (RAG)**
   - Users can ask questions like "What are the main characters in this chapter?"
   - The system queries embedded chapter content via a vector store and responds contextually

6. **Voice-to-Chat Integration**
   - Users can upload or record `.wav`/`.mp3` audio queries
   - Transcribes using OpenAI Whisper and passes to the chatbot engine

7. **RL Reward System**
   - Users submit 1–5 star feedback
   - Ratings influence reward computation, help rank generated content, and enable future supervised fine-tuning or RLHF


---

## 🧩 How It Works

### 📈 Full Workflow Example

1. **Scrape Chapter:** Load a chapter from a Wikisource link
2. **Select Style:** Choose "Simplified" for readability
3. **Rewrite:** AI spins the content to a simpler form
4. **Manual Edits:** Editor tweaks awkward phrases
5. **Voice Query:** Ask, "Who are the main villains?"
6. **Feedback:** Editor rates the AI’s rewrite as 4 stars
7. **Version Stored:** Snapshot saved with metadata

This workflow is ready for review, distribution, or training data generation.


---
## 🎯 Use Cases

| Sector        | Use Case                                                      |
|---------------|---------------------------------------------------------------|
| Education     | Simplify difficult texts for younger students                 |
| Publishing    | Create drafts for audiobook or voiceover content              |
| Media         | Repurpose public domain classics into modern adaptations      |
| Accessibility | Make literature easier to understand for non-native speakers  |
| AI Research   | Collect fine-tuning datasets via human feedback               |


---

## 🛡️ Licensing & Submission Notes

This project is submitted under evaluation guidelines.

Developer retains all rights and licensing.

No commercial intent by Soft-Nerve.

Plagiarism or automated AI tool-generated submissions will be rejected.


---

## 👨‍💻 Author

**Atishay Jain**  
BTech CSE - Data Science | Indore, India  
🔗 AI Research | Full-Stack Dev | Chess Enthusiast

## 📞 Contact

For inquiries or collaboration, reach out via [GitHub](https://github.com/atishaydeveloper) or [LinkedIn](https://www.linkedin.com/in/atishay-jain07/).