<div align="center">

# Hey, I'm Anshuman

**B.Tech @ VIT Bhopal · Class of 2027 · Machine Learning & AI**

I care about the unglamorous middle part of ML — getting a model out of a notebook and into something that survives real data and real traffic. Outside of that, chess is enough of an obsession that I built an engine for it instead of just playing.

[![Portfolio](https://img.shields.io/badge/Portfolio-0A1930?style=for-the-badge&logo=vercel&logoColor=D4AF37)](https://anshumanj.onrender.com/)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/anshuman-pandey-a77940279/)
[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/AnshumanJ28)

</div>

> [!NOTE]
> **Currently learning:** AI Agents · Vector Databases · Advanced RAG Architectures

---

<div align="center">

`Build the mechanism, not the wrapper.`

**Chess engine?** No Stockfish — wrote the MCTS, the ResNet, the self-play loop.
**Resume scorer?** No LLM — wrote the parser, the trie, the ranker in C++.
**Agent?** No LangChain — wrote the ReAct loop, the tool schemas, the guardrails.

</div>

---

## Pinned Projects

These are the ones I'd actually want you to look at first.

---

### LLM Agent From Scratch

A tool-using ReAct (Reason + Act) agent built **without any agent framework** — no LangChain, no LangGraph, no CrewAI. Everything an off-the-shelf framework would normally hand you is hand-rolled here instead, to prove out a real understanding of agent internals rather than framework glue.

```mermaid
flowchart LR
    A["Task"] --> B["LLM: Reason"]
    B --> C{"Action?"}
    C -->|"Yes"| D["Call Tool"]
    D --> E["Observe"]
    E --> B
    C -->|"No"| F["Final Answer"]

    style A fill:#16213e,stroke:#e94560,stroke-width:2px,color:#eee
    style B fill:#16213e,stroke:#58a6ff,stroke-width:2px,color:#eee
    style C fill:#16213e,stroke:#d29922,stroke-width:2px,color:#eee
    style D fill:#16213e,stroke:#3fb950,stroke-width:2px,color:#eee
    style E fill:#16213e,stroke:#bc8cff,stroke-width:2px,color:#eee
    style F fill:#16213e,stroke:#e94560,stroke-width:2px,color:#eee
```

| Component | What it does |
|:---|:---|
| Reasoning loop | Hand-rolled ReAct loop — no LangChain/LangGraph/CrewAI |
| Tool schemas | Auto-generated tool-calling schemas from function signatures |
| Memory | Conversation and task-state memory |
| Eval harness | 4/4 eval suite passing, 12 unit tests passing |
| Guardrails | Input/output guardrails around tool use |
| Sandboxed execution | Isolated Docker container for the agent's code-execution tool |
| Tracing | Full JSONL execution tracing for debugging agent runs |

[![Live Demo](https://img.shields.io/badge/Live_Demo-success?style=for-the-badge&logo=render&logoColor=white)](https://llm-agent-tez2.onrender.com)
[![View Repository](https://img.shields.io/badge/View_Repository-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/AnshumanJ28/LLM-agent)

---

### Chess Engine with AlphaZero-style AI

This is the one closest to my heart. A complete chess engine and AI, built from the ground up in Python — no Stockfish wrappers. A full rules engine, a custom residual network, and a self-play MCTS training loop inspired by DeepMind's AlphaZero.

```mermaid
flowchart LR
    A["Board State"] --> B["18-plane<br/>Tensor"]
    B --> C["10 ResBlocks"]
    C --> D["Policy Head<br/>Move Probs"]
    C --> E["Value Head<br/>Win Prob"]
    D & E --> F["MCTS<br/>Search"]
    F --> G["Best Move"]

    style A fill:#16213e,stroke:#58a6ff,stroke-width:2px,color:#eee
    style B fill:#16213e,stroke:#8b949e,stroke-width:2px,color:#eee
    style C fill:#16213e,stroke:#533483,stroke-width:2px,color:#eee
    style D fill:#16213e,stroke:#3fb950,stroke-width:2px,color:#eee
    style E fill:#16213e,stroke:#d29922,stroke-width:2px,color:#eee
    style F fill:#16213e,stroke:#e94560,stroke-width:2px,color:#eee
    style G fill:#16213e,stroke:#58a6ff,stroke-width:2px,color:#eee
```

| Component | What it does |
|:---|:---|
| `chesseng.py` | Full rules engine: move generation, castling, en passant, promotions, check/mate |
| `NeuralNet.py` | 10-ResBlock network with policy head (move probabilities) + value head (position eval) |
| `mcts.py` | MCTS with UCB scoring, Dirichlet noise for exploration, and value backup |
| `BoardEncoder.py` | 18-plane tensor encoding of full board state |
| `Train.py` | Self-play training loop (A3C) |

[![Live Demo](https://img.shields.io/badge/Live_Demo-success?style=for-the-badge&logo=render&logoColor=white)](https://alphaz0.onrender.com)
[![View Repository](https://img.shields.io/badge/View_Repository-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/AnshumanJ28/AlphaZ0)

---

### MLOps Demand Forecasting Pipeline

End-to-end MLOps pipeline for spatio-temporal traffic demand forecasting — data versioning, feature engineering, model training, API serving, and automated drift monitoring, all wired together with production tooling.

```mermaid
flowchart LR
    A["Raw Data<br/>(DVC)"] --> B["Feature<br/>Pipeline"]
    B --> C["LightGBM<br/>+ MLflow"]
    C --> D["FastAPI<br/>/predict"]
    D --> E["Evidently<br/>Drift Monitor"]

    style A fill:#16213e,stroke:#58a6ff,stroke-width:2px,color:#eee
    style B fill:#16213e,stroke:#3fb950,stroke-width:2px,color:#eee
    style C fill:#16213e,stroke:#d29922,stroke-width:2px,color:#eee
    style D fill:#16213e,stroke:#e94560,stroke-width:2px,color:#eee
    style E fill:#16213e,stroke:#bc8cff,stroke-width:2px,color:#eee
```

| Component | What it does |
|:---|:---|
| `src/features.py` | Geohash encoding, rush-hour flags, cyclical sine/cosine hour features |
| `src/train.py` | LightGBM training with RMSE, MAE, R² tracked on MLflow + DagsHub |
| `src/monitor.py` | Automated data drift detection with Evidently AI |
| `api/app.py` | FastAPI endpoint for real-time demand predictions |
| `ci.yml` | GitHub Actions CI running tests on every push |
| Storage | DVC + Google Drive remote, Docker containerized |

[![View Repository](https://img.shields.io/badge/View_Repository-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/AnshumanJ28/mlops-demand-forecasting)

---

### TalentMatch AI v2

Resume / Job Description ATS match scorer — upload a resume PDF, paste a JD, and get a 0-100 match score with a matched/missing/partial skills breakdown and plain-English explanation of the strongest signals. v2 rebuilt the entire scoring path in native C++: **no LLM, no API key, fully deterministic.**

```mermaid
flowchart LR
    A["PDF Upload"] --> B["PyMuPDF<br/>Extract"]
    B --> C["MiniLM<br/>Embed"]
    C -->|"ctypes FFI"| D["C++ Engine<br/>~85 Features"]
    D --> E["XGBoost<br/>Score 0-100"]
    D --> F["Explanation<br/>Factors"]

    style A fill:#062f4f,stroke:#38bdf8,stroke-width:2px,color:#f8fafc
    style B fill:#1e1b4b,stroke:#818cf8,stroke-width:2px,color:#f8fafc
    style C fill:#1e1b4b,stroke:#818cf8,stroke-width:2px,color:#f8fafc
    style D fill:#062f4f,stroke:#34d399,stroke-width:2px,color:#f8fafc
    style E fill:#062f4f,stroke:#34d399,stroke-width:2px,color:#f8fafc
    style F fill:#062f4f,stroke:#34d399,stroke-width:2px,color:#f8fafc
```

| Component | What it does |
|:---|:---|
| `cpp_core/parser/` | Deterministic regex-based resume parser (dates, contact info, sections) — replaced the old Groq/LLM parsing step |
| `cpp_core/skills/` | Aho-Corasick trie + synonym matching against a canonical skill taxonomy |
| `cpp_core/retrieval/` | BM25 probabilistic text retrieval for semantic/keyword overlap |
| `cpp_core/features/` | ~85-feature engineering pipeline (education, experience, skills, semantic) |
| `cpp_core/ranking/` | XGBoost ranker with a deterministic linear-weight fallback |
| `cpp_core/explainability/` | Rule-based template explanations — no AI-generated narrative |
| `src/bridge.py` | ctypes FFI bridge — Python only extracts PDF text and generates embeddings, C++ does all scoring |
| `app.py` | Gradio UI; also ships a FastAPI backend, web frontend, and Chrome extension |

v1 → v2 was a full de-LLM-ification: Groq/`llama-3.3-70b` parsing, LLM skill extraction, the hardcoded 60/40 `HeuristicRanker`, and AI-generated narrative explanations were all replaced with deterministic native code. No `.env` file or API key required to run it.

[![Live Demo](https://img.shields.io/badge/Live_Demo-success?style=for-the-badge&logo=vercel&logoColor=white)](https://talentmatch-ai-o22y.vercel.app/)
[![View Repository](https://img.shields.io/badge/View_Repository-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/AnshumanJ28/talentmatch-ai)

---

### Hybrid C++/Python Chatbot (No LLM)

A conversational chatbot that reasons and responds **without any generative model** — no OpenAI, no Groq, no text generation of any kind. Responses are retrieved, computed, and composed deterministically via knowledge-base search, dialogue management, and hand-written neural components, with Python orchestrating and C++ doing the compute-heavy work.

```mermaid
flowchart LR
    A["User Input"] --> B["Intent<br/>Router"]
    B --> C["Small Talk"]
    B --> D["Flow Engine<br/>Slot Filling"]
    B --> E["KB Search<br/>Cosine Sim"]
    B --> F["Web Search<br/>Fallback"]
    C & D & E & F --> G["Template<br/>Composer"]
    G --> H["Response"]

    style A fill:#16213e,stroke:#58a6ff,stroke-width:2px,color:#eee
    style B fill:#16213e,stroke:#d29922,stroke-width:2px,color:#eee
    style C fill:#16213e,stroke:#3fb950,stroke-width:2px,color:#eee
    style D fill:#16213e,stroke:#3fb950,stroke-width:2px,color:#eee
    style E fill:#16213e,stroke:#3fb950,stroke-width:2px,color:#eee
    style F fill:#16213e,stroke:#8b949e,stroke-width:2px,color:#eee
    style G fill:#16213e,stroke:#bc8cff,stroke-width:2px,color:#eee
    style H fill:#16213e,stroke:#e94560,stroke-width:2px,color:#eee
```

| Component | What it does |
|:---|:---|
| `cpp/src/lstm_cell.cpp` | Hand-written LSTM cell implemented from scratch in C++ |
| `cpp/src/attention_pooling.cpp` | Custom attention-pooling layer for sequence representations |
| `cpp/src/embedding_search.cpp` | Fast cosine-similarity search over the knowledge base |
| `cpp/src/cognitive_engine.cpp` | Core native inference engine, exposed to Python via pybind11 |
| `orchestrator/router.py` | Intent router dispatching between small talk, flow engine, KB search, and web search |
| `orchestrator/flow_engine.py` | Multi-turn slot-filling conversation engine |
| `orchestrator/dialogue_state.py` | Conversation history and dialogue-state tracking |
| `orchestrator/composer.py` | Template + slot-filling response composition |
| `orchestrator/tool_dispatch/web_search.py` | Optional live web search fallback (Google Custom Search), offline by default |

Design principles: no LLMs, no generated text, fully deterministic, offline-first, with the embedding encoder swappable for a real model like `all-MiniLM-L6-v2` if desired.

[![Live Demo](https://img.shields.io/badge/Live_Demo-success?style=for-the-badge&logo=vercel&logoColor=white)](https://chatbothybrid-1.onrender.com/)
[![View Repository](https://img.shields.io/badge/View_Repository-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/AnshumanJ28/ChatBothybrid)

---

### RAG Document QA — Hybrid Retrieval with Citations

Upload a PDF or text document, ask questions in plain English, and get answers grounded in the document with page-level source citations. Built with hybrid retrieval and a lightweight evaluation framework — no paid APIs beyond Gemini's free tier.

```mermaid
flowchart LR
    A["PDF Upload"] --> B["PyMuPDF<br/>Chunk + Pages"]
    B --> C["FAISS Vector<br/>+ BM25 Keyword"]
    C -->|"RRF Fusion"| D["Top Chunks"]
    D --> E["Gemini Flash<br/>Generate + Cite"]
    E --> F["Answer with<br/>[n] Citations"]

    style A fill:#16213e,stroke:#58a6ff,stroke-width:2px,color:#eee
    style B fill:#16213e,stroke:#8b949e,stroke-width:2px,color:#eee
    style C fill:#16213e,stroke:#3fb950,stroke-width:2px,color:#eee
    style D fill:#16213e,stroke:#d29922,stroke-width:2px,color:#eee
    style E fill:#16213e,stroke:#bc8cff,stroke-width:2px,color:#eee
    style F fill:#16213e,stroke:#e94560,stroke-width:2px,color:#eee
```

| Component | What it does |
|:---|:---|
| `src/ingest.py` | PyMuPDF extraction + chunking with overlap; page numbers preserved per chunk |
| `src/retriever.py` | FAISS vector search + BM25 fused with Reciprocal Rank Fusion |
| `src/generator.py` | Numbered [n] citations mapped back to source chunks via Gemini Flash |
| `src/evaluate.py` | Groundedness scoring via cosine similarity — no second LLM call needed |
| `api/` + `app/` | FastAPI backend + Streamlit frontend |
| `tests/` + CI | pytest with deterministic fake embeddings; CI runs fully offline |

[![View Repository](https://img.shields.io/badge/View_Repository-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/AnshumanJ28/rag-document-qa)

---

### Recommendation System with A/B Testing

An ALS-based recommender paired with a statistically rigorous A/B testing framework — the kind of evaluation layer most recsys portfolio projects skip entirely.

```mermaid
flowchart LR
    A["User Request"] --> B["MD5 Hash<br/>Assignment"]
    B --> C["Control: ALS"]
    B --> D["Treatment:<br/>Content-Based"]
    C & D --> E["Log to<br/>SQLite"]
    E --> F["z-test<br/>Significance"]

    style A fill:#16213e,stroke:#58a6ff,stroke-width:2px,color:#eee
    style B fill:#16213e,stroke:#d29922,stroke-width:2px,color:#eee
    style C fill:#16213e,stroke:#3fb950,stroke-width:2px,color:#eee
    style D fill:#16213e,stroke:#bc8cff,stroke-width:2px,color:#eee
    style E fill:#16213e,stroke:#8b949e,stroke-width:2px,color:#eee
    style F fill:#16213e,stroke:#e94560,stroke-width:2px,color:#eee
```

| Component | What it does |
|:---|:---|
| ALS model | Implicit-feedback matrix factorization for candidate recommendations |
| A/B assignment | Deterministic user bucketing via MD5 hashing, reproducible across runs |
| Significance testing | Two-proportion z-test with power analysis to validate uplift |
| Dashboard | Streamlit app for exploring results, served via Cloudflare Tunnel |
| `api/` | FastAPI serving layer for live recommendations |

[![View Repository](https://img.shields.io/badge/View_Repository-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/AnshumanJ28/recsys-ab-testing)

---

### YOLOv8 + ByteTrack Multi-Object Tracking

Real-time object detection and multi-object tracking pipeline. Detects objects frame-by-frame with YOLOv8, assigns persistent tracking IDs via ByteTrack, and exports an annotated video with bounding boxes, class labels, confidence scores, and track IDs.

```mermaid
flowchart LR
    A["Input<br/>Video"] --> B["YOLOv8<br/>Detection"]
    B --> C["ByteTrack<br/>Tracking"]
    C --> D["Annotated<br/>Output"]

    style A fill:#16213e,stroke:#58a6ff,stroke-width:2px,color:#eee
    style B fill:#16213e,stroke:#3fb950,stroke-width:2px,color:#eee
    style C fill:#16213e,stroke:#d29922,stroke-width:2px,color:#eee
    style D fill:#16213e,stroke:#e94560,stroke-width:2px,color:#eee
```

| Component | What it does |
|:---|:---|
| YOLOv8 detection | Frame-level object detection with Ultralytics YOLOv8 |
| ByteTrack | Multi-object tracking with persistent IDs across frames |
| Annotation | Bounding boxes, class labels, confidence scores, track IDs burned into output video |
| Gradio interface | Interactive testing without touching code |
| MLflow | Experiment tracking integration |

**Applications:** traffic monitoring, smart surveillance, sports analytics, crowd monitoring, retail analytics

[![View Repository](https://img.shields.io/badge/View_Repository-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/AnshumanJ28/YoLo8)

---

## Other Builds

A few more things I've shipped, worth a quick look if you're curious:

| Project | What it is |
|:---|:---|
| **[federated-learning-sim](https://github.com/AnshumanJ28/federated-learning-sim)** | Privacy-preserving FedAvg simulation across virtual clients (Flower + PyTorch), benchmarked against centralized training on IID and non-IID splits, with client dropout modeling, an optional differential-privacy layer (Opacus), MLflow tracking, and a Dockerized serving API |
| **[rag-document-chatbot](https://github.com/AnshumanJ28/rag-document-chatbot)** | A second take on RAG: MMR retrieval + cross-encoder re-ranking, Groq's Llama 3.1 for generation, and MLflow-tracked queries in a Gradio chat UI |
| **[NexusTwin](https://github.com/AnshumanJ28/NexusTwin)** | AI digital twin for smart building energy monitoring: simulated live sensor data, anomaly detection, forecasting, and optimization recommendations |
| **[Diabatic-B5](https://github.com/AnshumanJ28/Diabatic-B5)** | Retinal disease classification with EfficientNet-B5, trained on APTOS 2019 and tested for generalization on RFMiD |

---

## Tech Stack

**Languages**

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![C](https://img.shields.io/badge/C-00599C?style=for-the-badge&logo=c&logoColor=white)
![C++](https://img.shields.io/badge/C++17-00599C?style=for-the-badge&logo=cplusplus&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![HTML](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/CSS-1572B6?style=for-the-badge&logo=css3&logoColor=white)

**ML / Deep Learning**

![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)
![Keras](https://img.shields.io/badge/Keras-D00000?style=for-the-badge&logo=keras&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![XGBoost](https://img.shields.io/badge/XGBoost-006ACC?style=for-the-badge&logo=python&logoColor=white)
![LightGBM](https://img.shields.io/badge/LightGBM-9ACD32?style=for-the-badge&logo=python&logoColor=white)
![SciPy](https://img.shields.io/badge/SciPy-8CAAE6?style=for-the-badge&logo=scipy&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white)
![timm](https://img.shields.io/badge/timm-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![Ultralytics YOLO](https://img.shields.io/badge/YOLOv8-111F68?style=for-the-badge&logo=yolo&logoColor=white)
![ByteTrack](https://img.shields.io/badge/ByteTrack-111F68?style=for-the-badge&logo=yolo&logoColor=white)
![Plotly](https://img.shields.io/badge/Plotly-3F4F75?style=for-the-badge&logo=plotly&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-4C72B0?style=for-the-badge&logo=python&logoColor=white)

**LLM, Agents & RAG**

![FAISS](https://img.shields.io/badge/FAISS-0064C8?style=for-the-badge&logo=meta&logoColor=white)
![Google Gemini](https://img.shields.io/badge/Gemini-8E75B2?style=for-the-badge&logo=googlegemini&logoColor=white)
![Groq](https://img.shields.io/badge/Groq-F55036?style=for-the-badge&logo=groq&logoColor=white)
![Hugging Face](https://img.shields.io/badge/Hugging_Face-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black)
![Sentence Transformers](https://img.shields.io/badge/Sentence--Transformers-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black)
![No-Framework Agents](https://img.shields.io/badge/Agents-No_Framework-2E8B57?style=for-the-badge&logo=OpenAI&logoColor=white)

**Systems & Native Performance**

![pybind11](https://img.shields.io/badge/pybind11-EE4C2C?style=for-the-badge&logo=python&logoColor=white)
![CMake](https://img.shields.io/badge/CMake-064F8C?style=for-the-badge&logo=cmake&logoColor=white)
![Make](https://img.shields.io/badge/Make-A42E2B?style=for-the-badge&logo=gnu&logoColor=white)
![Aho-Corasick](https://img.shields.io/badge/Aho--Corasick-34d399?style=for-the-badge&logo=cplusplus&logoColor=white)
![BM25](https://img.shields.io/badge/BM25-34d399?style=for-the-badge&logo=cplusplus&logoColor=white)
![MCTS](https://img.shields.io/badge/MCTS-34d399?style=for-the-badge&logo=cplusplus&logoColor=white)

**Document & NLP Processing**

![PyMuPDF](https://img.shields.io/badge/PyMuPDF-1E90FF?style=for-the-badge&logo=adobeacrobatreader&logoColor=white)
![EasyOCR](https://img.shields.io/badge/EasyOCR-2C3E50?style=for-the-badge&logo=python&logoColor=white)
![Pydantic](https://img.shields.io/badge/Pydantic-E92063?style=for-the-badge&logo=pydantic&logoColor=white)
![RapidFuzz](https://img.shields.io/badge/RapidFuzz-4B8BBE?style=for-the-badge&logo=python&logoColor=white)

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
![Vercel](https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white)
![Hugging Face Spaces](https://img.shields.io/badge/HF_Spaces-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black)
![Cloudflare](https://img.shields.io/badge/Cloudflare_Tunnel-F38020?style=for-the-badge&logo=cloudflare&logoColor=white)

**Federated & Privacy-Preserving ML**

![Flower](https://img.shields.io/badge/Flower-1F41BB?style=for-the-badge&logo=python&logoColor=white)
![Opacus](https://img.shields.io/badge/Opacus-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)

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
<img src="https://streak-stats.demolab.com/?user=AnshumanJ28&hide_border=true&background=1A2B6D&ring=C0C0C0&fire=C0C0C0&currStreakLabel=E8E8E8&sideLabels=E8E8E8&currStreakNum=FFFFFF&sideNums=FFFFFF&dates=8FA0C7" width="49%" />
</div>

## LeetCode Stats

<div align="center">
<img src="https://leetcard.jacoblin.cool/Anshuman_Pandey28?theme=dark&font=baloo&ext=heatmap" width="49%" />
</div>

---

<div align="center">

Always up for talking ML, chess, or why your pipeline broke at 2am.

[![Portfolio](https://img.shields.io/badge/Portfolio-0A1930?style=for-the-badge&logo=vercel&logoColor=D4AF37)](https://anshumanj.onrender.com/)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/anshuman-pandey-a77940279/)
[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/AnshumanJ28)

</div>
