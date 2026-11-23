# Web-Search-AI-Agent

A user-friendly AI agent built with **Python, LangChain and Groq**. The agent can search the web, count words and combine these tools to respond to user queries.

This project demonstrates the basic principles of AI agents, including LLM integration, tool selection and tool execution. It is designed as a simple introduction to building AI applications with external tools.

## Features

- **Web Search:** Retrieves information from the web to answer questions.
- **Word Counting:** Counts the number of words in a given text.
- **Tool Integration:** Uses multiple tools within a single conversation.
- **LLM-powered Responses:** Uses a language model accessed through Groq.
- **Modular Structure:** Separates configuration, tools and agent logic.

## Technologies

- Python
- LangChain
- Groq API
- Large Language Models (LLMs)

## Requirements

Before running the project, make sure you have:

- Python 3.10 or newer
- A Groq account and API key
- Git
- A code editor such as VS Code

## Installation

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/YOUR_REPOSITORY.git
cd YOUR_REPOSITORY
```

### 2. Create and activate a virtual environment

**Windows:**

```bash
python -m venv ENV
ENV\Scripts\activate
```

**Mac / Linux:**

```bash
python3 -m venv ENV
source ENV/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Configure your API key

Create a `.env` file by copying the example configuration:

**Windows:**
```bash
copy .env.example .env
```

**Mac / Linux:**
```bash
cp .env.example .env
```

Open the `.env` file and add your Groq API key:

```env
GROQ_API_KEY=your_actual_key_here
```

You can obtain an API key from [Groq Console](https://console.groq.com/).

### 5. Run the agent

```bash
python agent.py
```

Once initialized, the agent will be ready to receive questions through the terminal.

## Example Usage

You can ask the agent to perform tasks such as:

```text
Search the web for the latest developments in artificial intelligence.
```

Or combine multiple tools in one request:

```text
Search for the latest LangChain version and count the words in your answer.
```

The agent determines which tools are needed, executes them and uses their results to generate a response.

## Project Structure

```text
Tool-Calling-AI-Agent/
│
├── agent.py
│
├── config/
│   └── settings.py
│
├── tools/
│   ├── search.py
│   └── word_count.py
│
├── docs/
│   ├── SETUP.md
│   ├── HOW_IT_WORKS.md
│   └── TROUBLESHOOTING.md
│
├── requirements.txt
├── .env.example
└── README.md
```

## How It Works

The agent uses four main components:

1. **Language Model:** Groq provides access to the LLM that processes user requests and generates responses.
2. **Tools:** The agent has access to web search and word-counting functions.
3. **Instructions:** Configuration settings define how the agent operates.
4. **Agent Execution Loop:** The agent receives a request, determines whether a tool is needed, executes the selected tool and uses the result to formulate its response.

The project currently does not include conversational memory, meaning that each new interaction starts independently.

## Possible Improvements

Some extensions that could make the agent more capable include:

- Adding conversational memory.
- Integrating a calculator tool.
- Enabling local file reading.
- Implementing streaming responses.
- Adding additional external tools and API integrations.

## License

This project is distributed under the MIT License. See the `LICENSE` file for further details.

## Acknowledgements

Built as a learning project, using the LangChain framework and Groq API to explore the fundamentals of tool-using AI agents.
