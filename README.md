# legal-rag-pipeline

A retrieval-augmented generation (RAG) pipeline that answers questions about legal contracts, built with LangChain and a Chroma vector store.

Given a question, the system retrieves the most relevant passages from a set of legal documents and asks a language model to answer using only those passages, so the answers stay grounded in the source material. The notebook also compares the RAG answers against a plain LLM-only baseline, to show where retrieval reduces hallucinations and unsupported claims.

## What it does

- Loads and explores the legal documents
- Splits them and builds a vector store with embeddings (Chroma)
- Retrieves the passages most relevant to a query
- Generates grounded answers with a LangChain RAG chain
- Compares LLM-only and RAG answers on accuracy and faithfulness

## Files

- `legal_rag_pipeline.ipynb` — the full pipeline, with explanations and outputs

## Running it

The notebook uses an OpenAI model through LangChain. Set your own key where indicated (`api_key = "your_api_key"`) to run it end to end. All outputs are already saved in the notebook, so you can also just read through it.
