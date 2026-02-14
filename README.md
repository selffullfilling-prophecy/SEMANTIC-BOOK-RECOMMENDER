# Semantic Book Recommender

A lightweight **semantic book recommendation** app that retrieves similar books from a **vector database (ChromaDB)** using **sentence embeddings**, then optionally refines results by **category** and **emotional tone**.

UI: **Gradio** gallery for fast, visual browsing of recommended covers + short captions.

---

## ✨ Features

- **Semantic search (vector similarity)** over book descriptions (not keyword matching) via ChromaDB + embeddings
- **Category filter** using `simple_categories`
- **Emotion / tone sorting** (Happy, Surprising, Angry, Suspenseful, Sad) based on precomputed emotion scores
- **Local-first**: uses a persisted Chroma DB folder (`chroma_db/`) and CSV assets shipped with the repo

---

## 🧱 Project Structure

- `gradio_dashboard.py` — Gradio UI + retrieval logic (main entry)
- `chroma_db/` — persisted Chroma vector database
- `tagged_description.txt` — corpus used for vector search (ISBN + description)
- Data files:
  - `books_cleaned.csv`
  - `books_with_categories.csv`
  - `books_with_emotions.csv`
- Notebooks (optional, for rebuild/experiments):
  - `data-exploration.ipynb`
  - `text-classification.ipynb` (zero-shot category classification)
  - `sentiment-analysis.ipynb` (emotion scoring)
  - `vector-search.ipynb` (build/load Chroma vector DB)

---

## ✅ Prerequisites

- Python **3.9+** recommended
- `pip` (or `conda`)
- (Optional) CUDA GPU if you want to run the notebooks faster. The app itself can run on CPU.

---

## 🚀 Quickstart (venv)

### 1) Clone
```bash
git clone https://github.com/selffullfilling-prophecy/SEMANTIC-BOOK-RECOMMENDER.git
cd SEMANTIC-BOOK-RECOMMENDER
