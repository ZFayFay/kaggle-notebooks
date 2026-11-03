# Kaggle notebooks

Original analysis notebooks I publish on Kaggle. Each folder has the notebook and a short summary.
Profile: [kaggle.com/zfayfay](https://www.kaggle.com/zfayfay) · Work log: [LOG.md](LOG.md)

| Notebook | Question | Key result |
|---|---|---|
| [Where is the bug? File-finding methods compared](gemma4-where-is-the-bug/) | Which search method finds the file a bug fix must change? (Gemma 4 Developer Agent, 129 real Python tasks) | Hybrid search puts the right file in the top 5 for 68% of tasks; graph-node BM25 reaches 84% in the top 10 |
| [Synthetic vs original: does it help?](s6e11-fraud-synthetic-vs-original/) | Credit card fraud (Playground S6E11): how far is the generated data from the original, and do the original rows help? | Adversarial AUC 0.90 vs original; adding the 20k original rows does not help (CV AUC 0.9462 vs 0.9460) |
