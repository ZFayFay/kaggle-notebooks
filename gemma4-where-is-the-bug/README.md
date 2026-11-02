# Where is the bug? File-finding methods compared

**Kaggle:** https://www.kaggle.com/code/zfayfay/where-is-the-bug-file-finding-methods-compared
**Competition:** Google – The Gemma 4 Developer Agent Competition

Every coding agent starts the same way: read the issue, find the file to edit. The public tasks ship with the reference fix,
so we know which files a correct fix touches. This notebook measures, for 7 search methods, how often a correct file is in the top k.

| Method | R@1 | R@5 | R@10 | MRR |
|---|---|---|---|---|
| 1 Path match | 0.10 | 0.26 | 0.32 | 0.19 |
| 2 Grep identifiers | 0.27 | 0.46 | 0.58 | 0.37 |
| 3 BM25 on files | 0.29 | 0.60 | 0.71 | 0.43 |
| 4 BM25 on graph nodes | 0.33 | 0.65 | **0.84** | 0.47 |
| 5 Graph expansion | 0.33 | 0.63 | 0.83 | 0.47 |
| 6 Embedding expansion | 0.33 | 0.64 | **0.84** | 0.48 |
| 7 Hybrid (RRF) | 0.32 | **0.68** | 0.82 | **0.48** |

128 tasks scored (fastapi, rich, requests, httpx). CPU only, about 6 minutes.

Takeaways: give an agent the top 5 files, not the top 1; search functions/classes (graph nodes), not whole files;
the ~20 tasks missed even in the top 10 are a good hard set for testing an agent's exploration loop.
