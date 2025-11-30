# Clinical RAG System with MIMIC-IV-Ext

This repository contains a Retrieval-Augmented Generation (RAG) system for answering clinical queries using the MIMIC-IV-Ext Direct dataset. The system retrieves relevant clinical notes and generates context-aware, coherent responses using a language model.

## Overview

The Clinical RAG system leverages dense retrieval and LLM-based generation to answer queries such as:

What are the symptoms of Type I Diabetes?

Which patients have hypertension as a symptom?

Describe clinical assessments for Alzheimer patients.

## Key components:

### Retriever
FAISS-based dense retrieval of relevant chunks from clinical notes.

### Generator
Instruction-following LLM (e.g., Nous-Hermes-2-Mistral-7B-DPO) that generates coherent, context-aware responses.

### RAG Pipeline
Combines retrieval + generation for seamless query answering.

### Frontend
Gradio interface for interactive exploration.

## Features

Chunk-based retrieval of clinical notes using embeddings.

Instruction-guided LLM generation of diagnostic explanations.

Retrieval evaluation with precision and recall metrics.

Ground truth construction for retrieval and generation evaluation.

Interactive Gradio frontend.

## Dataset

This project uses the MIMIC-IV-Ext Direct dataset:

Contains structured and unstructured clinical notes.

Includes diagnostic labels, risk factors, symptoms, and assessments.

Preprocessing: Notes are split into chunks and embedded for retrieval.

⚠️ Dataset contains sensitive medical information. This project is for research and educational purposes only. Do not expose or share patient-identifiable data.

## Installation Requirements

Python 3.10+

PyTorch 2.x

Transformers

HuggingFace Datasets & Tokenizers

FAISS

Gradio

BitsAndBytes (for 4-bit quantization if using Mistral-Hermes)

```
git clone https://github.com/Maham-1234/rag-Diagnostic-DiReCT.git
cd rag-Diagnostic-DiReCT
```

## Frontend

The system includes a Gradio interface for interactive querying:

Users enter clinical questions

Top retrieved chunks are displayed

Generated answers are shown alongside retrieved context

## Ethical Considerations

Only for research and educational purposes.

Do not expose patient-identifiable information.

Outputs are not clinical advice and should not be used for real-world diagnosis.

Ensure adherence to HIPAA and institutional privacy regulations.
