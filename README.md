
# RAG — Retrieval-Augmented Generation

**A notebook-based implementation exploring document ingestion, semantic retrieval, vector databases, and LLM-powered response generation.**

This project explores the core components of a Retrieval-Augmented Generation pipeline.

The implementation demonstrates how documents can be loaded, divided into chunks, converted into embeddings, indexed in a vector store, and retrieved to provide contextual information to a language model.

## Pipeline Architecture

```text
PDF / Text Documents
        |
        v
Document Loading
        |
        v
Text Chunking
        |
        v
Embedding Generation
        |
        v
ChromaDB Vector Store
        |
        v
Semantic Retrieval
        |
        v
Context Construction
        |
        v
Gemini LLM
        |
        v
Generated Response
```

## Technology Stack

### Language
- Python

### Document Processing
- LangChain document loaders
- PyMuPDF
- PyPDF

### Embeddings
- Sentence Transformers
- all-MiniLM-L6-v2

### Vector Database
- ChromaDB

### Language Model
- Google Gemini API

### Additional Libraries
- NumPy
- scikit-learn
- Pandas
- Python dotenv

## Implemented Components

### Document Ingestion
- Text document loading
- PDF document loading
- Directory-based document ingestion
- Document metadata handling

### Text Processing
- Recursive character text splitting
- Configurable chunk size
- Chunk overlap

### Embedding Management
- Sentence Transformer model loading
- Batch embedding generation
- Embedding dimension inspection

### Vector Storage
- Persistent ChromaDB client
- Collection management
- Document and embedding storage

### Retrieval
- Query embedding generation
- Similarity-based retrieval
- Top-K document retrieval
- Similarity threshold filtering
- Source metadata retrieval

### Response Generation
- Gemini integration
- Context-aware prompts
- Retrieved-context-based answer generation

## Repository Structure

```text
RAG/
├── data/
│   ├── pdf/
│   ├── text_files/
│   └── vector_store/
│
├── notebook/
│   └── document.ipynb
│
├── main.py
├── pyproject.toml
└── README.md
```

## Setup

The project dependencies are declared in `pyproject.toml`.

Install using pip:

```bash
pip install -e .
```

Configure your Gemini API key:

```env
GEMINI_API_KEY=your_api_key
```

## Running the Project

The current RAG implementation is in the notebook:

```bash
jupyter lab notebook/document.ipynb
```

Execute the notebook cells in order to load documents, generate embeddings, populate the vector store, retrieve relevant chunks, and generate responses.

**Note:** `main.py` is currently a placeholder and does not execute the RAG pipeline.

## Current Limitations

- The main Python entry point is not implemented.
- The pipeline is currently notebook-driven.
- Retrieval evaluation and benchmarking are not yet established.
- Retrieval confidence should not be interpreted as calibrated answer confidence.
- Source citation and grounded-response verification need further development.

## Future Work

- Modular Python pipeline
- Configurable document ingestion
- Hybrid retrieval
- Metadata filtering
- Reranking
- Retrieval evaluation
- Grounded citations
- Streaming responses
- Automated tests

## License

See the repository license information.
