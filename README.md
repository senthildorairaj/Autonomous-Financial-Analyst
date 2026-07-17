# Automated Mortgage Underwriting System

An Agentic AI Multi‑Agent Workflow for Automated Mortgage Underwriting.
Built as part of the Johns Hopkins University – Advanced Agentic AI program.


## Project Overview

The Automated Mortgage Underwriting System is an Agentic AI–powered multi‑agent workflow designed to automate and enhance the mortgage underwriting process. Built using LangGraph, LangChain, and OpenAI GPT‑4o‑mini, this system demonstrates how intelligent agents can collaborate to evaluate loan applications with consistency, transparency, and regulatory compliance.

Traditional mortgage underwriting is often time-consuming, document-heavy, inconsistent, and expensive. This AI-powered system addresses these challenges by:

- **Reducing processing time** from days to hours.
- Maintaining **consistent decision quality**.
- Providing an **audit trail** with clear reasoning chains.
- Ensuring **regulatory compliance** (e.g., Fair Lending Act).
- Scaling to handle **thousands of applications** simultaneously.

This project is ideal for learners exploring agentic AI, workflow orchestration, RAG, compliance engineering, and real-world deployment patterns.

## Learning Objectives

By exploring this project, you will be able to:

- **Understand Multi-Agent Systems**: Learn how specialized AI agents collaborate to solve complex problems.
- **Implement Agent Workflows**: Build coordinated workflows using LangGraph's state machine architecture.
- **Apply RAG Patterns**: Integrate retrieval-augmented generation for policy compliance.
- **Handle PII & Compliance**: Implement data sanitization and bias detection mechanisms.
- **Create HITL Systems**: Design human-in-the-loop workflows for high-risk decisions.
- **Production Deployment**: Understand real-world deployment considerations and monitoring.

## System Architecture

The system utilizes a hierarchical multi-agent pattern:  

Specialist Agents:
  -  Credit Analyst Agent
  -  Income Analyst Agent
  -  Asset Analyst Agent
  -  Collateral Analyst Agent

Coordination Agents:
  -  Supervisor Agent – orchestrates workflow
  -  Critic Agent – evaluates agent outputs
  -  Decision Agent – final underwriting decision

A LangGraph state machine coordinates agent interactions, ensuring deterministic and auditable execution.
    (https://github.com/senthildorairaj/Automated-Mortgage-Underwriting-System/blob/main/System%20Architecture.png)


## Technology Stack

- **LangGraph**: Agent orchestration & state management
- **LangChain**: LLM integration & tool management
- **OpenAI - GPT-4o-mini**: Language model for reasoning
- **ChromaDB**: Vector store for policy retrieval
- **Python**: Programming language
- **Jupyter / Colab**:  Interactive development

## Setup and Installation

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/senthildorairaj/Automated-Mortgage-Underwriting-System.git
    cd Automated-Mortgage-Underwriting-System
    ```
    

2.  **Install dependencies:**
    ```bash
    pip install \
      langgraph==1.0.5 \
      langchain==1.0.0 \
      langchain-openai==1.1.7 \
      langchain-community==0.4.1 \
      langchain-text-splitters==1.1.0 \
      chromadb==1.4.0 \
      pypdf==6.6.0
    ```

3.  **API Configuration:**
    This project uses an OpenAI-compatible API. You will need to set your `OPENAI_API_KEY` and `OPENAI_API_BASE` as environment variables or load them from a `config.json` file. Ensure `config.json` contains:
    ```json
    {
      "API_KEY": "YOUR_API_KEY",
      "OPENAI_API_BASE": "YOUR_API_BASE_URL"
    }
    ```
    *Note: For Google Colab, you can use Colab secrets for API keys.* 

## Usage

This project is best explored in a Jupyter Notebook or Google Colab environment. The `Automated_Mortgage_Underwriting_System.ipynb` notebook guides you through:

- Defining data models and state management.
- Building core components like utility tools, PII sanitization, and RAG policy retrieval.
- Implementing specialist agents (Credit, Income, Asset, Collateral, Critic, Decision).
- Integrating the complete workflow using LangGraph.
- Testing and evaluating the system with various test cases.
- Understanding production deployment considerations.

To run the notebook:

1.  Open the .ipynb file in Jupyter or Colab
2.  Execute cells sequentially to follow the multi-agent workflow development.
3.  Observe agent interactions and underwriting decisions.


### Explanation of the different modules (in case if you need more details):
### Part 1: Core Agent Implementation
- Utility tools for calculations 
- PII sanitization system 
- Bias detection mechanism
- RAG policy retrieval
- Test data preparation

### Part 2: Workflow & Orchestration
- Income Analyst Agent Implementation
- Asset Analyst Agent Implementation
- Collateral Analyst Agent Implementation
- Critic Agent Implementation
- Decision Agent Implementation
- Defining state and workflow/graph correctly

### Part 3: Testing & Analysis
- Run all test cases

### Part 4: Summary and Future Scope
- Summary/Observations about this Project
- Future scope of this Project 

## Future Scope

- Expand into full AUS capabilities with additional agents and rule engines.
- Integrate real-time data sources and external APIs (e.g., credit bureaus, bank statements).
- Build a full UI dashboard and case management system for operational visibility.
- Add monitoring, logging, and model evaluation pipelines.

## Contributing

Contributions are welcome! Please open an issue or submit a pull request.

## License

This project is licensed under the JHU License - see the LICENSE file for details.
