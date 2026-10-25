# Multi Agent AI Research System

This project is an AI powered research tool that helps explore a topic, collect information from the web, generate a research report, and review the report using AI.

Built with Python, LangChain, OpenAI GPT 4o mini, Tavily Search, and Streamlit, the system divides the research process into four stages: searching for information, reading web content, writing a report, and reviewing the final result.

## What Does This Project Do?

### 1. Search Agent

Uses the Tavily Search API to find relevant web pages and collect information related to the given topic.

### 2. Reader Agent

Extracts useful text from web pages using Requests and BeautifulSoup. The extracted content is used to prepare the research report.

### 3. Report Writer

Uses an OpenAI language model to generate a structured report containing an introduction, key findings, a conclusion, and sources.

### 4. Critic Agent

Reviews the generated report, assigns a score out of 10, highlights strengths, identifies areas for improvement, and provides an overall verdict.

The Streamlit interface brings everything together, allowing users to run the research process, view the results, and download the generated report as a Markdown file.

## Features

• Automated web research using Tavily Search

• Web page content extraction using BeautifulSoup

• AI generated research reports

• Report evaluation and feedback using a critic chain

• Interactive Streamlit dashboard

• Separate views for search results and extracted content

• Downloadable reports in Markdown format

• Option to run the research pipeline directly from the terminal

## Technologies Used

| Technology | Purpose |
| :--- | :--- |
| Python | Main programming language |
| Streamlit | Interactive web interface |
| LangChain | Language model integration and workflow management |
| OpenAI GPT 4o mini | Report generation and evaluation |
| Tavily Search | Finding relevant web pages |
| Requests | Fetching web page content |
| BeautifulSoup | Extracting readable text from HTML |
| python dotenv | Loading API keys from environment variables |

## Project Structure

```text
Multi Agent AI Research System/
│
├── app.py
├── agents.py
├── pipeline.py
├── tools.py
├── requirements.txt
├── .gitignore
├── README.md
└── __pycache__/
```

### File Overview

**app.py**

Contains the Streamlit interface where users enter a topic, run the research process, view the generated report, and download the results.

**agents.py**

Defines the search and reader agents, along with the report writing and critic chains.

**pipeline.py**

Coordinates the research stages and runs the complete workflow.

**tools.py**

Contains the web search and web page content extraction functions.

**requirements.txt**

Lists the Python libraries required to run the project.

**.gitignore**

Specifies files that Git should ignore when uploading the project.

## Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/mohda9as/Multi-Agent-AI-Research-System.git
cd Multi-Agent-AI-Research-System
```

### 2. Create a Virtual Environment

```bash
python -m venv .venv
```

Activate it on Windows:

```bash
.venv\Scripts\activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Configure API Keys

Create a file named `.env` in the project directory and add your API keys.

```env
OPENAI_API_KEY=your_openai_api_key
TAVILY_API_KEY=your_tavily_api_key
```

Replace the placeholder values with your actual API keys. Keep this file private and never upload it to GitHub.

### 5. Run the Application

```bash
streamlit run app.py
```

Once the application starts, open the local URL displayed in the terminal.

## Running the Pipeline Without Streamlit

You can also run the research workflow directly from the terminal.

```bash
python pipeline.py
```

Enter the topic you want to research when prompted. The pipeline will execute the research stages and return the collected information, generated report, and critic feedback.

## Use Cases

This project can be useful for researching technical topics, exploring AI developments, gathering information from web sources, preparing initial research reports, and reviewing generated content.

The generated information should be checked against the original sources because AI responses and web content can sometimes be inaccurate or incomplete.

## Future Improvements

Some improvements to explore include parallel execution of research agents, better source verification, research history, additional export formats, configurable report length, improved error handling, and automated testing.

## Author

**Mohd Anas**

GitHub: [@mohda9as](https://github.com/mohda9as)

Project Repository: [Multi Agent AI Research System](https://github.com/mohda9as/Multi-Agent-AI-Research-System)


