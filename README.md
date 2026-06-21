<div align="center">

# Anshuman Pandey

B.Tech @ VIT Bhopal · Class of 2027 · Machine Learning & AI

I care about building ML systems that actually ship — not just experiments that live in notebooks.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/anshuman-pandey-a77940279/)
[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/AnshumanJ28)

</div>

---

## What I'm about

I'm drawn to the part of ML that most people skip — getting models out of Colab and into something that runs reliably. My projects tend to involve the full stack: data pipelines, training, serving, monitoring, and the CI/CD glue that holds it together.

Right now I'm deepening my work in RAG systems, agentic AI, and production MLOps. Outside of that, I find chess fascinating — enough to build an engine from scratch.

**Currently learning:** AI Agents · Vector Databases · Advanced RAG architectures

---

## Tech Stack

### Languages
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![C](https://img.shields.io/badge/C-00599C?style=for-the-badge&logo=c&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=cplusplus&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![HTML](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/CSS-1572B6?style=for-the-badge&logo=css3&logoColor=white)

### ML / Data Science
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![LightGBM](https://img.shields.io/badge/LightGBM-9ACD32?style=for-the-badge&logo=python&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white)
![Keras](https://img.shields.io/badge/Keras-D00000?style=for-the-badge&logo=keras&logoColor=white)
![timm](https://img.shields.io/badge/timm-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![FAISS](https://img.shields.io/badge/FAISS-0064C8?style=for-the-badge&logo=meta&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-121212?style=for-the-badge&logo=chainlink&logoColor=white)
![Plotly](https://img.shields.io/badge/Plotly-3F4F75?style=for-the-badge&logo=plotly&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-4C72B0?style=for-the-badge&logo=python&logoColor=white)

### MLOps & Deployment
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white)
![MLflow](https://img.shields.io/badge/MLflow-0194E2?style=for-the-badge&logo=mlflow&logoColor=white)
![DVC](https://img.shields.io/badge/DVC-945DD6?style=for-the-badge&logo=dvc&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white)
![Evidently AI](https://img.shields.io/badge/Evidently_AI-FF6B35?style=for-the-badge&logo=python&logoColor=white)

### Tools & Platforms
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazon-aws&logoColor=white)
![N8N](https://img.shields.io/badge/N8N-EA4B71?style=for-the-badge&logo=n8n&logoColor=white)
![Excel](https://img.shields.io/badge/Microsoft_Excel-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white)
![Fusion 360](https://img.shields.io/badge/Fusion_360-0696D7?style=for-the-badge&logo=autodesk&logoColor=white)

---

## Projects

### MLOps Demand Forecasting Pipeline
End-to-end MLOps pipeline for spatio-temporal traffic demand forecasting — data versioning, feature engineering, model training, API serving, and automated drift monitoring, all wired together with production tooling.

| Component | What it does |
|---|---|
| `src/features.py` | Geohash encoding, rush-hour flags, cyclical sine/cosine hour features |
| `src/train.py` | LightGBM training with RMSE, MAE, R² tracked on MLflow + DagsHub |
| `src/monitor.py` | Automated data drift detection with Evidently AI |
| `api/app.py` | FastAPI endpoint for real-time demand predictions |
| `ci.yml` | GitHub Actions CI running tests on every push |
| Storage | DVC + Google Drive remote, Docker containerized |

[![View Repository](https://img.shields.io/badge/View_Repository-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/AnshumanJ28/mlops-demand-forecasting)

---

### RAG Document QA — Hybrid Retrieval with Citations
Upload a PDF or text document, ask questions in plain English, and get answers grounded in the document with page-level source citations. Built with hybrid retrieval and a lightweight evaluation framework — no paid APIs beyond Gemini's free tier.

| Component | What it does |
|---|---|
| `src/ingest.py` | PyMuPDF extraction + chunking with overlap; page numbers preserved per chunk |
| `src/retriever.py` | FAISS vector search + BM25 fused with Reciprocal Rank Fusion |
| `src/generator.py` | Numbered [n] citations mapped back to source chunks via Gemini Flash |
| `src/evaluate.py` | Groundedness scoring via cosine similarity — no second LLM call needed |
| `api/` + `app/` | FastAPI backend + Streamlit frontend |
| `tests/` + CI | pytest with deterministic fake embeddings; CI runs fully offline |

[![View Repository](https://img.shields.io/badge/View_Repository-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/AnshumanJ28/rag-document-qa)

---

### Chess Engine with AlphaZero-style AI
A complete chess engine and AI, built from the ground up in Python. No Stockfish wrappers — a full rules engine, a custom residual network, and a self-play MCTS training loop inspired by DeepMind's AlphaZero.

| Component | What it does |
|---|---|
| `chesseng.py` | Full rules engine: move generation, castling, en passant, promotions, check/mate |
| `NeuralNet.py` | 10-ResBlock network with policy head (move probabilities) + value head (position eval) |
| `mcts.py` | MCTS with UCB scoring, Dirichlet noise for exploration, and value backup |
| `BoardEncoder.py` | 18-plane tensor encoding of full board state |
| `Train.py` | Self-play training loop |

[![View Repository](https://img.shields.io/badge/View_Repository-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/AnshumanJ28/AlphaZ0)

---

### Diabatic-B5 — Retinal Disease Classification
Binary classification of retinal diseases from fundus images using EfficientNet-B5. Trained on APTOS 2019, tested for generalization on RFMiD. Strong ROC-AUC achieved with a two-phase fine-tuning strategy.

[![View Repository](https://img.shields.io/badge/View_Repository-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/AnshumanJ28/Diabatic-B5)

---

## GitHub Stats

<div align="center">

![AnshumanJ28's GitHub Stats](https://github-readme-stats.vercel.app/api?username=AnshumanJ28&show_icons=true&theme=react&include_all_commits=true&count_private=true)
![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=AnshumanJ28&layout=compact&langs_count=8&theme=react)

![GitHub Streak](https://github-readme-streak-stats.herokuapp.com/?user=AnshumanJ28&theme=react)

</div>

---

<div align="center">

Feel free to explore the repos or connect.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/anshuman-pandey-a77940279/)
[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/AnshumanJ28)

</div>
