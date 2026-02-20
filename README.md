# Strategic Intelligence Ranking Engine (RAG-Based)

A Retrieval-Augmented Generation (RAG) system that integrates quantitative financial metrics with qualitative AI initiative signals to rank organizations by growth trajectory and innovation readiness.

## Problem Context

Traditional investment analysis emphasizes numerical indicators such as market capitalization, revenue, and stock performance. While these metrics reflect current financial momentum, they often overlook qualitative signals related to long-term innovation and AI adoption.

Strategic documents contain valuable forward-looking insights, yet they are unstructured and difficult to integrate systematically with financial metrics.

This project bridges that gap by combining structured financial data with document-grounded reasoning using Retrieval-Augmented Generation (RAG).

## System Overview

The system integrates:

- Financial metrics retrieved via yfinance

- AI initiative documents (PDF ingestion)

- Recursive text chunking

- Embedding generation

- Chroma vector store for semantic retrieval

- LLM-based reasoning grounded in retrieved evidence

- Integrated ranking logic across quantitative and qualitative signals

## Architecture Components
1. Financial Signal Extraction

  - Market metrics such as market cap, P/E ratio, dividend yield, beta, and revenue are programmatically retrieved.

2. Document Processing Pipeline

  - PDF ingestion

  - Text splitting (RecursiveCharacterTextSplitter)

  - Embedding generation

  - Vector indexing using Chroma

3. Retrieval-Augmented Reasoning

  - The LLM generates responses grounded in semantically retrieved document chunks.

4. Integrated Ranking Output

  - Organizations are ranked using a combined evaluation of financial strength and innovation readiness.

## How to Run

1. Install dependencies:

> pip install -r requirements.txt

2. Set your OpenAI API key.

> On macOS/Linux:
>> export OPENAI_API_KEY="your-api-key"

> On Windows:
>> setx OPENAI_API_KEY "your-api-key"

> Alternatively, the notebook will prompt for the key if not already set.

3. Ensure required PDF documents are placed in the expected directory (see Data Setup below).

4. Run the notebook top-to-bottom.

## Data Setup

This project expects a directory containing PDF documents describing organizational AI initiatives.

Create the following structure:

Companies-AI-Initiatives/
├── company_a_ai_strategy.pdf
├── company_b_innovation_report.pdf
└── company_c_ai_overview.pdf

If running locally, update the PDF_DIR variable in the notebook accordingly.

## Future Improvements

- Add automated evaluation metrics for ranking robustness

- Introduce persistent embedding storage

- Implement structured score normalization

- Convert notebook into modular Python package architecture

