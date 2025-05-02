🧠 Legal-RAG: AI-Powered Legal Query Assistant
A domain-specific Retrieval-Augmented Generation (RAG) system that uses a fine-tuned LLaMA 3.2B model to provide context-rich answers to legal queries. Built with Unsloth, ChromaDB, and MiniLM embeddings, this project is tailored for handling complex legal conversations and document retrieval.

🚀 Features
🔧 Fine-tuned LLaMA 3.2B with LoRA on legal case conversations using unsloth

📄 Context-aware question answering using ChromaDB and Sentence Transformers (MiniLM)

🧠 Retrieval-Augmented Generation pipeline that combines embedding-based retrieval with generative AI

💬 Chat-style prompt formatting with HuggingFace chat templates for cleaner responses

🏗️ Tech Stack
Transformers (HuggingFace)

unsloth for efficient fine-tuning

ChromaDB for vector storage and retrieval

sentence-transformers (MiniLM-L6-v2)

TRL for supervised fine-tuning

Colab and CUDA for GPU-based training

📁 Dataset
Custom dataset of legal conversations in JSONL format with the structure:

json
Copy
Edit
{
  "conversations": [
    {"role": "user", "content": "What is civil law?"},
    {"role": "assistant", "content": "Civil law deals with disputes between individuals..."}
  ]
}
🛠️ Setup Instructions
Install dependencies:

bash
Copy
Edit
pip install unsloth transformers trl chromadb sentence-transformers
Fine-tune the model:

python
Copy
Edit
# See `Finetuning_Llama.ipynb` for complete code
Run the RAG pipeline:

python
Copy
Edit
# Launch script and input query when prompted
rag_generate_with_llama()
📸 Example Usage
Input:

pgsql
Copy
Edit
Enter your legal query: What is the difference between civil and criminal law?
Output:

csharp
Copy
Edit
📄 Final Answer:
Civil law is concerned with disputes between individuals or organizations, while criminal law deals with offenses against the state...
📦 Output
finetuned_model/ — directory containing the LoRA-adapted LLaMA weights

/content/Chroma_db/ — local persistent ChromaDB with indexed legal documents

🧠 Future Improvements
Add Streamlit or Gradio interface

Include document upload and automatic chunking

Extend to multilingual legal documents

📄 License
MIT License
