<div align="center">

# Hey, I'm Anshuman

portfolio : https://anshumanj.onrender.com/

B.Tech @ VIT Bhopal · Class of 2027 · Machine Learning & AI

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/anshuman-pandey-a77940279/)
[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/AnshumanJ28)

</div>

---

## A bit about me

I care about the unglamorous middle part of ML — getting a model out of a notebook and into something that survives real data and real traffic. Outside of that, chess is enough of an obsession that I built an engine for it instead of just playing.

**Currently learning:** AI Agents · Vector Databases · Advanced RAG architectures

---

## Pinned Projects

These are the ones I'd actually want you to look at first.

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

### Recommendation System with A/B Testing
An ALS-based recommender paired with a statistically rigorous A/B testing framework — the kind of evaluation layer most recsys portfolio projects skip entirely.

| Component | What it does |
|---|---|
| ALS model | Implicit-feedback matrix factorization for candidate recommendations |
| A/B assignment | Deterministic user bucketing via MD5 hashing, reproducible across runs |
| Significance testing | Two-proportion z-test with power analysis to validate uplift |
| Dashboard | Streamlit app for exploring results, served via Cloudflare Tunnel |
| `api/` | FastAPI serving layer for live recommendations |

[![View Repository](https://img.shields.io/badge/View_Repository-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/AnshumanJ28/recsys-ab-testing)

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

### YOLOv8 + ByteTrack Multi-Object Tracking
Real-time object detection and multi-object tracking pipeline. Detects objects frame-by-frame with YOLOv8, assigns persistent tracking IDs via ByteTrack, and exports an annotated video with bounding boxes, class labels, confidence scores, and track IDs.

| Component | What it does |
|---|---|
| YOLOv8 detection | Frame-level object detection with Ultralytics YOLOv8 |
| ByteTrack | Multi-object tracking with persistent IDs across frames |
| Annotation | Bounding boxes, class labels, confidence scores, track IDs burned into output video |
| Gradio interface | Interactive testing without touching code |
| MLflow | Experiment tracking integration |

**Pipeline:** Input Video → YOLOv8 Detection → ByteTrack Tracking → Annotated Output Video
**Applications:** traffic monitoring, smart surveillance, sports analytics, crowd monitoring, retail analytics

[![View Repository](https://img.shields.io/badge/View_Repository-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/AnshumanJ28/YoLo8)

---

### Chess Engine with AlphaZero-style AI
This is the one closest to my heart. A complete chess engine and AI, built from the ground up in Python — no Stockfish wrappers. A full rules engine, a custom residual network, and a self-play MCTS training loop inspired by DeepMind's AlphaZero.

| Component | What it does |
|---|---|
| `chesseng.py` | Full rules engine: move generation, castling, en passant, promotions, check/mate |
| `NeuralNet.py` | 10-ResBlock network with policy head (move probabilities) + value head (position eval) |
| `mcts.py` | MCTS with UCB scoring, Dirichlet noise for exploration, and value backup |
| `BoardEncoder.py` | 18-plane tensor encoding of full board state |
| `Train.py` | Self-play training loop |

[![View Repository](https://img.shields.io/badge/View_Repository-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/AnshumanJ28/AlphaZ0)

---

## Other builds

A few more things I've shipped, worth a quick look if you're curious:

- **[Diabatic-B5](https://github.com/AnshumanJ28/Diabatic-B5)** — Retinal disease classification with EfficientNet-B5, trained on APTOS 2019 and tested for generalization on RFMiD.

---

## Tech Stack

**Languages**

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![C](https://img.shields.io/badge/C-00599C?style=for-the-badge&logo=c&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=cplusplus&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![HTML](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/CSS-1572B6?style=for-the-badge&logo=css3&logoColor=white)

**ML / Data Science**

![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![LightGBM](https://img.shields.io/badge/LightGBM-9ACD32?style=for-the-badge&logo=python&logoColor=white)
![SciPy](https://img.shields.io/badge/SciPy-8CAAE6?style=for-the-badge&logo=scipy&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white)
![Keras](https://img.shields.io/badge/Keras-D00000?style=for-the-badge&logo=keras&logoColor=white)
![timm](https://img.shields.io/badge/timm-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![Ultralytics YOLO](https://img.shields.io/badge/YOLOv8-111F68?style=for-the-badge&logo=yolo&logoColor=white)
![Plotly](https://img.shields.io/badge/Plotly-3F4F75?style=for-the-badge&logo=plotly&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-4C72B0?style=for-the-badge&logo=python&logoColor=white)

**LLM & RAG**

![LangChain](https://img.shields.io/badge/LangChain-121212?style=for-the-badge&logo=chainlink&logoColor=white)
![FAISS](https://img.shields.io/badge/FAISS-0064C8?style=for-the-badge&logo=meta&logoColor=white)
![Google Gemini](https://img.shields.io/badge/Gemini-8E75B2?style=for-the-badge&logo=googlegemini&logoColor=white)
![Groq](https://img.shields.io/badge/Groq-F55036?style=for-the-badge&logo=groq&logoColor=white)
![Hugging Face](https://img.shields.io/badge/Hugging_Face-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black)

**MLOps & Deployment**

![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white)
![Gradio](https://img.shields.io/badge/Gradio-FF7C00?style=for-the-badge&logo=gradio&logoColor=white)
![MLflow](https://img.shields.io/badge/MLflow-0194E2?style=for-the-badge&logo=mlflow&logoColor=white)
![DVC](https://img.shields.io/badge/DVC-945DD6?style=for-the-badge&logo=dvc&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white)
![Evidently AI](https://img.shields.io/badge/Evidently_AI-FF6B35?style=for-the-badge&logo=python&logoColor=white)
![Render](https://img.shields.io/badge/Render-46E3B7?style=for-the-badge&logo=render&logoColor=white)
![Cloudflare](https://img.shields.io/badge/Cloudflare_Tunnel-F38020?style=for-the-badge&logo=cloudflare&logoColor=white)

**Tools & Platforms**

![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazon-aws&logoColor=white)
![Google Colab](https://img.shields.io/badge/Google_Colab-F9AB00?style=for-the-badge&logo=googlecolab&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![N8N](https://img.shields.io/badge/N8N-EA4B71?style=for-the-badge&logo=n8n&logoColor=white)
![Excel](https://img.shields.io/badge/Microsoft_Excel-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white)
![Fusion 360](https://img.shields.io/badge/Fusion_360-0696D7?style=for-the-badge&logo=autodesk&logoColor=white)

---

## GitHub Stats

<div align="center">




![GitHub Streak](https://github-readme-streak-stats.herokuapp.com/?user=AnshumanJ28&theme=react)

</div>

---

<div align="center">

Always up for talking ML, chess, or why your pipeline broke at 2am.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/anshuman-pandey-a77940279/)
[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/AnshumanJ28)

</div>
