# 📝 Groq Conversation Manager & Info Extractor (Colab Notebook)

This Colab notebook demonstrates:  
- Managing and summarizing conversations  
- Periodic summarization using **Groq LLaMA-3 models**  
- Extracting structured user details via **function-calling + JSON Schema**  
- Schema validation of extracted results  
- Offline fallback (regex-based extraction + local summarizer) if no API key is provided  

---

## 🚀 Getting Started  

### 1. Open in Google Colab  
Click here to open directly (replace with your repo link if uploaded):  

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/your-username/your-repo-name/blob/main/groq_assignment.ipynb)

---

### 2. Install Dependencies  
Run this inside Colab:  
```bash
!pip install openai jsonschema
