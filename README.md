# NexusRAG - n8n Multi-Agent AI Assistant

NexusRAG is an advanced multi-agent AI assistant built using n8n. The system intelligently analyzes user requests and routes them to specialized AI agents for web research, Retrieval-Augmented Generation (RAG), general assistance, and automation-related tasks.

## Workflow Architecture

Telegram Trigger → Supervisor Agent → Switch Router → Specialized AI Agents → Telegram Response

The Supervisor Agent classifies incoming user requests into four routes:

- Research Agent
- RAG Agent
- General Agent
- Automation Agent

## Features

- Intelligent AI request routing
- Multi-agent architecture
- Real-time web research using Tavily API
- Retrieval-Augmented Generation (RAG)
- Supabase Vector Store integration
- Google Gemini embeddings
- PDF document ingestion pipeline
- Semantic document search
- Telegram bot integration
- Specialized AI agents
- Modular n8n workflow architecture

## Agents

### Supervisor Agent

Analyzes each incoming Telegram message and routes it to the appropriate specialized agent.

### Research Agent

Searches the web using the Tavily API and generates answers based on current information.

### RAG Agent

Retrieves relevant information from documents stored in the Supabase Vector Store and generates context-grounded answers.

### General Agent

Handles general questions, explanations, coding assistance, brainstorming, and normal conversations.

### Automation Agent

Handles automation-related questions, workflow design, API integrations, and n8n troubleshooting.

## RAG Document Ingestion Pipeline

The project includes a separate document ingestion workflow.

Google Drive → Default Data Loader → Text Chunking → Google Gemini Embeddings → Supabase Vector Store

Documents are processed into chunks, converted into vector embeddings, and stored in Supabase for semantic retrieval.

## Technologies Used

- n8n
- OpenRouter
- Google Gemini Embeddings
- Supabase
- pgvector
- Tavily API
- Telegram Bot API
- Retrieval-Augmented Generation (RAG)
- Multi-Agent AI Architecture

## Repository Structure

n8n-multi-agent-rag-assistant/

├── workflows/
│   ├── multi-agent-telegram-assistant.json
│   └── rag-document-ingestion.json
│
├── sample-documents/
│   └── ai-automation-knowledge-base.pdf
│
├── README.md
├── .gitignore
└── LICENSE

## How It Works

1. A user sends a message through Telegram.
2. The Supervisor Agent analyzes the request.
3. The Switch node routes the request to the appropriate specialized agent.
4. The selected agent processes the request using its connected tools.
5. The Research Agent can access current web information using Tavily.
6. The RAG Agent retrieves relevant knowledge from Supabase.
7. The General and Automation Agents handle their specialized tasks.
8. The generated response is sent back to the user through Telegram.

## Author

Mekala Rushi Kumar

B.Tech Computer Science and Engineering student interested in AI, AI automation, agentic systems, RAG, and intelligent workflow development.
