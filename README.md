# Telecom Contract Analyzer — Multi-Tool RAG Agent
## What it does
Upload any telecom managed services agreement and query it conversationally using three AI-powered capabilities:
- **Clause Finder** — extracts SLA terms, penalties, pricing, and dates with exact section references
- **Risk Analyzer** — flags unfavourable terms and rates risk as High/Medium/Low
- **Compliance Checker** — validates alignment with UAE PDPL, TRA standards, and data sovereignty

## Tech Stack
- **n8n** — workflow orchestration (no-code)
- **Groq (Qwen 3.8-27B)** — LLM for intelligent responses
- **HuggingFace** — text embeddings for semantic search
- **In-Memory Vector Store** — document chunking and retrieval (RAG)

## How it works
1. Upload a telecom contract PDF via form trigger
2. PDF is chunked, embedded, and stored in vector store
3. Ask questions via chat — the agent selects the right tool and answers from the document only

## How to run
1. Import the `.json` file into your n8n instance
2. Add your Groq and HuggingFace API keys
3. Upload a contract PDF and start querying
