# 🧠 Legal-RAG: AI-Powered Legal Query Assistant

A domain-specific **Retrieval-Augmented Generation (RAG)** system that uses a fine-tuned [LLaMA 3.2B](https://huggingface.co/unsloth/Llama-3.2-3B-Instruct) model to provide context-rich answers to legal queries. Built with Unsloth, ChromaDB, and MiniLM embeddings, this project is tailored for handling complex legal conversations and document retrieval.

## 🚀 Features

- 🔧 Fine-tuned LLaMA 3.2B with LoRA on legal case conversations using `unsloth`
- 📄 Context-aware question answering using ChromaDB and Sentence Transformers (MiniLM)
- 🧠 Retrieval-Augmented Generation pipeline that combines embedding-based retrieval with generative AI
- 💬 Chat-style prompt formatting with HuggingFace chat templates for cleaner responses

## 🏗️ Tech Stack

- `Transformers` (HuggingFace)
- `unsloth` for efficient fine-tuning
- `ChromaDB` for vector storage and retrieval
- `sentence-transformers` (MiniLM-L6-v2)
- `TRL` for supervised fine-tuning
- `Colab` and `CUDA` for GPU-based training

## 📁 Dataset

Custom dataset of legal conversations in JSONL format with the structure:
```json
{
  "conversations": [
    {"role": "user", "content": "What is civil law?"},
    {"role": "assistant", "content": "Civil law deals with disputes between individuals..."}
  ]
}
