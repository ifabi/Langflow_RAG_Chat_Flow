# Langflow_RAG_Chat_Flow
RAG - Using a simple pdf input

Astra DB Configuration
----------------------------------------
Vector Database: DataStax Astra DB
Database: langflow-db
Collection: collection_name1
Embedding Model: text-embedding-3-small
Embedding Dimension: 1536
Similarity: Cosine


Reconstruction Process
--------------------------------------------
Clone repo
    ↓
Install dependencies
    ↓
Configure .env / Global Variables
    ↓
Create/connect Astra collection
    ↓
Import restaurant-rag-agent.json
    ↓
Upload Restaurant Q&A.pdf
    ↓
Run ingestion
    ↓
Use RAG chatbot


Architecture
--------------------------------------------------
Restaurant PDF
      ↓
Read File
      ↓
Split Text
      ↓
OpenAI Embeddings
      ↓
Astra DB
      │
      │ vector retrieval
      ↓
Parser
      ↓
Prompt Template
      ↑
Message History
      ↓
GPT-4o-mini
      ↓
Chat Output
      ↓
Message History Store