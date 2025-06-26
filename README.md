# Building Multi-Agentic AI RAG With Vector Database

This project implements a multi-agent Retrieval Augmented Generation (RAG) system leveraging vector databases to enable intelligent PDF document assistance. The assistant can ingest, embed, and search content from PDFs using state-of-the-art language models and vector storage, making it easy to extract, query, and interact with knowledge from documents.

## Features

- **PDF Knowledge Base**: Load and index PDF files for semantic search and retrieval.
- **Vector Database Integration**: Utilizes PostgreSQL with `pgvector` for scalable, efficient vector storage.
- **Multi-Agent Architecture**: Built on modular agents capable of running advanced LLMs (e.g., Groq's Llama-3) for reasoning and question answering.
- **Pluggable Embedding Models**: Supports HuggingFace and SentenceTransformer-based embedders.
- **Command Line Interface**: Interact with the assistant through a user-friendly CLI.
- **Chat History and Tool Use**: Remembers conversations and can call tools for extended functionalities.
- **Environment Configuration**: Uses `.env` for secure configuration of secrets and database URLs.

## Installation

1. **Clone the Repository**
   ```bash
   git clone https://github.com/KUHELI08/Building-Multi-Agentic-AI-RAG-With-Vector-Databse.git
   cd Building-Multi-Agentic-AI-RAG-With-Vector-Databse
   ```

2. **Install Dependencies**
   Make sure you have Python 3.8+ and PostgreSQL with `pgvector` extension installed. Then install requirements:
   ```bash
   pip install -r requirements.txt
   ```

3. **Set Up Environment Variables**
   Create a `.env` file in the project root with your configuration (e.g., database URL).

4. **Configure Database**
   Ensure PostgreSQL is running and the `pgvector` extension is enabled. Update the `db_url` in `pdf_assistant.py` or `.env` as needed.

## Usage

Run the PDF Assistant via the command line:
```bash
python pdf_assistant.py
```

- The assistant will load the configured PDF(s) into the vector database.
- It uses a powerful LLM (like Llama-3 via Groq) to answer questions about the document.
- All interactions are via a CLI with markdown support.

## Requirements

See `requirements.txt` for all dependencies, including:
- `phidata`
- `python-dotenv`
- `yfinance`
- `duckduckgo-search`
- `fastapi`, `uvicorn`
- `groq`, `openai`
- `sqlalchemy`, `pgvector`, `psycopg[binary]`
- `pypdf`
- `huggingface-hub`

## Customization

- **Change PDF Source**: Edit the `urls` parameter in `pdf_assistant.py` to use your own PDFs.
- **Update Embedding Model**: Swap the embedder to another supported model for different vectorization strategies.
- **Expand Agents**: Add or modify agent behaviors in the source code to suit your use case.

## License

This project is for educational and research purposes. Please add an open-source license if you intend to share or deploy it publicly.

## Contributing

Pull requests and suggestions are welcome! Please open an issue to discuss your ideas.

---

**Repository:** [KUHELI08/Building-Multi-Agentic-AI-RAG-With-Vector-Databse](https://github.com/KUHELI08/Building-Multi-Agentic-AI-RAG-With-Vector-Databse)
