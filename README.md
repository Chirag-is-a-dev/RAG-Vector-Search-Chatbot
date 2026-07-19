#  RAG Chatbot with n8n, Google Gemini, Hugging Face & Pinecone

An end-to-end **Retrieval-Augmented Generation (RAG)** chatbot built with **n8n**, **Google Gemini**, **Hugging Face Embeddings**, and **Pinecone Vector Database**. The system retrieves relevant information from a knowledge base and uses it to generate accurate, context-aware responses.

---

##  Features

-  Website content indexing
-  Semantic embeddings using Hugging Face
-  Vector storage with Pinecone
-  AI-powered responses using Google Gemini
-  Semantic search for relevant document retrieval
-  Workflow automation with n8n
-  Easy integration with web applications

---

##  Architecture

```text
                   Knowledge Base Indexing
┌────────────────────────────────────────────────────┐
│                                                      │
│ Website → Extract Content → Split Documents         │
│        → Hugging Face Embeddings → Pinecone         │
│                                                      │
└────────────────────────────────────────────────────┘

                         │
                         ▼

                 User asks a question

                         │
                         ▼

┌────────────────────────────────────────────────────┐
│                                                      │
│ Chat Interface → n8n AI Agent                        │
│                → Query Embedding                     │
│                → Pinecone Similarity Search           │
│                → Google Gemini                        │
│                → Context-Aware Response               │
│                                                      │
└────────────────────────────────────────────────────┘
```

---

##  Workflows

### Workflow 1 – Knowledge Base Indexing

This workflow prepares documents for semantic search.

**Steps**

- Fetch website content
- Extract readable text
- Split text into optimized chunks
- Generate embeddings using Hugging Face
- Store vectors in Pinecone

**Purpose**

Creates a searchable knowledge base that can be updated whenever website content changes.

---

### 🤖 Workflow 2 – AI RAG Chat Assistant

This workflow answers user questions using Retrieval-Augmented Generation (RAG).

**Steps**

- Receive user query
- Convert query into embeddings
- Perform semantic search in Pinecone
- Retrieve relevant document chunks
- Send retrieved context to Google Gemini
- Generate grounded, context-aware responses

**Purpose**

Reduces hallucinations by allowing the language model to answer using your organization's own knowledge.

---

## 🛠 Tech Stack

| Technology | Purpose |
|------------|---------|
| n8n | Workflow Automation |
| Google Gemini | Large Language Model |
| Hugging Face | Embedding Generation |
| Pinecone | Vector Database |
| HTML / CSS / JavaScript | Chat Interface |
| Firebase Hosting | Website Deployment |

---

##  Workflow Screenshots

### Knowledge Base Indexing

> Add screenshot here

```
images/knowledge-base-workflow.png
```

---

### RAG Chat Workflow

> Add screenshot here

```
images/rag-chat-workflow.png
```

---

##  Project Structure

```text
rag-chatbot-n8n-pinecone-gemini/

├── workflows/
│   ├── knowledge-base-indexing.json
│   └── rag-chat-workflow.json
│
└── README.md
```

---

##  Setup

### 1. Clone Repository

```bash
git clone https://github.com/yourusername/rag-chatbot-n8n-pinecone-gemini.git
```

---

### 2. Configure Credentials

Configure the following services inside n8n:

- Google Gemini API
- Pinecone API
- Hugging Face API

---

### 3. Import Workflows

Import both workflow JSON files into your n8n instance.

---

### 4. Run the Indexing Workflow

Execute the **Knowledge Base Indexing** workflow to populate Pinecone with embeddings.

---

### 5. Start Chatting

Run the **RAG Chat Workflow** and connect it to your frontend or chatbot interface.

---

##  Use Cases

- AI Customer Support
- Internal Knowledge Base
- Company Documentation Assistant
- HR Policy Assistant
- Technical Support Bot
- Website AI Assistant
- Enterprise Search
- FAQ Automation

---

##  Why Retrieval-Augmented Generation (RAG)?

Traditional LLMs rely solely on their training data, which can lead to outdated or inaccurate responses.

RAG improves response quality by retrieving relevant information from your own knowledge base before generating an answer.

### Benefits

-  Reduced hallucinations
-  Up-to-date information
-  Context-aware responses
-  No model retraining required
-  Enterprise-ready architecture

---

##  Contributing

Contributions are welcome!

If you'd like to improve this project, feel free to fork the repository and submit a pull request.

---

##  License

This project is licensed under the MIT License.

---

##  Author

**Chirag Sehgal**

Building intelligent automation solutions with AI.

If you found this project helpful, consider giving it a ⭐ on GitHub!
