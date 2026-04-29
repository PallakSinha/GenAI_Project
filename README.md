# AI-Powered Order Analytics Chatbot (RAG)

📌 Overview
This project builds an intelligent Order Analytics Chatbot using Retrieval-Augmented Generation (RAG). It allows users to query order data in natural language and receive context-aware, AI-generated responses.

The system combines:
- Semantic search using embeddings
- Fast similarity retrieval using FAISS
- Response generation using Google Gemini

### Key Features
📄 Extracts structured data from PDF files
🧠 Converts tabular data into natural language
🔍 Semantic search using embeddings (not keyword-based)
⚡ Fast retrieval with FAISS indexing
💬 Conversational AI interface powered by Gemini
📊 Provides intelligent insights from order data

### Tech Stack
Python
Sentence Transformers (for embeddings)
FAISS (vector similarity search)
Google Gemini API (LLM)
Tabula-py (PDF table extraction)
Pandas

### How It Works
1. Data Extraction
Extract tables from PDF using tabula-py
Convert into a structured DataFrame
2. Text Conversion
Each row is transformed into a readable sentence
Example:
Order ID 101 belongs to John and is delivered.
3. Embedding Generation
Sentences are converted into vector embeddings using Sentence Transformers
4. Vector Storage
Embeddings are stored in FAISS for efficient similarity search
5. Query Processing
User query → converted to embedding
FAISS retrieves top relevant records
6. Response Generation
Retrieved context + query → sent to Gemini
Gemini generates final response

###📂 Project Structure
├── GenAI_Project.ipynb   # Main implementation notebook
├── data/                 # Input PDF files
├── README.md             # Project documentation

### How to Run
1. Clone Repository
git clone https://github.com/your-username/order-analytics-chatbot.git
cd order-analytics-chatbot
2. Install Dependencies
pip install pandas tabula-py sentence-transformers faiss-cpu google-generativeai
3. Add API Key
import google.generativeai as genai
genai.configure(api_key="YOUR_API_KEY")
4. Run Notebook
Open:
GenAI_Project.ipynb
💬 Example Queries
"Who placed order 102?"
"List all orders of CustomerName"

### Output

The chatbot retrieves relevant order data and generates a natural language response based on context.

## Conclusion

This project demonstrates how Generative AI + Semantic Search can transform static datasets into interactive, intelligent systems for data analysis.
