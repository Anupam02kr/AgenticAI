# 🤖 Welcome to AgenticAI

Hey there! 👋 Welcome to **AgenticAI**. 

I put this project together to explore what autonomous AI agents can really do. Using the awesome [Agno](https://github.com/agno-agi/agno) framework, this repo is a playground for different AI personalities and capabilities—from searching the web and analyzing stocks to watching YouTube videos and even working together as a team!

## 📂 What's Inside?

I've broken things down into a few neat little scripts, each with its own "flavor" of AI:

- ✈️ **`agent.py`**: Your friendly neighborhood Travel Agent. It uses Groq and DuckDuckGo to browse the web and plan perfect trips.
- 📈 **`finance.py`**: A mini Wall Street analyst sitting right in your terminal. It pulls real-time stock data, checks fundamentals, and gives you the scoop using Yahoo Finance.
- 🍿 **`youtube_analyzer.py`**: Too busy to watch a long video? This agent watches (well, reads) YouTube content for you, breaks down the structure, and gives you the highlights. 
- 🎨 **`ui.py`**: A clean, interactive web app for the YouTube analyzer, built with [Streamlit](https://streamlit.io/). No terminal required!
- 🤝 **`teams.py`**: Why use one AI when you can have three? This script spins up a multi-lingual team (English, Chinese, and Hindi) that collaborates to answer your questions all at once.
- 🧠 **`memory.py`**: Ever wish your AI remembered what you talked about yesterday? This script uses a local SQLite database to give the agent a persistent memory.

## 🛠️ Getting Started

Want to take these agents for a spin? Awesome. Here is what you'll need to do.

First, make sure you have Python installed. Then, grab yourself a coffee and install the dependencies:

```bash
pip install agno streamlit python-dotenv rich yfinance duckduckgo-search
```

*Don't forget: depending on which agent you're talking to, you might also need the `openai` and `groq` Python packages.*

## 🔑 Bring Your Own Keys

Our AI friends need to authenticate with their AI brains. Create a `.env` file right here in the main folder and drop in your API keys:

```ini
OPENAI_API_KEY=your_openai_api_key_here
GROQ_API_KEY=your_groq_api_key_here
```

## 🚀 Let's Run It!

### Chat in the Terminal
To wake up one of the terminal-based agents, just run the script with Python. For example:

```bash
python finance.py
python memory.py
```
*(Pro-tip: A couple of these files only define the tools right now. If nothing happens when you run them, just add a quick `agent.print_response("Hello!")` block at the bottom!)*

### Spin up the Web UI
If you want to play with the YouTube Analyzer in a nice browser interface, run this:

```bash
streamlit run ui.py
```
A local server will pop up in your browser. Just paste a YouTube link, hit the button, and watch the magic happen! ✨
