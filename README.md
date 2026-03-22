# ml-llm-playground

A personal playground for exploring Machine Learning and Large Language Model (LLM) concepts. This repository contains hands-on Jupyter notebooks covering NLP fundamentals, Hugging Face tooling, and practical model fine-tuning.

---

## Repository Structure

```
ml-llm-playground/
├── bert-sentiment-analysis/
│   └── sentiment-analysis-with-bert-medium.ipynb
└── hugging-face-quick-guide/
    ├── 1.4-accessing-pretrained-models-in-hugging-face.ipynb
    ├── 2.6-tokenizer-fundamentals.ipynb
    ├── 2.7-working-with-models-in-transformers.ipynb
    ├── 2.8-creating-our-own-dataset-in-hugging-face.ipynb
    ├── 2.9-creating-our-own-tokenizer-in-hugging-face.ipynb
    └── 3.11-fine-tuning-bart-for-summarization.ipynb
```

---

## Notebooks

### BERT Sentiment Analysis

| Notebook                                    | Description                                                                                                                                                                                                                         |
| ------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `sentiment-analysis-with-bert-medium.ipynb` | Fine-tunes BERT on the Twitter Airline Sentiment dataset for 3-class sentiment classification (positive / neutral / negative). Covers data loading from Kaggle, text preprocessing with spaCy and NLTK, and PyTorch-based training. |

**Key libraries:** `transformers`, `torch`, `spacy`, `nltk`, `scikit-learn`, `pandas`, `matplotlib`

---

### Hugging Face Quick Guide

A progressive series of notebooks walking through the core Hugging Face ecosystem.

| Notebook | Topic                              | Description                                                                                                                                      |
| -------- | ---------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------ |
| `1.4`    | Accessing Pre-trained Models       | Load GPT-2 from the Hub and run text generation using both the pipeline API and direct model access (greedy decoding, batch generation).         |
| `2.6`    | Tokenizer Fundamentals             | Deep-dive into the tokenization pipeline with DistilBERT — padding, truncation, attention masks, token IDs, and decoding.                        |
| `2.7`    | Working with Models                | Compare high-level pipeline abstractions (sentiment analysis, text generation) with low-level model inference, including GPU setup.              |
| `2.8`    | Creating Datasets                  | Load datasets from Hugging Face Hub (`datasets`), explore, shuffle, split, and build custom datasets from external sources (Reuters articles).   |
| `2.9`    | Custom Tokenizer Training          | Fine-tune a GPT-2 tokenizer on Reuters articles, building a domain-specific vocabulary (52K tokens) and comparing tokenization before and after. |
| `3.11`   | Fine-tuning BART for Summarization | Fine-tune BART on the SAMSum dialogue summarization dataset for abstractive summarization. Covers dataset prep and GPU training setup.           |

**Key libraries:** `transformers`, `datasets`, `torch`, `huggingface_hub`

---

## Setup

This project uses [uv](https://github.com/astral-sh/uv) and requires Python ≥ 3.12.

```bash
# Install dependencies
uv sync

# Launch Jupyter
jupyter lab
```

Individual notebooks may require additional packages (e.g., `spacy`, `nltk`, `kaggle`). Install them as needed via `pip` or `uv add`.

---

## Goals

- Build intuition for transformer-based NLP models
- Get hands-on experience with the Hugging Face ecosystem (`transformers`, `datasets`, `tokenizers`)
- Practice fine-tuning pre-trained models for downstream tasks
