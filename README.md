# LangGraph Practice Projects

A collection of practice projects for learning and exploring LangGraph, a framework for building stateful, multi-actor applications with large language models.

## Project Overview

This repository contains hands-on labs that demonstrate core LangGraph concepts, from basic graph construction to building interactive AI chatbots.

## Project Structure

```
├── 01_lab.ipynb      # Lab 1: Simple LangGraph State Graph
├── 02_lab.ipynb      # Lab 2: LangGraph Chatbot with OpenAI
├── main.py           # Main entry point
├── pyproject.toml    # Project configuration
├── requirements.txt  # Python dependencies
└── README.md         # This file
```

## Labs

### Lab 1: Simple State Graph (`01_lab.ipynb`)

**Learning Objectives:**
- Define a state object using Pydantic
- Create a StateGraph builder
- Add nodes and edges
- Compile and visualize the graph

**What it does:**
- Creates a simple LangGraph with a single node
- The node randomly selects a country and capital from predefined lists
- Returns formatted output as a message
- Includes a Gradio chat interface for interaction

### Lab 2: LangGraph Chatbot (`02_lab.ipynb`)

**Learning Objectives:**
- Integrate OpenAI's ChatGPT with LangGraph
- Build an interactive chatbot using LangGraph
- Create a web interface with Gradio

**What it does:**
- Creates a LangGraph with a chatbot node powered by GPT-4o
- Processes user messages through the OpenAI API
- Provides responses in a Gradio chat interface
- Demonstrates message handling in stateful graphs

## Installation

### Prerequisites
- Python 3.12 or higher
- OpenAI API key (for Lab 2)

### Setup

1. **Clone or navigate to the project directory:**
   ```bash
   cd langgraph-projects
   ```

2. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```
   
   Or using the project configuration:
   ```bash
   pip install -e .
   ```

3. **Set up environment variables:**
   Create a `.env` file in the project root and add your OpenAI API key:
   ```
   OPENAI_API_KEY=your_api_key_here
   ```

## Running the Labs

### Lab 1: Simple State Graph
Open `01_lab.ipynb` in Jupyter or VS Code and run the cells sequentially. The final cell launches a Gradio chat interface.

### Lab 2: LangGraph Chatbot
Open `02_lab.ipynb` in Jupyter or VS Code and run the cells sequentially. The final cell launches a Gradio chat interface with AI-powered responses.

## Dependencies

The project includes the following key dependencies:
- **langgraph** - Core LangGraph framework
- **langchain** - LLM framework and utilities
- **langchain-openai** - OpenAI integration
- **langchain-community** - Community integrations
- **pydantic** - Data validation and settings
- **gradio** - Web interface for interaction
- **openai** - OpenAI API client
- **python-dotenv** - Environment variable management

See `requirements.txt` for the complete list with versions.

## Key Concepts

### State
- Defined using Pydantic models
- Manages the graph's data flow
- Uses `add_messages` for message aggregation

### Nodes
- Functions that process state
- Can be simple (Lab 1) or integrate external APIs (Lab 2)
- Return updated state

### Edges
- Define the flow between nodes
- `START` and `END` are special nodes
- Can be conditional or unconditional

### Graph Compilation
- Converts the graph builder into an executable graph
- Enables visualization and execution

## Tips for Learning

1. Start with Lab 1 to understand basic graph construction
2. Review the cell outputs and visualizations
3. Modify the examples (e.g., change the list of countries/capitals in Lab 1)
4. Experiment with different prompts in Lab 2
5. Explore the LangGraph documentation for advanced patterns

## Resources

- [LangGraph Documentation](https://langchain-ai.github.io/langgraph/)
- [LangChain Documentation](https://python.langchain.com/)
- [OpenAI API Documentation](https://platform.openai.com/docs/)
- [Gradio Documentation](https://gradio.app/)

## License

This is a practice project for learning purposes.
