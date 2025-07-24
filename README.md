---

# 🧾 TaxMate – RAG-based Tax Law Query Bot

![License](https://img.shields.io/badge/license-MIT-green)  
![Python](https://img.shields.io/badge/python-3.10-blue)  
![LLM](https://img.shields.io/badge/LLM-LLaMA_2_7B-orange)  
![Status](https://img.shields.io/badge/status-Active-brightgreen)

[![Deployed](https://img.shields.io/badge/Live%20Demo-Click%20Here-brightgreen?style=for-the-badge)](https://taxmate-rag.streamlit.app/)

> 📚 A semantic legal assistant built with Retrieval-Augmented Generation (RAG) to simplify access to Indian tax law using open-source LLMs and modern NLP tools.

---

## 🚀 Features

- 🔍 **Semantic Retrieval** using FAISS and MiniLM-SBERT embeddings
- 🔁 **Reranking with Cohere** for improved context precision
- 🧠 **Local Answer Generation** using Meta’s LLaMA 2–7B
- 📊 **Model Evaluation** using BLEU, ROUGE, METEOR, BERTScore, and QuESTEval
- 💡 **User-Controlled Temperature** for tuning creativity
- 🖥️ Built with **Streamlit** for an interactive chat UI

---

## 📌 Technologies Used

| Component | Tool/Library |
|----------|---------------|
| Embeddings | `all-MiniLM-L6-v2` (SBERT) |
| Vector Store | FAISS |
| Reranker | Cohere Rerank API |
| LLM | LLaMA 2–7B (4-bit quantized, local) |
| Frontend | Streamlit |
| Evaluation | BLEU, ROUGE, METEOR, BERTScore, QuESTEval |

---

## ⚙️ Installation

```bash
git clone https://github.com/akasha456/TaxMate.git
cd TaxMate
pip install -r requirements.txt
```

---

## 🧠 How It Works

```mermaid
flowchart TD
    Start([Start])
    A[Step 1: Input Collection]
    A1[Collect PAN, Aadhaar, Employer Details]
    A2[Collect Income Details (Form 16, Bank, Freelance)]
    A3[Collect Deduction Proofs (80C, Rent, Loans)]
    A4[Collect Capital Gains Info]
    A5[Collect Special Status (HUF, Senior Citizen)]

    B[Step 2: Backend Processing]
    B1[Categorize Income and Deductions]
    B2[Select ITR Form via Decision Tree]
    B3[Compute Taxes under Both Regimes]
    B4[Suggest Best Regime]
    B5[Check for Errors]
    B6[Generate Checklist]

    C[Step 3: Output Generation]
    C1[Display Tax Summary and Compare Regimes]
    C2[Generate JSON (ITD schema)]
    C3[Generate PDF Report]
    C4[Optional Excel Sheet]

    D[Step 4: Submission Preparation]
    D1[Login via OTP/Token]
    D2[API Integration or Manual Upload]
    D3[Track Submission Status]

    End([End])

    Start --> A --> A1 --> A2 --> A3 --> A4 --> A5 --> B
    B --> B1 --> B2 --> B3 --> B4 --> B5 --> B6 --> C
    C --> C1 --> C2 --> C3 --> C4 --> D
    D --> D1 --> D2 --> D3 --> End
```

---

## 📊 Model Evaluation Snapshot

| Model | BLEU | METEOR | ROUGE-1 | BERTScore F1 |
|-------|------|--------|---------|---------------|
| **Mistral AI** | 13.97 | 39.99 | 49.19 | 89.16 |
| **LLaMA 2–7B** | 7.98 | 41.83 | 36.83 | 87.06 |

---

## 📈 Embedding Model Comparison

| Model | Cosine MRR | Recall@5 |
|-------|-------------|-----------|
| MiniLM-SBERT | **1.0000** | **1.0000** |
| BERT | 0.8333 | 1.0000 |
| RoBERTa | 0.7500 | 1.0000 |

---

## 🌐 Future Enhancements

- 🧑‍⚖️ Expand to other domains like **GST** or **Labor Law**
- 📲 Web + Mobile deployment
- 🔔 Integrate real-time updates from government portals
- 🗣️ Voice input/output for accessibility
- 🤖 Fine-tuned LLM on Indian legal corpus

---

## 📜 License

This project is licensed under the MIT License.

---

## 💬 Acknowledgements

- [Meta AI](https://ai.meta.com/llama) for LLaMA 2  
- [Cohere](https://cohere.com) for reranking API  
- [SentenceTransformers](https://www.sbert.net) for embeddings  
- [Streamlit](https://streamlit.io) for the frontend

---


## Screenshots

[![Chatbot-Demo.jpg](https://i.postimg.cc/0NKJh9G5/Whats-App-Image-2025-04-23-at-09-56-12-153edaa2.jpg)](https://postimg.cc/Y4k9WKyT)

