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

## Getting Your API Keys

### Google Gemini (Vision + Language)
1. Go to [Google AI Studio](https://aistudio.google.com)
2. Click **Get API Key** → **Create API key**
3. Copy it into your `.env` as `GOOGLE_API_KEY`

> ⚠️ The free tier allows **20 requests per day** for `gemini-2.5-flash`.  
> Each agent turn counts as 1-3 requests depending on tool usage.  
> If you hit the limit you'll see a `429 RESOURCE_EXHAUSTED` error — wait until tomorrow.

### Tavily (Web Search)
1. Go to [tavily.com](https://tavily.com)
2. Sign up and grab your API key
3. Copy it into your `.env` as `TAVILY_API_KEY`

## Example Fridge Photo
The file `food_image_example.jpg` in this repo is the test image used during development.  
You can upload your own fridge photo when running the notebook!

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