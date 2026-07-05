
# 🔬 Multi-Agent-AI-Research System

ResearchMind is a powerful, multi-agent AI research system built with **Streamlit**, **LangChain**, and **Mistral AI**. It coordinates four specialized AI agents to automatically search the web, scrape deep content, draft comprehensive reports, and critique the final output.

## ✨ Features

* **Sleek Custom UI:** A beautiful, dark-themed Streamlit interface with step-by-step pipeline tracking, custom CSS, and responsive design.
* **4-Stage Agent Pipeline:** 
  1. **🔍 Search Agent:** Gathers recent web information using Tavily Search.
  2. **📄 Reader Agent:** Selects the best URLs and scrapes deep content using BeautifulSoup/lxml.
  3. **✍️ Writer Chain:** Synthesizes the raw data into a polished, structured Markdown report.
  4. **🧐 Critic Chain:** Reviews the draft and provides actionable feedback and scoring.
* **Multi-LLM Support:** Built to leverage the `langchain-mistralai` ecosystem alongside optional OpenAI models.
* **Async & Robust:** Uses asynchronous processing (`aiohttp`) and retry logic (`tenacity`) for stable, high-performance web scraping and API calls.
* **Exportable Results:** Download the final research report directly as a `.md` file.

## 🛠️ Tech Stack

* **Frontend:** Streamlit
* **Orchestration:** LangChain (`langchain`, `langchain-core`, `langchain-community`)
* **LLMs:** Mistral AI (`langchain-mistralai`, `mistralai`), OpenAI
* **Tools:** Tavily Search API
* **Scraping:** BeautifulSoup4, Requests, lxml, html5lib

## 📋 Prerequisites

* Python 3.9+
* API Keys for the models and tools you intend to use (e.g., Mistral AI, Tavily).

## 🚀 Installation & Setup

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/mansi-chaudhary-ai/Multi-Agent-AI-Research-System.git](https://github.com/mansi-chaudhary-ai/Multi-Agent-AI-Research-System.git)
   cd Multi-Agent-AI-Research-System

```

2. **Create and activate a virtual environment:**
```bash
python -m venv venv
# On macOS/Linux:
source venv/bin/activate
# On Windows:
venv\Scripts\activate

```


3. **Install dependencies:**
```bash
pip install -r requirements.txt

```


4. **Configure Environment Variables:**
Create a `.env` file in the root directory and add your API keys:
```env
# LLM Providers
MISTRAL_API_KEY=your_mistral_api_key_here
or
OPENAI_API_KEY=your_openai_api_key_here

# Search Tools
TAVILY_API_KEY=your_tavily_api_key_here

```



## 💻 Usage

Start the Streamlit application by running the following command in your terminal:

```bash
streamlit run app.py

```

Once the server starts, open your browser to `http://localhost:8501`. Enter a research topic in the input field and watch the agents collaborate in real-time!

## 📂 Project Structure

```text
researchmind/
├── app.py               # Main Streamlit UI and pipeline execution logic
├── agents.py            # LangChain agent definitions (Search, Reader, Writer, Critic)
├── requirements.txt     # Python dependencies
├── .env                 # API keys and environment variables (Not tracked in git)
└── README.md            # Project documentation

```

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to check the [issues page](https://www.google.com/search?q=https://github.com/yourusername/researchmind/issues).

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](https://www.google.com/search?q=LICENSE) file for details.

```

```
