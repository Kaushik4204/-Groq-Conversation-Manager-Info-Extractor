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
```

---

### 3. Configure API Key

You have two options:

Option A (recommended):
In Colab, set your key as an environment variable:

```bash
import os
os.environ["GROQ_API_KEY"] = "your_api_key_here"
```


Option B (interactive prompt):
If no key is found, the notebook will securely prompt you to paste your key (hidden input).

---

### ⚙️ Features

#### ✅ Conversation Manager

Maintains chat history

Retrieves last N turns / truncates by chars or words

Periodic summarization (e.g., every 3rd run)

Summarization via Groq API or offline fallback



####  ✅ Information Extraction

Extracts name, email, phone, location, age from free-form chats

Uses Groq’s function-calling API

Falls back to regex-based parser offline



####  ✅ Schema Validation

Ensures all extracted outputs match the JSON schema

Stores results in groq_conversation_assignment_results.json

---

## 📂 Repository Contents

groq_assignment.ipynb — Main Colab notebook (code + results)

groq_conversation_assignment_results.json — Saved extraction results

README.md — This file

---

## 📊 Example Output

Sample chat:

Hi, my name is John Doe. I’m 29 years old. You can reach me at john@example.com or call 9876543210. I live in Bangalore.


Extracted JSON:

{
  "name": "John Doe",
  "email": "john@example.com",
  "phone": "9876543210",
  "location": "Bangalore",
  "age": 29
}

### 🔒 Notes on Security

Never commit your API key to GitHub.

The notebook reads keys from environment variables or secure prompt.

.ipynb is safe to share without secrets.

---

### 🏆 Next Steps

Extend to support more fields (gender, company, etc.)

Use larger context window models for long chats

Deploy as a web app with FastAPI + Groq


---

