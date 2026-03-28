# Idea 4: Legal Research & Document Assistant

## Overview
Build an OpenClaw skill that ingests legal documents, case files, or contracts and allows lawyers and paralegals to query them in plain language, get summaries, flag risks, and generate first-draft clauses — all running locally for maximum confidentiality.

## Problem It Solves
Legal professionals deal with enormous volumes of documents. Existing AI tools raise data-privacy concerns when they upload sensitive documents to third-party servers. OpenClaw enables the same AI capabilities on-premises, keeping client data private.

## Core Features
- **Document Ingestion**: Drop PDFs or DOCX files into a watched folder; OpenClaw automatically indexes them into a local vector database.
- **Natural Language Q&A**: "What are the termination clauses in the NDA with Acme Corp?" → retrieves and cites the relevant section.
- **Risk Flagging**: Automatically highlight unusual or potentially unfavourable clauses compared to a set of standard templates.
- **Summary Generation**: Produce a one-page executive summary of any contract on demand.
- **Clause Drafting**: "Draft a non-compete clause valid in the Netherlands" → generates a first draft with jurisdiction-aware language.

## Tech Stack
- OpenClaw skill with file-watcher and vector DB (ChromaDB, Qdrant — local)
- PDF/DOCX parsing (pypdf, python-docx)
- RAG pipeline with local LLM (Ollama + Mistral or Llama 3)
- Telegram or WhatsApp interface

## Stretch Goals
- Multi-document comparison ("How do these two contracts differ in liability terms?")
- Integration with Dutch/EU legal databases via web scraping
- Audit log of all queries for compliance purposes

## Why It's Great for a Hackathon
Combines RAG, local LLMs, and a real-world use case in a domain (legal) where privacy is paramount. The privacy angle is a compelling differentiator from cloud-based alternatives.
