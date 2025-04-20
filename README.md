# LLM-questiongen-news

Use LLMs to auto-generate constructive questions from news articles.  
Aimed at enhancing **media literacy**, **critical reading**, and **educational applications**.

---

## ✨ Task Goal

This project builds an automated pipeline that:

- Loads and processes a dataset of **408 news articles**
- Batches them into groups of **15**
- Uses **Gemini** and **Groq's LLM APIs** to generate meaningful questions for each article
- Handles **error logging**, **API rate limits**, and **response parsing**
- Outputs the results into both **CSV** and **JSONL** formats

---

## 🪛 Methodology

- **Data Source**: News articles in `.jsonl` format with fields like title, content, and url  
- **Preprocessing**: Clean and extract relevant article text  
- **Prompt Engineering**: Design prompts that ensure questions are constructive, non-yes/no, and grounded in the article  
- **LLM Integration**:  
  - Originally used **Gemini Pro (Google)**  
  - Switched to **Groq API with LLaMA 3 70B model** for faster, efficient generation  
- **Batch & Delay**:  
  - Process 15 articles per batch  
  - Insert 30s delay between batches to respect rate limits  
- **Error Handling**:  
  - Catch and log API errors (e.g., deprecation, model access, format issues)  
  - Fallback structure to avoid interruption  
- **Output**:  
  - Combined result saved as `news_with_questions_all.csv` and `news_with_questions_all.jsonl`  

---

## 🟢 Results

- Successfully processed **408 news articles**
- Generated a diverse and constructive set of questions
- Achieved high API response accuracy and batch reliability
- Outputs structured and accessible for downstream analysis or use

---

## 🌷 Application

- **NLP Research**: Q&A dataset generation, question quality analysis  
- **AI Development**: Can be fine-tuned for intelligent tutoring or news summarization tasks  
- **Media Analysis**: Studying how AI generates inquiries based on media  
- **Education**: Reading comprehension, news literacy programs



