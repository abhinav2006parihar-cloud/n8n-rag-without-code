# RAG Without Code using n8n

## Project Overview

This project implements a simple Retrieval-Augmented Generation (RAG) Agent using n8n, Google Gemini, and Supabase Vector Store.

The system retrieves relevant information from a PDF knowledge document and uses it as context to generate grounded AI responses.

## RAG Pipeline

Document → Extract → Embed → Store → Retrieve → Context → Generate Answer

## Workflows

### Workflow 1 — Document Indexing
- Reads the PDF from local disk
- Extracts PDF content
- Generates embeddings using Google Gemini
- Stores document vectors in Supabase

### Workflow 2 — RAG Question Answering
- Receives a natural-language question through n8n Chat
- Searches the Supabase Vector Store
- Retrieves relevant document context
- Uses Google Gemini to generate the answer
- Avoids inventing information when the answer is unavailable

## Technologies Used

- n8n
- Google Gemini
- Supabase Vector Store
- PDF
- No-code/low-code workflow

## Sample Test

**Question:** How many days can employees work from home?

**Answer:** Employees can work from home up to 2 days per week, subject to manager approval.

## Project Files

- `Workflow 1` — Document Indexing
- `Workflow 2` — RAG Question Answering
- Sample PDF knowledge document
- Workflow screenshots

## Security

API credentials are stored inside n8n and are not included in the repository.

## Outcome

The project demonstrates the complete RAG pipeline:

**Document → Index → Search → Retrieve → Context → Generate → Answer**
