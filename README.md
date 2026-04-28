# ResearchMind: Multi-Agent AI Research System

A sophisticated AI-powered research assistant built with Streamlit, LangChain, and multiple specialized agents that collaborate to deliver comprehensive research reports.

## Features

- **Search Agent**: Uses Tavily to find recent, reliable web information
- **Reader Agent**: Scrapes and extracts deep content from relevant URLs
- **Writer Chain**: Crafts well-structured research reports
- **Critic Chain**: Reviews and scores the generated reports for quality
- **Interactive Web Interface**: Clean Streamlit UI with real-time pipeline visualization

## Architecture

The system employs a 4-agent pipeline:
1. **Search Agent** - Gathers recent web information
2. **Reader Agent** - Scrapes top resources for deeper content
3. **Writer Chain** - Drafts the full research report
4. **Critic Chain** - Reviews and provides feedback on the report

## Setup Instructions

### Prerequisites

- Python 3.8+
- OpenRouter API account (for AI models)
- Tavily API account (free tier available)

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd multi-agent-research-system
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   pip install streamlit
   ```

3. **Set up environment variables**
   ```bash
   cp .env.example .env
   ```

   Edit the `.env` file and add your API keys:
   - `OPENAI_API_KEY`: Get from [OpenRouter](https://openrouter.ai/keys) (OpenAI-compatible API)
   - `TAVILY_API_KEY`: Get from [Tavily](https://tavily.com/) (free tier available)

### Running the Application

```bash
streamlit run app.py
```

The application will open in your browser at `http://localhost:8501`.

## Usage

1. Enter your research topic in the input field
2. Click "⚡ Run Research Pipeline"
3. Watch the real-time progress through each agent
4. View the final research report and critic feedback
5. Download the report as a markdown file

## Example Topics

- "Quantum computing breakthroughs in 2025"
- "CRISPR gene editing advancements"
- "Fusion energy progress"
- "LLM agents 2025"

## Technologies Used

- **Streamlit**: Web interface and real-time updates
- **LangChain**: Agent orchestration and LLM integration
- **OpenRouter**: AI model API (OpenAI-compatible)
- **Tavily**: Web search API
- **BeautifulSoup**: Web scraping
- **Python-dotenv**: Environment variable management

## Project Structure

```
├── app.py              # Main Streamlit application
├── agents.py           # Agent definitions and chains
├── tools.py            # Custom tools for search and scraping
├── pipeline.py         # Pipeline orchestration (if separate)
├── requirements.txt    # Python dependencies
├── .env.example        # Environment variables template
└── README.md          # This file
```

## API Keys Required

- **OPENAI_API_KEY**: From OpenRouter for AI model access
- **TAVILY_API_KEY**: For web search functionality

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## License

[Add your license here]

## Support

For issues or questions, please open a GitHub issue.