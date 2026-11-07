# AI-Powered Insurance Claims Processing Assistant

## Project Overview

This project demonstrates an AI-powered Insurance Claims Processing Assistant built using Python, Large Language Models (LLMs), Pydantic, and Retrieval-Augmented Generation (RAG).

The application processes customer insurance claim emails, extracts structured information, validates the extracted data, and evaluates claim coverage based on a fictional insurance policy document.

## Problem Statement

Insurance claim emails often contain unstructured information. Manually extracting customer details, validating claim information, and checking policy coverage can be time-consuming.

This project explores how GenAI and RAG can help automate these steps.

## Architecture / Workflow

Customer Email  
↓  
LLM-Based Information Extraction  
↓  
Pydantic Structured Output  
↓  
Python Data Validation  
↓  
Policy Document Retrieval (RAG)  
↓  
LLM-Based Coverage Evaluation  
↓  
Final Claim Assessment

## Features

### 1. Structured Information Extraction
- Extract customer name and policy number.
- Identify incident date and location.
- Extract incident description.
- Capture claim amount and supporting documents.
- Categorize claims into Health, Vehicle, Home, or Other.

### 2. Data Validation
- Validate policy number.
- Check claim amount.
- Verify supporting documents.
- Identify incomplete claims requiring manual review.

### 3. Retrieval-Augmented Generation (RAG)
- Load the insurance policy document.
- Split the document into chunks.
- Generate embeddings.
- Store embeddings in a vector database.
- Retrieve relevant policy clauses using semantic similarity search.

### 4. Coverage Evaluation

The application evaluates claims against the retrieved policy information.

Possible outcomes:
- Covered
- Not Covered
- Not Specified
- Manual Review

### 5. Hallucination Control
- Evaluate claims using retrieved policy context.
- Avoid relying on general insurance knowledge.
- Provide policy-based explanations and supporting evidence.

## Technology Stack

- Python
- Pydantic
- Large Language Models (LLMs)
- JSON Schema Structured Outputs
- Embeddings
- Vector Database
- Retrieval-Augmented Generation (RAG)

## Test Scenarios

The project uses fictional customer emails covering:

1. Sudden water pipe burst.
2. Gradual water leakage.
3. Household theft without forced entry.
4. Accidental fire caused by an electrical short circuit.
5. Earthquake damage.
6. Claim submitted without supporting documents.

## Key Learnings

- Extracting structured information from unstructured text.
- Working with Pydantic models and JSON Schema.
- Implementing business validation using Python.
- Understanding document chunking and embeddings.
- Building a semantic search pipeline.
- Connecting LLMs with retrieved context.
- Evaluating AI responses against predefined business rules.

## Future Improvements

- Build a complete end-to-end `process_claim()` pipeline.
- Add robust exception handling and logging.
- Improve retrieval quality and evaluation.
- Add claim-level audit trails.
- Build an interactive user interface.
- Explore AI agent integration.

## Disclaimer

This is a learning project built using fictional insurance policy data. It is not intended for real insurance claim decisions or approvals.
