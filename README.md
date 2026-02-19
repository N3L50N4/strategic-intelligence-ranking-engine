# Strategic Intelligence Ranking Engine (RAG-Based)

## Overview
A Retrieval-Augmented Generation (RAG) system that integrates quantitative financial trends with qualitative strategic insights from company documents to rank organizations by growth trajectory and innovation readiness.

## Key Features
- Stock trend signals (e.g., Yahoo Finance)
- PDF/document retrieval with RAG
- LLM-based reasoning grounded in retrieved evidence
- Ranking output based on combined quantitative + qualitative signals

## How to Run
Open the notebook and run cells top-to-bottom.
If API keys are required, set them via environment variables (recommended).

## Future Improvements
- Add automated evaluation metrics
- Add persistent storage for embeddings
- Convert notebook into modular Python package

## Data Setup

This project expects a directory containing PDF documents describing organizational AI initiatives.

To run the notebook locally or in Colab:

1. Create a folder named `Companies-AI-Initiatives/`
2. Place PDF documents (one per organization) inside this folder
3. Update the notebook path if running outside Colab

Example structure:

Companies-AI-Initiatives/
├── company_a_ai_strategy.pdf
├── company_b_innovation_report.pdf
└── company_c_ai_overview.pdf

For demonstration purposes, any publicly available AI-related corporate reports can be used.


