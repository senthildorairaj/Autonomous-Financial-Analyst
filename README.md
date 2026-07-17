# Autonomous Financial Research Analyst

This project develops an autonomous financial research analyst powered by LangChain and LangGraph. The agent is designed to proactively gather comprehensive financial data, analyze market sentiment, retrieve proprietary AI initiative insights, and provide data-driven investment recommendations.

## Project Overview

Investment research often involves manual data gathering from various sources, making it slow and prone to inconsistencies. This project addresses these challenges by creating an intelligent system that automates much of this process, providing timely and in-depth analysis.

## Features

- **Goal-Oriented Agent Charter**: Defines a clear mission for the agent to generate comprehensive financial analysis reports.
- **Autonomous Tool Orchestration**: Utilizes 5 specialized tools:
  - `get_stock_price()`: Fetches real-time stock prices and metrics.
  - `get_stock_history()`: Retrieves historical stock performance for trend analysis.
  - `search_financial_news()`: Searches real-time financial news.
  - `analyze_sentiment()`: Analyzes sentiment of financial text using an LLM.
  - `query_private_database()`: Accesses private analyst reports and AI initiative documents via Retrieval-Augmented Generation (RAG).
- **Behavioral Constraints**: Implements proactive, reactive (error handling), and autonomous behaviors to guide decision-making and ensure transparent reporting.
- **RAG Implementation**: A full RAG pipeline is integrated to unlock insights from private analyst reports, ensuring grounded responses with source citations.
- **Multi-Company Ranking**: Capable of analyzing and ranking multiple companies based on both financial performance and strategic AI innovation.
- **Synergistic Tool Usage**: Demonstrates how multiple AI techniques work together to produce comprehensive insights.

## Setup and Installation

1.  **Install Dependencies**: Run the first code cell in the notebook to install all required Python packages:

    ```bash
    !pip install \
      langchain==0.3.27 \
      langchain-core==0.3.79 \
      langchain-openai==0.3.11 \
      langchain-community==0.3.31 \
      langgraph==0.3.7 \
      tavily-python \
      yfinance==0.2.66 \
      chromadb==1.3.4 \
      pypdf==6.2.0 \
      tiktoken==0.12.0
    ```

2.  **Configuration**: Ensure you have a `config.json` file in your environment with the following structure, replacing placeholders with your actual API keys:

    ```json
    {
      "API_KEY": "YOUR_OPENAI_API_KEY",
      "OPENAI_API_BASE": "YOUR_OPENAI_API_BASE_URL",
      "TAVILY_API_KEY": "YOUR_TAVILY_API_KEY"
    }
    ```
    The notebook will load these keys into environment variables.

3.  **AI Initiative Documents**: The project uses a `Companies-AI-Initiatives.zip` file. The notebook automatically unzips this file to set up the private database for RAG.

## Usage

Run the cells sequentially in the notebook to:

- Define the agent's charter and tools.
- Observe the evolution from a traditional LLM to a full autonomous agent.
- Test error handling capabilities.
- Explore the RAG implementation and its integration with the agent.
- Perform multi-company investment ranking.

### Interactive Testing

Use the final interactive cell (`Final Interactive Test Cell`) to experiment with your own custom queries and analyze different companies based on the agent's capabilities.

## Project Structure

The notebook is divided into several sections:

- **Prerequisites**: Package installation and initial imports.
- **Section 1.1: The Goal (Proactiveness)**: Defines the agent's charter.
- **Section 1.2: The Tools (Actuators)**: Defines the stock price, stock history, financial news search, and sentiment analysis tools.
- **Section 1.3: Constraints and Error Handling**: Details the full agent charter with proactive, reactive, and autonomous behaviors.
- **Building the Agent**: Code for creating the LangGraph agent with different configurations.
- **Testing the Agent**: Demonstrations of traditional LLM, basic agent, and full autonomous agent behavior, including error handling.
- **Section 2.1: RAG Implementation**: Steps for loading, chunking, embedding, and storing private AI initiative documents.
- **Section 2.2: Enhanced Agent with RAG**: Integrates the RAG tool into the agent and updates the charter.
- **Section 2.3: Testing the Enhanced Agent**: Tests the enhanced agent's ability to utilize RAG for AI research activity checks and synergistic tool usage.
- **Section 2.4: Investment Recommendation System**: Demonstrates multi-company ranking based on financial and AI innovation criteria.
- **Summary and Future Scope**: Observations, key learnings, and potential enhancements.

## Future Enhancements

- **Multi-Agent Specialization**: Introduce specialized agents (Market Data, News Intelligence, Risk Analysis) for deeper insights.
- **Enterprise Data Integration**: Connect to Bloomberg/Refinitiv APIs, SEC EDGAR feeds, and proprietary research databases.
- **Advanced Analytics**: Incorporate time-series forecasting, portfolio optimization, and risk scoring models.