# Project 3 — Natural Language Processing (Medical Assistant with RAG)

📌 **Personal / Academic project (outside of EA).**

---

## Overview
This project applied **Natural Language Processing (NLP) with Generative AI** to build a medical assistant that answers healthcare-related questions accurately and with grounding.  
The solution combines **prompt engineering** with **Retrieval-Augmented Generation (RAG)**, using the **Merck Manual (PDF)** as a knowledge source.

- **Goal:** Provide reliable, clinically grounded answers to medical queries  
- **Key Skills:** NLP, prompt engineering, LLM fine-tuning, RAG pipeline (retrieval + generation), evaluation with LLM-as-a-Judge  

---

## Contents
- [notebook.ipynb](./notebook.ipynb) → Colab notebook with data prep, retrieval setup, and QA experiments  
- [slides.pdf](./slides.pdf) → presentation summarizing problem, approach, and results  
- [data.pdf](./data.pdf) → medical corpus (Merck Manual excerpt) used for retrieval  

---

## Results
- RAG pipeline outperformed plain LLM responses by eliminating hallucinations and truncations  
- **Best Configuration:**  
  - `max_tokens = 512`  
  - `temperature = 0.2–0.3`  
  - `top_p = 0.9`  
  - `top_k = 30`  
  - `k = 3` retrieved chunks  
- Achieved **5/5 ratings** on both groundedness and relevance across test queries (LLM-as-a-Judge evaluation)  

---

## Business Takeaways
- Reliable RAG setup can power **clinical assistants** for doctors, nurses, and healthcare students  
- Config 5 delivered **clinically aligned, complete, and relevant answers**  
- Future improvements: explore fine-tuning and retrieval chunking for better performance on edge cases  

---

## How to Explore
1. Open the notebook (`notebook.ipynb`) to see preprocessing, RAG setup, and evaluation workflow  
2. Review the medical source document (`data.pdf`)  
3. Open the slides (`slides.pdf`) for a concise project summary  

---
