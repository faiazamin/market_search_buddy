# AI Multi-Source Market Research Agent

This project is an advanced AI-powered research assistant that synthesizes information from Google, Bing, and Reddit to answer user questions with comprehensive, multi-perspective insights. It leverages LLMs (e.g., GPT-4o via LangChain) and BrightData APIs for web and social data retrieval.

## Features

- **Parallel Search:** Simultaneously queries Google, Bing, and Reddit for the user's question.
- **Automated Analysis:** Uses LLMs to analyze and summarize search results from each source.
- **Reddit Deep Dive:** Selects the most relevant Reddit posts, retrieves detailed comments, and extracts community insights.
- **Synthesis:** Combines findings from all sources into a well-structured, balanced answer.
- **Modular Design:** Easily extendable for new sources or analysis strategies.

## Project Structure

- `main.py` — Entry point; runs the interactive research agent.
- `web_operations.py` — Handles Google/Bing/Reddit search and data retrieval via BrightData API.
- `snapshot_operations.py` — Manages BrightData snapshot polling and downloading.
- `prompts.py` — Contains all prompt templates and message construction logic for LLM interactions.
- `pyproject.toml` — Project dependencies and metadata.

## Setup

### Prerequisites

- Python 3.13+
- BrightData API key (for web and Reddit data)
- OpenAI API key (for LLM, if using LangChain OpenAI integration)

### Installation

1. Clone the repository:
	```sh
	git clone <repo-url>
	cd market_search_buddy
	```
2. Install dependencies:
	```sh
	pip install -r requirements.txt
	# or, if using poetry or pipenv, use the pyproject.toml
	```
3. Create a `.env` file in the project root with the following:
	```env
	BRIGHTDATA_API_KEY=your_brightdata_api_key
	OPENAI_API_KEY=your_openai_api_key
	```

## Usage

Run the agent interactively:

```sh
python main.py
```

You will be prompted to enter a question. The agent will:

1. Search Google, Bing, and Reddit in parallel.
2. Analyze and summarize results from each source.
3. Select and retrieve detailed Reddit posts and comments.
4. Synthesize all findings into a comprehensive answer.

Type `exit` to quit.

## Customization

- **Prompts:** Modify `prompts.py` to adjust how the LLM analyzes or synthesizes information.
- **APIs:** Update `web_operations.py` to add new data sources or change search logic.

## Dependencies

Key packages (see `pyproject.toml`):

- `langchain`, `langchain-openai`, `langgraph` — LLM orchestration and graph-based workflow
- `python-dotenv` — Environment variable management
- `requests` — HTTP requests for API calls

## License

MIT License (add your license here)

## Acknowledgments

- [LangChain](https://github.com/langchain-ai/langchain)
- [BrightData](https://brightdata.com/)
- [OpenAI](https://openai.com/)

---
*For questions or contributions, please open an issue or pull request.*
