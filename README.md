# ResearchPilot – AI-Powered Academic Research Assistant

ResearchPilot is an intelligent academic research assistant designed to simplify scientific literature exploration and research analysis. It combines local PDF document processing, semantic retrieval, external academic paper discovery, and Large Language Model (LLM) synthesis to generate evidence-based answers to research questions.

Built using Python, Gradio, ChromaDB, Sentence Transformers, OpenAlex API, and OpenAI, ResearchPilot provides an interactive platform for exploring academic documents and discovering relevant scientific publications.

## Key Features

- **PDF Document Upload:** Upload academic research papers in PDF format.
- **Semantic Search:** Retrieve relevant information from uploaded documents using vector embeddings.
- **Retrieval-Augmented Generation (RAG):** Generate context-aware research answers grounded in retrieved evidence.
- **Academic Literature Discovery:** Search academic publications through the OpenAlex API.
- **AI-Powered Research Synthesis:** Use OpenAI language models to generate structured academic responses.
- **Source Citations:** Reference retrieved evidence using citation identifiers such as `[L1]` and `[E1]`.
- **Multiple Research Modes:** Choose between Local PDF, External Papers, and Combined research.
- **Persistent Vector Storage:** Store indexed document chunks using ChromaDB.

## Technology Stack

| Technology | Purpose |
|---|---|
| Python | Core application development |
| Gradio | Interactive web interface |
| PyMuPDF | PDF text extraction |
| ChromaDB | Vector database |
| Sentence Transformers | Text embedding generation |
| OpenAI API | AI-powered research synthesis |
| OpenAlex API | Academic literature discovery |
| Requests | External API communication |

## How It Works

1. Upload an academic PDF document.
2. ResearchPilot extracts text from the PDF.
3. The extracted text is divided into overlapping chunks.
4. Sentence Transformers converts the chunks into vector embeddings.
5. ChromaDB stores the embeddings for semantic retrieval.
6. Enter a research question.
7. ResearchPilot retrieves relevant document passages and/or searches OpenAlex.
8. The retrieved evidence is supplied to an OpenAI language model.
9. The application generates a research response with evidence references.

## Research Modes

- **Local PDF:** Search uploaded academic documents and generate evidence-based answers.
- **External Papers:** Discover relevant academic publications using OpenAlex bibliographic metadata.
- **Combined:** Combine local document retrieval with external academic literature discovery.

## Installation

Clone the repository:

```bash
git clone https://github.com/YOUR_USERNAME/ResearchPilot.git
cd ResearchPilot
```

Install dependencies:

```bash
pip install gradio pymupdf chromadb requests openai sentence-transformers
```

Set your OpenAI API key:

```bash
export OPENAI_API_KEY="your_api_key"
```

Optional OpenAlex email configuration:

```bash
export OPENALEX_EMAIL="your_email@example.com"
```

Run the application:

```bash
python app.py
```

Open the local Gradio URL displayed in your terminal.

## Configuration

The application currently supports:

- Maximum PDF size: 25 MB
- Maximum PDF pages: 200
- Text chunk size: 450 words
- Chunk overlap: 50 words
- Local retrieval: Up to 6 relevant chunks
- External literature search: Up to 6 papers by default
- Embedding model: `all-MiniLM-L6-v2`
- LLM: `gpt-4o-mini`

## Important Notes

- External OpenAlex results currently provide bibliographic metadata only, not full-text scientific findings.
- AI-generated responses should be checked against the original academic publications.
- Scanned PDFs without extractable text are not currently supported.
- On free Hugging Face Spaces, local vector database storage may be temporary.

## Project Purpose

ResearchPilot aims to make academic research more accessible and efficient by bringing document intelligence, semantic retrieval, and AI-assisted literature discovery together in one platform.

## License

Add an appropriate open-source license before distributing or reusing this project.
