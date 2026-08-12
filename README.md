# Recommender System Challenge

A hybrid recommendation system developed for the Leiden University Recommender System Challenge.

The project explores multiple recommendation paradigms, including graph-based collaborative filtering, transformer-based sequential recommendation, co-visitation modeling, and hybrid rank fusion for next-item prediction.

---

## Features

- LightGCN
- Recency-aware LightGCN
- SASRec
- BERT4Rec
- Co-Visitation Recommendation
- Weighted Rank Fusion

---

## Dataset

The dataset consists of implicit user-item interactions and item metadata.

- 23,284 users
- 13,441 items
- 147,267 training interactions
- Evaluation metric: Recall@10

> The original dataset is provided by Leiden University and is therefore not included in this repository.

---

## Models

| Model | Public Score |
|--------|-------------:|
| Popularity | 0.01050 |
| LightGCN | 0.00942 |
| Recent LightGCN | 0.01084 |
| SASRec | 0.01021 |
| BERT4Rec | 0.01334 |
| Co-Visitation | 0.01236 |
| Hybrid Fusion | **0.01483** |

---

## Hybrid Pipeline

The final solution combines multiple recommendation signals.

```text
LightGCN
        \
         \
Co-Visitation -----> Rank Fusion -----> Top-10 Recommendation
         /
Popularity
```

---

## Repository Structure

```
.
├── notebook/
├── report/
├── README.md
├── requirements.txt
└── .gitignore
```

---

## Tech Stack

- Python
- PyTorch
- RecBole
- LightGCN
- SASRec
- BERT4Rec
- NumPy
- Pandas

---

## Future Improvements

- Refactor notebook into modular Python scripts
- Add training and inference pipelines
- Add Docker support
- Benchmark additional recommendation models

---

## Report

The complete project report is available in

```
report/RS_challenge.pdf
```