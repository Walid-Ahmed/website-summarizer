# 🌐 Website Summarizer

This project provides simple tools to **scrape and summarize websites** using either:
- [Ollama](https://ollama.ai) (local LLMs like `llama3.2`)
- [OpenAI](https://platform.openai.com) API (`gpt-4o-mini` or others)

The summarizer extracts the **main text** of a webpage (removing scripts, styles, and navigation noise) and generates a **clean markdown summary**.

---

## 🚀 Features
- Scrape website content with `BeautifulSoup`
- Summarize with **Ollama** (`summarizer_with_ollama.py`)
- Summarize with **OpenAI API** (`summarizer_with_openai.py`)
- Modular `Website` class for reuse (`website.py`)
- Outputs summaries in **Markdown**

---

## 📂 Project Files
- `website.py` → Utility class for scraping
- `summarizer_with_ollama.py` → Summarizer using Ollama
- `summarizer_with_openai.py` → Summarizer using OpenAI
- `requirements.txt` → Dependencies

---

## ⚙️ Setup

### 1️⃣ Clone the Repo
```bash
git clone https://github.com/Walid-Ahmed/website-summarizer.git
cd website-summarizer
```

### 2️⃣ Install Dependencies
```bash
pip install -r requirements.txt
```

### 3️⃣ Setup Environment Variables (for OpenAI)
Create a `.env` file with your API key:
```
OPENAI_API_KEY=your_api_key_here
```

---

## ▶️ Usage

### Using Ollama (local model)
```bash
python summarizer_with_ollama.py
```

### Using OpenAI API
```bash
python summarizer_with_openai.py
```

Both scripts will fetch **CNN homepage** as an example and print a summary.

---

## 🔧 Customization
- Change the target website URL inside the script:
  ```python
  website="https://example.com"
  response = summarize(website)
  print(response)
  ```

- Modify the **system prompt** for different summarization styles.

---

## 📜 License
MIT License
