🦉Conversational SupportChatBot (RAG + Ollama + n8n)

🚀 Medical Insurance Support Optimization via AI and Automation
This repository contains an advanced workflow developed in n8n that implements a conversational AI Agent designed to manage inquiries regarding medical insurance policies for the National Electoral Council (CNE).

📋 Project Description
The system utilizes a Retrieval-Augmented Generation (RAG) architecture to ensure that the bot's responses are not only natural but technically accurate and based exclusively on official policy documentation.

🛠️ Tech Stack
Orchestrator: n8n.

Local AI: Ollama (Llama 3.1:8b model).

Vector Database: Supabase (Vector Store).

Text Processing: Recursive Character Text Splitter.

Embeddings: bge-m3:567m (for high efficiency in relational searches).

Channels: Telegram (User Interface) and Google Drive (Document Ingestion).

⚙️ Key Features
RAG Architecture (Retrieval-Augmented Generation): The bot queries a vector database in Supabase to retrieve relevant policy fragments before generating a response, effectively eliminating hallucinations.

Automated Document Processing: Includes a Google Drive trigger that detects new PDF files, chunks them (text splitting), and automatically indexes them into the vector database.

Contextual Memory: Implementation of memory nodes to maintain conversational flow and understand previous user references.

Intelligent Escalation (Human-in-the-loop): Integrated conditional logic (If/Switch) to detect output errors or complex queries, automatically notifying a human agent via Telegram.

Privacy and Cost-Efficiency: By using Ollama locally, the system guarantees the privacy of sensitive employee data and reduces inference token costs to zero.

🛠️ Configuration and Installation
n8n: Import the .json file included in this repository.

Ollama: Ensure Ollama is running locally with the llama3.1 and embedding models configured.

Supabase: Create a vector table and configure your credentials in the Supabase Vector Store node.

Telegram: Create a bot via @BotFather and add the token to the "Telegram Trigger" node.

Google Drive: Configure Google Cloud credentials for document ingestion.

📊 Impact and Results
Availability: 24/7 technical and administrative support.

Efficiency: Reduced response time for medical coverage inquiries from minutes to seconds.

Reliability: Minimized interpretation errors by using relational embeddings for precise searches.

Developed by: Victor Batista

Full Stack & Automation Engineer specialized in process optimization.
