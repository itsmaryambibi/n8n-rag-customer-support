# n8n-rag-customer-support
RAG-powered customer support chatbot built with n8n, OpenAI, and Pinecone.
# RAG-Powered Customer Support Chatbot

An AI-powered customer support chatbot built using **n8n, OpenAI, and Pinecone**. This project uses Retrieval-Augmented Generation (RAG) to retrieve relevant information from stored documents and generate context-aware responses to customer queries.

## Project Overview

This project demonstrates how to build a RAG-based customer support system using three interconnected n8n workflows.

Instead of relying only on an AI model's general knowledge, the chatbot retrieves relevant information from a Pinecone vector database to provide more relevant answers.

## Workflows Included

### 1. Create Pinecone Index
Creates a Pinecone vector index to store and retrieve document embeddings.

### 2. Insert Documents into Pinecone
Accepts documents, processes their content, generates embeddings using OpenAI, and stores them in Pinecone.

### 3. RAG-Powered Customer Support
Receives customer questions through an n8n chat trigger, retrieves relevant information from Pinecone, and uses an OpenAI-powered AI Agent to generate responses.

## Technologies Used

- n8n – Workflow automation
- OpenAI – Language models and embeddings
- Pinecone – Vector database
- Retrieval-Augmented Generation (RAG) – Knowledge retrieval

## Workflow Architecture

**Document Ingestion:**

Documents → Data Loader → OpenAI Embeddings → Pinecone Vector Store

**Customer Support:**

Customer Query → Chat Trigger → AI Agent → Pinecone Retrieval → AI Response

## Setup Requirements

Before running the workflows, you need:

- An n8n account or self-hosted n8n instance
- An OpenAI API account
- A Pinecone account

Configure your OpenAI and Pinecone credentials inside n8n before executing the workflows.

## How to Use

1. Create a Pinecone index using the first workflow.
2. Upload and insert your documents using the second workflow.
3. Open the customer support workflow.
4. Configure the required credentials and Pinecone index.
5. Activate or execute the workflow and test the chatbot.

## Security

API keys and passwords should be stored using n8n Credentials. Never publish actual API keys, passwords, or access tokens in workflow JSON files.

## Project Purpose

This project was built as a practical learning project to understand RAG architecture, vector databases, AI agents, embeddings, and workflow automation using n8n.

## Author

Maryam Bibi
