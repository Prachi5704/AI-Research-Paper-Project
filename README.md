# AI Research Paper Intelligence System

An AI-powered system to semantically search, summarize, and analyze research papers using NLP and Deep Learning. Retrieves relevant papers, generates concise summaries, extracts keywords/entities, classifies research domains, answers questions, recommends similar papers, and supports custom PDF uploads.

## Features

- **Semantic Search** — Sentence Transformers (MiniLM) + FAISS for cosine-similarity based retrieval.
- **Abstractive Summarization** — BART (facebook/bart-large-cnn) for concise summaries.
- **Keyword Extraction** — KeyBERT for key phrase extraction.
- **Named Entity Recognition** — spaCy for identifying entities in text.
- **Zero-Shot Topic Classification** — BART-MNLI for domain classification without training.
- **Question Answering** — DistilBERT for extractive QA on paper abstracts.
- **Citation Recommender** — Finds similar papers via embedding similarity.
- **Custom PDF Analysis** — Upload any research paper PDF (via pdfplumber) for on-the-fly analysis.

## Tech Stack

- Python, Pandas
- Sentence Transformers, FAISS
- Hugging Face Transformers (BART, DistilBERT)
- KeyBERT, spaCy
- pdfplumber

## Workflow

1. Load research paper dataset (ML-ArXiv-Papers, 15,000 papers).
2. Generate embeddings using Sentence Transformers.
3. Build a FAISS index for fast semantic search.
4. Retrieve top-k relevant papers for a query.
5. Summarize abstracts using BART.
6. Extract keywords (KeyBERT) and entities (spaCy).
7. Classify papers into research domains (Zero-Shot).
8. Answer questions using DistilBERT QA.
9. Recommend similar papers via embedding similarity.
10. Optionally upload and analyze a custom PDF paper.

## Installation

\`\`\`bash
pip install -r requirements.txt
python -m spacy download en_core_web_sm
\`\`\`

