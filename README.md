# GSoC 2024: Implementation of RAG Pipelines using Apache Beam

Project Link : 

1) https://github.com/apache/beam/pull/31657
2) https://github.com/apache/beam/pull/32018

Project Overview: 

Building out data ingestion and enrichment pipeline for a Retrieval Augmented Generation (RAG) system using Apache Beam.
This repository contains the implementation of Retrieval-Augmented Generation (RAG) pipelines using Apache Beam, developed as part of the Google Summer of Code (GSoC) 2024 project. The goal of this project is to demonstrate the capabilities of Apache Beam for building semantic search-based applications by implementing data pipelines that create a knowledge base and enrich user queries using vector databases.

Key Features:
Batch Text Corpus Ingestion: Indexing text data from a public dataset (Wikipedia) using sentence-transformers/all-MiniLM-L6-v2 embeddings.
Knowledge Base Construction: Storage of embeddings in vector databases such as Redis Vector DB and OpenSearch.
Query Enrichment: Enrichment of user queries by retrieving semantically related text chunks from the knowledge base using custom enrichment handlers for Redis and OpenSearch.
Chunking Strategies: Implementation of various chunking strategies such as split_by_character, recursive_split_by_character, and split_by_tokens using LangChain’s library.
Project Structure
Pipeline 1: Ingestion, Indexing and chunking
Reads a batch text corpus.
Generates embeddings using the SentenceTransformerEmbeddings module.
Writes embeddings to a vector database (Redis/OpenSearch).
Pipeline 2: Query Enrichment
Reads user queries/prompt as an input.
Enriches queries with relevant text chunks from the vector database using semantic search.
returns the matching document/chunks

