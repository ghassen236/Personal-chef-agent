# 🍳 Personal Chef AI Agent

> My first AI agent, built after completing the LangChain Foundations course from LangChain Academy.

## What it does

The Personal Chef Agent takes your available ingredients and suggests recipes you can make right now. You can interact with it in two ways:
- **Text** — type out the ingredients you have
- **Image** — snap a photo of your fridge and let the agent figure it out!

It searches the web for real recipes, fetches full instructions, and remembers your conversation so you can ask natural follow-up questions like *"give me the full recipe for option 2"*.

## Tech Stack

- **LangChain** — agent framework
- **LangGraph** — memory and conversation management
- **Google Gemini 2.5 Flash** — vision model (image understanding)
- **Groq / LLaMA 3.3 70B** — language model
- **Tavily** — web search
- **BeautifulSoup** — full recipe page fetching

## Setup

1. Clone the repo
2. Create a virtual environment and install dependencies:
```bash
pip install -r requirements.txt
```
3. Copy `.env.example` to `.env` and fill in your API keys:
```
GOOGLE_API_KEY=...
TAVILY_API_KEY=...
GROQ_API_KEY=...
```
4. Open `notebooks/module-1/Personal Chef AI Agent.ipynb` in Jupyter and run!

## Project Structure
```
notebooks/module-1/
└── Personal Chef AI Agent.ipynb   # main project notebook
.env.example                        # API keys template
requirements.txt                    # dependencies
```

## Features

- ✅ Web search for real recipes
- ✅ Full recipe instruction fetching
- ✅ Fridge photo recognition
- ✅ Multi-turn conversation memory
- ✅ Clean response parsing