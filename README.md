<div align="center">

# Hey, I'm Anshuman

**B.Tech @ VIT Bhopal · Class of 2027 · Machine Learning & AI**

I care about the unglamorous middle part of ML — getting a model out of a notebook and into something that survives real data and real traffic. Outside of that, chess is enough of an obsession that I built an engine for it instead of just playing.

[![Portfolio](https://img.shields.io/badge/Portfolio-000000?style=for-the-badge&logo=render&logoColor=E63946)](https://anshumanj.onrender.com/)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/anshuman-pandey-a77940279/)
[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/AnshumanJ28)

</div>

> [!NOTE]
> **Currently learning:** AI Agents · Vector Databases · Advanced RAG Architectures

---

<div align="center">

`Build the mechanism, not the wrapper.`

**Chess engine?** No Stockfish — wrote the MCTS, the ResNet, the self-play loop.
**Neural net?** No PyTorch — wrote the forward/backward pass, the optimizer, the streaming trainer in C/C++.
**Resume scorer?** No LLM — wrote the parser, the trie, the ranker in C++.
**Agent?** No LangChain — wrote the ReAct loop, the tool schemas, the guardrails.

</div>

---

## Pinned Projects

| Project | Demo | Repo | Highlights |
|:---|:---:|:---:|:---|
| **Nocturne — NN Engine From Scratch** | [Demo](https://nn-trainer.onrender.com/) | [Repo](https://github.com/AnshumanJ28/Nocturne) | Full neural net engine in C/C++ — forward/backward prop, SGD, Xavier/He init, zero ML frameworks. Exposed via pybind11 + Flask SSE streaming, with a live weight editor. |
| **LLM Agent From Scratch** | [Demo](https://llm-agent-tez2.onrender.com) | [Repo](https://github.com/AnshumanJ28/LLM-agent) | Hand-rolled ReAct loop, no LangChain/LangGraph/CrewAI. Auto-generated tool schemas, task memory, Docker-sandboxed code exec, JSONL tracing, 4/4 eval suite passing. |
| **Chess Engine — AlphaZ0** | [Demo](https://alphaz0.onrender.com) | [Repo](https://github.com/AnshumanJ28/AlphaZ0) | Full rules engine, no Stockfish. 10-ResBlock policy/value network, MCTS with UCB + Dirichlet noise, self-play (A3C) training loop. |
| **chalk — Calculus Engine From Scratch** | [Demo](https://chalk-z9gs.onrender.com/) | [Repo](https://github.com/AnshumanJ28/chalk) | Hand-written C++17 calculus engine — differentiation, symbolic integration, limits, equation solving. No SymPy, no Wolfram. Exposed to a Flask web app via pybind11. |
| **TalentMatch AI v2** | [Demo](https://talentmatch-ai-jwqd.onrender.com/) | [Repo](https://github.com/AnshumanJ28/talentmatch-ai) | Resume/JD match scorer rebuilt fully native in C++ — no LLM, no API key. Aho-Corasick skill trie, BM25 retrieval, ~85-feature XGBoost ranker, rule-based explanations. |
| **Hybrid Chatbot — No LLM** | [Demo](https://chatbothybrid-1.onrender.com/) | [Repo](https://github.com/AnshumanJ28/ChatBothybrid) | Deterministic conversational engine: hand-written LSTM + attention pooling in C++ (pybind11), intent router, slot-filling flow engine, KB cosine search. |
| **MLOps Demand Forecasting** | — | [Repo](https://github.com/AnshumanJ28/mlops-demand-forecasting) | End-to-end spatio-temporal demand pipeline: DVC data versioning, LightGBM + MLflow, FastAPI serving, Evidently drift monitoring, CI on every push. |
| **RAG Document QA** | — | [Repo](https://github.com/AnshumanJ28/rag-document-qa) | Hybrid retrieval (FAISS + BM25, RRF fusion) over uploaded PDFs, Gemini Flash generation with page-level [n] citations, groundedness scoring, offline CI. |

---

## Other Builds

| Project | What it is |
|:---|:---|
| **[nninfer-c](https://github.com/AnshumanJ28/nninfer-c)** | Minimal C11 neural net inference engine — custom binary format, adversarial-input-safe loader, cache-blocked/threaded matmul with real before/after benchmarks |
| **[threadpool](https://github.com/AnshumanJ28/threadpool)** | Two C thread-pool schedulers — single-queue vs. work-stealing — verified with ThreadSanitizer/ASan, real throughput benchmarks |
| **[YoLo8](https://github.com/AnshumanJ28/YoLo8)** | Real-time detection + multi-object tracking with persistent IDs, annotated video export, Gradio interface, MLflow experiment tracking |
| **[recsys-ab-testing](https://github.com/AnshumanJ28/recsys-ab-testing)** | ALS recommender with a real evaluation layer — MD5-hashed bucketing, two-proportion z-test with power analysis, Streamlit dashboard, FastAPI serving |
| **[federated-learning-sim](https://github.com/AnshumanJ28/federated-learning-sim)** | Privacy-preserving FedAvg simulation (Flower + PyTorch) vs. centralized training, IID/non-IID splits, client dropout, optional Opacus differential privacy, Dockerized API |
| **[rag-document-chatbot](https://github.com/AnshumanJ28/rag-document-chatbot)** | MMR retrieval + cross-encoder re-ranking, Groq Llama 3.1 generation, MLflow-tracked queries, Gradio chat UI |
| **[NexusTwin](https://github.com/AnshumanJ28/NexusTwin)** | AI digital twin for smart building energy monitoring — simulated sensors, anomaly detection, forecasting, optimization recommendations |
| **[Diabatic-B5](https://github.com/AnshumanJ28/Diabatic-B5)** | Retinal disease classification with EfficientNet-B5, trained on APTOS 2019, tested for generalization on RFMiD |

---

## Tech Stack

| Category | Technologies |
|:---|:---|
| **Languages** | ![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white) ![C](https://img.shields.io/badge/C-00599C?style=for-the-badge&logo=c&logoColor=white) ![C++](https://img.shields.io/badge/C++17-00599C?style=for-the-badge&logo=cplusplus&logoColor=white) ![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white) |
| **ML / DL / LLM & RAG** | ![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white) ![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white) ![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white) ![XGBoost](https://img.shields.io/badge/XGBoost-006ACC?style=for-the-badge&logo=python&logoColor=white) ![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white) ![YOLOv8](https://img.shields.io/badge/YOLOv8-111F68?style=for-the-badge&logo=yolo&logoColor=white) ![FAISS](https://img.shields.io/badge/FAISS-0064C8?style=for-the-badge&logo=meta&logoColor=white) ![Gemini](https://img.shields.io/badge/Gemini-8E75B2?style=for-the-badge&logo=googlegemini&logoColor=white) ![Groq](https://img.shields.io/badge/Groq-F55036?style=for-the-badge&logo=groq&logoColor=white) ![Hugging Face](https://img.shields.io/badge/Hugging_Face-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black) |
| **Systems & Native Performance** | ![pybind11](https://img.shields.io/badge/pybind11-EE4C2C?style=for-the-badge&logo=python&logoColor=white) ![CMake](https://img.shields.io/badge/CMake-064F8C?style=for-the-badge&logo=cmake&logoColor=white) |
| **MLOps & Deployment** | ![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white) ![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white) ![MLflow](https://img.shields.io/badge/MLflow-0194E2?style=for-the-badge&logo=mlflow&logoColor=white) ![DVC](https://img.shields.io/badge/DVC-945DD6?style=for-the-badge&logo=dvc&logoColor=white) ![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white) ![Render](https://img.shields.io/badge/Render-46E3B7?style=for-the-badge&logo=render&logoColor=white) ![Vercel](https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white) |
| **Tools** | ![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white) ![AWS](https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazon-aws&logoColor=white) ![Google Colab](https://img.shields.io/badge/Google_Colab-F9AB00?style=for-the-badge&logo=googlecolab&logoColor=white) ![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white) |

---

## GitHub Stats

<div align="center">
<img src="https://streak-stats.demolab.com/?user=AnshumanJ28&hide_border=true&background=000000&ring=E63946&fire=E63946&currStreakLabel=E63946&sideLabels=E8E8E8&currStreakNum=FFFFFF&sideNums=FFFFFF&dates=A0A0A0" width="49%" />
</div>

## LeetCode Stats

<div align="center">
<img src="https://leetcard.jacoblin.cool/Anshuman_Pandey28?theme=dark&font=baloo&ext=heatmap" width="49%" />
</div>

---

<div align="center">

Always up for talking ML, chess, or why your pipeline broke at 2am.

[![Portfolio](https://img.shields.io/badge/Portfolio-000000?style=for-the-badge&logo=render&logoColor=E63946)](https://anshumanj.onrender.com/)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/anshuman-pandey-a77940279/)
[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/AnshumanJ28)

</div>
